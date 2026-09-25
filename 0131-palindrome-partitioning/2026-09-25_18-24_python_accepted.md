# 131. Palindrome Partitioning
  
<br>**Problem:** https://leetcode.com/problems/palindrome-partitioning/<br>

**Difficulty:** Medium<br>
**Topics:** String, Dynamic Programming, Backtracking<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 18:24 local time

**Runtime:** 90 ms (beats 14.531999999999949%)
**Memory:** 47.9 MB (beats 62.19319999999996%)


<!-- leetgit:submissionId=2152982564 codeHash=32381d76ea855bb7d591c47a314945034c5ddb072beb3c1a26dd1e52fd790d96 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def partition(self, s):
        part = []
        ans = []

        def dfs(i):
            if i >= len(s):
                ans.append(part[:])
                return

            for j in range(i, len(s)):
                if self.ispali(s, i, j):
                    part.append(s[i:j+1])
                    dfs(j + 1)
                    part.pop()

        dfs(0)
        return ans

    def ispali(self, s, i, j):
        return s[i:j+1] == s[i:j+1][::-1]
```
