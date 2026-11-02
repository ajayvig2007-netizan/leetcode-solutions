# 206. Reverse Linked List
  
<br>**Problem:** https://leetcode.com/problems/reverse-linked-list/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List, Recursion<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-02 16:58 local time

**Runtime:** 1 ms (beats 20.461600000000004%)
**Memory:** 14.1 MB (beats 96.1573%)


<!-- leetgit:submissionId=2187703452 codeHash=f338bb2199b5d08c01f43d7884d942490cbc987791dae711a53a7e907ecc579a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def reverseList(self, head):
        if head is None:
            return head
        else:
            curr=head
            if curr.next is not None:
                next1=curr.next
                while next1.next is not None:
                    c=next1.next
                    next1.next=curr
                    curr=next1
                    next1=c
                else:
                    l=head
                    l.next=None
                    next1.next=curr
                    head=next1
        return head



        
```
