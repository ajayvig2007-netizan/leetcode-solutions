# 239. Sliding Window Maximum
  
<br>**Problem:** https://leetcode.com/problems/sliding-window-maximum/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Queue, Sliding Window, Heap (Priority Queue), Monotonic Queue, Range Minimum/Maximum Query<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 11:40 local time

**Runtime:** 295 ms (beats 27.47249999999994%)
**Memory:** 28.9 MB (beats 55.98529999999998%)


<!-- leetgit:submissionId=2166016771 codeHash=6440073aad95198935bd767f7ac0e74ab8c020b1e3ffa48bc1aef94b43f240dc notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
from collections import deque
class Solution(object):
    def maxSlidingWindow(self,nums,k):
        ans=[]
        q=deque()
        for i in range(len(nums)):
            while q and q[0]<=i-k:
                q.popleft()
            while q and nums[q[-1]]<=nums[i]:
                q.pop()
            q.append(i)
            if i>=k-1:
                ans.append(nums[q[0]])
        return ans
```
