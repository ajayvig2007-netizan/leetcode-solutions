# 219. Contains Duplicate II
  
<br>**Problem:** https://leetcode.com/problems/contains-duplicate-ii/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 11:31 local time

**Runtime:** 39 ms (beats 92.82300000000001%)
**Memory:** 27.1 MB (beats 33.62989999999999%)


<!-- leetgit:submissionId=2141246130 codeHash=5b0c39eb33bdc52f154c5c3ebfc147f9b6899236a52f309a95dbb07bc2fd4f57 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def containsNearbyDuplicate(self, nums, k):
        if len(set(nums))==len(nums):
            return False
        hashmap={}
        for i in range(len(nums)):
            if nums[i] in hashmap:
                if abs(hashmap[nums[i]]-i)<=k:
                    return True
            hashmap[nums[i]]=i
        return False
        
        
```
