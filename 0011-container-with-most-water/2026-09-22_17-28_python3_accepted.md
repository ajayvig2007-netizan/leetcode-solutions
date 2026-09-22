# 11. Container With Most Water
  
<br>**Problem:** https://leetcode.com/problems/container-with-most-water/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Greedy<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 17:28 local time

**Runtime:** 103 ms (beats 5.68649999999999%)
**Memory:** 29.8 MB (beats 5.888200000000047%)


<!-- leetgit:submissionId=2149674980 codeHash=86cb9b9ab8e11bf6470bfbc9568b605129bae946514d0b92a12934d52c707996 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxArea(self, height: list[int]) -> int:
        r=len(height)-1
        l=0
        max1=0
        while l<r:
            res=(r-l)*min(height[l],height[r])
            max1=max(res,max1)
            if height[l]>height[r]:
                r-=1
            else:
                l+=1
        return max1
        
```
