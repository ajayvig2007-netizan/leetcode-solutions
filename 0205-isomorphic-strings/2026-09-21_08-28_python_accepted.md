# 205. Isomorphic Strings
  
<br>**Problem:** https://leetcode.com/problems/isomorphic-strings/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 08:28 local time

**Runtime:** 17 ms (beats 12.350500000000006%)
**Memory:** 13.5 MB (beats 62.77499999999999%)


<!-- leetgit:submissionId=2148197148 codeHash=4b284f17924006788bad4c76436ea934cde6328cb0fc3248a88a3918d0e5664d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isIsomorphic(self, s, t):
        hashmap1 = {}
        hashmap2 = {}

        for i in range(len(s)):
            if s[i] in hashmap1 and hashmap1[s[i]] != t[i]:
                return False

            if t[i] in hashmap2 and hashmap2[t[i]] != s[i]:
                return False

            hashmap1[s[i]] = t[i]
            hashmap2[t[i]] = s[i]

        return True
```
