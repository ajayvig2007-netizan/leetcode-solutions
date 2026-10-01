# 665. Non-decreasing Array
  
<br>**Problem:** https://leetcode.com/problems/non-decreasing-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 11:36 local time

**Runtime:** 3 ms (beats 30.1587%)
**Memory:** 13.1 MB (beats 84.1269%)


<!-- leetgit:submissionId=2158882517 codeHash=1ac8cdde7088558d6c089936aae5d9223a57e97dd8c4342d64e85828635167b4 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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

                if i > 1 and nums[i] < nums[i-2]:
                    nums[i] = nums[i-1]
                else:
                    nums[i-1] = nums[i]

        return True
```
