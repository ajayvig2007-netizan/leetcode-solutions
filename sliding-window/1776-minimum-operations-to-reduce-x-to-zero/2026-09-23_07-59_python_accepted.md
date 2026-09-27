# 1776. Minimum Operations to Reduce X to Zero
  
<br>**Problem:** https://leetcode.com/problems/minimum-operations-to-reduce-x-to-zero/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Binary Search, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-23 07:59 local time

**Runtime:** 88 ms (beats 70.12940000000002%)
**Memory:** 20.8 MB (beats 12.987000000000018%)


<!-- leetgit:submissionId=2150335184 codeHash=a4b1470a429e576ba44098de2da5e2302397b732686ae772762248ee48e568a5 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution:
    def minOperations(self, nums, x):
        n = len(nums)
        total = sum(nums)
        target = total - x

        if target < 0:
            return -1

        if target == 0:
            return n

        left = 0
        s = 0
        longest = -1

        for right in range(n):

            s += nums[right]

            while left <= right and s > target:
                s -= nums[left]
                left += 1

            if s == target:
                longest = max(longest, right - left + 1)

        return -1 if longest == -1 else n - longest
```
