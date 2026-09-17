# 189. Rotate Array
  
<br>**Problem:** https://leetcode.com/problems/rotate-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 08:54 local time

**Runtime:** 13 ms (beats 49.36989999999998%)
**Memory:** 28.2 MB (beats 17.875100000000007%)


<!-- leetgit:submissionId=2144245711 codeHash=355ba0c59ec4cf04dd20463d2e1b2df889f70d59ef5d3975fab776044c419e4a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def rotate(self, nums, k):
        k%=len(nums)
        nums[:]=nums[-k:]+nums[:-k]
        
        
```
