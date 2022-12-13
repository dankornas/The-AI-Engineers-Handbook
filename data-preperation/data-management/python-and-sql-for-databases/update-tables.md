# Update Tables

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Update Table

To update records in a table in a database with MySQL and Python, you can use the UPDATE SQL statement. This statement specifies the table to be updated, the columns to be updated, and the new values for the columns. It also specifies the conditions for selecting the records to be updated.

Here is an example of using the UPDATE SQL statement to update records in a table:

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

# Update the "username" and "password" columns in the "users" table
query = "UPDATE users SET username = 'user2', password = 'password2' WHERE username = 'user1'"
cursor.execute(query)

# Save the changes
cnx.commit()
```

In this example, the UPDATE statement is used to update the "username" and "password" columns in the "users" table. The new values for the columns are "user2" and "password2", and the records to be updated are selected using the WHERE clause. The changes are then saved using the cnx.commit() method.

## Prevent SQL Injection

It is recommended to escape the values of any query, including update statements.

This is done to avoid SQL injections, a frequent web hacking technique used to destroy or exploit your database.

The placeholder%s is used by the mysql.connector module to escape values in the delete statement.

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

sql = "UPDATE customers SET address = %s WHERE address = %s"
val = ("Valley 345", "Canyon 123")

mycursor.execute(sql, val)

mydb.commit()

print(mycursor.rowcount, "record(s) affected")
```



{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
