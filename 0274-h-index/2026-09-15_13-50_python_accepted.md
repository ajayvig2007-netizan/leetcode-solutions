# 274. H-Index
  
<br>**Problem:** https://leetcode.com/problems/h-index/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Sorting, Counting Sort<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 13:50 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.7 MB (beats 43.82469999999999%)


<!-- leetgit:submissionId=2142380715 codeHash=298d904e0ba2d15353ee762a482f0bde2f41a8b4b9ba0a48ccad88f9a50880ff notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def hIndex(self, citations):
        citations.sort()

        n = len(citations)

        for i in range(n):
            h = n - i

            if citations[i] >= h:
                return h

        return 0
```
