# 141. Linked List Cycle

## Problem
We are given the head of a linked list and need to determine if the linked list has a cycle in it. A cycle exists if some node in the list can be reached again by continuously following the next pointer.

## Approach
I used a two pointers approach with a slow pointer and a fast pointer. To be honest, I kinda cheated on this one because I randomly saw the solution in a Reels video.

Here is how it works:
If head is null, there is no cycle, so I return false right away.
I initialize two pointers, slow and fast, both starting at head.
While fast and fast.next are not null, I move slow forward by 1 step and fast forward by 2 steps.
If there is a cycle, the fast pointer will eventually catch up to the slow pointer, meaning slow == fast. When this happens, I return true.
If the loop ends because fast reaches null, it means the list has an end and no cycle exists, so I return false.

## Time Complexity
Time Complexity: O(n)

If there is no cycle, the fast pointer reaches the end of the list in n / 2 steps. If there is a cycle, the fast pointer catches up to the slow pointer within the loop iterations proportional to the list size n.

## Space Complexity
Space Complexity: O(1)

We only use two pointers (slow and fast) to traverse the list, so no extra memory is allocated.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.