# 3831. Find X Value of Array I
  
<br>**Problem:** https://leetcode.com/problems/find-x-value-of-array-i/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 08:09 local time

**Runtime:** 375 ms (beats 51.31550000000004%)
**Memory:** 34.4 MB (beats 32.8947%)


<!-- leetgit:submissionId=2148190183 codeHash=9893d341e12b75b7b6dedc97c8912cfe5de595ed9f37f40d8c2d75014fef764f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def resultArray(self, nums: List[int], k: int) -> List[int]:
        ans = [0] * k
        dp = [0] * k

        for num in nums:
            x = num % k
            nxt = [0] * k
            nxt[x] += 1

            for r in range(k):
                new_r = (r * x) % k
                nxt[new_r] += dp[r]

            for r in range(k):
                ans[r] += nxt[r]
            dp = nxt

        return ans
```
