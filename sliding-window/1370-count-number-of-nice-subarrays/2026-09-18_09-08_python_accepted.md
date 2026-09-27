# 1370. Count Number of Nice Subarrays
  
<br>**Problem:** https://leetcode.com/problems/count-number-of-nice-subarrays/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Math, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 09:08 local time

**Runtime:** 82 ms (beats 94.59090000000005%)
**Memory:** 17.3 MB (beats 21.13199999999999%)


<!-- leetgit:submissionId=2145305454 codeHash=5593d245a43c94f7e3b77d992fb398537e32c99f73d288c51b63da5911ffaaf1 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
