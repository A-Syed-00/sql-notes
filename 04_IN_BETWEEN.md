# IN 

- Checks if a value matches any in a list.

## ✨ Syntax

```sql
SELECT *
FROM table_name
WHERE column IN (value1, value2, .....); 
```

🪄 Example: 

```sql
-- Hogwarts students who are from Gryffindor and Hufflepuff 
SELECT name, house
FROM hogwarts_students 
WHERE house IN ('Gryffindor', 'Hufflepuff');
```

# BETWEEN 

- Filters values within a range (inclusive)

## ✨ Syntax

```sql
SELECT *
FROM table_name
WHERE column BETWEEN low AND high;
```

🪄 Example: 

```sql
-- Hogwarts students between year 4 or 5  
SELECT name, year
FROM hogwarts_students 
WHERE year BETWEEN 4 AND 5;
```





