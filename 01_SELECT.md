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

 💫 Examples: 
```sql
-- 1. Select first name and last name from employees table. 

SELECT first_name, last_name
FROM employees;


-- 2. Select movie_title and movie_genre from movies table. rename movie_title to movie and movie_genre to genre

SELECT movie_title AS movie,
       movie_genre AS "Genre"
FROM movies;
```       
