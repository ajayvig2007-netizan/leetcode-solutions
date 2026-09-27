# 451. Sort Characters By Frequency
  
<br>**Problem:** https://leetcode.com/problems/sort-characters-by-frequency/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sorting, Heap (Priority Queue), Bucket Sort, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 17:55 local time

**Runtime:** 11 ms (beats 96.38609999999998%)
**Memory:** 14.4 MB (beats 24.203299999999988%)


<!-- leetgit:submissionId=2154943028 codeHash=e24844f18ae1024e718e031402d3b79621a76a199660124b582f5efb4dbef366 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def frequencySort(self, s):
        list1=list(s)
        hashmap={}
        for x in list1:
            hashmap[x]=hashmap.get(x,0)+1
        ans=""
        for x in sorted(hashmap,key=hashmap.get,reverse=True):
            ans+=x*hashmap[x]
        return ans

        
        
        
        
```
