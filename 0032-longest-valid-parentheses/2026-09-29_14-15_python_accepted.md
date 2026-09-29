# 32. Longest Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/longest-valid-parentheses/<br>

**Difficulty:** Hard<br>
**Topics:** String, Dynamic Programming, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 14:15 local time

**Runtime:** 15 ms (beats 97.4243%)
**Memory:** 13.6 MB (beats 36.7959%)


<!-- leetgit:submissionId=2156876525 codeHash=6fef9ea0c4cf40859fdeef7fbd229068cb0fea606d181048923ae0eb616343c1 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestValidParentheses(self, s):
        stack = [-1]
        ans = 0

        for i, c in enumerate(s):
            if c == '(':
                stack.append(i)
            else:
                stack.pop()

                if not stack:
                    stack.append(i)
                else:
                    ans = max(ans, i - stack[-1])

        return ans
```
