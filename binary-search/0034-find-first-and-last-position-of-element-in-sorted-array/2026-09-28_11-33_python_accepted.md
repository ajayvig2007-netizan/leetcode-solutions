# 34. Find First and Last Position of Element in Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 11:33 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.1 MB (beats 70.2558%)


<!-- leetgit:submissionId=2155632404 codeHash=350037ce7d94ba706dcb494c3cce4819b86a3c21ce2185bb2dd25ef360da5942 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchRange(self, nums, target):
        ans = [-1, -1]
        l = 0
        r = len(nums) - 1
        while l <= r:
            mid = (l + r) // 2
            if nums[mid] == target:
                ans[0] = mid
                r = mid - 1
            elif nums[mid] < target:
                l = mid + 1
            else:
                r = mid - 1
        l = 0
        r = len(nums) - 1
        while l <= r:
            mid = (l + r) // 2
            if nums[mid] == target:
                ans[1] = mid
                l = mid + 1
            elif nums[mid] < target:
                l = mid + 1
            else:
                r = mid - 1
        return ans
```
