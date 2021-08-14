---
description: PriorityQueue
---

# \[数据结构\] PriorityQueue

PriorityQueue&lt;String&gt; pq = new PriorityQueue&lt;&gt;\(\);



### **核心的Syntax:**

★`pq.offer(element)`： 插入元素。时间`O(logn)`；

★`pq.poll()`：**取出并返回**PriorityQueue的第一个元素。时间`O(logn)`；

●`pq.peek()`：返回PriorityQueue的第一个元素，但是**不取出**。时间`O(1)`；

●`pq.remove(element)`：删去跟element相等的某一个元素，如果有多个相等，只删除一个。时间：O\(n\)

 此实现为排队和出队方法（offer、poll、remove\(\) 和 add）提供 O\(log\(n\)\) 时间；为 remove\(Object\) 和 contains\(Object\) 方法提供线性时间；为获取方法（peek、element 和 size）提供固定时间。

