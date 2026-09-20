# 48. Rotate Image
  
<br>**Problem:** https://leetcode.com/problems/rotate-image/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Matrix<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 12:55 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.2 MB (beats 69.7183%)


<!-- leetgit:submissionId=2147444696 codeHash=39a1976f5ca730ee7e14216d92c95c9b419131b7932d5352e40b3ae4e3172e91 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def rotate(self, matrix: list[list[int]]) -> None:
       matrix[:]=[list(x) for x in zip(*matrix)]
       for row in matrix:
            row.reverse()
       #matrix.reverse()
        
```
