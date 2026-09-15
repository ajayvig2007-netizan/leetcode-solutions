# 645. Set Mismatch
  
<br>**Problem:** https://leetcode.com/problems/set-mismatch/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Bit Manipulation, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 10:54 local time

**Runtime:** 8 ms (beats 82.9498%)
**Memory:** 13.8 MB (beats 55.2619%)


<!-- leetgit:submissionId=2142227404 codeHash=d2e8f4cdc60a90951e7bd6d22428d47191c2ce73e744b99180595b69dc4a4ba2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findErrorNums(self, nums):
        n = len(nums)
        set1 = set(nums)
        missing = 0
        for i in range(1, n + 1):
            if i not in set1:
                missing = i
                break
     
        expected = n * (n + 1) // 2
        actual = sum(nums)

        duplicate = missing - (expected - actual)

        return [duplicate, missing]
```
