# 1770. Minimum Deletions to Make Character Frequencies Unique
  
<br>**Problem:** https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 10:15 local time

**Runtime:** 199 ms (beats 53.77340000000009%)
**Memory:** 12.8 MB (beats 62.264100000000006%)


<!-- leetgit:submissionId=2164899184 codeHash=89c46f87fc71719014f5c4d74772c505623de7c947b22ecd3745bd94569d31c2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minDeletions(self, s):
        hashmap={}
        for r in s:
            hashmap[r]=hashmap.get(r,0)+1
        list1=[]

        count=0
        for r in set(s):
            if hashmap[r] not in list1:
                list1.append(hashmap[r])
            else:
                while hashmap[r] in list1 and hashmap[r]>0:
                    hashmap[r]-=1
                    count+=1
                # if hashmap[r]==0:
                #     del hashmap[r]
                else:
                    list1.append(hashmap[r])
        return count

        
        
```
