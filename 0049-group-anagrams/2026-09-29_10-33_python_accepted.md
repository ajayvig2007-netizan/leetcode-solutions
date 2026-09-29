# 49. Group Anagrams
  
<br>**Problem:** https://leetcode.com/problems/group-anagrams/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 10:33 local time

**Runtime:** 23 ms (beats 47.02439999999997%)
**Memory:** 16.1 MB (beats 57.72709999999999%)


<!-- leetgit:submissionId=2156676489 codeHash=c0755892aa93d278c308c0a47c74e774083ef52177e0ada6203dce856751b88f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def groupAnagrams(self, strs):
        ans = {}

        for i in strs:
            a = ''.join(sorted(i))

            if a not in ans:
                ans[a] = []

            ans[a].append(i)

        return list(ans.values())
```
