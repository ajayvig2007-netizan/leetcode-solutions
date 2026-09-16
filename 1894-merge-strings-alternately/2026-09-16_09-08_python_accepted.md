# 1894. Merge Strings Alternately
  
<br>**Problem:** https://leetcode.com/problems/merge-strings-alternately/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 09:08 local time

**Runtime:** 20 ms (beats 28.643899999999995%)
**Memory:** 12.5 MB (beats 21.26140000000001%)


<!-- leetgit:submissionId=2143209306 codeHash=02cb56bf652ce66b7f4a7c0e23600d7b50585ea9ce88c8ceabb5b8b90f098d16 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def mergeAlternately(self, word1, word2):
        ans=''
        for i in range(min(len(word1),len(word2))):
                ans+=word1[i]+word2[i]
        ans+=word1[i+1:] if len(word1)>len(word2) else word2[i+1:]
        return ans
```
