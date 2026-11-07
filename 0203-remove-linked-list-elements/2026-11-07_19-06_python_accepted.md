# 203. Remove Linked List Elements
  
<br>**Problem:** https://leetcode.com/problems/remove-linked-list-elements/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List, Recursion<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-07 19:06 local time

**Runtime:** 4 ms (beats 59.3277%)
**Memory:** 19.1 MB (beats 86.5904%)


<!-- leetgit:submissionId=2191289561 codeHash=06e9e704c55aa23a56e99288573578509349b84426d6502e88849eb29fbf7c24 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def removeElements(self, head, val):
        if head is None:
            return head
        while head is not None and head.val == val:
            head = head.next
        curr = head
        while curr is not None and curr.next is not None:
            if curr.next.val==val:
                curr.next=curr.next.next
            else:
                curr=curr.next
        return head

        
```
