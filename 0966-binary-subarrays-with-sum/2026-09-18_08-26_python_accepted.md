# 966. Binary Subarrays With Sum
  
<br>**Problem:** https://leetcode.com/problems/binary-subarrays-with-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 08:26 local time

**Runtime:** 32 ms (beats 80.32059999999997%)
**Memory:** 14.9 MB (beats 41.53339999999996%)


<!-- leetgit:submissionId=2145281953 codeHash=80bff4ed8a88157fdb1d228a0f41c1230b88aaa316b7363b20b3e517fab607c9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def numSubarraysWithSum(self, nums, goal):
        hashmap = {0: 1}
        sum1 = 0
        count = 0

        for num in nums:
            sum1 += num

            if sum1 - goal in hashmap:
                count += hashmap[sum1 - goal]

            hashmap[sum1] = hashmap.get(sum1, 0) + 1

        return count
```
