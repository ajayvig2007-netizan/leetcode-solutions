# 345. Reverse Vowels of a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-vowels-of-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 13:12 local time

**Runtime:** 16 ms (beats 58.095800000000004%)
**Memory:** 13.7 MB (beats 47.60910000000001%)


<!-- leetgit:submissionId=2149468824 codeHash=6bf6a3e37e870623b4231a026d459b3dc4678cc012e8d7523b3e14ee2460c24b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseVowels(self, s):
        s = list(s)

        l = len(s) - 1
        r = 0

        while r < l:

            if s[r] not in "aeiouAEIOU":
                r += 1

            elif s[l] not in "aeiouAEIOU":
                l -= 1

            else:
                s[l], s[r] = s[r], s[l]
                l -= 1
                r += 1

        return "".join(s)
```
