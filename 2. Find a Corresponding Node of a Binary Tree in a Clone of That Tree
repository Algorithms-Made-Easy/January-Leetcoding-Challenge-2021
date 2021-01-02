class Solution {
    
    TreeNode target, res;
    public final TreeNode getTargetCopy(final TreeNode original, final TreeNode cloned, final TreeNode target) {
        this.target = target;
        inorder(original,cloned);
        return res;
    }
    
    //Placeholder for the traversal methos
    public void inorder(TreeNode orig, TreeNode cloned) {
        if(orig != null) {
            //Traversal --> Inorder (L R Right)
            inorder(orig.left, cloned.left);
            if(orig==target) res = cloned;
            inorder(orig.right, cloned.right);
        }
    }
}
