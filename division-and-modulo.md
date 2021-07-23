---
description: 取整和求余
---

# Division "/"  and Modulo "%"

### 取整（Division "/"）：

**可以理解为：能被整除多少次；**

当数据类型为int时，只保留除法结果的整数部分，去掉小数部分；

只有当数据类型为double的时候，才会进行真正意义上的除法运算；

例子：

```text
System.out.println(1 / 3);    //结果为0
System.out.println(25 / 10);  //结果为2
```



### 求余（Modulo "%"）：

理解：就是字面上的意思，求余数。（并不限定于正整数）

例子：

```text
System.out.println(1 % 3);    //结果为1
System.out.println(25 % 10);  //结果为5
System.out.println(4.5 % 3);  //结果为1.5
```

应用1：判断奇偶

`return count % 2 == 0 ? 1 : -1;`  //意思是count为偶数返回1，奇数返回-1



例题：

[171. Excel Sheet Column Number](https://bhnigw.gitbook.io/leetcode/leetcode-171.-excel-sheet-column-number)

