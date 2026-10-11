# 1770. Minimum Deletions to Make Character Frequencies Unique
  
<br>**Problem:** https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 18:13 local time

**Runtime:** 203 ms (beats 52.83000000000009%)
**Memory:** 12.7 MB (beats 94.3396%)


<!-- leetgit:submissionId=2165278033 codeHash=cac0559435a7db23904556ff28c9c5510b1a3a78f007aa16ac829b6ffe20466a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minDeletions(self, s):
        hashmap={}
        count=0
        for r in s:
            hashmap[r]=hashmap.get(r,0)+1
        ans=[]
        for r in set(s):
            if hashmap[r] not in ans:
                ans.append(hashmap[r])
            else:
                while hashmap[r] in ans and hashmap[r]>0:
                    hashmap[r]-=1
                    count+=1    
                ans.append(hashmap[r])
        return count
        
        
```
