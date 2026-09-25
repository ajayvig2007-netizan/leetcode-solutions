# 1188. Brace Expansion II
  
<br>**Problem:** https://leetcode.com/problems/brace-expansion-ii/<br>

**Difficulty:** Hard<br>
**Topics:** Hash Table, String, Backtracking, Stack, Breadth-First Search, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-25 09:03 local time

**Runtime:** 38 ms (beats 13.33319999999999%)
**Memory:** 12.7 MB (beats 26.66680000000001%)


<!-- leetgit:submissionId=2152563453 codeHash=7cda67b0949afe84afd4d3a2b003458bdaaa518164fe652c4a986b489302e044 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution:
    def braceExpansionII(self, expression):
        ans = set()
        def dfs(s):
            r = s.find('}')
            if r == -1:
                ans.add(s)
                return

            l = s.rfind('{', 0, r)
            left = s[:l]
            right = s[r + 1:]
            inside = s[l + 1:r]

            for part in inside.split(','):
                dfs(left + part + right)

        dfs(expression)
        return sorted(ans)
```
