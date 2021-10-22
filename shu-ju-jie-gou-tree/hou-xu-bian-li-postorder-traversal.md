# 后序遍历 Post-order traversal

原题地址：[https://leetcode.com/problems/binary-tree-postorder-traversal/](https://leetcode.com/problems/binary-tree-postorder-traversal/)

### 后序遍历 Post-order：左→右→根 （`Bottom up`）



Post-order是先走左child，再走右child，最后把root加进去；

```
class Solution {
    public List<Integer> postorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<>();
        if (root == null) return res;
        
        helper(root, res);
        
        return res;
    }
    
    private void helper(TreeNode root, List<Integer> res) {      
        if (root.left != null) {
            helper(root.left, res);
        }
        
        if (root.right != null) {
            helper(root.right, res);
        }
                
        res.add(root.val); // 区别就在这一行的位置
    }
}
```

Time: `O(N)`，每个node走了一遍\
Space: `O(N)`，res的size&#x20;
