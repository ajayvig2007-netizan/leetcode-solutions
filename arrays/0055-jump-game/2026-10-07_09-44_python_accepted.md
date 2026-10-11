# 55. Jump Game
  
<br>**Problem:** https://leetcode.com/problems/jump-game/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 09:44 local time

**Runtime:** 29 ms (beats 71.90350000000002%)
**Memory:** 13.2 MB (beats 61.617999999999995%)


<!-- leetgit:submissionId=2164873140 codeHash=0ecfa8f74023b4eb845a773e71afe876716f5ef498288916c67abb3bd561c047 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canJump(self, nums):
        flag=0
        for r in range(len(nums)):
            if r>flag:
                return False
            if flag>=len(nums)-1:
                return True
            if flag<nums[r]+r:
                flag=nums[r]+r
        
```
