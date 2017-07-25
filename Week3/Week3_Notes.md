# Week 3 Notes
## Relational Model and SQL

### Data Model
Integrated collection of concepts for
    - describing data
    - relationships on the data
    - constraints on the data
    - describing finns awesomeness
- It doesn't matter how the data is stored on the disk we always only look at tables or diagramatic representation

### Levels of Abstraction
- Conceptual Model
    - ER Diagrams, UML
- Logical Layer
    - Relational data model (simple, record based)
    - Object data model
- Physical level (describes physical storage and implementation details)

### Three Schema Architecture
- External or (end user view) | Different roles see different things
- Logical View (Conceptual view / conceptual schema) or community view
- Internal or physical view

### Data Independance
- Logical Data Independence | Refers to the immunity of external views to changes in logical schema
- Physical Data Independence | Immunity of __conceptual schema__ to changes in the physical __schema__

### Relational model
- Is a logical data model
- In the relational model, data are organized into 2-dimensional tables | called relations
    - Each relation has a number of columns and rows
- A relational DB is a collection of relations
- The name of each column is called an __attribute__
- The name of each row in a table is called a __tuple__
- The set of all possible values for a columnm is called the __domain__ for that attribute

#### Rules for a table 
- Every table must have a unique name
- Every column within a table has a unique name
- No duplicate rows in a table
- Each data item in a cell should be an atomic value | Single value
- Each data item in a cell should not consist of multiple components

### Attribute Domains
- Atomic values in each cell
- Null can be used if the value is unknown

### Relation Schema vs Instance
- Relation Schema | Structure of a table
- Relation Instance | data in the table at any point in time
- Relational DB Scheme | The collection of relational schemas
- Relational DB Instance | The collection of relation instances

### Keys in Relations
##### Superkey
A set of attributes whose values can uniquely identify a row
- A set of attributes in a relation is a superkey iff no two tuples can agree in value on them
##### Candidate Key (CK):
Is a __minimal superkey__ (if you remove any attribute from it it will no longer be a super key)
##### Primary Key
A selected candidate key
##### Foreign Key
An attribute or set of attributes within one relation that matches the candidate key of some relation

### Integrity Constraints
##### Entity Integrity
- No __primary key__ can be null
##### Referential Integrity
- FK values must either be NULL or appear in the referenced relation
##### Domain Constraints
- Specify the possible values an attribute can be
##### Null-value constraints
- Specify whether Null value is allowed in a certain attribute

### General Constraints
- Additional rules specified by the users or DB admins that define or constrain some aspect of the enterprise.

## Database Languages and SQL
### Database languages
##### Data Definition Language (DDL)
- Allows the DBA or user to descrive the structure and constraints (define the data schema)
##### Data Manipulation Language (DML)
- Basic data manipulation on data in the database
##### Data Control Language (DCL)
- Access control

### Query Languages
Is used to retrieve data from DB
- Procedural query language
    - Tells the system __what__ data is needed and __how__ to get it
- Non-procedural (declaritive) language
    - Only tells the system __what data__ is needed and not how to get it

### SQL
SQL can be used as all three types of database languages ^^









