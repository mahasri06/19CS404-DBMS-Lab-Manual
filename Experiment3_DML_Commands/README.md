# Experiment 3: DML Commands

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
![image](https://github.com/user-attachments/assets/c2d351d4-10b6-49d3-bead-64264ff48f69)

```sql
UPDATE suppliers SET supplier_name='A1 Suppliers' WHERE supplier_id=8;
```

**Output:**

![image](https://github.com/user-attachments/assets/30b3c41b-0970-4ccd-b85b-99963df1412c)

**Question 2**
---
![image](https://github.com/user-attachments/assets/e44ed983-0975-4659-8adf-db3d5589347b)

```sql
UPDATE customer SET grade=5 WHERE city='Chennai';
```

**Output:**

![image](https://github.com/user-attachments/assets/e6d5d804-1710-4b73-9106-f06ed8912664)

**Question 3**
---
![image](https://github.com/user-attachments/assets/58f6aed5-f1a5-4eb7-b58a-a5aa5c3fff80)

```sql
UPDATE Employees SET salary=round(salary*1.25,1) WHERE department_id=40;
UPDATE Employees SET salary=round(salary*1.15,1) WHERE department_id=90;
UPDATE Employees SET salary=round(salary*1.1,1) WHERE department_id=110;
```

**Output:**

![image](https://github.com/user-attachments/assets/1002a362-2fda-4287-85a7-dbbdffac6d2e)

**Question 4**
---
![image](https://github.com/user-attachments/assets/3ccc396d-3179-4ece-9160-082a63c7c82a)

```sql
UPDATE Suppliers SET address="58 Lakeview, Magnolia" WHERE supplier_id=5;
```

**Output:**

![image](https://github.com/user-attachments/assets/7d114b78-12dd-4019-8f20-1d42f70eae3e)

**Question 5**
---
![image](https://github.com/user-attachments/assets/5dbc0632-93f6-460b-b4fc-eef1a07e4797)

```sql
UPDATE products SET product_name='Premium Bread' WHERE product_id=5;
```

**Output:**

![image](https://github.com/user-attachments/assets/a68644de-74e8-4479-a139-2e231ea21666)

**Question 6**
---
![image](https://github.com/user-attachments/assets/b02c74eb-201c-453d-8e32-c0e24a0d1c03)

```sql
DELETE FROM Doctors WHERE doctor_id BETWEEN 2 AND 4;
```

**Output:**

![image](https://github.com/user-attachments/assets/d8f11e27-b6cc-413e-a1d0-518a9a401af0)

**Question 7**
---
![image](https://github.com/user-attachments/assets/8a75151c-0327-4e3a-b7a4-b53ff477ab46)

```sql
DELETE FROM Doctors WHERE specialization IS NULL;
```

**Output:**

![image](https://github.com/user-attachments/assets/d8bf65b9-6a91-4860-87a5-5d6fd3e99cbf)

**Question 8**
---
![image](https://github.com/user-attachments/assets/ee8e7766-77a7-46fd-b555-b697fbe0b503)

```sql
DELETE FROM Doctors WHERE last_name IS NULL;
```

**Output:**

![image](https://github.com/user-attachments/assets/7760a7c1-410d-4f3f-8d83-ac0d7600cd34)

**Question 9**
---
![image](https://github.com/user-attachments/assets/34605fa7-7167-43ab-aabc-12ecf8cd6a23)

```sql
DELETE FROM Customer WHERE (GRADE=3 OR AGENT_CODE='A008') AND OUTSTANDING_AMT<5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/be84bfe6-f2dd-4945-82b6-ec33244774b3)

**Question 10**
---
![image](https://github.com/user-attachments/assets/5aaf3034-4131-457c-af25-1889d75465d0)

```sql
DELETE FROM Customer WHERE GRADE<2;
```

**Output:**

![image](https://github.com/user-attachments/assets/d0c42f99-02e6-4b69-8566-ea4d03e9c8c6)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
