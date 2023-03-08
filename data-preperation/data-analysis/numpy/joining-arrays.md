# Joining Arrays

### Joining arrays

Joining arrays in NumPy refers to combining two or more arrays into a single array. There are several ways to join arrays in NumPy, including concatenation, stacking, and hstack and vstack functions.

### Joining Numpy Arrays

To join two or more arrays in NumPy, we can use the `concatenate()` function. This function takes a sequence of arrays along with an optional axis parameter that specifies the axis along which the arrays will be joined.

```python
# Joining two arrays
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr = np.concatenate((arr1, arr2))
print(arr)
```

Output:

```csharp
[1 2 3 4 5 6]
```

In this example, we first create two 1D arrays `arr1` and `arr2`, and then join them using the `concatenate()` function.

### Joining Arrays Using Stack Functions

NumPy provides several stack functions that allow us to join arrays along different axes.

### **Stacking Along Rows**

To stack arrays along rows, we can use the `hstack()` function. This function takes a sequence of arrays and stacks them horizontally.

```python
# Stacking along rows
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr = np.hstack((arr1, arr2))
print(arr)
```

Output:

```csharp
[1 2 3 4 5 6]
```

In this example, we first create two 1D arrays `arr1` and `arr2`, and then stack them horizontally using the `hstack()` function.

### **Stacking Along Columns**

To stack arrays along columns, we can use the `vstack()` function. This function takes a sequence of arrays and stacks them vertically.

```python
# Stacking along columns
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr = np.vstack((arr1, arr2))
print(arr)
```

Output:

```lua
[[1 2 3]
 [4 5 6]]
```

In this example, we first create two 1D arrays `arr1` and `arr2`, and then stack them vertically using the `vstack()` function.

### **Stacking Along Height (depth)**

To stack arrays along the third axis, we can use the `dstack()` function. This function takes a sequence of arrays and stacks them depth-wise.

```python
# Stacking along height (depth)
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr = np.dstack((arr1, arr2))
print(arr)
```

Output:

```lua
[[[1 4]
  [2 5]
  [3 6]]]
```

In this example, we first create two 1D arrays `arr1` and `arr2`, and then stack them along the third axis using the `dstack()` function.

In summary, joining arrays in NumPy can be accomplished using various methods, including concatenation, stacking, hstack and vstack functions. By using these functions, we can combine arrays in different ways depending on the desired output.
