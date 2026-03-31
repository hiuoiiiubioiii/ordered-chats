You asked for the master map. This is it. 

To master LeetCode at the Oracle level, you must view the 3,800+ questions not as a random list, but as a biological classification system. Every question belongs to a Kingdom, a Phylum, and a Class. 

Here is the definitive **Taxonomy of the LeetCode Universe**. 



---

## Domain 1: Linear & Sequential (The 1D World)
These problems exist on a flat timeline. The data is arranged in a strict line, from index `0` to `n`. Your goal is almost always to scan it efficiently without using nested loops.

### Phylum 1.1: Arrays & Strings
The most common data structures. The challenge is usually optimizing time or space.
* **Class A: Two Pointers**
    * *Order 1: The Pinch* (Moving inward from both ends. Used for sorted arrays, palindromes, Two Sum II).
    * *Order 2: The Chase / Slow & Fast* (Moving in the same direction. Used for removing duplicates, grouping zeros).
* **Class B: Sliding Window**
    * *Order 1: Fixed Window* (Window size $K$ is constant. Used for max sum of subarray size $K$).
    * *Order 2: Variable Window* (Window stretches and shrinks. Used for longest substring without repeating characters).
* **Class C: Pre-computation**
    * *Order 1: Prefix Sum* (Calculating running totals to find range sums in $O(1)$ time).
    * *Order 2: Difference Arrays* (Tracking the *change* between elements to apply range updates efficiently).
* **Class D: The Monotonic Stack/Queue**
    * *Order 1: Next Greater/Smaller Element* (Keeping a stack strictly increasing or decreasing. Used for "Daily Temperatures" or "Largest Rectangle in Histogram").

### Phylum 1.2: Linked Lists
Data in a line, but you cannot jump to an index. You must walk node by node.
* **Class A: Cycle Detection** (Floyd’s Tortoise and Hare algorithm).
* **Class B: In-Place Reversal** (Reversing pointers without creating a new list. Used in "Reverse Linked List II" or "Reverse Nodes in k-Group").
* **Class C: Merging & Sorting** (Using dummy nodes and two pointers to weave lists together).

---

## Domain 2: Hierarchical & Networked (The Connected World)
The data branches out. Flat loops no longer work; you must use recursion or queues to navigate the pathways.

### Phylum 2.1: Trees (Binary, BST, N-Ary)
Data flowing downward from a single root.
* **Class A: Depth-First Search (DFS)**
    * *Order 1: Pre/In/Post-order Traversal* (The fundamental ways to visit nodes).
    * *Order 2: Tree DP / Post-order Info Gathering* (A node must ask its children for information before it can calculate its own answer. Used in "Diameter of Binary Tree").
* **Class B: Breadth-First Search (BFS)**
    * *Order 1: Level-Order Traversal* (Using a Queue to process a tree row-by-row).
* **Class C: Binary Search Tree (BST) Properties**
    * *Order 1: Validation & Searching* (Exploiting the rule that left is smaller, right is bigger).

### Phylum 2.2: Graphs
Data connected in a web, where cycles and infinite loops are a constant danger.
* **Class A: Graph Traversal** (Standard DFS/BFS, but heavily reliant on a `visited` set to avoid infinite loops).
* **Class B: Topological Sorting** (Kahn's Algorithm. Used for dependency resolution, like "Course Schedule").
* **Class C: Disjoint Set / Union-Find** (Instantly determining if two nodes belong to the same connected family. Used in "Number of Connected Components").
* **Class D: Shortest Path Algorithms**
    * *Order 1: Dijkstra's Algorithm* (Finding the shortest path on weighted graphs).
    * *Order 2: Minimum Spanning Tree* (Kruskal’s or Prim’s algorithms to connect all nodes with minimal wire).

---

## Domain 3: State-Space & Optimization (The Decision World)
These are the hardest problems. The data structure doesn't matter as much as the *decisions* you have to make. 

### Phylum 3.1: The Search Spaces
* **Class A: Backtracking**
    * *Order 1: Combinatorics* (Generating all subsets, permutations, or combinations).
    * *Order 2: Grid Exploration* (Word Search, N-Queens, Sudoku Solver).
* **Class B: Binary Search (Advanced)**
    * *Order 1: Searching the Answer Space* (The array isn't sorted, but the *possible answers* are. E.g., "Koko Eating Bananas").

### Phylum 3.2: Dynamic Programming (DP)
* **Class A: 1D DP** (Fibonacci sequence, Climbing Stairs, House Robber).
* **Class B: 2D DP**
    * *Order 1: Grid Paths* (Finding unique paths from top-left to bottom-right).
    * *Order 2: Two-String Matching* (Longest Common Subsequence, Edit Distance).
    * *Order 3: The Knapsack Problem* (Optimizing weight vs. value constraints).
* **Class C: Interval DP** (Solving smaller chunks of an array and merging the answers outwards, like "Burst Balloons").

### Phylum 3.3: Greedy Algorithms
Making the locally optimal choice.
* **Class A: Interval Overlaps** (Merge Intervals, Insert Interval, Non-overlapping Intervals. Almost always requires sorting by start or end time first).
* **Class B: Array Jumps / Fuel** (Jump Game, Gas Station).

---

## Domain 4: Specialized & Abstract (The Niche World)
Highly specific tools for highly specific problems. 

### Phylum 4.1: Frequency & Priority
* **Class A: Heaps / Priority Queues**
    * *Order 1: Top K Elements* (Finding the K-th largest/smallest item in a stream).
    * *Order 2: Two Heaps* (Maintaining a Min-Heap and Max-Heap simultaneously to find the running Median).
* **Class B: Hashing**
    * *Order 1: Frequency Maps* (Counting occurrences).
    * *Order 2: Hash Sets* (O(1) lookups for existence).

### Phylum 4.2: Bitwise & Math
* **Class A: Bit Manipulation** (Using XOR to find missing numbers, bitmasking to represent state).
* **Class B: Tries (Prefix Trees)** (A specialized tree strictly for searching dictionaries of words and autocomplete features).
* **Class C: Pure Math / Geometry** (Prime number sieves, Greatest Common Divisor, Matrix rotations).

---

### The Master Strategy
If you want to conquer this taxonomy, you do not read it top-to-bottom. You learn one Class from each Domain to build cross-disciplinary strength. 

**Which specific Phylum or Class on this map looks the most alien or intimidating to you right now? Let's zoom in and dissect its specific anatomy.**