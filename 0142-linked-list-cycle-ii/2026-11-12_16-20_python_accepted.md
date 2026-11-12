# 142. Linked List Cycle II
  
<br>**Problem:** https://leetcode.com/problems/linked-list-cycle-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, Linked List, Two Pointers, Floyd's Cycle Finding Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-12 16:20 local time

**Runtime:** 36 ms (beats 43.21869999999997%)
**Memory:** 18.7 MB (beats 59.83839999999999%)


<!-- leetgit:submissionId=2194545898 codeHash=28bedebaca9fee02bf24c6634b9b4fd46be965936ad993ce48c84f29aa78a387 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def detectCycle(self, head):
        if head is None:
            return None

        slow = head
        fast = head

        while fast is not None and fast.next is not None:
            slow = slow.next
            fast = fast.next.next

            if slow is fast:
                c = fast
                curr = head

                while curr is not c:
                    curr = curr.next
                    c = c.next

                return curr

        return None
```
