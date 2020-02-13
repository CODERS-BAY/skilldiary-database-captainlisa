## Diary 13.02.2020

### Foreign Key
* is an attribute, that links one relational database table with another. the foreign key in table A must be the primary key in table B (aka the table it links to)
* So a foreign key links to tables in order to get more information. For example, table A is the description of a product with serial number, name etc. now you can get more information through accessing table B with the help of the foreign key. table B contains information about the production of the article that is not included in table A.

### Normal Forms

* There are 12 normal forms, but only 5 are commonly used. 
* A **key candidate** is an attribute that *could* function as a primary key
* Normalising means that we seperate the attributes of an entity in several relation models (aka tables)
* The goal of this is to get rid of redundant information and make sure there are no anomalies within the database, e.g. wrong information
* **1. Normal Form**: 
  * is a table that is not uniformly structured. information is seperated in to the smallest, most logical attributes, e.g. the attribute "name" would be seperated into "first name" and "surname"
* **2. Normal Form**: 
  * mostly reached through the ER-Model, separates tables into smaller relation models. 
  * for every key candidate there is a new relation model created, where the specific key candidate is the primary key
  * sorts attributes to their respective entities like the ERM
  * there are no dependencies between key attributes
* **3. Normal Form**: 
  * eliminates anomalies and redundances
  * eliminates dependencies between non-key attributes, so there are no transitive dependencies left
  * for example: the postal code and the name of a place are dependent to each other and to the person. so those two attributes are outsourced into a separate relation model
 

### 3 Anomalies:
   * insert: wrong information, too much or too little information is added 
   * update: information is wrong after changing it, i.e. something got deleted or changed that shouldn't have been changed
   * delete: delete information accidental or delete too much

### Dependency:
 *  functional dependency: to every X there is a Y that depends on it.
 *  fully functional dependency: an attribute that is not a key candidate is dependent on every other attribute in the table
 *  transitive dependency: X is dependent on Y, Y is dependent on Z, therefore X is dependent on Z (meaning the dependency between non-key attributes)

