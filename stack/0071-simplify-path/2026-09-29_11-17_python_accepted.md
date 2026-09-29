# 71. Simplify Path
  
<br>**Problem:** https://leetcode.com/problems/simplify-path/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 11:17 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.5 MB (beats 22.764699999999998%)


<!-- leetgit:submissionId=2156720731 codeHash=b371f1d204e29aeaaec6ac32034d0ef8c77be2ee6176ed00380fb2b1440d9e86 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def simplifyPath(self, path):
        stack = []
        for i in path.split('/'):
            if i == '' or i == '.':
                continue
            elif i == '..':
                if stack:
                    stack.pop()
            else:
                stack.append(i)
        return '/' + '/'.join(stack)
```
