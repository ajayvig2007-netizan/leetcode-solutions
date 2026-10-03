# 452. Minimum Number of Arrows to Burst Balloons
  
<br>**Problem:** https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Greedy, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 16:04 local time

**Runtime:** 221 ms (beats 13.540000000000058%)
**Memory:** 43.6 MB (beats 89.36200000000002%)


<!-- leetgit:submissionId=2160976703 codeHash=003a79db9ac88e49fd0452c77b19b87d115bd91634db9b31dd1fd55dc895c32c notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findMinArrowShots(self, intervals):
        intervals=sorted(intervals)
        first=intervals[0]
        ans=[]
        count=1
        for i in range(1,len(intervals)):
            if first[1]>=intervals[i][0]:
                first[1]=min(first[1],intervals[i][1])
            else:
                count+=1
                ans.append(first)
                first=intervals[i]
        ans.append(first)
        return count
        

        
```
