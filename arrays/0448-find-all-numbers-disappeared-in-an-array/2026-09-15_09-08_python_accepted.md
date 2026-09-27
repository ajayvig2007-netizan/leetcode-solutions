# 448. Find All Numbers Disappeared in an Array
  
<br>**Problem:** https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 09:08 local time

**Runtime:** 87 ms (beats 5.180100000000031%)
**Memory:** 26.8 MB (beats 75.30020000000002%)


<!-- leetgit:submissionId=2142140268 codeHash=6da63c0a1ebec7080bfd118d9fe458c36da92dc4333643cd2b1d760d8f1fea05 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findDisappearedNumbers(self, nums):
        arra = []
        len1=len(nums)
        nums = set(sorted(nums))

        for i in range(1,len1+1):
            if i not in nums:
                arra.append(i)

        return arra
```
