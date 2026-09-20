# 1. Two Sum
  
<br>**Problem:** https://leetcode.com/problems/two-sum/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 09:29 local time

**Runtime:** 3 ms (beats 55.888%)
**Memory:** 13.1 MB (beats 54.77689999999998%)


<!-- leetgit:submissionId=2147279490 codeHash=6d2efd42748ffac4bf69f4752e25433eca017653ed7478ec361c9d18115daa57 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def twoSum(self, nums, target):
        hashmap={}
        r=0
        while r<len(nums):
            if target-nums[r] in hashmap:
                return(r,hashmap[target-nums[r]])
            hashmap[nums[r]]=r
            r+=1
        
        
        
```
