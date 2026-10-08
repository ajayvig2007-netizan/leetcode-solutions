# 1078. Remove Outermost Parentheses
  
<br>**Problem:** https://leetcode.com/problems/remove-outermost-parentheses/<br>

**Difficulty:** Easy<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 08:10 local time

**Runtime:** 3 ms (beats 64.633%)
**Memory:** 19.2 MB (beats 70.87429999999999%)


<!-- leetgit:submissionId=2165858796 codeHash=145110cfd4c38ee76cb780bd64c45bfe94d77ab8c0f8bf43dc3feb4e4538a48a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def removeOuterParentheses(self, s: str) -> str:
        res, stack = [], []
        for c in s:
            if c == ")":
                stack.pop()
            if stack:
                res.append(c)
            if c == "(":
                stack.append(c)
        return "".join(res)
```
