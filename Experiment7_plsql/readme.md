# Experiment 7: PL/SQL – Variables, Control Structures and Loops
NAME: LEKSHMEENDHRA S
REG NO:212225040198

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Greater number is: 80
program
```
DECLARE
    n NUMBER := 10;     -- Value of N
    i NUMBER := 1;      -- Counter variable
    sum NUMBER := 0;    -- Initialize sum
BEGIN
    WHILE i <= n LOOP
        sum := sum + i; -- Add current number to sum
        i := i + 1;     -- Increment counter
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || sum);
END;

```
output 
<img width="515" height="106" alt="image" src="https://github.com/user-attachments/assets/a88601cc-ed14-44ee-a351-503bc6e44259" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Sum of first 10 natural numbers is: 55
program
```
DECLARE
    n NUMBER := 10;     -- Value of N
    i NUMBER := 1;      -- Counter variable
    sum NUMBER := 0;    -- Initialize sum
BEGIN
    WHILE i <= n LOOP
        sum := sum + i; -- Add current number to sum
        i := i + 1;     -- Increment counter
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || sum);
END;

```
output 

<img width="570" height="112" alt="image" src="https://github.com/user-attachments/assets/e4ee6cd5-6e60-425d-85d3-770705b98928" />


## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8
program
```
SET SERVEROUTPUT ON;
DECLARE
    num NUMBER := &n;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
    i NUMBER := 3;
BEGIN
    DBMS_OUTPUT.PUT_LINE('n = ' || num);
    DBMS_OUTPUT.PUT('Fibonacci sequence: ' || a || ', ' || b);

    WHILE i <= num LOOP
        c := a + b;
        DBMS_OUTPUT.PUT(', ' || c);
        a := b;
        b := c;
        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.NEW_LINE;
END;


```
output 
<img width="317" height="116" alt="image" src="https://github.com/user-attachments/assets/cea79cf5-fcdb-4166-a7da-1eb4fa66daa3" />

---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351
program
```
DECLARE
    n NUMBER := 1535;
    remainder NUMBER;
    reverse_num NUMBER := 0;
BEGIN
    WHILE n > 0 LOOP
        remainder := MOD(n,10);
        reverse_num := reverse_num * 10 + remainder;
        n := TRUNC(n/10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reversed number is ' || reverse_num);
END;
```
output
<img width="306" height="106" alt="image" src="https://github.com/user-attachments/assets/913ac743-7ebe-4683-9785-a9cb6c125548" />

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15
program
```
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
BEGIN
    IF a > b AND a > c THEN
        DBMS_OUTPUT.PUT_LINE('Largest number is ' || a);
    ELSIF b > a AND b > c THEN
        DBMS_OUTPUT.PUT_LINE('Largest number is ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest number is ' || c);
    END IF;
END;
```
output
<img width="365" height="109" alt="image" src="https://github.com/user-attachments/assets/ef21b32e-ad9f-43e1-a2ce-49fa52ef0736" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
