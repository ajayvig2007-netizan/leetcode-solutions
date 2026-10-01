# 128. Longest Consecutive Sequence
  
<br>**Problem:** https://leetcode.com/problems/longest-consecutive-sequence/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Union-Find<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 20:53 local time

**Runtime:** 60 ms (beats 37.18250000000002%)
**Memory:** 26.8 MB (beats 72.07169999999996%)


<!-- leetgit:submissionId=2159331350 codeHash=1059ef9b67861153dccb7feae3f1256104c97edd6229de677f95969182ad1d62 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestConsecutive(self, nums):
        nums=set(nums)
        count=0
        max1=0
        for i in nums:
            if i-1 not in nums:
                count=1
                while i+1 in nums:
                    count+=1
                    i+=1
                max1=max(max1,count)
        return max1
        
```
