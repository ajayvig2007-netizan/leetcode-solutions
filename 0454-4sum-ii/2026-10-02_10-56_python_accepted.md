# 454. 4Sum II
  
<br>**Problem:** https://leetcode.com/problems/4sum-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-02 10:56 local time

**Runtime:** 465 ms (beats 49.35449999999982%)
**Memory:** 12.8 MB (beats 22.844899999999996%)


<!-- leetgit:submissionId=2159808140 codeHash=f682aa788c519e3dadae91be9a9456596155b05e67834efea253914b970911b4 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
                    # else:
                    #     hashmap[-(i+j)]=0
        return count


        
        
```
