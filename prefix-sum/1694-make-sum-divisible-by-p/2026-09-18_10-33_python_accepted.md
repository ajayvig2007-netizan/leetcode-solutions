# 1694. Make Sum Divisible by P
  
<br>**Problem:** https://leetcode.com/problems/make-sum-divisible-by-p/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 10:33 local time

**Runtime:** 88 ms (beats 24.747100000000035%)
**Memory:** 30.1 MB (beats 13.636100000000003%)


<!-- leetgit:submissionId=2145372470 codeHash=67bd8606b478f40c1e6540d0ad1845d4c1c4de05052069b14e082dbf73e9cedc notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minSubarray(self, nums, p):
        total = sum(nums)
        need = total % p

        if need == 0:
            return 0

        mp = {0: -1}
        curr = 0
        ans = len(nums)

        for i in range(len(nums)):
            curr = (curr + nums[i]) % p

            target = (curr - need) % p

            if target in mp:
                ans = min(ans, i - mp[target])

            mp[curr] = i

        if ans == len(nums):
            return -1

        return ans
```
