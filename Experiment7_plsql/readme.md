## Name : Vignesh S
## Reg No : 212224110061
# Experiment 7: PL/SQL – Variables, Control Structures and Loops

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

### Program :
```
DECLARE
    a NUMBER := 25;
    b NUMBER := 15;
BEGIN
    IF a > b THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || a);
    ELSIF b > a THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Both numbers are equal');
    END IF;
END;
```

<img width="1917" height="1087" alt="image" src="https://github.com/user-attachments/assets/83c262a8-e489-49a9-8ec2-9b4d106eb68e" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Sum of first 10 natural numbers is: 55

### Program :

```
DECLARE
    n NUMBER := 10;
    total NUMBER := 0;
BEGIN
    FOR i IN 1..n LOOP
        total := total + i;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || total);
END;

```
<img width="1915" height="1085" alt="image" src="https://github.com/user-attachments/assets/586f1602-4cdb-48ac-bc3e-c65c69fdd43c" />

---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

### Program :

```
DECLARE
    n NUMBER := 10;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci Series:');

    FOR i IN 1..n LOOP
        DBMS_OUTPUT.PUT_LINE(a);

        c := a + b;
        a := b;
        b := c;
    END LOOP;
END;

```

<img width="1917" height="1086" alt="image" src="https://github.com/user-attachments/assets/2fa93146-18e0-4284-86ed-b58d5e2baeb7" />


---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351

### Program :

```
DECLARE
    n NUMBER := 12345;
    rev NUMBER := 0;
    rem NUMBER;
BEGIN
    WHILE n > 0 LOOP
        rem := MOD(n, 10);
        rev := rev * 10 + rem;
        n := TRUNC(n / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reverse number is: ' || rev);
END;

```

<img width="1917" height="1092" alt="image" src="https://github.com/user-attachments/assets/1d50b3c5-ca88-4702-a71a-56166d75ad43" />

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

### Program :
```
DECLARE
    a NUMBER := 10;
    b NUMBER := 45;
    c NUMBER := 30;
BEGIN
    IF a >= b AND a >= c THEN
        DBMS_OUTPUT.PUT_LINE('Largest number is: ' || a);
    ELSIF b >= a AND b >= c THEN
        DBMS_OUTPUT.PUT_LINE('Largest number is: ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest number is: ' || c);
    END IF;
END;
```

<img width="1917" height="1030" alt="image" src="https://github.com/user-attachments/assets/38ec4649-114f-49ba-9aab-b673e4220cf9" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
