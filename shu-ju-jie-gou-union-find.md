---
description: Union Find
---

# \[数据结构] Union Find

Union Find的作用/目的：

1. 用来判断两个节点是否在同一个图中（Determine whether two nodes are in the same connected component）
2. 通过往图里添加edge，来判断它是否导致图里出现环cycle/loop；



具体实现：\
假设图中有n个node，给出n和edges的值：\
`Input: n = 5, edges = [[0,1], [1,2], [2,3], [1,4], [1,3]] `

![](<.gitbook/assets/tree2-graph (1).jpg>)

### Make set：

初始化一个数组`parent[]`，用来记录每一个节点的parent node；初始值是每一个node本身的值。

![](.gitbook/assets/IMG\_6364.jpg)



### Find：

`Find(x)`是寻找元素x属于哪一个set；\
过程就是随着x的parent node一路找下去，直到找到root node；

```
// Find root of each node

    public int find(int node) {
        while (node != parent[node]) { 
            node = parent[node]; 
        }
        //随着parent node一路找下去，直到node等于parent[]
        
        return node;
    }
```



### Union：

有两个set，A和B，`Union(A, B)`过程就是把A和B取并集：`A⋃B`；\
融合变为一个set；

```
    public boolean union(int nodeA, int nodeB) {
        int rootA = find(nodeA); //用find找到每一个点的root
        int rootB = find(nodeB);
        
        if (rootA == rootB) return false; // 如果两root相等，说明检测到Cycle
        
        parent[rootA] = rootB; //不相等，则融合变为一个set
        
        return true;
    }
```



详细图解：`edges = [[0,1], [1,2], [2,3], [1,4], [1,3]] `

第一步：`union(0, 1)`，用find()找到rootA和rootB，判断其是否相等，若不等，则把两个节点union成一个set，具体实现是更新parent数组：`parent[rootA] = rootB`

![](.gitbook/assets/IMG\_6367.jpg)



第二步：`union(1, 2)`，用find()找到rootA和rootB，判断其是否相等，若不等，则把两个节点union成一个set，具体实现是更新parent数组：`parent[rootA] = rootB`

![](.gitbook/assets/IMG\_6368.jpg)



第三步：`union(2, 3)`，用find()找到rootA和rootB，判断其是否相等，若不等，则把两个节点union成一个set，具体实现是更新parent数组：`parent[rootA] = rootB`

![](.gitbook/assets/IMG\_6369.jpg)



第四步：`union(1, 4)`，用find()找到rootA和rootB，判断其是否相等，若不等，则把两个节点union成一个set，具体实现是更新parent数组：`parent[rootA] = rootB`

![](.gitbook/assets/IMG\_6371.jpg)



第五步：`union(1, 3)`，用find()找到rootA和rootB，这里rootA和rootB值相等都为4，说明出现了cycle：

![](.gitbook/assets/IMG\_6372.jpg)



Time：

Space：





### Path compression？



例题：[261. Graph Valid Tree](https://bhnigw.gitbook.io/leetcode/leetcode-261.-graph-valid-tree)
