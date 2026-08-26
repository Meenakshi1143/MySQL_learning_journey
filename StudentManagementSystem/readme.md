\# Student Management System



\## Project Overview



The \*\*Student Management System\*\* is a relational database project developed using \*\*MySQL\*\*.



The project is designed to manage student academic information such as departments, courses, enrollments, attendance, examinations, results, and payments.



The database demonstrates the implementation of:



\- Database and table creation

\- Primary and foreign keys

\- NOT NULL, UNIQUE, DEFAULT and CHECK constraints

\- Data insertion

\- Table relationships

\- Joins

\- Aggregate functions

\- Subqueries

\- CASE expressions

\- GROUP BY and HAVING

\- ORDER BY

\- Date functions

\- SQL queries of different difficulty levels

\- Data analysis using SQL



\## Technologies Used



\- MySQL

\- SQL

\- GitHub



\## Database Name



```sql

student\_management

```



\## Database Entities



\### 1. STUDENTS

Stores basic information about students.



Important columns:

\- `student\_id` – Primary Key

\- `dept\_id` – Foreign Key

\- `first\_name`

\- `last\_name`

\- `gender`

\- `email`

\- `phone`

\- `date\_of\_birth`

\- `enroll\_date`



\### 2. DEPARTMENTS

Stores department information.



\- `dept\_id` – Primary Key

\- `dept\_name`

\- `location`



\### 3. INSTRUCTORS

Stores instructor information.



\- `instructor\_id` – Primary Key

\- `first\_name`

\- `last\_name`

\- `email`

\- `phone`

\- `qualification`

\- `hire\_date`



\### 4. COURSES

Stores courses offered by departments.



\- `course\_id` – Primary Key

\- `course\_name`

\- `credits`

\- `dept\_id` – Foreign Key

\- `instructor\_id` – Foreign Key



\### 5. ENROLLMENTS

Stores which students are enrolled in which courses.



\- `enrollment\_id` – Primary Key

\- `student\_id` – Foreign Key

\- `course\_id` – Foreign Key

\- `enroll\_date`

\- `semester`

\- `academic\_year`



\### 6. ATTENDANCE

Stores student attendance for enrolled courses.



\- `attendance\_id` – Primary Key

\- `enrollment\_id` – Foreign Key

\- `attendance\_date`

\- `status`



\### 7. EXAMINATIONS

Stores examination details for courses.



\- `exam\_id` – Primary Key

\- `course\_id` – Foreign Key

\- `exam\_type`

\- `exam\_date`

\- `max\_marks`



\### 8. RESULTS

Stores marks obtained by students in examinations.



\- `result\_id` – Primary Key

\- `exam\_id` – Foreign Key

\- `student\_id` – Foreign Key

\- `marks\_obtained`

\- `grade`



\### 9. PAYMENTS

Stores student fee/payment information.



\- `payment\_id` – Primary Key

\- `student\_id` – Foreign Key

\- `payment\_date`

\- `amount`

\- `payment\_type`

\- `payment\_status`



\## Main Relationships



\- One department can have many students.

\- One department can offer many courses.

\- One instructor can teach many courses.

\- One student can have many enrollments.

\- One course can have many enrollments.

\- One enrollment can have many attendance records.

\- One course can have many examinations.

\- One examination can have many results.

\- One student can have many result records.

\- One student can make many payments.



\## Cardinality Summary



| Relationship | Cardinality |

|---|---|

| DEPARTMENTS → STUDENTS | 1 : N |

| DEPARTMENTS → COURSES | 1 : N |

| INSTRUCTORS → COURSES | 1 : N |

| STUDENTS → ENROLLMENTS | 1 : N |

| COURSES → ENROLLMENTS | 1 : N |

| ENROLLMENTS → ATTENDANCE | 1 : N |

| COURSES → EXAMINATIONS | 1 : N |

| EXAMINATIONS → RESULTS | 1 : N |

| STUDENTS → RESULTS | 1 : N |

| STUDENTS → PAYMENTS | 1 : N |



\## SQL Queries Included



\### Easy Level



Queries using:



\- SELECT

\- WHERE

\- Comparison operators

\- BETWEEN

\- IN

\- LIKE

\- IS NULL

\- ORDER BY

\- DISTINCT



\### Intermediate Level



Queries using:



\- COUNT()

\- SUM()

\- AVG()

\- MAX()

\- MIN()

\- GROUP BY

\- HAVING

\- INNER JOIN

\- LEFT JOIN

\- DATE functions

\- CASE



\### Hard Level



Queries using:



\- Multiple-table JOINs

\- Subqueries

\- Correlated subqueries

\- EXISTS

\- NOT EXISTS

\- Common Table Expressions (CTEs)

\- Window functions

\- Ranking

\- Conditional aggregation



\## Example Business Questions



\### Easy



1\. Display all students.

2\. Display students from a particular department.

3\. Find students enrolled after a given date.

4\. Find courses having more than 3 credits.

5\. Display students whose names start with 'A'.



\### Intermediate



6\. Count students in each department.

7\. Find the average marks for each examination.

8\. Display students with their department names.

9\. Find the number of students enrolled in each course.

10\. Calculate total payments made by each student.



\### Hard



11\. Find the top-performing student in each department.

12\. Find students whose marks are above the overall average.

13\. Find courses having more students than the average course enrollment.

14\. Rank students based on their total marks.

15\. Identify students whose attendance percentage is below 75%.



\## Project Features



\- Proper relational database design

\- Primary and foreign key implementation

\- Referential integrity

\- Sample records for testing

\- Multiple table relationships

\- SQL queries from basic to advanced levels

\- Academic performance analysis

\- Attendance analysis

\- Fee/payment analysis

\- ER diagram included



\## Learning Outcomes



Through this project, the following concepts were practiced:



\- Database design

\- Normalization

\- Primary and foreign keys

\- Constraints

\- SQL query writing

\- Joins and relational analysis

\- Aggregate functions

\- Subqueries

\- Conditional logic using CASE

\- Grouping and filtering

\- Date-based analysis

\- Window functions

\- ER diagram design



\## Project Structure



```text

Student-Management-System/

│

├── README.md

├── student\_management\_queries.sql

└── student\_management\_ER.png

```
