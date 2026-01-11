# Comprehensive Algorithm Guide for LLM Agents

This guide synthesizes fundamental algorithm knowledge for training LLM agents to understand, analyze, design, and implement algorithms effectively.

---

## Part I: Foundations of Algorithm Analysis

### 1. What is an Algorithm?

An algorithm is a well-defined computational procedure that takes input and produces output through a finite sequence of steps. Key properties:

- **Correctness**: Produces the correct output for all valid inputs
- **Finiteness**: Terminates after a finite number of steps
- **Definiteness**: Each step is precisely defined
- **Input/Output**: Has zero or more inputs and one or more outputs
- **Effectiveness**: Each step is basic enough to be carried out

### 2. Asymptotic Notation

Asymptotic notation describes algorithm efficiency as input size grows toward infinity.

#### Big-O Notation (Upper Bound)
```
f(n) = O(g(n)) if there exist constants c > 0 and n₀ ≥ 0 such that
f(n) ≤ c·g(n) for all n ≥ n₀
```

**Common complexity classes (slowest to fastest growth):**
- O(1) - Constant time
- O(log n) - Logarithmic time
- O(n) - Linear time
- O(n log n) - Linearithmic time
- O(n²) - Quadratic time
- O(n³) - Cubic time
- O(2ⁿ) - Exponential time
- O(n!) - Factorial time

#### Big-Omega Notation (Lower Bound)
```
f(n) = Ω(g(n)) if there exist constants c > 0 and n₀ ≥ 0 such that
f(n) ≥ c·g(n) for all n ≥ n₀
```

#### Big-Theta Notation (Tight Bound)
```
f(n) = Θ(g(n)) if f(n) = O(g(n)) and f(n) = Ω(g(n))
```

### 3. Proving Big-O Bounds

**Method 1: Direct Proof**
To prove f(n) = O(g(n)), find specific values of c and n₀ that satisfy the definition.

Example: Prove 3n² + 5n + 2 = O(n²)
- For n ≥ 1: 3n² + 5n + 2 ≤ 3n² + 5n² + 2n² = 10n²
- Choose c = 10, n₀ = 1

**Method 2: Limit Method**
```
If lim(n→∞) f(n)/g(n) = L where 0 < L < ∞, then f(n) = Θ(g(n))
If lim(n→∞) f(n)/g(n) = 0, then f(n) = O(g(n)) but f(n) ≠ Θ(g(n))
```

### 4. Recurrence Relations

Recurrences express runtime of recursive algorithms.

#### Master Theorem
For recurrences of form T(n) = aT(n/b) + f(n) where a ≥ 1, b > 1:

Let c_crit = log_b(a)

1. If f(n) = O(n^(c_crit - ε)) for some ε > 0, then T(n) = Θ(n^c_crit)
2. If f(n) = Θ(n^c_crit), then T(n) = Θ(n^c_crit · log n)
3. If f(n) = Ω(n^(c_crit + ε)) for some ε > 0 and af(n/b) ≤ cf(n), then T(n) = Θ(f(n))

**Common recurrences:**
- T(n) = T(n/2) + O(1) → T(n) = O(log n) [Binary search]
- T(n) = 2T(n/2) + O(n) → T(n) = O(n log n) [Merge sort]
- T(n) = 2T(n/2) + O(1) → T(n) = O(n) [Tree traversal]
- T(n) = T(n-1) + O(n) → T(n) = O(n²) [Selection sort]
- T(n) = T(n-1) + O(1) → T(n) = O(n) [Linear recursion]

---

## Part II: Algorithm Design Paradigms

### 1. Divide and Conquer

**Strategy:**
1. **Divide** the problem into smaller subproblems
2. **Conquer** subproblems recursively
3. **Combine** solutions to solve original problem

**Template:**
```
function divideAndConquer(problem):
    if problem is small enough:
        return baseCaseSolution(problem)

    subproblems = divide(problem)
    solutions = [divideAndConquer(sub) for sub in subproblems]
    return combine(solutions)
```

**Classic Examples:**

