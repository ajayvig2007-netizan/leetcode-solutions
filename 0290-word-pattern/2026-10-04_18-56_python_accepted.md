# 290. Word Pattern
  
<br>**Problem:** https://leetcode.com/problems/word-pattern/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-04 18:56 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 59.191500000000005%)


<!-- leetgit:submissionId=2162133155 codeHash=98b85b777650ec77b454ac2f5828e45203ff0008fa3e4136df85b4f85f9adadc notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def wordPattern(self, pattern, s):
        s=s.split(" ")
        if len(s)!=len(pattern):
            return False
        hashmap1={}
        hashmap2={}
        for i in range(len(s)):
            if s[i] in hashmap1 and hashmap1[s[i]]!=pattern[i]:
                return False
            if pattern[i] in hashmap2 and hashmap2[pattern[i]]!=s[i]:
                return False
            hashmap1[s[i]]=pattern[i]
            hashmap2[pattern[i]]=s[i]
        return True


        
        
```
