# 290. Word Pattern
  
<br>**Problem:** https://leetcode.com/problems/word-pattern/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 11:09 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 57.120799999999996%)


<!-- leetgit:submissionId=2148304363 codeHash=fc84fa1be817e55aefc358093327a5e65592bd94130aa4e3f172de4037f0d287 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def wordPattern(self, pattern, s):
        hashmap1={}
        hashmap={}
        s=s.split()
        if len(s)!=len(pattern):
            return False
        for i in range(len(pattern)):
                
            if pattern[i]  in hashmap and hashmap[pattern[i]]!=s[i]:
                return False
            elif s[i]  in hashmap1 and hashmap1[s[i]]!=pattern[i]:
                return False
            hashmap1[s[i]]=pattern[i]
            hashmap[pattern[i]]=s[i]   
        return True  
```