#### Merge Sort - O(n log n)
```
function mergeSort(A, p, r):
    if p < r:
        q = (p + r) / 2
        mergeSort(A, p, q)
        mergeSort(A, q+1, r)
        merge(A, p, q, r)

function merge(A, p, q, r):
    # Merge sorted subarrays A[p..q] and A[q+1..r]
    L = A[p..q] + [∞]
    R = A[q+1..r] + [∞]
    i = j = 0
    for k = p to r:
        if L[i] ≤ R[j]:
            A[k] = L[i]; i++
        else:
            A[k] = R[j]; j++
```

#### Binary Search - O(log n)
```
function binarySearch(A, target, low, high):
    if low > high:
        return NOT_FOUND
    mid = (low + high) / 2
    if A[mid] == target:
        return mid
    else if A[mid] > target:
        return binarySearch(A, target, low, mid-1)
    else:
        return binarySearch(A, target, mid+1, high)
```

### 2. Dynamic Programming

**Key Insight:** Solve each subproblem once and store results to avoid redundant computation.

**Requirements:**
1. **Optimal Substructure**: Optimal solution contains optimal solutions to subproblems
2. **Overlapping Subproblems**: Same subproblems recur many times

**Approaches:**
- **Top-down (Memoization)**: Recursive with caching
- **Bottom-up (Tabulation)**: Iterative, solve smaller subproblems first

**Template:**
```
# Top-down with memoization
function dpTopDown(problem, memo={}):
    if problem in memo:
        return memo[problem]
    if isBaseCase(problem):
        return baseCaseSolution

    result = combine(dpTopDown(subproblem) for subproblem in subproblems)
    memo[problem] = result
    return result

# Bottom-up tabulation
function dpBottomUp(n):
    dp = array of size n+1
    dp[0] = baseCase
    for i = 1 to n:
        dp[i] = combine(dp[j] for relevant j < i)
    return dp[n]
```

**Classic Examples:**

#### Fibonacci Numbers
```
# Naive recursive: O(2^n)
function fib(n):
    if n ≤ 1: return n
    return fib(n-1) + fib(n-2)

# DP with memoization: O(n)
function fibMemo(n, memo={}):
    if n in memo: return memo[n]
    if n ≤ 1: return n
    memo[n] = fibMemo(n-1) + fibMemo(n-2)
    return memo[n]

# DP bottom-up: O(n) time, O(1) space
function fibDP(n):
    if n ≤ 1: return n
    prev, curr = 0, 1
    for i = 2 to n:
        prev, curr = curr, prev + curr
    return curr
```

#### 0/1 Knapsack Problem
Given items with weights w[i] and values v[i], maximize value for capacity W.

```
function knapsack(W, weights, values, n):
    dp = 2D array of size (n+1) x (W+1)

    for i = 0 to n:
        for w = 0 to W:
            if i == 0 or w == 0:
                dp[i][w] = 0
            else if weights[i-1] <= w:
                dp[i][w] = max(
                    values[i-1] + dp[i-1][w - weights[i-1]],
                    dp[i-1][w]
                )
            else:
                dp[i][w] = dp[i-1][w]

    return dp[n][W]
```

#### Longest Common Subsequence
```
function LCS(X, Y):
    m, n = len(X), len(Y)
    dp = 2D array of size (m+1) x (n+1)

    for i = 0 to m:
        for j = 0 to n:
            if i == 0 or j == 0:
                dp[i][j] = 0
            else if X[i-1] == Y[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])

    return dp[m][n]
```

### 3. Greedy Algorithms

**Strategy:** Make locally optimal choices at each step, hoping to find global optimum.

**When to use:**
- Problem has optimal substructure
- Greedy choice property: locally optimal leads to globally optimal

**Template:**
```
function greedy(problem):
    solution = empty
    while problem not solved:
        choice = selectBest(available choices)
        if isValid(solution + choice):
            solution = solution + choice
    return solution
```

**Classic Examples:**

