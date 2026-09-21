# 49. Group Anagrams
  
<br>**Problem:** https://leetcode.com/problems/group-anagrams/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 10:32 local time

**Runtime:** 31 ms (beats 20.539499999999986%)
**Memory:** 18.2 MB (beats 9.813199999999984%)


<!-- leetgit:submissionId=2148272091 codeHash=0a6081942f7409364f7ffd3f66c02c2d2f663029633d3e284d891efac5e06f4d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
from collections import defaultdict

class Solution(object):
    def groupAnagrams(self, strs):
        hashmap = defaultdict(list) 
        for word in strs: 
            count = [0] * 26
            for char in word:
                count[ord(char) - ord('a')] += 1
            hashmap[tuple(count)].append(word)   
        return list(hashmap.values())
```
