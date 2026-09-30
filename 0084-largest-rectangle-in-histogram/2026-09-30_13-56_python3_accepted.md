# 84. Largest Rectangle in Histogram
  
<br>**Problem:** https://leetcode.com/problems/largest-rectangle-in-histogram/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Stack, Monotonic Stack, Range Minimum/Maximum Query<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 13:56 local time

**Runtime:** 203 ms (beats 12.99219999999991%)
**Memory:** 31 MB (beats 72.6891%)


<!-- leetgit:submissionId=2157958090 codeHash=ecddc3e0bf60533dce121bad3fca9035910e29ff6072fd81ee90a888a0af1782 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
# Python
class Solution:
    def largestRectangleArea(self, heights: List[int]) -> int:
        n = len(heights)
        left, right = [-1]*n, [n]*n
        stack = []

        # Nearest Smaller to Left
        for i in range(n):
            while stack and heights[stack[-1]] >= heights[i]:
                stack.pop()
            left[i] = stack[-1] if stack else -1
            stack.append(i)

        stack.clear()

        # Nearest Smaller to Right
        for i in range(n-1, -1, -1):
            while stack and heights[stack[-1]] >= heights[i]:
                stack.pop()
            right[i] = stack[-1] if stack else n
            stack.append(i)

        max_area = 0
        for i in range(n):
            width = right[i] - left[i] - 1
            max_area = max(max_area, heights[i] * width)

        return max_area
```
