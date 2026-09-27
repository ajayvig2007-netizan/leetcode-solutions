# 647. Palindromic Substrings
  
<br>**Problem:** https://leetcode.com/problems/palindromic-substrings/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 10:30 local time

**Runtime:** 158 ms (beats 82.74480000000008%)
**Memory:** 12.4 MB (beats 71.4872%)


<!-- leetgit:submissionId=2152627478 codeHash=d9a1cfe4eb1e18eebcab92c78cd9d4d0d7ab85cce70160b0cdec305f55e2a111 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):

    def countSubstrings(self, s):
        c = 0
        for i in range(len(s)):
            c += self.exp(s,i,i)
            c += self.exp(s,i,i+1)
        return c
    def exp(self,s,l,r):
        c=0
        while l>=0 and r<len(s) and s[l]==s[r]:
            c+=1
            l-=1
            r+=1
        return c
```
