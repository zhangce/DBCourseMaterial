
#### Create a Database

Now we are connected to our DBMS, we can use the following
command to list all existing database instances:

``\l``{{execute}}

We see that there are three databaes instances already
there. Let's create a new one for this tutorial with 
the name `testdatabase`. We can use the `CREATE DATABASE`
command for this purpose:

``CREATE DATABASE testdatabase;``{{execute}}

Now let's run `\l` again

``\l``{{execute}}

and we can see that we now have three database instances.
We can use `\c` to connect to `testdatabase`.

``\c testdatabase``{{execute}}
