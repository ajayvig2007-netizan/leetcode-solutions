# 954. Maximum Sum Circular Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-sum-circular-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Divide and Conquer, Dynamic Programming, Queue, Monotonic Queue<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 10:49 local time

**Runtime:** 103 ms (beats 62.9090999999999%)
**Memory:** 15 MB (beats 27.391799999999996%)


<!-- leetgit:submissionId=2163843065 codeHash=0a1942ca5f38f7b6ee055dd3cd0ed963196c262d0a043e017c8a9f363f75d9db notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxSubarraySumCircular(self, nums):
        total=nums[0]
        curr=nums[0]
        max1=nums[0]
        mincurr=nums[0]
        min1=nums[0]

        for i in range(1,len(nums)):
            total+=nums[i]

            curr=max(nums[i],curr+nums[i])
            max1=max(max1,curr)

            mincurr=min(nums[i],mincurr+nums[i])
            min1=min(min1,mincurr)

        if max1<0:
            return max1

        
        return max(max1,total-min1)
```
