# Week 8 Notes
Note | w.r.t = with respect to

### Data redundancy
- Data redundancies can cause __update anomalies__
    - Insertion anomaly
    - Deletion anomaly 
    - Modification anomaly | May have to modify something in multiple places if the data is redundant

### Normal Forms
- To minimize redundancy we need tables that are in a _normal form_
- Some normal forms are defined using functional dependencies
    - 1st normal form | 1NF
    - 2nd normal form | 2NF
    - 3rd normal form | 3NF
    - Boyce-Codd normal form | BCNF

### Functional Dependencies
- A FD is a formula of the form A->B (Where A and B are sets).
    - If two records have the same value for A then they also have the same value for B
    - For each value of A there is a unique value of B
    - We say that A functionally determines B or B is functionally dependant on A
- A -> B can also be written as A1, A2,... Ak -> B1, B2,... Bn

### Trivial Functional Dependency
- If B is a subset of A, then A->B and this is a trivial dependency
- Trivial dependencies are not considered in normalization

### Some observations
- All attributes in a table are FD on the PK

### FD Inference
If we know A->B, B->C, then we can infer that A->C
If A->B, A,C -> B,C

### Inference Rules
Reflexivity
- If B is a subset of A, then A -> B
Augmentation
- If A->B, then A,C->B,C
Transitivity
- If A->B and B->C, then A->C

### Closure set of a set of attributes
- Let F be a set of FDs, A be a set of attributes
    - The closure set of A w.r.t F, denoted A+ is the set of all attributes that are functionally dependant on A
    Closure set of A is the set of all attributes that are FD on A

### Finding Candidate Keys using Functional Dependencies
- Any super key must contain all the attributes that do not appear on the right hand side of the arrow
- So start with the set of keys that have not appeared on the right
- If A+ contains all attributes then the it is the _only_ candidate key
- Otherwise keep adding attributes into A
- To make sure A is a CK you need to make sure any subset of A is not a super key





