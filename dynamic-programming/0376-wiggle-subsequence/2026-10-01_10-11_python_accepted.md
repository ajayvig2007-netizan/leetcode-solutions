# 376. Wiggle Subsequence
  
<br>**Problem:** https://leetcode.com/problems/wiggle-subsequence/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 10:11 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 65.798%)


<!-- leetgit:submissionId=2158796331 codeHash=5867fb27f2e0bd0e7e94639b3210f1aa1e2507c01cd1d5b9fa0f2b694658973e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def wiggleMaxLength(self, nums):
        if len(nums) == 1:
            return 1

        count = 1
        prev = 0

        for i in range(1, len(nums)):
            if nums[i] > nums[i-1]:
                if prev != 1:
                    count += 1
                    prev = 1

            elif nums[i] < nums[i-1]:
                if prev != -1:
                    count += 1
                    prev = -1

        return count
```
