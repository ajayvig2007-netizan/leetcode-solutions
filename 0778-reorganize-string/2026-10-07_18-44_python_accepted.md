# 778. Reorganize String
  
<br>**Problem:** https://leetcode.com/problems/reorganize-string/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Greedy, Sorting, Heap (Priority Queue), Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 18:44 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 62.2465%)


<!-- leetgit:submissionId=2165304567 codeHash=1002e94e33d504adeb233bf53e12d4149aa5289ecd3d429860f760ad4867d507 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reorganizeString(self, s):
        hashmap={}
        max1=0
        ans=['']*len(s)
        maxchar=''
        c=0
        i=0

        for r in s:
            hashmap[r]=hashmap.get(r,0)+1
            if max1<hashmap[r]:
                max1=hashmap[r]
                maxchar=r

        if max1>(len(s)+1)//2:
            return ""

        while i<max1:
            ans[c]=maxchar
            hashmap[maxchar]-=1
            c+=2
            i+=1

        for r in hashmap:
            while hashmap[r]>0:
                if c>=len(s):
                    c=1
                ans[c]=r
                c+=2
                hashmap[r]-=1

        return ''.join(ans)
```
