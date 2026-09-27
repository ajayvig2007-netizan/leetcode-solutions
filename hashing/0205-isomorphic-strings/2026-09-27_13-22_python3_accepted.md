# 205. Isomorphic Strings
  
<br>**Problem:** https://leetcode.com/problems/isomorphic-strings/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 13:22 local time

**Runtime:** 7 ms (beats 40.3929%)
**Memory:** 19.1 MB (beats 97.88520000000003%)


<!-- leetgit:submissionId=2154749707 codeHash=4185f4660838df6df2c42cb9de0e86b5cde81933f04f11d5557bfbbec3b4a267 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def isIsomorphic(self, s: str, t: str) -> bool:
        hashmap1={}
        hashmap2={}
        for x in range(len(s)):
            if s[x]  in hashmap1 and hashmap1[s[x]]!=t[x]:
                return False
            if t[x] in hashmap2 and hashmap2[t[x]]!=s[x]:
                return False
            hashmap1[s[x]]=t[x]
            hashmap2[t[x]]=s[x]
        return True

        
```
