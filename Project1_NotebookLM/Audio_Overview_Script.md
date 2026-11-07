# Audio Overview Script — DSA: Sorting and Trees

**Approximate length:** 3 minutes  
**Use:** Companion narration draft. Ask NotebookLM to create its own Audio Overview from the imported sources; do not label this text as a NotebookLM-generated audio file.

Welcome to this short revision session on sorting and binary search trees, based on MIT OpenCourseWare's Introduction to Algorithms lectures.

First, insertion sort. Imagine the left side of an array is already sorted. Each step takes the next key and places it into the right position in that sorted prefix. This is easy to trace by hand. But in the reverse-ordered worst case, many elements must move for every new key. The MIT notes count this as quadratic work.

Binary insertion sort uses binary search to find where the next key belongs. That saves comparisons, but it does not remove the need to shift elements to open a position. This is a useful reminder: reducing comparisons does not always reduce the whole algorithm's running time.

Now compare that with merge sort. Merge sort divides the array into two halves, recursively sorts each half, and merges the two sorted results. The merge step examines and places each of the n elements, so one merge level costs linear time. The recurrence is T of n equals two times T of n over two, plus a linear merge cost. The recursion tree has logarithmically many levels, with linear work per level, giving n log n total time.

Finally, a binary search tree. Each node has a key and may link to a left and right child. The ordering rule places keys no larger than a node in its left subtree and keys no smaller than it in its right subtree. Searching follows one path: compare, then go left or right. Finding the minimum follows left links until there are no more.

The cost of these BST operations depends on the tree height h. A balanced tree can be shallow, but inserting already-sorted values can produce a chain-like tree. So do not automatically write logarithmic time for every BST operation: the safe statement from this lecture is O of h.

For revision, practise tracing insertion sort, writing the merge-sort recurrence, and following a BST search path. Then open the cited MIT lecture passages and check each answer against the source. That is the habit of source-grounded learning: understand the concept, and verify the evidence.
