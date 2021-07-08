---
description: 'Set, HashSet'
---

# \[数据结构\] Set

概念：HashSet是一个集合\(Set\)，是不能有重复元素的，而且是无序的，可以有null值。 

**初始化**： 

`HashSet<String> set = new HashSet<>();` 

`Set<Character> set = new HashSet<>();`



**核心的Syntax:**

1. add\(\): 加入一个值 

2. clear\(\): 去掉set里所有值. 

3. contains\(Object o\): 判断set里是否有这个值，有就return true 

4. remove\(Object o\): 去掉set里某个值 

5. iterator\(\): Used to return an iterator over the element in the set. 

6. isEmpty\(\): 判断set是否为空 

7. size\(\): 返回set的size，是int值 

8. clone\(\): 复制这个set



\*把set转换为数组的形式： Object\[\] arr = HashSet.toArray\(\)

