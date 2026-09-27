# 242. Valid Anagram
  
<br>**Problem:** https://leetcode.com/problems/valid-anagram/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 13:11 local time

**Runtime:** 15 ms (beats 85.14260000000002%)
**Memory:** 12.4 MB (beats 86.69969999999999%)


<!-- leetgit:submissionId=2154741770 codeHash=17b00154c24e18b8bc85a70f33028f2fb2d321f51bad23999dea4ab1a7190865 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isAnagram(self, s, t):
        hashmap={}
        hashmap1={}
        for x in s:
            hashmap[x]=hashmap.get(x,0)+1
        for xx in t:
            hashmap1[xx]=hashmap1.get(xx,0)+1
        return hashmap1==hashmap

        
```
