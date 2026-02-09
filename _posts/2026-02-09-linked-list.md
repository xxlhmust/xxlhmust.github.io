---
layout: post
title: "链表：原理、应用与LeetCode实战"
date: 2026-02-09 10:00:00 +0800
categories: [数据结构与算法, LeetCode]
tags: [链表, 数据结构, 算法, 时间复杂度, LeetCode]
author: xxlh
toc: true
comments: true
math: true
mermaid: true
pin: false
---

## 📚 链表的基本概念

链表（Linked List）是一种线性数据结构，由一系列节点（Node）组成，每个节点包含数据和指向下一个节点的指针。与数组不同，链表中的元素在内存中不是连续存储的。

### 核心特性

1. **动态内存分配**：链表的大小可以在运行时动态增长或缩小
2. **非连续存储**：节点在内存中分散存储，通过指针连接
3. **灵活插入删除**：插入和删除操作的时间复杂度为 O(1)
4. **顺序访问**：访问特定位置的元素需要 O(n) 时间

## 🔍 链表的特点

1. **指针连接**：每个节点通过指针指向下一个节点，形成链式结构
2. **动态大小**：无需预先知道数据规模，可以随时扩展
3. **内存效率**：只有在需要时才分配内存，减少内存浪费
4. **灵活操作**：插入和删除操作非常高效，只需修改指针

### 例题
```html
<h6>1.相交链表</h6>
<pre><code class="language-python">
class Solution:
    def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
        qa = headA
        qb = headB
        while qa != qb:     
            qa = qa.next if qa else headB
            qb = qb.next if qb else headA  #双方分别便利全部的链表，即从a-->b,b-->a
        return qa
</code></pre>
<h6>2.反转链表</h6>
<pre><code class="language-python">
class Solution:
    def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        pre = None
        cur = head
        while  cur:
            nxt = cur.nxt  #先保存 在修改指向
            cur.next = pre
            pre = cur
            cur = nxt
         return pre #（双指针）
</code></pre>
<h6>3.回文链表</h6>
<pre><code class="language-python">
class Solution:
    def isPalindrome(self, head: Optional[ListNode]) -> bool:
        empty = []
        cur = head
        while cur:
            empty-list.append(cur.val)
            cur = cur.next
        return empty == empty[::-1]  #时间空间复杂度均为O(n)
<h6>4.环形链表</h6>
<pre><code class="language-python">
class Solution:
    def hasCycle(self, head: ListNode) -> bool:
        if not head:
            return False   # 避免fast报错，一旦head = None,head.next无意义
        slow = head
        fast = head.next
        while slow != fast:
            if not fast or  not fast.next :
                 return False
            slow = slow.next
            fast = fast.next.next
        return True       #快慢指针（双指针）
        





