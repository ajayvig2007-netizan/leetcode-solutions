# 334. Increasing Triplet Subsequence
  
<br>**Problem:** https://leetcode.com/problems/increasing-triplet-subsequence/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Greedy, Longest Increasing Subsequence<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 10:06 local time

**Runtime:** 23 ms (beats 75.16180000000003%)
**Memory:** 24.4 MB (beats 57.78190000000003%)


<!-- leetgit:submissionId=2158791959 codeHash=573e9bb9097882872b7d46b7a2cc18bef97822047e633bdfb7584d81f0127a61 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def increasingTriplet(self, nums):
        a = float('inf')
        b = float('inf')
        for x in nums:
            if x <= a:
                a = x
            elif x <= b:
                b = x
            else:
                return True
                
        return False
```
