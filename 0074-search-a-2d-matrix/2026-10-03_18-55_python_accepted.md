# 74. Search a 2D Matrix
  
<br>**Problem:** https://leetcode.com/problems/search-a-2d-matrix/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 18:55 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.7 MB (beats 33.15950000000001%)


<!-- leetgit:submissionId=2161099613 codeHash=ba097de23d830eee067cdab8e226aa6f56a04c91f4a77b491a8e1de126371f0b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchMatrix(self, matrix, target):
        i=len(matrix)-1
        j=0
        while i>=0 and j<len(matrix[0]):
            if matrix[i][j]==target:
                return True
            elif matrix[i][j]>target:
                i-=1
            else:# matrix[i][j]<target:
                j+=1
        return False
        
        
```
