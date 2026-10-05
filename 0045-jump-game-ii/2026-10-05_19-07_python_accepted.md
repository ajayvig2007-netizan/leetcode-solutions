# 45. Jump Game II
  
<br>**Problem:** https://leetcode.com/problems/jump-game-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 19:07 local time

**Runtime:** 4 ms (beats 93.0681%)
**Memory:** 13.2 MB (beats 22.689299999999992%)


<!-- leetgit:submissionId=2163163979 codeHash=a3a6598a7486ba18aa1ca93887034827a64511bbf4d5bcc1d3ec9369aa22a9fc notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def jump(self, nums):
        start=0
        flag=0
        count=0
        for i in range(len(nums)-1):
            flag=max(flag,nums[i]+i)
            if start==i:
                count+=1
                start=flag
        return count
                
        
```
