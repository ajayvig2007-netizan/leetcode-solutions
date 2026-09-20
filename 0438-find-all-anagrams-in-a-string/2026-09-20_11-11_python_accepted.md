# 438. Find All Anagrams in a String
  
<br>**Problem:** https://leetcode.com/problems/find-all-anagrams-in-a-string/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 11:11 local time

**Runtime:** 51 ms (beats 55.197699999999955%)
**Memory:** 13.3 MB (beats 85.3587%)


<!-- leetgit:submissionId=2147354034 codeHash=e7f9fbbd7aa07bc1e0fd959b57b7f25ced24acfab776214d8b557765b23c79f3 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def findAnagrams(self, s, p):
        hashmap2={}
        hashmap1={}
        ans=[]
        for x in p:
            hashmap2[x]=hashmap2.get(x,0)+1
        l=0
        r=0
        while r<len(s):
            hashmap1[s[r]]=hashmap1.get(s[r],0)+1
            if r-l+1==len(p):
                if hashmap1==hashmap2:
                    ans.append(l)
                hashmap1[s[l]]-=1
                if hashmap1[s[l]]==0:
                    del hashmap1[s[l]]
                l+=1
            r+=1
        return ans

        
        
```
