# 454. 4Sum II
  
<br>**Problem:** https://leetcode.com/problems/4sum-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-02 10:56 local time

**Runtime:** 627 ms (beats 23.277399999999876%)
**Memory:** 12.8 MB (beats 22.844899999999996%)


<!-- leetgit:submissionId=2159808502 codeHash=28aa8f371bf67b666c25744b5832e30b1c72ed8853e15b1c83c181a139008575 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def fourSumCount(self, nums1, nums2, nums3, nums4):
        hashmap={}
        count=0
        for i in nums1:
            for j in nums2:
                hashmap[i+j]=hashmap.get(i+j,0)+1
        for i in nums3:
            for j in nums4:
                if -(i+j) in hashmap:
                    count+=hashmap[-(i+j)]
                else:
                    hashmap[-(i+j)]=0
        return count


        
        
```
