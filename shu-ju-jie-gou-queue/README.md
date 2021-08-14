---
description: 'Queue, LinkedList'
---

# \[数据结构\] Queue

核心：First-in-First-out**；**

**初始化：**`Queue<String> qName = new LinkedList<>();` 注意后面是LinkedList



### **核心的Syntax:**

●`qName.offer(element)`： 把一个元素加到queue的末尾tail。offer\(\)比add\(\)更优，因为capacity满了后不会报错。Because this method does not throws an exception when the capacity of the container is full since it returns false. 

●`qName.poll()`：**取出并返回**queue的第一个元素。如果queue是空的就返回Null

●`qName.peek()`：返回queue的第一个元素，但是**不取出**。如果queue是空的就返回Null



#### 其他Syntax:

`qName.isEmpty()`：判断是否为空

`qName.size()`：返回queue中元素的个数

`qName.add(element)`：把一个元素加到queue的末尾tail；一般用offer\(\)更好

`qName.remove()`：**取出并返回**queue的第一个元素。 

`qName.contains(element)`：判断是否包含element这个元素，有就返回true。



### 方法比较：

●`add()`和`offer()`：功能一样，都是插入元素。区别：capacity满了后，add\(\)会报错，offer\(\)则会返回false。所以offer\(\)更优。

●`remove()`和`poll()`： 功能一样，都是获取并删除队首元素。区别：queue为空的时候，remove\(\)会报NoSuchElementException的错，但是poll\(\)会返回null。所以poll\(\)更优。







关系图：

![](../.gitbook/assets/queue-deque-priorityqueue-in-java.png)









