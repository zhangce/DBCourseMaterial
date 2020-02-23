
#### Manipulate Database Instances

We can now use the DDL and DML statements we learned in our class to manipulate 
our test database instance `testdatabase`.

The command `\d` lists all existing relations in our database instance.

``\d``{{execute}}

We can see that there is nothing here at the moment.

We can create a `Professor` relation as follows.

``CREATE TABLE Professor(PersNr integer, Name varchar(100), Level varchar(2), Room integer, PRIMARY KEY (PersNr));``{{execute}}

Running `\d` again

``\d``{{execute}}

and we can see that now we have the `Professor` relation.
We can create the `Lecture` relation similarly.

``CREATE TABLE Lecture (LectureID integer, Title varchar(100), CP integer, ProfNr integer, PRIMARY KEY (LectureID));``{{execute}}

We can insert some tuples into our relations, e.g.,

``INSERT INTO Professor VALUES (2125, 'John', 'AP', 226);``{{execute}}

If we run the following query, which selects all tuples in the `Professor` relation

``SELECT * FROM Professor;``{{execute}}

we can see the tuple that we just inserted into the relation, and nothing else.
Let's insrt two more tuples

``INSERT INTO Professor VALUES (2126, 'David', 'FP', 232);``{{execute}}

``INSERT INTO Professor VALUES (2127, 'Anna', 'FP', 310);``{{execute}}

If we select all tuples in `Professor`

``SELECT * FROM Professor;``{{execute}}

we can see all three tuples returned by the system.

Let's now exit the DBMS and also log out as the user `postgres`:

``\q``{{execute}}

``exit``{{execute}}