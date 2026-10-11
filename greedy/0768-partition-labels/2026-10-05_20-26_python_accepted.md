# 768. Partition Labels
  
<br>**Problem:** https://leetcode.com/problems/partition-labels/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, Two Pointers, String, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 20:26 local time

**Runtime:** 3 ms (beats 94.36619999999999%)
**Memory:** 12.3 MB (beats 57.746500000000005%)


<!-- leetgit:submissionId=2163245707 codeHash=a627a4a56bbf31c83e39d5339ae8d519a016e85467deddea6ea8e7787946873d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def partitionLabels(self, s):
        hashmap={}
        for i,c in enumerate(s):
            hashmap[c]=i
        ans=[]
        si,e=0,0
        for i,c in enumerate(s):
            si+=1
            e=max(e,hashmap[c])
            if i==e:
                ans.append(si)
                e=0
                si=0
        return ans

        
        
```
