# 3. Longest Substring Without Repeating Characters
  
<br>**Problem:** https://leetcode.com/problems/longest-substring-without-repeating-characters/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-13 12:07 local time

**Runtime:** 371 ms (beats 47.97050000000009%)
**Memory:** 16.8 MB (beats 25.33550000000004%)


<!-- leetgit:submissionId=2140334920 codeHash=2de40dd0559b0cd8ec7a59d94f1a95acb9f84a3ab99c7274a00ea29524b7d2fa notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def lengthOfLongestSubstring(self, s):
        l=set()
        la=0
        max1=0
        for r in range(len(s)):
            while s[r] in l:
                l.remove(s[la])
                la+=1
            else:
                l.add(s[r])
                max1=max(r-la+1,max1)
        return max1



        
```
