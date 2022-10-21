# Analyzing DataFrames

***

### Viewing the Data

One of the most used method for getting a quick overview of the DataFrame, is the `head()` method.

The `head()` method returns the headers and a specified number of rows, starting from the top.

#### Example

Get a quick overview by printing the first 10 rows of the DataFrame:

import pandas as pd

df = pd.read\_csv('data.csv')

print(df.head(10))

Try it Yourself »

In our examples we will be using a CSV file called 'data.csv'.

Download data.csv, or open data.csv in your browser.

**Note:** if the number of rows is not specified, the `head()` method will return the top 5 rows.

#### Example

Print the first 5 rows of the DataFrame:

import pandas as pd

df = pd.read\_csv('data.csv')

print(df.head())

Try it Yourself »

There is also a `tail()` method for viewing the _last_ rows of the DataFrame.

The `tail()` method returns the headers and a specified number of rows, starting from the bottom.

***

***

### Info About the Data

The DataFrames object has a method called `info()`, that gives you more information about the data set.

#### Example

Print information about the data:

print(df.info())&#x20;

### Result

```
  <class 'pandas.core.frame.DataFrame'>
  RangeIndex: 169 entries, 0 to 168
  Data columns (total 4 columns):
   #   Column    Non-Null Count  Dtype  
  ---  ------    --------------  -----  
   0   Duration  169 non-null    int64  
   1   Pulse     169 non-null    int64  
   2   Maxpulse  169 non-null    int64  
   3   Calories  164 non-null    float64
  dtypes: float64(1), int64(3)
  memory usage: 5.4 KB
  None
    
```

Try it Yourself »

### Result Explained

The result tells us there are 169 rows and 4 columns:

```
  RangeIndex: 169 entries, 0 to 168
  Data columns (total 4 columns):
```

And the name of each column, with the data type:

```
   #   Column    Non-Null Count  Dtype  
  ---  ------    --------------  -----  
   0   Duration  169 non-null    int64  
   1   Pulse     169 non-null    int64  
   2   Maxpulse  169 non-null    int64  
   3   Calories  164 non-null    float64
```

### Null Values

The `info()` method also tells us how many Non-Null values there are present in each column, and in our data set it seems like there are 164 of 169 Non-Null values in the "Calories" column.

Which means that there are 5 rows with no value at all, in the "Calories" column, for whatever reason.

Empty values, or Null values, can be bad when analyzing data, and you should consider removing rows with empty values. This is a step towards what is called _cleaning data_, and you will learn more about that in the next chapters.

***

\
