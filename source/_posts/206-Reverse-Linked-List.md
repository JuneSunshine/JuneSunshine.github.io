---
title: 206. Reverse Linked List
date: 2017-09-19 16:40:51
tags: [Leetcode, Linked List]
categories: Tech
---

## Problem
>Reverse a singly linked list.

<!--more-->

## Solution

1. #### Iterative
```python
class Solution(object):
    def reverseList(self, head):
        """
        :type head: ListNode
        :rtype: ListNode
        """
        prev = None
        while head:
            curr = head
            head = head.next
            curr.next = prev
            prev = curr
        return prev
```

2. #### Recursive    
```python
class Solution(object):
    def reverseList(self, head):
       """
       :type head: ListNode
       :rtype: ListNode
       """
       return self._reverse(head)
            
    def _reverse(self, node, prev = None):
       if not node:
           return prev
       n = node.next
       node.next = prev
       return self._reverse(n, node)
```

