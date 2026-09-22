# 345. Reverse Vowels of a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-vowels-of-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 13:28 local time

**Runtime:** 9 ms (beats 96.7702%)
**Memory:** 13.5 MB (beats 75.62920000000001%)


<!-- leetgit:submissionId=2149478486 codeHash=6896c31e063c541dccae5d6740ab802fa5378ed383dfd50930f61c2dda327730 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseVowels(self, s):
        s = list(s)
        v = set("aeiouAEIOU")
        l, r = 0, len(s) - 1

        while l < r:
            while l < r and s[l] not in v:
                l += 1
            while l < r and s[r] not in v:
                r -= 1

            s[l], s[r] = s[r], s[l]
            l += 1
            r -= 1

        return "".join(s)
```
