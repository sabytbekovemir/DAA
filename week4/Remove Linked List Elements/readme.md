# 203. Remove Linked List Elements

## Problem
Given the head of a linked list and an integer val, remove all the nodes of the linked list that have Node.val == val, and return the new head.

## Approach
I used a dummy node to easily handle edge cases, such as when the head itself needs to be removed.

Here is how it works:
I create a dummy node that points to head, and set a current pointer starting at dummy.
While current.next is not null, I check if current.next.val is equal to target val.
If it is equal, I skip the next node by doing current.next = current.next.next.
If it is not equal, I just move current to current.next.
Finally, I return dummy.next, which is the head of the updated list.

## Time Complexity
Time Complexity: O(n)

We traverse the list once, visiting each node one time where n is the number of nodes in the list.

## Space Complexity
Space Complexity: O(1)

We only use a dummy node and a current pointer variable, so no extra memory is allocated proportional to input size.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.