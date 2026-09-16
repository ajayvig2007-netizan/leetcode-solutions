# 909. Stone Game
  
<br>**Problem:** https://leetcode.com/problems/stone-game/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Dynamic Programming, Minimax, Game Theory, Zero-Sum Game<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 11:43 local time

**Runtime:** 643 ms (beats 5.067900000000014%)
**Memory:** 47.8 MB (beats 5.050300000000025%)


<!-- leetgit:submissionId=2143346050 codeHash=fb89a2466971da0463024c48f6a5e2e4496d33dfbc13eef7606edc04eac2a570 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def stoneGame(self, piles):
        memo = {}
        
        def solve(l, r):
            if l == r:
                return piles[l]
            if (l, r) in memo:
                return memo[l, r]

            memo[l, r] = max(piles[l] - solve(l+1,r),
                             piles[r] - solve(l,r-1))
            return memo[l, r]

        return solve(0, len(piles)-1) > 0
```
