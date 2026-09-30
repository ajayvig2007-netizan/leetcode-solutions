# 84. Largest Rectangle in Histogram
  
<br>**Problem:** https://leetcode.com/problems/largest-rectangle-in-histogram/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Stack, Monotonic Stack, Range Minimum/Maximum Query<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 14:12 local time

**Runtime:** 136 ms (beats 29.85049999999993%)
**Memory:** 31.5 MB (beats 44.454499999999996%)


<!-- leetgit:submissionId=2157970623 codeHash=30ad2beb25cc792736a90ab3d68a644895866b63ebf6b7c80949624e02620634 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def largestRectangleArea(self, a):
        stack = []
        ans = 0

        for i in range(len(a) + 1):
            while stack and (i == len(a) or a[stack[-1]] > a[i]):
                h = a[stack.pop()]
                
                if stack:
                    w = i - stack[-1] - 1
                else:
                    w = i

                ans = max(ans, h * w)

            stack.append(i)

        return ans
```
