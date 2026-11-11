# 404. Sum of Left Leaves

## Problem
Given the root of a binary tree, return the sum of all left leaves.

## Approach
I used a recursive Depth-First Search (DFS) approach to identify and sum up only the nodes that are left leaves.

Here is how it works:
If the root is null, I return 0.
I check if the left child exists and if it is a leaf (has no left or right children).
If it is a left leaf, I add its value to the total sum and recursively process the right subtree.
Otherwise, if the left child is not a leaf, I recursively call sumOfLeftLeaves on both the left and right subtrees.
Finally, I return the calculated sum.

## Time Complexity
Time Complexity: O(n)

We visit each node in the binary tree at most once.

## Space Complexity
Space Complexity: O(n)

In the worst-case scenario (a skewed tree), the recursion call stack takes O(n) space.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.