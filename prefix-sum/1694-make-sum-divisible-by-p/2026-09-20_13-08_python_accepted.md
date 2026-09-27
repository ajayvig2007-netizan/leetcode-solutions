# 1694. Make Sum Divisible by P
  
<br>**Problem:** https://leetcode.com/problems/make-sum-divisible-by-p/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 13:08 local time

**Runtime:** 85 ms (beats 33.00960000000002%)
**Memory:** 30.1 MB (beats 14.563200000000009%)


<!-- leetgit:submissionId=2147455102 codeHash=638190c5d0c652d0dcf2496638919fbdc68451ac585be35f4abdffa1f63d9ea5 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minSubarray(self, nums, p):
        total = sum(nums)
        rem = total % p

        if rem == 0:
            return 0

        hashmap = {0: -1}
        prefix = 0
        ans = len(nums)

        for r in range(len(nums)):
            prefix += nums[r]

            need = (prefix - rem) % p

            if need in hashmap:
                ans = min(ans, r - hashmap[need])

            hashmap[prefix % p] = r

        if ans == len(nums):
            return -1

        return ans
        
```
