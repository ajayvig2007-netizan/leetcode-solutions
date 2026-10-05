# 45. Jump Game II
  
<br>**Problem:** https://leetcode.com/problems/jump-game-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 09:54 local time

**Runtime:** 7 ms (beats 80.6628%)
**Memory:** 13.1 MB (beats 81.49619999999999%)


<!-- leetgit:submissionId=2162698424 codeHash=923948991e72a2e53b3f6abd0381a2d5dbea826d71a39f216b8a9f11dbf1085f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def jump(self, nums):
        count=0
        len1=0
        end=0
        for i in range(len(nums)-1):
            len1=max(len1,nums[i]+i)
            if i==end:
                count+=1
                end=len1
        
        return count
        
        
```
