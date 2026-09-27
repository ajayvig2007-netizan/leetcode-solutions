# 75. Sort Colors
  
<br>**Problem:** https://leetcode.com/problems/sort-colors/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting, Quicksort, Bubble Sort<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 11:11 local time

**Runtime:** 7 ms (beats 7.530199999999999%)
**Memory:** 12.3 MB (beats 91.4506%)


<!-- leetgit:submissionId=2144361202 codeHash=9ce9f37f3d2729427482715af7871ae4f1161536b695cabe73e263d4e2865a91 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def sortColors(self, nums):
        n = len(nums)

        for j in range(n):
            for i in range(n - 1 - j):
                if nums[i] > nums[i + 1]:
                    nums[i], nums[i + 1] = nums[i + 1], nums[i]
```
