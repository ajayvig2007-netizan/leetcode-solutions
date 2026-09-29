# 162. Find Peak Element
  
<br>**Problem:** https://leetcode.com/problems/find-peak-element/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 22:12 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 55.7055%)


<!-- leetgit:submissionId=2156218476 codeHash=4404ee694f88e54ac82b9ecfc26f274c428dd8fa3ad64c302b832af2686f2906 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findPeakElement(self, nums):
        l = 0
        r = len(nums) - 1

        while l < r:
            mid = (l + r) // 2

            if nums[mid] > nums[mid + 1]:
                r = mid
            else:
                l = mid + 1

        return l
```
