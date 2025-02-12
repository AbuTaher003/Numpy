# Numpy

```markdown
# NumPy Code Examples

This repository contains various NumPy code examples that demonstrate how to create and manipulate arrays using NumPy functions. Each code snippet is explained with the output.

## 1. Creating a 1D Array

```python
import numpy as np

myarr = np.array([2,3,4,5,6,67], np.int32)
print(myarr)
```
**Explanation**: This creates a one-dimensional array with the specified elements. The array is initialized with integer values, and `np.int32` specifies the data type.
**Output:**
```
[ 2  3  4  5  6 67]
```

---

## 2. Modifying an Element in the Array

```python
myarr[0, 1] = 45
print(myarr)
```
**Explanation**: This changes the second element of the array to 45. We access elements in the array by using their indices.
**Output:**
```
[45  3  4  5  6 67]
```

---

## 3. Creating a 2D Array

```python
listarray = np.array([[1,2,3], [4,5,6], [7,8,9]])
print(listarray)
```
**Explanation**: This creates a two-dimensional array (matrix) with the given elements. The inner lists represent rows.
**Output:**
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

---

## 4. Array Shape and Type

```python
print(listarray.shape)  # Output: (3, 3)
print(listarray.dtype)  # Output: int32
```
**Explanation**: The `.shape` method returns the dimensions of the array, and `.dtype` provides the data type of the elements in the array.
**Output:**
```
(3, 3)
int32
```

---

## 5. Create an Array of Zeros

```python
zeros = np.zeros((2, 5))
print(zeros)
```
**Explanation**: This creates a 2x5 array filled with zeros. The `np.zeros()` function is used to initialize an array with zero values.
**Output:**
```
[[0. 0. 0. 0. 0.]
 [0. 0. 0. 0. 0.]]
```

---

## 6. Create a Range of Values

```python
rng = np.arange(15)
print(rng)
```
**Explanation**: The `np.arange()` function generates a range of values starting from 0 up to the specified number (exclusive). In this case, it generates values from 0 to 14.
**Output:**
```
[ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14]
```

---

## 7. Linearly Spaced Values

```python
lspace = np.linspace(1, 5, 12)
print(lspace)
```
**Explanation**: The `np.linspace()` function generates an array of 12 linearly spaced values between 1 and 5 (inclusive). The values are evenly distributed between the start and end points.
**Output:**
```
[1.         1.36363636 1.72727273 2.09090909 2.45454545 2.81818182
 3.18181818 3.54545455 3.90909091 4.27272727 4.63636364 5.        ]
```

---

## 8. Create an Empty Array

```python
emp = np.empty((4, 6))
print(emp)
```
**Explanation**: The `np.empty()` function creates an array without initializing the values, meaning it contains random values based on the memory content at the time of creation.
**Output:**
```
[[ 1.45636739e-311  0.00000000e+000  1.45636739e-311  0.00000000e+000
   0.00000000e+000  1.45636739e-311]
 [ 0.00000000e+000  1.45636739e-311  1.45636739e-311  0.00000000e+000
   0.00000000e+000  0.00000000e+000]
 [ 0.00000000e+000  1.45636739e-311  1.45636739e-311  0.00000000e+000
   1.45636739e-311  0.00000000e+000]
 [ 1.45636739e-311  0.00000000e+000  1.45636739e-311  1.45636739e-311
   1.45636739e-311  0.00000000e+000]]
```

---

## 9. Create an Array Like Another Array

```python
emp_like = np.empty_like(lspace)
print(emp_like)
```
**Explanation**: The `np.empty_like()` function creates an array with the same shape and type as another array (`lspace` in this case), but the values are not initialized, meaning they contain random values.
**Output:**
```
[1. 1. 1. 1. 1. 1. 1. 1. 1. 1. 1. 1.]
```

---


### 10. **Creating an Identity Matrix**

```python
import numpy as np
ide = np.identity(3)
print(ide)
```

This code creates a 3x3 identity matrix. The diagonal elements are 1, and all other elements are 0.

### 11. **Checking the Data Type of the Identity Matrix**

```python
print(ide.dtype)
```

This code prints the data type of the elements in the identity matrix, which will be `int32` by default.

### 12. **Checking the Shape of the Identity Matrix**

```python
print(ide.shape)
```

This code checks the shape of the identity matrix, which will be `(3, 3)` for a 3x3 matrix.

### 13. **Creating a Range of Numbers**

```python
arr = np.arange(99)
print(arr)
```

This code creates an array of numbers from 0 to 98 (99 elements).

### 14. **Reshaping the Array**

```python
arr = arr.reshape(3, 33)
print(arr)
```

This code reshapes the array `arr` into a 3x33 matrix. It permanently changes the shape of `arr`.

### 15. **Flattening the Array**

```python
arr = arr.ravel()
print(arr)
```

This code flattens the array `arr` into a 1-dimensional array.

### 16. **Creating a NumPy Array from a List**

```python
x = [[1, 2, 3], [4, 5, 6], [7, 1, 0]]
ar = np.array(x, np.int32)
print(ar)
```

This code creates a 3x3 NumPy array from a Python list and assigns the `int32` data type to the array.

### 17. **Summing Columns of the Array**

```python
print(ar.sum(axis=0))
```

This code calculates the sum of the elements in each column (axis 0) of the array.

### 18. **Summing Rows of the Array**

```python
print(ar.sum(axis=1))
```

This code calculates the sum of the elements in each row (axis 1) of the array.

### 19. **Transpose of the Array**

```python
print(ar.T)
```

This code transposes the array, switching its rows with columns.

### 20. **Using the Flat Iterator**

```python
for item in ar.flat:
    print(item, end=" ")
