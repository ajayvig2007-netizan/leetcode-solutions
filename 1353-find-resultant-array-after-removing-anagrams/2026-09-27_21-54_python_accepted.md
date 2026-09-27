# 1353. Find Resultant Array After Removing Anagrams
  
<br>**Problem:** https://leetcode.com/problems/find-resultant-array-after-removing-anagrams/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 21:54 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 71.7791%)


<!-- leetgit:submissionId=2155146864 codeHash=23972cc0db1946120aed6d7b6e822449605601187da0c6e281376fe8c94bbbe0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def removeAnagrams(self, words):
        res=[]
        seen=[]
        for w in words:
            so=sorted(w)
            if so !=seen:
                seen=so
                res.append(w)
        return res        
```
