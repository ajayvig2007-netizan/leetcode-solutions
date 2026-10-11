# 1988. Minimize Maximum Pair Sum in Array
  
<br>**Problem:** https://leetcode.com/problems/minimize-maximum-pair-sum-in-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:12 local time

**Runtime:** 1175 ms (beats 5.9569999999999155%)
**Memory:** 24.7 MB (beats 84.76809999999999%)


<!-- leetgit:submissionId=2163113622 codeHash=e83b7d4bba30616d3c5ebbcbc13dc809cecbcba6ac3b5ea44dfdebbe178802ca notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minPairSum(self, nums):
        nums.sort()
        max1=0
        for i in range(len(nums)//2):
            max1=max(nums[i]+nums[len(nums)-1-i],max1)
        return max1
            
        
```
