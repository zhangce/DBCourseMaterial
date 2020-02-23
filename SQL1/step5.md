``PGPASSWORD=myPassword psql -h localhost -p 5432 -U postgres testdatabase``{{execute}}

``SELECT * FROM Professor;``{{execute}}

``\copy Professor TO '/root/professor.csv' DELIMITER ',' CSV HEADER;``{{execute}}

``\q``{{execute}}

``ls``{{execute}}

``professor.csv``{{execute}}