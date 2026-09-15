# 442. Find All Duplicates in an Array
  
<br>**Problem:** https://leetcode.com/problems/find-all-duplicates-in-an-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-15 09:41 local time

**Runtime:** 90 ms (beats 6.973000000000018%)
**Memory:** 23.8 MB (beats 40.90309999999998%)


<!-- leetgit:submissionId=2142163201 codeHash=0e0d6b45da954da6ec89cd68aec0aa43a609c0568c53b4d4f10c53b9eb91aa88 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findDuplicates(self, nums):
        from collections import Counter

        freq = Counter(nums)
        ans = []

        for x in freq:
            if freq[x] == 2:
                ans.append(x)

        return ans
```
