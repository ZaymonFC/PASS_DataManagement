# Week 4 Notes

### Oracle built in types
- Numbers | Number | Number(n, scale)
- Character Strings | Char[n], varchar2 | char(10), VarChar2(50)
- Date and time | Date
- Large strings and BLOBS

### Creating a table
```SQL
create table Department(
    Dept_no char(4)PRIMARY KEY,
    Dept_name varchar2(25)); 
```
Or with constraints:
```SQL
create table Department(
    dept_no char(4),
    dept_name varchar2(25),
    CONSTRAINT dept_PK PRIMARY KEY(dept_no));
``` 

### Defining Foreign Key
```SQL
create table Staff(
    staff_no char(3),
    staff_name varchar2(20),
    dept_name char(4),
    CONSTRAINT staff_pk PRIMARY KEY(staff_no),
    CONSTRAINT staff_fk foreign key(dept_no)
        references department(dept_no)
);
```
Note that it is important that FK attributes have the same type

### Check Constraints
```SQL
create table Staff(
    staff_no char(3),
    staff_name varchar2(20) not null,
    staff_gender char(1) check (staff_gender in ('M', 'F')),
    staff_salary number(8, 2) not null,
    Constraint staff_pk Primary key (staff_no),
    Constraint staff_sal check (staff_salary > 1000.00),
);
```

### Inserting data
`Insert into Department values ('0001', 'sales');`
`Insert into Department values ('0002','accounting');`

### Deleting data
`Delete from staff;`
`Delete from staff where staff_no = '002';`
`Delete from staff where staff_salary > 500000;`

## Part 2
### Alter tables
```SQL
Alter table table_name
    add(column_spec constraint);
```
### Modify Tables
```SQL
Alter table table_name
    drop (column_name);
```
### Dropping Tables
`Drop table Department`
If you have foreign keys it will drop the constraint
`Drop table Department cascade constraints`

## Viewing Tables and Table Structures
`select * from cat;`
Where cat is the system catalogue (Oracle feature)

### Updating Data
```SQL
Update staff
SET staff_name = 'David Smith'
    dept_no='0002'
Where staff_no = '001';
```

### Rollback and Commit
To make your data update permanent, `commit;`
To undo your data update, `rollback;`

## Making Selections
```SQL
Select *
from product;
```

Select two different values
```SQL
select prodNo, prodName
from product
where price <=200;
```

```SQL
select custName
from customer
where age > 25 and custCity ='Gold Coast'
order by age;
```

