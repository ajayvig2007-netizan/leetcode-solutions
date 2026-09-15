# 268. Missing Number
  
<br>**Problem:** https://leetcode.com/problems/missing-number/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Math, Binary Search, Bit Manipulation, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 18:39 local time

**Runtime:** 19 ms (beats 26.242200000000008%)
**Memory:** 13.2 MB (beats 67.96789999999999%)


<!-- leetgit:submissionId=2142607487 codeHash=467fade168c8a6d0df16cdea809c9d5f4a14b775a07d2b188f751cdb95ff5009 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def missingNumber(self, nums):
        i=0
        while i<len(nums):
            correct=nums[i]
            if correct<len(nums)and nums[correct]!=nums[i] and i!=correct:
                nums[i],nums[correct]=nums[correct],nums[i]
            else:
                i+=1
        for i in range(len(nums)):
            if i!=nums[i]:
                return i
        return len(nums)
        
```
