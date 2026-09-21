# 49. Group Anagrams
  
<br>**Problem:** https://leetcode.com/problems/group-anagrams/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-21 09:08 local time

**Runtime:** 18 ms (beats 80.68509999999999%)
**Memory:** 16.1 MB (beats 72.43679999999999%)


<!-- leetgit:submissionId=2148214161 codeHash=ad14a42968e71dd9157c25c0c3b0d55a12c4807b4acfeb80cc7b080f703912e8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def groupAnagrams(self, strs):
        hashmap = {}

        for word in strs:
            key = ''.join(sorted(word))

            if key not in hashmap:
                hashmap[key] = []

            hashmap[key].append(word)

        return list(hashmap.values())
```
