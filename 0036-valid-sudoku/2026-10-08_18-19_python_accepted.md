# 36. Valid Sudoku
  
<br>**Problem:** https://leetcode.com/problems/valid-sudoku/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 18:19 local time

**Runtime:** 6 ms (beats 59.9211%)
**Memory:** 12.4 MB (beats 25.23429999999999%)


<!-- leetgit:submissionId=2166319559 codeHash=cdad7550d259e7fbfaa307ea4584bd024ec1bbf6398d6eab7e17c4ac2f4efa38 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isValidSudoku(self, board):
        
        for  i in range(9):
            row=set()
            col=set()
            for j in range(9):
                if board[i][j]!='.':
                    if board[i][j] in row:
                        return False
                    row.add(board[i][j])
                if board[j][i]!='.':
                    if board[j][i] in col:
                        return False
                    col.add(board[j][i])
        for i in range(0,9,3):
            for j in range(0,9,3):
                list1=set()
                for r in range(i,i+3):
                    for l in range(j,j+3):
                        if board[r][l]!='.':
                            if board[r][l]  in list1:
                                return False
                            list1.add(board[r][l])
        return True



            


        
```
