# 15. 3Sum
  
<br>**Problem:** https://leetcode.com/problems/3sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 10:08 local time

**Runtime:** 9806 ms (beats 5.007599999999177%)
**Memory:** 19.5 MB (beats 7.483899999999976%)


<!-- leetgit:submissionId=2147306516 codeHash=579f92a9ca3748755fa2bcca1d500ca17c975ca69b05d5efe2241b0279b0075e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def threeSum(self, nums):
        r=0
        ans=[]
        l=0
        
        while r<len(nums)-2:
            dict1={}
            
            l=r+1
            while l<len(nums):
                need = -(nums[r] + nums[l])
                
                if need in dict1:
                    triplet = [need, nums[r], nums[l]]
                    triplet.sort()

                    if triplet not in ans:
                        ans.append(triplet)
                dict1[nums[l]]=l
                l+=1
            r+=1
        return ans
                    

        
```
