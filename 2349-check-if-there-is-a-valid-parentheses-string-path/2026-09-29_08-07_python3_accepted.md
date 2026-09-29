# 2349.  Check if There Is a Valid Parentheses String Path
  
<br>**Problem:** https://leetcode.com/problems/check-if-there-is-a-valid-parentheses-string-path/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Dynamic Programming, Matrix, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 08:07 local time

**Runtime:** 15 ms (beats 84%)
**Memory:** 20.7 MB (beats 100%)


<!-- leetgit:submissionId=2156565434 codeHash=b3bd10a6784314db3e7390a095e848fc32664742d2ce1af40ec762b23fffaef3 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def hasValidPath(self, grid: list[list[str]]) -> bool:
        m, n=len(grid), len(grid[0])
        lim=(n+m)>>1
        if ((m+n)&1)==0 or grid[0][0]==')' or grid[m-1][n-1]=='(':
            return False
        maxMask=(1<<(lim+1))-1
        dp=[0]*n

        dp[0]=1<<1
        p=1
        for j in range(1, n):
            p+=(grid[0][j]=='(')-(grid[0][j]==')')
            if p<0 or p>lim: break
            dp[j]=1<<p
        p=1
        for i in range(1, m):
            p+=(grid[i][0]=='(')-(grid[i][0]==')')
            if dp[0]==0 or p<0 or p>lim: dp[0]=0
            else: dp[0]=1<<p
            for j in range(1, n):
                dp[j]=dp[j-1]|dp[j]
                dp[j]=(dp[j]<<1)& maxMask if grid[i][j]=='(' else dp[j]>>1
        return dp[-1]&1==1
```
