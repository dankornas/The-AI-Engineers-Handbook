# Adding Records to Tables

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

To add records to a table in a database with MySQL and Python, you will first need to connect to the database using the mysql.connector.connect() function. This function takes the server connection details, such as hostname, username, and password, as arguments and returns a connection object. Here is an example of connecting to a MySQL server:

```python
import mysql.connector

# Connect to the MySQL server
cnx = mysql.connector.connect(
    host="localhost",
    user="username",
    password="password"
)
```

Once you are connected to the database, you can create a cursor object for executing SQL queries using the mysql.connector.cursor() function. This function takes the connection object as an argument and returns a cursor object that can be used to execute SQL queries. Here is an example of creating a cursor object:

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
```

## Adding Records

After creating the cursor object, you can use the INSERT SQL statement to add records to the table. This statement specifies the values to be inserted into the columns of the table. Here is an example of inserting records into a table:

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

# Insert records into the "users" table
query = "INSERT INTO users (username, password) VALUES ('user1', 'password1'), ('user2', 'password2')"
cursor.execute(query)
```

In this example, the INSERT statement is used to insert two rows into the "users" table. The "username" and "password" values are specified for each row.

After inserting records into the table, you can commit the changes to the database using the mysql.connector.commit() function. This function takes the connection object as an argument and saves the changes to the database. Here is an example of committing changes to the database:

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

# Insert records into the "users" table
query = "INSERT INTO users (username, password) VALUES ('user1', 'password1'), ('user2', 'password2')"
cursor.execute(query)

# Commit the changes to the database
cnx.commit()
```

In this example, the mysql.connector.commit() function is used to save the changes to the database after inserting records into the "users" table.

In summary, to add records to a table in a database with MySQL and Python, you will need to connect to the database, create a cursor object, use the INSERT SQL statement to insert records into the table, and commit the changes to the database using the mysql.connector.commit() function.
