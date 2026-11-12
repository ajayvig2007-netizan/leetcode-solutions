# 141. Linked List Cycle
  
<br>**Problem:** https://leetcode.com/problems/linked-list-cycle/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, Linked List, Two Pointers, Floyd's Cycle Finding Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-12 16:01 local time

**Runtime:** 38 ms (beats 60.11019999999997%)
**Memory:** 19.2 MB (beats 93.7154%)


<!-- leetgit:submissionId=2194535458 codeHash=d31d13d5b0e70e3c5ce5ee3efddc476bf114c835ea91ad76238322d5bef9c9a6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def hasCycle(self, head):
        if head is None:
            return False

        slow = head
        fast = head

        while fast is not None and fast.next is not None:
            slow = slow.next
            fast = fast.next.next

            if slow is fast:
                return True

        return False
```
