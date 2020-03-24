# Diary 24.03.2020

## Database Development Life Cycle
1. Planning: what is the goal of the db? what does it need to accomplish those goals? How long will it take and how much money is it going to cost?
2. Requirement gathering: determining the tasks that the db is expected to perform, special needs
3. Conceptual design: organizing the data into relational tables
4. Logical design: determine constraints and rules of the db
5. Physical design: translate the design plan into your RDBMS
6. Construction: built the database components inside the RDBMS
7. Implementation and rollout: installing the database on the clients machines, training users
8. Ongoing support: continue to work on it, fix bugs, implement new features

## Relational Database Theory
* Open/Closed Principle: is a rule of designing databases that states that tables should be open for extension, but closed for modification
* "scope creep": when new features and enhancements keep getting added to the project, that were not part of the innitial plan.
* A mission statement helps to avoid this. 
* OLAP: Online analytical processing
* OLTP: Online transactional processing
* you can specify a character set for your database. the usual charset (for MySQL) is latin1, but some people recommend utf-8. you specify this at the very beginning, when creating the database:
```sql
CREATE DATABASE IF NOT EXISTS my_database DEFAULT CHARACTER SET utf8;
```
* Collation is the ordering of a character set. It is tied to the character set itself. Many of the charsets have corresponding collations with descriptions in the MySQL manual.
  * ci = case insensitive
  * cs = case sensitive
  * default is case insensitive