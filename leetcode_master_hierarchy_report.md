# LeetCode Master Hierarchy, Taxonomy, and Anatomy

Corpus size classified: **3873 questions**.

This hierarchy is a source-driven normalization built from the uploaded master HTML. Because the source does not explicitly label every question with data structure, variation, canonical archetype, or Big-O, those fields are **heuristic classifications inferred from the optimized-pattern column, drawing columns, and complexity prose**.

## Top data-shape buckets

- **Array / Sequence** — 858
- **Number / Bit / Math** — 824
- **Matrix / Grid** — 410
- **String / Text** — 387
- **Tree / Trie** — 382
- **Relational Table / SQL** — 331
- **Graph / Network** — 249
- **Intervals / Geometry / Coordinates** — 200
- **Object / Process / API** — 152
- **Linked List** — 80

## Top primary engines

- **Dynamic Programming** — 354
- **Greedy** — 261
- **Custom Exact Technique** — 246
- **Hash Map** — 213
- **Math / Number Theory** — 197
- **Two Pointers** — 180
- **Prefix / Suffix Precompute** — 158
- **Sliding Window** — 150
- **Counting** — 141
- **DFS** — 128
- **Binary Search** — 127
- **BFS** — 126
- **Matrix / Grid** — 110
- **Heap** — 101
- **SQL / Window Function** — 94
- **Simulation / Scan / Precompute** — 90
- **Shell / Unix** — 89
- **SQL / Join** — 87
- **Hash Set** — 80
- **Tree** — 79

## Biggest canonical archetypes

- **Canonical: Exact custom named technique** — 246
- **Canonical: Gas Station / local-choice greedy** — 208
- **Canonical: Coin Change / state-transition DP** — 188
- **Canonical: Two Sum II / Container With Most Water** — 166
- **Canonical: Mathematical invariant** — 152
- **Canonical: Frequency counting** — 139
- **Canonical: Grid traversal / DP scan** — 110
- **Canonical: Direct lookup dictionary** — 110
- **Canonical: Minimum Window / variable-size window** — 109
- **Canonical: Group Anagrams / frequency map** — 100
- **Canonical: Range Sum Query** — 99
- **Canonical: Ranking & running-row analytics** — 94
- **Canonical: Top K Frequent Elements / merge-k** — 92
- **Canonical: Text-processing pipeline** — 89
- **Canonical: Combine Two Tables** — 87
- **Canonical: Contains Duplicate / seen-set uniqueness** — 80
- **Canonical: Basic filter / reshape / null-handling** — 78
- **Canonical: Grouped aggregation / departmental summary** — 72
- **Canonical: Binary Search / median partition** — 71
- **Canonical: Permutations / combinations search** — 70

## Sample hierarchy paths

- **Number / Bit / Math → Math / Number Theory → Formula / constructive math → None → Canonical: Mathematical invariant** — 94
- **Relational Table / SQL → SQL / Table Ops → Filtering / reshaping / scalar SQL ops → None → Canonical: Basic filter / reshape / null-handling** — 52
- **Matrix / Grid → Matrix / Grid → Grid / board traversal → None → Canonical: Grid traversal / DP scan** — 46
- **Array / Sequence → Greedy → Local-choice optimization → None → Canonical: Gas Station / local-choice greedy** — 45
- **Array / Sequence → Custom Exact Technique → Exact custom / named technique → None → Canonical: Exact custom named technique** — 44
- **Relational Table / SQL → SQL / Join → Key-based row matching → None → Canonical: Combine Two Tables** — 36
- **Relational Table / SQL → SQL / Group By → Grouped aggregation → None → Canonical: Grouped aggregation / departmental summary** — 36
- **Matrix / Grid → Dynamic Programming → 2D DP → None → Canonical: Edit Distance / Grid DP** — 35
- **Number / Bit / Math → Custom Exact Technique → Exact custom / named technique → None → Canonical: Exact custom named technique** — 33
- **Relational Table / SQL → SQL / Join → Left join / null retention → None → Canonical: Combine Two Tables** — 33
- **Relational Table / SQL → SQL / Window Function → Partitioned window analytics → None → Canonical: Ranking & running-row analytics** — 31
- **Tree / Trie → Tree → Recursive subtree aggregation → None → Canonical: Binary Tree recursion** — 30
- **Graph / Network → Union-Find → Connectivity / component merging → None → Canonical: Number of Connected Components / Redundant Connection** — 30
- **Number / Bit / Math → Greedy → Local-choice optimization → None → Canonical: Gas Station / local-choice greedy** — 30
- **String / Text → Custom Exact Technique → Exact custom / named technique → None → Canonical: Exact custom named technique** — 28
- **Array / Sequence → Dynamic Programming → State-transition DP → None → Canonical: Coin Change / state-transition DP** — 27
- **String / Text → Two Pointers → Boundary / pointer sweep → None → Canonical: Two Sum II / Container With Most Water** — 26
- **Array / Sequence → Greedy → Sort-then-greedy → + Sorting → Canonical: Merge Intervals / scheduling greedy** — 26
- **Array / Sequence → Hash Map → Frequency dictionary → + Counting → Canonical: Group Anagrams / frequency map** — 25
- **Matrix / Grid → Dynamic Programming → State-transition DP → None → Canonical: Coin Change / state-transition DP** — 25
- **Array / Sequence → Two Pointers → Boundary / pointer sweep → None → Canonical: Two Sum II / Container With Most Water** — 24
- **Tree / Trie → DFS → Tree DFS → + Tree → Canonical: Path Sum / subtree DFS** — 24
- **String / Text → Greedy → Local-choice optimization → None → Canonical: Gas Station / local-choice greedy** — 23
- **Array / Sequence → Prefix / Suffix Precompute → Range-sum precompute → None → Canonical: Range Sum Query** — 21
- **Number / Bit / Math → Math / Number Theory → Digit arithmetic / carry → None → Canonical: Add Two Numbers / Reverse Integer** — 21

## Field meanings

- **data_shape**: input-world / terrain (array, string, tree, graph, grid, SQL, etc.)
- **primary_engine**: main solving engine
- **variation**: subtype of that engine
- **composite_helper**: secondary helper or paired engine
- **canonical_link**: prototype problem family
- **opt_time_budget / opt_space_budget**: normalized from the optimized complexity and memory columns when possible; otherwise inferred
- **draw_anatomy_bucket**: visual canvas bucket from the source-wide drawing analysis