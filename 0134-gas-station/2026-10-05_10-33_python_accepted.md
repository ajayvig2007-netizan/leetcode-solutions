# 134. Gas Station
  
<br>**Problem:** https://leetcode.com/problems/gas-station/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 10:33 local time

**Runtime:** 53 ms (beats 16.74739999999999%)
**Memory:** 18.5 MB (beats 15.18440000000001%)


<!-- leetgit:submissionId=2162732391 codeHash=1932491c22b64bb2536cfdc0711be0ec9263414d6789aea0222a28b665603400 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def canCompleteCircuit(self,gas,cost):
        total=0
        tank=0
        start=0
        for i in range(len(gas)):
            total+=gas[i]-cost[i]
            tank+=gas[i]-cost[i]
            if tank<0:
                tank=0
                start=i+1
        if total>=0:
            return start
        return -1
```
