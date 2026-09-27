# 41. First Missing Positive
  
<br>**Problem:** https://leetcode.com/problems/first-missing-positive/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Hash Table<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 19:24 local time

**Runtime:** 91 ms (beats 5.234300000000031%)
**Memory:** 20.2 MB (beats 40.8303%)


<!-- leetgit:submissionId=2142650509 codeHash=a1454767d14e4ee3e9203ddcc142ed5a03cbf4d5977866f66f9b0b1885f70fd5 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def firstMissingPositive(self, nums):
        i=0
        while i<len(nums):
                correct =nums[i]-1
                if nums[i] >= 1 and nums[i] <= len(nums) and nums[correct] != nums[i]:
                    nums[correct],nums[i]=nums[i],nums[correct]
                else:
                    i+=1
        for i in range(len(nums)):
            if i+1!=nums[i]:
                return i+1
        return len(nums)+1
```
