# 3869. Smallest Index With Digit Sum Equal to Index
  
<br>**Problem:** https://leetcode.com/problems/smallest-index-with-digit-sum-equal-to-index/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Math<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-24 08:10 local time

**Runtime:** 3 ms (beats 75.36229999999999%)
**Memory:** 12.4 MB (beats 61.594200000000015%)


<!-- leetgit:submissionId=2151480679 codeHash=f848e567625599969e5a9bc614fb902c933dc7580bc790b8bc0d4ac85e7b58c1 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution:
    def smallestIndex(self, nums):
        for i, num in enumerate(nums):
            total = 0
            while num > 0:
                total += num % 10
                num //= 10
            if total == i:
                return i
        return -1
```
