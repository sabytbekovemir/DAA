# 160. Intersection of Two Linked Lists

## Problem
We are given the heads of two singly linked lists, headA and headB. We need to find the node at which the two lists intersect. If they do not intersect at all, return null.

## Approach
I could not come up with the optimal two-pointer trick, so I solved it using a nested loop approach. 

Here is how it works:
I set a pointer currentA to headA to iterate through the first list.
For every node in list A, I start another pointer currentB at headB and iterate through the entire second list.
Inside the inner loop, I check if currentA is equal to currentB.
If they point to the exact same node, I return currentA because that is the intersection point.
If the inner loop finishes without finding a match, I move currentA to the next node and repeat the process.
If both loops finish and no common node is found, I return null.

## Time Complexity
Time Complexity: O(n * m)

For each node in list A (length n), we potentially traverse all nodes in list B (length m). In the worst case, this results in quadratic-like time complexity.

## Space Complexity
Space Complexity: O(1)

We only use two pointer variables, currentA and currentB, so no extra memory is allocated.

## Reflection / Improvement
Things that could be improved in the code:
The time complexity is too slow for large inputs, so optimizing it to O(n + m) time using two pointers would be a clear improvement.