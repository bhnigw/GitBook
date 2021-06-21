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



其他Syntax:

`qName.isEmpty()`：判断是否为空

`qName.size()`：返回queue中元素的个数

`qName.add(element)`：把一个元素加到queue的末尾tail；一般用offer\(\)更好

`qName.remove()`：**取出并返回**queue的第一个元素。 

poll\(\)和remove\(\)的区别：功能是一样的，区别体现在queue为空的时候：remove\(\) 会报NoSuchElementException的错，但是poll\(\)会返回null，所以一般用poll\(\)更好





关系图：

![](../.gitbook/assets/queue-deque-priorityqueue-in-java.png)









