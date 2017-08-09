# Week 5 Notes

### Two Approaches
- Top-down | Focus for this course
    - Model the requirements using a diagram
    - Map the diagram to a set of tables including keys and FK's
    - Add constraints
- Bottom-up
    - Collect all possible attributes in the DB
    - Normalize

### Entity-Relationship Diagram
- Views a DB as consisting of
    - Entities and relationships

### Entities
> A real world or abstract object
Every entity has attributes which describe it
- Entity is drawn in a rectangle

### Attributes
- An attribute can be
    - Single or __composite__
    - Single valued or __multi-valued__
The attribute domain is the set of values an attribute uses
> Attributes are drawn in an ERD as an ellipse
- Derived attributes have dotted lines (Like age from date of birth)
- Multivalued attributes have double lines
- Concept attributes are decomposed into the separate parts
- Primary key is __Underlined__

### Relationships
We draw the relationships in a diamond between two entities
- Attributes of relationships are added with ellipses
- Relationships can have different degrees
    - UNARY | (recursive) between instances of the same set
    - BINARY | between instances of two entities
    - TERNARY | between instances of three entities
    - N-ARY | between instances of N entities

### Cardinality Constraint
- Describes the multiplicity of the relationship
- 1:1, 1:M, M:M, M:1
- Can have explicit cardinalities

### Participation
- Participation of entity instances in relationships can be
    - Optional | 
    - Mandatory | 

### Weak Entities
- Existence depends on the existence of other entities
- PK's partially or completely derived from the parent entity
- Any dependant is generally a weak entity
- Can't be many to many







