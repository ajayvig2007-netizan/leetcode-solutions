# 41. First Missing Positive
  
<br>**Problem:** https://leetcode.com/problems/first-missing-positive/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Hash Table<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 10:14 local time

**Runtime:** 31 ms (beats 86.46500000000003%)
**Memory:** 26.2 MB (beats 13.167700000000012%)


<!-- leetgit:submissionId=2142190258 codeHash=18da825fbe3b6ea7576c1d2b098b8ba9f20c54c35d8adcfc811cc982e9257655 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def firstMissingPositive(self, nums):
        set1=set(nums)
        i=1
        while i<=len(nums):
            if i not in set1:
                return i
            i+=1
        return len(nums)+1

        
        
```
