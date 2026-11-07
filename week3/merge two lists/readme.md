# 21. Merge Two Sorted Lists

## Problem
We are given the heads of two sorted linked lists, list1 and list2. We need to merge the two lists into one sorted linked list and return its head.

## Approach
I used an iterative approach with a dummy node to build the new sorted list. At first I did not understand how and why to use a dummy node and what it is, so I asked Gemini to explain it to me.

Here is how it works:
I create a dummy node to serve as the start of the new list and a current pointer to keep track of the end.
While both list1 and list2 are not null, I compare their current values.
If list1 value is smaller or equal, I connect current.next to list1 and move list1 to its next node.
Otherwise, I connect current.next to list2 and move list2 to its next node.
Then I move current to current.next.
After the loop, if one of the lists still has remaining nodes, I attach it to the end of current.
Finally, I return dummy.next, which is the head of the merged list.

## Time Complexity
Time Complexity: O(n + m)

We iterate through both lists node by node. The total number of steps depends on the total length of list1 (n) and list2 (m).

## Space Complexity
Space Complexity: O(1)

We only reuse the existing list nodes and change their pointers using a few variables like dummy and current. No extra memory is allocated.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.