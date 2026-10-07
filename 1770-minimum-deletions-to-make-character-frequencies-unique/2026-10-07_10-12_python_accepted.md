# 1770. Minimum Deletions to Make Character Frequencies Unique
  
<br>**Problem:** https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 10:12 local time

**Runtime:** 203 ms (beats 52.83000000000009%)
**Memory:** 12.8 MB (beats 62.264100000000006%)


<!-- leetgit:submissionId=2164896642 codeHash=8c51e9a26b9c7d7c5ce10deed08c2b80b1b046aec99d77b1d14c858f51a8db4d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minDeletions(self, s):
        hashmap={}
        for r in s:
            hashmap[r]=hashmap.get(r,0)+1
        list1=[]
        del1=[]
        count=0
        for r in set(s):
            if hashmap[r] not in list1:
                list1.append(hashmap[r])
            else:
                while hashmap[r] in list1 and hashmap[r]>=0:
                    hashmap[r]-=1
                    count+=1
                if hashmap[r]==0:
                    del hashmap[r]
                else:
                    list1.append(hashmap[r])
        return count

        
        
```