```

This code uses the `flat` iterator to iterate through all the elements in the array and print them.

### 21. **Checking the Dimensions of the Array**

```python
print(ar.ndim)
```

This code checks the number of dimensions of the array. For a 2D array, it will return `2`.

### 22. **Checking the Size of the Array**

```python
print(ar.size)
```

This code prints the total number of elements in the array, which will be `9` for the 3x3 array.

---

## 23. Creating a One-Dimensional Array

```python
import numpy as np

one = np.array([1, 4, 3, 64, 2])  # Creating a one-dimensional array
```

- This code creates a one-dimensional NumPy array named `one` with the values `[1, 4, 3, 64, 2]`.

---

## 24. Finding the Index of Maximum Element

```python
print(one.argmax())  # Returns the index of the maximum element
```

- `one.argmax()` returns the index of the maximum element in the array `one`. In this case, it will return `3` because the maximum value is `64` and it is at index `3`.

---

## 25. Finding the Index of Minimum Element

```python
print(one.argmin())  # Returns the index of the minimum element
```

- `one.argmin()` returns the index of the minimum element in the array `one`. In this case, it will return `0` because the minimum value is `1` and it is at index `0`.

---

## 26. Sorting the Array and Getting Sorted Indices

```python
print(one.argsort())  # Returns the indices that would sort the array
```

- `one.argsort()` returns the indices that would sort the array `one`. In this case, it will return `[0, 4, 2, 1, 3]`, meaning the array would be sorted as `[1, 2, 3, 4, 64]` using these indices.

---

## 27. Demonstrating the Use of Axis in `argmax()`

```python
ar = np.array([[7, 8, 9], [3, 4, 5], [2, 1, 6]])
print(ar.argmax(axis=0))  # Maximum element indices for each column
print(ar.argmax(axis=1))  # Maximum element indices for each row
```

- `ar.argmax(axis=0)` returns the indices of the maximum element for each column.
- `ar.argmax(axis=1)` returns the indices of the maximum element for each row.

---

## 28. Array Addition in NumPy

```python
ar2 = np.array([[7, 8, 9], [3, 4, 5], [2, 1, 6]])
print(ar + ar2)  # Adding two arrays element-wise
```

- This code demonstrates element-wise addition of two NumPy arrays `ar` and `ar2`. The result will be the sum of corresponding elements in the two arrays.

---

## 29. Demonstrating List Addition in Python (Without NumPy)

```python
list1 = [23, 24]
list2 = [25, 26]

print(list1 + list2)  # Just extends the list
```
# NumPy Array Operations and Insights

### 30. Square Root of Elements
```python
import numpy as np
ar = np.array([[7, 8, 9],
               [3, 4, 5],
               [2, 1, 6]])
np.sqrt(ar)
```
**Explanation:**
This computes the square root of each element in the array `ar`.

### 31. Maximum and Minimum Values in the Array
```python
ar.max()  # Finds the maximum element in the array.
ar.min()  # Finds the minimum element in the array.
```
**Explanation:**
- `ar.max()` returns the largest element in the array.
- `ar.min()` returns the smallest element in the array.

### 32. Finding Positions of Elements Greater than a Value
```python
np.where(ar > 5)
```
**Explanation:**
This returns the indices of all elements in `ar` that are greater than `5`.

### 33. Counting Non-Zero Elements
```python
np.count_nonzero(ar)
```
**Explanation:**
This counts the number of non-zero elements in the array `ar`.

### 34. Finding Non-Zero Element Positions
```python
np.nonzero(ar)
```
**Explanation:**
This returns a tuple with indices of all non-zero elements for each axis. For example:
- If `ar = [[7, 0], [3, 4]]`, `np.nonzero(ar)` returns `([0, 1, 1], [0, 0, 1])`.

### 35. Modifying Array Elements
```python
ar[1, 2] = 0
np.nonzero(ar)
```
**Explanation:**
- Before modification: The element at index `(1, 2)` was non-zero.
- After setting `ar[1, 2] = 0`, `np.nonzero(ar)` excludes this position.

### 36. Memory Comparison: Python List vs NumPy Array
```python
import sys
py_ar = [1, 2, 3, 4]  # Python list
np_ar = np.array(py_ar)  # NumPy array

# Memory used by Python list
total_memory_list = sys.getsizeof(1) * len(py_ar)

# Memory used by NumPy array
total_memory_numpy = np_ar.itemsize * np_ar.size
```
**Explanation:**
- `sys.getsizeof(1) * len(py_ar)` calculates the memory required to store the Python list.
- `np_ar.itemsize * np_ar.size` calculates the memory required to store the NumPy array.
- Example:
  - Python list may require `112 bytes`.
  - NumPy array may require `32 bytes`.

### 37. Converting NumPy Array to Python List
```python
bal = np_ar.tolist()
type(bal)
```
**Explanation:**
- `np_ar.tolist()` converts a NumPy array to a Python list.
- `type(bal)` confirms the data type of the result.

---

### Why Use NumPy?
The examples above highlight the efficiency of NumPy:
- Faster computations.
- Significant memory savings.
- Simplified operations compared to native Python lists.


- This code shows how Python lists behave when you use the `+` operator. It simply extends the list rather than performing element-wise arithmetic addition.

---


