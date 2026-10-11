# 45. Jump Game II
  
<br>**Problem:** https://leetcode.com/problems/jump-game-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 09:58 local time

**Runtime:** 3 ms (beats 97.31940000000002%)
**Memory:** 13 MB (beats 81.67309999999999%)


<!-- leetgit:submissionId=2164884760 codeHash=b6d7e72fde85a644d5095db566386ca289e3f93ad0df87c2e6cf18713edec691 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def jump(self, nums):
        flag=0
        start=0
        count=0
        for r in range(len(nums)-1):
            flag=max(nums[r]+r,flag)  
            if r==start:
                count+=1
                start=flag
                      
        return count
                

        
        
```
