# 88. Merge Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/merge-sorted-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 13:46 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 58.43420000000002%)


<!-- leetgit:submissionId=2144496011 codeHash=5378fb60a308ebe958da0b736a8abf3fa9c27e23d1a0c8fc3a7efacf59303f63 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def merge(self, nums1, m, nums2, n):
        nums1[:]=nums1[:m]
        nums1[:]=sorted(nums1+nums2)

        
        
```
