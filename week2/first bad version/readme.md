# 278. First Bad Version

## Problem
We are given n versions of a product and need to find the first bad version. We have an API isBadVersion(version) that tells us if a version is bad. Every version after a bad one is also bad.

## Approach
To get O(log n) time complexity, I used binary search with a while loop and two pointers.

Here is how it works:
I set left to 1 and right to n.
While left is less than right, I calculate the middle version: mid = (left + right) / 2.
If isBadVersion(mid) returns true, it means mid is bad, so the first bad version could be mid or somewhere on the left side. So I set right = mid.
If it returns false, mid is good, so the first bad version must be on the right side. So I set left = mid + 1.
When left and right meet, the loop stops, and left points to the first bad version.

## Time Complexity
Time Complexity: O(log n)

In every step, we split the search range in half, so the number of API calls grows very slowly as log n.

## Space Complexity
Space Complexity: O(1)

The solution only uses a few simple variables like left, right, and mid, so extra memory is constant.

## Reflection / Improvement
Things that could be improved in the code:
Honestly, see nothing to improve as well. Maybe some code decorations only.