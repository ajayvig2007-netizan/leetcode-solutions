# 739. Daily Temperatures
  
<br>**Problem:** https://leetcode.com/problems/daily-temperatures/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Stack, Monotonic Stack<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-30 10:35 local time

**Runtime:** 173 ms (beats 37.47130000000001%)
**Memory:** 27.1 MB (beats 20.263199999999955%)


<!-- leetgit:submissionId=2157791332 codeHash=d2cc2016657a38a3a9157f8a9b9b75861e8d24bf5eee639dbb4f51dd4fcb0ee5 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
