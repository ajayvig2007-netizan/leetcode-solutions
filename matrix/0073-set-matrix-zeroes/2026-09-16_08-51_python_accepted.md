# 73. Set Matrix Zeroes
  
<br>**Problem:** https://leetcode.com/problems/set-matrix-zeroes/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 08:51 local time

**Runtime:** 520 ms (beats 8.349299999999946%)
**Memory:** 13.5 MB (beats 95.10269999999998%)


<!-- leetgit:submissionId=2143198812 codeHash=31d44e7549fd0021d861edefa0cd816108b98ac69ad6e19c535e3d8c6ba26c46 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def setZeroes(self, matrix):
        rows=[]
        cols=[]
        for i in range(len(matrix)):
            for j in range(len(matrix[0])):
                if matrix[i][j]==0:
                    rows.append(i)
                    cols.append(j)
        for i in rows:
            for j in range(len(matrix[0])):
                matrix[i][j] = 0

        for j in cols:
            for i in range(len(matrix)):
                matrix[i][j] = 0
        
        
```
