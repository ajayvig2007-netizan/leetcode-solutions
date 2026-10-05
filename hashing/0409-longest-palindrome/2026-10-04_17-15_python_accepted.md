# 409. Longest Palindrome
  
<br>**Problem:** https://leetcode.com/problems/longest-palindrome/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-04 17:15 local time

**Runtime:** 4 ms (beats 43.7579%)
**Memory:** 12.3 MB (beats 63.2484%)


<!-- leetgit:submissionId=2162050622 codeHash=8e2078de294bb56a6db023c2d459a033f379d8480ec66effa98a33e57431095a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def longestPalindrome(self, s):
        hashmap={}
        count=0
        for i in s:
            hashmap[i]=hashmap.get(i,0)+1
        for i in set(s):
            if hashmap[i]%2==0:
                count+=hashmap[i]
            else:
                count+=hashmap[i]-1
        if hashmap[i]==len(s):
            return len(s)
        if count<len(s):
            count+=1
        return count



        
```
