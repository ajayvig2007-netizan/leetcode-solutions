# 443. String Compression
  
<br>**Problem:** https://leetcode.com/problems/string-compression/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 10:16 local time

**Runtime:** 4 ms (beats 37.33100000000002%)
**Memory:** 12.4 MB (beats 54.418399999999984%)


<!-- leetgit:submissionId=2149312523 codeHash=1e33d6524576d9ec5111f71c9ccff2bbefb927f6f70c44e9ef5e8375362893d0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
from itertools import groupby

class Solution(object):
    def compress(self, chars):
        ans = []

        for ch, group in groupby(chars):
            count = len(list(group))
            ans.append(ch)

            if count > 1:
                ans.extend(str(count))

        chars[:] = ans
        return len(ans)
```
