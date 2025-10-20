
# Aggregate Functions 

Aggregate functions allow calculations on groups of data - for example, counting how many students 
are in each house or finding the highest grade in a class. 

## 1. COUNT()
Counts the number of rows that match a condition. 

**Syntax:**
```sql
SELECT COUNT(column)
FROM table_name
WHERE condition;
```

🪄 Example

 ```sql
-- Count all students
SELECT COUNT(*) AS total_students
FROM students;
 ```

## 2. SUM()

Adds up numeric values in a column. 

**Syntax:**
```sql
SELECT SUM(column)
FROM table_name;
```
🪄 Example
 ```sql
-- total sum of house points 
SELECT house, SUM(points) AS total_points
FROM house_points
GROUP BY house;
```

## 3. AVG()

Finds the average (mean) of a numeric column. 

**Syntax:**
```sql
SELECT AVG(column)
FROM table_name;
```
🪄 Example
 ```sql
-- Finding the average grade for each course then grouping them by course

SELECT course_name, AVG(grade) AS avg_course_grade
FROM student_grades
GROUP BY course_name;
 ```

## 4. MIN() and MAX()
Finds the smallest and largest values in a column. 

**Syntax:**
```sql
SELECT MIN(column), MAX(column)
FROM table_name;
```
🪄 Example
 ```sql
-- Finds the highest and lowest score in each subject 
SELECT 
  subject,
  MIN(score) AS lowest_score,
  MAX(score) AS highest_score
FROM exam_scores
GROUP BY subject;
 ```

## 5. GROUP BY

GROUP BY groups rows that share the same value so that you can aggregate within each group. 

**Syntax:**
```sql
SELECT column, AGGREGATE_FUNCTION(column)
FROM table_name
GROUP BY column;
```

🪄 Example
```sql
--Counts students per house
SELECT house, COUNT(*) AS num_students
FROM students
GROUP BY house;
```

## 6. HAVING 







