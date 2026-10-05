# 55. Jump Game
  
<br>**Problem:** https://leetcode.com/problems/jump-game/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 09:17 local time

**Runtime:** 39 ms (beats 40.93760000000001%)
**Memory:** 13.2 MB (beats 61.7408%)


<!-- leetgit:submissionId=2162671674 codeHash=c93a2d432df3f9f64fcad6c9dff7ded0f7eea73762a47a01c44ada2792e66699 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canJump(self, nums):
        len1=0
        for i in range(0,len(nums)):
            if len1<i:
                return False
            len1=max(i+nums[i],len1)
            if len1>=len(nums)-1:
                return True
        return False
        
        
```
