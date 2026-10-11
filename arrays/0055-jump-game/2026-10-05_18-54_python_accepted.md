# 55. Jump Game
  
<br>**Problem:** https://leetcode.com/problems/jump-game/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:54 local time

**Runtime:** 39 ms (beats 40.93760000000001%)
**Memory:** 13.3 MB (beats 61.7408%)


<!-- leetgit:submissionId=2163151308 codeHash=5e0100edc89cea143bfbb1e626edf0cbb37d3bc63e78ada878998b219c9977d7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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

        # return False
        
```
