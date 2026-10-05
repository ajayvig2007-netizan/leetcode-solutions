# 22. Generate Parentheses
  
<br>**Problem:** https://leetcode.com/problems/generate-parentheses/<br>

**Difficulty:** Medium<br>
**Topics:** String, Dynamic Programming, Backtracking, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-02 10:37 local time

**Runtime:** 3 ms (beats 30.518599999999996%)
**Memory:** 19.4 MB (beats 74.7977%)


<!-- leetgit:submissionId=2159793579 codeHash=0dbe5d15b7a728c18ddf2853c5f79c9971fc867fbb9be11260ee1a9979ac5bb1 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def generateParenthesis(self, n: int) -> List[str]:
        res = []

        def dfs(openP, closeP, s):
            if openP == closeP and openP + closeP == n * 2:
                res.append(s)
                return
            
            if openP < n:
                dfs(openP + 1, closeP, s + "(")
            
            if closeP < openP:
                dfs(openP, closeP + 1, s + ")")

        dfs(0, 0, "")

        return res
```
