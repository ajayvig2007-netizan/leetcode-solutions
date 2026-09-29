# 33. Search in Rotated Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/search-in-rotated-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 19:32 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 10.4546%)


<!-- leetgit:submissionId=2157153957 codeHash=3124ab3b53909aea1fbd5df15f8f91206779caf789f671c9a9fd39ca993ce83e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):

    def search(self, nums, target):

        l = 0
        r = len(nums) - 1
        p = -1

        while l <= r:

            mid = (l + r) // 2

            if mid < r and nums[mid] > nums[mid + 1]:
                p = mid
                break

            if mid > l and nums[mid] < nums[mid - 1]:
                p = mid - 1
                break

            if nums[mid] >= nums[l]:
                l = mid + 1
            else:
                r = mid - 1

        if p == -1:
            l = 0
            r = len(nums) - 1
        elif target >= nums[0]:
            l = 0
            r = p
        else:
            l = p + 1
            r = len(nums) - 1

        while l <= r:

            mid = (l + r) // 2

            if nums[mid] == target:
                return mid

            if nums[mid] < target:
                l = mid + 1
            else:
                r = mid - 1

        return -1
```
