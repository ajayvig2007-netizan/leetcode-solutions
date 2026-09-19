# 1501. Circle and Rectangle Overlapping
  
<br>**Problem:** https://leetcode.com/problems/circle-and-rectangle-overlapping/<br>

**Difficulty:** Medium<br>
**Topics:** Math, Geometry<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-19 08:58 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.4 MB (beats 18.666600000000003%)


<!-- leetgit:submissionId=2146240704 codeHash=e69f5edfcdf159508b55dd9291903f9871b8d68d685eea1e680fd78b568b288b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def checkOverlap(self, radius: int, xCenter: int, yCenter: int,
                     x1: int, y1: int, x2: int, y2: int) -> bool:

        x = max(x1, min(xCenter, x2)) - xCenter
        y = max(y1, min(yCenter, y2)) - yCenter

        return x * x + y * y <= radius * radius
```
