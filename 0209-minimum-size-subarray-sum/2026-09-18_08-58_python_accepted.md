# 209. Minimum Size Subarray Sum
  
<br>**Problem:** https://leetcode.com/problems/minimum-size-subarray-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 08:58 local time

**Runtime:** 32 ms (beats 13.93790000000002%)
**Memory:** 19.4 MB (beats 88.42060000000002%)


<!-- leetgit:submissionId=2145299646 codeHash=2690ff8b3c8c454644869639ff3f80001bc5b301d0d74f847023d503a49cdf30 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minSubArrayLen(self, target, nums):
        r=0
        l=0
        min1=float('inf')
        sum1=0
        while r<len(nums):
            sum1+=nums[r]
            while sum1>=target:
                min1=min(r-l+1,min1)
                sum1-=nums[l]
                l+=1
            r+=1
        if min1==float('inf'):
            return 0
        return min1

        
```
