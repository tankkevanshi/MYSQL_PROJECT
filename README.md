# 🔎 Project 1 — Data Digger

> **Advanced MySQL E-Commerce Data Analysis & Database Querying**

## 📌 Project Overview

**Data Digger** is a practical MySQL database project designed to demonstrate how relational databases can be created, populated, queried, and analyzed to extract meaningful information from e-commerce data.

The project uses an **`ecommerce_store`** database and demonstrates the complete SQL workflow — from database and table creation to data insertion, validation, filtering, aggregation, and analytical querying.

The project also documents actual MySQL CLI execution, including database creation, table definitions, query execution, and error correction.

---

# 🎯 Project Objectives

The project focuses on developing practical SQL and database-management skills through:

* Relational database creation
* Table design and primary keys
* Structured data insertion
* Data retrieval and filtering
* Sorting and grouping
* Aggregate calculations
* Multi-condition analysis
* Data validation
* SQL error identification and correction
* Business-oriented e-commerce analysis

---

# 🏗️ Database Architecture

```text
                    E-COMMERCE STORE
                           │
                           ▼
                 ┌──────────────────┐
                 │  ecommerce_store  │
                 └────────┬─────────┘
                          │
             ┌────────────┴────────────┐
             │                         │
             ▼                         ▼
     ┌───────────────┐        ┌────────────────┐
     │   Customers   │        │     Orders     │
     ├───────────────┤        ├────────────────┤
     │ CustomerID PK │        │ OrderID        │
     │ Name          │        │ CustomerID     │
     │ Email         │        │ OrderDate      │
     │ Address       │        │ Amount         │
     └───────────────┘        └────────────────┘
```

> The schema diagram represents the analytical structure of the project; additional tables can be added as the project evolves.

---

# 🗄️ Database Setup

The project creates the following database:

```sql
CREATE DATABASE ecommerce_store;
```

The database is then selected using:

```sql
USE ecommerce_store;
```

The project verifies the database environment with:

```sql
SHOW DATABASES;
```

The actual execution log in the repository confirms successful creation and selection of `ecommerce_store`.

---

# 👥 Customer Data Model

The `Customers` table contains core customer information.

```sql
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    Name VARCHAR(10),
    Email VARCHAR(100),
    Address VARCHAR(200)
);
```

### Schema

| Column       | Data Type | Key | Purpose                    |
| ------------ | --------- | --- | -------------------------- |
| `CustomerID` | INT       | PK  | Unique customer identifier |
| `Name`       | VARCHAR   | —   | Customer name              |
| `Email`      | VARCHAR   | —   | Customer email             |
| `Address`    | VARCHAR   | —   | Customer location          |

The repository's execution output confirms the table structure and `CustomerID` primary key.

---

# 🔄 Data Ingestion

Customer records are inserted using multi-row `INSERT` statements.

```sql
INSERT INTO Customers
(CustomerID, Name, Email, Address)
VALUES
(1, 'Alice', 'alice@gmail.com', 'Surat'),
(2, 'Bob', 'bob@gmail.com', 'Ahmdabad'),
(3, 'Charlie', 'charlie@gmail.com', 'Vadodra'),
(4, 'David', 'david@gmail.com', 'Mumbai');
```

This demonstrates efficient insertion of multiple records in a single SQL statement.

---

# 🧪 SQL Error Handling & Debugging

One useful aspect of the project is that it records an actual SQL syntax error and its subsequent correction.

### Initial issue

```sql
INSERT INTO Customers (...) VALEUS
```

The incorrect keyword produced:

```text
ERROR 1064 (42000)
```

The query was then corrected to:

```sql
INSERT INTO Customers (...) VALUES
```

This demonstrates an important practical SQL development workflow:

```text
Write Query
    ↓
Execute
    ↓
Identify Error
    ↓
Analyze Error Message
    ↓
Correct Syntax
    ↓
Re-Execute
    ↓
Validate Result
```

The error and corrected execution are documented directly in the project file.

---

# 🔍 SQL Operations Covered

## 1. Database Management

```text
CREATE DATABASE
USE
SHOW DATABASES
```

## 2. Table Management

```text
CREATE TABLE
DESC
SHOW TABLES
```

## 3. Data Manipulation

```text
INSERT
SELECT
UPDATE
DELETE
```

## 4. Data Filtering

```text
WHERE
AND
OR
IN
BETWEEN
LIKE
```

## 5. Sorting

```text
ORDER BY
ASC
DESC
```

## 6. Aggregation

```text
COUNT()
SUM()
AVG()
MIN()
MAX()
```

## 7. Group Analysis

```text
GROUP BY
HAVING
```

## 8. Relational Analysis

```text
INNER JOIN
LEFT JOIN
RIGHT JOIN
```

---

# 📊 Analytical Workflow

