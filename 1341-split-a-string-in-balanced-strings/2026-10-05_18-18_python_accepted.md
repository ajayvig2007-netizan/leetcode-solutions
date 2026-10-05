# 1341. Split a String in Balanced Strings
  
<br>**Problem:** https://leetcode.com/problems/split-a-string-in-balanced-strings/<br>

**Difficulty:** Easy<br>
**Topics:** String, Greedy, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:18 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.5 MB (beats 21.6802%)


<!-- leetgit:submissionId=2163118869 codeHash=bf5b75511780b41c1fe5c039a9bca996cdefb93fe13b93cdb4c2bfb86ed6c9ab notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def balancedStringSplit(self, s):
        l=0
        count=0
        cr=0
        cl=0
        r=0
        while r<len(s):
            if s[r]=='R':
                cr+=1
            else:
                cl+=1
            if cl==cr and cl!=0:
                count+=1
                l=r+1
            r+=1
        return count
            



        
```
