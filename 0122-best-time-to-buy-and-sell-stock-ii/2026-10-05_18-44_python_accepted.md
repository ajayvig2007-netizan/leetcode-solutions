# 122. Best Time to Buy and Sell Stock II
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:44 local time

**Runtime:** 3 ms (beats 66.15449999999998%)
**Memory:** 13.8 MB (beats 66.6113%)


<!-- leetgit:submissionId=2163141270 codeHash=ff0d53ffc2d6e5bc7a3c03b70be0fdd1056fa3dc3bfe4bca6f62838418f938f8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxProfit(self, prices):
        ans=0
        for i in range(len(prices)-1):
            if prices[i]<prices[i+1]:
                ans+=prices[i+1]-prices[i]
        return ans

        
```
