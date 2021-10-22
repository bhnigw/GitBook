---
description: array，char array
---

# \[数据结构] Array

### 数组初始化的默认值：

整数类型（byte、short、int、long）**默认值是0； **

布尔类型（boolean）**默认值是false； **

浮点类型（float、double）默认值是0.0；&#x20;

字符类型（char）默认值是'\u0000'；&#x20;

类型的引用类型（类、数组、接口、String）默认值是null；



### 初始化方式：&#x20;

#### 一.静态初始化：初始化时人为指定每个数组元素的初始值，由系统决定数组的长度；&#x20;

示例1： \
`int[] nums; `\
`nums = new int[]{1, 6, 3, 4, 5, 9}; `

示例2：\
`String[] str = {"aaa", "bbb", "ccc"};`

#### 二.动态初始化：初始化时人为指定数组的长度，由系统初始化每个数组元素的默认值；

示例： \
`int[] nums = new int[10];` 此时数组所有元素默认值为0



### 一些Syntax：

●`Arrays.sort()`：升序排列，sort in ascending order；

●`Arrays.fill(nums, 10)`：把数组`nums[]`里面所有数变成10；

●`Arrays.equals(nums1, nums2))`：比较两个array是否完全一样，一样就返回true；



{% hint style="danger" %}
#### 注意：`Arrays.sort()`方法本身的return type是void，它只排序数组，并不返回任何东西，所以不能用它来赋值；
{% endhint %}

#### 以下写法都是错误的：

❌   `int nums1[] = Arrays.sort(nums2);`

❌   `return Arrays.sort(nums);`





### 怎样初始化一个char array：

`char arr1[] = {'a', 'b', 'c'};`

`char arr2[] = new char[]{'a', 'b', 'c'};`

`char arr3[] = new char[3]; `\
`d[0] = 'a'; `\
`d[1] = 'b'; `\
`d[2] = 'c';`



### 怎样遍历26个英文字母：

`for (char ch = 'a'; ch <= 'z'; ch++) {`\
`...}`







