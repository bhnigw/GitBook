# 空间复杂度 Space complexity

●如果用HashMap或者StringBuilder新建一个长度为n的东西，空间复杂度为`O(n)`；

●如果新建一个长度为n的数组，空间复杂度为`O(n)`；



●DFS：  
空间复杂度为DFS的层数，也就是树的高度。

●BFS：  
空间复杂度为BFS的最大深度，也就是能够reach到图的最深处的那条路径的长度。  
假设有n个node，构成一个图，进行BFS，那么worst case就是所有的node构成一条直线图；  
在backtrack的时候，我们需要用一个`visited[]`的数组来记录已经访问过的node，这个数组的长度就为n，所以空间为`O(n)`；



●Union find：

