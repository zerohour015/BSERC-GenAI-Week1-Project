# DSA Exam Kit — Source-grounded study guide

**Scope:** This guide covers sorting and binary search trees in the MIT 6.006 lecture PDFs listed in the source register. It is a study companion, not a replacement for your college syllabus.

## 1. Insertion sort

Insertion sort maintains a prefix of the array that is already sorted. It takes the next key and moves it left through the sorted prefix until it reaches the position where the ordering is preserved.

**How to trace it:**
1. Treat the first element as a sorted prefix.
2. Take the next element as the key.
3. Compare it with elements in the sorted prefix, moving larger elements right as necessary.
4. Insert the key into its correct position.
5. Repeat until the entire array is sorted.

The MIT lecture analyses a reverse-ordered input as a worst case: comparisons and swaps grow quadratically, giving Θ(n²) for that case. Binary insertion sort uses binary search to reduce comparisons for locating the insertion position, but shifting elements to make room still takes linear time per insertion; total shifts remain quadratic. [MIT Lecture 03, printed pages 5 and 16–17](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/90a37c49b07b105ea7a027abc67eddc6_MIT6_006F11_lec03.pdf).

## 2. Merge sort

Merge sort follows divide and conquer:
1. If the input has one element, it is already sorted.
2. Otherwise, split the array into two halves.
3. Recursively sort each half.
4. Merge the two sorted halves into one sorted result.

The merge step scans the two sorted subarrays and selects the next smallest element. Processing all n elements in one merge takes Θ(n) time.

The lecture gives the recurrence:

`T(1) = Θ(1)`  
`T(n) = 2T(n/2) + Θ(n)` for `n > 1`.

The recursion tree has about log₂ n levels; total merge work per level is proportional to n. Therefore overall running time is Θ(n log n). [MIT Lecture 03, printed pages 18 and 31–42](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/90a37c49b07b105ea7a027abc67eddc6_MIT6_006F11_lec03.pdf).

## 3. Binary search tree (BST)

A BST node stores a key and may have a left child, a right child and a parent pointer. The ordering invariant in the MIT notes is:
- Keys in the left subtree of a node are less than or equal to that node's key.
- Keys in the right subtree are greater than or equal to that node's key.

**Core operations described in the lecture:**
- `insert(value)`: follow left/right pointers until the insertion position is found.
- `find(value)`: follow left/right pointers until the value is found or a NIL link is reached.
- `findmin()`: follow left links until no further left child exists.
- `next-larger(node)`: if the node has a right subtree, return that subtree's minimum; otherwise move upward until leaving a left-child relationship, then return the corresponding ancestor if one exists.

The lecture states that these operations are O(h), where h is the height of the BST. This is not automatically O(log n): inserting values in an order that produces a chain-like tree can make h proportional to n. [MIT Lecture 05, printed pages 4–7](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/d9c745bbfb610e9e53f6aef4261f3805_MIT6_006F11_lec05.pdf).

## 4. Compare the structures and algorithms

| Topic | Key idea | Cost supported by the listed MIT lecture notes |
|---|---|---|
| Insertion sort, reverse-ordered worst case | Insert each next key into sorted prefix | Θ(n²) comparisons/swaps in the lecture's worst-case example |
| Binary insertion sort | Binary-search insertion position | Θ(n log n) comparisons; shifting remains quadratic overall |
| Merge sort | Recursively sort halves, then merge | Θ(n log n) total; merge step Θ(n) |
| BST search/insert/minimum/next-larger | Follow parent/child links along a path | O(h), where h is tree height |

## 5. Exam checklist

- Trace insertion sort on a short array.
- Explain why reverse order forces many shifts/comparisons.
- Write merge sort's divide-and-conquer steps.
- Write and solve `T(n) = 2T(n/2) + Θ(n)`.
- State the BST ordering invariant accurately, including the equal-key convention.
- Trace BST insert, find, minimum and next-larger.
- Explain why BST operation cost is expressed in terms of height and why an unbalanced BST can be slow.

## Sources

1. [MIT 6.006 Lecture 03 PDF — Insertion sort, merge sort](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/90a37c49b07b105ea7a027abc67eddc6_MIT6_006F11_lec03.pdf)
2. [MIT 6.006 Lecture 05 PDF — Binary search trees, BST sort](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/d9c745bbfb610e9e53f6aef4261f3805_MIT6_006F11_lec05.pdf)
3. [MIT 6.006 Lecture notes index](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/pages/lecture-notes/)
