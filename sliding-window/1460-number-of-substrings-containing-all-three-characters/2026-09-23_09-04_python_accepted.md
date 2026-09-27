# 1460. Number of Substrings Containing All Three Characters
  
<br>**Problem:** https://leetcode.com/problems/number-of-substrings-containing-all-three-characters/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-23 09:04 local time

**Runtime:** 416 ms (beats 5.0863999999998235%)
**Memory:** 12.6 MB (beats 79.452%)


<!-- leetgit:submissionId=2150373013 codeHash=126b17e8630080804d1ff3ab993ec4b53240c80a5e2d4564f09f0aff45bd64bb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def numberOfSubstrings(self, s):
        seen = {'a':1, 'b':1, 'c':1}
        count = 0
        hashmap = {}
        l = 0
        r = 0

        while r < len(s):
            hashmap[s[r]] = hashmap.get(s[r], 0) + 1

            while all(x in hashmap for x in seen):
                count += len(s) - r

                hashmap[s[l]] -= 1
                if hashmap[s[l]] == 0:
                    del hashmap[s[l]]
                l += 1

            r += 1

        return count
```
