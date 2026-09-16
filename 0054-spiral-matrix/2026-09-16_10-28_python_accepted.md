# 54. Spiral Matrix
  
<br>**Problem:** https://leetcode.com/problems/spiral-matrix/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 10:28 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 57.249100000000006%)


<!-- leetgit:submissionId=2143275084 codeHash=73b92925154a37cfa835e2101292c0f69955a788a4200a05eb53feb85e5ab667 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def spiralOrder(self, matrix):
        ans = []
        while matrix:
            ans += matrix.pop(0)
            matrix = [list(x) for x in zip(*matrix)][::-1]
        return ans
```
