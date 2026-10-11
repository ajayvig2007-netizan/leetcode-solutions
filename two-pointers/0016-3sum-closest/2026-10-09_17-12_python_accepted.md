# 16. 3Sum Closest
  
<br>**Problem:** https://leetcode.com/problems/3sum-closest/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 17:12 local time

**Runtime:** 476 ms (beats 25.815200000000132%)
**Memory:** 12.3 MB (beats 98.03139999999999%)


<!-- leetgit:submissionId=2167245470 codeHash=03cf4f660c61898724e25e0593f1fd7b8fea8b72848639a520405c57d383e849 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
                ans=nums[i]+nums[r]+nums[l]
                if abs(target-ans)<abs(target-s):
                    s=ans
                if ans==target:
                    return ans
                elif ans<target:
                    l+=1
                else:
                    r-=1
        return s



        
```
