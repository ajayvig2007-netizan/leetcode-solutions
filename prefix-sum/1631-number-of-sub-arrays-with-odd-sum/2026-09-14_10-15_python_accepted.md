# 1631. Number of Sub-arrays With Odd Sum
  
<br>**Problem:** https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Dynamic Programming, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 10:15 local time

**Runtime:** 91 ms (beats 32.291499999999964%)
**Memory:** 17.8 MB (beats 16.66659999999999%)


<!-- leetgit:submissionId=2141187607 codeHash=fca558c2ecf6236a1927777b423df9319ef429acbcb0cb013e355bc6432fadac notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def numOfSubarrays(self, arr):
        prefixarr=[]
        even=1
        odd=0
        curr=0
        for r in arr:
            curr+=r
            prefixarr.append(curr)
            if curr%2==0 or curr==0:
                even+=1
            else:
                odd+=1
        return (odd*even)%(10**9+7)

        
        
```
