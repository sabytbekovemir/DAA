# 144. Binary Tree Preorder Traversal

## Problem
Given the root of a binary tree, return the preorder traversal of its nodes' values.

## Approach
I solved this problem on my own using a simple recursive helper function to perform the preorder traversal (Root -> Left -> Right). Almost same as inorder traversal.

Here is how it works:
I create an empty list called result to store node values.
I call a recursive helper function starting at the root.
If the current node is null, the function simply returns.
Otherwise, it first adds the current node's value to the result list.
Then it recursively visits the left subtree.
Finally, it recursively visits the right subtree.
After traversing the tree, I return the result list.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree exactly once, where n is the number of nodes.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a skewed tree), the recursion stack will hold up to n function calls.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.