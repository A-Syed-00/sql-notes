# AND, OR, NOT

- Combining multiple conditions

🪄 Examples:

```sql
--1. AND -> Both conditions must be true.
-- Students that are in year 5 and are in Ravenclaw
SELECT name, year, house
FROM hogwarts_students
WHERE year = 5 AND house = 'Ravenclaw';

--2. OR -> Either condition can be true.
-- Students from either Ravenclaw or Slytherin

SELECT name, year, house
FROM hogwarts_students
WHERE house = 'Ravenclaw' OR house = 'Slytherin'

--3. NOT -> Condition is not true
-- Exclude students from year 1
SELECT name, year, house
FROM hogwarts_students
WHERE NOT year = 1;
```



