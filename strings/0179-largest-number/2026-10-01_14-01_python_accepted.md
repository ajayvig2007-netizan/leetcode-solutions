# 179. Largest Number
  
<br>**Problem:** https://leetcode.com/problems/largest-number/<br>

**Difficulty:** Medium<br>
**Topics:** Array, String, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 14:01 local time

**Runtime:** 13 ms (beats 12.508099999999983%)
**Memory:** 12.3 MB (beats 97.52449999999999%)


<!-- leetgit:submissionId=2159005524 codeHash=6b591db03d6959c936461e56cda3b7e3252eef4ba4be56b80e8c9419d14ae4ea notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def largestNumber(self, nums):
        nums = list(map(str, nums))
        ans = ""

        while nums:
            k = 0

            for i in range(1, len(nums)):
                if nums[i] + nums[k] > nums[k] + nums[i]:
                    k = i

            ans += nums[k]
            nums.pop(k)

        if ans[0] == '0':
            return '0'

        return ans
```
