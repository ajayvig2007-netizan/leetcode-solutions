# 18. 4Sum
  
<br>**Problem:** https://leetcode.com/problems/4sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 09:53 local time

**Runtime:** 532 ms (beats 50.343199999999804%)
**Memory:** 12.2 MB (beats 99.4107%)


<!-- leetgit:submissionId=2165920752 codeHash=8bcf9400e289602cba0cb21e15d91676774ec92d8618469e72cd28389ee1f19f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def fourSum(self,nums,target):
        nums.sort()
        ans=[]
        n=len(nums)

        for i in range(n-3):
            if i>0 and nums[i]==nums[i-1]:
                continue

            for j in range(i+1,n-2):
                if j>i+1 and nums[j]==nums[j-1]:
                    continue

                l=j+1
                r=n-1

                while l<r:
                    s=nums[i]+nums[j]+nums[l]+nums[r]

                    if s==target:
                        ans.append([nums[i],nums[j],nums[l],nums[r]])

                        while l<r and nums[l]==nums[l+1]:
                            l+=1
                        while l<r and nums[r]==nums[r-1]:
                            r-=1

                        l+=1
                        r-=1

                    elif s<target:
                        l+=1
                    else:
                        r-=1

        return ans
```
