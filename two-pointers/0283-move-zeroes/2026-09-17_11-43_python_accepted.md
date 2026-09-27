# 283. Move Zeroes
  
<br>**Problem:** https://leetcode.com/problems/move-zeroes/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 11:43 local time

**Runtime:** 7 ms (beats 56.370499999999986%)
**Memory:** 13.5 MB (beats 50.17029999999998%)


<!-- leetgit:submissionId=2144393972 codeHash=179c54602a5f4710e9d07a1978f6b8b186f5243e3afec2615626d60d7ece9207 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def moveZeroes(self, nums):
        j = 0

        for i in range(len(nums)):
            if nums[i] != 0:
                nums[i], nums[j] = nums[j], nums[i]
                j += 1
```
