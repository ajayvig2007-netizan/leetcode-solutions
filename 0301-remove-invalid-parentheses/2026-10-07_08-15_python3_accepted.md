# 301. Remove Invalid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/remove-invalid-parentheses/<br>

**Difficulty:** Hard<br>
**Topics:** String, Backtracking, Breadth-First Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 08:15 local time

**Runtime:** 1 ms (beats 98.7997%)
**Memory:** 19.4 MB (beats 94.37359999999998%)


<!-- leetgit:submissionId=2164819967 codeHash=7ee9867f177062b9ccafffb609b100eb390ce6fbaa663b5733171d3c5a6477d8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def removeInvalidParentheses(self, s: str) -> List[str]:
        ans = []
        self.remove(s, ans, 0, 0, ['(', ')'])
        return ans

    def remove(self, s, ans, i, j, p):
        count = 0

        for k in range(i, len(s)):
            if s[k] == p[0]:
                count += 1
            if s[k] == p[1]:
                count -= 1

            if count < 0:
                for x in range(j, k + 1):
                    if s[x] == p[1] and (x == j or s[x - 1] != p[1]):
                        self.remove(s[:x] + s[x + 1:], ans, k, x, p)
                return

        rev = s[::-1]

        if p[0] == '(':
            self.remove(rev, ans, 0, 0, [')', '('])
        else:
            ans.append(rev)
```
