# 179. Largest Number
  
<br>**Problem:** https://leetcode.com/problems/largest-number/<br>

**Difficulty:** Medium<br>
**Topics:** Array, String, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 13:56 local time

**Runtime:** 9 ms (beats 27.687299999999983%)
**Memory:** 12.6 MB (beats 39.34859999999999%)


<!-- leetgit:submissionId=2159001915 codeHash=6305b953ca59fd92e85926e7936e8eeb47944a56e4a53ea7ef4534e61f6956aa notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def largestNumber(self, nums):
        from functools import cmp_to_key

        nums = map(str, nums)

        def cmp(a, b):
            if a + b > b + a:
                return -1
            return 1

        nums = sorted(nums, key=cmp_to_key(cmp))

        ans = ''.join(nums)

        if ans[0] == '0':
            return '0'

        return ans
```
