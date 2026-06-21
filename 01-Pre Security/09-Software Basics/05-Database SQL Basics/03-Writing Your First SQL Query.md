# Database SQL Basics — Study Note

## Writing Your First SQL Query

### Overview

SQL (Structured Query Language) is the standard language used to interact with relational databases. It allows users to retrieve, filter, sort, and manage data stored within database tables.

In this section, we learn how to write basic SQL queries using four essential commands:

```sql
SELECT
FROM
WHERE
ORDER BY
```

These commands form the foundation of database querying and are widely used in database administration, software development, data analysis, and cybersecurity investigations.

---

## Main Concept

### What is it?

An SQL query is a command that asks a database to return specific information.

Instead of manually searching through records, SQL allows the database management system to quickly locate and display the required data.

Basic Query Structure:

```sql
SELECT column_name
FROM table_name;
```

Example:

```sql
SELECT * FROM Orders;
```

This query retrieves all data from the Orders table.

---

## How It Works

### Step 1: Select a Table

The `FROM` keyword specifies which table the query should use.

Example:

```sql
FROM Orders
```

The database searches the Orders table.

---

### Step 2: Choose Data to Display

The `SELECT` keyword determines which columns should be displayed.

Example:

```sql
SELECT *
```

Displays all columns.

Example:

```sql
SELECT drink, price
```

Displays only the drink and price columns.

---

### Step 3: Filter Data

The `WHERE` clause filters records based on specified conditions.

Example:

```sql
WHERE drink = 'Coffee'
```

Only coffee orders are displayed.

---

### Step 4: Sort Results

The `ORDER BY` clause sorts query results.

Example:

```sql
ORDER BY price
```

Sorts prices from lowest to highest.

Example:

```sql
ORDER BY price DESC
```

Sorts prices from highest to lowest.

---

### Step 5: Combine Multiple Clauses

SQL allows multiple clauses in a single query.

Example:

```sql
SELECT *
FROM Orders
WHERE drink = 'Coffee'
ORDER BY price DESC;
```

This query:

1. Retrieves all columns.
2. Displays only coffee orders.
3. Sorts coffee orders by price from highest to lowest.

---

## Important Components

### SELECT

Used to specify which columns should be displayed.

Syntax:

```sql
SELECT column_name
FROM table_name;
```

Example:

```sql
SELECT drink, price
FROM Orders;
```

---

### Asterisk (`*`)

Represents all columns.

Example:

```sql
SELECT *
FROM Orders;
```

Output:

```text
All available columns
```

---

### FROM

Specifies the table to query.

Example:

```sql
FROM Orders
```

---

### WHERE

Filters rows based on a condition.

Syntax:

```sql
WHERE condition
```

Example:

```sql
WHERE drink = 'Coffee'
```

---

### ORDER BY

Sorts query results.

Syntax:

```sql
ORDER BY column_name
```

Example:

```sql
ORDER BY price
```

---

### DESC

Sorts results in descending order.

Example:

```sql
ORDER BY price DESC
```

Output:

```text
Highest Price → Lowest Price
```

---

### ASC

Sorts results in ascending order.

Example:

```sql
ORDER BY price ASC
```

Output:

```text
Lowest Price → Highest Price
```

Note:

```text
ASC is the default sorting order.
```

---

## Advantages / Benefits

* Quickly retrieves information.
* Reduces manual searching.
* Filters relevant data efficiently.
* Organizes results through sorting.
* Supports large-scale data analysis.
* Improves database management productivity.
* Forms the foundation of advanced SQL operations.

---

## Key Characteristics

* SQL queries are structured commands.
* `SELECT` retrieves data.
* `FROM` identifies the table.
* `WHERE` filters records.
* `ORDER BY` sorts results.
* Queries can combine multiple clauses.
* Queries retrieve information without modifying stored data.

---

## Example

### Display All Orders

```sql
SELECT *
FROM Orders;
```

Result:

