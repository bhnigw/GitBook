# ASCII码

**全称：**  
ASCII \(\(American Standard Code for Information Interchange\): 美国信息交换标准代码

Standard ASCII 码使用7位二进制数组合来表示**128**个字符，包括所有的大写和小写字母，数字0到9，标点符号，以及在美式英语中使用的特殊控制字符。

Extended ASCII 码使用8位二进制数组合来表示256个字符。比Standard ASCII 码扩充出来的符号包括表格符号、计算符号、希腊字母和特殊的拉丁符号。

下图是Standard ASCII ：

![](../.gitbook/assets/screen-shot-2021-07-08-at-9.40.47-pm.png)





对于Character来说，可以作为index直接放进数组。

```text
    int[] nums = new int[128];
    nums['B']++;

    for (int i = 0; i < 128; i++) {
        if (nums[i] == 1) {
            System.out.println(i); //这里会输出66，与上图对应
        }
    }
```







对于Character来说，可以作为index直接放进数组。

两个char相加：



数字和char相加：



如何把index转化为char：















确定每个digit字符相应的指数位置应该是该字符减1，而不是减0：  
`ch - '0'`：意思是求ch本身是数字几，假设ch='5'，那么`ch - '0'`就等于整数5；  
`ch - '1'`：意思是求index，假设ch='5'，那么`ch - '1'`就等于整数4，意思是`nums[4]`的位置对应字符ch='5'；









使用：`int num = ch - '0';` 找ASCII code中的位置差，注意是减，因为字符ch的位置index，与字符'0'的位置index的差值，就是这个ch代表的整数值

使用：**`char ch = (char)(num + '0');`**找ASCII code中的位置差，**注意是加**，因为字符'0'的位置index，加上数值num，得出的数字就是字符ch应该在的位置index







