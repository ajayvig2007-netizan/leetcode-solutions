# 289. Game of Life
  
<br>**Problem:** https://leetcode.com/problems/game-of-life/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 11:10 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.4 MB (beats 50.229099999999995%)


<!-- leetgit:submissionId=2143313558 codeHash=21eb289ab3b81a21d85af5f04a5bcc5591a1f6588b4165c53a3d64141d62a6e2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def gameOfLife(self, board: list[list[int]]) -> None:
        old=[r[:] for r in board]; [board.__setitem__(i,[int((c:=sum(old[x][y] for x in range(i-1,i+2) for y in range(j-1,j+2) if 0<=x<len(board) and 0<=y<len(board[0]) and (x,y)!=(i,j)))==3 or old[i][j] and c==2) for j in range(len(board[0]))]) for i in range(len(board))]

        
```
