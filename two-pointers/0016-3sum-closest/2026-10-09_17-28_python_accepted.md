# 16. 3Sum Closest
  
<br>**Problem:** https://leetcode.com/problems/3sum-closest/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 17:28 local time

**Runtime:** 469 ms (beats 38.75180000000013%)
**Memory:** 12.3 MB (beats 79.2037%)


<!-- leetgit:submissionId=2167254590 codeHash=43a6624dd929c9daef2b51c5bbdfdfc9c1105f6ed4c88bc1afd29c8e12eac1ea notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def threeSumClosest(self, nums, target):
        nums=sorted(nums)
        s=nums[0]+nums[1]+nums[2]
        for i in range(len(nums)-2):
            l=i+1
            r=len(nums)-1
            while l<r:
                currsum=nums[i]+nums[l]+nums[r]
                if abs(target-currsum)<abs(target-s):
                    s=currsum
                if currsum==target:
                    return s
                elif currsum<target:
                    l+=1
                else:
                    r-=1
        return s       
```
