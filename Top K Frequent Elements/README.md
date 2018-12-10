***
# Problem
***

## Top K Frequent Elements

Given a non-empty array of integers, return the k most frequent elements.

*Example 1:*

    Input: nums = [1,1,1,2,2,3], k = 2
    Output: [1,2]
*Example 2:*

    Input: nums = [1], k = 1
    Output: [1]
*Note:*

    * You may assume k is always valid, 1 ≤ k ≤ number of unique elements.
    * Your algorithm's time complexity must be better than O(n log n), where n is the array's size.


***
# What I learned
***
    Initially I thought that for this problem we had to find all elements that repeated at leas k times, and so I built the solution above with that in mind. After my test cases did not pass and I analyzed the expected output, I realized that it was asking for a ranking of up to k elements. If I had to do it again I would ask clarifying questions to  make sure that I am solving the correct problem. 

   
***
# Code
***

```python

class Solution:
    def topKFrequent(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: List[int]
        """
        if k == 1:
            my_list = []
            for num in nums:
                if num not in my_list:
                    my_list.append(num)
            return my_list
        
        my_dict = {}
        result = []
        
        for num in nums:
            
            if num in my_dict.keys():
                my_dict[num] += 1
                if my_dict[num] >= k:
                    if num not in result:
                        result.append(num)
            else:
                my_dict[num] = 1
                
        return result
```

    

