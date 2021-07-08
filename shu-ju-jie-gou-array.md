---
description: array，char array
---

# \[数据结构\] Array

#### 一些Syntax：

●`Arrays.sort()`：升序排列，sort in ascending order；

●`Arrays.fill(nums, 10)`：把数组`nums[]`里面所有数变成10；

●`Arrays.equals(nums1, nums2))`：比较两个array是否完全一样，一样就返回true；



#### ⚠️  注意：`Arrays.sort()`方法本身的return type是void，它只排序数组，并不返回任何东西，所以不能用它来赋值；

#### 以下写法都是错误的：

❌   `int nums1[] = Arrays.sort(nums2);`

❌   `return Arrays.sort(nums);`





### 怎样初始化一个char array：

`char arr1[] = {'a', 'b', 'c'};`

`char arr2[] = new char[]{'a', 'b', 'c'};`

`char arr3[]=new char[3];   
d[0] = 'a';   
d[1] = 'b';   
d[2] = 'c';`





