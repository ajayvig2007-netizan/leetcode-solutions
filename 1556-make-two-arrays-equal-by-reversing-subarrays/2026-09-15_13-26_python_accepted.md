# 1556. Make Two Arrays Equal by Reversing Subarrays
  
<br>**Problem:** https://leetcode.com/problems/make-two-arrays-equal-by-reversing-subarrays/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 13:26 local time

**Runtime:** 5 ms (beats 48.0582%)
**Memory:** 12.6 MB (beats 57.76700000000001%)


<!-- leetgit:submissionId=2142364459 codeHash=e66db00556fac17ff98b80497478ccffec902d818e824711daa4ad24d073bc94 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canBeEqual(self, target, arr):
        hashmap={}
        hashmap1={}
        for i in range(len(target)):
            hashmap[target[i]]=hashmap.get(target[i],0)+1
            hashmap1[arr[i]]=hashmap1.get(arr[i],0)+1
        return (hashmap==hashmap1)   
```
