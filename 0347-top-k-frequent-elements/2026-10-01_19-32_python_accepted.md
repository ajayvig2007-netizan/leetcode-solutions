# 347. Top K Frequent Elements
  
<br>**Problem:** https://leetcode.com/problems/top-k-frequent-elements/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Divide and Conquer, Sorting, Heap (Priority Queue), Bucket Sort, Counting, Quickselect<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-01 19:32 local time

**Runtime:** 67 ms (beats 7.102900000000007%)
**Memory:** 14.1 MB (beats 70.77350000000001%)


<!-- leetgit:submissionId=2159259604 codeHash=dab93c7ee56e3caa62695ddc3e94da20fb7d2008a0722f6600a18f3a7763527d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def topKFrequent(self, nums, k):
        hashmap={}
        ans=[]
        for i in nums:
            hashmap[i]=hashmap.get(i,0)+1
        while k > 0:
            max1 = 0
            value = 0

            for i in hashmap:
                if hashmap[i] > max1:
                    max1 = hashmap[i]
                    value = i

            ans.append(value)
            del hashmap[value]
            k -= 1
        return ans

        
```
