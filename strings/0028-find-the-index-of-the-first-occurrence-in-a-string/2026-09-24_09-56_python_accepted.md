# 28. Find the Index of the First Occurrence in a String
  
<br>**Problem:** https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String, String Matching, Z Algorithm, Knuth–Morris–Pratt Algorithm, Boyer–Moore String-Search Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-24 09:56 local time

**Runtime:** 1 ms (beats 24.012200000000007%)
**Memory:** 12.5 MB (beats 20.38850000000001%)


<!-- leetgit:submissionId=2151553708 codeHash=11c7e19e80ed8362c082ddc0e4e2ea7a8cd63313bf871b24eb7d0d81792cdc4d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def strStr(self, haystack, needle):
        for i in range(len(haystack) - len(needle) + 1):
            if haystack[i:i+len(needle)] == needle:
                return i
        return -1
```
