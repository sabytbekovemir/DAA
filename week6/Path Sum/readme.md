# 112. Path Sum

## Problem
Given the root of a binary tree and an integer targetSum, return true if the tree has a root-to-leaf path such that adding up all the values along the path equals targetSum.

## Approach
My first thought was to go all the way to the right first, and if the path sum exceeds targetSum, stop and switch to the left sibling.
However, I realized this tree is a general Binary Tree, not a Binary Search Tree, and node values can be negative.
So going right first does not help, and we cannot simply prune paths when the sum exceeds targetSum.

Instead, I used a recursive approach by subtracting the current node's value from targetSum as I go down the tree.

Here is how it works:
If root is null, there is no path, so I return false.
If the current node is a leaf (both left and right children are null), I check if targetSum equals root.val.
Otherwise, I recursively call hasPathSum on the left and right subtrees with the updated targetSum (targetSum - root.val).
If either subtree finds a valid path, I return true.

## Time Complexity
Time Complexity: O(n)

We visit each node in the tree at most once.

## Space Complexity
Space Complexity: O(n)

In the worst case (a completely skewed tree), the call stack takes O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.