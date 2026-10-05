# 56. Merge Intervals
  
<br>**Problem:** https://leetcode.com/problems/merge-intervals/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Sorting, Quicksort<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 15:52 local time

**Runtime:** 9 ms (beats 71.7073%)
**Memory:** 16.2 MB (beats 40.8378%)


<!-- leetgit:submissionId=2160968033 codeHash=e1a8d72d0e9a1a1485580d15409cd787ddfef14875995398ee4e4afded83a66b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def merge(self, intervals):
        intervals=sorted(intervals)
        first=intervals[0]
        ans=[]
        for i in range(1,len(intervals)):
            if first[1]>=intervals[i][0]:
                first[1]=max(first[1],intervals[i][1])
            else:
                ans.append(first)
                first=intervals[i]
        ans.append(first)
        return ans


        
        
```
