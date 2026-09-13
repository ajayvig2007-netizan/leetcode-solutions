# 724. Find Pivot Index
  
<br>**Problem:** https://leetcode.com/problems/find-pivot-index/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 12:28 local time

**Runtime:** 3028 ms (beats 5.10970000000012%)
**Memory:** 13.3 MB (beats 26.787099999999988%)


<!-- leetgit:submissionId=2140352036 codeHash=d11bfc95477a9e9dd56b0c44039d4876a750f6f52c3f655f98bf27c3e5d1ac0b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def pivotIndex(self, nums):
        leftsum=0
        rightsum=0
        for i in range(len(nums)):
            if sum(nums[:i+1])==sum(nums[i:len(nums)]):
                return i
        return -1
        
        
```
