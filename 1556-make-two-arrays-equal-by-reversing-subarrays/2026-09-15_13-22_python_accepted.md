# 1556. Make Two Arrays Equal by Reversing Subarrays
  
<br>**Problem:** https://leetcode.com/problems/make-two-arrays-equal-by-reversing-subarrays/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 13:22 local time

**Runtime:** 7 ms (beats 37.378600000000006%)
**Memory:** 12.7 MB (beats 3.398100000000012%)


<!-- leetgit:submissionId=2142361368 codeHash=39556341c10cc85a717a6edfe71f9b24ab808b2d146d7fa2642fd97982dd9220 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canBeEqual(self, target, arr):
        hashmap={}
        hashmap1={}
    
        for i in range(len(target)):
            hashmap[target[i]]=hashmap.get(target[i],0)+1
            hashmap1[arr[i]]=hashmap1.get(arr[i],0)+1
        if hashmap!=hashmap1:
                return False
        return True      
```
