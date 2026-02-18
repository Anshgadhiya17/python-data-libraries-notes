# 🔢 NumPy Notes (Complete Guide)

## 📌 Introduction

NumPy (Numerical Python) is a powerful Python library used for:

- Numerical computations
- Working with arrays
- Mathematical operations
- Scientific computing

It is the foundation for Pandas, Machine Learning, and Data Science libraries.

---

## 📦 Installation & Import

```bash
pip install numpy
```

```python
import numpy as np
```

---

# 🔹 Creating Arrays

## 1️⃣ From List

```python
import numpy as np

arr = np.array([1, 2, 3, 4])
print(arr)
```

Output:
```
[1 2 3 4]
```

---

## 2️⃣ 2D Array

```python
arr = np.array([[1, 2], [3, 4]])
print(arr)
```

Output:
```
[[1 2]
 [3 4]]
```

---

# 🔹 Array Properties

```python
arr = np.array([[1,2,3],[4,5,6]])

print(arr.ndim)
print(arr.shape)
print(arr.size)
print(arr.dtype)
```

Output:
```
2
(2, 3)
6
int64
```

---

# 🔹 Special Arrays

## Zeros

```python
print(np.zeros((2, 3)))
```

Output:
```
[[0. 0. 0.]
 [0. 0. 0.]]
```

---

## Ones

```python
print(np.ones((2, 2)))
```

Output:
```
[[1. 1.]
 [1. 1.]]
```

---

## Identity Matrix

```python
print(np.eye(3))
```

Output:
```
[[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]]
```

---

## Range

```python
print(np.arange(0, 10, 2))
```

Output:
```
[0 2 4 6 8]
```

---

## Linspace

```python
print(np.linspace(0, 1, 5))
```

Output:
```
[0.   0.25 0.5  0.75 1.  ]
```

---

# 🔹 Reshaping Arrays

```python
arr = np.arange(6)
print(arr.reshape(2, 3))
```

Output:
```
[[0 1 2]
 [3 4 5]]
```

Flatten:

```python
arr = np.array([[1,2],[3,4]])
print(arr.flatten())
```

Output:
```
[1 2 3 4]
```

---

# 🔹 Indexing & Slicing

```python
arr = np.array([10, 20, 30, 40])

print(arr[0])
print(arr[1:3])
```

Output:
```
10
[20 30]
```

2D Array:

```python
arr = np.array([[1,2,3],[4,5,6]])

print(arr[0, 1])
print(arr[:, 1])
```

Output:
```
2
[2 5]
```

---

# 🔹 Arithmetic Operations (Vectorized)

```python
arr = np.array([10, 20, 30])

print(arr + 5)
print(arr - 2)
print(arr * 2)
print(arr / 2)
```

Output:
```
[15 25 35]
[ 8 18 28]
[20 40 60]
[ 5. 10. 15.]
```

Array with array:

```python
a = np.array([1,2,3])
b = np.array([4,5,6])

print(a + b)
print(a * b)
```

Output:
```
[5 7 9]
[ 4 10 18]
```

---

# 🔹 Mathematical Functions

```python
arr = np.array([10, 20, 30, 40])

print(np.sum(arr))
print(np.mean(arr))
print(np.median(arr))
print(np.std(arr))
print(np.min(arr))
print(np.max(arr))
```

Output:
```
100
25.0
25.0
11.180339887498949
10
40
```

---

# 🔹 Axis Operations

```python
arr = np.array([[1,2,3],[4,5,6]])

print(np.sum(arr, axis=0))
print(np.sum(arr, axis=1))
```

Output:
```
[5 7 9]
[ 6 15]
```

---

# 🔹 Random Module

```python
print(np.random.randint(1, 10, 5))
```

Output (random every time):
```
[3 7 1 9 5]
```

---

# 🔹 Boolean Masking

```python
arr = np.array([10, 20, 30, 40])
print(arr[arr > 20])
```

Output:
```
[30 40]
```

---

# 🔹 Copy vs View

```python
a = np.array([1,2,3])
b = a.copy()

b[0] = 100
print(a)
print(b)
```

Output:
```
[1 2 3]
[100   2   3]
```

---

# 🔹 Broadcasting

```python
arr = np.array([1,2,3])
print(arr + 10)
```

Output:
```
[11 12 13]
```

---

# 🔹 Matrix Operations

```python
a = np.array([[1,2],[3,4]])
b = np.array([[5,6],[7,8]])

print(np.dot(a, b))
```

Output:
```
[[19 22]
 [43 50]]
```

Transpose:

```python
print(a.T)
```

Output:
```
[[1 3]
 [2 4]]
```

---

# 🔹 Sorting

```python
arr = np.array([30, 10, 20])
print(np.sort(arr))
```

Output:
```
[10 20 30]
```

---

# 🔹 Unique Values

