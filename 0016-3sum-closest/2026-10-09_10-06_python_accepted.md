# 16. 3Sum Closest
  
<br>**Problem:** https://leetcode.com/problems/3sum-closest/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 10:06 local time

**Runtime:** 466 ms (beats 44.89450000000013%)
**Memory:** 12.6 MB (beats 8.126099999999994%)


<!-- leetgit:submissionId=2166922484 codeHash=1ff8cd9e5b1a83f79919218c9c7af8ca42dbd50c6503120ace666da9cc9c3bf7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def threeSumClosest(self, nums, target):
        nums.sort()
        ans=nums[0]+nums[1]+nums[2]
        for i in range(len(nums)-2):
            l=i+1
            r=len(nums)-1
            while l<r:
                s=nums[i]+nums[l]+nums[r]
                if abs(target-s)<abs(target-ans):
                    ans=s
                if s==target:
                    return s
                elif s<target:
                    l+=1
                else:
                    r-=1

        return ans
```
