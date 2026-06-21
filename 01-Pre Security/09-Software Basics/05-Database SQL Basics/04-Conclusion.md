# Database SQL Basics — Study Note

## Database Fundamentals and Basic SQL Operations

### Overview

Databases are essential systems used to store, organize, manage, and retrieve information efficiently. As data volumes grow, manual record-keeping methods become impractical, making databases a critical component of modern computing environments.

This room introduced the fundamental concepts of databases, table structures, and SQL querying. Through a café management scenario, we explored how information is stored in tables and how SQL can be used to retrieve, filter, and sort data quickly and accurately.

---

## Main Concept

### What is it?

A database is a structured collection of information that enables efficient storage, management, and retrieval of data.

Relational databases organize information into tables consisting of rows and columns.

SQL (Structured Query Language) is the language used to communicate with relational databases and retrieve specific information.

Core concepts covered:

```text
Database
Table
Row
Column
SQL Query
```

These components form the foundation of database management systems.

---

## How It Works

### Step 1: Store Information

Data is stored inside database tables.

Example:

| Order ID | Drink  | Price |
| -------- | ------ | ----- |
| 1        | Coffee | 5.00  |
| 2        | Tea    | 3.50  |

---

### Step 2: Organize Data

Tables organize information into:

```text
Columns → Data Categories
Rows → Individual Records
```

---

### Step 3: Query Information

SQL queries are used to retrieve specific information.

Example:

```sql
SELECT * FROM Orders;
```

Displays all records from the Orders table.

---

### Step 4: Filter Results

Conditions can be applied to display only relevant data.

Example:

```sql
SELECT * FROM Orders
WHERE drink = 'Coffee';
```

---

### Step 5: Sort Results

Records can be organized in ascending or descending order.

Example:

```sql
SELECT * FROM Orders
ORDER BY price DESC;
```

---

## Important Components

### Database

Stores related information in a structured format.

Example:

```text
Cafe Database
School Database
Employee Database
```

---

### Table

A collection of related records organized into rows and columns.

Example:

| ID | Drink  | Price |
| -- | ------ | ----- |
| 1  | Coffee | 5.00  |

---

### Column

Represents a specific type of information.

Examples:

```text
ID
Drink
Price
Time
```

---

### Row

Represents one complete record.

Example:

```text
Order ID: 1
Drink: Coffee
Price: 5.00
```

---

### SQL

Structured Query Language used to communicate with databases.

Example:

```sql
SELECT * FROM Orders;
```

---

### Query

A request sent to the database for information.

Examples:

```sql
SELECT
FROM
WHERE
ORDER BY
```

---

## Advantages / Benefits

* Efficient data storage.
* Fast information retrieval.
* Easy data organization.
* Simplifies reporting and analysis.
* Supports business growth.
* Improves data consistency.
* Enables automated data management.

---

## Key Characteristics

* Databases store structured information.
* Tables contain rows and columns.
* SQL retrieves and manages data.
* Queries can filter and sort records.
* Relational databases connect related information.
* Data can be accessed quickly even in large systems.

---

## Example

### Display All Orders

```sql
SELECT * FROM Orders;
```

---

### Display Specific Columns

```sql
SELECT drink, price
FROM Orders;
```

---

### Filter Records

```sql
SELECT * FROM Orders
WHERE drink = 'Coffee';
```

---

### Sort Results

```sql
SELECT * FROM Orders
ORDER BY price DESC;
```

---

### Combined Query

```sql
SELECT * FROM Orders
WHERE drink = 'Coffee'
ORDER BY price DESC;
```

---

## Key Notes

* Databases organize information efficiently.
* Tables consist of rows and columns.
* Rows represent records.
* Columns represent data categories.
* SQL is used to query relational databases.
* `SELECT` retrieves data.
* `FROM` identifies the source table.
* `WHERE` filters records.
* `ORDER BY` sorts results.
* Unauthorized modification of database records can compromise data integrity and business operations.

---

## Learning Outcome

After completing this room, I understood how relational databases store and organize information using tables, rows, and columns. I learned the purpose of SQL and how it is used to retrieve, filter, and sort information efficiently. Through practical exercises, I gained experience writing basic SQL queries using `SELECT`, `FROM`, `WHERE`, and `ORDER BY`, providing a strong foundation for future database administration, cybersecurity investigations, and data analysis tasks.

---

# Database SQL Basics — Project Report

## Objective

The objective of this room was to introduce database fundamentals and basic SQL operations. The room focused on understanding how information is organized within relational databases and how SQL queries can be used to retrieve, filter, and sort stored data efficiently.

---

## Tasks Completed

### Challenge 1

**Question:**

What is a database?

**Answer:**

```text
A database is an organized collection of data
that allows information to be stored,
managed, searched, and retrieved efficiently.
```

---

### Challenge 2

**Question:**

What are tables, rows, and columns?

**Answer:**

```text
Table  = Collection of related data.
Column = Specific type of information.
Row    = One complete record.
```

---

### Challenge 3

**Question:**

How can all records be displayed from a table?

**Answer:**

```sql
SELECT * FROM Orders;
```

---

### Challenge 4

**Question:**

How can specific columns be displayed?

**Answer:**

```sql
SELECT drink, price
FROM Orders;
```

---

### Challenge 5

**Question:**

How can records be filtered?

**Answer:**

```sql
SELECT * FROM Orders
WHERE drink = 'Coffee';
```

---

### Challenge 6

**Question:**

How can results be sorted?

**Answer:**

```sql
SELECT * FROM Orders
ORDER BY price DESC;
```

---

### Challenge 7

**Question:**

Which SQL commands were learned in this room?

**Answer:**

```text
SELECT
FROM
WHERE
ORDER BY
```

---

### Challenge 8

**Question:**

What could happen if someone were allowed to change or remove café orders without permission?

**Answer:**

```text
Unauthorized users could alter,
delete, or manipulate business records,
resulting in inaccurate reports,
financial losses,
data integrity issues,
and potential security risks.
```

---

## Skills Practiced

* Database Fundamentals
* SQL Basics
* Data Retrieval
* Data Filtering
* Data Sorting
* Table Analysis
* Understanding Rows and Columns
* Query Construction
* Relational Database Concepts
* Information Management

---

## Key Concepts Learned

* Database
* Table
* Row
* Column
* Record
* SQL
* Query
* SELECT
* FROM
* WHERE
* ORDER BY
* Data Integrity
* Access Control

---

## Conclusion

Through this room, I gained foundational knowledge of relational database systems and SQL querying. I learned how data is structured within tables, how rows and columns represent information, and how SQL commands can be used to retrieve, filter, and sort records efficiently. Additionally, I developed an understanding of the importance of data integrity and access control in database environments. This room provided a strong starting point for more advanced SQL operations, database administration, and cybersecurity-related database analysis.
