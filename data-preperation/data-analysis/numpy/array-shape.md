# Array Shape

***

### Shape of an Array

The shape of an array is the number of elements in each dimension.

***

### Get the Shape of an Array

NumPy arrays have an attribute called `shape` that returns a tuple with each index having the number of corresponding elements.

#### Example

Print the shape of a 2-D array:

import numpy as np

arr = np.array(\[\[1, 2, 3, 4], \[5, 6, 7, 8]])

print(arr.shape)

Try it Yourself »

The example above returns `(2, 4)`, which means that the array has 2 dimensions, where the first dimension has 2 elements and the second has 4.

#### Example

Create an array with 5 dimensions using `ndmin` using a vector with values 1,2,3,4 and verify that last dimension has value 4:

import numpy as np

arr = np.array(\[1, 2, 3, 4], ndmin=5)

print(arr)\
print('shape of array :', arr.shape)

Try it Yourself »

### What does the shape tuple represent?

Integers at every index tells about the number of elements the corresponding dimension has.

In the example above at index-4 we have value 4, so we can say that 5th ( 4 + 1 th) dimension has 4 elements.

***

### Test Yourself With Exercises

### Exercise:

Use the correct NumPy syntax to check the shape of an array.

```
arr = np.array([1, 2, 3, 4, 5])

print(arr.)
```

Start the Exercise

\
