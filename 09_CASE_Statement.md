# CASE Statement 

## Purpose
+ CASE adds conditional logic to queries (similiar to if/else in programming) 
+ Used to: 
   + Create new categorical columns 
   + Apply conditional labels 
   + Grouping numeric values
 
## Basic Syntax

```sql
SELECT *,
CASE WHEN condition_1 THEN result_1
WHEN condition_2 THEN result_2
ELSE result_3
END
FROM Table;
```
Else is optional (returns NULL if omitted) 

### Example 1- Categorizing

```sql
-- Categorizing student's spell activity in charms class by low, medium or high
SELECT name, year, class, spell_grade
CASE
     WHEN spell_grade >= 40 THEN 'High'
     WHEN spell_grade >= 20 THEN 'Medium'
     ELSE 'Low'
   END AS spell_level_charms
FROM hogwarts_classes
WHERE class = 'Charms'
```

### Example 2- Aggregation 

```sql
-- Label houses based on total spells cast

SELECT
  house,
  SUM(spells_cast) AS total_spells,
  CASE
    WHEN SUM(spells_cast) >= 70 THEN 'Top House'
    WHEN SUM(spells_cast) >= 40 THEN 'Mid Tier'
    ELSE 'Needs Improvement'
  END AS house_rank
FROM students
GROUP BY house;
```

### Example 3 - COUNT (Conditional Aggregation) 

```sql
-- count how many high-performing students each house has in their exams

SELECT house 
      COUNT(
      CASE
         WHEN spell_grade >= 45 THEN student_id
      END ) AS high_performer_potions
FROM exam_grades
GROUP BY house;
```

**Key Idea**
+ Case runs inside the aggregate function
+ Only rows meeting the condition are counted

### Common Use Cases 
+ Categorizing numerical vales (age, score)
+ Flagging rows (yes/no)
+ Conditional aggregation
