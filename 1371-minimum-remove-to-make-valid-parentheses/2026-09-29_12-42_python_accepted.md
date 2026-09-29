# 1371. Minimum Remove to Make Valid Parentheses
  
<br>**Problem:** https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 12:42 local time

**Runtime:** 95 ms (beats 31.15540000000005%)
**Memory:** 16.4 MB (beats 45.22610000000004%)


<!-- leetgit:submissionId=2156808728 codeHash=cdef31c3d8729c5cac947d52708a9ec4a6d120f5bb8165bfd29f9be9c960e35b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minRemoveToMakeValid(self, s):
        stack = []
        remove = set()

        for i in range(len(s)):
            if s[i] == '(':
                stack.append(i)

            elif s[i] == ')':
                if stack:
                    stack.pop()
                else:
                    remove.add(i)

        remove.update(stack)

        ans = []

        for i in range(len(s)):
            if i not in remove:
                ans.append(s[i])

        return ''.join(ans)
```
