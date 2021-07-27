# 前序遍历 Pre-order traversal

原题地址：[https://leetcode.com/problems/binary-tree-preorder-traversal/](https://leetcode.com/problems/binary-tree-preorder-traversal/)

### 前序遍历 Pre-order：根→左→右（`Top down`） 



Pre-order是先把root加进去，再走左child，和右child；

```text
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<>();
        if (root == null) return res;
        
        helper(root, res);
        
        return res;
    }
    
    private void helper(TreeNode root, List<Integer> res) {
        res.add(root.val); // 区别就在这一行的位置
        
        if (root.left != null) {
            helper(root.left, res);
        }
        
        if (root.right != null) {
            helper(root.right, res);
        }
    }
}
```

Time: `O(N)`，每个node走了一遍  
Space: `O(N)`，res的size 

