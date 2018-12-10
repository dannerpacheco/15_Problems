***
# Problem
***

## Product of Array Except Self

Given an array nums of n integers where n > 1,  return an array output such that output[i] is equal to the product of all the elements of nums except nums[i].

### Example:

    Input:  [1,2,3,4]
    Output: [24,12,8,6]
Note: Please solve it without division and in O(n).

Follow up:
    Could you solve it with constant space complexity? (The output array does not count as extra space for the purpose of space complexity analysis.)


***
# What I learned
***

At first I thought this problem was going to be trivial and easy to solve, so I started coding right away; this was my first mistake. when I got to the point in the code shown below, I got stuck. I should have run trough some examples and analyze the problem better. 


   
***
# Code
***

```python

class Solution:
    def productExceptSelf(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        output = list()
        
        for i in range(len(nums)):
            num = 
            for j in nums:
                if j != i:
                    output.append()
                    
```

    

