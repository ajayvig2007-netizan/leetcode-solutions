# 169. Majority Element
  
<br>**Problem:** https://leetcode.com/problems/majority-element/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Divide and Conquer, Sorting, Counting, Boyer–Moore Majority Vote Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-16 08:36 local time

**Runtime:** 44 ms (beats 5.224700000000004%)
**Memory:** 13.7 MB (beats 18.230199999999986%)


<!-- leetgit:submissionId=2143189974 codeHash=f735d335debe45697536fcc1b60cec6ea62bbc0d6ff89de95abbfe1aa89cfd5a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def majorityElement(self, nums):
        from collections import Counter
        freq=Counter(nums)
        for i in nums:
            if freq[i]>len(nums)//2:
                return i
        
```
