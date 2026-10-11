# 55. Jump Game
  
<br>**Problem:** https://leetcode.com/problems/jump-game/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:53 local time

**Runtime:** 43 ms (beats 27.99770000000001%)
**Memory:** 13.3 MB (beats 29.9439%)


<!-- leetgit:submissionId=2163149950 codeHash=0d403ebcae50e2ebe8f6f5d41b742cf5d8ab40de995b55664b3b55c45d681c3f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canJump(self, nums):
        flag=0
        start=0
        # if len(nums)==1:
        #     return True
        # if nums[0]==0:
        #     return False
        for i in range(len(nums)):
            if i>start:
                return False
            if start>=len(nums)-1:
                return True
            flag=max(flag,nums[i]+i)
            start=flag

        return False
        
```
