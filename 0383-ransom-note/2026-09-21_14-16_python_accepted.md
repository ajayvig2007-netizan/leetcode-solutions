# 383. Ransom Note
  
<br>**Problem:** https://leetcode.com/problems/ransom-note/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 14:16 local time

**Runtime:** 43 ms (beats 27.04999999999998%)
**Memory:** 12.6 MB (beats 88.28219999999999%)


<!-- leetgit:submissionId=2148450241 codeHash=7b24ed7f2c0967d020fb0d9761f423ef90d28d01b0bdaa8bf13ca67b4c8784f0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canConstruct(self, ransomNote, magazine):
        hashmap1={}
        hashmap2={}
        for i in ransomNote:
            hashmap1[i]=hashmap1.get(i,0)+1
        for j in magazine:
            if j in ransomNote:
                hashmap2[j]=hashmap2.get(j,0)+1
        for j in ransomNote:
            if j not in hashmap2:
                return False
            if hashmap1[j]>hashmap2[j]:
                return False
        return True
        
        

```
