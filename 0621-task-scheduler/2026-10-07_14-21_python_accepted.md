# 621. Task Scheduler
  
<br>**Problem:** https://leetcode.com/problems/task-scheduler/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Greedy, Sorting, Heap (Priority Queue), Counting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-07 14:21 local time

**Runtime:** 40 ms (beats 72.07350000000001%)
**Memory:** 13.6 MB (beats 66.388%)


<!-- leetgit:submissionId=2165098499 codeHash=8682b5a4d7184f77d9962bdf7e288dec633a5b5617154e3a6c8aece1f5d6f893 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def leastInterval(self, tasks, n):
        freq = collections.Counter(tasks)
        max_freq = max(freq.values())
        freq = list(freq.values())
        max_freq_ele_count = 0                
        i = 0
        while( i < len(freq)):
            if freq[i] == max_freq:
                max_freq_ele_count += 1
            i += 1
        ans = (max_freq - 1) * (n+1) + max_freq_ele_count
        return max(ans, len(tasks))
        
        
```
