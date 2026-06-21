# Database SQL Basics — Study Note

## Understanding Tables, Rows, and Columns

### Overview

Databases organize information in a structured format that allows computers to store, search, retrieve, and manage large amounts of data efficiently. The primary structure used in relational databases is the table, which consists of rows and columns.

Understanding tables, rows, and columns is essential because they form the foundation of how information is stored and queried using SQL.

---

## Main Concept

### What is it?

A relational database stores information inside tables.

A table is similar to a spreadsheet where data is organized into:

```text
Columns (Fields)
Rows (Records)
```

Each row contains a complete set of information, while each column stores a specific type of data.

For example, in a café order system:

| Order ID | Drink  | Price | Time  |
| -------- | ------ | ----- | ----- |
| 1        | Coffee | 5.00  | 09:00 |
| 2        | Tea    | 3.50  | 09:15 |

This table stores customer order information in a structured format.

---

## How It Works

### Step 1: Data is Collected

The café records information such as:

```text
Drink Name
Price
Order Time
Order Number
```

---

### Step 2: Data is Stored in a Table

The information is organized into rows and columns.

Example:

| Order ID | Drink  | Price | Time  |
| -------- | ------ | ----- | ----- |
| 1        | Coffee | 5.00  | 09:00 |
| 2        | Tea    | 3.50  | 09:15 |

---

### Step 3: Columns Define Data Types

Each column stores a specific category of information.

Example:

```text
Order ID
Drink
Price
Time
```

---

### Step 4: Rows Store Individual Records

Each row represents one complete café order.

Example:

```text
Order ID: 1
Drink: Coffee
Price: 5.00
Time: 09:00
```

This entire record is stored in a single row.

---

### Step 5: SQL Queries Retrieve Data

Users can ask questions about stored information.

Example:

```sql
SELECT * FROM Orders;
```

The database searches the table and returns matching records.

---

## Important Components

### Database

A structured collection of information stored electronically.

Example:

```text
Cafe Database
School Database
Employee Database
```

---

### Table

A collection of related information organized into rows and columns.

Example:

| Order ID | Drink  | Price |
| -------- | ------ | ----- |
| 1        | Coffee | 5.00  |
| 2        | Tea    | 3.50  |

---

### Column

A column represents one type of information.

Examples:

```text
Order ID
Drink Name
Price
Time
```

Columns are the vertical sections of a table.

---

### Row

A row represents one complete record.

Example:

| Order ID | Drink  | Price |
| -------- | ------ | ----- |
| 1        | Coffee | 5.00  |

This entire entry is a single row.

**Important:**

```text
One Row = One Complete Record
```

In the café example:

```text
One Row = One Café Order
```

---

### Record

A record is another name for a row.

Example:

```text
Customer Record
Employee Record
Order Record
```

---

### SQL Query

A command used to retrieve information from a database.

Example:

```sql
SELECT * FROM Orders;
```

---

## Advantages / Benefits

* Organizes data efficiently.
* Simplifies data management.
* Enables fast searching and filtering.
* Supports large volumes of information.
* Reduces manual record keeping.
* Makes reporting and analysis easier.
* Improves data accuracy and consistency.

---

## Key Characteristics

* Databases store information in tables.
* Tables contain rows and columns.
* Columns define data categories.
* Rows contain complete records.
* New records create new rows.
* SQL is used to retrieve information.
* Queries can search, sort, and display data quickly.

---

## Example

### Café Orders Table

| Order ID | Drink  | Price | Time  |
| -------- | ------ | ----- | ----- |
| 1        | Coffee | 5.00  | 09:00 |
| 2        | Tea    | 3.50  | 09:15 |
| 3        | Latte  | 6.00  | 09:30 |

---

### Understanding the Structure

Columns:

```text
Order ID
Drink
Price
Time
```

Rows:

```text
Row 1 = Coffee Order
Row 2 = Tea Order
Row 3 = Latte Order
```

---

### Example SQL Questions

Show all orders:

```sql
SELECT * FROM Orders;
```

Show only coffee orders:

```sql
SELECT * FROM Orders
WHERE Drink = 'Coffee';
```

Find the cheapest drink:

```sql
SELECT * FROM Orders
ORDER BY Price ASC;
```

---

## Key Notes

* A database is a structured collection of data.
* Information is stored in tables.
* Columns define the type of information.
* Rows contain complete records.
* One row represents one café order in the example.
* SQL is used to query databases.
* Queries retrieve information without modifying data.
* Relational databases organize data efficiently for large-scale use.

---

## Learning Outcome

After completing this section, I understood how relational databases organize information using tables, rows, and columns. I learned that columns define categories of data while rows store complete records. I also gained an understanding of how SQL queries are used to retrieve information from tables efficiently, allowing users to search, filter, and analyze data without manually reviewing individual records.

---

# Database SQL Basics — Project Report

## Objective

The objective of this section was to understand how relational databases organize information using tables, rows, and columns. The lesson introduced the structure of database tables and demonstrated how SQL queries can be used to retrieve information efficiently from stored records.

---

## Tasks Completed

### Challenge 1

**Question:**

In a café database table, what does one row represent?

**Answer:**

```text
One complete café order.
```

---

### Challenge 2

**Question:**

What does a column represent in a database table?

**Answer:**

```text
A column represents one type of information,
such as a drink name, price, order number,
or order time.
```

---

### Challenge 3

**Question:**

What does a row represent in a database table?

**Answer:**

```text
A row represents one complete record
containing all related information.
```

---

### Challenge 4

**Question:**

What is a database?

**Answer:**

```text
A database is an organized collection of data
that allows information to be stored,
managed, searched, and retrieved efficiently.
```

---

### Challenge 5

**Question:**

What is an SQL query?

**Answer:**

```text
An SQL query is a command used to ask
questions and retrieve information
from a database.
```

---

## Skills Practiced

* Database Fundamentals
* Understanding Table Structures
* Data Organization
* Identifying Rows and Columns
* SQL Concepts
* Data Retrieval Concepts
* Relational Database Fundamentals

---

## Key Concepts Learned

* Database
* Table
* Row
* Column
* Record
* SQL Query
* Data Organization
* Data Storage
* Data Retrieval
* Relational Databases

---

## Conclusion

Through this section, I gained a clear understanding of how relational databases organize information using tables, rows, and columns. I learned that each row represents a complete record while columns define specific categories of information. Additionally, I explored how SQL queries allow users to retrieve and analyze data efficiently, providing a strong foundation for working with database systems and performing data-driven operations in future SQL exercises.
