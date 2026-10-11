# 692. Top K Frequent Words
  
<br>**Problem:** https://leetcode.com/problems/top-k-frequent-words/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Trie, Sorting, Heap (Priority Queue), Bucket Sort, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 09:12 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.5 MB (beats 38.03680000000001%)


<!-- leetgit:submissionId=2164849605 codeHash=4abc26aa6b4ea5bc5e3421b8328a7988a4246995caa3cec8d8e955a924292e25 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def topKFrequent(self, words, k):
        hashmap={}
        for i in range(len(words)):
            hashmap[words[i]]=hashmap.get(words[i],0)+1
        list1=sorted(hashmap.keys(),key=lambda word:(-hashmap[word],word))
        return list1[:k]
        
        
        
```
