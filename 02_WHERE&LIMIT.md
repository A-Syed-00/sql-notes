# WHERE Statement

 - The `WHERE' clause filters rows based on a condition. 
- It works with numbers, text, and dates 

## 🔹 Syntax

```sql
SELECT column1, column2
FROM table_name;
WHERE condition; 
```

 💫 Example

 ```sql
-- Select 'sales' from the department column in the employees table. 

SELECT * 
FROM employees 
WHERE department = 'Sales'; 
```





# LIMIT 

- Restricts number of rows returned 
- Helpful for checking sample data

## 🔹 Syntax

```sql
SELECT *
FROM table_name;
LIMIT n;  
```
💫 Example

 ```sql
-- Limit row output to only 15 results from the employees table 

SELECT * 
FROM employees 
LIMIT 15;
```

