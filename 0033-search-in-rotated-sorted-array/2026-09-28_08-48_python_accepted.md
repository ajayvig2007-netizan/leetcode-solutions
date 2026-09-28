# 33. Search in Rotated Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/search-in-rotated-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 08:48 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 10.623399999999997%)


<!-- leetgit:submissionId=2155495994 codeHash=6e740ace1daedbb837ca8ec5bf948b3fceeb9aae46f16da62f2e262a2c58f69b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def search(self, nums, target):
        for i in range(len(nums)):
            if nums[i]==target:
                return i
        return -1
            
```
