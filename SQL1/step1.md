
#### Installing a DBMS

We first install a DBMS in Ubuntu. Here we will install PostgreSQL 
and use it as an example.

##### Dependencies

`apt-get install wget ca-certificates`{{execute}}

`wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -`{{execute}}

``sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'``{{execute}}

``apt-get update``{{execute}}

``apt-get install -y postgresql postgresql-contrib``{{execute}}

``pg_ctlcluster 12 main start``{{execute}}

``su - postgres``{{execute}}

``psql``{{execute}}

``ALTER USER postgres PASSWORD 'myPassword';``{{execute}}