# 908. Middle of the Linked List
  
<br>**Problem:** https://leetcode.com/problems/middle-of-the-linked-list/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-02 17:20 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.2 MB (beats 96.8696%)


<!-- leetgit:submissionId=2187715187 codeHash=6994261e22d6009c5bd04b4b1bcf6b2b603b25f60bf655dfa88fd00267f301e0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def middleNode(self, head):
        curr=head
        count=0
        mid=1
        while curr is not None:
            curr=curr.next
            count+=1
        mid=(count//2)+1
        c=0
        curr=head
        while c!=mid-1:
            curr=curr.next
            c+=1
        head=curr
        return head




        
```
