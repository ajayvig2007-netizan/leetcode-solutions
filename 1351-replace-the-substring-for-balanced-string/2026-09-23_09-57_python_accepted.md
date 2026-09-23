# 1351. Replace the Substring for Balanced String
  
<br>**Problem:** https://leetcode.com/problems/replace-the-substring-for-balanced-string/<br>

**Difficulty:** Medium<br>
**Topics:** String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-23 09:57 local time

**Runtime:** 174 ms (beats 72.22200000000001%)
**Memory:** 16.4 MB (beats 37.03690000000002%)


<!-- leetgit:submissionId=2150423291 codeHash=28020922ecc125c4d2e5e0fbb01105ae18f2daf8e1104532f1078c8c9ccbaf13 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def balancedString(self, s):
        n=len(s)
        k=n//4
        count={'Q':0,'W':0,'E':0,'R':0}
        for ch in s:
            count[ch]+=1
        if count['Q']==k and count['W']==k and count['E']==k and count['R']==k:
            return 0
        l=0
        ans=n
        for r in range(n):
            count[s[r]]-=1
            while l<=r and max(count.values())<=k:
                ans = min(ans,r-l+1)
                count[s[l]]+=1
                l+=1
        return ans
```
