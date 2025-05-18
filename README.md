# DbStudent-SQL-Scripts



---

````markdown
# 📊 SQL Server Project – Employee & Trainee Management

This repository contains structured SQL scripts created using **Microsoft SQL Server Management Studio (SSMS)**. It includes schema creation, data insertion, and queries for managing simple `Trainees` and `Employee1` tables.

---

## ✅ Project Summary

This project was created as part of SQL practice to understand:
- Table creation
- Identity columns
- Data insertion
- Querying
- Altering tables
- Dropping tables and databases

---

## 🏗️ Tables Created

### 1. `Trainees`
```sql
CREATE TABLE Trainees (
    Trainee_ID INT NOT NULL PRIMARY KEY IDENTITY,
    Name VARCHAR NOT NULL,
    Age INT NOT NULL,
    Address VARCHAR(100)
);
````

### 2. `Employee1`

```sql
CREATE TABLE Employee1 (
    Employee_ID INT NOT NULL PRIMARY KEY IDENTITY(1,1),
    Name VARCHAR(100) NOT NULL,
    Gender VARCHAR(100) NOT NULL,
    Age INT NOT NULL,
    Address VARCHAR(100),
    Email_ID VARCHAR(100) NOT NULL,
    Department VARCHAR(100) NOT NULL,
    Salary INT NOT NULL
);
```

---

## 📝 Sample Inserts

```sql
-- Trainees table inserts
INSERT INTO Trainees VALUES ('r', 34, 'pune');
INSERT INTO Trainees VALUES ('m', 30, 'mumbai'), ('s', 31, 'nashik');

-- Employee1 table inserts
INSERT INTO Employee1 VALUES 
('Rupali', 'Female', 33, 'pune', 'rupali@gmail.com', 'IT', 96000),
('Dipali', 'Female', 34, 'pune', 'dipali@gmail.com', 'IT', 36000),
('Rashmi', 'Female', 35, 'Nashik', 'rashmi@gmail.com', 'Testing', 35000),
('Rahul', 'Male', 33, 'hyd', 'rahul@gmail.com', 'HR', 66000),
('Swaroop', 'Male', 29, 'Mumbai', 'swaroop@gmail.com', 'IT', 48000);
```

---

## 🔧 Alter Table Operations

```sql
-- Change column data types or constraints
ALTER TABLE Employee1 ALTER COLUMN Email_ID VARCHAR(100) NOT NULL;
ALTER TABLE Employee1 ALTER COLUMN Department VARCHAR(100) NOT NULL;
ALTER TABLE Employee1 ALTER COLUMN Salary INT NOT NULL;
```

---

## 📌 Useful Commands for Reference

```sql
-- List all databases
SELECT name FROM sys.databases;

-- Drop a database
DROP DATABASE DbStudent;

-- Drop a table
DROP TABLE Employee1;

-- View data
SELECT * FROM Trainees;
SELECT * FROM Employee1;

-- Reset identity value (after deleting all rows)
DBCC CHECKIDENT ('Employee1', RESEED, 0);
```

---

## 📂 Tools Used

* Microsoft SQL Server Management Studio (SSMS)
* SQL Server (local instance)

---

## 👤 Author

Created by: *Pramod Kumar D*
Purpose: SQL practice & database understanding
Date: *May 2025*
