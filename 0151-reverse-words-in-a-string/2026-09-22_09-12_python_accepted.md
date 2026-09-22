# 151. Reverse Words in a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-words-in-a-string/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-22 09:12 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.6 MB (beats 38.4814%)


<!-- leetgit:submissionId=2149258451 codeHash=8c75c4ddce94868f2f927fceb927dad8145f7ff79a14f96fc0d659f2a7fd4b75 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseWords(self, s):
        s = s.split()
        s.reverse()
        return " ".join(s)
       
```
