# 792. Binary Search
  
<br>**Problem:** https://leetcode.com/problems/binary-search/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 08:43 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.4 MB (beats 38.0275%)


<!-- leetgit:submissionId=2155493324 codeHash=92c6f5100df67e047dd5702702bdeaf07334f1f2041805e69a621c98d85dd567 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def search(self, nums, target):
        l=0
        r=len(nums)-1
        mid=0
        while(l<=r):
            mid=(l+r)//2
            if nums[mid]==target:
                return mid
            elif nums[mid]>target:
                r=mid-1
            else:
                l=mid+1
        return -1

      
```
