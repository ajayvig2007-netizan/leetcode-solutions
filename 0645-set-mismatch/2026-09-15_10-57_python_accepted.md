# 645. Set Mismatch
  
<br>**Problem:** https://leetcode.com/problems/set-mismatch/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Bit Manipulation, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 10:57 local time

**Runtime:** 51 ms (beats 22.368799999999982%)
**Memory:** 14.1 MB (beats 16.2954%)


<!-- leetgit:submissionId=2142229770 codeHash=3ebdd7df9cd4c9da6664a8425546e04fd8432c581687d4b53c2349e36e4151ab notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findErrorNums(self, nums):
        from collections import Counter

        count = Counter(nums)

        duplicate = 0
        missing = 0

        for i in range(1, len(nums) + 1):
            if count[i] == 2:
                duplicate = i
            if count[i] == 0:
                missing = i

        return [duplicate, missing]
```
