# 560. Subarray Sum Equals K
  
<br>**Problem:** https://leetcode.com/problems/subarray-sum-equals-k/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 12:28 local time

**Runtime:** 27 ms (beats 88.82359999999997%)
**Memory:** 15.1 MB (beats 26.067199999999996%)


<!-- leetgit:submissionId=2140352519 codeHash=296a1471d46be71f63a3e82c5400c9a2f96ba058d436e07d6f712fb1bf80f16c notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def subarraySum(self, nums, k):
        hashmap={0:1}
        count=0
        sum=0
        for i in range(len(nums)):
            sum+=nums[i]
            if sum-k in hashmap:
                count += hashmap[sum-k]

            if sum in hashmap:
                hashmap[sum]+=1
            else:
                hashmap[sum]=1
        return count

        
```
