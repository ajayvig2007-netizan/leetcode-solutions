# 74. Search a 2D Matrix
  
<br>**Problem:** https://leetcode.com/problems/search-a-2d-matrix/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 19:13 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.7 MB (beats 2.8486000000000082%)


<!-- leetgit:submissionId=2161115321 codeHash=b592e5fa84d7688c7682e5af101f2e9db140b933ce59b61b3d4189476c9f6f34 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchMatrix(self, matrix, target):
        l=0
        r=len(matrix[0])*len(matrix)-1
        while l<=r:
            mid=(l+r)//2
            row=mid//len(matrix[0])
            col=mid%len(matrix[0])
            if matrix[row][col]==target:
                return True
            elif matrix[row][col]>target:
                r=mid-1
            else:
                l=mid+1
        return False
        
        
```
