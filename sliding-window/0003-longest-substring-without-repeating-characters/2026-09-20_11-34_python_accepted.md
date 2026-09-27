# 3. Longest Substring Without Repeating Characters
  
<br>**Problem:** https://leetcode.com/problems/longest-substring-without-repeating-characters/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 11:34 local time

**Runtime:** 559 ms (beats 9.371099999999693%)
**Memory:** 16.8 MB (beats 10.965199999999928%)


<!-- leetgit:submissionId=2147373843 codeHash=37eee406f395bb89afecbcf657e11a8a5c8fc2100eeb67340156d6a88c829e27 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def lengthOfLongestSubstring(self, s):
        if len(s)==1:
            return 1
        hashmap1={}
        max1=0
        r=0
        l=0
        for r in range(len(s)):
            hashmap1[s[r]] =hashmap1.get(s[r],0)+1
            while hashmap1[s[r]]>1:
                
                hashmap1[s[l]]-=1
                if hashmap1[s[r]]==0:
                    del hashmap1[s[l]]
                l+=1
            max1=max(r-l+1,max1)

        return max1

        
```
