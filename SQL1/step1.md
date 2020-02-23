

`apt-get install wget ca-certificates`{{execute}}

`wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -`{{execute}}

``sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'``{{execute}}

``apt-get update``{{execute}}

``apt-get install postgresql postgresql-contrib``{{execute}}

``pg_ctlcluster 12 main start``{{execute}}

``su - postgres``{{execute}}

``psql``
