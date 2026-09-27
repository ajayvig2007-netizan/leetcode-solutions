# 78. Subsets
  
<br>**Problem:** https://leetcode.com/problems/subsets/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Backtracking, Bit Manipulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-26 15:43 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 58.8077%)


<!-- leetgit:submissionId=2153758811 codeHash=b61b2bd508e02af1634fc969d9bb2922e4c1941cb682836584d1975baed94ddf notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def subsets(self, nums):
        ans=[]
        part=[]
        def dfs(i):
            ans.append(part[:])
            for j in range(i,len(nums)):
                part.append(nums[j])
                dfs(j+1)
                part.pop()
        dfs(0)
        return ans
        
```
