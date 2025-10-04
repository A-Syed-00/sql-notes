# WHERE Statement

 - The `WHERE' clause filters rows based on a condition. 
- It works with numbers, text, and dates 

## 🔹 Syntax

```sql
SELECT column1, column2
FROM table_name
WHERE condition; 
```

 🪄 Example

 ```sql
-- Find all Gryffindor students

SELECT name, house
FROM hogwarts_students 
WHERE house = 'Gryffindor'; 
```





# LIMIT 

- Restricts number of rows returned 
- Helpful for checking sample data

## 🔹 Syntax

```sql
SELECT *
FROM table_name
LIMIT n;  
```
 🪄 Example

 ```sql
-- Limit output to just 15 students 

SELECT * 
FROM hogwarts_students 
LIMIT 15;
```

