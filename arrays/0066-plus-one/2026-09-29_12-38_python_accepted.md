# 66. Plus One
  
<br>**Problem:** https://leetcode.com/problems/plus-one/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Math<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 12:38 local time

**Runtime:** 3 ms (beats 6.5045000000000055%)
**Memory:** 12.1 MB (beats 99.9606%)


<!-- leetgit:submissionId=2156804621 codeHash=7ef1323843b726bb887fc4387cf80962e4a59607ad2bbbb08dc234a63d887522 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def plusOne(self, digits):
        a = ''.join(map(str, digits))
        b = int(a) + 1
        return [int(x) for x in str(b)]
```
