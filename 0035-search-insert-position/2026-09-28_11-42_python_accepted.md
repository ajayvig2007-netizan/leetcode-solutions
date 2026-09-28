# 35. Search Insert Position
  
<br>**Problem:** https://leetcode.com/problems/search-insert-position/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 11:42 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13 MB (beats 31.296299999999995%)


<!-- leetgit:submissionId=2155641222 codeHash=d4b12a717cdc550ff575596e74229f416ef6983fca6cda63e0f8dec602a92848 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchInsert(self, nums, target):
        l=0
        r=len(nums)-1
        while(l<=r):
            mid=(l+r)//2
            if nums[mid]==target:
                return mid
            elif nums[mid]>target:
                r=mid-1
            else:
                l=mid+1
        return l

        
```
