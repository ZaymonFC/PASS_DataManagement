# Week 5 Ex Answers
## Question 1
```sql
INSERT into alumni
select *
from student
where to_date(grad_date) >= '01-jan-2017';
```

## Question 2
```sql
SELECT b.Author, a.Author, title, country
from book b, author a
WHERE b.Author=a.Author;
```

## Question 3
```sql
SELECT isbn, SUM(quantity)
FROM orders
GROUP BY isbn;
```