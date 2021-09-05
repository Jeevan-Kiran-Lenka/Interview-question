Intial solution using **Divison**

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
---

Intial solution **without using Divison**

```python
def exceptI(arr):
    n = len(arr)
    
    # create a left array to store the product before the ith element
    left = [0]*n
    
    # create a right array to store the product after the ith element
    right = [0]*n
    
    # create a product array to store the product of left and right array
    product = [0]*n
    
    # Intialising the left most element of left array with 1
    left[0] = 1
    
    # Intialising the right most element of right array with 1
    right[n-1] = 1
    
    # Constructing the left array
    for i in range(1,n):
        left[i] = left[i-1] * arr[i-1]
    
    # Constructing the right array    
    for i in range(n-2, -1, -1):
        right[i] = right[i+1] * arr[i+1]
    
    # Constructing the product array by multiplying left and right array     
    for i in range(0,n):
        product[i] = left[i] * right[i]
    
    return(product)
    
# can optimise space complexity without creating a new array
        

# Driver program to test the above function
arr = [1, 2, 3, 4, 5]

ans = exceptI(arr)
print(ans)


# This code is contributed by Jeevan Kiran Lenka

```
