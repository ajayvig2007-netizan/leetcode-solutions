# 516. Longest Palindromic Subsequence
  
<br>**Problem:** https://leetcode.com/problems/longest-palindromic-subsequence/<br>

**Difficulty:** Medium<br>
**Topics:** String, Dynamic Programming<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 11:31 local time

**Runtime:** 1085 ms (beats 59.81329999999989%)
**Memory:** 27 MB (beats 78.20209999999997%)


<!-- leetgit:submissionId=2152679694 codeHash=1d82f154b839a7ccbf9d6625500d72805d021f595d4bf2b1f1802e708b9636f4 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPalindromeSubseq(self, s):
        n = len(s)
        dp = [[0] * n for _ in range(n)]

        for i in range(n):
            dp[i][i] = 1

        for length in range(2, n + 1):
            for i in range(n - length + 1):
                j = i + length - 1

                if s[i] == s[j]:
                    dp[i][j] = dp[i + 1][j - 1] + 2
                else:
                    dp[i][j] = max(dp[i + 1][j], dp[i][j - 1])

        return dp[0][n - 1]
```
