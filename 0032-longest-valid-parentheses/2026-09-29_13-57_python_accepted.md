# 32. Longest Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/longest-valid-parentheses/<br>

**Difficulty:** Hard<br>
**Topics:** String, Dynamic Programming, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 13:57 local time

**Runtime:** 18 ms (beats 82.79090000000001%)
**Memory:** 13.4 MB (beats 87.9705%)


<!-- leetgit:submissionId=2156862422 codeHash=2c00fa2739b9310e196116b6854246babb636c5414408bf46198ab39e74d4467 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
