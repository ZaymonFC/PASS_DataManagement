# Week 4 Ex Answers
#### Question 1
```SQL
create table Staff(
    staff_no char(3),
    staff_name varchar2(20),
    dept_name char(4),
    CONSTRAINT staff_pk PRIMARY KEY(staff_no)
);
```

#### Question 2
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

#### Question 3
```SQL
create table Books(
    ISBN char(13) not null,
    author varchar(40) not null,
    publish_date date,
    genre varchar(35),
    CONSTRAINT book_pk PRIMARY KEY(ISBN)
);
```

### Question 4
```SQL
Insert into Books values('','', TO_DATE('12/07/1994', 'dd/mm/yyyy'), 'Fantasy');
```

### Question 5
```SQL
Delete from Staff where staff_no ='007';
```