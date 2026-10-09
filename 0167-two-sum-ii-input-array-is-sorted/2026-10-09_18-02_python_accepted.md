# 167. Two Sum II - Input Array Is Sorted
  
<br>**Problem:** https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Binary Search<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 18:02 local time

**Runtime:** 11 ms (beats 31.136800000000004%)
**Memory:** 14.3 MB (beats 45.532500000000006%)


<!-- leetgit:submissionId=2167275270 codeHash=d2077b8b468fc00e0d38912d5d59d88ff96c1a53b1a676857ce60aed110b4869 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def twoSum(self, numbers, target):
        l=0
        r=len(numbers)-1
        while l<r:
            sum1=numbers[l]+numbers[r]
            if sum1==target:
                return[l+1,r+1]
            elif sum1>target:
                r-=1
            else:
                l+=1

        
```
