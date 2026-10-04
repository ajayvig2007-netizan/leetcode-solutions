# 678. Valid Parenthesis String
  
<br>**Problem:** https://leetcode.com/problems/valid-parenthesis-string/<br>

**Difficulty:** Medium<br>
**Topics:** String, Dynamic Programming, Stack, Greedy, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-04 15:06 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.2 MB (beats 89.99009999999998%)


<!-- leetgit:submissionId=2161950853 codeHash=3a01117d7b893bb73825b529716264c71eee897c2199d07ad441dab6600d25ea notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def checkValidString(self, s: str) -> bool:
        l = h = 0

        for c in s:
            l += ((c == '(') << 1) - 1
            h += ((c != ')') << 1) - 1

            if h < 0: return False

            l = max(l, 0)

        return l == 0
```
