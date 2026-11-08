# 104. Maximum Depth of Binary Tree

## Problem
Given the root of a binary tree, return its maximum depth.

## Approach
I used a simple recursive post-order traversal to calculate the height of the tree.

Here is how it works:
If the root is null, the tree depth is 0, so I return 0.
I recursively call maxDepth on the left subtree to find its height.
I recursively call maxDepth on the right subtree to find its height.
I take the maximum depth between the left and right subtrees and add 1 for the current node.
Finally, I return this calculated height.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree exactly once.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a completely skewed tree), the recursion stack will take O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.