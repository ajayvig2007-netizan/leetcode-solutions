# 75. Sort Colors
  
<br>**Problem:** https://leetcode.com/problems/sort-colors/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting, Quicksort, Bubble Sort<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 19:33 local time

**Runtime:** 4 ms (beats 13.417200000000008%)
**Memory:** 12.5 MB (beats 20.170299999999997%)


<!-- leetgit:submissionId=2148706453 codeHash=fd9c1a2204762f092de04bf01943f5ebcaba103ac5e675830358bd5ea7c19285 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def sortColors(self, nums):
        for i in range(len(nums)):
            for j in range(i+1,len(nums)):
                if nums[i]>nums[j]:
                    nums[i],nums[j]=nums[j],nums[i]
        
```
