# 217. Contains Duplicate
  
<br>**Problem:** https://leetcode.com/problems/contains-duplicate/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 10:39 local time

**Runtime:** 18 ms (beats 81.0618%)
**Memory:** 26 MB (beats 23.92579999999998%)


<!-- leetgit:submissionId=2141204685 codeHash=50dc445e7cbd2bc38179372190bd9ffeac97afafa80bbbdeda054c130e91fd65 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def containsDuplicate(self, nums):
        if len(set(nums))<len(nums):
            return True
        return False
        
        
```
