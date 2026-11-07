# 704. Binary Search

## Problem
We need to find a target number in an array that is already sorted. If the target exists, we return its index. If not, we return -1.

## Approach
At first, I solved it using a simple for loop. It worked, but it was kinda slow.

Then I changed it to a while loop with two pointers (left and right) to get O(log n) time complexity.

Here is how it works:
I set left to 0 and right to the end of the array.
While left is less than or equal to right, I calculate the middle index: mid = (left + right) / 2.
If nums[mid] equals the target, I return mid right away.
If nums[mid] is greater than target, it means the target is on the left side, so I update right = mid - 1.
If it is smaller, it means the target is on the right side, so I update left = mid + 1.
If the loop ends and nothing is found, I return -1.

## Time Complexity
Time Complexity: O(log n)

In every step of the loop, the array is split in half and one half is discarded. Because of this, the number of steps grows very slowly, which is log n.

## Space Complexity
Space Complexity: O(1)

I only use three variables: left, right, and mid. No extra arrays are created, so memory usage does not depend on the input size.

## Reflection / Improvement
In terms of complexity, O(log n) time and O(1) space is already optimal.

Things that could be improved in the code:
Honestly, see nothing to improve.