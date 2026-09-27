# 20. Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/valid-parentheses/<br>

**Difficulty:** Easy<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 16:55 local time

**Runtime:** 5 ms (beats 20.06260000000001%)
**Memory:** 12.6 MB (beats 11.384099999999997%)


<!-- leetgit:submissionId=2140547275 codeHash=1d1ff8919615499964594bd97872e4e778176a9c7cd34c49d3f713e90082b882 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isValid(self, s):
        stack=[]
        for i in s:
            if  i in"({[":
                stack.append(i)
            if i in ")]}":
                if not stack:
                    return False
                top=stack.pop()
                if i == ")" and top != "(":
                    return False
                if i == "}" and top != "{":
                    return False
                if i == "]" and top != "[":
                    return False

        return len(stack) == 0
        

        
        
```
