# \[数学方法] Java Math Method

## Java Math Method

●`Math.max(23.1, 19)`：返回二者中最大的数

●`Math.min(23.1, 19)`：返回二者中最小的数

★`Math.pow(a, b)`：次方，a是底数base，b是指数exponent

●`Math.sqrt(81)`：求平方根

●`Math.abs(-4.7)`：取绝对值



★`Integer.MAX_VALUE`：Integer类型最大值，也就是2 ^ 31 - 1 = 2147483647&#x20;

★`Integer.MIN_VALUE`：Integer类型最小值，也就是 - 2 ^ 31 = - 2147483648

●`Long.MAX_VALUE`：Long类型最大值，也就是2 ^ 63 - 1&#x20;

●`Long.MIN_VALUE`：Long类型最小值，也就是 - 2 ^ 63



## 如何产生一个随机数：

●`Math.random()`：随机产生一个0～1之间的小数；

●`nextInt(a)`：随机产生一个0～a之间的整数，不包括a；

例：`Random rand = new Random(); `\
`int rand_int = rand.nextInt(100);`
