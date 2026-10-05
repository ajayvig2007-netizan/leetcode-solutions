# 32. Longest Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/longest-valid-parentheses/<br>

**Difficulty:** Hard<br>
**Topics:** String, Dynamic Programming, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 14:18 local time

**Runtime:** 20 ms (beats 54.2599%)
**Memory:** 13.5 MB (beats 67.1667%)


<!-- leetgit:submissionId=2156879286 codeHash=9a3c452db943d23746a70a5f5b110d1126f1656ad051e95847288c6ce3853036 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestValidParentheses(self, s):
        dp = [0] * len(s)
        ans = 0

        for i in range(1, len(s)):
            if s[i] == ')':
                if s[i - 1] == '(':
                    dp[i] = 2
                    if i >= 2:
                        dp[i] += dp[i - 2]

                elif dp[i - 1] > 0:
                    j = i - dp[i - 1] - 1

                    if j >= 0 and s[j] == '(':
                        dp[i] = dp[i - 1] + 2
                        if j >= 1:
                            dp[i] += dp[j - 1]

                ans = max(ans, dp[i])

        return ans
```
