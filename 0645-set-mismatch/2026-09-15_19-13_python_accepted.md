# 645. Set Mismatch
  
<br>**Problem:** https://leetcode.com/problems/set-mismatch/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Bit Manipulation, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 19:13 local time

**Runtime:** 39 ms (beats 27.121699999999976%)
**Memory:** 13.5 MB (beats 67.7855%)


<!-- leetgit:submissionId=2142639926 codeHash=01b56d99e97c3512f2beed0bfc7b2d8cf9a599c8ef3f9cad10349bed7c126a4a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findErrorNums(self, nums):
        i=0
        while i<len(nums):
            correct=nums[i]-1
            if nums[correct]!=nums[i] and correct!=i:
                nums[correct],nums[i]=nums[i],nums[correct]
            else:
                i+=1
        for i in range(len(nums)):
            if i+1!=nums[i]:
                return [nums[i],i+1]


        
```
