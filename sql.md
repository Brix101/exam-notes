# Basic and Advanced concepts

## Basic SQL Commands:

- SELECT, INSERT, UPDATE, DELETE: Understand how to retrieve data from a database, insert new records, update existing records, and delete records.
- WHERE clause: Know how to filter data using conditions.
- ORDER BY clause: Understand how to sort the result set.
- GROUP BY and HAVING: Know how to group data and filter groups based on conditions.

## Joins:

- INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN: Understand different types of joins and when to use them.
- ON clause: Know how to specify join conditions.

## Subqueries:

- Understand how to use subqueries within SELECT, WHERE, and FROM clauses.

## Aggregation Functions:

- SUM, AVG, COUNT, MAX, MIN: Know how to use these functions to perform calculations on data.

## Indexes:

- Understand the concept of indexes and how they can improve query performance.

## Constraints:

- PRIMARY KEY, FOREIGN KEY, UNIQUE, NOT NULL: Understand how to use constraints to maintain data integrity.

## Views:

- Know how to create and use views to simplify complex queries.

## Normalization:

- Understand the basics of database normalization to design efficient and scalable databases.

## Transactions:

- Know the basics of transactions, including COMMIT and ROLLBACK statements.

## Security:

- Understand basic security principles, such as user privileges and access control.

# SQL queries

```sql
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department_id INT
);
```

### Retrieve all employees and their details from the "employees" table.

```sql
SELECT * FROM employees;
```

### Retrieve the first and last names of employees in the "Sales" department.

```sql
SELECT first_name, last_name
FROM employees
WHERE department_id = (SELECT department_id FROM departments WHERE department_name = 'Sales');
```

> **Note:** In this example, we use a subquery in the WHERE clause to find the department_id for 'Sales' and then filter the employees based on that department_id.

### Calculate the average salary of employees in the "Finance" department.

Assuming there is a "salaries" table with a structure like:

```sql
CREATE TABLE salaries (
    employee_id INT,
    salary INT
);
```

The query would be:

```sql
SELECT AVG(salary) AS average_salary
FROM employees e
JOIN salaries s ON e.employee_id = s.employee_id
WHERE e.department_id = (SELECT department_id FROM departments WHERE department_name = 'Finance');
```

This example involves a JOIN operation to combine data from the "employees" and "salaries" tables.

These are just simple examples, and the complexity of queries can increase based on the specific requirements and the database schema.