#### Activity Selection
Select maximum non-overlapping activities.
```
function activitySelection(activities):
    sort activities by finish time
    selected = [activities[0]]
    lastFinish = activities[0].finish

    for i = 1 to n-1:
        if activities[i].start >= lastFinish:
            selected.append(activities[i])
            lastFinish = activities[i].finish

    return selected
```

#### Huffman Coding
Build optimal prefix-free codes for data compression.
```
function huffman(frequencies):
    heap = min-heap of (freq, node) pairs

    while heap.size > 1:
        left = heap.extractMin()
        right = heap.extractMin()
        merged = new Node(left.freq + right.freq, left, right)
        heap.insert(merged)

    return heap.extractMin()  # Root of Huffman tree
```

---

## Part III: Sorting Algorithms

### Comparison-Based Sorting

| Algorithm | Best | Average | Worst | Space | Stable |
|-----------|------|---------|-------|-------|--------|
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | No |
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | No |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | No |

**Lower bound for comparison sorts: Ω(n log n)**

### Key Implementations

#### Insertion Sort
```
function insertionSort(A):
    for j = 1 to length(A) - 1:
        key = A[j]
        i = j - 1
        while i >= 0 and A[i] > key:
            A[i + 1] = A[i]
            i = i - 1
        A[i + 1] = key
```

**Loop Invariant:** At the start of each iteration, A[0..j-1] contains the original elements in sorted order.

#### Quick Sort
```
function quickSort(A, low, high):
    if low < high:
        pivot = partition(A, low, high)
        quickSort(A, low, pivot - 1)
        quickSort(A, pivot + 1, high)

function partition(A, low, high):
    pivot = A[high]
    i = low - 1
    for j = low to high - 1:
        if A[j] <= pivot:
            i = i + 1
            swap(A[i], A[j])
    swap(A[i + 1], A[high])
    return i + 1
```

#### Heap Sort
```
function heapSort(A):
    buildMaxHeap(A)
    for i = length(A) - 1 down to 1:
        swap(A[0], A[i])
        heapSize = heapSize - 1
        maxHeapify(A, 0)

function maxHeapify(A, i):
    left = 2*i + 1
    right = 2*i + 2
    largest = i
    if left < heapSize and A[left] > A[largest]:
        largest = left
    if right < heapSize and A[right] > A[largest]:
        largest = right
    if largest != i:
        swap(A[i], A[largest])
        maxHeapify(A, largest)
```

### Non-Comparison Sorting (Linear Time)

#### Counting Sort - O(n + k)
For integers in range [0, k].
```
function countingSort(A, k):
    count = array of size k+1, initialized to 0
    output = array of size len(A)

    for x in A:
        count[x] = count[x] + 1

    for i = 1 to k:
        count[i] = count[i] + count[i-1]

    for j = len(A) - 1 down to 0:
        output[count[A[j]] - 1] = A[j]
        count[A[j]] = count[A[j]] - 1

    return output
```

#### Radix Sort - O(d(n + k))
For d-digit numbers.
```
function radixSort(A, d):
    for i = 1 to d:
        stableSort A on digit i  # Using counting sort
```

---

## Part IV: Graph Algorithms

### Graph Representations

**Adjacency List:** Space O(V + E), preferred for sparse graphs
```
graph[v] = list of vertices adjacent to v
```

**Adjacency Matrix:** Space O(V²), preferred for dense graphs
```
matrix[u][v] = 1 if edge (u,v) exists, 0 otherwise
```

### Graph Traversals

#### Breadth-First Search (BFS) - O(V + E)
```
function BFS(G, source):
    visited = set containing source
    queue = [source]
    distance[source] = 0

    while queue not empty:
        u = queue.dequeue()
        for v in G.adjacent(u):
            if v not in visited:
                visited.add(v)
                distance[v] = distance[u] + 1
                parent[v] = u
                queue.enqueue(v)
```

**Use cases:** Shortest path in unweighted graphs, level-order traversal

