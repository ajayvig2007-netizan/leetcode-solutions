# 189. Rotate Array
  
<br>**Problem:** https://leetcode.com/problems/rotate-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 09:08 local time

**Runtime:** 148 ms (beats 22.895599999999966%)
**Memory:** 26.8 MB (beats 49.050000000000004%)


<!-- leetgit:submissionId=2144254512 codeHash=3b35eb03059fc5ccb7d69fb53bf225580bb15d4838811f2315113711225bf0aa notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def rotate(self, nums, k):
        k %= len(nums)

        def reverse(l, r):
            while l < r:
                nums[l], nums[r] = nums[r], nums[l]
                l += 1
                r -= 1

        reverse(0, len(nums)-1)
        reverse(0, k-1)
        reverse(k, len(nums)-1)
```
