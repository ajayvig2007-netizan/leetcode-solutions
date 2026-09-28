# 34. Find First and Last Position of Element in Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 19:37 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.1 MB (beats 29.898599999999995%)


<!-- leetgit:submissionId=2156044909 codeHash=de94669cbad59962219a3b0f5dc24d61d10de1b11b3409fbb87c9b8d6fc5461d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def searchRange(self, nums, target):
        l=0
        r=len(nums)-1
        ans=[-1,-1]
        while(l<=r):
            mid=(l+r)//2
            if nums[mid]==target:
                ans[0]=mid
                r=mid-1
            elif nums[mid]>target:
                r=mid-1
            else:
                l=mid+1
        l=0
        r=len(nums)-1
        while(l<=r):
            mid=(l+r)//2
            if nums[mid]==target:
                ans[1]=mid
                l=mid+1
            elif nums[mid]>target:
                r=mid-1
            else:
                l=mid+1
        return ans

        
```