| id | drink  | price | time  |
| -- | ------ | ----- | ----- |
| 1  | Coffee | 5.00  | 09:00 |
| 2  | Tea    | 3.50  | 09:15 |

---

### Display Specific Columns

```sql
SELECT drink, price
FROM Orders;
```

Result:

| drink  | price |
| ------ | ----- |
| Coffee | 5.00  |
| Tea    | 3.50  |

---

### Filter Coffee Orders

```sql
SELECT *
FROM Orders
WHERE drink = 'Coffee';
```

Result:

| id | drink  | price | time  |
| -- | ------ | ----- | ----- |
| 1  | Coffee | 5.00  | 09:00 |

---

### Sort by Price

```sql
SELECT *
FROM Orders
ORDER BY price DESC;
```

Result:

```text
Highest priced orders displayed first.
```

---

### Filter and Sort Together

```sql
SELECT *
FROM Orders
WHERE drink = 'Coffee'
ORDER BY price DESC;
```

Result:

```text
Only coffee orders shown,
sorted from highest to lowest price.
```

---

## Key Notes

* `SELECT` retrieves data.
* `FROM` specifies the table.
* `WHERE` filters rows.
* `ORDER BY` sorts results.
* `DESC` means descending order.
* `ASC` means ascending order.
* `*` selects all columns.
* Multiple SQL clauses can be combined in one query.
* SQL queries do not modify data unless specific modification commands are used.

---

## Learning Outcome

After completing this section, I understood how to write basic SQL queries to retrieve information from relational databases. I learned how to use `SELECT` to choose data, `FROM` to specify a table, `WHERE` to filter records, and `ORDER BY` to sort results. I also gained practical experience combining multiple SQL clauses to create more precise and useful database queries, providing a foundation for more advanced database operations and data analysis tasks.

---

# Database SQL Basics — Project Report

## Objective

The objective of this section was to introduce basic SQL query construction and demonstrate how to retrieve, filter, and sort information stored within database tables using the fundamental SQL commands: `SELECT`, `FROM`, `WHERE`, and `ORDER BY`.

---

## Tasks Completed

### Challenge 1

**Question:**

How can all records from the Orders table be displayed?

**Answer:**

```sql
SELECT * FROM Orders;
```

---

### Challenge 2

**Question:**

How can only the drink and price columns be displayed?

**Answer:**

```sql
SELECT drink, price
FROM Orders;
```

---

### Challenge 3

**Question:**

How can only coffee orders be displayed?

**Answer:**

```sql
SELECT *
FROM Orders
WHERE drink = 'Coffee';
```

---

### Challenge 4

**Question:**

How can orders be sorted by price from lowest to highest?

**Answer:**

```sql
SELECT *
FROM Orders
ORDER BY price;
```

---

### Challenge 5

**Question:**

How can orders be sorted by price from highest to lowest?

**Answer:**

```sql
SELECT *
FROM Orders
ORDER BY price DESC;
```

---

### Challenge 6

**Question:**

How can coffee orders be filtered and sorted by price in descending order?

**Answer:**

```sql
SELECT *
FROM Orders
WHERE drink = 'Coffee'
ORDER BY price DESC;
```

---

## Skills Practiced

* SQL Fundamentals
* Query Construction
* Data Retrieval
* Table Navigation
* Record Filtering
* Result Sorting
* Database Exploration
* SQL Syntax Understanding
* Relational Database Interaction

---

## Key Concepts Learned

* SELECT Statement
* FROM Clause
* WHERE Clause
* ORDER BY Clause
* ASC Sorting
* DESC Sorting
* Database Tables
* Rows and Columns
* Query Filtering
* Query Optimization Basics

---

## Conclusion

Through this section, I gained practical experience writing basic SQL queries to retrieve information from relational databases. I learned how to select specific data, filter records based on conditions, and sort results using SQL commands. By combining `SELECT`, `FROM`, `WHERE`, and `ORDER BY`, I developed a foundational understanding of database querying techniques that are essential for database administration, software development, data analysis, and cybersecurity investigations.
