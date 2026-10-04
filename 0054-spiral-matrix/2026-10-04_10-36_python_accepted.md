# 54. Spiral Matrix
  
<br>**Problem:** https://leetcode.com/problems/spiral-matrix/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-04 10:36 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.2 MB (beats 91.4538%)


<!-- leetgit:submissionId=2161743344 codeHash=0aea1aaea0a34f965ed30c1dfea78e877c2361cb7af368dfae74c9f8faf88be2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def spiralOrder(self, matrix):
        ans=[]
        top=0
        bottom=len(matrix)-1
        left=0
        right=len(matrix[0])-1
        while top<=bottom and left<=right:
            i=left
            while i<=right:
                ans.append(matrix[top][i])
                i+=1
            top+=1
            i=top
            while i<=bottom:
                ans.append(matrix[i][right])
                i+=1
            right-=1
            if top<=bottom:
                i=right
                while i>=left:
                    ans.append(matrix[bottom][i])
                    i-=1
                bottom-=1
            if left<=right:
                i=bottom
                while i>=top:
                    ans.append(matrix[i][left])
                    i-=1
                left+=1
        return ans
```
