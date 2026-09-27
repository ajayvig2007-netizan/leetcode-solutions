# 303. Range Sum Query - Immutable
  
<br>**Problem:** https://leetcode.com/problems/range-sum-query-immutable/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Design, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 09:55 local time

**Runtime:** 5 ms (beats 63.0343%)
**Memory:** 15.9 MB (beats 87.17600000000002%)


<!-- leetgit:submissionId=2141173755 codeHash=9ce4fd75ba169a6aa0500ea705963dc6bbafd45e98dee23f7f11314989dc7d77 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class NumArray(object):

    def __init__(self, nums):
        self.prefix=[]
        curr=0
        for i in nums:
            curr+=i
            self.prefix.append(curr)

        
        

    def sumRange(self, left, right):
        r=self.prefix[right]
        l=self.prefix[left-1]  if left>0 else 0
        return r-l

        


# Your NumArray object will be instantiated and called as such:
# obj = NumArray(nums)
# param_1 = obj.sumRange(left,right)
```
