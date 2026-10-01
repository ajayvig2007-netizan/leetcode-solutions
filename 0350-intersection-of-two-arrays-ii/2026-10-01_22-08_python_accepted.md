# 350. Intersection of Two Arrays II
  
<br>**Problem:** https://leetcode.com/problems/intersection-of-two-arrays-ii/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Two Pointers, Binary Search, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 22:08 local time

**Runtime:** 18 ms (beats 22.623100000000004%)
**Memory:** 12.6 MB (beats 29.704900000000023%)


<!-- leetgit:submissionId=2159403663 codeHash=703f1522b3891d4ef2567649296597536bab8df72dd482e2e87756d0363dfc6c notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def intersect(self, nums1, nums2):
        ans = []

        if len(nums1) > len(nums2):
            for i in nums2:
                if i in nums1:
                    ans.append(i)
                    nums1.remove(i)
        else:
            for i in nums1:
                if i in nums2:
                    ans.append(i)
                    nums2.remove(i)

        return (ans)
```
