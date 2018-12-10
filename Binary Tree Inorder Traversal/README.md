***
# Problem
***

## Binary Tree Inorder Traversal

Given a binary tree, return the inorder traversal of its nodes' values.

### Example:

    Input: [1,null,2,3]
       1
        \
         2
        /
       3

    Output: [1,3,2]
    Follow up: Recursive solution is trivial, could you do it iteratively?


***
# What I learned
***
   
I first implemented the recursive solution to try and move on to an iterative solution. I drew a small tree and tried to create an algorithm that did not use recursion. The drawing helped me visualized the algorithm and it is something I should use more often. However I could not come up with the algorithm in time. 

   
***
# Code
***

```python

# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def inorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        if root == None:
            return
        inorderTraversal(root.left)
        print(root.val)
        inorderTraversal(root.right)
```

    

