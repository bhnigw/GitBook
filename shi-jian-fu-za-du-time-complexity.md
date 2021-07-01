# 时间复杂度 Time complexity

●DFS：  
时间为DFS的最大深度，也就是能够reach到图的最深处的那条路径的长度。  
假设有n个node，构成一个图，进行DFS，那么worst case就是所有的node构成一条直线图；  
那么时间就是`O(n)`；或者是顶点vertex总数，加上edge的总数的总和`O(N + E)`；



●BFS：  
顶点vertex总数，加上edge的总数的总和，worst case下需要访问所有的vertex和edge；  
所以时间就是`O(N + E)`；



●Backtrack：  
如果有n个node，构成一个图，进行Backtrack，那么worst case就是所有的node构成一条直线图：  
假如n = 5，那么图为：

![](.gitbook/assets/207_chain.png)

每一多个step，时间复杂度就加一，上图的复杂度为4+3+2+1；

如果有n个node，那么时间复杂度就为\(\(n - 1\) + 1\) \* n /2 （首项加末项乘以项数除以二）  
也就是`O(n^2)`



●Union find：







