# 39. Combination Sum
  
<br>**Problem:** https://leetcode.com/problems/combination-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Backtracking<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-26 16:25 local time

**Runtime:** 31 ms (beats 8.001900000000017%)
**Memory:** 12.6 MB (beats 19.79310000000001%)


<!-- leetgit:submissionId=2153789986 codeHash=af59a28621be43a3a7d79e3215ce3b0ae05a78053422f998293542b68a769e08 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def combinationSum(self, nums, k):
        ans=[]
        part=[]
        def dfs(i):
            if sum(part)==k:
                if part not in ans:
                    ans.append(part[:])
                return
            if sum(part)>k:
                return
            for j in range(i,len(nums)):
                part.append(nums[j])
                dfs(j)
                part.pop()
        dfs(0)
        return ans

        
```
