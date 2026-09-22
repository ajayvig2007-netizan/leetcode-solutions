# 345. Reverse Vowels of a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-vowels-of-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 13:26 local time

**Runtime:** 16 ms (beats 58.095800000000004%)
**Memory:** 13.6 MB (beats 47.60910000000001%)


<!-- leetgit:submissionId=2149477264 codeHash=b5cdf7d4d6aa7736eb66672bfc121faa7e72c5cc9abef5515ca9559ba1d509c0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseVowels(self, s):
        s = list(s)
        vowels = "aeiouAEIOU"
        l = len(s) - 1
        r = 0

        while r < l:
            if s[r] not in vowels:
                r += 1
            elif s[l] not in vowels:
                l -= 1
            else:
                s[r], s[l] = s[l], s[r]
                r += 1
                l -= 1

        return "".join(s)
```
