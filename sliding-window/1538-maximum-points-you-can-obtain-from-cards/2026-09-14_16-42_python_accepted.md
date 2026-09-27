# 1538. Maximum Points You Can Obtain from Cards
  
<br>**Problem:** https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 16:42 local time

**Runtime:** 27 ms (beats 47.643399999999986%)
**Memory:** 19.3 MB (beats 30.32789999999999%)


<!-- leetgit:submissionId=2141484605 codeHash=5887e8e1cfe1b496e0971066af31b88f304aa9738df7df6be6895a7a0ac46cdb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxScore(self, cardpoints, k):
        sum1=0
        for r in range(0,k,1):
            sum1+=cardpoints[r]
        max1=sum1
        k=len(cardpoints)-k
        for l in range(len(cardpoints)-1,k-1,-1):
            sum1-=cardpoints[r]
            sum1+=cardpoints[l]
            max1=max(max1,sum1)
            r-=1
        return max1
            

        
        
```
