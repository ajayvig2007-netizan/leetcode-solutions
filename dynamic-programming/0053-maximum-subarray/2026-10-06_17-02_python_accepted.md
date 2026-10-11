# 53. Maximum Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Divide and Conquer, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 17:02 local time

**Runtime:** 107 ms (beats 11.334900000000019%)
**Memory:** 21.2 MB (beats 70.66619999999999%)


<!-- leetgit:submissionId=2164171940 codeHash=09da621f93dbc2a213e756252bd18414d85ec31bcd3473f7e2be757b39b3da27 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxSubArray(self, nums):
        curr=nums[0]
        max1=nums[0]
        for r in range(1,len(nums)):
            curr=max(curr+nums[r],nums[r])
            max1=max(curr,max1)
        return max1
        
```
