# 1987. Substrings of Size Three with Distinct Characters
  
<br>**Problem:** https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Sliding Window, Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 10:47 local time

**Runtime:** 1 ms (beats 69.3811%)
**Memory:** 12.4 MB (beats 56.5146%)


<!-- leetgit:submissionId=2140271474 codeHash=fa512458246641799323877ba189e5b04dbea87e48baa19f77edda2a5c3701cb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def countGoodSubstrings(self, s):
        list1=list(s)
        l=0
        r=0
        count=0
        sum1=1
        for r in range(len(list1)):
            if r-l+1==3:
                if(len(set(list1[l:r+1])))==3:
                    count+=1
                l+=1
        return count

        
        
```
