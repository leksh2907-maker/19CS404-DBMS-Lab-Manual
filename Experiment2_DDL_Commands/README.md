# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
<img width="582" height="286" alt="image" src="https://github.com/user-attachments/assets/2c046bba-1c46-4c41-be49-b2cbcf839c3b" />


```sql
-- INSERT INTO Employee(EmployeeID,Name,Department,Salary)
SELECT EmployeeID,Name,Department,Salary
FROM Former_employees;
```

**Output:**
<img width="663" height="206" alt="image" src="https://github.com/user-attachments/assets/a9406a1f-c106-428a-ac75-b79fee2121ab" />

**Question 2**
<img width="658" height="389" alt="image" src="https://github.com/user-attachments/assets/c93e11b8-a7e0-41f2-a9c9-25fb3327079c" />

```sql
-- INSERT INTO student_details(RollNo,Name,Gender,Subject,MARKS)
VALUES(205,'Olivia Green','F',NULL,NULL),
(207,'Liam Smith','M','Mathematic',85),
(208,'Sophia Johns','F','Science',NULL);
```

**Output:**
<img width="647" height="224" alt="image" src="https://github.com/user-attachments/assets/25e5dd3f-481f-4948-808a-e3f808631f53" />

**Question 3**
---
<img width="655" height="330" alt="image" src="https://github.com/user-attachments/assets/3ea1bab6-b3c7-439f-a4a0-ff2bbca9dc93" />

```sql
-- ALTER TABLE Student_details ADD MobileNumber NUMBER;
ALTER TABLE Student_details ADD Address VARCHAR(100);
```

**Output:**
<img width="661" height="318" alt="image" src="https://github.com/user-attachments/assets/f4fe361c-cd52-4767-8c61-8cf718318dc9" />

**Question 4**
---
<img width="660" height="365" alt="image" src="https://github.com/user-attachments/assets/600d1486-d935-4262-aef4-f3773cef8767" />

```sql
-- CREATE TABLE item(
    item_id TEXT primary KEY,
    item_desc TEXT NOT NULL,
    rate INTEGER NOT NULL,
    icom_id TEXT(4),
    FOREIGN KEY(icom_id) REFERENCES company(com_id) ON UPDATE SET NULL ON DELETE SET NULL
);
```

**Output:**
<img width="646" height="278" alt="image" src="https://github.com/user-attachments/assets/8c2d26c2-156e-422c-8ed1-34d7ce4e7719" />

**Question 5**
---
<img width="659" height="422" alt="image" src="https://github.com/user-attachments/assets/5353b6f7-6f15-43aa-9a36-3c4d36dc9dfd" />

```sql
-- ALTER TABLE customer
RENAME COLUMN city TO location;
```

**Output:**

<img width="630" height="250" alt="image" src="https://github.com/user-attachments/assets/2a7cdd6e-6a29-4fb2-b843-fc17a51f77f4" />

**Question 6**
---

<img width="641" height="218" alt="image" src="https://github.com/user-attachments/assets/dd738808-710d-479c-9c2d-bc95f9a1d870" />

```sql
-- INSERT INTO Products(ProductID,Name,Category)
VALUES (104,'Tablet','Electronics');
```

**Output:**

<img width="652" height="237" alt="image" src="https://github.com/user-attachments/assets/1c3ad6eb-71c9-466f-b838-51857aa8f0fe" />

**Question 7**
---
<img width="654" height="348" alt="image" src="https://github.com/user-attachments/assets/bbf0ef1d-50ab-47b4-88db-f1147a454b1a" />

```sql
-- CREATE TABLE item(
  item_id TEXT PRIMARY KEY,
  item_desc TEXT NOT NULL,
  rate INTEGER NOT NULL,
  icom_id VARCHAR(4),
  FOREIGN KEY(icom_id) REFERENCES company (com_id) ON UPDATE CASCADE ON DELETE CASCADE
);
```

**Output:**

<img width="646" height="271" alt="image" src="https://github.com/user-attachments/assets/19db63b1-5bbe-434f-9ae8-bcbc94719853" />

**Question 8**
---

<img width="637" height="311" alt="image" src="https://github.com/user-attachments/assets/ac87ff8d-3b86-499a-ae0c-c1d5f62773c4" />

```sql
---CREATE TABLE Tasks(
    TaskID INTEGER,
    TaskName TEXT,
    DueDate DATE
);
```

**Output:**
<img width="659" height="269" alt="image" src="https://github.com/user-attachments/assets/c4bed9eb-c9bc-49d0-b454-621bdb277830" />

**Question 9**
---
<img width="661" height="283" alt="image" src="https://github.com/user-attachments/assets/33f11353-b32c-443f-83ad-28abd45eabcb" />

```sql
-- CREATE TABLE Department(
 DepartmentID INTEGER PRIMARY KEY,
 DepartmentName TEXT UNIQUE NOT NULL,
 Location TEXT

);
```

**Output:**

<img width="643" height="218" alt="image" src="https://github.com/user-attachments/assets/6368980a-0b6d-4844-b0cd-bcd1b0bc96c4" />

**Question 10**
---
<img width="648" height="291" alt="image" src="https://github.com/user-attachments/assets/93ec7f33-4aa1-459b-b5bb-a03124bbe5d9" />

```sql
-- CREATE TABLE Bonuses(
     BonusID INTEGER PRIMARY KEY,
     EmployeeID INTEGER,
     BonusAmount REAL CHECK (BonusAmount>0),
     BonusDate DATE,
     Reason TEXT NOT NULL,
     FOREIGN KEY (EmployeeID)REFERENCES Employees(EmployeeID)
);
```

**Output:**

<img width="654" height="258" alt="image" src="https://github.com/user-attachments/assets/f0892741-097a-4f76-97bf-d02f3f31e997" />

## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
