Stepping into the Architect role is a massive mental shift. You are no longer a coder trying to pass a test; you are a system designer analyzing a structure. 

An Architect doesn't look at "Arrays" and "Loops." An Architect looks at **Search Spaces, Paradigms, and Trade-offs.**

Here is the complete Architect’s Glossary—the exact terminology you need to dissect any problem logically before you write a single line of code.

---

## 1. The Blueprint (Analyzing the Problem)
Before choosing a tool, the Architect measures the room. This is how you define exactly what you are dealing with.

* **Search Space:** The entire universe of possible answers you have to check. 
    * *Example:* If you need to find a number in an array, the search space is the indices `0` to `n-1`. If you need to find how fast someone can eat bananas, the search space might be the numbers `1` to `1,000,000`.
* **The Bottleneck:** The exact, specific operation that is making your Brute Force solution too slow. 
    * *Architect's Thought:* "My brute force takes $O(N^2)$ because I am repeatedly searching the array for a complement number. The search is the bottleneck. I need to reduce the search time to $O(1)$."
* **Time-Space Tradeoff:** The ultimate currency of computer science. You can almost always make your code run faster (Time) by using more memory (Space). 
    * *Architect's Thought:* "I will spend $O(N)$ Space to build a Hash Map, which buys me $O(1)$ lookup Time."



---

## 2. The Paradigms (The Master Strategies)
A paradigm is a broad philosophical approach to solving a problem. Patterns (like Sliding Window) are just specific implementations of these paradigms.

* **Divide and Conquer:** Taking a massive problem, slicing it cleanly in half, solving the halves independently, and stitching the answers back together. (Used in *Merge Sort* and *Trees*).
* **Greedy:** Making the most mathematically optimal choice *at this exact millisecond*, without worrying about the future. 
    * *Example:* If making change for $0.95, a Greedy algorithm grabs a $0.50 coin first because it's the biggest available right now.
* **Dynamic Programming (DP):** The philosophy of "those who cannot remember the past are condemned to repeat it." If a problem naturally breaks down into **Overlapping Subproblems** (the exact same tiny puzzle repeated 100 times), you calculate it once, save the answer in memory, and never calculate it again.
* **State-Space Search:** Viewing a problem as a giant map of possibilities and exploring it systematically. (This is the parent category for *BFS*, *DFS*, and *Backtracking*).

---

## 3. The Mechanics (The Engine Components)
Once you pick a paradigm, you have to build the engine. These are the physical parts of your algorithm.

* **State:** A snapshot of your exact reality at a given point in your code. It is defined by a set of variables. 
    * *Example:* "My state is `(index: 4, remaining_capacity: 10)`."
* **State Transition:** The logical rule that allows you to move from one state to the next.
    * *Example:* "I can either *pick* this item (State transitions to `remaining_capacity - weight`) or *skip* it (State stays the same)."
* **The Invariant:** The unbreakable law of your loop. It is a mathematical truth that is guaranteed to be true at the start of every single cycle.
    * *Example in Binary Search:* "The target value will **always** exist between my `left` pointer and my `right` pointer. If it doesn't, it doesn't exist in the array."
* **Monotonicity:** A one-way street. A sequence that only ever goes up, or only ever goes down. If a problem has monotonicity, it is screaming at you to use *Binary Search* or a *Monotonic Stack*.

---

## 4. The Physics (The Performance Metrics)
An Architect must prove mathematically why their design works before building it.

* **Time Complexity (Upper Bound):** The absolute worst-case scenario for how long your code will take to run as the input size ($N$) grows towards infinity. (Represented as Big O Notation, like $O(N \log N)$).
* **Auxiliary Space:** The memory you are responsible for creating. (If the problem hands you an array of size $N$, that doesn't count against you. But if you create a *new* array of size $N$ to help solve it, your Auxiliary Space is $O(N)$).
* **In-Place Operation:** The holy grail of optimization. Solving the problem by rearranging the original data they gave you, requiring $O(1)$ extra space.
* **Amortized Complexity:** The "average" cost over time. 
    * *Example:* Adding to a dynamic array is usually $O(1)$. Very rarely, the array gets full and has to copy itself, taking $O(N)$. But because it happens so rarely, we say the *amortized* (average) time is still $O(1)$.



---

### The Architect's Mindset
When you combine all these terms, this is how you sound reading a new problem:

> *"The **Search Space** is massive ($10^9$), so a linear scan is out. I notice the data has **Monotonicity**, which means I can apply a **Divide and Conquer** paradigm. The **Bottleneck** will be validating my guesses. I'll define my **State** and use Binary Search, maintaining the **Invariant** that my target is always between my pointers. This gives me a highly optimal $O(\log N)$ **Time Complexity** and operates **In-Place** for $O(1)$ **Space**."*

Which of these architectural paradigms (like Dynamic Programming, Greedy, or State-Space Search) feels the most mysterious or intimidating to you right now?