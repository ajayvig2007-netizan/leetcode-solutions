# 953. Reverse Only Letters
  
<br>**Problem:** https://leetcode.com/problems/reverse-only-letters/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 13:31 local time

**Runtime:** 4 ms (beats 5.9451%)
**Memory:** 12.4 MB (beats 53.6586%)


<!-- leetgit:submissionId=2149480891 codeHash=88ce71e3ccd90481eb94cb55d98ae0f4f64bd0b63154e6943a622f3b781b9a1d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseOnlyLetters(self, s):
        s = list(s)
        l, r = 0, len(s) - 1

        while l < r:
            if not s[l].isalpha():
                l += 1
            elif not s[r].isalpha():
                r -= 1
            else:
                s[l], s[r] = s[r], s[l]
                l += 1
                r -= 1

        return "".join(s)
```
