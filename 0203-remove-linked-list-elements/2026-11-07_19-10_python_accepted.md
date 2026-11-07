# 203. Remove Linked List Elements
  
<br>**Problem:** https://leetcode.com/problems/remove-linked-list-elements/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List, Recursion<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-07 19:10 local time

**Runtime:** 4 ms (beats 59.3277%)
**Memory:** 19.2 MB (beats 86.5904%)


<!-- leetgit:submissionId=2191291433 codeHash=7691a8d9ba13b11601840f013a9b86dccb763d83a0229573cd1123f74412d73b notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def removeElements(self, head, val):
        if head is None:
            return head
        while head is not None and head.val==val:
            head=head.next
        curr=head
        while curr is not None and curr.next is not None:
            prev=curr
            curr=curr.next
            while curr is not None and curr.val==val:
                prev.next=curr.next
                curr=curr.next
        return head
        
        
```
