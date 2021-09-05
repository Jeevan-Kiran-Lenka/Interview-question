Inatial solution using Divison

```python
def excepti(arr):
    n = len(arr)
    product = 1
    # newarr = [0]*n
    for i in range(0,n):
        product *= arr[i]
    
    for i in range(0,n):
        arr[i] = product//arr[i]
    
    return(arr)
    
# can optimise space complexity without creating a new array
        

# Driver program to test the above function
arr = [1, 2, 3, 4, 5]

ans = excepti(arr)
print(ans)


# This code is contributed by Jeevan Kiran Lenka
```
