# 745. Find Smallest Letter Greater Than Target
  
<br>**Problem:** https://leetcode.com/problems/find-smallest-letter-greater-than-target/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 19:18 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.6 MB (beats 37.87570000000001%)


<!-- leetgit:submissionId=2156024955 codeHash=2bb2545501d6bca7b73d9eca316e1225feccb935eb752bde6ef77384c955e01b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def nextGreatestLetter(self, nums, target):
        l=0
        r=len(nums)-1
        if nums[r]<=target:
            return nums[0]
        while(l<=r):
            mid=(r+l)//2
            if nums[mid]==target:
                while nums[mid]==target:
                    mid+=1
                return nums[mid]
            elif nums[mid]>target:
                r=mid-1
            else:
                l=mid+1
        
        return nums[l]
        
        
```
