# 1298. Reverse Substrings Between Each Pair of Parentheses
  
<br>**Problem:** https://leetcode.com/problems/reverse-substrings-between-each-pair-of-parentheses/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 10:11 local time

**Runtime:** 7 ms (beats 42.992399999999996%)
**Memory:** 19.2 MB (beats 91.2879%)


<!-- leetgit:submissionId=2154604238 codeHash=4cb229b5c369cc103ba609f5f141b27034970d0ea41f38881f7555bde6b377da notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution(object):
    def reverseParentheses(self, s):
       
      
        st = []
        res = []

        for ch in s:
            if ch == '(':
                st.append(len(res))
            elif ch == ')':
                start = st.pop()
                end = len(res) - 1
                self.reverse(res, start, end)
            else:
                res.append(ch)

        return ''.join(res)

    def reverse(self, sb, start, end):
        while start < end:
            sb[start], sb[end] = sb[end], sb[start]
            start += 1
            end -= 1
```
