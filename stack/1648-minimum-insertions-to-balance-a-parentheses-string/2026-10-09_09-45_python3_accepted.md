# 1648. Minimum Insertions to Balance a Parentheses String
  
<br>**Problem:** https://leetcode.com/problems/minimum-insertions-to-balance-a-parentheses-string/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack, Greedy, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 09:45 local time

**Runtime:** 91 ms (beats 24.911700000000017%)
**Memory:** 19.8 MB (beats 88.77189999999999%)


<!-- leetgit:submissionId=2166904323 codeHash=8a97bab98dcb9869df198acd124846303e089b0341e38cd39aba8d664527e8ac notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def minInsertions(self, s: str) -> int:
        open = ans = 0
        i = 0

        while i < len(s):
            if s[i] == '(':
                open += 1
            else:
                # Step 1: make a "))"
                if i + 1 < len(s) and s[i + 1] == ')':
                    i += 1
                else:
                    ans += 1

                # Step 2: find its '('
                if open > 0:
                    open -= 1
                else:
                    ans += 1
            i += 1

        return ans + open * 2
```
