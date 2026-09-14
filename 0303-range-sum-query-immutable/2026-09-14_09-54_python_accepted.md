# 303. Range Sum Query - Immutable
  
<br>**Problem:** https://leetcode.com/problems/range-sum-query-immutable/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Design, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 09:54 local time

**Runtime:** 347 ms (beats 20.463499999999986%)
**Memory:** 16 MB (beats 87.17600000000002%)


<!-- leetgit:submissionId=2141172930 codeHash=653cd07a59496a90abe5b5b463b0187b3da5186927762631060f76a205a272bc notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class NumArray(object):

    def __init__(self, nums):
        self.prefix=[]
        curr=0
        for i in nums:
            self.prefix.append(i)

        
        

    def sumRange(self, left, right):
       # r=self.prefix[right]
        #l=self.prefix[left-1]  if left>0 else 0
        return sum(self.prefix[left:right+1])

        


# Your NumArray object will be instantiated and called as such:
# obj = NumArray(nums)
# param_1 = obj.sumRange(left,right)
```
