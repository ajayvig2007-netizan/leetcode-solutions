# 1737. Maximum Nesting Depth of the Parentheses
  
<br>**Problem:** https://leetcode.com/problems/maximum-nesting-depth-of-the-parentheses/<br>

**Difficulty:** Easy<br>
**Topics:** String, Stack, Bracket Sequences<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 08:03 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.5 MB (beats 0.6641000000000048%)


<!-- leetgit:submissionId=2155474436 codeHash=4ee1792863f6977c6fe72d8e08ccad927096d69fbe2c6c09e67f50705979dbdf notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution:
    def maxDepth(self, s):
        depth = 0
        r = 0
        for c in s:
            if c == ')':
                depth -= 1
                continue
            if c != '(':
                continue
            depth += 1
            if depth > r:
                r = depth
        return r
```
