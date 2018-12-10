***
# Problem
***

## Range Sum of BST

Given the root node of a binary search tree, return the sum of values of all nodes with value between L and R (inclusive).

The binary search tree is guaranteed to have unique values.

 

#### Example 1:

    Input: root = [10,5,15,3,7,null,18], L = 7, R = 15
    Output: 32
### Example 2:

    Input: root = [10,5,15,3,7,13,18,1,null,6], L = 6, R = 10
    Output: 23


    Note:

    The number of nodes in the tree is at most 10000.
    The final answer is guaranteed to be less than 2^31.


***
# What I learned
***
This problem was relatively simple to understand, it is just a matter of traversing the tree and finding all of the nodes that are within the range, and sum their values. This can be done the naive way by traversing the whole tree and finding the values, or by taking advantage that this is a binary search tree, and visiting the nodes that are necessary. I did not complete the code. 

   
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

    sum = 0
    
    def rangeSumBST(self, root, L, R):
        """
        :type root: TreeNode
        :type L: int
        :type R: int
        :rtype: int
        """
        
        def sumNodes(node):
            if node != None:
            
                if L <= node.val <= R:
                    sum += node.val
                if L < node.val:
                    sumNodes(node.left)
                
        
```

    

