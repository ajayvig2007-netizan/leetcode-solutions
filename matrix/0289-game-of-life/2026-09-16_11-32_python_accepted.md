# 289. Game of Life
  
<br>**Problem:** https://leetcode.com/problems/game-of-life/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 11:32 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.9 MB (beats 1.6559999999999988%)


<!-- leetgit:submissionId=2143334757 codeHash=daf6bd3b68db78a2d63f359345f748828a585151c5b67597ecc67c5b6fd1c498 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def gameOfLife(self, board):
        m, n = len(board), len(board[0])
        old = [r[:] for r in board]

        def solve(i, j):
            if i == m:
                return
            if j == n:
                solve(i + 1, 0)
                return

            c = sum(old[x][y] for x in range(i-1, i+2)
                    for y in range(j-1, j+2)
                    if 0 <= x < m and 0 <= y < n and (x, y) != (i, j))

            board[i][j] = int(c == 3 or (old[i][j] and c == 2))
            solve(i, j + 1)

        solve(0, 0)
```
