# 73. Set Matrix Zeroes
  
<br>**Problem:** https://leetcode.com/problems/set-matrix-zeroes/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 17:54 local time

**Runtime:** 21 ms (beats 15.981200000000001%)
**Memory:** 13.7 MB (beats 51.44629999999997%)


<!-- leetgit:submissionId=2143631690 codeHash=127a9ad9d0e064d5fe0b2c9393508170001f19f3de01fa9e65a6dcae46abd589 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def setZeroes(self, matrix):
        rows=False
        cols=False
        for i in range(len(matrix)):
            for j in range(len(matrix[0])):
                if matrix[i][j]==0:
                    if i==0:
                        rows=True
                    if j==0:
                        cols=True
                    matrix[0][j]=0
                    matrix[i][0]=0
        for i in range(1,len(matrix)):
            for j in range(1,len(matrix[0])):
                if matrix[i][0]==0 or matrix[0][j]==0:
                    matrix[i][j]=0
        if(rows):
            for i in range(len(matrix[0])):
                matrix[0][i]=0
        if(cols):
            for i in range(len(matrix)):
                matrix[i][0]=0

                
                   

        
```
