# 49. Group Anagrams
  
<br>**Problem:** https://leetcode.com/problems/group-anagrams/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-27 22:01 local time

**Runtime:** 35 ms (beats 13.722699999999994%)
**Memory:** 18.3 MB (beats 5.956099999999994%)


<!-- leetgit:submissionId=2155154434 codeHash=0a45fabcbe91a5b1eeb35e15e16ba162177c981be1fc30d3337df6eaf25db228 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def groupAnagrams(self, strs):
        res={}
        for s in strs:
            count=[0]*26
            for ch in s:
                count[ord(ch)-ord('a')]+=1
            if tuple(count) not in res:
                res[tuple(count)]=[]
            res[tuple(count)].append(s)
        return list(res.values())
        
```