#### Depth-First Search (DFS) - O(V + E)
```
function DFS(G):
    time = 0
    for each vertex u in G:
        color[u] = WHITE
    for each vertex u in G:
        if color[u] == WHITE:
            DFSVisit(G, u)

function DFSVisit(G, u):
    time = time + 1
    discover[u] = time
    color[u] = GRAY
    for v in G.adjacent(u):
        if color[v] == WHITE:
            parent[v] = u
            DFSVisit(G, v)
    color[u] = BLACK
    time = time + 1
    finish[u] = time
```

**Use cases:** Topological sort, cycle detection, strongly connected components

### Shortest Path Algorithms

#### Dijkstra's Algorithm - O((V + E) log V)
Single-source shortest paths for non-negative edge weights.
```
function dijkstra(G, source):
    dist[source] = 0
    dist[v] = ∞ for all other v
    priorityQueue = all vertices with dist as key

    while priorityQueue not empty:
        u = extractMin(priorityQueue)
        for each neighbor v of u:
            if dist[u] + weight(u, v) < dist[v]:
                dist[v] = dist[u] + weight(u, v)
                parent[v] = u
                decreaseKey(priorityQueue, v, dist[v])
```

#### Bellman-Ford Algorithm - O(VE)
Handles negative edge weights, detects negative cycles.
```
function bellmanFord(G, source):
    dist[source] = 0
    dist[v] = ∞ for all other v

    for i = 1 to |V| - 1:
        for each edge (u, v) in G:
            if dist[u] + weight(u, v) < dist[v]:
                dist[v] = dist[u] + weight(u, v)
                parent[v] = u

    # Check for negative cycles
    for each edge (u, v) in G:
        if dist[u] + weight(u, v) < dist[v]:
            return "Negative cycle detected"
```

#### Floyd-Warshall Algorithm - O(V³)
All-pairs shortest paths.
```
function floydWarshall(G):
    dist = adjacency matrix (∞ for non-edges)

    for k = 1 to |V|:
        for i = 1 to |V|:
            for j = 1 to |V|:
                if dist[i][k] + dist[k][j] < dist[i][j]:
                    dist[i][j] = dist[i][k] + dist[k][j]
```

### Minimum Spanning Trees

#### Kruskal's Algorithm - O(E log E)
```
function kruskal(G):
    MST = empty set
    sort edges by weight
    makeSet(v) for each vertex v

    for each edge (u, v) in sorted order:
        if findSet(u) != findSet(v):
            MST = MST ∪ {(u, v)}
            union(u, v)

    return MST
```

#### Prim's Algorithm - O((V + E) log V)
```
function prim(G, root):
    key[v] = ∞ for all v
    key[root] = 0
    inMST[v] = false for all v
    priorityQueue = all vertices with key as priority

    while priorityQueue not empty:
        u = extractMin(priorityQueue)
        inMST[u] = true
        for each neighbor v of u:
            if not inMST[v] and weight(u, v) < key[v]:
                parent[v] = u
                key[v] = weight(u, v)
                decreaseKey(priorityQueue, v, key[v])
```

### Topological Sort

For directed acyclic graphs (DAGs).
```
function topologicalSort(G):
    result = empty list
    visited = empty set

    function visit(node):
        if node in visited:
            return
        visited.add(node)
        for each neighbor m of node:
            visit(m)
        result.prepend(node)

    for each node in G:
        visit(node)

    return result
```

---

## Part V: Data Structures for Algorithms

### Arrays and Dynamic Arrays
- Access: O(1)
- Search: O(n) unsorted, O(log n) sorted
- Insert/Delete at end: O(1) amortized
- Insert/Delete at arbitrary position: O(n)

### Linked Lists
- Access: O(n)
- Insert/Delete at known position: O(1)
- Search: O(n)

### Hash Tables
- Average case: O(1) for insert, delete, search
- Worst case: O(n)
- Good hash function crucial for performance

### Binary Search Trees
- Average case: O(log n) for all operations
- Worst case: O(n) for unbalanced trees

### Balanced BSTs (AVL, Red-Black)
- O(log n) guaranteed for all operations

