# 20. Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/valid-parentheses/<br>

**Difficulty:** Easy<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 17:08 local time

**Runtime:** 2 ms (beats 81.4504%)
**Memory:** 12.5 MB (beats 40.0121%)


<!-- leetgit:submissionId=2140556758 codeHash=c177be6f77a146d058045146794fc44fc2945b58ab4e0854ff1e85500bca0a7a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isValid(self, s):
        stack = []
        pair = {')':'(', ']':'[', '}':'{'}

        for i in s:
            if i in "([{":
                stack.append(i)
            else:
                if not stack or stack.pop() != pair[i]:
                    return False

        return len(stack) == 0
```
