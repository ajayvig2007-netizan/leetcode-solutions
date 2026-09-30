# 503. Next Greater Element II
  
<br>**Problem:** https://leetcode.com/problems/next-greater-element-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Stack, Monotonic Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 11:45 local time

**Runtime:** 7288 ms (beats 5.04649999999997%)
**Memory:** 14.1 MB (beats 79.27640000000001%)


<!-- leetgit:submissionId=2157856662 codeHash=3eeae55d8258198c81bccc93188f99e4d0788ea4e475affdfd6b3ab50ddf62a0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def nextGreaterElements(self, nums):
        n = len(nums)
        ans = [-1] * n

        for i in range(n):
            for j in range(1, n):
                k = (i + j) % n

                if nums[k] > nums[i]:
                    ans[i] = nums[k]
                    break

        return ans
        
```
