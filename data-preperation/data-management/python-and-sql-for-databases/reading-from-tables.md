# Reading from Tables

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Select From a Table

To read from tables in a database with MySQL and Python, you will first need to connect to the database using the mysql.connector.connect() function and create a cursor object using the mysql.connector.cursor() function. Then, you can use the SELECT SQL statement to read from the table. Here is an example of reading from a table:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.cursor()

# Read from the "users" table
query = "SELECT * FROM users"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to read from the "users" table and print the rows returned from the query to the console.

## Selecting Columns

To select specific columns from a table in a database with MySQL and Python, you will need to use the SELECT SQL statement and specify the columns to be returned from the table. Here is an example of selecting specific columns from a table:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.cursor()

# Select specific columns from the "users" table
query = "SELECT id, username FROM users"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to select the "id" and "username" columns from the "users" table. The rows returned from the query are then printed to the console.

To specify the columns to be returned from the table, you can list the column names separated by commas in the SELECT statement. In the example above, the "id" and "username" columns are selected from the "users" table.

## Using the `fetchone()` method

To use the fetch method to retrieve records from a table in a database with MySQL and Python, you will first need to connect to the database using the mysql.connector.connect() function and create a cursor object using the mysql.connector.cursor() function. Then, you can use the SELECT SQL statement to read from the table and call the fetch method on the cursor object to retrieve the records.

Here is an example of using the fetch method to retrieve records from a table:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.cursor()

# Select specific columns from the "users" table
query = "SELECT * FROM users"
cursor.execute(query)

# Fetch the first record from the result set
row = cursor.fetchone()

# Print the row
print(row)

# Fetch the next record from the result set
row = cursor.fetchone()

# Print the row
print(row)
```

In this example, the SELECT statement is used to read from the "users" table. The cursor.fetchone() method is then called to retrieve the first record from the result set. This method returns the first row from the result set and moves the cursor to the next row. The cursor.fetchone() method is called again to retrieve the next row from the result set.

The cursor.fetchone() method can be called repeatedly to retrieve each row from the result set one by one. This method is useful when working with large result sets where you want to retrieve the records in small batches to avoid running out of memory.

## Limit the returned results

To limit the number of records returned from a table in a database with MySQL and Python, you can use the LIMIT clause in the SELECT SQL statement. This clause specifies the maximum number of records to be returned from the table. Here is an example of using the LIMIT clause to limit the number of records returned from a table:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.cursor()

# Select specific columns from the "users" table
query = "SELECT * FROM users LIMIT 10"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to read from the "users" table and the LIMIT clause is used to specify that only the first 10 records should be returned from the table. The rows returned from the query are then printed to the console.

The LIMIT clause can be combined with the OFFSET clause to specify the number of records to skip before returning the records. This is useful when paginating the result set and only retrieving a certain number of records at a time. Here is an example of using the OFFSET clause with the LIMIT clause:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.cursor()

# Select specific columns from the "users" table
query = "SELECT * FROM users LIMIT 10 OFFSET 10"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

## Start From Another Position

To start from a specific position when retrieving records from a table in a database with MySQL and Python, you can use the OFFSET clause in the SELECT SQL statement. This clause specifies the number of records to skip before returning the records from the table. Here is an example of using the OFFSET clause to start from a specific position when retrieving records from a table:

```python
Copy codeimport mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.cursor()

# Select specific columns from the "users" table
query = "SELECT * FROM users OFFSET 10"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to read from the "users" table and the OFFSET clause is used to specify that the first 10 records should be skipped before returning the records from the table. The rows returned from the query are then printed to the console.

The OFFSET clause can be combined with the LIMIT clause to specify the maximum number of records to be returned from the table. This is useful when paginating the result set and only retrieving a certain number of records at a time. Here is an example of using the LIMIT clause with the OFFSET clause:

```python
Copy codeimport mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)

# Create a cursor object for executing SQL queries
cursor = cnx.
```
