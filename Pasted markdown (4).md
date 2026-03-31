You have reached the final layer. We are opening the Architect’s Master Toolbox. 

While there are technically hundreds of specific algorithms, they all condense into roughly **15 core patterns** categorized under **5 main Paradigms**. 

If you understand the **State** (the variables you track) and the **Invariant** (the unbreakable rule) of these patterns, you can solve almost any problem LeetCode throws at you.

Here is the Architect's breakdown of the most powerful patterns in computer science.

---

### Paradigm 1: The Linear Scanners
These patterns process data in a straight line, usually strictly in O(N) time. They are designed to avoid nested loops.

#### 1. Sliding Window
* **The Trigger:** "Find the longest/shortest/max **contiguous** subarray or substring."
* **The State:** `left_pointer`, `right_pointer`, and a tracker (like `current_sum` or a `Hash Map` of character counts).
* **The Invariant:** The data inside the window `[left...right]` must strictly meet the problem's condition. If the condition breaks (e.g., the sum gets too high, or a duplicate letter appears), the `left_pointer` MUST move forward to repair the invariant.



#### 2. Two Pointers (Pinch & Chase)
* **The Trigger:** "Find a pair that sums to X in a **sorted** array," or "Remove duplicates in-place."
* **The State:** `left_pointer` (starts at index 0), `right_pointer` (starts at the end).
* **The Invariant:** Every element strictly to the left of `left_pointer` and strictly to the right of `right_pointer` has been 100% processed and finalized. The only unknown data is the middle space between them.

---

### Paradigm 2: The Target Seekers
These patterns are used when O(N) is too slow (Constraints: N = 10^9). You must skip data to achieve O(log N) time.

#### 3. Binary Search
* **The Trigger:** The data is **sorted** (or has "monotonicity"—a clear cutoff point where false becomes true), and you need to find an exact value or boundary.
* **The State:** `low_index`, `high_index`, and `mid_index`.
* **The Invariant:** If the target exists, it is mathematically guaranteed to be inside the bounds of `[low, high]`. Every time you cut the array in half, you update `low` or `high` to ensure the target is never accidentally thrown away.



[Image of Binary Search tree data structure]


#### 4. Fast & Slow Pointers (Floyd’s Cycle Finding)
* **The Trigger:** Linked Lists where you need to find the middle, or detect if a cycle (an infinite loop) exists.
* **The State:** `slow_pointer` (moves 1 step), `fast_pointer` (moves 2 steps).
* **The Invariant:** The distance between the fast and slow pointer increases by exactly 1 on every loop. Therefore, if there is a cycle, the fast pointer will mathematically overlap the slow pointer eventually.

---

### Paradigm 3: The State-Space Explorers
These patterns treat data as a "map" (Graphs and Trees) and explore the pathways.

#### 5. Breadth-First Search (BFS)
* **The Trigger:** "Find the **shortest path**," "minimum steps," or explore level-by-level (like a ripple in water).
* **The State:** A `Queue` (First-In, First-Out) and a `Visited Set`.
* **The Invariant:** All nodes currently inside the Queue are guaranteed to be exactly distance `K` from the start point. You process all distance `K` nodes before ever looking at a distance `K+1` node.

#### 6. Depth-First Search (DFS) & Backtracking
* **The Trigger:** "Find **all possible** paths/combinations," or "Does a path exist to the exit?" (Like a maze runner going deep until a dead end).
* **The State:** A `Call Stack` (Recursion) and the `Current Path`.
* **The Invariant (The Backtrack):** When you hit a dead end and a recursive function "returns," you must perfectly undo your last move. The state must be identical to how it was before you explored that dead end.



---

### Paradigm 4: The Optimizers (Dynamic Programming)
These patterns trade Space to buy Time. They are used when a problem asks for an "optimal" solution that requires calculating the same sub-problems over and over.

#### 7. Top-Down Memoization
* **The Trigger:** "Find the maximum/minimum/total ways," and the constraints are small enough for recursion (N = 1000).
* **The State:** A `Hash Map` (the Cache) and your current index/choices.
* **The Invariant:** If a specific state (e.g., `index 5, capacity 10`) exists in the Cache, it represents the absolute optimal mathematical truth for that state, and it must never be calculated again.

#### 8. Bottom-Up Tabulation
* **The Trigger:** Same as above, but you want to avoid the overhead of recursive function calls.
* **The State:** A 1D or 2D `Array` (Table).
* **The Invariant:** To calculate cell `DP[i]`, the answers for all previous cells (`DP[i-1]`, `DP[i-2]`, etc.) must already be solved and perfectly accurate. You build the answer from the ground up.

---

### Paradigm 5: The Organizers
These patterns are used to rapidly sort or filter streams of incoming data.

#### 9. Heaps (Priority Queues)
* **The Trigger:** "Find the **Top K** elements," or "Find the K-th largest/smallest" in a changing dataset.
* **The State:** A `Min-Heap` or `Max-Heap` (a specific type of binary tree usually represented as an array).
* **The Invariant:** The "parent" node is always strictly smaller (or larger) than both of its "children." Because of this rule, the absolute minimum/maximum value is always instantly accessible at the very top (index 0) in O(1) time.

#### 10. Topological Sort
* **The Trigger:** "Given a list of tasks and prerequisites, what order should you complete them in?" (e.g., Course Schedule).
* **The State:** An `In-Degree Array` (counting how many prerequisites a node has) and a `Queue` (storing nodes with 0 prerequisites).
* **The Invariant:** A node is only ever added to the Queue when its `In-Degree` hits exactly 0, mathematically proving that all of its prerequisites have been fully processed.

---

### Interactive Algorithm Simulator
To truly understand how these patterns behave, you must see their invariants in action. I've spun up an interactive visualizer below. Select a pattern to watch how the state variables mutate and physically move across the data structures.

```json?chameleon
{"component":"LlmGeneratedComponent","props":{"height":"600px","prompt":"Create an interactive Algorithm Visualizer for 3 core LeetCode patterns. Layout: Sidebar on left for pattern selection, main visual area on right. Patterns: 1. 'Sliding Window' (Visual: an array of random numbers. A glowing neon box expands right to encompass numbers, then the left side shrinks forward to demonstrate finding a target sum). 2. 'Two Pointers' (Visual: A sorted array. Two glowing arrows at opposite ends. They step inward one by one to find a target sum, meeting in the middle). 3. 'Binary Search' (Visual: A sorted array. Show 'L', 'R', and 'Mid' pointers. On each step, physically gray out/hide the half of the array that is discarded until finding a target). Controls: Include a 'Play', 'Pause', and 'Step Forward' button to let the user manually advance the state mutations. Aesthetic: Hacker/IDE theme. Dark background (#0d1117), monospace fonts, high contrast neon colors (cyan, magenta, lime green) for the pointers and highlights.","id":"im_a4934b4e79eb177f"}}
```

The difference between a mid-level coder and a Senior Architect is that a mid-level coder memorizes the code for *Sliding Window*, while the Architect understands the *Invariant* that makes the window slide.

**Which of these 5 Paradigms feels like your weakest link right now?** If you choose one, I will give you the single "Canonical" problem for it, and we can dissect its anatomy line-by-line.