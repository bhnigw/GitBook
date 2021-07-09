# \[数据结构\] String和Character

## **初始化：**

#### **String初始化：**

`String str = "abcd";`

`String str = new String("abcd");`

#### **Character初始化：**

`char ch = 'a';`   

`Character ch = 'a';`   

`Character ch = new Character('a');`

区别：char是一个primitive data type；而Character是一个Object 它包含许多static methods，如toUpperCase\(\)等。 

#### char\[ \] array的初始化：

1. `char[] JavaCharArray = {'a', 'b', 'c', 'd'};` 
2. `char[] JavaCharArray = new char[4];`



## 如何遍历String里面的characters：

方法一：直接用charAt\(\)

```text
    String str = "abcd";
		for (int i = 0; i < str.length(); i++) {
			char ch = str.charAt(i);
		}
```

方法二：转换为char\[ \] array

```text
    String str = "abcd";
		char[] JavaCharArray = str.toCharArray();
		for (char ch : JavaCharArray) {
			//操作
		}
```



## String和Character之间的互相转换：

### **1️⃣ 单个Character和String的相互转换：**

#### **String 转化为➔ Character:**

* 使用：`char ch = str.charAt(i);` 单个返回str中第i个字符

#### **Character 转化为➔ String:**

1. 使用：`String str = Character.toString(ch);`
2. 使用：`String str = String.valueOf(ch);`



### 2️⃣ 一串char\[ \] array和**String的互相转换：**

#### **String 转化为➔** char\[ \] array**:**

`String str = "abcd";  
char[] JavaCharArray = str.toCharArray();`

#### char\[ \] array **转化为➔ String:**

`char[] JavaCharArray = {'a', 'b', 'c', 'd', 'e'};   
String str = new String(JavaCharArray);`





## 两个character相加减是什么意思：

两个char相加：



数字和char相加：



如何把index转化为char：





## Java String Methods:

●`str.length()`：返回str的长度

●`str.charAt()`：返回char

●`str.tocharArray()`：把str转化为一个char\[ \] array

●`str.isEmpty()`：判断str是否为空

●`str.contains(subStr)`：如果str里包含某段subStr就返回true

★`String.valueOf()`：把括号里的值变为一个string，不管括号里是整数小数还是boolean

★`str.trim()`：去掉str首尾的所有空格

★`str1.equals(str2)`：如果str1和str2相同则返回true

★`str.split("@")`：若str是"How@Are@You?"，则返回"How"，"Are"，"You?"这三个string；

★`str.split("@", 2)`：若str是"How@Are@You?"，则返回"How"，"Are@You?"这两个string；



★`str.compare()`：把str1和str2做lexicographical的比较，返回1或-1或0；  
                                                    若返回结果为1，则str1 &gt; str2；  
                                                    若返回结果为-1，则str1 &lt; str2；  
                                                    若返回结果为0，则str1, str2相同；

★`str1.compareTo(str2)`：把str1和str2做lexicographical的比较，返回它们在Unicode中的位置差  
                                                    若返回结果 &gt; 0，则str1 &gt; str2；  
                                                    若返回结果 &lt; 0，则str1 &lt; str2；  
                                                    若返回结果 = 0，则str1, str2相同；



★`str.replace(char searchChar, char newChar)`：在str里寻找前面的char，并把str里**所有的**这个char换成第二个新的char

★`str.replaceAll(String searchStr, String newStr)`：在str里寻找前面的这个searchStr，并把str里**所有的**这个字符串换成第二个新的newStr



★`str.substring(int startIndex)`：去掉startIndex之前的所有，保留从startIndex开始直到末尾的subString并返回。英文更好理解：Substring starting from startIndex.

★`str.substring(int startIndex, int endIndex)`：截取这段index内的subString，**包括startIndex，不包括endIndex；**



●`str.toLowerCase()`：把str里所有字母变成小写

●`str.toUpperCase()`：把str里所有字母变成大写





## Java Character Methods：

★`Character.isLetter('A')`：判断char是不是英文字母，无论大小写

★`Character.isDigit('6')`：判断char是不是数字

★`Character.getNumericValue('6')`：把char转化为整数int

●`Character.isLetterOrDigit(ch)`：如果是字母或者数字就返回true，相当于\(Character.isLetter\(ch\) \|\| Character.isDigit\(ch\)\)为真

●`Character.isWhitespace(' ')`：判断char是不是空格

●`Character.isUpperCase('B')`：判断char是不是大写字母

●`Character.isLowerCase('b')`：判断char是不是小写字母

●`Character.isUpperCase('B')`：判断char是不是大写字母

●`Character.isLowerCase('b')`：判断char是不是小写字母

●`Character.toUpperCase('A')`：把char变成大写字母

●`Character.toLowerCase('A')`：把char变成小写字母

●`ch.charValue()`：把Character类型的ch转化成char的primitive type

●`Character.toString('A')`：把字符'A'转化为string "A"

●`ch1.equals(ch2)`：判断ch1, ch2是否一样





![](.gitbook/assets/screen-shot-2021-07-08-at-9.40.47-pm.png)





### \*\*\*\*



