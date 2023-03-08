# Pandas Series

***

### What is a Series?

In Pandas, a Series is a one-dimensional labeled array capable of holding any data type. It is similar to a column in a spreadsheet or a SQL table. A Series can hold a variety of data types, including integers, floats, strings, and Python objects.

### Labels in a Series

One of the key features of a Series is its ability to have labels. These labels allow for quick and easy indexing of values in the Series. Labels can be any immutable data type, such as integers or strings.

### Creating a Series

You can create a Pandas Series by using the `pd.Series()` function. The simplest way to create a Series is to pass a list of values:

```python
import pandas as pd

# create a series from a list
s = pd.Series([1, 2, 3, 4, 5])

# print the series
print(s)
```

This will create a Series object with the values `[1, 2, 3, 4, 5]`. By default, Pandas will assign integer labels starting from 0 to each value in the Series.

### Creating Labels

You can also create labels for a Series by passing a second parameter to the `pd.Series()` function. This parameter should be a list or array of the same length as the values list:

```python
import pandas as pd

# create a series with labels
s = pd.Series([1, 2, 3, 4, 5], index=['a', 'b', 'c', 'd', 'e'])

# print the series
print(s)
```

In this example, we create a Series object with the values `[1, 2, 3, 4, 5]` and the labels `['a', 'b', 'c', 'd', 'e']`. You can access the values in the Series using their label, like this:

```python
# access the value with the label 'a'
print(s['a'])
```

### Key/Value Objects as Series

Another way to create a Series is to pass a dictionary of key/value pairs to the `pd.Series()` function. The keys of the dictionary will become the labels of the Series, and the values will become the values in the Series:

```python
pythonCopy codeimport pandas as pd

# create a series from a dictionary
d = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
s = pd.Series(d)

# print the series
print(s)
```

In this example, we create a dictionary with the keys `['a', 'b', 'c', 'd', 'e']` and values `[1, 2, 3, 4, 5]`. We then pass this dictionary to the `pd.Series()` function, which creates a Series object with the same keys and values.
