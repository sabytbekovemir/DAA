# 145. Binary Tree Postorder Traversal

## Problem
Given the root of a binary tree, return the postorder traversal of its nodes' values.

## Approach
I used a simple recursive helper function to perform the postorder traversal (Left -> Right -> Root).
Almost same as inorder and preorder traversals.

Here is how it works:
I create an empty list called result to store node values.
I call a recursive helper function starting at the root.
If the current node is null, the function simply returns.
Otherwise, it first visits the left subtree recursively.
Then it visits the right subtree recursively.
Finally, it adds the current node's value to the result list.
After the traversal is done, I return the result list.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree exactly once, where n is the number of nodes.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a completely skewed tree), the recursion stack will hold up to n function calls.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.