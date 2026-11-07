# DSA Self-Test — Sorting and Binary Search Trees

Try all questions before opening the answer key. Questions are based on the two MIT 6.006 lecture PDFs in the source register.

## Questions

1. In insertion sort, what part of the array is kept sorted while the algorithm proceeds?
2. What happens to the key during each insertion-sort iteration?
3. What input order is used in the MIT lecture to illustrate insertion sort's quadratic worst case?
4. In binary insertion sort, what does binary search improve, and what cost remains?
5. List the three main stages of merge sort.
6. Why does a merge of two sorted subarrays take Θ(n) time for n total elements?
7. Write the merge-sort recurrence for n greater than 1.
8. What is the resulting asymptotic running time of merge sort?
9. State the BST ordering rule for the left and right subtrees as given in the MIT notes.
10. How does the BST lecture express the time cost of its core operations, and what does h represent?
11. How does `findmin()` locate the minimum key?
12. What can happen to BST height if keys are inserted in sorted order?

## Answer key

1. The prefix containing the elements already processed.
2. It is moved through the sorted prefix to the position that preserves order.
3. Reverse order: `[n, n-1, ..., 2, 1]`.
4. It reduces comparisons used to locate the insertion point; shifting elements to make room is still linear for an insertion and total shifts remain quadratic.
5. Divide into halves; recursively sort both halves; merge the sorted halves.
6. Each element is considered and placed once during the merge, so work is proportional to the total number of elements.
7. `T(1)=Θ(1)` and `T(n)=2T(n/2)+Θ(n)` for `n>1`.
8. `Θ(n log n)`.
9. Left-subtree keys are `≤` the node's key; right-subtree keys are `≥` the node's key.
10. `O(h)`, where h is the height of the BST.
11. Follow left-child links until no further left child exists.
12. It can become chain-like, with height proportional to n, so operations can degrade to linear time.

## Source check

Answers 1–8: MIT Lecture 03, printed pages 5, 16–18 and 31–42. Answers 9–12: MIT Lecture 05, printed pages 4–7. Open the relevant source and verify the passage; do not treat this self-test as evidence that NotebookLM generated its Quiz feature.
