#### Install PostgreSQL

We first install PostgreSQL and start the DB

`apt-get install wget ca-certificates`{{execute}}

`wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -`{{execute}}

``sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'``{{execute}}

``apt-get update``{{execute}}

``apt-get install -y cmake postgresql-9.6 postgresql-server-dev-9.6 postgresql-plpython-9.6 postgresql-9.6-plr libkrb5-dev postgresql-client postgresql-contrib``{{execute}}

``pg_ctlcluster 12 main start``{{execute}}

``su - postgres``{{execute}}

``psql``{{execute}}

#### Install MADlib

In this course, we will use a library called MADlib



