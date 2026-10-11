# 55. Jump Game
  
<br>**Problem:** https://leetcode.com/problems/jump-game/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:55 local time

**Runtime:** 30 ms (beats 69.93160000000002%)
**Memory:** 13.3 MB (beats 61.7408%)


<!-- leetgit:submissionId=2163151753 codeHash=ee5f761c06f6ed18eca3149b39e740314df8577c1b3eda83596b657c45153a42 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canJump(self, nums):
        flag=0
        start=0
        for i in range(len(nums)):
            if i>start:
                return False
            if start>=len(nums)-1:
                return True
            flag=max(flag,nums[i]+i)
            start=flag
        
```
