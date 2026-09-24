# 1508. Longest Happy Prefix
  
<br>**Problem:** https://leetcode.com/problems/longest-happy-prefix/<br>

**Difficulty:** Hard<br>
**Topics:** String, Rolling Hash, String Matching, Hash Function, Z Algorithm, Knuth–Morris–Pratt Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-24 14:14 local time

**Runtime:** 145 ms (beats 47.48240000000005%)
**Memory:** 16.9 MB (beats 36.69069999999999%)


<!-- leetgit:submissionId=2151786061 codeHash=2a4e669ed58bbcf09baae9b9bef79ad6474e47e4c1f22b34cb04279ddbed14e1 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPrefix(self, s):
        lps=[0]*len(s)
        l=0
        i=1
        while i<len(s):
            if s[i]==s[l]:
                l+=1
                lps[i]=l
                i+=1    
            else:
                if l!=0:
                    l=lps[l-1]
                else:
                    lps[i]=0
                    i+=1
        return s[:lps[-1]]

        
        
```
