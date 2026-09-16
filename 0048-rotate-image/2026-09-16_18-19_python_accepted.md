# 48. Rotate Image
  
<br>**Problem:** https://leetcode.com/problems/rotate-image/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 18:19 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 24.734199999999987%)


<!-- leetgit:submissionId=2143650181 codeHash=1c73ed2e8558492b5a35e1b08bd63b01054d8b2a51420b37b1663a435fe11f4b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def rotate(self, matrix):
        r=len(matrix)-1
        l=0
        while r>l:
            for i in range(r-l):
                top,bottom=l,r
                temp=matrix[top][l+i]
                matrix[top][l+i]=matrix[bottom-i][l]
                matrix[bottom-i][l]=matrix[bottom][r-i]
                matrix[bottom][r-i]=matrix[top+i][r]
                matrix[top+i][r]=temp
            r-=1
            l+=1
            
        
```
