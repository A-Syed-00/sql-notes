# SELECT Statement

## 🔹 Definition
The `SELECT` statement is used to retrieve data from a table.


---
## 🔹 Syntax

```sql
SELECT column1, column2
FROM table_name;
```
-------




## ⭐️ Key Points 

- Use * to select all columns 
- Columns can be renamed using `AS`

 🪄 Examples: 
```sql
-- 1. Select first name and last name from Hogwarts faculty. 

SELECT first_name, last_name
FROM hogwarts_faculty;


-- 2. Select course_name and rename to class. Also select course_books and rename to books.

SELECT course_name AS class,
       course_books AS "books"
FROM hogwarts_courses;
```       
