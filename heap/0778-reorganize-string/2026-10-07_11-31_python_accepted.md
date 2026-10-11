# 778. Reorganize String
  
<br>**Problem:** https://leetcode.com/problems/reorganize-string/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Greedy, Sorting, Heap (Priority Queue), Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 11:31 local time

**Runtime:** 15 ms (beats 5.772399999999992%)
**Memory:** 12.3 MB (beats 94.2278%)


<!-- leetgit:submissionId=2164967522 codeHash=a964bbff3c8617d63bf437720c0d5b1bc32947e42984f5dbede032c0643ba389 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python

class Solution(object):
    def reorganizeString(self,s):
        hashmap={}
        for c in s:
            hashmap[c]=hashmap.get(c,0)+1
        ans=""
        while hashmap:
            x=sorted(hashmap,key=hashmap.get,reverse=True)
            if len(ans)>0 and x[0]==ans[-1]:
                if len(x)==1:
                    return ""
                c=x[1]
            else:
                c=x[0]
            ans+=c
            hashmap[c]-=1
            if hashmap[c]==0:
                del hashmap[c]
        return ans

```
