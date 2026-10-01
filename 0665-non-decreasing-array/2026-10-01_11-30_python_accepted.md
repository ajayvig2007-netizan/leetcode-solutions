# 665. Non-decreasing Array
  
<br>**Problem:** https://leetcode.com/problems/non-decreasing-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 11:30 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 13.2 MB (beats 53.96820000000001%)


<!-- leetgit:submissionId=2158875484 codeHash=c77c5a9db3e1a61eef0b6b18bd6c10eae3b34c5fe91ef1b06830c7a9333f2dba notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def checkPossibility(self, nums):
        count = 0

        for i in range(1, len(nums)):
            if nums[i] < nums[i-1]:
                count += 1

                if count > 1:
                    return False

                if i == 1 or nums[i] >= nums[i-2]:
                    nums[i-1] = nums[i]
                else:
                    nums[i] = nums[i-1]

        return True
```
