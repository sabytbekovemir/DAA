# 226. Invert Binary Tree

## Problem
Given the root of a binary tree, invert the tree, and return its root.

## Approach
I used a simple recursive approach to invert the binary tree by swapping the left and right subtrees at each node.

Here is how it works:
If the root is null, I return null.
I save the left child in a temporary variable.
I recursively invert the right subtree and assign it to root.left.
I recursively invert the left subtree (using the stored temporary variable) and assign it to root.right.
Finally, I return root.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree exactly once, where n is the number of nodes.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a completely skewed tree), the recursion stack takes O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.