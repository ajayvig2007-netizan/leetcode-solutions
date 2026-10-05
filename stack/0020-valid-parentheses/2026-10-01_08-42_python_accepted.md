# 20. Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/valid-parentheses/<br>

**Difficulty:** Easy<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 08:42 local time

**Runtime:** 3 ms (beats 74.05649999999999%)
**Memory:** 12.5 MB (beats 73.3496%)


<!-- leetgit:submissionId=2158726442 codeHash=59442d8f943e5189d7fc1a26578f8679cf1651b1c0094a95530a4c05873bb3e2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
