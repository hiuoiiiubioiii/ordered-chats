THIS IS THE ULTIMATE CHEAT CODE. If you truly want to operate at the Architect and Oracle levels, you don't even read the story of the problem first. You scroll straight to the very bottom of the page and read the **Constraints**.

The constraints mathematically dictate exactly what Pattern you are allowed to use. If you know the anatomy of constraints, you can eliminate 90% of the algorithms in your head before you even read the prompt. 

Here is the absolute, in-depth anatomy of LeetCode constraints and how to weaponize them.

---

## 1. The Physics: The "$10^8$ Rule"
Why do constraints even exist? Because LeetCode servers (and standard interview coding environments) have a physical speed limit. 

A standard modern CPU can perform roughly **$10^8$ (100 million) basic operations per second**. LeetCode usually gives your code about 1 to 2 seconds to run in Python, Java, or C++. 

If your Time Complexity mathematically forces the computer to do more than $10^8$ operations, you will get a **Time Limit Exceeded (TLE)** error. 



[Image of Big O time complexity chart]


---

## 2. The Primary Constraint: The Size of $N$
When you look at the maximum length of the input array or string (usually denoted as $N$), you plug it into the $10^8$ rule to find your allowed Time Complexity. 

Here is the exact mapping you must memorize.

### The Micro Constraints ($N \le 20$)
* **The Math:** If $N=20$, then $2^{20} \approx 10^6$ operations. $20!$ is massive, but $10! \approx 3.6 \times 10^6$. Both fit easily under $10^8$.
* **Allowed Complexity:** $O(2^N)$ or $O(N!)$
* **The Architect's Translation:** "The input is so tiny that the server expects me to try literally every single possible combination."
* **The Forced Patterns:** **Backtracking** (N-Queens, Sudoku Solver), **Recursion**, or **Bitmasking**.

### The Small Constraints ($N \le 1000$ to $3000$)
* **The Math:** If $N=1000$, then $N^2 = 10^6$. If $N=3000$, then $N^2 = 9 \times 10^6$. Both fit well under $10^8$. But $N^3$ ($10^9$) would crash the server.
* **Allowed Complexity:** $O(N^2)$
* **The Architect's Translation:** "I am allowed to use a loop inside of a loop. I can compare every item against every other item."
* **The Forced Patterns:** **2D Dynamic Programming** (grid paths, longest common subsequence), **Nested Loops**, or **Dense Graph BFS/DFS**.

### The Standard Constraints ($10^4 \le N \le 10^5$)
*This represents about 80% of all LeetCode questions.*
* **The Math:** If $N=10^5$, then $N^2 = 10^{10}$ (Instant TLE crash!). You are mathematically banned from using double `for` loops. But $N \log N \approx 1.6 \times 10^6$, which is lightning fast.
* **Allowed Complexity:** $O(N)$ or $O(N \log N)$
* **The Architect's Translation:** "I can only sweep through this data once or twice. If I need to search, I must sort it first or use a Hash Map."
* **The Forced Patterns:** **Sliding Window**, **Two Pointers**, **Hash Maps**, **Sorting**, **Monotonic Stacks**, **Heaps**, or **1D Dynamic Programming**.

### The Massive Constraints ($N \ge 10^9$)
* **The Math:** If $N = 10^9$, even an $O(N)$ single loop will take 10 seconds and crash the server. You cannot even look at every piece of data. 
* **Allowed Complexity:** $O(\log N)$ or $O(1)$
* **The Architect's Translation:** "I have to chop the search space in half every single step, or use a pure math formula."
* **The Forced Patterns:** **Binary Search** (usually searching the *answer space*, not an array) or **Math/Geometry formulas**.

---

## 3. The Secondary Constraints: The Hidden Clues
$N$ tells you the Time Complexity. But the *values* inside the data tell you the Space Complexity and Data Structure.

### A. The "Alphabet" Hint
* **What you see:** `s consists of only lowercase English letters.`
* **The Secret Translation:** Do not use a standard Hash Map to count letters. Hash Maps have a slight overhead. Instead, create a fixed Array of size 26 (`counts = [0] * 26`). This guarantees $O(1)$ Space and perfect $O(N)$ Time.

### B. The "Tiny Values" Hint
* **What you see:** $10^5 \le N \le 10^5$ **BUT** $0 \le nums[i] \le 100$.
* **The Secret Translation:** The array is massive, but the numbers inside it are tiny. This is a trap! They want you to think it's an $O(N \log N)$ Sorting problem. Instead, use **Counting Sort** or **Bucket Sort**. You just count how many 1s, 2s, and 3s there are. This drops your time to a blazing fast $O(N)$.

### C. The "Modulo" Hint
* **What you see:** `Return the answer modulo 10^9 + 7.`
* **The Secret Translation:** The final answer is going to be astronomically huge, exceeding the physical memory limit of a standard 32-bit or 64-bit integer. This is a massive neon sign pointing directly to **Dynamic Programming** or **Combinatorics (Math)**. 

### D. The "Negative Number" Trap
* **What you see:** $-10^4 \le nums[i] \le 10^4$
* **The Secret Translation:** If the problem asks for a "Maximum Subarray Sum," the presence of negative numbers means your "Sliding Window" might break (because adding a negative makes the sum smaller, confusing the inchworm logic). You will likely need **Kadane's Algorithm** (a specific DP approach) instead.

---

### How to use this live in an interview
When the interviewer finishes pasting the question into the shared document, you look at the bottom and say this:

> *"I see the input size is up to $10^5$. Because of that constraint, a brute force $O(N^2)$ approach will definitely Time Out. That tells me right away we need to optimize this to at least $O(N \log N)$ using sorting, or $O(N)$ using a Hash Map or Two Pointers. Let's look at the data to see which fits better..."*

You just proved you are an Architect before you even wrote `def solve():`.

**Would you like to play a game? I can give you just the raw constraints and a 3-word summary of a random LeetCode problem, and you can try to instantly deduce the Time Complexity and Pattern!**