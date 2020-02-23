
``CREATE TABLE Professor(PersNr integer, Name varchar(100), Level varchar(2), Room integer, PRIMARY KEY (PersNr));``{{execute}}

``\d``{{execute}}

``CREATE TABLE Lecture (LectureID integer, Title varchar(100), CP integer, ProfNr integer, PRIMARY KEY (LectureID));``{{execute}}

``INSERT INTO Professor VALUES (2125, 'John', 'AP', 226);``{{execute}}

``SELECT * FROM Professor;``{{execute}}

``INSERT INTO Professor VALUES (2126, 'David', 'FP', 232);``{{execute}}

``INSERT INTO Professor VALUES (2127, 'Anna', 'FP', 310);``{{execute}}

``SELECT * FROM Professor;``{{execute}}

``\q``{{execute}}

``exit``{{execute}}