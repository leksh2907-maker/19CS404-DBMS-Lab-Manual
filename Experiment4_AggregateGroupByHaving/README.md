# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
How many appointments are scheduled for each doctor?

```sql
SELECT DoctorID, COUNT(*) AS TotalAppointments
FROM Appointments
GROUP BY DoctorID
ORDER BY DoctorID;
```

**Output:**
<img width="574" height="506" alt="image" src="https://github.com/user-attachments/assets/e84b81a5-df08-42d9-8b86-58cfd0ad4ff5" />

**Question 2**
---
What is the average dosage prescribed for each medication?

```sql
SELECT Medication,AVG(Dosage) AS AvgDosage
FROM Prescriptions
GROUP BY Medication
ORDER BY Medication;
```

**Output:**
<img width="519" height="612" alt="image" src="https://github.com/user-attachments/assets/d04918be-83fd-4bff-bbf6-4855b3dcc71b" />

**Question 3**
---
How many patients are there in each city?

```sql
SELECT Address,COUNT(*) AS TotalPatients
FROM Patients
GROUP BY Address
ORDER BY Address;
```

**Output:**

<img width="506" height="334" alt="image" src="https://github.com/user-attachments/assets/54a5df50-ced6-49e1-b574-1cdf792a1a1b" />


**Question 4**
---
Write a SQL query to return the total number of rows in the 'customer' table where the city is not Noida.
```sql
SELECT COUNT(*) AS COUNT FROM customer
WHERE city!='Noida';
```

**Output:**
<img width="262" height="222" alt="image" src="https://github.com/user-attachments/assets/d04d4d76-34cd-43da-b9a2-f9ff21797e9e" />

**Question 5**
---
Write a SQL query to calculate the average purchase amount of all orders. Return average purchase amount.

Sample table: orders

ord_no purch_amt ord_date customer_id salesman_id
70001 150.5 2012-10-05 3005 5002

70009 270.65 2012-09-10 3001 5005

70002 65.26 2012-10-05 3002 5001

```sql
SELECT AVG(purch_amt) AS AVERAGE
FROM orders;
```

**Output:**
<img width="278" height="237" alt="image" src="https://github.com/user-attachments/assets/da4381a0-9523-4517-9a81-14e431084034" />

**Question 6**
---
Write a SQL query to determine the number of customers who received at least one grade for their activity.

Sample table: customer

customer_id | cust_name | city | grade | salesman_id

-------------+----------------+------------+-------+-------------
```sql
    3002 | Nick Rimando   | New York   |   100 |        5001

    3007 | Brad Davis     | New York   |   200 |        5001

    3005 | Graham Zusi    | California |   200 |        5002

SELECT COUNT(*) AS COUNT FROM customer
WHERE grade IS NOT NULL;
```

**Output:**
<img width="270" height="203" alt="image" src="https://github.com/user-attachments/assets/86847507-32bd-4727-88ac-f740c8551792" />

**Question 7**
---
Write a SQL query to find how many employees have an income greater than 50K?

Table: employee

name type
id INTEGER name TEXT age INTEGER city TEXT income INTEGER

```sql
SELECT COUNT(*) AS employees_count FROM employee
WHERE income>50000;
```

**Output:**
<img width="345" height="204" alt="image" src="https://github.com/user-attachments/assets/c4f53f66-b679-4f69-863a-cff971f29384" />

**Question 8**
---
Write the SQL query that achieves the grouping of data by age intervals using the expression (age/5)5, calculates the total salary sum for each group, and excludes groups where the total salary sum is not greater than 5000.

```sqlSELECT (age/5)*5 AS age_group,SUM(salary)
FROM customer1
GROUP BY age_group
HAVING SUM(salary)>5000;
```

**Output:**
<img width="474" height="278" alt="image" src="https://github.com/user-attachments/assets/ccdcc229-a386-4cba-8695-f32f34cb4203" />

**Question 9**
---
Write the SQL query that achieves the grouping of data by city, calculates the average income for each city, and includes only those cities where the average income is greater than 500,000
```sql
SELECT city,AVG(income)
FROM employee
GROUP BY city
HAVING AVG(income)>500000;
```

**Output:**
<img width="478" height="330" alt="image" src="https://github.com/user-attachments/assets/1bb6e0be-6151-46c6-87c3-2b81e853855b" />

**Question 10**
Write the SQL query that achieves the grouping of data by occupation, calculates the average work hours for each occupation, and includes only those occupations where the average work hour falls between 10 and 12.
```sql
SELECT occupation,AVG(workhour)
FROM employee1
GROUP BY occupation
HAVING AVG(workhour) BETWEEN 10 AND 12;
```

**Output:**
<img width="513" height="302" alt="image" src="https://github.com/user-attachments/assets/1ca9a430-324a-454f-a090-5e68a8bfb437" />

## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
