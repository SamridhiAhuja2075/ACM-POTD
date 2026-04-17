## Easy Solution
```class Solution(object):
    def height(self,root,diameter):
        if not root:
            return 0
        l=self.height(root.left,diameter)
        r=self.height(root.right,diameter)
        diameter[0]=max(l+r,diameter[0])
        return 1+max(l,r)
        

    def diameterOfBinaryTree(self, root):
        diameter=[0]
        self.height(root,diameter)
        return diameter[0]
```
![alt text](image.png)