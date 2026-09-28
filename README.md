# 🗄️ MySQL Data Transformer

> A practical SQL project focused on data transformation, analysis, and relational database operations using MySQL.

## 📌 Overview

**MySQL Data Transformer** is a database project created to practice SQL and understand how data can be transformed into useful information.

The project works with multiple related tables and demonstrates how SQL can be used to retrieve, connect, filter, and analyze data efficiently.

## ✨ Features

* 🔹 Retrieve required data from tables
* 🔹 Filter records using conditions
* 🔹 Combine data using `JOIN`
* 🔹 Perform calculations using aggregate functions
* 🔹 Use subqueries for advanced filtering
* 🔹 Remove duplicate results using `DISTINCT`
* 🔹 Analyze customer and order information
* 🔹 Transform raw database records into meaningful results

## 🧩 Tables Used

### 👥 Customers

Stores customer-related information such as customer ID and name.

### 👨‍💼 Employees

Stores employee-related information.

### 🛒 Orders

Stores customer orders and order amounts.

## 🧠 SQL Skills Demonstrated

```text
SELECT
WHERE
DISTINCT
JOIN
GROUP BY
ORDER BY
COUNT()
SUM()
AVG()
MIN()
MAX()
Subqueries
```

## 🔎 Sample Analysis

The project includes queries that can identify customers based on their order activity and compare individual order values with overall order statistics.

Example:

```sql
SELECT DISTINCT
    C.CustomerID,
    C.FirstName,
    C.LastName
FROM Customers C
JOIN Orders O
    ON C.CustomerID = O.CustomerID
WHERE O.TotalAmount > (
    SELECT AVG(TotalAmount)
    FROM Orders
);
```

### 📈 Result

This query identifies customers whose order amount is **greater than the average order amount** across the Orders table.

## 🛠️ Tech Stack

| Technology | Usage              |
| ---------- | ------------------ |
| MySQL      | Database           |
| SQL        | Data querying      |
| GitHub     | Project repository |

## 📂 Repository

```text
MYSQL_PROJECT
│
├── PR_2_Data Transformer.txt
│
└── README.md
```

## ▶️ Getting Started

### Clone the Repository

```bash
git clone https://github.com/tankkevanshi/MYSQL_PROJECT.git
```

### Open MySQL

```sql
USE data_transfer;
```

Then execute the queries from:

```text
PR_2_Data Transformer.txt
```

## 🎯 Purpose

This project was created to strengthen practical knowledge of **MySQL, SQL queries, data transformation, and relational database concepts**.

It can also serve as a foundation for larger **Data Analytics and Database projects**.

## 👩‍💻 Author

### Kevanshi Tank

GitHub: **@tankkevanshi**

---

⭐ **MySQL | SQL | Data Transformation | Data Analysis**
