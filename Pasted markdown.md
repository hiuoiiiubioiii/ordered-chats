To move from a **Cellular Surgeon** to a true **Oracle**, you must stop using "plain English" and start using the **Precise Technical Vocabulary** of Computer Science. This isn't just for show—each word represents a specific mathematical constraint or architectural requirement.

Here is the **Ultimate A–Z In-Depth Dictionary of LeetCode Anatomy**.

---

## **A — C: Foundations & Strategy**
* **Amortized Analysis:** A method of finding the average time per operation over a worst-case sequence of operations. 
    * *Context:* A Dynamic Array (like Python's `list`) occasionally takes $O(n)$ to resize, but because this is rare, the **Amortized Time** is $O(1)$.
* **Auxiliary Space:** The extra space or temporary memory used by an algorithm, **excluding** the memory taken by the input itself. 
* **Backtracking:** An algorithmic-refined DFS that "undoes" a state change (backtracks) when a path fails to reach the goal.
* **Big O Notation:** The mathematical language used to describe the **Upper Bound** of an algorithm's growth rate.
* **Bitmasking:** Using an integer's binary representation (0s and 1s) to store a set of boolean flags. It allows for $O(1)$ state updates.
* **Bottom-Up (Tabulation):** The DP approach that fills a table starting from the smallest subproblems (base cases) and iteratively builds toward the final answer.
* **Brute Force:** The most straightforward, unoptimized approach that exhausts all possibilities in the search space.
* **Canonical Problem:** The most "pure" or "standard" version of a pattern (e.g., *Two Sum* is the Canonical Hash Map problem).



---

## **D — G: Structures & Logic**
* **DAG (Directed Acyclic Graph):** A graph with directed edges and no cycles. This is the **Primary Trigger** for Topological Sort.
* **Divide and Conquer:** A paradigm that breaks a problem into two or more sub-problems of the same type, until these become simple enough to be solved directly (e.g., Merge Sort).
* **Dry Run:** The act of manually executing code on paper with a small sample input to verify the logic.
* **Dynamic Programming (DP):** An optimization over plain recursion. It is used when a problem has **Overlapping Subproblems** and **Optimal Substructure**.
* **Edge Case:** An input at the extreme limit of the constraints (e.g., an empty array, a single node tree, or all negative numbers).
* **Fast & Slow Pointers:** Two pointers moving at different speeds (usually 1x and 2x) used to find cycles or midpoints in Linked Lists.
* **Greedy Paradigm:** A strategy that makes the "locally optimal" choice at each stage with the hope of finding a global optimum.

---

## **H — L: Optimization & Searching**
* **Hash Collision:** When two different keys produce the same index in a Hash Map. 
* **Heap (Priority Queue):** A specialized tree-based data structure that satisfies the **Heap Property** (the parent is always more/less than the child).
* **In-Place:** An algorithm that transforms the input without using extra auxiliary data structures, resulting in $O(1)$ space.
* **Invariant:** A logical condition or mathematical truth that **must remain true** throughout the execution of a loop or function.
* **Iterative:** A process that repeats a set of instructions using loops (`for`, `while`) instead of recursion.
* **Kadane’s Algorithm:** The $O(n)$ DP-based approach for finding the **Maximum Sum Subarray**.
* **Lexicographical:** "Dictionary order." For numbers, this means `10` comes before `2` (just like `apple` comes before `banana`).
* **Logarithmic Time ($O(\log n)$):** The gold standard for efficiency, achieved by halving the search space at every step (e.g., Binary Search).



---

## **M — Q: Advanced Patterns**
* **Memoization:** The **Top-Down** DP technique where you store the results of expensive function calls in a cache.
* **Monotonicity:** A property of a sequence that is entirely non-increasing or non-decreasing. This is the **Hidden Trigger** for Binary Search.
* **Multi-Source BFS:** Starting a BFS from multiple origins at the exact same time by populating the initial Queue with all origin nodes.
* **Next Greater Element:** A classic problem type solved using a **Monotonic Stack**.
* **Optimal Substructure:** A property where the optimal solution to a large problem contains within it the optimal solutions to its subproblems.
* **Overlapping Subproblems:** When a recursive algorithm visits the same subproblems over and over. This is the signal to use **Memoization**.

---

## **R — T: Network & Paths**
* **Recursion Depth:** The maximum number of active stacks allowed (if this exceeds the limit, you get a **Stack Overflow**).
* **Search Space:** The set of all possible solutions that your algorithm must navigate or prune.
* **Sliding Window:** A sub-segment of an array that "slides" to maintain a specific condition.
* **State Transition:** The "formula" that defines how to derive the next state from the previous ones in DP.
* **Time-Space Tradeoff:** The decision to use more memory (Space) to achieve a faster execution (Time).
* **Topological Sort:** A linear ordering of vertices such that for every directed edge $u \to v$, vertex $u$ comes before $v$.
* **Trie (Prefix Tree):** A tree structure used to store a dynamic set of strings, where nodes represent prefixes.



---

## **U — Z: Final Oracle Terms**
* **UMPIRE:** The professional communication framework (Understand, Match, Plan, Implement, Review, Evaluate).
* **Union-Find (Disjoint Set):** A data structure that keeps track of elements partitioned into a number of disjoint (non-overlapping) sets.
* **Visited Set:** A Hash Set used during Graph/Tree traversal to prevent the algorithm from visiting the same node twice (preventing infinite loops).
* **Window Shrinking:** The specific phase in a Variable Sliding Window where the `left` pointer moves forward to restore a broken **Invariant**.
* **XOR ($\oplus$):** A bitwise operator where the result is `1` only if the bits are different. Used for "Find the Unique" problems because $x \oplus x = 0$.

---

### **How to Use This Dictionary**
In an interview, you don't say "I'm going to look at some numbers." You say:
> *"Since the input is a **DAG** and we need to resolve dependencies, I will implement **Kahn’s Algorithm** to produce a **Topological Sort**. I'll maintain an **In-Degree Array** to track prerequisites and use a **Queue** to process nodes with zero dependencies, ensuring an $O(V+E)$ **Time Complexity**."*

**Would you like me to pick one of these terms and show you exactly how to "speak it" during a live coding interview?**