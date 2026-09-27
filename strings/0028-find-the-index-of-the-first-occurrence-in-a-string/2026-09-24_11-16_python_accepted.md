# 28. Find the Index of the First Occurrence in a String
  
<br>**Problem:** https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String, String Matching, Z Algorithm, Knuth–Morris–Pratt Algorithm, Boyer–Moore String-Search Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-24 11:16 local time

**Runtime:** 3 ms (beats 19.842800000000008%)
**Memory:** 12.9 MB (beats 6.825200000000011%)


<!-- leetgit:submissionId=2151633211 codeHash=e2d7a411764016606d5fc1e443ff384c04740525883ffeb473e1fe9fbed45127 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def strStr(self, haystack, needle):
        lps=[0]*len(needle)
        i=1
        l=0
        while i<len(needle):
            if needle[i]==needle[l]:
                l+=1
                lps[i]=l
                i+=1
            else:
                if l!=0:
                    l=lps[l-1]
                else:
                    lps[i]=0
                    i+=1
        i,j=0,0
        while i<len(haystack):
            if(haystack[i]==needle[j]):
                i+=1
                j+=1
            
            else:
                if(j!=0):
                     j=lps[j-1]
                else:
                    i+=1
            if(j==len(needle)):
                return i-j
        return -1
        
```
