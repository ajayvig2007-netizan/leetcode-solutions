# 882. Peak Index in a Mountain Array
  
<br>**Problem:** https://leetcode.com/problems/peak-index-in-a-mountain-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Ternary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 21:50 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 21.6 MB (beats 73.2855%)


<!-- leetgit:submissionId=2156190527 codeHash=dc7c76e28a673042201baaf208698182262ae2edfda055d60c4527dbbb0cb365 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def peakIndexInMountainArray(self, arr):
        l = 0
        r = len(arr) - 1

        while l<r:
            mid=(l+r)//2
            if arr[mid]<arr[mid + 1]:
                l=mid+1
            else:
                r=mid

        return l
```
