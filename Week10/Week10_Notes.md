# Week 8 Notes
Note | w.r.t = with respect to

### Normal Forms
- 1st normal form | 1NF
- 2nd normal form | 2NF
- 3rd normal form | 3NF
- Boyce-Codd normal form | BCNF
The higher the normal form the less redundancies

### 1st Normal Form
A relation is in normal form if all attributes are atomic
Usually every table will be in 1st normal form 1NF
> Every relation generated from ERD will be in first normal form

### Non-Key Attributes
- Any attributes of relation R which are not part of __any__ candidate key of R

### Partial Dependency
- X->Y is a partial dependency if X is a subset of some candidate key
> We can then say that Y is partially dependent on the candidate key

### 2NF
A relation is in 2NF if there is no non-key attribute in R which is partially dependant on a candidate key of R

### Transitive Dependency
Let X -> Y be an FD that holds for relation R. We say that X->Y 
if X->Y is not a partial dependency and X is not a super key

### 3NF
A relation is in 3NF if the relation is in 2NF and there iff for every non-trivial FD -> X-Y
either X is a superkey of R or Y is a set of key attributes

### Normalising to 2NF
B->D Partial Dependency
- Create a new relation (B,D)
- Create a new relation with B and all remaining attributes
R1.B is a foreign key to R2.B
- Reinstate FD's on the new relations

### Normalising to 3NF
Normalise the tables to 2NF
If there is a non trivial FD X->Y that violates the definition of
the normal form, then decompose the table into two
One contains X,Y , the other contains X and all other attributes

### Step by Step Approach to Table Normalisation
1NF -> 2NF  | Remove Partial Dependencies
2NF -> 3NF  | Remove transitive Dependencies
3NF -> BCNF | Remove functional dependencies where LHS is not a SK
