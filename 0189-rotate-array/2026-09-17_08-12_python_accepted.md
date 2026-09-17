# 189. Rotate Array
  
<br>**Problem:** https://leetcode.com/problems/rotate-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 08:12 local time

**Runtime:** 25 ms (beats 33.85039999999998%)
**Memory:** 28.2 MB (beats 17.875100000000007%)


<!-- leetgit:submissionId=2144223942 codeHash=8180946503eccc89469d1af1bbb83b5c2a29843303f61f5f0778844d9118ec1b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def rotate(self, nums, k):
        k%=len(nums)
        nums[:]=nums[-k:]+nums[:-k]
        return nums
        
```
