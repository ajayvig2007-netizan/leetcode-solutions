# 387. First Unique Character in a String
  
<br>**Problem:** https://leetcode.com/problems/first-unique-character-in-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Queue, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-04 17:34 local time

**Runtime:** 108 ms (beats 41.24519999999992%)
**Memory:** 12.5 MB (beats 89.39339999999999%)


<!-- leetgit:submissionId=2162064826 codeHash=853230375b88db7ad16b5bc5ef2a2bafc8510a2199d124bfbec497b7348dbf35 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def firstUniqChar(self, s):
        hashmap={}
        for i in s:
            hashmap[i]=hashmap.get(i,0)+1
        for i,j in enumerate(s):
            if hashmap[j]==1:
                return i
        return -1

    

        
        
```
