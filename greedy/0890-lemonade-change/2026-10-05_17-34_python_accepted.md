# 890. Lemonade Change
  
<br>**Problem:** https://leetcode.com/problems/lemonade-change/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Greedy<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-05 17:34 local time

**Runtime:** 9 ms (beats 21.523600000000005%)
**Memory:** 15.3 MB (beats 45.1182%)


<!-- leetgit:submissionId=2163086362 codeHash=db3f3c9aa9606a63395732394a6cf96f694a229333f1d178446995adbb3320ef notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def lemonadeChange(self, bills):
        five=0
        ten=0
        for i in bills:
            if i==5:
                five+=1
            elif i==10:
                ten+=1
                if five<1:
                    return False
                else:
                    five-=1
            elif i==20:
                if five>=1 and ten>=1:
                    five-=1
                    ten-=1
                elif five>=3:
                    five-=3
                else:
                    return False
        return True




        
```
