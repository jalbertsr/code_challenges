## REMDUPLK
#### Python
#### 18 min 

Given a sorted linked list, delete all duplicates such that each element appear only once.

For example,
Given `1->1->2`, return `1->2`.
Given `1->1->2->3->3`, return `1->2->3`.

My solution:

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None
class Solution:
    # @param A : head node of linked list
    # @return the head node in the linked list
    def deleteDuplicates(self, A):
        head = current = A
        previous = None
        while current.next is not None:
            if current.val == current.next.val:
                if previous is None:
                    head = current.next
                else:
                    previous.next = current.next
            else:
                previous = current
            current = current.next
        return head
```
