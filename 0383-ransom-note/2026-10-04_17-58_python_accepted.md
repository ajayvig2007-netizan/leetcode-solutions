# 383. Ransom Note
  
<br>**Problem:** https://leetcode.com/problems/ransom-note/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-04 17:58 local time

**Runtime:** 49 ms (beats 23.71129999999999%)
**Memory:** 12.7 MB (beats 23.08149999999999%)


<!-- leetgit:submissionId=2162083085 codeHash=0720c91dab6a40febb4ece48d5d0718d05104fedbe1164081c696142e4911b68 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canConstruct(self, ransomNote, magazine):
        if len(ransomNote)>len(magazine):
            return False
        hashmap1={}
        hashmap2={}
        for i in magazine:
            hashmap1[i]=hashmap1.get(i,0)+1
        for i in ransomNote:
            hashmap2[i]=hashmap2.get(i,0)+1
        for i in ransomNote:
            if i not in hashmap1 or hashmap2[i]>hashmap1[i]:
                return False
        return True

                
        
```
