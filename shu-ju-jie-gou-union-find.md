---
description: Union Find
---

# \[数据结构\] Union Find

Union Find的作用/目的：

1. 用来判断两个节点是否在同一个图中（Determine whether two nodes are in the same connected component）
2. 通过往图里添加edge，来判断它是否导致图里出现环cycle/loop；



具体实现：  
图有n个node，假设此时n = 5；



#### Make set：

初始化一个数组`parent[]`，用来记录每一个节点的parent node；初始值是每一个node本身的值。

![](.gitbook/assets/img_6364.jpg)





#### Find：

`Find(x)`是寻找元素x属于哪一个set；  
过程就是随着x的parent node一路找下去，直到找到root node；

```text
// Find root of each node

    public int find(int node) {
        while (node != parent[node]) { 
            node = parent[node];
        }
        
        return node;
    }
```

#### Union：

有两个set，A和B，`Union(A, B)`过程就是把A和B取并集：`A⋃B`；  
融合变为一个set；



```text
    public boolean union(int nodeA, int nodeB) {
        int rootA = find(nodeA); 
        int rootB = find(nodeB);
        
        if (rootA == rootB) return false; // 检测到Cycle
        
        parent[rootA] = rootB; //融合变为一个set
        
        return true;
    }
```

#### 









### Path compression？



例题：[261. Graph Valid Tree](https://bhnigw.gitbook.io/leetcode/leetcode-261.-graph-valid-tree)

