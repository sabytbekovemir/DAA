# 94. Binary Tree Inorder Traversal

## Problem
Given the root of a binary tree, return the inorder traversal of its nodes' values.

## Approach
I used a simple recursive helper function to perform the inorder traversal.

Here is how it works:
I create an empty list called result to hold node values.
I call a recursive helper function starting at the root.
If the current node is null, the function simply returns.
Otherwise, it first visits the left subtree recursively.
Then it adds the current node's value to the result list.
Finally, it visits the right subtree recursively.
After the traversal is done, I return the result list.

## Time Complexity
Time Complexity: O(n)

We visit each node exactly once, where n is the total number of nodes in the binary tree.

## Space Complexity
Space Complexity: O(n)

In the worst case (a skewed tree), the recursion stack will hold up to n function calls.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.