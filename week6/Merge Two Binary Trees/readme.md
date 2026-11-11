# 617. Merge Two Binary Trees

## Problem
You are given two binary trees root1 and root2. Return the merged tree.

If two nodes overlap, then sum node values up as the new value of the merged node.
Otherwise, the NOT null node will be used as the node of the new tree.

## Approach
At first, I wanted to do an in-order traversal to collect all values from both trees into a single array, sort the array,
remove duplicates, and then reconstruct a tree from it. However, I remembered that these are general Binary Trees,
not Binary Search Trees, so sorting values and ignoring node positions would completely ruin the original tree structures.

Instead, I used a recursive Depth-First Search (DFS) approach to merge the two trees node by node based on their actual positions.

Here is how it works:
If root1 is null, I return root2.
If root2 is null, I return root1.
Otherwise, I create a new node whose value is the sum of root1.val and root2.val.
I recursively call mergeTrees on the left children of both nodes and assign the result to the merged node's left child.
I recursively call mergeTrees on the right children of both nodes and assign the result to the merged node's right child.
Finally, I return the merged node.

## Time Complexity
Time Complexity: O(n)

We visit each overlapping node once, where n is the minimum number of nodes between the two trees.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a skewed tree), the recursion call stack takes O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe mutating root1 directly instead of creating new nodes to save memory allocation overhead.