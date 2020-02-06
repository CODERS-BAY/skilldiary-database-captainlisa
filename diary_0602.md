## Skill Diary Database
06.02.2020

### Why do we need databases?
Databases are needed to secure and store information and make it possible for several users to access the same data simultaneously.

### Codd's requirements
A computer scientist named Codd created a set of rules that every database has to fulfill. These include the integration of information to avoid unecessary data and repetition. Users have to be able to search for, save, add and edit data. It is required to have different user access for certain groups of users and different groups of people can view the same database but see different parts of it. The data has to be correct (e.g. data matching datatype) and it is possible to recover information.

### CRUD
means "create read update delete"

### ER-model
The Entity-Relationship-Model is a way to organize different entities (objects, like students, lecutres, etc.) with relationships to each other. With the Chen-Notation, there are different attributes (e.g. social security number, name, etc.) added to the entities to distinguish between different entities. Every entity needs a key-attribute that is a unique mark of identification (e.g. social security number, serial number, etc.).

### Datatypes
a list of some datatypes:
```varchar```, ```int```, ```bigint```, ```numeric```, ```decimal```, ```blob``` (binary large object), ```clob``` (character large object), ```float```, ```double```, ```date```, ```time```, ```timestamp```, ```boolean```, ```interval```

### Relationships
There are different relationships between entities. 
* One-to-One
* One-to-Many (Many-to-One)
* Many-to-Many
The different grades of relationships are:
* unary
* binary
* ternary

### Textual Presentation
Apart from the ER-model, there is also a way to present the data as text. Here, it is important to not only write down the entity and their attributes, but also the datatype of the certain attribute. Example:
```
Entity (Attribute1:Datatype1, Attribute2:Datatype2, ... , AttributeN:DatatypeN)
```

### Exercises
As exercises we tried to create ER-models for two different exercises, both individually and as a group