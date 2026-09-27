# 217. Contains Duplicate
  
<br>**Problem:** https://leetcode.com/problems/contains-duplicate/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 10:39 local time

**Runtime:** 33 ms (beats 29.003700000000016%)
**Memory:** 25.8 MB (beats 71.91109999999998%)


<!-- leetgit:submissionId=2141204974 codeHash=7c32d0bd34371f3408d654c681730afa89862c7da440b728d75673c9f4560055 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def containsDuplicate(self, nums):
        seen = set()

        for x in nums:
            if x in seen:
                return True
            seen.add(x)

        return False
```
