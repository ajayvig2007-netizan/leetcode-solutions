# 42. Trapping Rain Water
  
<br>**Problem:** https://leetcode.com/problems/trapping-rain-water/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Two Pointers, Dynamic Programming, Stack, Monotonic Stack<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 17:41 local time

**Runtime:** 4 ms (beats 83.57860000000001%)
**Memory:** 21 MB (beats 85.1546%)


<!-- leetgit:submissionId=2149684946 codeHash=e6a2ac877852e38eb48ab41740dceb1ec76aaf71a0d514fbbc394ccd2036f64e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
