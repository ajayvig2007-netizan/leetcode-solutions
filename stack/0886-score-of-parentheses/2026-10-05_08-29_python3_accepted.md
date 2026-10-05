# 886. Score of Parentheses
  
<br>**Problem:** https://leetcode.com/problems/score-of-parentheses/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 08:29 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.4 MB (beats 17.127600000000008%)


<!-- leetgit:submissionId=2162646198 codeHash=4afe6ad04e9d5621eacfd9cff3642d0f176e7dee9609d0b8f9ff0687bcb34eeb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def scoreOfParentheses(self, s: str) -> int:
        def F(i: int, j: int) -> int:
            ans = bal = 0
            start = i
            for k in range(start, j):
                bal += 1 if s[k] == '(' else -1
                if bal == 0:
                    if k - start == 1:
                        ans += 1
                    else:
                        ans += 2 * F(start + 1, k)
                    start = k + 1
            return ans
            
        return F(0, len(s))
```
