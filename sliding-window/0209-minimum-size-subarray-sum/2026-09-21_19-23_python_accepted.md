# 209. Minimum Size Subarray Sum
  
<br>**Problem:** https://leetcode.com/problems/minimum-size-subarray-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 19:23 local time

**Runtime:** 19 ms (beats 98.85720000000002%)
**Memory:** 20 MB (beats 75.60570000000001%)


<!-- leetgit:submissionId=2148696434 codeHash=5a4c723c0d3a1a97c4441805a26f51d400af8682b85e90d5d2b59078b35ffd7f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minSubArrayLen(self, target, nums):
        l = 0
        sum1 = 0
        min1 = float("inf")

        for r in range(len(nums)):
            sum1 += nums[r]

            while sum1 >= target:
                min1 = min(min1, r - l + 1)
                sum1 -= nums[l]
                l += 1

        if min1 == float("inf"):
            return 0

        return min1
```
