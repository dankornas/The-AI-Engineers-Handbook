# Create a Database

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

To create a database with MySQL and Python, you will first need to import the mysql.connector module. This module provides classes and methods for connecting to and interacting with a MySQL server. Here is an example of importing the mysql.connector module:

```python
import mysql.connector
```

### Connecting to a MySQL Server

Once the mysql.connector module is imported, you can use the mysql.connector.connect() function to connect to a MySQL server. This function takes the server connection details, such as hostname, username, and password, as arguments and returns a connection object. Here is an example of connecting to a MySQL server:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)
```

### Creating a Database

Once you are connected to the MySQL server, you can create a new database using the mysql.connector.cursor() function and the CREATE DATABASE SQL statement. This function returns a cursor object that can be used to execute SQL queries. Here is an example of creating a database:

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

# Create a new database with the name "my_database"
query = "CREATE DATABASE my_database"
cursor.execute(query)
```

### Switching to the New Database

After creating the database, you can use the mysql.connector.cursor() function and the USE SQL statement to switch to the new database. This allows you&#x20;

to execute SQL queries on the new database. Here is an example of switching to the new database:

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

# Switch to the new database
query = "USE my_database"
cursor.execute(query)
```

In this example, the mysql.connector.cursor() function is used to create a cursor object for executing SQL queries. The USE SQL statement is then used to switch to the new database "my\_database".

Once you have switched to the new database, you can create tables and insert data into the database using SQL commands. For example, you can create a table with the name "users" using the CREATE TABLE SQL statement, and then insert data into the table using the INSERT SQL statement. Here is an example of creating a table and inserting data:

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

# Switch to the new database
query = "USE my_database"
cursor
```

