# 77. Combinations
  
<br>**Problem:** https://leetcode.com/problems/combinations/<br>

**Difficulty:** Medium<br>
**Topics:** Backtracking<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-26 16:00 local time

**Runtime:** 271 ms (beats 21.667300000000058%)
**Memory:** 131.2 MB (beats 50.566800000000015%)


<!-- leetgit:submissionId=2153771363 codeHash=2d0994a6461536848ba98c61a0c8fdf8bcff3b3f4e753a4c9eec40781e69a066 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def combine(self, n, k):
        ans = []
        part = []
        list1 = list(range(1, n + 1))
        def dfs(i):
            if len(part) == k:
                ans.append(part[:])
                return
            for j in range(i, len(list1)):
                part.append(list1[j])
                dfs(j + 1)
                part.pop()

        dfs(0)
        return ans
```
