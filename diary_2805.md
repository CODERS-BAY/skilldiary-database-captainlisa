# Diary 28.05.2020

## Types of databases

* embedded: when the java program and database are on the same system
* network remote: the programm is on one server, the database on another, they communicate via http
* remote: java system and the db run in the same network but in a different software
* SQLite: is the name for the local embedded database on mobile devices

## commands to create a table via java

```sql
CREATE TABLE todo (
                           todo_id INTEGER NOT NULL GENERATED ALWAYS AS IDENTITY (START WITH 1, INCREMENT BY 1),
                           todo_name varchar(50),
                           CONSTRAINT todo_id PRIMARY KEY (todo_id)
     )

CREATE TABLE task (
         task_id INTEGER NOT NULL GENERATED ALWAYS AS IDENTITY (START WITH 1, INCREMENT BY 1),
         todo_id INTEGER REFERENCES todo(todo_id),
         task_name varchar(50),
         CONSTRAINT task_id PRIMARY KEY (task_id)
     )
```
    