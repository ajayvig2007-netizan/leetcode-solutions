# 1370. Count Number of Nice Subarrays
  
<br>**Problem:** https://leetcode.com/problems/count-number-of-nice-subarrays/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Math, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 09:09 local time

**Runtime:** 79 ms (beats 96.10030000000005%)
**Memory:** 17.3 MB (beats 21.13199999999999%)


<!-- leetgit:submissionId=2145306432 codeHash=eec8301f10663ae79e6dccb093920bf636143c3516702da609186a421d7c35d0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def numberOfSubarrays(self, nums, k):
        count = {0: 1}
        odd = 0
        ans = 0
        for x in nums:
            if x % 2 == 1:
                odd += 1
            if odd - k in count:
                ans += count[odd - k]
            if odd in count:
                count[odd] += 1
            else:
                count[odd] = 1
        return ans
```
