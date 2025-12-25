# Database Tuning Reference Guide

> A comprehensive reference for analyzing database performance issues and optimizing existing databases, based on "Database Tuning: Principles, Experiments, and Troubleshooting Techniques" by Dennis Shasha and Philippe Bonnet

---

## Table of Contents

1. [Fundamental Principles](#1-fundamental-principles)
2. [Concurrency Control Tuning](#2-concurrency-control-tuning)
3. [Logging and Recovery](#3-logging-and-recovery)
4. [Operating System Considerations](#4-operating-system-considerations)
5. [Hardware and Storage Tuning](#5-hardware-and-storage-tuning)
6. [Index Tuning](#6-index-tuning)
7. [Query Optimization](#7-query-optimization)
8. [Common Performance Issues Checklist](#8-common-performance-issues-checklist)
9. [Troubleshooting Guide](#9-troubleshooting-guide)
10. [Quick Reference](#10-quick-reference)

---

## 1. Fundamental Principles

### The Five Basic Principles of Tuning

| Principle | Description |
|-----------|-------------|
| **Think Globally, Fix Locally** | Understand the whole system before optimizing specific parts |
| **Partitioning Breaks Bottlenecks** | Divide hot resources to reduce contention |
| **Start-up Costs Are High, Running Costs Are Low** | Batch operations when possible |
| **Render Unto Server What Is Due Unto Server** | Let the database do what it does best |
| **Be Prepared for Trade-offs** | Every optimization has costs |

### Performance Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| **Response Time** | Time to complete single operation | Application-dependent |
| **Throughput** | Operations per unit time | Maximize |
| **Hit Ratio** | Buffer cache hit rate | > 90% |
| **CPU Utilization** | Processor usage | 70-80% (not 100%) |
| **I/O Wait** | Time waiting for disk | Minimize |

### The Tuning Cycle

```
Monitor → Analyze → Hypothesize → Test → Implement → Monitor
```

---

## 2. Concurrency Control Tuning

### Transaction Isolation Levels

| Level | Dirty Read | Non-Repeatable Read | Phantom | Use Case |
|-------|------------|---------------------|---------|----------|
| **READ UNCOMMITTED** | Yes | Yes | Yes | Approximate counts |
| **READ COMMITTED** | No | Yes | Yes | Most OLTP (default) |
| **REPEATABLE READ** | No | No | Yes | Financial transactions |
| **SERIALIZABLE** | No | No | No | Critical consistency |

### Lock Granularity

| Granularity | Pros | Cons | Best For |
|-------------|------|------|----------|
| **Row Locks** | High concurrency | High overhead | Short transactions |
| **Page Locks** | Moderate overhead | Moderate blocking | Mixed workloads |
| **Table Locks** | Low overhead | High blocking | Batch operations |

### Tuning Guidelines

#### Long vs Short Transactions
```
Long transactions → Use TABLE locks (avoid deadlocks)
Short transactions → Use ROW locks (maximize concurrency)
```

#### Lock Escalation
- Set escalation threshold HIGH for online environments
- Monitor lock table size
- Avoid DDL during heavy transaction periods

### Avoiding Hot Spots

**Problem:** Single data item accessed/updated by many transactions

**Solutions:**

1. **Partition the hot spot**
   - Multiple insertion points for history tables
   - Use at least n/4 insertion points where n = max concurrent transactions

2. **Access hot spot LATE in transaction**
   - Minimizes lock hold time
   - Reduces blocking

3. **Use system facilities**
   - Oracle: SEQUENCES instead of counter tables
   - SQL Server: IDENTITY columns
   - Avoids locking overhead

### Deadlock Prevention

```sql
-- BAD: Different lock ordering
-- Thread 1: lock(A), lock(B)
-- Thread 2: lock(B), lock(A)

-- GOOD: Consistent lock ordering
-- Thread 1: lock(A), lock(B)
-- Thread 2: lock(A), lock(B)
```

**Rules:**
- Always acquire locks in the same order
- Keep transactions short
- Access hot spots last
- Use appropriate isolation level

---

## 3. Logging and Recovery

### Log Configuration

#### Critical Rule: Separate Log Disk
```
ALWAYS put log files on dedicated disk(s)
- Enables sequential writes
- No seeks = high throughput
- ~30% performance improvement
```

#### Group Commit
- Batches multiple transaction commits
- Reduces log disk writes
- Enable for high-transaction workloads
- Increase log buffer size for heavy loads

### Checkpoint Tuning

| Parameter | Impact | Recommendation |
|-----------|--------|----------------|
| **Checkpoint Interval** | Recovery time vs. online performance | 20 min for high availability |
| **Log File Size** | Checkpoint frequency | Size to avoid forced checkpoints |
| **Dirty Page Threshold** | Write frequency | Balance based on workload |

### Database Dumps

**Benefits:**
- Insurance against disk failure
- Source for data warehouse queries
- Point-in-time recovery

**Schedule:**
- High availability: Daily dumps
- Standard: Weekly dumps
- Always: Mirror the log

### Recovery Tuning Tips

1. **Separate log from database disks**
2. **Mirror the log** (RAID 1)
3. **Use group commit** for high transaction rates
4. **Set appropriate checkpoint intervals**
5. **Size log files to avoid forced checkpoints**

---

## 4. Operating System Considerations

### Buffer/Cache Configuration

#### Buffer Size Guidelines

```
Increase buffer until:
1. Hit ratio flattens out (diminishing returns)
2. OS paging begins (too large)

Target: > 90% hit ratio
```

#### Hit Ratio Calculation
```
Hit Ratio = (Logical Reads - Physical Reads) / Logical Reads
```

### Memory Economics (5-Minute Rule)

Keep a page in memory if accessed more frequently than every 5 minutes:
```
If (access_interval < 5 minutes) → Keep in RAM
If (access_interval > 5 minutes) → Keep on disk
```

### Multiprogramming Level

**Problem:** Too many concurrent connections = thrashing

**Solution:** Incremental steps method:
1. Start with low concurrency limit
2. Increase by 1, measure performance
3. Stop when performance degrades
4. First local maximum = optimal level

### Thread/Process Priorities

**Warning:** Priority inversion can occur!

```
Scenario:
- T1 (high priority) waits for lock held by T3 (low priority)
- T2 (medium priority) runs, blocking T3
- Result: T1 is indirectly blocked by T2
```

**Solution:** Give same priority to all database transactions

---

## 5. Hardware and Storage Tuning

### RAID Configuration

| RAID Level | Description | Best For |
|------------|-------------|----------|
| **RAID 0** | Striping only | Temp files, non-critical data |
| **RAID 1** | Mirroring | **Log files**, rollback segments |
| **RAID 5** | Parity striping | Read-heavy data/index files |
| **RAID 10** | Striped mirrors | High-performance, fault-tolerant |

#### RAID Selection Guide

```
Log Files        → RAID 1 (or RAID 10 for high volume)
Temp/Sort Files  → RAID 0
Data Files       → RAID 5 (read-heavy) or RAID 10 (write-heavy)
Index Files      → RAID 5 or RAID 10
```

### Stripe Size
```
Stripe size = Database page size (optimal)
```

### Controller Cache

| Mode | Description | Use When |
|------|-------------|----------|
| **Write-Through** | Writes go directly to disk | Heavy sustained writes |
| **Write-Back** | Writes cached, flushed later | Bursty write patterns |
| **Read-Ahead** | Prefetch sequential data | DB handles this better |

**Recommendation:** Let database handle read-ahead; use write-back cautiously

### Disk Layout

```
Disk 1: Log files (dedicated, mirrored)
Disk 2: System catalog, temp files
Disk 3: Data files
Disk 4: Index files (separate from data)
Disk 5+: Additional data partitions
```

### Capacity Planning

1. **Separate log from data** (always)
2. **Separate indexes from data** (write-intensive)
3. **Partition large tables** (read-intensive)
4. **Use RAID appropriately**
5. **Monitor disk utilization** (not just space)

---

## 6. Index Tuning

### Index Types

| Type | Best For | Avoid For |
|------|----------|-----------|
| **B-Tree** | Range queries, ordering, most cases | - |
| **Hash** | Point queries only | Range queries, ordering |
| **Bitmap** | Low cardinality, data warehouse | OLTP, frequent updates |

### Query Types and Index Effectiveness

| Query Type | B-Tree | Hash | Example |
|------------|--------|------|---------|
| Point | Good | Best | `WHERE id = 123` |
| Multipoint | Good | Good | `WHERE dept = 'HR'` |
| Range | Best | Useless | `WHERE salary > 50000` |
| Prefix Match | Best | Useless | `WHERE name LIKE 'Sm%'` |
| Ordering | Best | Useless | `ORDER BY date` |
| Extremal | Good | Useless | `MAX(salary)` |

### Clustering vs Non-Clustering

#### Clustering Index
- **One per table** (defines physical order)
- Sparse or dense (system-dependent)
- Best for multipoint and range queries
- Requires maintenance (reorganization)

#### Non-Clustering Index
- **Multiple per table**
- Always dense
- Best when covering the query
- Good for point queries

### When to Use Each Index Type

```
Clustering Index:
- Frequently used range queries
- Multipoint queries on low-cardinality columns
- ORDER BY queries
- Join columns with many duplicates

Non-Clustering Index:
- Point queries (unique lookups)
- Covering indexes
- Secondary access paths
- Multiple query patterns on same table
```

### Composite Index Guidelines

**Order attributes by:**
1. Equality conditions first
2. Most selective conditions first
3. Range conditions last

```sql
-- Index on (A, B, C) is good for:
WHERE A = 1                      -- Uses full prefix
WHERE A = 1 AND B = 2           -- Uses full prefix
WHERE A = 1 AND B = 2 AND C > 5 -- Uses all columns

-- Less effective for:
WHERE B = 2                      -- Skips A (partial use)
WHERE C = 5                      -- Skips A, B (minimal use)
```

### Index Maintenance

**Signs index needs maintenance:**
- Query performance degradation over time
- High number of page splits
- Large overflow chains
- Low page utilization

**Actions:**
- Reorganize/rebuild index
- Update statistics
- Consider dropping unused indexes

### Index Decision Matrix

| Scenario | Action |
|----------|--------|
| Point queries on unique column | Non-clustering index |
| Range queries | Clustering B-tree index |
| Multipoint queries (many matches) | Clustering index |
| Multipoint queries (few matches) | Non-clustering index |
| Covering query | Composite non-clustering index |
| Ordering/sorting | Clustering index on ORDER BY column |
| Join on foreign key | Index on foreign key column |

---

## 7. Query Optimization

### Join Strategies

| Strategy | Best When | Avoid When |
|----------|-----------|------------|
| **Nested Loop** | Small outer table, indexed inner | Large tables, no index |
| **Hash Join** | No useful indexes, equality join | Memory constrained |
| **Merge Join** | Both tables sorted on join key | Unsorted data |
| **Index Nested Loop** | Index exists on inner table | Large result sets |

### Query Writing Best Practices

#### Use Set-Based Operations
```sql
-- BAD: Row-by-row processing
DECLARE CURSOR FOR SELECT * FROM orders
WHILE (FETCH NEXT)
    UPDATE inventory SET qty = qty - @ordered_qty

-- GOOD: Set-based
UPDATE inventory i
SET qty = qty - (SELECT SUM(qty) FROM orders o WHERE o.item_id = i.id)
```

#### Avoid Functions on Indexed Columns
```sql
-- BAD: Function prevents index use
WHERE YEAR(order_date) = 2023

-- GOOD: Index can be used
WHERE order_date >= '2023-01-01' AND order_date < '2024-01-01'
```

#### Use EXISTS Instead of IN for Large Subqueries
```sql
-- Often slower
WHERE id IN (SELECT id FROM large_table WHERE condition)

-- Often faster
WHERE EXISTS (SELECT 1 FROM large_table WHERE large_table.id = outer.id AND condition)
```

### Query Execution Plan Analysis

**Look for:**
- Full table scans (unexpected)
- Index scans vs seeks
- Sort operations
- Hash operations (memory pressure)
- Estimated vs actual row counts

**Red Flags:**
- Table scan on large table
- Nested loop with large outer table
- Sort on large result set
- Hash join spilling to disk

---

## 8. Common Performance Issues Checklist

### Slow Queries

- [ ] Missing index on WHERE clause columns
- [ ] Missing index on JOIN columns
- [ ] Function on indexed column prevents index use
- [ ] Outdated statistics
- [ ] Inappropriate isolation level
- [ ] Full table scan when index should be used
- [ ] Too many indexes causing slow writes
- [ ] Index fragmentation

### Concurrency Issues

- [ ] Lock contention on hot tables
- [ ] Long-running transactions holding locks
- [ ] Deadlocks due to inconsistent lock ordering
- [ ] Lock escalation causing blocking
- [ ] Inappropriate isolation level
- [ ] DDL operations during peak hours

### I/O Bottlenecks

- [ ] Log and data on same disk
- [ ] Insufficient buffer/cache size
- [ ] No index on frequently queried columns
- [ ] Unpartitioned large tables
- [ ] RAID misconfiguration
- [ ] Controller cache misconfigured

### Memory Issues

- [ ] Buffer cache too small (low hit ratio)
- [ ] Buffer cache too large (OS paging)
- [ ] Memory-intensive queries (large sorts, hashes)
- [ ] Too many concurrent connections
- [ ] Memory leaks in connection pooling

### CPU Issues

- [ ] Too many concurrent users
- [ ] Inefficient queries (full scans)
- [ ] Excessive parsing (no prepared statements)
- [ ] Complex stored procedures
- [ ] Missing indexes causing sorts

---

## 9. Troubleshooting Guide

### Problem: Variable Response Times

**Possible Causes:**
1. DDL operations during online activity
2. Checkpoint/backup running
3. Lock contention
4. I/O contention

**Solutions:**
1. Schedule DDL/maintenance outside peak hours
2. Tune checkpoint frequency
3. Review transaction design
4. Separate disk resources

### Problem: Slow Insert Performance

**Possible Causes:**
1. Too many indexes on table
2. Sequential key causing page contention
3. Last page bottleneck
4. Trigger overhead

**Solutions:**
1. Review and remove unnecessary indexes
2. Use non-sequential keys or multiple insertion points
3. Use row locking
4. Optimize or remove triggers

### Problem: Join Query Taking Hours

**Possible Causes:**
1. Missing index on join column
2. Wrong join order
3. Cartesian product (missing join condition)
4. Outdated statistics

**Solutions:**
1. Add index on join columns
2. Use hints or rewrite query
3. Verify join conditions
4. Update statistics

### Problem: Database Running Out of Locks

**Possible Causes:**
1. Long transactions with many row locks
2. Lock escalation threshold too low
3. Lock table too small

**Solutions:**
1. Break long transactions into smaller ones
2. Increase escalation threshold
3. Increase lock table size
4. Use table locks for batch operations

### Problem: High Disk I/O

**Possible Causes:**
1. Buffer cache too small
2. Log and data on same disk
3. Missing indexes (full scans)
4. No prefetching configured

**Solutions:**
1. Increase buffer size
2. Separate log to dedicated disk
3. Add appropriate indexes
4. Configure prefetching for scan-heavy queries

### Problem: Deadlocks

**Possible Causes:**
1. Inconsistent lock ordering
2. Long transactions
3. Lock escalation

**Solutions:**
1. Establish consistent lock ordering
2. Shorten transactions
3. Use table locks for long transactions
4. Access hot spots late in transaction

---

## 10. Quick Reference

### SQL Server Specific

```sql
-- Check index fragmentation
SELECT * FROM sys.dm_db_index_physical_stats(DB_ID(), NULL, NULL, NULL, 'DETAILED')

-- Check wait statistics
SELECT * FROM sys.dm_os_wait_stats ORDER BY wait_time_ms DESC

-- Check buffer hit ratio
SELECT (1 - (physical_reads / (reads + 0.001))) * 100 AS BufferHitRatio
FROM sys.dm_exec_query_stats

-- Rebuild index
ALTER INDEX index_name ON table_name REBUILD

-- Update statistics
UPDATE STATISTICS table_name
```

### Oracle Specific

```sql
-- Check buffer cache hit ratio
SELECT 1 - (phy.value / (cur.value + con.value)) "Buffer Hit Ratio"
FROM v$sysstat cur, v$sysstat con, v$sysstat phy
WHERE cur.name = 'db block gets'
AND con.name = 'consistent gets'
AND phy.name = 'physical reads';

-- Check for full table scans
SELECT * FROM v$sql WHERE executions > 10
AND disk_reads/executions > 100;

-- Gather statistics
EXEC DBMS_STATS.GATHER_TABLE_STATS('schema', 'table_name');

-- Rebuild index
ALTER INDEX index_name REBUILD;
```

### PostgreSQL Specific

```sql
-- Check cache hit ratio
SELECT
  sum(heap_blks_read) as heap_read,
  sum(heap_blks_hit)  as heap_hit,
  sum(heap_blks_hit) / (sum(heap_blks_hit) + sum(heap_blks_read)) as ratio
FROM pg_statio_user_tables;

-- Check index usage
SELECT relname, indexrelname, idx_scan, idx_tup_read, idx_tup_fetch
FROM pg_stat_user_indexes;

-- Analyze table
ANALYZE table_name;

-- Reindex
REINDEX INDEX index_name;

-- Check for locks
SELECT * FROM pg_locks WHERE NOT granted;
```

### Performance Monitoring Checklist

| What to Monitor | Healthy Range | Action if Outside |
|-----------------|---------------|-------------------|
| Buffer Hit Ratio | > 90% | Increase buffer size |
| Lock Waits | Low | Review transactions, indexes |
| I/O Wait | < 20% | Add disks, tune queries |
| CPU Usage | 70-80% | Add CPU or tune queries |
| Log Disk Utilization | Not 100% | Separate log disk |
| Checkpoint Duration | Predictable | Tune checkpoint interval |

### Index Selection Quick Guide

```
For WHERE clause:
  - Equality (=) → B-tree or Hash
  - Range (>, <, BETWEEN) → B-tree only
  - LIKE 'prefix%' → B-tree only
  - LIKE '%suffix' → Full scan (no index helps)

For JOIN:
  - Always index foreign key columns
  - Index the smaller table's join column

For ORDER BY:
  - Clustering index on ORDER BY column
  - Composite index if WHERE + ORDER BY

For GROUP BY:
  - Index on GROUP BY columns
  - Consider covering index
```

### Tuning Priority Order

1. **Eliminate full table scans** (add indexes)
2. **Separate log from data disks**
3. **Size buffer cache appropriately**
4. **Update statistics regularly**
5. **Review and tune slow queries**
6. **Configure proper RAID levels**
7. **Partition large tables**
8. **Tune checkpoint/backup schedules**

---

## Resources

- **Book:** "Database Tuning: Principles, Experiments, and Troubleshooting" by Shasha & Bonnet
- **Oracle:** Oracle Database Performance Tuning Guide
- **SQL Server:** SQL Server Performance Tuning documentation
- **PostgreSQL:** PostgreSQL Performance Tips documentation

---

*This reference guide summarizes key database tuning concepts for quick lookup during performance analysis and optimization.*
