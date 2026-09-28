# 34. Find First and Last Position of Element in Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 19:49 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.1 MB (beats 29.898599999999995%)


<!-- leetgit:submissionId=2156057130 codeHash=d3eab68b6d0517649a9ff6bcadf67d1972f766e36299d66c92a2130bbaec33b6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchRange(self, nums, target):
        l = 0
        r = len(nums) - 1
        ans = [-1, -1]

        while l <= r:
            mid = (l + r) // 2

            if nums[mid] == target:

                # find first
                x = mid
                while x >= 0 and nums[x] == target:
                    x -= 1
                ans[0] = x + 1

                # find last
                x = mid
                while x < len(nums) and nums[x] == target:
                    x += 1
                ans[1] = x - 1

                break

            elif nums[mid] > target:
                r = mid - 1
            else:
                l = mid + 1

        return ans
```
