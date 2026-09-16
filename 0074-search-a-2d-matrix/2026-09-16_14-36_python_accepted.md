# 74. Search a 2D Matrix
  
<br>**Problem:** https://leetcode.com/problems/search-a-2d-matrix/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 14:36 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 33.150000000000006%)


<!-- leetgit:submissionId=2143484299 codeHash=b56053661b69f0f3ed2bfd28291f192a8471890864cc7261e30f01fe78bfd494 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchMatrix(self, matrix, target):
        m, n = len(matrix), len(matrix[0])
        lo, hi = 0, m * n - 1
        while lo <= hi:
            mid = (lo + hi) // 2
            val = matrix[mid // n][mid % n]
            if val == target: return True
            elif val < target: lo = mid + 1
            else: hi = mid - 1
        return False
        
```
