# 中序遍历 In-order traversal

原题地址：[https://leetcode.com/problems/binary-tree-inorder-traversal/](https://leetcode.com/problems/binary-tree-inorder-traversal/)

### 中序遍历 In-order：左→根→右



In-order是先走左child，再把root加进去，最后走右child；

```
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<>();
        if (root == null) return res;
        
        helper(root, res);
        
        return res;
    }
    
    private void helper(TreeNode root, List<Integer> res) {      
        if (root.left != null) {
            helper(root.left, res);
        }
        
        res.add(root.val); // 区别就在这一行的位置
        
        if (root.right != null) {
            helper(root.right, res);
        }
    }
}
```

Time: `O(N)`，每个node走了一遍\
Space: `O(N)`，res的size&#x20;