### Heaps (Binary Heap)
```
Parent(i) = (i-1) / 2
Left(i) = 2*i + 1
Right(i) = 2*i + 2
```
- Insert: O(log n)
- Extract-min/max: O(log n)
- Find-min/max: O(1)
- Build heap: O(n)

### Union-Find (Disjoint Set)
With union by rank and path compression:
- Nearly O(1) amortized per operation
- Formally O(α(n)) where α is inverse Ackermann function

```
function makeSet(x):
    parent[x] = x
    rank[x] = 0

function find(x):
    if parent[x] != x:
        parent[x] = find(parent[x])  # Path compression
    return parent[x]

function union(x, y):
    rootX = find(x)
    rootY = find(y)
    if rootX == rootY:
        return
    # Union by rank
    if rank[rootX] < rank[rootY]:
        parent[rootX] = rootY
    else if rank[rootX] > rank[rootY]:
        parent[rootY] = rootX
    else:
        parent[rootY] = rootX
        rank[rootX] = rank[rootX] + 1
```

---

## Part VI: Algorithm Correctness

### Mathematical Induction

Used to prove algorithm correctness for recursive algorithms.

**Structure:**
1. **Base Case:** Prove P(0) or P(1) is true
2. **Inductive Hypothesis:** Assume P(k) is true for some k
3. **Inductive Step:** Prove P(k+1) is true using the hypothesis

**Example: Proving sum formula**
Prove: 1 + 2 + ... + n = n(n+1)/2

Base case (n=1): 1 = 1(2)/2 = 1 ✓

Inductive step: Assume true for k. For k+1:
1 + 2 + ... + k + (k+1) = k(k+1)/2 + (k+1)
                        = (k+1)(k/2 + 1)
                        = (k+1)(k+2)/2 ✓

### Loop Invariants

A property that holds before and after each iteration.

**Three steps:**
1. **Initialization:** Invariant is true before first iteration
2. **Maintenance:** If true before an iteration, remains true after
3. **Termination:** When loop terminates, invariant gives useful property

**Example: Insertion Sort**
Invariant: A[0..j-1] contains original elements in sorted order.

- Initialization: Before j=1, A[0..0] has one element, trivially sorted
- Maintenance: Moving A[j] into sorted position maintains sorted property
- Termination: When j=n, A[0..n-1] is sorted

---

## Part VII: Problem-Solving Strategies

### 1. Understand the Problem
- What are the inputs and outputs?
- What are the constraints?
- Are there edge cases?

### 2. Design the Algorithm
- Start with brute force
- Identify repeated work or optimal substructure
- Choose appropriate paradigm:
  - Independent subproblems → Divide and Conquer
  - Overlapping subproblems → Dynamic Programming
  - Local choices lead to global optimum → Greedy
  - State space exploration → BFS/DFS

### 3. Analyze Complexity
- Time complexity (worst, average, best case)
- Space complexity
- Is it acceptable for the problem constraints?

### 4. Implement Carefully
- Handle edge cases
- Use appropriate data structures
- Test with examples

### 5. Optimize if Needed
- Can preprocessing help?
- Can we use better data structures?
- Is there a different algorithmic approach?

---

## Part VIII: Common Patterns and Techniques

### Two Pointers
Use when processing arrays/strings from both ends or finding pairs.
```
left, right = 0, n-1
while left < right:
    # Process and move pointers
```

### Sliding Window
For subarray/substring problems with fixed or variable window.
```
for right = 0 to n-1:
    # Add element at right to window
    while window_invalid:
        # Remove element at left from window
        left = left + 1
    # Process current window
```

### Binary Search Variations
```
# Find first occurrence
while low < high:
    mid = low + (high - low) / 2
    if condition(mid):
        high = mid
    else:
        low = mid + 1

# Find last occurrence
while low < high:
    mid = low + (high - low + 1) / 2
    if condition(mid):
        low = mid
    else:
        high = mid - 1
```

### Backtracking
For constraint satisfaction and combinatorial problems.
```
function backtrack(state):
    if isGoal(state):
        recordSolution(state)
        return

    for choice in getChoices(state):
        if isValid(choice):
            makeChoice(choice)
            backtrack(newState)
            undoChoice(choice)
```

