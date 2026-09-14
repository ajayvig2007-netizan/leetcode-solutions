# 219. Contains Duplicate II
  
<br>**Problem:** https://leetcode.com/problems/contains-duplicate-ii/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 11:31 local time

**Runtime:** 70 ms (beats 29.613000000000035%)
**Memory:** 29.5 MB (beats 8.247100000000003%)


<!-- leetgit:submissionId=2141246408 codeHash=76e556b0d7a43ba600d86f0e0b49edc6224239c51bbd916823b1de1f1439d402 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def containsNearbyDuplicate(self, nums, k):
        """if len(set(nums))==len(nums):
            return False"""
        hashmap={}
        for i in range(len(nums)):
            if nums[i] in hashmap:
                if abs(hashmap[nums[i]]-i)<=k:
                    return True
            hashmap[nums[i]]=i
        return False
        
        
```
