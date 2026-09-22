# 125. Valid Palindrome
  
<br>**Problem:** https://leetcode.com/problems/valid-palindrome/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 08:21 local time

**Runtime:** 11 ms (beats 92.40060000000001%)
**Memory:** 14.1 MB (beats 17.512500000000014%)


<!-- leetgit:submissionId=2149230396 codeHash=6cf035d0f5d3ad1a7b0077a6b2d3c1eac33b538c21d6e0a1b8e04f24b88eee39 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isPalindrome(self, s):
        s = "".join(x.lower() for x in s if x.isalnum())
        return s == s[::-1]
```
