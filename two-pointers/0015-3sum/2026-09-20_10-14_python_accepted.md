# 15. 3Sum
  
<br>**Problem:** https://leetcode.com/problems/3sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 10:14 local time

**Runtime:** 9283 ms (beats 5.007599999999177%)
**Memory:** 19 MB (beats 14.828499999999975%)


<!-- leetgit:submissionId=2147310648 codeHash=f3bf25fd48423362f6a3d407287c823fc5827eb822c733c21b263bcd9bc1fea9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def threeSum(self, nums):
        ans = []

        for r in range(len(nums) - 2):
            seen = set()

            for l in range(r + 1, len(nums)):
                need = -(nums[r] + nums[l])

                if need in seen:
                    triplet = [need, nums[r], nums[l]]
                    triplet.sort()

                    if triplet not in ans:
                        ans.append(triplet)

                seen.add(nums[l])

        return ans
```
