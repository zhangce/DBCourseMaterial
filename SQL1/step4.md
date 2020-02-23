
#### Interact with DB from Python

Now we have a DB instance created, how can we interact with it?
There are in general two ways to interact with a DB: (1)
from external program, and (2) from a DB client.

We first look at how to interact with a DB from external program.

##### Install Dependencies

For this example, we will use Python and `psycopg2`. We first
install some dependencies.

``apt-get install -y libpq-dev python-pip``{{execute}}

``pip install psycopg2``{{execute}}

##### Interact!

Let's run Python in an interactive way

``python``{{execute}}

Import `psycopg2` which we will use to interact with the DB:

``import psycopg2``{{execute}}

We first built a "connection" to the DB we just created. One
can do that using `psycopg2.connect` and pass in the information
that our Python script can locate and authenticate into our DB.
This includes where the DBMS server is running (for this tutorial
it is on our `localhost` at port `5432`), the information 
of the user (for this tutorial it is our `postgres` user
with password `myPassword`), and the name of the DB instance
(for this tutorial it is `testdatabase`).

``connection = psycopg2.connect(user = "postgres", password = "myPassword", host = "127.0.0.1", port = "5432", database = "testdatabase")``{{execute}}

``cursor = connection.cursor()``{{execute}}

We can now execute a simple SQL queries:

``cursor.execute("SELECT * FROM Professor;")``{{execute}}

The above query will return a new Relation. One can enumerate
all tuples in this new relation by enumerate
`cursor.fetchall()` in Python:

``for l in cursor.fetchall(): print l``{{execute}}

(Remeber to hit `Enter` in the terminal!)

We see that all three tuples are now being printed out. One can
process them in Python just like any other Python objects.

We exit our Python REPL.

``exit()``{{execute}}