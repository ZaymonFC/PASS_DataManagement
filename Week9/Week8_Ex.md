# Week 8 Ex
### Knowledge Questions
- What is data redundancy
- What are the three kinds of update anomalies?
- Give an example of inferring a functional dependency
- What are three inference rules?
- What is a closure set?
- T/F The closure set of a superkey will contain every attribute in the table
- What is the efficient method of finding candidate keys using functional dependencies?


### Problem Solving
#### Find the closure set of attributes A given that,
```js
A={bookNumber, bookPrice}
F={
    bookType -> bookStyle
    bookNumber -> author, title
    bookPrice -> bookType
}
```
### Find the candidate keys of the following table
1. R(A, B, C, D, E), With the following functional dependencies
```js
    A->C
    C->E
    A,D->B
```
2. R(A, B, C, D, E), With the following functional dependencies
```js
    A,B,C -> D,E
    B,E -> A
```

