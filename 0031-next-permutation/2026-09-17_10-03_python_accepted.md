# 31. Next Permutation
  
<br>**Problem:** https://leetcode.com/problems/next-permutation/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 10:03 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 59.267300000000006%)


<!-- leetgit:submissionId=2144297089 codeHash=a3ccd7b5d41fb8f0327c9fb63a4354d521d4710ed91258622d3926096b8e9d61 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def nextPermutation(self, nums):
        i = len(nums) - 2

        while i >= 0 and nums[i] >= nums[i+1]:
            i -= 1

        if i >= 0:
            j = len(nums) - 1
            while nums[j] <= nums[i]:
                j -= 1
            nums[i], nums[j] = nums[j], nums[i]

        l = i + 1
        r = len(nums) - 1

        while l < r:
            nums[l], nums[r] = nums[r], nums[l]
            l += 1
            r -= 1
```
