# Distinct 

## Purpose
+ DISTINCT removes duplicate values from a query result.
+ It returns unique combnations of selected columns.
+ Can use in aggregations, more commonly with COUNT.

## Basic Syntax 

```sql
SELECT DISTINCT column_name
FROM table;
```
+ Uniqueness is evaluated across all selected columns.
+ DISTINCT applies to the entire row.

### Examples: 

1. **Example 1: Getting unique houses**

   ```sql
   SELECT DISTINCT house
   FROM students;
   ```
→ Note that even though multiple students may belong to a certain house, each house only appears once so the results look like: 
Gryffindor, Slytherin, Hufflepuff, Ravenclaw

2. **Example 2: DISTINCT On Multiple Columns** 

```sql
SELECT DISTINCT house, year
FROM students;
```
→ SQL returns unique combinations of (house, year) so a house can appear multiple times if the year is different. 

3. **Example 3: COUNT and COUNT(DISTINCT)**
   
   Goal: To count total students vs unique houses.

```sql
SELECT 
COUNT(*) AS total_students, 
COUNT(DISTINCT house) as unique_houses
FROM students; 
```
+ COUNT(*) → counts all rows
+ COUNT(DISTINCT house) → counts unique house values

### DISTINCT vs GROUP BY 

```sql
--DISTINCT
SELECT DISTINCT house
FROM students;

-- equivalent GROUP BY
SELECT house
FROM students
GROUP BY house;
```
+ DISTINCT for uniqueness
+ GROUP BY for aggregation

## Other Notes: 

**1. DISTINCT with WHERE**

```sql
SELECT DISTINCT house
FROM students
WHERE year = 5;
```
→ Filters first then returns unique values. 

**2.DISTINCT applies to all selected columns**

```sql
SELECT DISTINCT house, name
FROM students;
```
→  Each (house, name) pair is unique 

**3. DISTINCT ignores NULL duplicates** 
+ Multiple NULLs count as 1 or 0
+ COUNT(DISTINCT) does **not** count NULL values

**4. DISTINCT with CASE**

Goal: Count houses with at least one high performing student. 

```sql
SELECT
COUNT(DISTINCT
 CASE
   WHEN grades >= 85 THEN house
 END ) as houses_with_high_performers
FROM students;
```
→ CASE controls which values meet the criteria
→ DISTINCT removes duplicates
→ COUNT counts the result 



