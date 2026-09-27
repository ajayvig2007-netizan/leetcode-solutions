# 287. Find the Duplicate Number
  
<br>**Problem:** https://leetcode.com/problems/find-the-duplicate-number/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Binary Search, Bit Manipulation, Pigeonhole Principle, Floyd's Cycle Finding Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 10:26 local time

**Runtime:** 51 ms (beats 24.4663%)
**Memory:** 27.1 MB (beats 15.617799999999994%)


<!-- leetgit:submissionId=2142200360 codeHash=6cc6d554dfc039df49ce75fff2d715d9676ede3688c2cbb33789e5d3a7990d9a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findDuplicate(self, nums):
        hashmap={}
        for i in range(len(nums)):
            hashmap[nums[i]]=hashmap.get(nums[i],0)+1
            if hashmap[nums[i]]>1:
                return nums[i]

        
```
