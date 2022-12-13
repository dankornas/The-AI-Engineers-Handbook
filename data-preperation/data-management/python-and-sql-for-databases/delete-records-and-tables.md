# Delete Records & Tables

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Deleting a Record

To delete records from a table in a database with MySQL and Python, you can use the DELETE SQL statement. This statement specifies the table from which the records should be deleted and the conditions for selecting the records to be deleted.

Here is an example of using the DELETE SQL statement to delete records from a table:

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

# Delete records from the "users" table
query = "DELETE FROM users WHERE username = 'user1'"
cursor.execute(query)

# Save the changes
cnx.commit()
```

In this example, the DELETE statement is used to delete records from the "users" table where the "username" column has a value of "user1". The changes are then saved using the cnx.commit() method.

## Prevent SQL Injection

It is recommended to escape the values of any query, including delete commands.

This is done to avoid SQL injections, a frequent web hacking technique used to destroy or exploit your database. The placeholder `%s` is used by the mysql.connector module to escape values in the delete statement.

Escape values by using the placeholder `%s` method:

```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DELETE FROM customers WHERE address = %s"
adr = ("Yellow Garden 2", )

mycursor.execute(sql, adr)

mydb.commit()

print(mycursor.rowcount, "record(s) deleted")
```

## Delete a Table

To delete an entire table from a database with MySQL and Python, you can use the DROP TABLE SQL statement. This statement specifies the name of the table to be deleted.

Here is an example of using the DROP TABLE statement to delete a table:

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

# Delete the "users" table
query = "DROP TABLE users"
cursor.execute(query)

# Save the changes
cnx.commit()
```

In this example, the DROP TABLE statement is used to delete the "users" table from the database. The changes are then saved using the cnx.commit() method.

## Delete a Table ONLY IF it Exists

To delete an entire table from a database with MySQL and Python only if it exists, you can use the IF EXISTS keyword in the DROP TABLE SQL statement. This keyword will check if the table exists before attempting to delete it, and will only delete the table if it exists.

Here is an example of using the IF EXISTS keyword in the DROP TABLE statement to delete a table:

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

# Delete the "users" table only if it exists
query = "DROP TABLE IF EXISTS users"
cursor.execute(query)

# Save the changes
cnx.commit()
```

In this example, the DROP TABLE statement is used with the IF EXISTS keyword to delete the "users" table from the database only if it exists. The changes are then saved using the cnx.commit() method.

{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
