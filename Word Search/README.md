***
# Problem
***

## Word Search

Given a 2D board and a word, find if the word exists in the grid.

The word can be constructed from letters of sequentially adjacent cell, where "adjacent" cells are those horizontally or vertically neighboring. The same letter cell may not be used more than once.

### Example:

    board =
    [
      ['A','B','C','E'],
      ['S','F','C','S'],
      ['A','D','E','E']
    ]

    Given word = "ABCCED", return true.
    Given word = "SEE", return true.
    Given word = "ABCB", return false.


***
# What I learned
***
For this problem I took more time to analyze it. It appeared to me that this problem can be solved by using a graph represented as an adjecency matrix, each node representing a letter. Each node can only be visited once. Then a graph search algorithm can be used to look for a path that matches the word. I did not write any code for this, but I feel that this approach should work.

   
***
# Code
***

```python

class Solution:
    def exist(self, board, word):
        """
        :type board: List[List[str]]
        :type word: str
        :rtype: bool
        """
        
```

    

