# Operators (=, >, <, >=, <=, <>)

- Used to compare values in conditions.

 🪄 Examples: 

```sql
--1. Hogwarts students who are in years higher/greater than year 5 (Greater than) 
SELECT *
FROM hogwarts_students 
WHERE year > 5;

--2.  All Hogwarts faculty who taught Defense Against the Dark Arts Classes (Equal to)
SELECT
teachers, class
FROM hogwarts_faculty
WHERE class = 'Defense Against the Dark Arts';

```


# LIKE Statement 

- Filters text using wildcards
- % → any sequence of characters
- _ → a single character

🪄 Example: 

```sql
-- Hogwarts faculty whose name starts with H
SELECT name
FROM hogwarts_faculty 
WHERE name LIKE 'H%';
```




