# 442. Find All Duplicates in an Array
  
<br>**Problem:** https://leetcode.com/problems/find-all-duplicates-in-an-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 19:08 local time

**Runtime:** 75 ms (beats 15.140200000000018%)
**Memory:** 19.6 MB (beats 62.21779999999999%)


<!-- leetgit:submissionId=2142635286 codeHash=624225db999d15ad771fc4d19d57dc0a6f5054faf8bd725559fe95a553406001 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findDuplicates(self, nums):
        i=0
        result=[]
        while i<len(nums):
            correct=nums[i]-1
            if nums[correct]!=nums[i] and i!=correct:
                nums[correct],nums[i]=nums[i],nums[correct]
            else:
                i+=1
        for i in range(len(nums)):
            if i+1!=nums[i]:
                result.append(nums[i])
        return result
        
        
```
