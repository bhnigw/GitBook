# DFS模版







```text
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

