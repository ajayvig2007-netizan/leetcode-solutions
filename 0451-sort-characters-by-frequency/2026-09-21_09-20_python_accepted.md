# 451. Sort Characters By Frequency
  
<br>**Problem:** https://leetcode.com/problems/sort-characters-by-frequency/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sorting, Heap (Priority Queue), Bucket Sort, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 09:20 local time

**Runtime:** 15 ms (beats 80.34970000000001%)
**Memory:** 13.4 MB (beats 74.6894%)


<!-- leetgit:submissionId=2148220621 codeHash=c6871add7eeac807e28adaa6ee5aa42b0532875f1bfdfb62c9d7de3f620067c2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def frequencySort(self, s):
        d = {}

        for x in s:
            d[x] = d.get(x, 0) + 1

        ans = ""

        for x in sorted(d, key=d.get, reverse=True):
            ans += x * d[x]

        return ans
```
