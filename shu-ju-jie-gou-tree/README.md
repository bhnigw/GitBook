---
description: Tree
---

# \[数据结构\] Tree

## Tree的概念和性质

树是一种无向图（undirected graph），其中任意两个顶点间存在唯一一条路径。

{% hint style="info" %}
**一个graph能称作是一个tree，那么它必须满足以下条件/具有以下特点：**

1. 任何两个节点之间都有一条连接的路径；也就是说，所有点都必须fully connected，不能有落单的；
2. 图中不能有环cycle/loop；
3. ★**如果一个tree有n个节点，那么它必然有n - 1条edges**； 若少于`n - 1`则必然有点没有连接上， 若多于`n - 1`则必然有环cycle/loop；
{% endhint %}



## Binary Trees

**二叉树Binary trees**：每个节点至多含有两个子树的树称为二叉树；



### ★**Binary tree二叉树**的构造方法：背下来❗️❗️❗️

```text
public class TreeNode {
	int val;
	TreeNode left;
	TreeNode right;

	TreeNode() {}  //注意这里是什么意思

	TreeNode(int val) {
		this.val = val;
	}

	TreeNode(int val, TreeNode left, TreeNode right) {
		this.val = val;
		this.left = left;
		this.right = right;
	}
}

```

第6行的操作是什么意思？  
意思是：可以进行没有参数的初始化。没有这句的话，初始化就必须`TreeNode t = new TreeNode(3)`；有了这句就可以`TreeNode t = new TreeNode()`；



## Binary Search Trees

对于每一个节点，它的左子树上**所有节点**全都小于它的根节点的值；root的右子树不空，则右子树上所有节点的值均大于它的根节点的值；

how to add new node to a binary search tree？



Perfect Trees and Almost Complete Trees



Heaps \(min-heaps and max-heaps\)





怎样区分Queue中的结点来自哪一层？

