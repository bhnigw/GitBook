# String, Character, Integer之间的互相转换：

## 单个Character和Integer之间的互相转换：

#### **1️⃣  Character 转化为➔ Integer:**

1. ★使用：`int num = ch - '0';` 找ASCII code中的位置差，注意是减，因为字符ch的位置index，与字符'0'的位置index的差值，就是这个ch代表的整数值
2. ★使用：`int num = Character.getNumericValue(ch);`
3. 使用：`int num = Integer.parseInt(String.valueOf(ch));`先用转化为string，然后转化为integer



#### **2️⃣**  ★**Integer 转化为➔ Character:**

* 使用：**`char ch = (char)(num + '0');`**找ASCII code中的位置差，**注意是加**，因为字符'0'的位置index，加上数值num，得出的数字就是字符ch应该在的位置index





## String和Integer之间的互相转换（长度不限）：

#### **1️⃣  String 转化为➔Integer:**

1. ★使用：**`int num = Integer.parseInt(str);`** 返回的是int，是primitive type
2. 使用：`Integer num = Integer.valueOf(str);` 注意Integer.valueOf\(\)返回的是object，所以要用Integer而不是int来初始化；int是primitive类型，Integer是Object。 

   如果一定要用此方法，那就需要用intValue\(\)方法把Integer转化成int：`int i = num.intValue();`  

#### **2️⃣  Integer 转化为➔ String:**

1. 使用：`String str = Integer.toString(num);`
2. ★使用：`String str = String.valueOf(num);`





## String和Character之间的互相转换：

### **1️⃣ 单个Character和String的相互转换：**

#### **String 转化为➔ Character:**

       使用：`char ch = str.charAt(i);` 单个返回str中第i个字符

#### **Character 转化为➔ String:**

1. 使用：`String str = Character.toString(ch);`
2. 使用：`String str = String.valueOf(ch);`





### 2️⃣ 一串char\[ \] array和**String的互相转换：**

#### **String 转化为➔** char\[ \] array**:**

`String str = "abcd";  
char[] JavaCharArray = str.toCharArray();`

#### 

#### char\[ \] array **转化为➔ String:**

`char[] JavaCharArray = {'a', 'b', 'c', 'd', 'e'};` 

1. 使用：`String str = new String(JavaCharArray);`
2. 使用：`String str = String.valueOf(JavaCharArray);`



