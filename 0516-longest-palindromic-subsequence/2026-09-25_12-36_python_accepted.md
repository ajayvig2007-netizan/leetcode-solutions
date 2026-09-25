# 516. Longest Palindromic Subsequence
  
<br>**Problem:** https://leetcode.com/problems/longest-palindromic-subsequence/<br>

**Difficulty:** Medium<br>
**Topics:** String, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 12:36 local time

**Runtime:** 1544 ms (beats 36.92789999999965%)
**Memory:** 106.6 MB (beats 5.587699999999927%)


<!-- leetgit:submissionId=2152739293 codeHash=19442fc1a89a6aa63fa0e320ccd04752558d30eefdb7a7e6156af1db304c7165 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPalindromeSubseq(self, s):
        dp = {}

        def solve(i, j):
            if i > j:
                return 0

            if i == j:
                return 1

            if (i, j) in dp:
                return dp[(i, j)]

            if s[i] == s[j]:
                dp[(i, j)] = 2 + solve(i + 1, j - 1)
            else:
                dp[(i, j)] = max(
                    solve(i + 1, j),
                    solve(i, j - 1)
                )

            return dp[(i, j)]

        return solve(0, len(s) - 1)
```
