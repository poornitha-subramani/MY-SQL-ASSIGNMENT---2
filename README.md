# 👨‍💼 Employee Database Management — SQL Project

A hands-on **MySQL database project** demonstrating fundamental to intermediate SQL concepts using an employee management database.

This project covers data insertion, filtering, sorting, aggregate functions, grouping, and different types of SQL joins.

 📌 Project Overview

The **Employee Database Management System** is designed to store and analyze information about employees, departments, and office locations.

The project demonstrates how SQL can be used to:

* Manage employee records
* Organize employees by departments and locations
* Retrieve specific employee information
* Perform salary and age analysis
* Calculate aggregate statistics
* Group and filter data
* Combine information from multiple tables using joins

 🗂️ Database Structure

The database consists of three main tables:

 1. employees

Stores employee-related information.

| Column          | Description                |
| --------------- | -------------------------- |
| employee_id  | Unique employee identifier |
| employee_name | Employee's name            |
| gender        | Employee gender            |
| age           | Employee age               |
| hire_date     | Date of joining            |
| designation  | Job designation            |
| department_id | Department reference       |
| location_id   | Location reference         |
| salary        | Employee salary            |

2. departments

Stores department information.

| Column            | Description                  |
| ----------------- | ---------------------------- |
| department_id   | Unique department identifier |
| department_name | Name of the department       |

Example departments include:

* Software Development
* Marketing
* Data Science
* Human Resources
* Product Management
* Finance
* IT
* Operations
* Research and Development

 3. location

Stores office location information.

| Column          | Description                |
| --------------- | -------------------------- |
| location_id   | Unique location identifier |
| location_name | Name of the location       |

Example locations:

* Chennai
* Bangalore
* Hyderabad
* Pune


 🛠️ SQL Concepts Covered

🔹 Database & Table Operations
* USE
* INSERT INTO
* Database and table relationships

🔹 Data Retrieval
* SELECT
* DISTINCT
* Column aliases using AS
  
🔹 Filtering
* WHERE
* Comparison operators
* AND
* IS NULL
* LIKE

🔹 Sorting
* ORDER BY
* ASC
* DESC

 🔹 Limiting Results
* LIMIT
  
🔹 Data Modification
* UPDATE
* SET
* WHERE
  
🔹 Aggregate Functions
* SUM()
* MIN()
* MAX()
* AVG()
* COUNT()
* 
🔹 Grouping
* GROUP BY`
* HAVING

🔹 Pattern Matching
* LIKE
* % wildcard

 🔹 SQL Joins
* INNER JOIN
* LEFT JOIN
* RIGHT JOIN


📊 Queries Implemented

The project includes SQL queries for:

1. Retrieving distinct employee salaries
2. Creating aliases for employee age and salary
3. Finding employees based on salary and hiring date
4. Identifying employees with missing designations
5. Updating missing designations
6. Sorting employees by department and salary
7. Finding employees hired in 2018
8. Calculating total salary in the Finance department
9. Finding the minimum employee age
10. Finding the maximum salary for each location
11. Calculating average salary for Analyst designations
12. Finding departments with fewer than three employees
13. Finding locations where female employees have an average age below 30
14. Listing employees with their department names
15. Counting employees in each department
16. Listing employees by location
17. Demonstrating `INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN`

🔍 Example SQL Queries

 Find distinct salaries

SELECT DISTINCT salary
FROM employees;

Find employees earning more than ₹50,000 and hired before 2016

SELECT *
FROM employees
WHERE salary > 50000
  AND hire_date < '2016-01-01';

 Find the maximum salary by location

SELECT location_id, MAX(salary) AS max_salary
FROM employees
GROUP BY location_id;

Find average salary of Analysts

SELECT designation, AVG(salary) AS avg_salary
FROM employees
WHERE designation LIKE '%Analyst%'
GROUP BY designation;

Count employees in each department

SELECT department_id, COUNT(*) AS employee_count
FROM employees
GROUP BY department_id;

Find departments with fewer than 3 employees

SELECT department_id, COUNT(*) AS employee_count
FROM employees
GROUP BY department_id
HAVING COUNT(*) < 3;

Employee and Department Information

SELECT 
    e.employee_name,
    e.designation,
    d.department_name
FROM employees e
JOIN departments d
    ON e.department_id = d.department_id;

📁 Project Structure

Employee-Database-SQL/
│
├── README.md
│
├── employee_database.sql
│
└── screenshots/
    ├── MY SQL ASSIGNMENT -2.pdf

 💻 Technologies Used

* **MySQL**
* **MySQL Workbench**
* **SQL**

 🎯 Learning Objectives

Through this project, I practiced:

* Writing SQL queries from business requirements
* Working with relational databases
* Filtering and sorting records
* Handling missing values
* Performing salary and employee analysis
* Using aggregate functions
* Grouping and filtering grouped data
* Understanding SQL joins
* Working with multiple related tables
* Updating records safely using conditions

📈 Key SQL Skills Demonstrated

SQL Basics
    ↓
SELECT & WHERE
    ↓
Filtering & Sorting
    ↓
Aggregate Functions
    ↓
GROUP BY & HAVING
    ↓
Pattern Matching
    ↓
UPDATE Operations
    ↓
INNER / LEFT / RIGHT JOIN
    ↓
Relational Database Analysis


This project is part of my journey toward developing practical **Data Analytics and SQL skills**.
