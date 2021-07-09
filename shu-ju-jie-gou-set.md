---
description: 'Set, HashSet'
---

# \[数据结构\] Set

概念：HashSet是一个集合\(Set\)，**不能有重复元素**，而且是无序的，可以有null值。 

**初始化**： 

`HashSet<String> set = new HashSet<>();` 

`Set<Character> set = new HashSet<>();`



### **核心的Syntax:**

●`set.add()`: 加入一个值 

●`set.remove(Object o)`: 去掉set里某个值 

★**`set.contains(Object o)`**: 判断set里是否有这个值，有就return true 

●`set.size()`: 返回set的size，是int值 



#### 其他Syntax：

●`set.isEmpty()`: 判断set是否为空 

`set.clear()`: 去掉set里所有值. 

`set.iterator()`: Used to return an iterator over the element in the set. 

`set.clone()`: 复制这个set



#### Set如何转化成Array?

●`Object[] arr = HashSet.toArray();`



### ❗️Set如何转化成ArrayList?

●`List<String> list = new ArrayList(set);`







