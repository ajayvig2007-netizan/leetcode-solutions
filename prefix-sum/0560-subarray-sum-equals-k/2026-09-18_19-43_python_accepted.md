# 560. Subarray Sum Equals K
  
<br>**Problem:** https://leetcode.com/problems/subarray-sum-equals-k/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 19:43 local time

**Runtime:** 38 ms (beats 54.3657%)
**Memory:** 15.2 MB (beats 18.237100000000016%)


<!-- leetgit:submissionId=2145806930 codeHash=e878ac386031fe82ba0197c5aabb9c720b9a3e97d93f42463b514c6a83d5957f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def subarraySum(self, nums, k):
        hashmap={0:1}
        sum1=0
        count=0
        for i in range(len(nums)):
            sum1+=nums[i]
            if sum1-k in hashmap:
                count+=hashmap[sum1-k]
            hashmap[sum1]=hashmap.get(sum1,0)+1
        return count
        
```
