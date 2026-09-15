# 645. Set Mismatch
  
<br>**Problem:** https://leetcode.com/problems/set-mismatch/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Bit Manipulation, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 10:59 local time

**Runtime:** 6 ms (beats 88.23089999999999%)
**Memory:** 14 MB (beats 39.117%)


<!-- leetgit:submissionId=2142232398 codeHash=684514c8bebe40e18c2f527ddad4be6aa6656fa13842798d6138c0bfcea4857d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findErrorNums(self, nums):
        n = len(nums)
        set1 = set(nums)
        find= 0
        for i in range(1, n + 1):
            if i not in set1:
                find=i
                break
     
        exe=n*(n + 1)//2
        total=sum(nums)

        duplicate=find-(exe-total)

        return [duplicate, find]
```
