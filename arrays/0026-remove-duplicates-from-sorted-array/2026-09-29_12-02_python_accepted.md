# 26. Remove Duplicates from Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/remove-duplicates-from-sorted-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 12:02 local time

**Runtime:** 6 ms (beats 22.50629999999999%)
**Memory:** 13.2 MB (beats 93.0217%)


<!-- leetgit:submissionId=2156770271 codeHash=af4a53ce8d658d7016f902992948170f1d7ac77936269c239d11971b72ad8a41 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def removeDuplicates(self, nums):
        nums[:]=sorted(list(set(nums)))
        
```
