---
description: 'StringBuilder, StringBuffer'
---

# \[数据结构\] StringBuilder

概念：StringBuilder表示一个可变的字符characters序列。注意是character而不是string。可以实现对字符序列的增删改查。 

**初始化**：`StringBuilder sb = new StringBuilder();` 



❗️注意：此时初始化的sb只是一堆字符characters，如果要转化为字符串string，必须要用到**`sb.toString()`**方法。



**核心的Syntax:**

★`sb.append(element)`：把element加到str里；可以是String, Character, boolean... 

★`sb.reverse()`：把所有的characters颠倒 

●`sb.length()`：返回长度

●`sb.charAt(index)` 



其他Syntax:

●`sb.deleteCharAt(int index)`：删掉该index的字符 

●`sb.insert(index, ch)`：把字符ch插入到指数为index的地方去

`sb.delete(int start, int end)`：删掉这段字符，start index包括，end index不包括；

`sb.indexOf(ch)`

`sb.setCharAt(int index, char ch)`：把该index的数改为

`sb.substring(int start)`：删掉start index之前的characters，返回从start index开始，一直到最末尾的characters



 

**StringBuilder和StringBuffer的区别：**

**StringBuffer**是synchronized，是thread safe的，StringBuilder不是。但是**StringBuilder**更快。

StringBuffer is synchronized, thread safe. StringBuilder is non-synchronized, not thread safe.   
StringBuilder is more efficient than StringBuffer.

