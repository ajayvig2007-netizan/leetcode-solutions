# 525. Contiguous Array
  
<br>**Problem:** https://leetcode.com/problems/contiguous-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 18:27 local time

**Runtime:** 142 ms (beats 7.828799999999989%)
**Memory:** 17.4 MB (beats 6.466899999999969%)


<!-- leetgit:submissionId=2159204816 codeHash=8fc83263da2e65281d1c2ecf8ce42718e0e50552b501f9d4d5677f0fcc2e1276 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findMaxLength(self, nums):
        num1=[0]*len(nums)
        sum1=0
        for i in range(len(nums)):
            if nums[i]==0:
                sum1-=1
            else:
                sum1+=1
            num1[i]=sum1
        d = {0: -1}
        max1 = 0

        for i in range(len(nums)):
            if num1[i] in d:
                max1 = max(max1, i - d[num1[i]])
            else:
                d[num1[i]] = i

        return max1
                  
```
