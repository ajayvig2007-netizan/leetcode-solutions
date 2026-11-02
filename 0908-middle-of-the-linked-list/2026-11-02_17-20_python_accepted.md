# 908. Middle of the Linked List
  
<br>**Problem:** https://leetcode.com/problems/middle-of-the-linked-list/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-02 17:20 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.5 MB (beats 20.996499999999997%)


<!-- leetgit:submissionId=2187715041 codeHash=2dfee5bf260393b96f11cd168392664f28d44d2a4fc5e716ef0f09f322097b48 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
        if count%2!=0:
            mid=(count//2)+1
        else:
            mid=(count//2)+1
        c=0
        curr=head
        while c!=mid-1:
            curr=curr.next
            c+=1
        head=curr
        return head




        
```
