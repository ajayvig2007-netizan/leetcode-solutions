# 387. First Unique Character in a String
  
<br>**Problem:** https://leetcode.com/problems/first-unique-character-in-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Queue, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 11:15 local time

**Runtime:** 110 ms (beats 36.4469999999999%)
**Memory:** 15.9 MB (beats 19.42029999999998%)


<!-- leetgit:submissionId=2148308963 codeHash=9fce4e5380f89b0da4803efd06ba8d8e6cf83a5fac90fa1d11ce5acbea303c33 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def firstUniqChar(self, s):
        hashmap={}
        for x in s:
            hashmap[x]=hashmap.get(x,0)+1
        for i in range(len(s)):
            if hashmap[s[i]]==1:

                return i
        return -1

        
```
