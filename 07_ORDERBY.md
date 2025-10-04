#ORDER BY

- Sorts results in ascending (ASC, default) or descending (DESC) order.

## ✨ Syntax
```sql
SELECT *
FROM table_name
ORDER BY column ASC|DESC;
```

🪄 Example: 

```sql
-- Rank students by year (ascending), then by name
SELECT name, house, year
FROM hogwarts_students
ORDER BY year ASC, name ASC;
```
