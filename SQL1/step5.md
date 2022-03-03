
#### Bulk Load and Query

##### Bulk Load

We can also load data in bulk into a DB. Let's create a CSV
file with three rows:

``echo "5001,Databases,4,2125" > lecture.csv``{{execute}}

``echo "5041,Networks,4,2126" >> lecture.csv``{{execute}}

``echo "5043,Theory,4,2127" >> lecture.csv``{{execute}}

``cat lecture.csv``{{execute}}

We will load this CSV file into the `Lecture` relation.

We first connect to our DB:

``PGPASSWORD=myPassword psql -h localhost -p 5432 -U postgres testdatabase``{{execute}}

Then use the `\copy` command to load the CSV file:

``\copy Lecture FROM '/root/lecture.csv' DELIMITER ',';``{{execute}}

Now let's select all tuples in the `Lecture` relation

``SELECT * FROM Lecture;``{{execute}}

We see all three tuples inserted.

##### Query

We can now issue SQL queries. For example, if we want to find out
the professor who teaches the DB lecture, we can issue the
following query

``SELECT * FROM Professor p, Lecture l WHERE p.PersNr = l.ProfNr AND l.title = 'Databases';``{{execute}}

We see the output from DBMS makes perfect sense.

You can now issue whatever query you wants -- the world is your oyster!
When you are done, you can exit the DB REPL.

``\q``{{execute}}
