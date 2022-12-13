# Joining Tables

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Join Two or More Tables

You can combine rows from two or more tables, based on a related column between them, by using a JOIN statement.

Consider you have a "users" table and a "products" table:

{% code title="users table" %}
```
{ id: 1, name: 'John', fav: 154},
{ id: 2, name: 'Peter', fav: 154},
{ id: 3, name: 'Amy', fav: 155},
{ id: 4, name: 'Hannah', fav:},
{ id: 5, name: 'Michael', fav:}
```
{% endcode %}

{% code title="products table" %}
```
{ id: 154, name: 'Chocolate Heaven' },
{ id: 155, name: 'Tasty Lemons' },
{ id: 156, name: 'Vanilla Dreams' }
```
{% endcode %}

These two tables can be combined by using users' `fav` field and products' `id` field.

Join users and products to see the name of the users favorite product:

```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  INNER JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)

### RESULT ###
# ('John', 'Chocolate Heaven')
# ('Peter', 'Chocolate Heaven')
# ('Amy', 'Tasty Lemon')
```

You can use JOIN instead of INNER JOIN. They will both give you the same result.

## LEFT JOIN

Hannah and Michael were excluded from the result in the preceding example because INNER JOIN only displays data when there is a match.

Use the LEFT JOIN statement to show all users, even if they don't have a favorite product.

Select all users and their favorite product:

<pre class="language-python"><code class="lang-python">import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  LEFT JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)

  
### RESULT ###
<strong># ('John', 'Chocolate Heaven')
</strong># ('Peter', 'Chocolate Heaven')
# ('Amy', 'Tasty Lemon')
# ('Hannah', None)
# ('Michael', None)</code></pre>

## RIGHT JOIN

Use the RIGHT JOIN statement to return all items and people who have them as their favorite, even if no user has them as their favorite.

Select all products, and the user(s) who have them as their favorite:

<pre class="language-python"><code class="lang-python">import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="myusername",
  password="mypassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  RIGHT JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)

### RESULT ###
# ('John', 'Chocolate Heaven')
<strong># ('Peter', 'Chocolate Heaven')
</strong># ('Amy', 'Tasty Lemon')
# (None, 'Vanilla Dreams')</code></pre>



{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
