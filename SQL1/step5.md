
#### Interact with DB from DB REPL

We can also directly query a DB using its built-in REPL such as `psql`.
We can connect to a DB by passing the hostname, port, username, password,
and DB name to `psql`:

``PGPASSWORD=myPassword psql -h localhost -p 5432 -U postgres testdatabase``{{execute}}

Now we are connected! We can select all tuples in the `Professor` relation

``SELECT * FROM Professor;``{{execute}}

and see the three tuples that we just inserted.

##### Getting Data out of DB (Bulk Dump)

We can get the data out of DBMS by bulk dump all tuples into a file.
The `\copy` command provides _one_ way to do it:

``\copy Professor TO '/root/professor.csv' DELIMITER ',' CSV HEADER;``{{execute}}

Now we exit the DB REPL

``\q``{{execute}}

If we do `ls` we will see that now we have a CSV file `professor.csv`
in our folder:

``ls``{{execute}}

Run `cat` and we can see its content, which is the three tupled we had in our DB.

``cat professor.csv``{{execute}}