# Cleaning Data

Pandas is a popular Python library used for data manipulation and analysis. It provides powerful data structures for working with tabular and time-series data. However, real-world data is often messy and needs to be cleaned before it can be analyzed. This tutorial will cover some common data cleaning techniques using Pandas.

### Introduction to Data Cleaning

Data cleaning is the process of identifying and correcting errors, inaccuracies, and inconsistencies in the data. It is an important step in data preprocessing, as it ensures that the data is accurate, complete, and ready for analysis.

Here are some common data cleaning tasks:

* Removing duplicates
* Handling missing values
* Fixing data types
* Renaming columns
* Removing unnecessary columns
* Handling outliers

In this tutorial, we will focus on removing duplicates, handling missing values, and fixing data types.

### Importing Pandas

To get started, you will need to import the Pandas library. You can do this using the following code:

```python
import pandas as pd
```

### Removing Duplicates

Duplicate data can skew analysis and lead to inaccurate results. Pandas provides a simple way to remove duplicates using the `drop_duplicates()` method. This method returns a new DataFrame with duplicate rows removed.

Here is an example of how to remove duplicates from a DataFrame:

```bash
df = pd.read_csv('data.csv')  # read in the data
df = df.drop_duplicates()  # remove duplicates
```

In the above example, we first read in the data from a CSV file using the `read_csv()` method. Then, we remove duplicates using the `drop_duplicates()` method and assign the new DataFrame back to `df`.

### Handling Missing Values

Missing values are a common problem in real-world data. Pandas provides several methods to handle missing values.

#### Dropping Rows with Missing Values

One way to handle missing values is to simply drop the rows that contain them using the `dropna()` method. This method returns a new DataFrame with rows that contain missing values removed.

Here is an example of how to drop rows with missing values:

```bash
df = pd.read_csv('data.csv')  # read in the data
df = df.dropna()  # drop rows with missing values
```

#### Filling in Missing Values

Another way to handle missing values is to fill them in with a default value using the `fillna()` method. This method returns a new DataFrame with missing values filled in.

Here is an example of how to fill in missing values:

```bash
df = pd.read_csv('data.csv')  # read in the data
df['column_name'].fillna(value, inplace=True)  # fill in missing values in column_name with value
```

In the above example, we fill in missing values in a specific column called `column_name` with a default value called `value`.

### Fixing Data Types

Pandas can sometimes misinterpret data types, especially when reading in data from external sources. To fix this, we can use the `astype()` method to convert data types.

Here is an example of how to convert data types:

```bash
df = pd.read_csv('data.csv')  # read in the data
df['column_name'] = df['column_name'].astype('int')  # convert column_name to integer
```

In the above example, we convert a specific column called `column_name` to an integer data type using the `astype()` method.

### Renaming Columns

Renaming columns is a common task in data cleaning. Pandas provides the `rename()` method to rename columns in a DataFrame.

Here is an example of how to rename columns:

```bash
df = pd.read_csv('data.csv')  # read in the data
df = df.rename(columns={'old_name': 'new_name'})  # rename column old_name to new_name
```

In the above example, we rename a column called `old_name` to `new_name` using the `rename()` method.

### Removing Unnecessary Columns

Sometimes a DataFrame may contain columns that are not needed for analysis. Pandas provides the `drop()` method to remove columns from a DataFrame.

Here is an example of how to remove columns:

```bash
df = pd.read_csv('data.csv')  # read in the data
df = df.drop(['column_name_1', 'column_name_2'], axis=1)  # remove columns column_name_1 and column_name_2
```

In the above example, we remove two columns called `column_name_1` and `column_name_2` using the `drop()` method.

### Handling Outliers

Outliers are data points that are significantly different from other data points in the dataset. Handling outliers is important for accurate analysis. Pandas provides several methods to handle outliers.

#### Detecting Outliers

One way to detect outliers is to use the `describe()` method to get summary statistics of the data. The `describe()` method returns the count, mean, standard deviation, minimum, maximum, and quartile values of the data. By looking at these values, we can identify potential outliers.

Here is an example of how to use the `describe()` method:

```bash
df = pd.read_csv('data.csv')  # read in the data
summary = df.describe()  # get summary statistics of the data
```

#### Removing Outliers

One way to remove outliers is to use the `quantile()` method to set a threshold for acceptable data values. The `quantile()` method returns the value at a specified quantile of the data.

Here is an example of how to use the `quantile()` method:

```bash
df = pd.read_csv('data.csv')  # read in the data
q1 = df['column_name'].quantile(0.25)  # get the value at the 25th percentile
q3 = df['column_name'].quantile(0.75)  # get the value at the 75th percentile
iqr = q3 - q1  # calculate the interquartile range
lower_bound = q1 - 1.5 * iqr  # calculate the lower bound
upper_bound = q3 + 1.5 * iqr  # calculate the upper bound
df = df[(df['column_name'] >= lower_bound) & (df['column_name'] <= upper_bound)]  # remove outliers
```

In the above example, we first calculate the interquartile range (IQR) of a specific column called `column_name`. Then, we calculate the lower and upper bounds using the IQR and a factor of 1.5. Finally, we remove outliers by selecting only the rows that fall within the lower and upper bounds.
