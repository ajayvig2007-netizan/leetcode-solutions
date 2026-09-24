# 459. Repeated Substring Pattern
  
<br>**Problem:** https://leetcode.com/problems/repeated-substring-pattern/<br>

**Difficulty:** Easy<br>
**Topics:** String, String Matching, Z Algorithm, Knuth–Morris–Pratt Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-24 12:33 local time

**Runtime:** 71 ms (beats 16.405200000000008%)
**Memory:** 12.9 MB (beats 9.308800000000005%)


<!-- leetgit:submissionId=2151712260 codeHash=34df89eef32dfd9ba6e50c130ed78990aa8b3edeed3bb8fad33f36cdaeeb9e3e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def repeatedSubstringPattern(self, s):
        lps=[0]*len(s)
        i=1
        l=0
        while i<len(s):
            if s[i]==s[l]:
                l+=1
                lps[i]=l
                i+=1
            else:
                if l!=0:
                    l=lps[l-1]
                else:
                    i+=1
        length=len(s)-lps[-1]
        if lps[-1]!=0 and len(s)%length==0:
            return True
        return False
```
