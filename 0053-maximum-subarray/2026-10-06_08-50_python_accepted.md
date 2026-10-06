# 53. Maximum Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Divide and Conquer, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 08:50 local time

**Runtime:** 98 ms (beats 37.191400000000016%)
**Memory:** 21.3 MB (beats 46.09989999999999%)


<!-- leetgit:submissionId=2163736462 codeHash=4e01e3ece267ff6215c64d3430470e3c779787dfccdb56d390de5789f1e96f38 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
