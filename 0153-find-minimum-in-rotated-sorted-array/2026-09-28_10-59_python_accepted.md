# 153. Find Minimum in Rotated Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 10:59 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.5 MB (beats 37.145700000000005%)


<!-- leetgit:submissionId=2155601771 codeHash=087b3b918993f5fbf50d91c650612e115d1aa9a1e4dad15300d372c50d75142b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findMin(self, nums):
        l=0
        r=len(nums)-1
        while l<r:
            mid=(l + r)//2
            if nums[mid]>nums[r]:
                l=mid+1
            else:
                r=mid
        return nums[l]
```
