# 892. Shortest Subarray with Sum at Least K
  
<br>**Problem:** https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Binary Search, Queue, Sliding Window, Heap (Priority Queue), Prefix Sum, Monotonic Queue<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-06 14:24 local time

**Runtime:** 174 ms (beats 51.445499999999996%)
**Memory:** 17.8 MB (beats 17.34100000000001%)


<!-- leetgit:submissionId=2164039177 codeHash=95e08ceb047b9769693e76fdef9b96eee93cf1acab6e777ef632ff899eefd683 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
from collections import deque
class Solution(object):
    def shortestSubarray(self, nums, k):
        q = deque()
        q.append((-1, 0))
        ans = float('inf')
        s = 0
        for i in range(len(nums)):
            s += nums[i]
            while q and s - q[0][1] >= k:
                ans = min(ans, i - q[0][0])
                q.popleft()
            while q and q[-1][1] >= s:
                q.pop()
            q.append((i, s))
        return ans if ans != float('inf') else -1
```
