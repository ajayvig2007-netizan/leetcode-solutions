# 152. Maximum Product Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-product-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 09:24 local time

**Runtime:** 12 ms (beats 29.692999999999987%)
**Memory:** 13.2 MB (beats 32.793000000000006%)


<!-- leetgit:submissionId=2163760224 codeHash=989d6946e7d5b278c3ff8a4ad97afd44e47ce2a3eee9aebffecd429df2e8ff23 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxProduct(self, nums):
        curr=nums[0]
        temp=nums[0]
        max1=nums[0]

        for r in range(1,len(nums)):
            a=curr
            b=temp

            curr=max(a*nums[r],nums[r],b*nums[r])
            temp=min(a*nums[r],nums[r],b*nums[r])

            max1=max(max1,curr)

        return max1
```
