# 141. Linked List Cycle
  
<br>**Problem:** https://leetcode.com/problems/linked-list-cycle/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, Linked List, Two Pointers, Floyd's Cycle Finding Algorithm<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-12 16:00 local time

**Runtime:** 36 ms (beats 71.39239999999997%)
**Memory:** 19.3 MB (beats 93.7154%)


<!-- leetgit:submissionId=2194535023 codeHash=da6084aff90ae89218fc257c0505bec45f06a44d9402f7ce51b3c3a74b3f892d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def hasCycle(self, head):
        if head is None:
            return False
        if head.next is None or head.next.next is None:
            return False
        slow=head
        fast=head.next.next
        c=0
        while fast.next is not None and fast.next.next is not None:
            if slow is fast:
                return True
            slow=slow.next
            fast=fast.next.next
        return False
```
