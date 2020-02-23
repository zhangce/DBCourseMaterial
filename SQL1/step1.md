
#### Installing a DBMS

We first install a DBMS in Ubuntu. Here we will install PostgreSQL 
and use it as an example.

##### Setup

Like all software, to install a DBMS, we need to set-up 
our environments and dependencies. This process is
particularly easy for installing PostgreSQL
in Ubuntu. We first step-up the `apt-get`
environment as follows:

`apt-get install wget ca-certificates`{{execute}}

`wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -`{{execute}}

``sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'``{{execute}}

``apt-get update``{{execute}}

We can now install `PostgreSQL`:

``apt-get install -y postgresql postgresql-contrib``{{execute}}

##### Start DBMS

Now we have `PostgreSQL` installed, we can start it 
by using the following command.

``pg_ctlcluster 12 main start``{{execute}}

##### Connect 

Now `PostgreSQL` is running as a service in the background and we can
connect to it using its default client `psql`. By default,
`PostgreSQL` will create a user `postgres` and it is
easier to connect to it as this user.

We first swtich the user to `postgres`

``su - postgres``{{execute}}

Runinng `psql` will connect us with the DBMS engine.

``psql``{{execute}}

We can now type some commands. For example, let's change
the password for our default user `postgres`.

``ALTER USER postgres PASSWORD 'myPassword';``{{execute}}

We can quit the `psql` program with

