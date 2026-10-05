# 496. Next Greater Element I
  
<br>**Problem:** https://leetcode.com/problems/next-greater-element-i/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Stack, Monotonic Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 08:55 local time

**Runtime:** 210 ms (beats 5.166099999999984%)
**Memory:** 12.7 MB (beats 26.482600000000012%)


<!-- leetgit:submissionId=2157711933 codeHash=f1f686e503d19a8da781310cef0f6166ea255b3a0c51bb27d43e6b4ebd1dd94a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def nextGreaterElement(self, nums1, nums2):
        ans=[-1]*(len(nums1))
        for i in range(len(nums1)):
            for j in range(len(nums2)):
                if nums1[i]==nums2[j]:
                    for k in range(j+1,len(nums2)):
                        if nums1[i]<nums2[k]:
                            ans[i]=nums2[k]
                            break
        return ans

        
```
