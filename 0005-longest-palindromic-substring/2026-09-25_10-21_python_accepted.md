# 5. Longest Palindromic Substring
  
<br>**Problem:** https://leetcode.com/problems/longest-palindromic-substring/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String, Dynamic Programming, Manacher<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 10:21 local time

**Runtime:** 491 ms (beats 23.981000000000353%)
**Memory:** 12.5 MB (beats 56.02149999999999%)


<!-- leetgit:submissionId=2152619832 codeHash=6fff8163861fb86744c3845f6e6eb55f8ca360c76f65f64c35129f48c3bc2bc6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPalindrome(self, s):
        res = ""

        for i in range(len(s)):
            for l, r in ((i, i), (i, i + 1)):
                while l >= 0 and r < len(s) and s[l] == s[r]:

                    if (r - l + 1) > len(res):
                        res = s[l:r+1]

                    l, r = l - 1, r + 1

        return res
```
