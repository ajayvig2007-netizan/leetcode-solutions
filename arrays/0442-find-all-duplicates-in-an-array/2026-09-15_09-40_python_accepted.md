# 442. Find All Duplicates in an Array
  
<br>**Problem:** https://leetcode.com/problems/find-all-duplicates-in-an-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 09:40 local time

**Runtime:** 60 ms (beats 30.08020000000002%)
**Memory:** 25.1 MB (beats 16.135499999999986%)


<!-- leetgit:submissionId=2142162193 codeHash=6655dbb11311880ce77862e26d47505fb2cb922c48834bd883892416a9208d02 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findDuplicates(self, nums):
        hashmap={}
        c=[]
        for i in range(len(nums)):
            hashmap[nums[i]]=hashmap.get(nums[i],0)+1
            if hashmap[nums[i]]>=2:
                c.append(nums[i])
        return c

        

        
```
