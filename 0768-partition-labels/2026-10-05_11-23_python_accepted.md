# 768. Partition Labels
  
<br>**Problem:** https://leetcode.com/problems/partition-labels/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, Two Pointers, String, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 11:23 local time

**Runtime:** 4 ms (beats 80.14079999999998%)
**Memory:** 12.6 MB (beats 1.4085000000000036%)


<!-- leetgit:submissionId=2162780286 codeHash=7460da8d8bde4d34f26323352b6de3835f13af318004061fac8ecc7ad85956c6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def partitionLabels(self,s):
        last={}
        for i in range(len(s)):
            last[s[i]]=i
        ans=[]
        start=0
        end=0
        for i in range(len(s)):
            end=max(end,last[s[i]])
            if i==end:
                ans.append(i-start+1)
                start=i+1
        return ans
```
