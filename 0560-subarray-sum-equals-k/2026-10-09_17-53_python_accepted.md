# 560. Subarray Sum Equals K
  
<br>**Problem:** https://leetcode.com/problems/subarray-sum-equals-k/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 17:53 local time

**Runtime:** 35 ms (beats 67.0908%)
**Memory:** 15.2 MB (beats 25.937299999999997%)


<!-- leetgit:submissionId=2167270143 codeHash=117181f46484fbf9942fae87f8404baaa0ee011cb092205dd734e6d58b705800 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def subarraySum(self, nums, k):
        hashmap={0:1}
        count=0
        sum1=0
        for r in range(len(nums)):
            sum1+=nums[r]
            if sum1-k in hashmap:
                count+=hashmap[sum1-k]
            hashmap[sum1]=hashmap.get(sum1,0)+1
        return count
        
```
