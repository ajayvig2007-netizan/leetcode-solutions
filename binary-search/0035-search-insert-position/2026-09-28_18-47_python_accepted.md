# 35. Search Insert Position
  
<br>**Problem:** https://leetcode.com/problems/search-insert-position/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 18:47 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.9 MB (beats 66.779%)


<!-- leetgit:submissionId=2155993176 codeHash=bb6c366cacf3b29d9f7f5a2b4ba7c976343b9aa122075baedb61175a42f1b00d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchInsert(self, nums, target):
        l=0
        r=len(nums)-1
        while(l<=r):
            mid=(r+l)//2
            if nums[mid]==target:
                return mid
            elif nums[mid]>target:
                r=mid-1
            else:
                l=mid+1
        return l
        
```
