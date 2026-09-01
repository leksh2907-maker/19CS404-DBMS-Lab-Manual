<img width="653" height="293" alt="image" src="https://github.com/user-attachments/assets/ce80791c-5f40-4eb0-acd7-09b5d3a142b2" /># Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- <img width="653" height="293" alt="image" src="https://github.com/user-attachments/assets/d84d5b25-9752-4e85-9cb4-3ae5905ce89a" />


```sql
-- UPDATE Products
SET quantity = quantity * 1.10;
```

**Output:**
<img width="640" height="447" alt="image" src="https://github.com/user-attachments/assets/b6644165-1827-4235-9e49-faf9bc0bd5fe" />

**Question 2**
---
<img width="636" height="222" alt="image" src="https://github.com/user-attachments/assets/c5cf84e5-acc3-4f39-86f5-081b213a2737" />

```sql
--UPDATE Products
SET product_name='Grapefruit'
WHERE product_id=4;
```

**Output:**
<img width="653" height="244" alt="image" src="https://github.com/user-attachments/assets/d942c468-244e-4abd-8b54-fbd1717e50c1" />

**Question 3**
---
--<img width="651" height="505" alt="image" src="https://github.com/user-attachments/assets/39b4f853-7049-497e-b1d7-c1b6b1587b98" />


```sql
---- UPDATE employees
SET salary=salary*2
WHERE department_id=20
    AND job_id LIKE '%MAN';
```

**Output:**
<img width="636" height="277" alt="image" src="https://github.com/user-attachments/assets/25b9cf69-27a4-4f0c-9257-3a6a549ba3b4" />


**Question 4**
---
<img width="650" height="298" alt="image" src="https://github.com/user-attachments/assets/c7c9b5f0-5669-41b1-bcbd-458b8d7b9b1a" />

```sql
-- UPDATE suppliers
SET supplier_name='A1 Suppliers'
WHERE supplier_id=8;
```

**Output:**
<img width="645" height="358" alt="image" src="https://github.com/user-attachments/assets/99d5055a-f9eb-48bb-8f4f-90aaaefe662a" />

**Question 5**
---
<img width="659" height="366" alt="image" src="https://github.com/user-attachments/assets/c0464711-9b9a-4731-a0ca-ac6ed0f5efd6" />

```sql
-- UPDATE suppliers
SET supplier_name=UPPER(supplier_name)
WHERE contact_person LIKE '%Singh%';
```

**Output:**
<img width="647" height="344" alt="image" src="https://github.com/user-attachments/assets/4ca15cb5-895a-4ba1-bb12-165a243a1c1f" />

**Question 6**
<img width="655" height="176" alt="image" src="https://github.com/user-attachments/assets/56d39395-f5ee-4de2-a225-33382f202977" />


```sql
-- -- DELETE FROM Doctors
WHERE specialization='Pediatrics'
    AND first_name = 'Michael';
```

**Output:**
<img width="645" height="323" alt="image" src="https://github.com/user-attachments/assets/c2a44ae7-294e-4603-bf67-5b0979e9bcde" />

**Question 7**
---
-- <img width="647" height="364" alt="image" src="https://github.com/user-attachments/assets/df3cc934-374e-433f-8fa6-5241aed32bb7" />


```sql
-- DELETE FROM Customer
WHERE GRADE %2!=0;
```

**Output:**
<img width="646" height="327" alt="image" src="https://github.com/user-attachments/assets/2b2e94e4-da97-4577-82b0-ad9f29f19d56" />

**Question 8**
---
-- <img width="651" height="403" alt="image" src="https://github.com/user-attachments/assets/b28a2418-0521-44dc-b6e5-d72779368202" />

```sql
-- DELETE FROM Customer 
WHERE (GRADE>2 AND  PAYMENT_AMT<(SELECT AVG(PAYMENT_AMT) FROM Customer))
    OR OUTSTANDING_AMT>8000;
```

**Output:**
<img width="619" height="497" alt="image" src="https://github.com/user-attachments/assets/e922cbf8-6a74-4372-855e-96303c0699fa" />


**Question 9**
---
<img width="653" height="458" alt="image" src="https://github.com/user-attachments/assets/a01fb03a-519c-404d-b149-fd159e457dda" />


```sql
-- DELETE FROM Customer
WHERE CUST_NAME LIKE '%Holmes%';
```

**Output:**

<img width="652" height="434" alt="image" src="https://github.com/user-attachments/assets/ad65be81-3ca1-488a-983f-33e667c3d835" />


**Question 10**
---
<img width="667" height="416" alt="image" src="https://github.com/user-attachments/assets/7df2ef3b-3f49-4fe4-925a-ab50d1813da6" />


```sql
-- DELETE FROM Doctors
WHERE specialization IS NULL;
```

**Output:**
<img width="647" height="468" alt="image" src="https://github.com/user-attachments/assets/be8c25f3-7d31-4aee-9e02-113d2e68ce94" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
