# 234. Palindrome Linked List

## Problem
Given the head of a singly linked list, return true if it is a palindrome or false otherwise.

## Approach
I could not find an elegant solution using linked lists as they are, so I googled how to convert them into an array and did that instead.

Here is how it works:
I copy all node values into an ArrayList by traversing the linked list from head to end.
I initialize two pointers, left at 0 and right at the last index of the list.
While left is less than right, I compare the values at both positions.
If the values are not equal, the list is not a palindrome, so I return false.
If they match, I increment left and decrement right.
If the loop finishes without finding mismatched values, I return true.

## Time Complexity
Time Complexity: O(n)

Traversing the linked list to fill the ArrayList takes O(n) time, and checking the ArrayList with two pointers takes O(n) time.

## Space Complexity
Space Complexity: O(n)

We use an extra ArrayList to store all values from the linked list of length n.

## Reflection / Improvement
Things that could be improved in the code:
Maybe there is a way to solve this directly with linked lists without spending extra memory for the array.