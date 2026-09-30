# 1208. Maximum Nesting Depth of Two Valid Parentheses Strings
  
<br>**Problem:** https://leetcode.com/problems/maximum-nesting-depth-of-two-valid-parentheses-strings/<br>

**Difficulty:** Medium<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 11:39 local time

**Runtime:** 4 ms (beats 18.981499999999993%)
**Memory:** 19.5 MB (beats 7.407400000000006%)


<!-- leetgit:submissionId=2157850491 codeHash=8cba0c67df01b0d9c6d4ef66c116af273cae7907b13192b95b475f3671dd460e notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxDepthAfterSplit(self, seq: str) -> list[int]:
        res = []

        for i in range(len(seq)):
            res.append((i ^ ord(seq[i])) & 1)

        return res
```
