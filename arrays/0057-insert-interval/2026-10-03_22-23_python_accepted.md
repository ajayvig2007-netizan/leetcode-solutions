# 57. Insert Interval
  
<br>**Problem:** https://leetcode.com/problems/insert-interval/<br>

**Difficulty:** Medium<br>
**Topics:** Array<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 22:23 local time

**Runtime:** 1 ms (beats 72.6944%)
**Memory:** 14 MB (beats 91.2594%)


<!-- leetgit:submissionId=2161285180 codeHash=9935e174ccdaea6fdd7683b872715259083dc97035e55f5bfc643bd9a5d728a7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def insert(self, intervals, newInterval):
        intervals.append(newInterval)
        intervals=sorted(intervals)
        start=intervals[0]
        ans=[]
        for i in range(1,len(intervals)):
            if start[1]>=intervals[i][0]:
                start[1]=max(start[1],intervals[i][1])
            else:
                ans.append(start)
                start=intervals[i]
        ans.append(start)
        return ans
                
        
```
