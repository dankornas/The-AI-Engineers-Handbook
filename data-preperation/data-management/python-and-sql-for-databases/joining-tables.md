# Joining Tables

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Join Two or More Tables

To join two or more tables in a database with MySQL and Python, you can use the JOIN clause in the SELECT SQL statement. This clause specifies the tables to be joined and the columns that are used for matching records in the tables.

Here is an example of using the JOIN clause to join two tables:

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

# Join the "users" and "posts" tables
query = "SELECT u.username, p.title FROM users AS u INNER JOIN posts AS p ON u.id = p.user_id"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to join the "users" and "posts" tables. The JOIN clause is used to specify the tables to be joined (users and posts) and the columns that are used for matching records in the tables (id and user\_id). The rows returned from the query are then printed to the console.

## LEFT JOIN

To use a left join to join two tables in a database with MySQL and Python, you can use the LEFT JOIN keyword in the JOIN clause of the SELECT SQL statement. This keyword specifies that all the records from the left table (the first table specified in the FROM clause) will be included in the result set, even if there are no matching records in the right table (the second table specified in the FROM clause).

Here is an example of using a left join to join two tables:

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

# Join the "users" and "posts" tables using a left join
query = "SELECT u.username, p.title FROM users AS u LEFT JOIN posts AS p ON u.id = p.user_id"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to join the "users" and "posts" tables using a left join. The LEFT JOIN keyword is used to specify that all the records from the "users" table will be included in the result set, even if there are no matching records in the "posts" table. The rows returned from the query are then printed to the console.

## RIGHT JOIN

To use a right join to join two tables in a database with MySQL and Python, you can use the RIGHT JOIN keyword in the JOIN clause of the SELECT SQL statement. This keyword specifies that all the records from the right table (the second table specified in the FROM clause) will be included in the result set, even if there are no matching records in the left table (the first table specified in the FROM clause).

Here is an example of using a right join to join two tables:

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

# Join the "users" and "posts" tables using a right join
query = "SELECT u.username, p.title FROM users AS u RIGHT JOIN posts AS p ON u.id = p.user_id"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to join the "users" and "posts" tables using a right join. The RIGHT JOIN keyword is used to specify that all the records from the "posts" table will be included in the result set, even if there are no matching records in the "users" table. The rows returned from the query are then printed to the console.
