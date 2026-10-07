# 692. Top K Frequent Words
  
<br>**Problem:** https://leetcode.com/problems/top-k-frequent-words/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Trie, Sorting, Heap (Priority Queue), Bucket Sort, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 18:06 local time

**Runtime:** 4 ms (beats 53.61959999999999%)
**Memory:** 12.5 MB (beats 38.03680000000001%)


<!-- leetgit:submissionId=2165272175 codeHash=073ad9698416d8386f9237107ecdd2800dca9cd2bbd136fe1e5983a257b30e05 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def topKFrequent(self, words, k):
        hashmap={}
        for r in words:
            hashmap[r]=hashmap.get(r,0)+1
        list1=sorted(hashmap.keys(),key= lambda x: (-hashmap[x],x))
        return list1[:k]
        
```
