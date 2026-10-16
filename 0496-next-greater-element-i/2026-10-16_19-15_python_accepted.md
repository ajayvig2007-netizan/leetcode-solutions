# 496. Next Greater Element I
  
<br>**Problem:** https://leetcode.com/problems/next-greater-element-i/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Stack, Monotonic Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-16 19:15 local time

**Runtime:** 213 ms (beats 5.058900000000038%)
**Memory:** 12.5 MB (beats 93.4989%)


<!-- leetgit:submissionId=2173863099 codeHash=75acf97a569ff48ed52d1907ad9418985362be5ce2e4fbad2029671c9c84e6f0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def nextGreaterElement(self, nums1, nums2):
        ans=[-1]*len(nums1)
        for j in range (len(nums1)):
            for i in range(len(nums2)):
                if nums1[j]==nums2[i]:
                    for k in range(i+1,len(nums2)):
                        if nums1[j]<nums2[k]:
                            ans[j]=nums2[k]
                            break
        return ans

        
        
```
