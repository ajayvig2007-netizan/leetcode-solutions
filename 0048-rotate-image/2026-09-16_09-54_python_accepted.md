# 48. Rotate Image
  
<br>**Problem:** https://leetcode.com/problems/rotate-image/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 09:54 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 60.69919999999999%)


<!-- leetgit:submissionId=2143245378 codeHash=2a9f068142a352831b4b1a86da0e7b3893968e7f5ef24f91b3bb77b57d604a12 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def rotate(self, matrix):
        n = len(matrix)

        
        for i in range(n):
            for j in range(i + 1, n):
                matrix[i][j], matrix[j][i] = matrix[j][i], matrix[i][j]

       
        for i in range(n):
            matrix[i].reverse()
            

       
```
