# 49. Group Anagrams
  
<br>**Problem:** https://leetcode.com/problems/group-anagrams/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 21:40 local time

**Runtime:** 27 ms (beats 29.142499999999995%)
**Memory:** 18.4 MB (beats 5.956099999999994%)


<!-- leetgit:submissionId=2155134224 codeHash=6aec1272dd55fbafdde59786828397a741bea25ba996631999060b9440e32845 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def groupAnagrams(self, strs):
        res = {}

        for x in strs:
            count = [0] * 26

            for ch in x:
                count[ord(ch) - ord('a')] += 1

            key = tuple(count)

            if key not in res:
                res[key] = []

            res[key].append(x)

        return list(res.values())
```
