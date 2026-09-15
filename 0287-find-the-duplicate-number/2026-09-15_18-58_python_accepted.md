# 287. Find the Duplicate Number
  
<br>**Problem:** https://leetcode.com/problems/find-the-duplicate-number/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Binary Search, Bit Manipulation, Pigeonhole Principle, Floyd's Cycle Finding Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 18:58 local time

**Runtime:** 161 ms (beats 5.3932000000000135%)
**Memory:** 20.3 MB (beats 99.49430000000001%)


<!-- leetgit:submissionId=2142625457 codeHash=f26ccbbd77e375015cc952232e95c49196916aaf0d24497324098cccc940bb2c notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findDuplicate(self, nums):
        i=0
        while i<len(nums):
            correct=nums[i]-1
            if nums[correct]!=nums[i] and correct!=i:
                nums[correct],nums[i]=nums[i],nums[correct]
            else:
                i+=1
        for i in range(0,len(nums)):
            if i+1!=nums[i]:
                return nums[i]

        
```
