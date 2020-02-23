
``apt-get install -y libpq-dev python-pip``{{execute}}

``pip install psycopg2``{{execute}}

``python``{{execute}}

``import psycopg2``{{execute}}

``connection = psycopg2.connect(user = "postgres", password = "myPassword", host = "127.0.0.1", port = "5432", database = "testdatabase")``{{execute}}

``cursor = connection.cursor()``{{execute}}

``cursor.execute("SELECT * FROM Professor;")``{{execute}}

``for l in cursor.fetchall(): print l``{{execute}}

``exit()``{{execute}}