# 907. Koko Eating Bananas
  
<br>**Problem:** https://leetcode.com/problems/koko-eating-bananas/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 09:58 local time

**Runtime:** 158 ms (beats 70.19279999999998%)
**Memory:** 13.5 MB (beats 15.265600000000006%)


<!-- leetgit:submissionId=2156642636 codeHash=758bc7537b5dd5ffc6d92c5d7986ab1dda3496437705c7b96664166b566f50c0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minEatingSpeed(self, piles, h):
        l = 1
        r = max(piles)

        while l <= r:
            mid = (l + r) // 2
            count = 0

            for x in piles:
                count += (x + mid - 1) // mid

            if count <= h:
                r = mid - 1
            else:
                l = mid + 1

        return l
```
