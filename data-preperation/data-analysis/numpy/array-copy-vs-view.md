# Array Copy vs View

***

### The Difference Between Copy and View

The main difference between a copy and a view of an array is that the copy is a new array, and the view is just a view of the original array.

The copy _owns_ the data and any changes made to the copy will not affect original array, and any changes made to the original array will not affect the copy.

The view _does not own_ the data and any changes made to the view will affect the original array, and any changes made to the original array will affect the view.

***

### COPY:

#### Example

Make a copy, change the original array, and display both arrays:

import numpy as np

arr = np.array(\[1, 2, 3, 4, 5])\
x = arr.copy()\
arr\[0] = 42

print(arr)\
print(x)

Try it Yourself »

The copy SHOULD NOT be affected by the changes made to the original array.

***

### VIEW:

#### Example

Make a view, change the original array, and display both arrays:

import numpy as np

arr = np.array(\[1, 2, 3, 4, 5])\
x = arr.view()\
arr\[0] = 42

print(arr)\
print(x)

Try it Yourself »

The view SHOULD be affected by the changes made to the original array.

#### Make Changes in the VIEW:

#### Example

Make a view, change the view, and display both arrays:

import numpy as np

arr = np.array(\[1, 2, 3, 4, 5])\
x = arr.view()\
x\[0] = 31

print(arr)\
print(x)

Try it Yourself »

The original array SHOULD be affected by the changes made to the view.

***

***

### Check if Array Owns its Data

As mentioned above, copies _owns_ the data, and views _does not own_ the data, but how can we check this?

Every NumPy array has the attribute `base` that returns `None` if the array owns the data.

Otherwise, the `base`  attribute refers to the original object.

#### Example

Print the value of the base attribute to check if an array owns it's data or not:

import numpy as np

arr = np.array(\[1, 2, 3, 4, 5])

x = arr.copy()\
y = arr.view()

print(x.base)\
print(y.base)

Try it Yourself »

The copy returns `None`.\
The view returns the original array.

***

### Test Yourself With Exercises

### Exercise:

Use the correct method to make a copy of the array.

```
arr = np.array([1, 2, 3, 4, 5])

x = arr.
```

Start the Exercise

\
