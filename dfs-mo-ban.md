# DFS模版

### 经典例题：

[200. Number of Islands](https://bhnigw.gitbook.io/leetcode/leetcode/leetcode-200.-number-of-islands)

[529. Minesweeper](https://bhnigw.gitbook.io/leetcode/leetcode/leetcode-529.-minesweeper)

[79. Word Search](https://bhnigw.gitbook.io/leetcode/leetcode/leetcode-79.-word-search)

```
class Solution {
    public int numIslands(char[][] grid) {
        int res = 0;
        
        if (grid == null || grid.length == 0) return 0;
        
        for (int i = 0; i < grid.length; i++) {
            for (int j = 0; j < grid[0].length; j++) {
                if (grid[i][j] == '1') { //遇到island就加一
                    res++;
                    dfs(grid, i, j);                               
                } 
            } 
        }
        
        return res;
    }
    
    private void dfs(char[][] grid, int m, int n) {
        if(m < 0 || n < 0 || m >= grid.length || n >= grid[0].length || grid[m][n] == '0') {
            return;
        }//这里if包含了；两个判断，一个是如果grid[m][n]=='0'就直接return
         //第二个判断是：下面的m,n加一减一不能out of bound
        
        grid[m][n] = '0';
        dfs(grid, m - 1, n); //注意这里m-1不能小于0
        dfs(grid, m + 1, n); //这里m+1不能大于等于grid.length
        dfs(grid, m, n + 1);
        dfs(grid, m, n - 1); //这里n+1不能大于等于grid[0].length
    }
}                

```





```
class Solution {
    public (char[][] board, String word) {        
        if (word == null || word.length() == 0) return false;
        
        for (int i = 0; i < board.length; i++) {
            for (int j = 0; j < board[0].length; j++) {
                if (dfs(board, word, i, j, 0)) {       
                    return true;
                }
            }
        }
        
        return false;
    }
    
    private boolean dfs(char[][] board, String word, int i, int j, int index) {
        if (index == word.length()) return true; //注意

        if (i < 0 || i >= board.length || j < 0 || j >= board[0].length) return false;
        
        char ch = board[i][j];
        if (ch != word.charAt(index)) return false; //字母不同，或者是星号'*'，返回false
        
        board[i][j] = '*';
        
        boolean found = false;
        
        if (dfs(board, word, i + 1, j, index + 1) || dfs(board, word, i - 1, j, index + 1) || 
           dfs(board, word, i, j + 1, index + 1) || dfs(board, word, i, j - 1, index + 1)) {
            found = true;
        }
        
        board[i][j] = ch;
        
        return found;
    }
}
```
