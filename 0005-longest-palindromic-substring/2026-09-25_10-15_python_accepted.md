# 5. Longest Palindromic Substring
  
<br>**Problem:** https://leetcode.com/problems/longest-palindromic-substring/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String, Dynamic Programming, Manacher<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 10:15 local time

**Runtime:** 334 ms (beats 91.59600000000026%)
**Memory:** 12.5 MB (beats 56.02149999999999%)


<!-- leetgit:submissionId=2152615511 codeHash=2b45b050cddfd058a3480a786c651e8513d915aa4c69bf6ffd6589a91e48e892 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPalindrome(self, s):
        st=0
        end=0
        for i in range(len(s)):
            len1=self.exp(s,i,i)
            len2=self.exp(s,i,i+1)
            lenmax=max(len1,len2)
            if(lenmax>end-st+1):
                st=i-(lenmax-1)//2
                end=i+lenmax//2
        return s[st:end+1]
    def exp(self,s,le,ri):
        while(le>=0 and ri<len(s) and s[le]==s[ri]):
            le-=1
            ri+=1
        return ri-le-1
        
```
