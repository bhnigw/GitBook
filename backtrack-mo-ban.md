---
description: Backtrack，Recursive
---

# Backtrack模板

**概念：**回溯法是一种搜索算法，当探索到某一步时，发现此选择并不优，或达不到目标，就退回一步重新选择，这种走不通就退回再走的技术称为**back tracking；**

**理解：**可以理解为通过选择不同的岔路口寻找目的地，一个岔路口一个岔路口的去尝试找到目的地。如果走错了路，继续返回来找到岔路口的另一条路，直到找到目的地。

{% hint style="info" %}
#### Backtrack的核心是，在每一次往回back track的时候，都要抹去它走过的痕迹！
{% endhint %}



### 典型例子：

#### 例1：求子集[Generate all subsets](https://bhnigw.gitbook.io/leetcode/leetcode-78.-subsets)：

在往回back track的时候，要去掉current subset的末尾的元素：

![](.gitbook/assets/IMG\_6394.jpg)



#### 例2：有向图中检查环 [Detect cycle in a directed graph](https://bhnigw.gitbook.io/leetcode/ji-chu-bi-hui/detect-cycle-in-a-directed-graph)：

走过的节点在`visited[]`里标记为true，在往回back track的时候，要变回false；

比如在下图中，路径`4 -> 0 -> 1`不是环，所以回到起点4后，boolean数组就变回了`visited = [F, F, F, F, T]`

![](.gitbook/assets/IMG\_6338.jpg)

