# 451. Sort Characters By Frequency
  
<br>**Problem:** https://leetcode.com/problems/sort-characters-by-frequency/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sorting, Heap (Priority Queue), Bucket Sort, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 10:43 local time

**Runtime:** 12 ms (beats 89.64560000000002%)
**Memory:** 13.5 MB (beats 30.234700000000004%)


<!-- leetgit:submissionId=2148282100 codeHash=085fc3c22d41a9d5e2ca7546198932dbaaf2d5cbae3dfd6f7cfef077e28eb109 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
