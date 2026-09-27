# 2713. Find the Divisibility Array of a String
  
<br>**Problem:** https://leetcode.com/problems/find-the-divisibility-array-of-a-string/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-18 11:00 local time

**Runtime:** 203 ms (beats 100%)
**Memory:** 18.1 MB (beats 51.8519%)


<!-- leetgit:submissionId=2145396609 codeHash=70c47facfbaaff44fa754b259234628a69e8f2f5aad6b7674e6e678ecc72fc3d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def divisibilityArray(self, word, m):
        ans = []
        rem = 0

        for digit in word:
            rem = rem * 10 + int(digit)

            if rem % m == 0:
                ans.append(1)
            else:
                ans.append(0)

            rem = rem % m

        return ans
```
