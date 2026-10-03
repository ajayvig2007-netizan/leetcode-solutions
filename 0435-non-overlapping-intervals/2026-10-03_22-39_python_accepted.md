# 435. Non-overlapping Intervals
  
<br>**Problem:** https://leetcode.com/problems/non-overlapping-intervals/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 22:39 local time

**Runtime:** 176 ms (beats 29.868300000000055%)
**Memory:** 45.3 MB (beats 26.886100000000056%)


<!-- leetgit:submissionId=2161301775 codeHash=c1f9f2db9a79966c50c90f8346f60cd1d942d34271ed41f91fd82af3246b7895 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def eraseOverlapIntervals(self, intervals):
        intervals=sorted(intervals,key=lambda x: x[1])
        start=intervals[0]
        count=0
        for i in range(1,len(intervals)):
            if start[1]>intervals[i][0]:
                count+=1
            else:
                start=intervals[i]
        return count
```
