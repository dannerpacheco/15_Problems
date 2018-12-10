***
# Problem
***

## Find Bottom Left Tree Value

Given a binary tree, find the leftmost value in the last row of the tree.

Example 1:
Input:

    2
   / \
  1   3

Output:
1
Example 2: 
Input:

        1
       / \
      2   3
     /   / \
    4   5   6
       /
      7

Output:
7
***
# What I learned
***
What I first tought of finding the max depth of the tree recursively, then print the leftmost value only when at that depth. I created the method to find the depth, but for some reason I could not run it on leetcode. I believe that this solution might have worked, but it is not the most efficient one. 

   
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
    def findBottomLeftValue(self, root):
        """
        :type root: TreeNode
        :rtype: int
        """
     
        
        def findDepth(self, root):
            if root == None:
                return 0
            
            return 1 + max(findDepth(root.left), findDepth(root.right))
        
        depth = findDepth(self, root)
        
        
```

    

