# 33. Search in Rotated Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/search-in-rotated-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 18:22 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 10.4546%)


<!-- leetgit:submissionId=2157082867 codeHash=1962b7fcfb6eb3ff3a074e3cfade0608b7bc5d79eb8d1bfc1625b730176a86cd notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def search(self, nums, target):

        l = 0
        r = len(nums) - 1

        while l <= r:

            mid = (l + r) // 2

            if nums[mid] == target:
                return mid

            if nums[l] <= nums[mid]:

                if nums[l] <= target < nums[mid]:
                    r = mid - 1
                else:
                    l = mid + 1

            else:

                if nums[mid] < target <= nums[r]:
                    l = mid + 1
                else:
                    r = mid - 1

        return -1
```
