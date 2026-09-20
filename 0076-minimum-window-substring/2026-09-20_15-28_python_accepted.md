# 76. Minimum Window Substring
  
<br>**Problem:** https://leetcode.com/problems/minimum-window-substring/<br>

**Difficulty:** Hard<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 15:28 local time

**Runtime:** 220 ms (beats 17.11959999999998%)
**Memory:** 12.7 MB (beats 71.2291%)


<!-- leetgit:submissionId=2147556423 codeHash=757450e690b9abef1f249e7198352528353c2da8291ac2f7010f0cfbb680b890 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minWindow(self, s, t):
        r=0
        l=0
        min1=float('inf')
        ans=''
        hashmap1={}
        count=0
        hashmap2={}
        for x in t:
            hashmap1[x]=hashmap1.get(x,0)+1
        while r<len(s):
            if s[r] in hashmap1:
                hashmap2[s[r]]=hashmap2.get(s[r],0)+1
                if hashmap1[s[r]]>=hashmap2[s[r]]:
                    count+=1
            while count==len(t):
                while s[l] not in hashmap1:
                    l+=1
                if min1>=r-l+1:
                    min1=r-l+1
                    ans=s[l:r+1]
                if s[l] in hashmap2:
                    hashmap2[s[l]]-=1
                    if hashmap2[s[l]]<hashmap1[s[l]]:
                        count-=1
                        #l+=1
                l+=1
            r+=1
        
        return ans
        
```
