# 257. Binary Tree Paths

## Problem
Given the root of a binary tree, return all root-to-leaf paths in any order.

## Approach
I struggled with this problem for a long time, so I googled it and found the Depth-First Search (DFS) approach.

Here is how it works:
I create a list called result to store all formatted paths.
I call a recursive helper function dfs starting from the root with an empty initial path string.
At each node, if it is a leaf (both left and right children are null), I append the node's value to the current path string and add it to result.
If the node has children, I append the node's value followed by "->" to the path string and recursively visit existing left and right children.
Finally, I return the result list.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree at most once, where n is the number of nodes.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a skewed tree), the recursion call stack takes O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe using StringBuilder instead of String concatenation for performance optimization in larger trees.