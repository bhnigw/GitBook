# 关于Test Case

对于确定类型的input，一般都有通用的test case模板。

## Input是String：

1. Empty or null&#x20;
2. Uppercase or lowercase
3. Special character&#x20;
4. With or without punctuation in the end （标点符号）
5. Multiple while spaces in between &#x20;
6. Very long string

最后一点，关于怎样算是very long string：\
取决于Java Virtual Machine(JVM)的memeory；Java里String可允许的最大length大约是2 billion（无需回答具体数字）



## Input是Linked list：

1. Empty list;
2. List that has cycle/loop;
3. List that spreads to two or multiple branches;
4. List is huge, too long;



Input是char array：



## Input是TreeNode：

如果是非常大的input怎么办？有两种方案：

1. 核心思想都是partition。仅处理左子树，然后把结果存到一边，然后处理右子树，把结果存到一边，最后把结果merge。
2. 分层处理，最后把结果merge



