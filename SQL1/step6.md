``echo "5001,Databases,4,2125" > lecture.csv``{{execute}}

``echo "5041,Networks,4,2126" >> lecture.csv``{{execute}}

``echo "5043,Theory,4,2127" >> lecture.csv``{{execute}}

``cat lecture.csv``{{execute}}

``PGPASSWORD=myPassword psql -h localhost -p 5432 -U postgres testdatabase``{{execute}}

``\copy Lecture FROM '/root/lecture.csv' DELIMITER ',';``{{execute}}

``SELECT * FROM Lecture;``{{execute}}

``SELECT * FROM Professor p, Lecture l WHERE p.PersNr = l.ProfNr AND l.title = 'Databases';``{{execute}}

``\q``{{execute}}