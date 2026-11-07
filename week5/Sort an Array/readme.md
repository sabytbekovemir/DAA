# 912. Sort an Array

## Problem
Given an array of integers nums, sort the array in ascending order and return it.

## Approach
Simple sorting methods like bubble sort are too slow for this problem, so I used merge sort. 

Here is how it works:
I divide the array into two halves until each sub-array contains only one element.
Then I merge the smaller sorted arrays back together step by step.
To merge two sorted parts, I use a temporary array and two pointers to compare elements from the left and right sides.
I pick the smaller element and put it into the temporary array, moving the pointer forward.
After both sides are fully compared and remaining elements are copied over, I copy everything back into the original nums array.

## Time Complexity
Time Complexity: O(n log n)

Dividing the array takes O(log n) steps, and merging elements at each level takes O(n) time.

## Space Complexity
Space Complexity: O(n)

We need extra space for the temporary array during the merge step.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.