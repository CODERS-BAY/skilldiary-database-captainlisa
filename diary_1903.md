# Diary 19.03.2020

* SQL = Structured Query Language
* RDBMS = Relational Database Management System
* ANSI SQL = American National Standards Institute SQL, the version of SQL that is defined by the ANSI, most basic/standard set of commands for SQL
* there are other versions with specific features that may be needed,like T-SQL, MySQL
* SQL is a data manipulation language (DML) = in order to interact with the data in the database, we write statements for DBMS
* SQL is also a data definiton language (DDL) and a data control language (DCL) = it offers options to manage the database itself and control the access to tables
* for each statement in SQL there is a keyword that specifies an action, like ```SELECT``` or ```FROM``` or ```WHERE```. expressions and predicates set parameters within which to operate. a clause can look something like this:
```sql
SELECT FirstName, LastName FROM Customers WHERE LastName = 'Jenkins';
```
* Query = a statement that asks for information from the database or asks the database to do something
* Keywords are commonly written in uppercase, which is not necessary, but it helps with readability and structure
* CRUD = Create, Read, Update, Delete; basics of interacting with data
* referantial integrity = means the database will be aware of the relationship and will not let you or another user modify data in a way that violates that relationship
* First Normal Form requires that values in each cell are atomic, and that tables have no repeating groups, i.e. that every field in each table has only one value in it and that there are no columns representing repeated kinds of data for each row.
* Second Normal Form says that no value in our table should depend only on a part of a key that can be used to uniquely identify a row. This means that for every column in the table that isn't a key, each of the values must rely on only the whole key.
* Third Normal Form tells us we shouldn't be able to figure out any value in a column from a field that isn't a key. 
* Denormalization is the process of intentionally duplicating information in tables in violation of normalization rules. Denormalization is done after normalizing a database!
* with denormalization, you may gain speed, but reduce some of the consistency of the database
* PII = Personally identifiable information