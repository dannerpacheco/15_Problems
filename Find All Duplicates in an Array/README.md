***
# Problem
***

## Find All Duplicates in an Array

Given an array of integers, 1 ≤ a[i] ≤ n (n = size of array), some elements appear twice and others appear once.

Find all the elements that appear twice in this array.

Could you do it without extra space and in O(n) runtime?

### Example:
    Input:
    [4,3,2,7,8,2,3,1]

    Output:
    [2,3]


***
# What I learned
***

Thanks to my previous experience dealing with this type of problem, I was able to solve this problem. I identified that I should use a dictionary to make things go faster, and to not use nested loops so that it won't take more time. I would like to solve this problem without using the extra space, but I will come back to that later. 


   
***
# Code
***

```python

class Solution:
    def findDuplicates(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        my_dict = dict()
        
        for num in nums:
            if num in my_dict.keys():
                my_dict[num] += 1
            else:
                my_dict[num] = 1
        
        my_list = list()
        
        for key, value in my_dict.items():
            if value == 2:
                my_list.append(key)
                
        return my_list
            
                    
```

    

