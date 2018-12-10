***
# Problem
***

## Jump Game

Given an array of non-negative integers, you are initially positioned at the first index of the array.

Each element in the array represents your maximum jump length at that position.

Determine if you are able to reach the last index.

### Example 1:

    Input: [2,3,1,1,4]
    Output: true
    Explanation: Jump 1 step from index 0 to 1, then 3 steps to the last index.
### Example 2:

    Input: [3,2,1,0,4]
    Output: false
    Explanation: You will always arrive at index 3 no matter what. Its maximum jump length is 0, which makes it impossible to reach the last index.


***
# What I learned
***
My approach to solving this was not very effective. I jumped straight to trying to code a solution, but I realize that my solution is far too simple. I should have understood the problem better, and then try to come up with possible solutions to it. 

   
***
# Code
***

```python

class Solution:
    def canJump(self, nums):
        """
        :type nums: List[int]
        :rtype: bool
        """
        
        next_jump = nums[0]
        
        while(True):
            if next_jump >= len(nums):
                return True
            next_jump += nums[next_jump]
            
            if next_jump == 0:
                return False
        
                    
```

    

