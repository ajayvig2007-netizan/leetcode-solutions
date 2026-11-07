# 83. Remove Duplicates from Sorted List
  
<br>**Problem:** https://leetcode.com/problems/remove-duplicates-from-sorted-list/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-07 19:18 local time

**Runtime:** 4 ms (beats 21.2517%)
**Memory:** 12.4 MB (beats 52.961900000000014%)


<!-- leetgit:submissionId=2191295211 codeHash=c7d3ef4889fa0ffe37c5a0fbcdc844b56bf68dd0c247e0b08305f981661d6086 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def deleteDuplicates(self, head):
        if head is None:
            return head
        curr=head
        while curr is not None:
            while curr.next is not None and  curr.val==curr.next.val:
                curr.next=curr.next.next
            curr=curr.next
        return head
        
```
