# 680. Valid Palindrome II
  
<br>**Problem:** https://leetcode.com/problems/valid-palindrome-ii/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String, Greedy<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 10:53 local time

**Runtime:** 63 ms (beats 30.006100000000004%)
**Memory:** 19.7 MB (beats 16.684400000000007%)


<!-- leetgit:submissionId=2149346982 codeHash=0f3a793165af2df94e90a5e9b4d08dd1ec0d4a180e79fc8648d6378c4d6c8f8a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def validPalindrome(self, s: str) -> bool:
        def isPalindrome(l, r):
            while l < r:
                if s[l] != s[r]:
                    return False
                l += 1
                r -= 1
            return True
        
        left, right = 0, len(s) - 1
        while left < right:
            if s[left] != s[right]:
                return isPalindrome(left + 1, right) or isPalindrome(left, right - 1)
            left += 1
            right -= 1
        return True
```
