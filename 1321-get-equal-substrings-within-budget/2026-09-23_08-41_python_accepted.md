# 1321. Get Equal Substrings Within Budget
  
<br>**Problem:** https://leetcode.com/problems/get-equal-substrings-within-budget/<br>

**Difficulty:** Medium<br>
**Topics:** String, Binary Search, Sliding Window, Prefix Sum<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-23 08:41 local time

**Runtime:** 35 ms (beats 89.36170000000003%)
**Memory:** 15.6 MB (beats 15.425500000000005%)


<!-- leetgit:submissionId=2150357832 codeHash=d980b55c68b5dfd150f8b503a75bd32ed31455b45a0b3e3a13790c2f557105bb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def equalSubstring(self, s, t, maxcost):
        count=0
        i=0
        max1=0
        l=0
        for i in range(len(s)):
            maxcost-=abs(ord(s[i])-ord(t[i]))
            while maxcost<0:
                 #if maxcost ==0 return i+1 else i
                maxcost+=abs(ord(s[l])-ord(t[l]))
                l+=1
            max1=max(i-l+1,max1)
                
        return max1
        
        
```
