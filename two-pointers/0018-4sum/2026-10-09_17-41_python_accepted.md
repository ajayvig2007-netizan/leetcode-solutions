# 18. 4Sum
  
<br>**Problem:** https://leetcode.com/problems/4sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 17:41 local time

**Runtime:** 555 ms (beats 16.8389999999997%)
**Memory:** 12.3 MB (beats 65.65899999999999%)


<!-- leetgit:submissionId=2167262425 codeHash=95545eb7309f47f4ff30350e32bc4cd9ba45ce75e290b9e641a0b7c42809df15 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def fourSum(self, nums, target):
        nums=sorted(nums)
        ans=[]
        for i in range(len(nums)-3):
            if i>0 and nums[i]==nums[i-1]:
                continue
            for j in range(i+1,len(nums)-2):
                if j>i+1 and nums[j-1]==nums[j]:
                    continue
                l=j+1
                r=len(nums)-1
                while l<r:
                    sum1=nums[i]+nums[j]+nums[r]+nums[l]
                    if sum1==target:
                        ans.append([nums[i],nums[j],nums[r],nums[l]])
                        l+=1
                        r-=1
                        while l<r and nums[r+1]==nums[r]:
                            r-=1
                        while l<r  and nums[l-1]==nums[l]:
                            l+=1
                    elif sum1>target:
                        r-=1
                    else:
                        l+=1
        return ans
                
        
```