```text
             Raw E-Commerce Data
                     │
                     ▼
             Database Creation
                     │
                     ▼
               Table Design
                     │
                     ▼
              Data Insertion
                     │
                     ▼
             Data Validation
                     │
                     ▼
             Data Filtering
                     │
                     ▼
          Aggregation & Grouping
                     │
                     ▼
             Relational Analysis
                     │
                     ▼
              Business Insights
```

---

# 💼 Business Questions

The project can be used to answer practical e-commerce questions such as:

### Customer Analysis

* How many customers are registered?
* Which customers belong to a particular location?
* How can customer records be filtered?
* How can customer information be sorted?
* How can duplicate or repeated information be identified?

### Order Analysis

* What is the total order value?
* Which orders have the highest value?
* What is the average order amount?
* How many orders were placed?
* Which customers generated the highest order value?

### Data Quality

* Are customer identifiers unique?
* Are required fields populated?
* Are email values consistent?
* Are duplicate records present?
* Are location values standardized?

---

# 🧠 Key SQL Concepts

| Category          | Concepts                                |
| ----------------- | --------------------------------------- |
| Database          | `CREATE DATABASE`, `USE`                |
| Schema            | `CREATE TABLE`, `DESC`                  |
| Data Manipulation | `INSERT`, `UPDATE`, `DELETE`            |
| Retrieval         | `SELECT`                                |
| Filtering         | `WHERE`, `IN`, `BETWEEN`, `LIKE`        |
| Sorting           | `ORDER BY`                              |
| Aggregation       | `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`     |
| Grouping          | `GROUP BY`, `HAVING`                    |
| Relationships     | `JOIN`                                  |
| Validation        | Schema inspection & result verification |
| Debugging         | SQL error identification & correction   |

---

# 🛠️ Technology Stack

```text
Database      : MySQL
Language      : SQL
Interface     : MySQL Command Line
Version       : MySQL 9.x
Repository    : GitHub
Project Type  : Relational Database / E-Commerce Analytics
```

The repository execution log records MySQL Community Server **9.7.2** during the documented run.

---

# 📂 Project Structure

```text
MYSQL_PROJECT/
│
├── project 1_Data Digger.txt
│
└── README.md
```

---

# ▶️ How to Run

### Step 1 — Start MySQL

Open MySQL Workbench or MySQL Command Line.

### Step 2 — Create the Database

```sql
CREATE DATABASE ecommerce_store;
```

### Step 3 — Select the Database

```sql
USE ecommerce_store;
```

### Step 4 — Create the Tables

Execute the table-creation queries from:

```text
project 1_Data Digger.txt
```

### Step 5 — Insert Data

Run the provided `INSERT` statements.

### Step 6 — Verify the Schema

```sql
SHOW TABLES;
```

and:

```sql
DESC Customers;
```

### Step 7 — Execute Analytical Queries

Run the remaining SQL queries to perform data exploration and analysis.

---

# 📈 Expected Outcomes

After executing the project, users can obtain:

* Structured customer datasets
* Filtered customer information
* Aggregated business metrics
* Order-level analysis
* Customer-level analysis
* Location-based analysis
* Sorted analytical results
* Validated relational data
* Practical SQL debugging experience

---

# 🧩 Skills Demonstrated

```text
✓ MySQL
✓ SQL
✓ Relational Database Design
✓ Primary Keys
✓ Data Modeling
✓ CRUD Operations
✓ Data Insertion
✓ Data Filtering
✓ Data Aggregation
✓ GROUP BY / HAVING
✓ JOIN Operations
✓ Data Validation
✓ SQL Debugging
✓ E-Commerce Data Analysis
✓ Command-Line SQL Execution
```

---

# 🚀 Future Enhancements

The project can be expanded into a complete e-commerce analytics system by adding:

* `Products` table
* `Categories` table
* `OrderDetails` table
* Foreign-key relationships
* Product inventory analysis
* Customer segmentation
* Revenue dashboards
* Monthly sales analysis
* Customer lifetime value
* Views
* Stored procedures
* Common Table Expressions `(CTEs)`
* Window functions
* Index optimization
* Query performance analysis

### Possible Advanced Architecture

```text
Customers
    │
    └───────┐
            ▼
          Orders ────────── OrderDetails
                               │
                               ▼
                           Products
                               │
                               ▼
                           Categories
```

---

# 🎓 Learning Outcomes

This project provides hands-on experience with the complete SQL development cycle:

```text
DATABASE
   ↓
SCHEMA
   ↓
DATA
   ↓
QUERY
   ↓
DEBUG
   ↓
ANALYZE
   ↓
INSIGHT
```

The main focus is not only writing SQL queries, but also understanding how relational data can be structured, validated, transformed, and analyzed for practical use cases.

---

# 👩‍💻 Author

**Kevanshi Tank**

**Project:** Data Digger
**Domain:** E-Commerce Data Analysis
**Technology:** MySQL / SQL

---

## ⭐ Project Highlights

> **Data Digger transforms raw e-commerce records into structured, queryable information using practical SQL and relational database concepts.**

**Built with MySQL • Structured with SQL • Analyzed with Data**

