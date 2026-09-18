# 1370. Count Number of Nice Subarrays
  
<br>**Problem:** https://leetcode.com/problems/count-number-of-nice-subarrays/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Math, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 10:01 local time

**Runtime:** 94 ms (beats 89.05640000000005%)
**Memory:** 17.1 MB (beats 27.42129999999999%)


<!-- leetgit:submissionId=2145344240 codeHash=dc69ac0adfa6dfc89ba5fd24f75a9854917119dabbf953362eb7ca3275461b21 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def numberOfSubarrays(self, nums, k):
        count={0: 1}
        odd=0
        ans=0
        for x in nums:
            if x%2==1:
                odd+=1
            if odd-k in count:
                ans+=count[odd-k]
            if odd in count:
                count[odd]+=1
            else:
                count[odd]=1
        return ans
```
