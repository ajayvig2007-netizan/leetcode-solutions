# 36. Valid Sudoku
  
<br>**Problem:** https://leetcode.com/problems/valid-sudoku/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Matrix<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 11:15 local time

**Runtime:** 4 ms (beats 77.4125%)
**Memory:** 12.3 MB (beats 93.06269999999999%)


<!-- leetgit:submissionId=2165992516 codeHash=e20df41f8a08d64a659174c160134f96ed6dccabce135d862592b0c4955461f7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isValidSudoku(self, board):
        for i in range(9):
            row = set()
            col = set()

            for j in range(9):
                if board[i][j] != '.':
                    if board[i][j] in row:
                        return False
                    row.add(board[i][j])

                if board[j][i] != '.':
                    if board[j][i] in col:
                        return False
                    col.add(board[j][i])

        for r in range(0, 9, 3):
            for c in range(0, 9, 3):
                s = set()

                for i in range(3):
                    for j in range(3):
                        x = board[r+i][c+j]

                        if x != '.':
                            if x in s:
                                return False
                            s.add(x)

        return True
```
