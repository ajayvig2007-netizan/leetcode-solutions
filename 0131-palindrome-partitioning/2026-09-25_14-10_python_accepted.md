# 131. Palindrome Partitioning
  
<br>**Problem:** https://leetcode.com/problems/palindrome-partitioning/<br>

**Difficulty:** Medium<br>
**Topics:** String, Dynamic Programming, Backtracking<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 14:10 local time

**Runtime:** 73 ms (beats 70.76799999999996%)
**Memory:** 47.8 MB (beats 78.67429999999996%)


<!-- leetgit:submissionId=2152800092 codeHash=b5c181d2871f82117d54ae2d1fed4c37731fbcf12c940f85251d4342c56fc833 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def partition(self, s):
        ans = []

        def backtrack(start, path):
            if start == len(s):
                ans.append(path[:])
                return

            for end in range(start, len(s)):
                part = s[start:end+1]

                if part == part[::-1]:
                    path.append(part)
                    backtrack(end + 1, path)
                    path.pop()

        backtrack(0, [])
        return ans
```
