# 882. Peak Index in a Mountain Array
  
<br>**Problem:** https://leetcode.com/problems/peak-index-in-a-mountain-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Ternary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 17:51 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 21.5 MB (beats 73.3924%)


<!-- leetgit:submissionId=2157057622 codeHash=9dded8a9f125b15f79fba08d2ae2f35f1be13920e26b89eb34e8725368271b0f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def peakIndexInMountainArray(self, arr):
        l=0
        r=len(arr)-1
        while l<r:
            mid=(l+r)//2
            if arr[mid]>arr[mid+1]:
                r=mid
            else:
                l=mid+1
        return r
        
```
