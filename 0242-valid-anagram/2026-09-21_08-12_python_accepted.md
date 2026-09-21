# 242. Valid Anagram
  
<br>**Problem:** https://leetcode.com/problems/valid-anagram/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 08:12 local time

**Runtime:** 23 ms (beats 47.06720000000003%)
**Memory:** 13.5 MB (beats 30.003700000000002%)


<!-- leetgit:submissionId=2148191173 codeHash=7b4fb831c0c86c226e6844cc85225f9caf139e476f0bc4be15fbe471dbaf6bed notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def isAnagram(self, s, t):
        return sorted(s)==sorted(t)
        
```
