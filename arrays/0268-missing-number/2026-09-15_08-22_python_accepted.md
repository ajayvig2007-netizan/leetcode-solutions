# 268. Missing Number
  
<br>**Problem:** https://leetcode.com/problems/missing-number/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Math, Binary Search, Bit Manipulation, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 08:22 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.2 MB (beats 94.30619999999999%)


<!-- leetgit:submissionId=2142116406 codeHash=c222cbdf4d0acfc232501e9c7e9d295a8cfaa23ed36ab35f0dcd3d401f1ef8d6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def missingNumber(self, nums):
        a=len(nums)
        sum1=a*(a+1)//2
        sum12=sum(nums)
        return abs(sum12-sum1)
        
        
```
