# 345. Reverse Vowels of a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-vowels-of-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 13:27 local time

**Runtime:** 15 ms (beats 71.5815%)
**Memory:** 13.6 MB (beats 47.60910000000001%)


<!-- leetgit:submissionId=2149478260 codeHash=94f8e628ad239ee22ee85162c95ba93bfed660bcfa6719aafdb9097f3efa37c6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseVowels(self, s):
        s = list(s)
        v = set("aeiouAEIOU")
        l, r = 0, len(s) - 1

        while l < r:
            if s[l] not in v:
                l += 1
            elif s[r] not in v:
                r -= 1
            else:
                s[l], s[r] = s[r], s[l]
                l += 1
                r -= 1

        return "".join(s)
```
