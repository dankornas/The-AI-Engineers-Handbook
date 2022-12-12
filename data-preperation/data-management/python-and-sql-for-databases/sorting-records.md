# Sorting Records

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

To sort the records returned from a table in a database with MySQL and Python, you can use the ORDER BY clause in the SELECT SQL statement. This clause specifies the column or columns to be used for sorting the records and the sorting order (ascending or descending).

Here is an example of using the ORDER BY clause to sort the records returned from a table:

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
query = "SELECT * FROM users ORDER BY username ASC"
cursor.execute(query)

# Print the rows returned from the query
for row in cursor.fetchall():
    print(row)
```

In this example, the SELECT statement is used to read from the "users" table and the ORDER BY clause is used to sort the records by the "username" column in ascending order. The rows returned from the query are then printed to the console.

The ORDER BY clause can be used with the DESC keyword to sort the records in descending order. Here is an example of using the DESC keyword in the ORDER BY clause:

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
query
```

In this example, the SELECT statement is used to read from the "users" table and the ORDER BY clause is used with the DESC keyword to sort the records by the "username" column in descending order. The rows returned from the query are then printed to the console.

{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
