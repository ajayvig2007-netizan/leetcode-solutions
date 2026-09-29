# 32. Longest Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/longest-valid-parentheses/<br>

**Difficulty:** Hard<br>
**Topics:** String, Dynamic Programming, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 14:14 local time

**Runtime:** 19 ms (beats 77.2432%)
**Memory:** 13.5 MB (beats 36.7959%)


<!-- leetgit:submissionId=2156875551 codeHash=7e38a8eb9e4c021f1cecadb7e90d0b5f2fbd0a327d74b2e46247d0dc89a76c08 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestValidParentheses(self, s):
        stack = [-1]
        ans = 0
        for i in range(len(s)):
            if s[i] == '(':
                stack.append(i)
            else:
                stack.pop()
                if not stack:
                    stack.append(i)
                else:
                    ans = max(ans, i - stack[-1])
        return ans
```
