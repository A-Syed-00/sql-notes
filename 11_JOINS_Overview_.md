# JOINS (Overview) 

## What is a JOIN?
 JOINS combine rows from two or more tables based on a related column between them. 
 Relationships are usually defined using **keys**
 Most JOIN's connect: 
 + a **primary key** in one table
 + to a **foreign key** in another table.

## Keys 

### Primary Key 
+ Uniquely identifies each row in a table
+ Can't be NULL
+ Each table has one primary key

For example: 
students.student_id ← student_id is the primary key from the table students

### Foreign Key 
+ A column that references a primary key in another table
+ Can have duplicates
+ Can be NULL (depends)

For example: 
enrollments.student_id ← student_id is the foreign key in the enrollments table

## Basic Syntax 

```sql
SELECT columns
FROM table_1
JOIN table_2
   ON table_1.key = table_2.key;
```
+ ON defines how the tables are related
+ The JOIN condition usually matches Primary Key → Foreign Key

## Table Aliases 
+ Aliases help by making queries shorter and easier to read

### Alias Syntax
```sql
FROM students AS s
JOIN enrollments AS e
ON s.student_id = e.student_id;
```
+ AS is optional

```sql
FROM students s
```
