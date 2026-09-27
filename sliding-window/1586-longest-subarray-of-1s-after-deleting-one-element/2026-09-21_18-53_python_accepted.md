# 1586. Longest Subarray of 1's After Deleting One Element
  
<br>**Problem:** https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 18:53 local time

**Runtime:** 115 ms (beats 5.725500000000137%)
**Memory:** 14.5 MB (beats 92.9338%)


<!-- leetgit:submissionId=2148667276 codeHash=d7364a6790a6cdd16f9ce22a09447b3cadf489db148b5ca068f9b7cbc8721fa2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestSubarray(self, nums):
        hashmap1={}
        l=0
        max1=0
        r=0
        while r<len(nums):
            if nums[r]==0:
                hashmap1[nums[r]]=hashmap1.get(nums[r],0)+1
                while hashmap1[0]>1:
                    if nums[l]==0:
                        hashmap1[0]-=1
                    l+=1
            max1=max(max1,r-l)
            r+=1

        return max1


        
        
```
