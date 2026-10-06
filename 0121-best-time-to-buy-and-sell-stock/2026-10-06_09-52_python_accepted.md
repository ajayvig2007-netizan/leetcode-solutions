# 121. Best Time to Buy and Sell Stock
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 09:52 local time

**Runtime:** 173 ms (beats 5.113899999999995%)
**Memory:** 19.5 MB (beats 14.628500000000003%)


<!-- leetgit:submissionId=2163785365 codeHash=389768776a8eb40685794e1ddaae8995e7d32c0f70bd2ee29de89844a045f4d3 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxProfit(self, nums):
        buy=nums[0]
        profit=0
        buy=nums[0]
        for i in range(1,len(nums)):
            buy=min(buy,nums[i])
            profit=max(profit,-buy+nums[i])
        return profit
```
