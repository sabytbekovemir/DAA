# 148. Sort List

## Problem
Given the head of a linked list, return the list after sorting it in ascending order.

## Approach
I could not figure out how to solve this on my own, so I googled the approach and recreated it. I used merge sort on the linked list because it provides O(n log n) time complexity.

Here is how it works:
If head is null or head.next is null, the list is already sorted, so I return head right away.
I use two pointers, slow and fast, to find the middle node of the list and split the list into two halves.
I recursively call sortList on the left half and the right half.
Then I use a helper merge function with a dummy node to combine the two sorted halves back together into a single sorted list.
Finally, I return dummy.next from the merge step.

## Time Complexity
Time Complexity: O(n log n)

Splitting the list in half takes O(log n) recursive levels, and merging the lists at each level takes O(n) time.

## Space Complexity
Space Complexity: O(log n)

The recursion stack takes memory proportional to the height of the split tree, which is O(log n).

## Reflection / Improvement
Things that could be improved in the code:
As far as I know, there is nothing to fix here, unless I missed something.