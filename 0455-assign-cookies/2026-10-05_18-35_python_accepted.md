# 455. Assign Cookies
  
<br>**Problem:** https://leetcode.com/problems/assign-cookies/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers, Greedy, Sorting, Quicksort<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 18:35 local time

**Runtime:** 39 ms (beats 15.832899999999949%)
**Memory:** 14.1 MB (beats 51.870799999999996%)


<!-- leetgit:submissionId=2163133245 codeHash=095278ec1fe37e3e276955fac1dcc255844eb7b341e0a837ca4ea5375060cf2d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findContentChildren(self, g, s):
        count=0
        i=0
        j=0
        g.sort()
        s.sort()
        while i<len(s) and j<len(g):
            if s[i]>=g[j]:
                count+=1
                i+=1
                j+=1
            else:
                i+=1
        return count

        
        
```
