# 125. Valid Palindrome
  
<br>**Problem:** https://leetcode.com/problems/valid-palindrome/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 23:07 local time

**Runtime:** 18 ms (beats 49.01630000000001%)
**Memory:** 14.1 MB (beats 23.8742%)


<!-- leetgit:submissionId=2161331309 codeHash=b267f3bdde821a2bd505332046dc4863d572be2b3f164a5fd45c53e19cc7f189 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isPalindrome(self, s):
        s=''.join(x.lower() for  x in s if x.isalnum())
        return s[::]==s[::-1]
        
```
