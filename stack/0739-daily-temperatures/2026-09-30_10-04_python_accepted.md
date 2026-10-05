# 739. Daily Temperatures
  
<br>**Problem:** https://leetcode.com/problems/daily-temperatures/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Stack, Monotonic Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 10:04 local time

**Runtime:** 165 ms (beats 52.673700000000004%)
**Memory:** 27 MB (beats 40.641399999999955%)


<!-- leetgit:submissionId=2157763440 codeHash=c4114ae3361d4b6183eab969eab7d904b075a44756a1b12041d276fa99de27cb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def dailyTemperatures(self, temperatures):
        ans=[0]*len(temperatures)
        stack=[]

        for i in range(len(temperatures)):
            while stack and temperatures[i]>temperatures[stack[-1]]:
                j=stack.pop()
                ans[j]=i-j

            stack.append(i)

        return ans
```
