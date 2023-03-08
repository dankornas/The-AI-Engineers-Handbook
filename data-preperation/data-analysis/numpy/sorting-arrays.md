# Sorting Arrays

### Sorting Arrays

NumPy provides several functions to sort arrays. These functions include:

* `sort()`: Sorts an array in-place.
* `argsort()`: Returns the indices that would sort an array.
* `lexsort()`: Performs an indirect sort on multiple keys.
* `partition()`: Rearranges the array in such a way that the first `k` elements are the smallest elements in the array, in no particular order.
* `argpartition()`: Returns the indices that would partition an array.

### **`sort()`**

The `sort()` function sorts an array in-place. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([3, 2, 1, 4, 6, 5])

# Sort the array
arr.sort()

# Print the sorted array
print(arr)
```

In this example, we create a 1-dimensional array with the values `[3, 2, 1, 4, 6, 5]`. We then use the `sort()` function to sort the array in-place. The output of the code will be:

```csharp
[1 2 3 4 5 6]
```

### **`argsort()`**

The `argsort()` function returns the indices that would sort an array. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([3, 2, 1, 4, 6, 5])

# Get the indices that would sort the array
indices = np.argsort(arr)

# Print the indices
print(indices)
```

In this example, we create a 1-dimensional array with the values `[3, 2, 1, 4, 6, 5]`. We then use the `argsort()` function to get the indices that would sort the array. The output of the code will be:

```csharp
[2 1 0 3 5 4]
```

### **`lexsort()`**

The `lexsort()` function performs an indirect sort on multiple keys. Here's an example:

```python
import numpy as np

# Create 2 1-dimensional arrays
last_name = np.array(['Smith', 'Jones', 'Lee', 'Lee', 'Brown'])
first_name = np.array(['John', 'Alice', 'Emily', 'David', 'Rachel'])

# Get the indices that would sort the arrays together
indices = np.lexsort((first_name, last_name))

# Print the sorted names
print(last_name[indices], first_name[indices])
```

In this example, we create two 1-dimensional arrays: `last_name` and `first_name`. We then use the `lexsort()` function to get the indices that would sort the arrays together. The output of the code will be:

```css
['Brown' 'Jones' 'Lee' 'Lee' 'Smith'] ['Rachel' 'Alice' 'Emily' 'David' 'John']
```

### **`partition()`**

The `partition()` function rearranges the array in such a way that the first `k` elements are the smallest elements in the array, in no particular order. The remaining elements are placed after the `k`th element in the array. Here's an example:

```python
pythonCopy codeimport numpy as np

# Create a 1-dimensional array
arr = np.array([3, 2, 1, 4, 6, 5])

# Partition the array
np.partition(arr, 3)

# Print the partitioned array
print(arr)
```

In this example, we create a 1-dimensional array with the values \`\[3, 2, 1, 4, 6, 5]`. We then use the` partition()\` function to rearrange the array such that the first 3 elements are the smallest elements in the array, in no particular order. The remaining elements are placed after the 3rd element in the array. The output of the code will be:

```csharp
[2 1 3 4 6 5]
```

### **`argpartition()`**

The `argpartition()` function returns the indices that would partition an array. Here's an example:

```python
import numpy as np

# Create a 1-dimensional array
arr = np.array([3, 2, 1, 4, 6, 5])

# Get the indices that would partition the array
indices = np.argpartition(arr, 3)

# Print the partitioned indices
print(indices)
```

In this example, we create a 1-dimensional array with the values `[3, 2, 1, 4, 6, 5]`. We then use the `argpartition()` function to get the indices that would partition the array, such that the first 3 elements are the smallest elements in the array, in no particular order. The remaining elements are placed after the 3rd element in the array. The output of the code will be:

```csharp
[2 1 0 3 4 5]
```

These are some of the most common functions used for sorting arrays in NumPy. They are useful for many applications, such as data analysis, machine learning, and scientific computing.
