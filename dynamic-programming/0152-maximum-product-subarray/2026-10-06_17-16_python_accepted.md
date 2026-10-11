# 152. Maximum Product Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-product-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 17:16 local time

**Runtime:** 19 ms (beats 5.147999999999986%)
**Memory:** 13.1 MB (beats 71.78620000000001%)


<!-- leetgit:submissionId=2164181578 codeHash=6c376b49780d1327431fbac4e8699f2d4f4a5c78dad8178be2e94f558f12bd44 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxProduct(self, nums):
        max1=nums[0]
        min1=nums[0]
        curr=nums[0]

        for r in range(1,len(nums)):
            b=min1
            c=max1

            max1=max(nums[r],b*nums[r],nums[r]*c)
            min1=min(nums[r],nums[r]*b,nums[r]*c)
            curr=max(curr,max1)

        return curr
```
