# 56. Merge Intervals
  
<br>**Problem:** https://leetcode.com/problems/merge-intervals/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Sorting, Quicksort<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-03 09:55 local time

**Runtime:** 8 ms (beats 83.8249%)
**Memory:** 16.1 MB (beats 55.740700000000004%)


<!-- leetgit:submissionId=2160696563 codeHash=dd90885769935ada9ab7b92c1847bf623310e9f9d6521c8f71411a8017790948 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def merge(self, intervals):
        intervals=sorted(intervals)
        first=intervals[0]
        ans=[]
        for i in range(1,len(intervals)):
            if first[1]>=intervals[i][0]:
                first[1]=max(intervals[i][1],first[1])
            else:
                ans.append(first)
                first=intervals[i]
        ans.append(first)
        return ans

        
        
```
