```python
def find(num,target):
        dp = {}

        def backtrack(i, cur_sum):
            if (i, cur_sum) in dp:
                return dp[(i, cur_sum)]
            
            if i == len(num):
                return 1 if cur_sum == target else 0
            
            dp[(i, cur_sum)] = (
                backtrack(i + 1, cur_sum + num[i]) +  
                backtrack(i + 1, cur_sum - num[i])    
            )
            return dp[(i, cur_sum)]
        
        return backtrack(0, 0)
print(find([1,1,1],2))
```