# 162. Find Peak Element
  
<br>**Problem:** https://leetcode.com/problems/find-peak-element/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 17:36 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 55.55280000000001%)


<!-- leetgit:submissionId=2157046085 codeHash=3301323e4642b03c63c4e456733c7f0c861abd2cabb844d0305ede1cbf57c0cd notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findPeakElement(self, nums):
        l=0
        r=len(nums)-1
        while l<r:
            mid=(l+r)//2
            if nums[mid]>nums[mid+1]:
                r=mid
            else:
                l=mid+1
        return l
```
