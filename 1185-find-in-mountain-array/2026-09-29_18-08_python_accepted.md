# 1185. Find in Mountain Array
  
<br>**Problem:** https://leetcode.com/problems/find-in-mountain-array/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Binary Search, Interactive, Ternary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 18:08 local time

**Runtime:** 38 ms (beats 87.14290000000001%)
**Memory:** 13.5 MB (beats 9.285800000000002%)


<!-- leetgit:submissionId=2157070629 codeHash=3d9073df6a9de7494ef736e090e6d63f8cb58078c4808167807ed212d54e961d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findInMountainArray(self, target, mountainArr):

        l = 0
        r = mountainArr.length() - 1

        # Find peak
        while l < r:
            mid = (l + r) // 2

            if mountainArr.get(mid) > mountainArr.get(mid + 1):
                r = mid
            else:
                l = mid + 1

        peak = l

        # Search increasing part
        l = 0
        r = peak

        while l <= r:
            mid = (l + r) // 2
            x = mountainArr.get(mid)

            if x == target:
                return mid
            elif x < target:
                l = mid + 1
            else:
                r = mid - 1

        # Search decreasing part
        l = peak + 1
        r = mountainArr.length() - 1

        while l <= r:
            mid = (l + r) // 2
            x = mountainArr.get(mid)

            if x == target:
                return mid
            elif x > target:
                l = mid + 1
            else:
                r = mid - 1

        return -1
```
