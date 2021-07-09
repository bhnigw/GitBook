---
description: 'Set, HashSet'
---

# \[数据结构\] Set

概念：HashSet是一个集合\(Set\)，**不能有重复元素**，而且是无序的，可以有null值。 

**初始化**： 

`HashSet<String> set = new HashSet<>();` 

`Set<Character> set = new HashSet<>();`



### **核心的Syntax:**

★**`set.add()`**: 加入一个值；同时，add\(\)方法也会返回一个boolean值，如果要加入的值是set里没有的就返回true，如果要加入的值set里已经有了，就返回false；\(见下面例子\)  
**相当于add\(\)方法就已经包含了contains\(\)方法❗️❗️**

★**`set.contains(Object o)`**: 判断set里是否有这个值，有就return true 

●`set.remove(Object o)`: 去掉set里某个值 

●`set.size()`: 返回set的size，是int值 



示例：

```text
    Set<Integer> set = new HashSet<>();
		
		set.add(1);
		set.add(2);
		set.add(3);
		set.add(4);

		System.out.println(set.add(3)); //这里会返回false
```

#### 其他Syntax：

●`set.isEmpty()`: 判断set是否为空 

`set.clear()`: 去掉set里所有值. 

`set.iterator()`: Used to return an iterator over the element in the set. 

`set.clone()`: 复制这个set



#### Set如何转化成Array?

●`Object[] arr = HashSet.toArray();`



### ❗️Set如何转化成ArrayList?

●`List<String> list = new ArrayList(set);`







