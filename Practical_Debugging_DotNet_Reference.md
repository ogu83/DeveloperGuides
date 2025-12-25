# Practical Debugging for .NET Developers - Reference Guide

> A comprehensive reference for debugging .NET applications, summarized from "Practical Debugging for .NET Developers" by Michael Shpilt

---

## Table of Contents

1. [Essential Debugging Tools](#1-essential-debugging-tools)
2. [General Debugging Strategies](#2-general-debugging-strategies)
3. [Working with Breakpoints](#3-working-with-breakpoints)
4. [Memory Dumps](#4-memory-dumps)
5. [Debugging Hangs and Deadlocks](#5-debugging-hangs-and-deadlocks)
6. [Memory Issues](#6-memory-issues)
7. [Performance Issues](#7-performance-issues)
8. [Third-Party and Production Code](#8-third-party-and-production-code)
9. [ASP.NET Request Failures](#9-aspnet-request-failures)

---

## 1. Essential Debugging Tools

### Decompilers
| Tool | Description |
|------|-------------|
| **ILSpy** | Free, open-source .NET decompiler |
| **dotPeek** | Free JetBrains decompiler with symbol server capability |
| **dnSpy** | Decompiler + Debugger - can debug without source code |

### Memory Profilers
| Tool | Description |
|------|-------------|
| **dotMemory** | JetBrains memory profiler |
| **ANTS Memory Profiler** | RedGate memory profiler |
| **SciTech Memory Profiler** | Advanced memory analysis |
| **Visual Studio Diagnostic Tools** | Built-in memory profiling |

### Performance Profilers
| Tool | Description |
|------|-------------|
| **dotTrace** | JetBrains performance profiler |
| **ANTS Performance Profiler** | RedGate performance profiler |
| **PerfView** | Free Microsoft tool using ETW events |
| **Visual Studio Profiler** | Built-in performance profiling |

### Network Tools
| Tool | Description |
|------|-------------|
| **Fiddler** | HTTP/HTTPS traffic monitoring and replay |
| **Wireshark** | Network packet analysis |

### System Tools
| Tool | Description |
|------|-------------|
| **Sysinternals Suite** | Process Explorer, ProcMon, ProcDump, DebugView |
| **WinDbg** | Low-level Windows debugger |
| **Event Viewer** | Windows event logs |
| **Performance Monitor (PerfMon)** | Performance counters monitoring |

---

## 2. General Debugging Strategies

### The Scientific Method for Debugging
1. **Observe** - Gather information about the bug
2. **Hypothesize** - Form theories about the cause
3. **Predict** - What should happen if hypothesis is correct
4. **Test** - Verify the prediction
5. **Iterate** - Refine hypothesis based on results

### Key Debugging Tactics

#### Divide and Conquer
- Remove code systematically until bug disappears
- Binary search approach: remove half the code, check if bug persists
- Helps isolate the exact cause

#### Reproduce First
- Create a minimal, reproducible test case
- Automate reproduction if possible
- Document exact steps to reproduce

#### Check Recent Changes
- Use source control to identify recent modifications
- Git bisect can help find the exact commit that introduced the bug

#### Simplify the Problem
- Strip away unnecessary complexity
- Create isolated test cases
- Remove dependencies where possible

### Questions to Ask
- When did this start happening?
- Does it happen consistently or intermittently?
- What changed recently?
- Can you reproduce it in a different environment?
- What are the exact error messages?

---

## 3. Working with Breakpoints

### Breakpoint Types

| Type | Use Case |
|------|----------|
| **Line Breakpoint** | Stop at specific line |
| **Conditional Breakpoint** | Stop only when condition is true |
| **Hit Count Breakpoint** | Stop after N hits |
| **Function Breakpoint** | Stop at function entry (works without source) |
| **Data Breakpoint** | Stop when variable changes |
| **Tracepoint** | Log without stopping |

### Conditional Breakpoints
```csharp
// Condition examples:
i == 100
customer.Name == "John"
items.Count > 50
```

### Actions (Tracepoints)
- Log messages without breaking
- Include variable values: `{variableName}`
- Useful for debugging loops without stopping

### Advanced Techniques

#### Make Object ID
1. Set breakpoint where object is created
2. Right-click variable → Make Object ID
3. Creates weak reference `$1`, `$2`, etc.
4. Check if object is collected later (memory leak detection)

#### Dependent Breakpoints
- Break at A only if B was hit first
- Useful for complex debugging scenarios

---

## 4. Memory Dumps

### Dump Types

| Type | Size | Contains |
|------|------|----------|
| **Minidump** | Small | Thread stacks, loaded modules |
| **Minidump with heap** | Medium | Above + managed heap |
| **Full dump** | Large | Complete process memory |

### Capturing Dumps

#### Using ProcDump
```bash
# Basic dump
procdump -ma <pid>

# On crash
procdump -ma -e <pid>

# On first-chance exception
procdump -ma -e 1 <pid>

# On specific exception
procdump -ma -e 1 -f "NullReference" <pid>

# On high CPU
procdump -ma -c 90 <pid>

# On memory threshold
procdump -ma -m 1024 <pid>
```

#### Using Task Manager
- Right-click process → Create dump file

#### Using Visual Studio
- Debug → Save Dump As...

### Analyzing Dumps

#### In Visual Studio
1. File → Open → File → select .dmp
2. Click "Debug with Managed Only" or "Debug with Mixed"
3. View threads, call stacks, locals

#### In WinDbg
```
# Load SOS extension
.loadby sos clr

# Common commands
!threads          # List all threads
!clrstack         # Managed call stack
!dumpheap -stat   # Heap statistics
!pe               # Print exception
!gcroot <addr>    # Find GC roots
```

---

## 5. Debugging Hangs and Deadlocks

### Types of Hangs

| Type | Description | Detection |
|------|-------------|-----------|
| **Deadlock** | Threads waiting for each other | Circular lock dependency |
| **UI Freeze** | UI thread blocked | Non-responsive window |
| **Infinite Loop** | CPU-bound hang | High CPU usage |
| **Resource Starvation** | Waiting for unavailable resource | External dependency check |

### Detecting Deadlocks

#### Visual Studio
1. Attach to hung process
2. Debug → Break All
3. Debug → Windows → Parallel Stacks
4. Look for threads waiting on locks

#### Using Dumps
1. Capture dump of hung process
2. Analyze thread states
3. Check for lock contentions

### Common Deadlock Patterns

#### Classic Deadlock
```csharp
// Thread 1
lock(A) {
    lock(B) { }  // Waits for B
}

// Thread 2
lock(B) {
    lock(A) { }  // Waits for A - DEADLOCK!
}
```

#### Solution: Lock Ordering
```csharp
// Always acquire locks in same order
lock(A) {
    lock(B) { }
}
```

### UI Thread Freezes

#### Common Causes
- Long-running operations on UI thread
- Synchronous I/O operations
- Blocking calls to external services

#### Solutions
- Use async/await
- Move work to background threads
- Use `.ConfigureAwait(false)` when possible

---

## 6. Memory Issues

### Memory Problem Types

| Issue | Symptom | Cause |
|-------|---------|-------|
| **Memory Leak** | Memory rises over time | Objects not released |
| **GC Pressure** | High % time in GC | Too many allocations |
| **OutOfMemoryException** | Crash | Memory limit reached |

### Detecting Memory Leaks

#### Performance Counters
```
Process | Private Bytes          # Total memory
.NET CLR Memory | # Bytes in all Heaps  # Managed memory
.NET CLR Memory | % Time in GC   # GC overhead
```

#### Memory Profiler Technique
1. Take snapshot at idle state
2. Run suspected operation
3. Return to idle, take second snapshot
4. Compare snapshots - new objects are potential leaks

### Common Memory Leak Sources

#### 1. Event Subscriptions
```csharp
// LEAK: subscriber referenced by publisher
publisher.Event += handler;

// FIX: Always unsubscribe
publisher.Event -= handler;
```

#### 2. Static Variables
```csharp
// LEAK: Static list holds references forever
static List<MyClass> _instances = new List<MyClass>();
```

#### 3. Captured Variables in Lambdas
```csharp
// LEAK: _id captures 'this'
stockMarketPortfolio.Execute(() => {
    Log.Info("ID:" + _id);
});

// FIX: Use local variable
var id = _id;
stockMarketPortfolio.Execute(() => {
    Log.Info("ID:" + id);
});
```

#### 4. Timers Not Stopped
```csharp
// LEAK: Timer keeps reference to handler
Timer timer = new Timer(HandleTick);
timer.Change(TimeSpan.FromSeconds(5), TimeSpan.FromSeconds(5));
// Timer never stopped = memory leak
```

#### 5. Caching Without Eviction
- Implement eviction policies (LRU, time-based)
- Set maximum cache size
- Use weak references when appropriate

### GC Pressure

#### Detection
- `% Time in GC` > 20% is problematic
- Frequent Generation 2 collections
- Visual Studio Diagnostic Tools shows frequent GC

#### Causes
- Many short-lived allocations reaching Gen 2
- Large object heap fragmentation
- Inefficient use of strings/arrays

#### Solutions

##### Use ArrayPool
```csharp
var pool = ArrayPool<int>.Shared;
int[] array = pool.Rent(1000);
try {
    // Use array
}
finally {
    pool.Return(array);
}
```

##### Use structs for small, short-lived data
```csharp
struct Point { public int X, Y; }  // Stack allocated
```

##### Use StringBuilder for many concatenations
```csharp
// Bad for many strings
string result = a + b + c + d + e + f + ...;

// Good for many strings
var sb = new StringBuilder();
sb.Append(a).Append(b)...
```

##### Avoid Finalizers
- Finalizers are expensive (300x slower)
- Use IDisposable instead
- Call `GC.SuppressFinalize(this)` in Dispose

### Dispose Pattern
```csharp
public class MyClass : IDisposable
{
    private IntPtr _buffer;
    private bool _disposed = false;

    protected virtual void Dispose(bool disposing)
    {
        if (_disposed) return;

        if (disposing) {
            // Dispose managed resources
        }

        // Free unmanaged resources
        Marshal.FreeHGlobal(_buffer);
        _disposed = true;
    }

    public void Dispose()
    {
        Dispose(true);
        GC.SuppressFinalize(this);
    }

    ~MyClass() => Dispose(false);
}
```

---

## 7. Performance Issues

### When to Worry About Performance
- In algorithms and hot paths
- High-throughput servers
- Libraries used by others
- Mobile/IoT devices

### Performance Analysis Workflow

1. **Monitor** - Use performance counters
2. **Profile** - Use performance profiler
3. **Identify** - Find bottleneck
4. **Optimize** - Fix specific issue
5. **Benchmark** - Verify improvement

### Key Performance Counters

| Counter | Normal | Problem |
|---------|--------|---------|
| `% Time in GC` | < 10% | > 20% |
| `% Processor Time` | Varies | 100% sustained |
| `Exceptions/sec` | Low | High |
| `Contention Rate/sec` | Low | High |

### Profiling Modes

| Mode | Use Case | Overhead |
|------|----------|----------|
| **Sampling** | General performance | Low |
| **Tracing** | Hit counts, all calls | Medium |
| **Line-by-line** | Algorithm analysis | High |
| **Timeline** | Chronological view | Low |

### Using PerfView

```bash
# Collect trace
PerfView collect output.etl

# Collect for specific time
PerfView collect output.etl /MaxCollectSec:60

# With circular buffer (keeps last 1GB)
PerfView collect output.etl -CircularMB:1024
```

### Common Performance Issues

#### Too Many Exceptions
- Exceptions are expensive
- Don't use for control flow
- Check `Exceptions/sec` counter

#### JIT Compilation Overhead
- Affects startup time
- Use NGEN or ReadyToRun (R2R) for AOT compilation
- Check `% Time in JIT`

#### Lock Contention
```csharp
// Problem: Long operations inside lock
lock(obj) {
    DoLongOperation();  // Other threads wait
}

// Solution: Minimize lock scope
Data data;
lock(obj) {
    data = GetData();
}
DoLongOperationWith(data);
```

#### Frozen UI
- Never do I/O on UI thread
- Use async/await with ConfigureAwait(false)
```csharp
async Task LoadDataAsync()
{
    var data = await httpClient.GetAsync(url)
        .ConfigureAwait(false);
    // Continues on thread pool, not UI thread
}
```

### Optimization Techniques

#### Caching
- Cache expensive operation results
- Implement eviction policies
- Consider distributed cache (Redis)

#### Lazy Initialization
```csharp
Lazy<ExpensiveObject> _obj = new Lazy<ExpensiveObject>(
    () => new ExpensiveObject()
);

// Created only when first accessed
var obj = _obj.Value;
```

#### Parallel Processing
- Use for CPU-bound work
- Be careful of overhead and contention

### Benchmarking with BenchmarkDotNet
```csharp
[Benchmark]
public void Method1() { /* ... */ }

[Benchmark]
public void Method2() { /* ... */ }

// Run benchmarks
BenchmarkRunner.Run<MyBenchmarks>();
```

---

## 8. Third-Party and Production Code

### Debugging Without Source Code

#### Using dnSpy
1. Open assembly in dnSpy
2. Set breakpoints in decompiled code
3. Start debugging or attach to process
4. Full debugging experience with decompiled code

#### Using Visual Studio + dotPeek
1. Open assembly in dotPeek
2. Start Symbol Server in dotPeek
3. Add dotPeek URL to VS symbol locations
4. Debug with decompiled source

### Handling Optimized Code

#### Problem
- Production code is optimized
- Can't see some local variables
- Some breakpoints don't hit

#### Solutions

##### dnSpy
- Automatically disables JIT optimization when starting process
- Best to start process with dnSpy, not attach

##### Visual Studio
1. Uncheck "Enable Just My Code"
2. Check "Suppress JIT optimization on module load"

##### Using .ini file
Create `AssemblyName.ini` next to the DLL:
```ini
[.NET Framework Debugging Control]
GenerateTrackingInfo=1
AllowOptimize=0
```

### Breaking on Third-Party Exceptions

1. Disable "Enable Just My Code" in VS options
2. Enable "Suppress JIT optimization"
3. Configure Exception Settings to break on desired exceptions

### Function Breakpoints (No Source Code)
1. Debug → Windows → Breakpoints
2. New → Function Breakpoint
3. Enter: `Namespace.Class.Method`

---

## 9. ASP.NET Request Failures

### Information Needed for Debugging
- Exception type and message
- Stack trace with line numbers
- Local variables at exception
- Request parameters
- Database/HTTP calls made

### Detection Methods

| Method | Information Provided |
|--------|---------------------|
| Event Viewer | Exception details |
| Developer Exception Page | Stack trace, code |
| stdout logs | Full exception info |
| Error Monitoring (Raygun) | Aggregated errors, counts |
| Application Insights | Timeline, dependencies |
| Snapshot Debugger | Full debugging experience |

### Developer Exception Page (ASP.NET Core)
```csharp
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    if (env.IsDevelopment())
    {
        app.UseDeveloperExceptionPage();
    }
}
```

### Error Logging Middleware
```csharp
public class ErrorLoggingMiddleware
{
    private readonly RequestDelegate _next;

    public ErrorLoggingMiddleware(RequestDelegate next)
    {
        _next = next;
    }

    public async Task Invoke(HttpContext context)
    {
        try
        {
            await _next(context);
        }
        catch (Exception e)
        {
            // Log exception details
            Logger.LogError(e, "Request failed");
            throw;
        }
    }
}
```

### Enable stdout Logs
In `web.config`:
```xml
<aspNetCore stdoutLogEnabled="true"
            stdoutLogFile=".\logs\stdout" />
```

### Capture Dumps on Exception
```bash
# On first-chance exception
procdump -ma -e 1 <pid>

# On specific exception type
procdump -ma -e 1 -f "NullReference" <pid>
```

---

## Quick Reference: Common Commands

### ProcDump
```bash
procdump -ma <pid>                    # Full dump
procdump -ma -e <pid>                 # On crash
procdump -ma -e 1 <pid>               # On first-chance exception
procdump -ma -c 90 <pid>              # CPU > 90%
procdump -ma -m 1024 <pid>            # Memory > 1GB
```

### WinDbg SOS Commands
```
.loadby sos clr                       # Load SOS
!threads                              # List threads
!clrstack                             # Managed stack
!dumpheap -stat                       # Heap stats
!dumpheap -type <TypeName>            # Objects of type
!do <address>                         # Dump object
!gcroot <address>                     # GC roots
!pe                                   # Print exception
!syncblk                              # Sync blocks (locks)
```

### dotnet-counters (.NET Core)
```bash
dotnet-counters ps                    # List processes
dotnet-counters list                  # List counters
dotnet-counters monitor -p <pid>      # Monitor counters
```

### dotnet-trace (.NET Core)
```bash
dotnet trace list-processes           # List processes
dotnet trace collect -p <pid>         # Collect trace
```

---

## Debugging Checklist

### Before Starting
- [ ] Can you reproduce the issue?
- [ ] What changed recently?
- [ ] Check logs and error messages
- [ ] Identify the type of issue (crash, hang, performance, memory)

### For Crashes
- [ ] Get exception details (type, message, stack trace)
- [ ] Capture dump if needed
- [ ] Check for null references, invalid operations
- [ ] Verify input data

### For Hangs
- [ ] Check CPU usage (100% = loop, 0% = waiting)
- [ ] Capture dump and analyze threads
- [ ] Look for deadlocks in lock order
- [ ] Check external dependencies

### For Memory Issues
- [ ] Monitor memory over time
- [ ] Compare memory snapshots
- [ ] Check for event subscriptions
- [ ] Review caching strategies
- [ ] Look for finalizer issues

### For Performance
- [ ] Profile with sampling mode first
- [ ] Check % Time in GC
- [ ] Identify hot paths
- [ ] Benchmark before and after changes

---

## Resources

- **Book**: "Practical Debugging for .NET Developers" by Michael Shpilt
- **Blog**: [michaelscodingspot.com](https://michaelscodingspot.com)
- **PerfView Tutorials**: Microsoft Channel 9
- **BenchmarkDotNet**: [benchmarkdotnet.org](https://benchmarkdotnet.org)

---

*This reference guide is a summary of "Practical Debugging for .NET Developers" for quick lookup during debugging sessions.*