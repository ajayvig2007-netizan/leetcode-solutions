# 18. 4Sum
  
<br>**Problem:** https://leetcode.com/problems/4sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 17:13 local time

**Runtime:** 541 ms (beats 29.794199999999805%)
**Memory:** 12.3 MB (beats 94.572%)


<!-- leetgit:submissionId=2166273405 codeHash=e0e6e1ecb546d2fb818690d2bcd88a9b457273fae20df53ff6e10eb8b258370b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def fourSum(self, nums, target):
        nums=sorted(nums)
        ans=[]
        sum1=0
        for i in range(len(nums)-3):
            if i>0 and nums[i-1]==nums[i]:
                continue
            for j in range(i+1,len(nums)-2):
                if j>i+1 and nums[j-1]==nums[j]:
                    continue
                l=j+1
                r=len(nums)-1
                while l<r:
                    sum1=nums[i]+nums[j]+nums[l]+nums[r]
                    if sum1==target:
                        ans.append([nums[i],nums[j],nums[l],nums[r]])
                        l+=1
                        r-=1
                        while l<r and nums[l-1]==nums[l]:
                            l+=1
                        while r>l and nums[r+1]==nums[r]:
                            r-=1
                    elif sum1>target:
                        r-=1
                    else:
                        l+=1
        return ans
                
        
```
