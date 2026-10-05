# 66. Plus One
  
<br>**Problem:** https://leetcode.com/problems/plus-one/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Math<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 12:35 local time

**Runtime:** 3 ms (beats 6.5045000000000055%)
**Memory:** 12.3 MB (beats 90.0779%)


<!-- leetgit:submissionId=2156802419 codeHash=3b0314108170c39783ba47054e783086ce21afe4e267067afee8ce22469287ec notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def plusOne(self, digits):
        a = ''.join(map(str, digits))
        b = int(a) + 1
        return list(map(int, str(b)))
```
