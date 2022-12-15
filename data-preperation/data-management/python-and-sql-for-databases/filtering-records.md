# Filtering Records

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Select With a Filter

To filter the records returned from a table in a database with MySQL and Python, you can use the WHERE clause in the SELECT SQL statement. This clause specifies the conditions that must be met for the records to be returned from the table. Here is an example of using the WHERE clause to filter the records returned from a table:

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
query = "SELECT * FROM users WHERE username = 'user1'"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to read from the "users" table and the WHERE clause is used to filter the records by the "username" column. Only records with a "username" value of "user1" will be returned from the table. The rows returned from the query are then printed to the console.

The WHERE clause can be used with various comparison operators, such as =, >, <, >=, <=, etc., to specify the conditions for filtering the records. You can also use the AND and OR keywords to combine multiple conditions in the WHERE clause. Here is an example of using multiple conditions in the WHERE clause:

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
query = "SELECT * FROM users WHERE username = 'user1' AND password = 'password1'"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to read from the "users" table and the WHERE clause is used to filter the records by the "username" and "password" columns. Only records with a "username" value of "user1" and a "password" value of "password1" will be returned from the table. The rows returned from the query are then printed to the console.

## Wildcard Characters

To use wildcard characters in the WHERE clause of the SELECT SQL statement in a database with MySQL and Python, you can use the % character to match any string of zero or more characters. This character can be used in the middle, at the beginning, or at the end of the string to be matched.

Here is an example of using the % wildcard character in the WHERE clause:

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
query = "SELECT * FROM users WHERE username LIKE '%user%'"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the % wildcard character is used to match any "username" value that contains the string "user". The rows returned from the query are then printed to the console.

## Prevent SQL Injection

When the user provides query values, you should escape the values.

This is done to avoid SQL injections, a frequent web hacking technique used to destroy or exploit your database. The mysql.connector module has methods to escape query values.

Escape query values by using the placholder `%s` method:

```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address = %s"
adr = ("Yellow Garden 2", )

mycursor.execute(sql, adr)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```



{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
