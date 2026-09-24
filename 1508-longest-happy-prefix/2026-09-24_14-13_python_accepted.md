# 1508. Longest Happy Prefix
  
<br>**Problem:** https://leetcode.com/problems/longest-happy-prefix/<br>

**Difficulty:** Hard<br>
**Topics:** String, Rolling Hash, String Matching, Hash Function, Z Algorithm, Knuth–Morris–Pratt Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-24 14:13 local time

**Runtime:** 168 ms (beats 20.864000000000047%)
**Memory:** 17.5 MB (beats 30.935399999999994%)


<!-- leetgit:submissionId=2151785315 codeHash=974dbaee799b6bc67c95beb39b9c07992450ca8453bea57fd515f1bbdce0342d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPrefix(self, s):
        list1=list(s)
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
        return "".join(list1[:lps[-1]])

        
        
```
