# 76. Minimum Window Substring
  
<br>**Problem:** https://leetcode.com/problems/minimum-window-substring/<br>

**Difficulty:** Hard<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-14 00:04 local time

**Runtime:** 215 ms (beats 17.664300000000004%)
**Memory:** 15.7 MB (beats 24.11699999999999%)


<!-- leetgit:submissionId=2140924029 codeHash=85eb6d18cd7a746255f02cd13654a9678db39ddd5c14036511dba388efa81bc3 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minWindow(self, s, t):
        freq={}
        window={}
        min1=float('inf')
        ans=""
        count=0
        l=0
        for x in t:
            freq[x]=freq.get(x,0)+1
        for r in range(len(s)):
            window[s[r]]=window.get(s[r],0)+1
            if s[r] in t and window[s[r]]<=freq[s[r]]:
                count+=1
            while count==len(t):
                if r-l+1<min1:
                    ans=s[l:r+1]
                    min1=r-l+1
                if s[l] in freq:
                    window[s[l]]-=1
                    if freq[s[l]]>window[s[l]]:
                        count-=1
                l+=1
                    
               
        return ans


        
```
