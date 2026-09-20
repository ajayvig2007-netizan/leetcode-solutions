# 3811. Reverse Degree of a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-degree-of-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** String, Simulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 08:40 local time

**Runtime:** 15 ms (beats 24.72330000000001%)
**Memory:** 12.4 MB (beats 22.878300000000003%)


<!-- leetgit:submissionId=2147205850 codeHash=acdcf6c62f8ad4296e2bf92f292e878d72fe291b36e1dcb82831ed367db12a25 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseDegree(self, s):
        a = 0
        for i in range(len(s)):
            value = ord('z') - ord(s[i]) + 1
            a += value * (i + 1)

        return a
```
