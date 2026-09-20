# 560. Subarray Sum Equals K
  
<br>**Problem:** https://leetcode.com/problems/subarray-sum-equals-k/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 09:38 local time

**Runtime:** 39 ms (beats 50.773300000000006%)
**Memory:** 14.6 MB (beats 73.34640000000002%)


<!-- leetgit:submissionId=2147286800 codeHash=f8aad80862494ad9a18ccd8e4933c2d8cee2822b9e5593c5ed50c25da25f0d80 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def subarraySum(self, nums, k):
        hashmap={0:1}
        r=0
        sum1=0
        count=0
        while r<len(nums):
            sum1+=nums[r]
            if sum1-k in hashmap:
                count+=hashmap[sum1-k] 
            hashmap[sum1]=hashmap.get(sum1,0)+1
            r+=1
        return count  
        
```
