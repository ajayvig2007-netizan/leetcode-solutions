# 42. Trapping Rain Water
  
<br>**Problem:** https://leetcode.com/problems/trapping-rain-water/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Two Pointers, Dynamic Programming, Stack, Monotonic Stack<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 10:37 local time

**Runtime:** 7 ms (beats 72.48580000000001%)
**Memory:** 21.2 MB (beats 25.711600000000008%)


<!-- leetgit:submissionId=2156680804 codeHash=e6a2ac877852e38eb48ab41740dceb1ec76aaf71a0d514fbbc394ccd2036f64e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def trap(self, height: list[int]) -> int:
        if len(height) == 0:
            return 0

        l, r = 0, len(height)-1
        leftmax = height[l]
        rightmax = height[r]
        res = 0

        while l < r:
            if leftmax < rightmax:
                l += 1
                leftmax = max(leftmax, height[l])
                res += leftmax - height[l]
            else:
                r -= 1
                rightmax = max(rightmax, height[r])
                res += rightmax - height[r]

        return res
```
