# 958. Sort Array By Parity II
  
<br>**Problem:** https://leetcode.com/problems/sort-array-by-parity-ii/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-17 12:08 local time

**Runtime:** 19 ms (beats 21.778799999999993%)
**Memory:** 14.2 MB (beats 67.1506%)


<!-- leetgit:submissionId=2144420823 codeHash=ba6ac45e901a69eb2d64284a9c559661090c04fdce57768fd285db85d3ce65d4 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def sortArrayByParityII(self, nums):
        even = 0
        odd = 1

        while even < len(nums) and odd < len(nums):
            if nums[even] % 2 == 0:
                even += 2
            elif nums[odd] % 2 == 1:
                odd += 2
            else:
                nums[even], nums[odd] = nums[odd], nums[even]
                even += 2
                odd += 2

        return nums
```