### Prefix Sums
For range sum queries.
```
prefix[0] = 0
for i = 1 to n:
    prefix[i] = prefix[i-1] + array[i-1]

sum(i, j) = prefix[j+1] - prefix[i]
```

---

## Part IX: Advanced Topics

### String Algorithms

#### KMP Pattern Matching - O(n + m)
```
function computeLPS(pattern):
    lps = array of size m
    lps[0] = 0
    len = 0
    i = 1
    while i < m:
        if pattern[i] == pattern[len]:
            len = len + 1
            lps[i] = len
            i = i + 1
        else if len != 0:
            len = lps[len - 1]
        else:
            lps[i] = 0
            i = i + 1
    return lps
```

#### Rabin-Karp - O(n + m) average
Uses rolling hash for pattern matching.

### Number Theory

#### GCD (Euclidean Algorithm)
```
function gcd(a, b):
    while b != 0:
        a, b = b, a mod b
    return a
```

#### Fast Exponentiation - O(log n)
```
function power(base, exp, mod):
    result = 1
    while exp > 0:
        if exp is odd:
            result = (result * base) mod mod
        base = (base * base) mod mod
        exp = exp / 2
    return result
```

### Bit Manipulation

```
x & (x - 1)      # Clear lowest set bit
x | (x + 1)      # Set lowest clear bit
x & -x           # Extract lowest set bit
x ^ y            # XOR for finding unique elements
```

---

## Part X: Complexity Classes

### P (Polynomial Time)
Problems solvable in polynomial time. Examples: sorting, shortest path.

### NP (Nondeterministic Polynomial)
Problems whose solutions can be verified in polynomial time.

### NP-Complete
Hardest problems in NP. If any NP-complete problem has a polynomial solution, then P = NP.

**Classic NP-Complete Problems:**
- SAT (Boolean Satisfiability)
- Traveling Salesman Problem (decision version)
- Graph Coloring
- Subset Sum
- Hamiltonian Path

### NP-Hard
At least as hard as NP-complete problems, but may not be in NP.

### Dealing with NP-Hard Problems
1. **Approximation algorithms:** Find near-optimal solutions
2. **Heuristics:** No guarantees but often work well
3. **Parameterized algorithms:** Efficient for small parameter values
4. **Special cases:** Some instances may be tractable

---

## Summary: Algorithm Selection Guide

| Problem Type | Consider |
|--------------|----------|
| Sorted array search | Binary search O(log n) |
| Finding minimum/maximum | Single pass O(n) |
| Sorting | Quick sort, Merge sort O(n log n) |
| Shortest path (unweighted) | BFS O(V + E) |
| Shortest path (weighted, positive) | Dijkstra O((V+E) log V) |
| Shortest path (negative weights) | Bellman-Ford O(VE) |
| All-pairs shortest path | Floyd-Warshall O(V³) |
| Minimum spanning tree | Kruskal, Prim O(E log V) |
| Optimal substructure + overlapping | Dynamic Programming |
| Making local optimal choices | Greedy |
| Divide into independent parts | Divide and Conquer |
| Exploring all possibilities | Backtracking |
| Processing in levels | BFS |
| Processing to depth | DFS |

---

## Key Takeaways for Algorithm Design

1. **Start simple:** Begin with brute force, then optimize
2. **Know your paradigms:** D&C, DP, Greedy, Backtracking
3. **Analyze before implementing:** Ensure complexity is acceptable
4. **Choose right data structures:** They often determine algorithm efficiency
5. **Prove correctness:** Use induction and loop invariants
6. **Consider edge cases:** Empty input, single element, duplicates
7. **Practice pattern recognition:** Many problems reduce to known patterns
8. **Trade-offs exist:** Time vs space, simplicity vs efficiency

This guide provides the foundational knowledge needed to analyze, design, and implement algorithms effectively. Mastery comes through practice and applying these concepts to diverse problem sets.
