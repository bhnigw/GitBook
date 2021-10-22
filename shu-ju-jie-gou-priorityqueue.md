---
description: PriorityQueue, Heaps
---

# \[数据结构] PriorityQueue / Heaps

底层数据结构：Binary tree。按给定的优先级排列。

**初始化：**`PriorityQueue<String> pq = new PriorityQueue<>();`

![](.gitbook/assets/939998-20160512205540484-823563038.png)



### **核心的Syntax:**

★`pq.offer(element)`： 插入元素。时间`O(logn)`；

★`pq.poll()`：**取出并返回**PriorityQueue的第一个元素（二叉树的头节点）。时间`O(logn)`；

●`pq.peek()`：返回PriorityQueue的第一个元素（二叉树的头节点），但是**不取出**。时间`O(1)`；

●`pq.remove(element)`：删去等于element的元素，如果有多个相等，只删除一个。时间：`O(n)`；

&#x20;

## Min Heap 最小堆

●`ListNode node;`\
&#x20; `PriorityQueue<ListNode> pq = new PriorityQueue<>((node1, node2) -> node1.val - node2.val);`\
意思是：根据ListNode的val值，构建min Heap，它的Heap堆顶会存放val值最小的node。





