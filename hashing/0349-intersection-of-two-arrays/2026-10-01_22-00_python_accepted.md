# 349. Intersection of Two Arrays
  
<br>**Problem:** https://leetcode.com/problems/intersection-of-two-arrays/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Two Pointers, Binary Search, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 22:00 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.7 MB (beats 31.2935%)


<!-- leetgit:submissionId=2159395287 codeHash=90485d8df494f7385aa71402a993441407c4bda0b72caa068c00fdac115bb28b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def intersection(self, nums1, nums2):
        nums1=set(nums1)
        nums2=set(nums2)
        ans=[]
        if len(nums1)>len(nums2):
            for i in nums2:
                if i in nums1:
                    ans.append(i)
        else:
            for i in nums1:
                if i in nums2:
                    ans.append(i)
        return ans

```
