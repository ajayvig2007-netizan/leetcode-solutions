# 643. Maximum Average Subarray I
  
<br>**Problem:** https://leetcode.com/problems/maximum-average-subarray-i/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 08:50 local time

**Runtime:** 151 ms (beats 10.690899999999985%)
**Memory:** 18.6 MB (beats 86.77729999999998%)


<!-- leetgit:submissionId=2145295130 codeHash=4408e4139f7303e838db645ccbd1d56886d2ac6573adb80434ad924af7c2d1ff notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findMaxAverage(self, nums, k):
        r=0
        max1=float("-inf")
        l=0
        sum1=0
        while r<len(nums):
            sum1+=nums[r]
            if r+1>=k:
                avg=float(sum1)/k
                max1=max(avg,max1)
                sum1-=nums[l]
                l+=1
            r+=1
        return max1

        
```
