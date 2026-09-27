# 643. Maximum Average Subarray I
  
<br>**Problem:** https://leetcode.com/problems/maximum-average-subarray-i/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 09:59 local time

**Runtime:** 151 ms (beats 10.619399999999995%)
**Memory:** 19.1 MB (beats 51.71670000000002%)


<!-- leetgit:submissionId=2140241092 codeHash=e01144fffa44abc79cd8e6e83de6820556f3eac032f2b92350a556176b55963b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findMaxAverage(self, nums, k):
        l=0
        sum1=0
        max1=float('-inf')
        avg=0
        for r in range(len(nums)):
            sum1+=nums[r]
            if r-l+1==k:
                avg=sum1/(k*1.00)
                max1=max(max1,avg)
                sum1-=nums[l]
                l+=1
        return float(max1)
            

        
        
```
