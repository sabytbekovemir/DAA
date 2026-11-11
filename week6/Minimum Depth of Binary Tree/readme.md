# 111. Minimum Depth of Binary Tree

## Problem
Given a binary tree, find its minimum depth.

## Approach
I used a recursive post-order traversal to calculate the minimum depth to a leaf node.

Here is how it works:
If the root is null, the depth is 0, so I return 0.
If the left child is null, I must continue searching in the right subtree.
If the right child is null, I must continue searching in the left subtree.
If both children exist, I take the minimum depth between the left and right subtrees and add 1 for the current node.
Finally, I return this calculated minimum depth.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree at most once.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a completely skewed tree), the recursion stack takes O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.