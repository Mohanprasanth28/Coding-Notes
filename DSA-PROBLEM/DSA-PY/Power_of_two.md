## 231mPower of two

### Problem Explanation:
     Goal:  Given an integer n, return true if it is a power of two. Otherwise, return false.
    
### Approach:

    Check if n is even:
        n != 2 return false
    If n is even:
        Iterative division:
            While n % 2 == 0
                n = n // 2
            AFter loop end:
                Return true if n is 1
                else return false
    
