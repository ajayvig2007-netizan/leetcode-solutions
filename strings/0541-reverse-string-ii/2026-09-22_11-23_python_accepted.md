# 541. Reverse String II
  
<br>**Problem:** https://leetcode.com/problems/reverse-string-ii/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 11:23 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 43.75%)


<!-- leetgit:submissionId=2149374217 codeHash=aed7939cb51f1dfe0a8c5d798121f700ad4d771404a0bc8d6af8710cfa4aa19c notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseStr(self, s, k):
        s = list(s)
        for i in range(0, len(s), 2*k):
            s[i:i+k] = s[i:i+k][::-1]
        return "".join(s)
```
