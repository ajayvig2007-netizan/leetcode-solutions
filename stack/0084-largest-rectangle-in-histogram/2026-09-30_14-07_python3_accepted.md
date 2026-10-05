# 84. Largest Rectangle in Histogram
  
<br>**Problem:** https://leetcode.com/problems/largest-rectangle-in-histogram/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Stack, Monotonic Stack, Range Minimum/Maximum Query<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 14:07 local time

**Runtime:** 200 ms (beats 13.73969999999991%)
**Memory:** 30.9 MB (beats 83.6827%)


<!-- leetgit:submissionId=2157967174 codeHash=fe2e5e6452876b50bd96b2095dd85309becb4a0c21ebd60093df223cd3e9e1ba notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
# Python
class Solution:
    def largestRectangleArea(self, heights: List[int]) -> int:
        n = len(heights)
        left, right = [-1]*n, [n]*n
        stack = []

        for i in range(n):
            while stack and heights[stack[-1]] >= heights[i]:
                stack.pop()
            left[i] = stack[-1] if stack else -1
            stack.append(i)

        stack.clear()

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
