# IS NULL / IS NOT NULL 

- Checks for missing values. 

🪄 Examples: 

```sql
--Students with no pet
SELECT name
FROM hogwarts_students
WHERE pet IS NULL;

--Students with a pet
SELECT name
FROM hogwarts_students
WHERE pet IS NOT NULL;
```
