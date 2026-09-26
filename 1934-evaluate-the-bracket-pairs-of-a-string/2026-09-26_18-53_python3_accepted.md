# 1934. Evaluate the Bracket Pairs of a String
  
<br>**Problem:** https://leetcode.com/problems/evaluate-the-bracket-pairs-of-a-string/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, String<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-26 18:53 local time

**Runtime:** 36 ms (beats 92.21180000000001%)
**Memory:** 51.4 MB (beats 81.6199%)


<!-- leetgit:submissionId=2153890273 codeHash=6b048abc8fdbb15d5c8956bc1ccb9f384de46d71d6b083500db48877e660ac61 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def evaluate(self, s: str, knowledge: List[List[str]]) -> str:
        d = dict(knowledge)
        return re.sub(r"\((\w+)\)", lambda m: d.get(m[1], "?"), s)
```
