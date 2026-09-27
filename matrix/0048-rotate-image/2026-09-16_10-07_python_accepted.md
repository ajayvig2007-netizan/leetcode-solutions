# 48. Rotate Image
  
<br>**Problem:** https://leetcode.com/problems/rotate-image/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 10:07 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 24.734199999999987%)


<!-- leetgit:submissionId=2143256483 codeHash=076458ce524636a317c093b262ba8c8f16c15f798c44f8cad195c0df5297ea78 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
