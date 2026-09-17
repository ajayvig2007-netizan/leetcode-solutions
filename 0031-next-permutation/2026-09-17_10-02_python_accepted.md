# 31. Next Permutation
  
<br>**Problem:** https://leetcode.com/problems/next-permutation/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 10:02 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 21.605700000000006%)


<!-- leetgit:submissionId=2144296034 codeHash=22668f3263f133b271d93a51209d56d34e5cb8c3ef252c4532334d5ab1cb37b3 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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

        nums[i+1:] = nums[i+1:][::-1]
```
