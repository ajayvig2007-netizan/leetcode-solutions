# 76. Minimum Window Substring
  
<br>**Problem:** https://leetcode.com/problems/minimum-window-substring/<br>

**Difficulty:** Hard<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 13:42 local time

**Runtime:** 210 ms (beats 18.2757%)
**Memory:** 15.8 MB (beats 24.11699999999999%)


<!-- leetgit:submissionId=2140407353 codeHash=187cb398526fddee4b3ae9f306760052bfc310cd7970ec0ad29a5fa00deb6311 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def minWindow(self, s, t):
        freq={}
        for r in t:
            freq[r]=freq.get(r,0)+1
        l=0
        window={}
        count=0
        ans=""
        minvalue=float('inf')
        for r in range(len(s)):
            window[s[r]]=window.get(s[r],0)+1
            if s[r] in freq and window[s[r]]<=freq[s[r]]:
                count+=1
            while count==len(t):
                if r-l+1<=minvalue:
                    minvalue=r-l+1
                    ans=s[l:r+1]
                window[s[l]]-=1
                if s[l] in  freq and window[s[l]]<freq[s[l]]:
                    count-=1
                l+=1
        return ans


        
```
