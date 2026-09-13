# 1987. Substrings of Size Three with Distinct Characters
  
<br>**Problem:** https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Sliding Window, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 10:49 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 90.7166%)


<!-- leetgit:submissionId=2140272806 codeHash=8d16d9e3a2785ea20f5e09d8128d59953a1fa01555a4c31a3efafd1a774daa4a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def countGoodSubstrings(self, s):
        list1=list(s)
        count=0
        l=0
        for r in range(len(list1)):
            if r-l+1==3:
                if(len(set(list1[l:r+1])))==3:
                    count+=1
                l+=1
        return count

        
        
```
