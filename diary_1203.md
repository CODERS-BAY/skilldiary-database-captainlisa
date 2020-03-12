# Diary 12.03.2020

## XAMPP & SQL & Stuffs
* conceptual scheme = ERD
* logical scheme = relational model
* referential integrity = the accuracy of relationships
* SQL stands for Structured Query Language and is based on relational algebra
* DDL(data definition language), DML(data management language) and DCL(data control language)
* constraints are conditions, e.g. NOT NULL, CHECK, UNIQUE, PRIMARY KEY, FOREIGN KEY (attribute) REFERENCES TABLE (attribute)
* creating a table:
  ```
  CREATE TABLE Professors (Name VARCHAR(32), PRIMARY KEY (Name));

  CREATE TABLE IF NOT EXISTS Professoren (Name VARCHAR(32) NOT NULL, Personsnr INT(8), PRIMARY KEY(Personsnr));

  CREATE TABLE IF NOT EXISTS Vorlesungen
  (Name VARCHAR(32), SWS INT(4), GelesenVon INT(8), PRIMARY KEY (Name), FOREIGN KEY (GelesenVon) REFERENCES Professoren(Personsnr));
  ```
* altering a table:
  ```
  ALTER TABLE Professoren ADD (Titel VARCHAR(30));
  ALTER TABLE Professoren MODIFY (Titel VARCHAR(40));
  ALTER TABLE Professoren DROP COLUMN Titel;
  ```
* deleting a table:
  ```
  DROP TABLE Professoren;
  DROP TABLE Professoren CASCADE;
  ```
* with ```insert into Table values (A1, A2, ...)``` you can add attributes to your table
* another code:
  ```
  UPDATE table SET A1 = V1 where CONDITION;
  ```