```python
arr = np.array([1,2,2,3,3,3])
print(np.unique(arr))
```

Output:
```
[1 2 3]
```

---

# ✅ Why NumPy is Fast?

✔ Written in C  
✔ Uses contiguous memory  
✔ Supports vectorized operations  
✔ Avoids Python loops  

---
# 🔢 NumPy Array Manipulation

NumPy provides powerful functions to manipulate arrays efficiently.

Array manipulation includes:
✔ Reshaping  
✔ Flattening  
✔ Transposing  
✔ Joining  
✔ Splitting  
✔ Adding/Removing elements  
✔ Sorting  

---

# 📦 Import NumPy

```python
import numpy as np
```

---

# 🧱 Create Sample Array

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

print(arr)
```

---

# 📐 1️⃣ Reshape Array

Changes shape without changing data.

```python
arr = np.array([1,2,3,4,5,6])

reshaped = arr.reshape(2,3)
print(reshaped)
```

Auto reshape:

```python
arr.reshape(3, -1)
```

-1 automatically calculates dimension.

---

# 🔄 2️⃣ Flatten Array

Convert multi-dimensional array into 1D.

```python
arr = np.array([[1,2,3],[4,5,6]])

flat = arr.flatten()
print(flat)
```

Alternative:

```python
arr.ravel()
```

---

# 🔁 3️⃣ Transpose Array

Rows ↔ Columns

```python
arr = np.array([[1,2,3],[4,5,6]])

print(arr.T)
```

---

# ➕ 4️⃣ Add Elements

## Append

```python
arr = np.array([1,2,3])

new_arr = np.append(arr, 4)
print(new_arr)
```

## Insert

```python
np.insert(arr, 1, 99)
```

---

# ➖ 5️⃣ Delete Elements

```python
arr = np.array([1,2,3,4])

np.delete(arr, 1)
```

Delete row:

```python
arr = np.array([[1,2],[3,4]])
np.delete(arr, 0, axis=0)
```

axis=0 → row  
axis=1 → column  

---

# 🔗 6️⃣ Join Arrays

## Concatenate

```python
a = np.array([1,2])
b = np.array([3,4])

np.concatenate((a,b))
```

## Stack

```python
np.hstack((a,b))   # Horizontal
np.vstack((a,b))   # Vertical
```

---

# ✂ 7️⃣ Split Arrays

```python
arr = np.array([1,2,3,4,5,6])

np.split(arr, 3)
```

Horizontal split:

```python
arr = np.array([[1,2],[3,4],[5,6]])
np.vsplit(arr, 3)
```

---

# 🔍 8️⃣ Indexing & Slicing

```python
arr = np.array([10,20,30,40,50])

print(arr[0])      # First element
print(arr[1:4])    # Slice
```

2D slicing:

```python
arr = np.array([[1,2,3],
                [4,5,6]])

print(arr[0,1])    # Row 0, Col 1
print(arr[:,1])    # All rows, Col 1
```

---

# 🎭 9️⃣ Boolean Indexing

```python
arr = np.array([10,20,30,40])

print(arr[arr > 20])
```

Output:
```
[30 40]
```

---

# 🔃 🔟 Sorting

```python
arr = np.array([5,2,8,1])

print(np.sort(arr))
```

Sort 2D:

```python
arr = np.array([[3,2],[1,4]])

np.sort(arr, axis=0)
```

---

# 📊 1️⃣1️⃣ Shape & Dimension

```python
arr.shape      # Shape
arr.ndim       # Number of dimensions
arr.size       # Total elements
arr.dtype      # Data type
```

---

# 🎯 1️⃣2️⃣ Resize Array

```python
arr = np.array([1,2,3,4])

arr.resize(2,2)
print(arr)
```

---

# 🔢 1️⃣3️⃣ Unique & Count

```python
arr = np.array([1,2,2,3,3,3])

np.unique(arr)
```

With count:

```python
np.unique(arr, return_counts=True)
```

---

# 📌 1️⃣4️⃣ Reverse Array

```python
arr = np.array([1,2,3,4])

print(arr[::-1])
```

---

# 🧮 1️⃣5️⃣ Mathematical Operations

```python
arr = np.array([1,2,3])

print(arr + 2)
print(arr * 3)
print(np.sqrt(arr))
```

---

# 📊 Important Axis Concept

For 2D Array:

```
axis=0 → Row wise (Down direction)
axis=1 → Column wise (Across direction)
```

Example:

```python
arr.sum(axis=0)   # Column sum
arr.sum(axis=1)   # Row sum
```

---

# 🚀 Final Summary

✔ reshape() → Change shape  
✔ flatten() → Convert to 1D  
✔ concatenate() → Join arrays  
✔ split() → Divide array  
✔ slicing → Access data  
✔ boolean indexing → Filter data  

---

