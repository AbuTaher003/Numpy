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

