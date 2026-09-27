# 1631. Number of Sub-arrays With Odd Sum
  
<br>**Problem:** https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Dynamic Programming, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 10:34 local time

**Runtime:** 66 ms (beats 79.16659999999999%)
**Memory:** 15.9 MB (beats 35.41659999999999%)


<!-- leetgit:submissionId=2141201105 codeHash=bb161900761a6e289bdb696ca7782e65fbeb8a4ce1709bba94340cd1cf75b984 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
            if curr%2==0 or curr==0:
                even+=1
            else:
                odd+=1
        return (odd*even)%(10**9+7)

        
        
```
