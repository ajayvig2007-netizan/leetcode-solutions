# 151. Reverse Words in a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-words-in-a-string/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 09:04 local time

**Runtime:** 3 ms (beats 32.620400000000004%)
**Memory:** 12.5 MB (beats 38.4814%)


<!-- leetgit:submissionId=2149253491 codeHash=59f3a0d1f9c6df8fbdb3a1286d335bd7ac2ad71346a7de024b122de34c5cdc29 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseWords(self, s):
        s = s.split()
        b = ''

        for c in range(len(s) - 1, -1, -1):
            b = b + ' ' + s[c]

        return b.strip()
```
