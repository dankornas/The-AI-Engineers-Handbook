# Pandas DataFrames

***

### What is a DataFrame?

A Pandas DataFrame is a 2 dimensional data structure, like a 2 dimensional array, or a table with rows and columns.

#### Example

Create a simple Pandas DataFrame:

import pandas as pd

data = {\
&#x20; "calories": \[420, 380, 390],\
&#x20; "duration": \[50, 40, 45]\
}

\#load data into a DataFrame object:\
df = pd.DataFrame(data)

print(df)&#x20;

### Result

```
     calories  duration
  0       420        50
  1       380        40
  2       390        45
```

Try it Yourself »

***

### Locate Row

As you can see from the result above, the DataFrame is like a table with rows and columns.

Pandas use the `loc` attribute to return one or more specified row(s)

#### Example

Return row 0:

\#refer to the row index:\
print(df.loc\[0])

### Result

```
  calories    420
  duration     50
  Name: 0, dtype: int64
```

Try it Yourself »

**Note:** This example returns a Pandas **Series**.

#### Example

Return row 0 and 1:

\#use a list of indexes:\
print(df.loc\[\[0, 1]])

### Result

```
     calories  duration
  0       420        50
  1       380        40
```

Try it Yourself »

**Note:** When using `[]`, the result is a Pandas **DataFrame**.

***

***

### Named Indexes

With the `index` argument, you can name your own indexes.

#### Example

Add a list of names to give each row a name:

import pandas as pd

data = {\
&#x20; "calories": \[420, 380, 390],\
&#x20; "duration": \[50, 40, 45]\
}

df = pd.DataFrame(data, index = \["day1", "day2", "day3"])

print(df)&#x20;

### Result

```
        calories  duration
  day1       420        50
  day2       380        40
  day3       390        45
```

Try it Yourself »

### Locate Named Indexes

Use the named index in the `loc` attribute to return the specified row(s).

#### Example

Return "day2":

\#refer to the named index:\
print(df.loc\["day2"])

### Result

```
  calories    380
  duration     40
  Name: 0, dtype: int64
```

Try it Yourself »

***

### Load Files Into a DataFrame

If your data sets are stored in a file, Pandas can load them into a DataFrame.

#### Example

Load a comma separated file (CSV file) into a DataFrame:

import pandas as pd

df = pd.read\_csv('data.csv')

print(df)&#x20;

Try it Yourself »

You will learn more about importing files in the next chapters.

***

### Test Yourself With Exercises

\
