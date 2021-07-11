# ASCII码

**全称：**  
ASCII \(\(American Standard Code for Information Interchange\): 美国信息交换标准代码

Standard ASCII 码使用7位二进制数组合来表示**128**个字符，包括所有的大写和小写字母，数字0到9，标点符号，以及在美式英语中使用的特殊控制字符。

Extended ASCII 码使用8位二进制数组合来表示256个字符。比Standard ASCII 码扩充出来的符号包括表格符号、计算符号、希腊字母和特殊的拉丁符号。

下图是Standard ASCII ：

![](../.gitbook/assets/screen-shot-2021-07-08-at-9.40.47-pm.png)

## char类型的加减法运算 

char字符变量可以进行加减运算，在运算的时候，通过查找char字符对应的的ASCII值，然后用ASCII里的对应值进行加减运算。

●**可以简单理解为：字符加减就是ASCII中对应的index相加减；**

例1：  
`char a = '1';`                           //字符'1'对应049  
`char b = '2';`                           //字符'2'对应050  
`System.out.println(a + b);` //这里会输出99

例2：  
`char a = '3';`                           //字符'3'对应051  
`char b = 'D';`                           //字符'D'对应068  
`System.out.println(a + b);` //这里会输出119



### 应用1：把char字符转化为整数int类型

`char ch = '6';`   
**`int num = ch - '0';`**            //当公式来记  
`System.out.println(num);` //这里会输出int类型的6

这里为什么是减法❓  
如果是加法，那`'6'`对应054，`'0'`对应048，加起来就是102；  
如果是减法，那`'6'`对应054，`'0'`对应048，相减就是6；

可以理解为：数字字符`ch`和字符`'0'`的位置差就是这个数字本身，所以要通过index相减，来算位置差。



### 应用2：把整数int类型转化为char字符

`int num = 6;`  
**`char ch = (char)(num + '0');`**   //当公式来记  
`System.out.println(ch);`             //这里会输出字符类型的'6'

这里为什么是加法❓  
如果是减法，那整数6本身是6，`'0'`对应048，相减就是 - 42，无意义；  
如果是加法，那整数6本身是6，`'0'`对应048，加起来就是054，ACSII里对应的位置就是`'6'`；

可以理解为：字符`'0'`对应的index，加上整数num，就是num对应的数字字符在ACSII中的index；  




#### 前情提要：char字符可以作为index直接放进数组

```text
    int[] ascii = new int[128];
    ascii['B']++;

    for (int i = 0; i < 128; i++) {
        if (ascii[i] == 1) {
            System.out.println(i); //这里会输出66，与上图对应
        }
    }
```

根据这个前情提要，我们可以得出应用3：



### 应用3：统计数字或字母的出现次数

#### 一、统计数字（适用于统计只含0～9的char array）

方法：使用长度为10的`nums[]`数组，数字出现一次就在对应的index加一：`nums[ch - '0']++;`

`nums[]`的长度为10，对应数字0～9，`'0'`的index是0，`'1'`的index是1，是一一对应的；

```text
		char[] Array = { '3', '5', '3', '1' };
		int[] nums = new int[10];

		for (char ch : Array) {
			nums[ch - '0']++;
		}
```

此时nums等于`{ 0, 1, 0, 2, 0, 1, 0, 0, 0, 0 }`



#### 二、统计字母



#### 三、同时统计字母和数字





确定每个digit字符相应的指数位置应该是该字符减1，而不是减0：  
`ch - '0'`：意思是求ch本身是数字几，假设ch='5'，那么`ch - '0'`就等于整数5；  
`ch - '1'`：意思是求index，假设ch='5'，那么`ch - '1'`就等于整数4，意思是`nums[4]`的位置对应字符ch='5'；











例题：

[171. Excel Sheet Column Number](https://bhnigw.gitbook.io/leetcode/leetcode-171.-excel-sheet-column-number)

[36. Valid Sudoku](https://bhnigw.gitbook.io/leetcode/leetcode-36.-valid-sudoku)



