# 1538. Maximum Points You Can Obtain from Cards
  
<br>**Problem:** https://leetcode.com/problems/maximum-points-you-can-obtain-from-cards/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 16:39 local time

**Runtime:** 28 ms (beats 39.85649999999998%)
**Memory:** 19.4 MB (beats 30.32789999999999%)


<!-- leetgit:submissionId=2141482660 codeHash=17e275e5f88e621a00a51f0ee25269f6fc63e4398c25ce57f56cd62c7624126f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def maxScore(self, cardPoints, k):
        sum1=0
        for i in range(k):
            sum1+=cardPoints[i]
        max1=sum1
        r=k-1
        l=len(cardPoints)-1
        while r>=0:
            sum1-=cardPoints[r]
            sum1+=cardPoints[l]
            l-=1
            r-=1
            max1=max(max1,sum1)
        return max1


        
```
