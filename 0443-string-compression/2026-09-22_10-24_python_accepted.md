# 443. String Compression
  
<br>**Problem:** https://leetcode.com/problems/string-compression/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 10:24 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.7 MB (beats 18.124399999999987%)


<!-- leetgit:submissionId=2149319492 codeHash=6e111399053efade6c542fc5c59ca8b6a134101a9ee5f2a65bfb264c529959be notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def compress(self, chars):
        ans = []
        i = 0
        while i < len(chars):
            count = 1
            while i + count < len(chars) and chars[i] == chars[i + count]:
                count += 1
            ans.append(chars[i])
            if count > 1:
                ans.extend(str(count))
            i += count
        chars[:] = ans
        return len(ans)
```
