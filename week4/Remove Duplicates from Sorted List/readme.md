# 83. Remove Duplicates from Sorted List

## Problem
We are given the head of a sorted linked list. We need to delete all duplicates so that each element appears only once, and return the linked list sorted as well.

## Approach
Since the list is already sorted, duplicate numbers are right next to each other. I used a single pointer to go through the list and remove duplicates on the fly.

Here is how it works:
I set a current pointer to the head of the list.
While current and current.next are not null, I check if the value of current is equal to the value of current.next.
If they are equal, it means there is a duplicate. I skip the next node by setting current.next = current.next.next.
If they are different, I just move the current pointer forward to current.next.
Finally, I return head.

## Time Complexity
Time Complexity: O(n)

We traverse the list once. In the worst case, we visit each node one time, where n is the number of nodes in the list.

## Space Complexity
Space Complexity: O(1)

We only use one pointer variable named current, so we do not use any extra memory.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.