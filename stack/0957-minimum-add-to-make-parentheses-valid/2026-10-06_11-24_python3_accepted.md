# 957. Minimum Add to Make Parentheses Valid
  
<br>**Problem:** https://leetcode.com/problems/minimum-add-to-make-parentheses-valid/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack, Greedy, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 11:24 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.1 MB (beats 86.70710000000001%)


<!-- leetgit:submissionId=2163880341 codeHash=8a1b4886493e3c9d7c054123352239ac503fb494e0e5c9f85a2b312ca82119b8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def minAddToMakeValid(self, s: str) -> int:
        open = 0
        ans = 0

        for c in s:
            if c == '(':
                open += 1
            else:
                if open > 0:
                    open -= 1
                else:
                    ans += 1

        return ans + open
```
