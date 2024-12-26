## 292. Nim Game

### Problem Statment:

Goal:To determine if you can win the Nim game given the number of stones n in the heap.

### Solution:

### Approach:

    - Modulo Operation:

          Check if n % 4 == 0. If true, return False.
          Otherwise, return True.

### Program:

```python
class Solution(object):
    def canWinNim(self, n):
        """
        :type n: int
        :rtype: bool
        """
        return False if (n % 4 == 0) else True
```
        
        