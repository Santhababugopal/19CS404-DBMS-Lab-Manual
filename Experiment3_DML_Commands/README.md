Skip to content
prahathieswaransstudent-maker
19CS404-DBMS-Lab-Manual
Repository navigation
Code
Pull requests
Agents
Actions
Projects
Security and quality
Insights
Comparing changes
Choose two branches to see what’s changed or to start a new pull request. If you need to, you can also  or learn more about diff comparisons.
 
...
 
 Able to merge. These branches can be automatically merged.
Discuss and review the changes in this comparison with others. Learn about pull requests
 1 commit
 1 file changed
 1 contributor
Commits on Aug 21, 2026
Add SQL DML command examples to README 

@prahathieswarans-ship-it
prahathieswarans-ship-it authored 1 minute ago
 Showing  with 64 additions and 30 deletions.
  94 changes: 64 additions & 30 deletions94  
Experiment3_DML_Commands/README.md
Original file line number	Diff line number	Diff line change
@@ -47,123 +47,157 @@ SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- Paste Question 1 here
<img width="1195" height="434" alt="image" src="https://github.com/user-attachments/assets/fe93d080-1dcf-450d-9926-4d40589cc23d" />


```sql
-- Paste your SQL code below for Question 1
UPDATE products
SET product_name = 'Grapefruit'
WHERE product_id = 4;
```

**Output:**

<img width="1264" height="373" alt="image" src="https://github.com/user-attachments/assets/0cff3e01-af07-47d5-bf51-a5dc72c4e555" />


**Question 2**
---
<img width="982" height="455" alt="image" src="https://github.com/user-attachments/assets/6136e92c-c19f-41e7-8390-f0250e714724" />


```sql
-- Paste your SQL code below for Question 2
UPDATE SALES
SET total_sell_price = quantity * sell_price
WHERE product_id = 10;
```

**Output:**
<img width="1055" height="320" alt="image" src="https://github.com/user-attachments/assets/3f9faf7a-2a11-40c4-b0cd-502e2ff16520" />


**Question 3**
---
-- Paste Question 3 here
<img width="1120" height="144" alt="image" src="https://github.com/user-attachments/assets/ef7e7bc5-7d87-4369-abdb-ac6576be6e33" />


```sql
-- Paste your SQL code below for Question 3
UPDATE Products
SET 
quantity = quantity*1.10;
```

**Output:**

<img width="1267" height="438" alt="image" src="https://github.com/user-attachments/assets/eaeb18c8-b1e5-4c6d-ab3d-9166f64777c5" />

**Question 4**
---
<img width="1193" height="620" alt="image" src="https://github.com/user-attachments/assets/9181ccff-4b0c-4767-b554-06b14b961acc" />

```sql
-- Paste your SQL code below for Question 4
DELETE FROM doctors 
WHERE ((specialization = 'Pediatrics') OR (specialization = 'Cardiology')) AND (last_name = "Brown");
```

**Output:**

<img width="1268" height="542" alt="image" src="https://github.com/user-attachments/assets/a502cf8e-0939-4100-8a80-96a8eb5bd911" />

**Question 5**
---
<img width="1193" height="620" alt="image" src="https://github.com/user-attachments/assets/464134e3-fbf8-4e6a-8796-d0c2982ef9d9" />

```sql
-- Paste your SQL code below for Question 5
SELECT *
FROM EmployeeInfo
ORDER BY
CASE Department
    WHEN 'HR' THEN 1
    WHEN 'Account' THEN 2
    WHEN 'Admin' THEN 3
END,
EmpLname ASC;
```

**Output:**

<img width="696" height="567" alt="image" src="https://github.com/user-attachments/assets/4ab6e79b-e1d3-40ca-b548-7dc2828b8472" />

**Question 6**
---
<img width="706" height="677" alt="image" src="https://github.com/user-attachments/assets/fd20016e-5291-4c5e-97b0-815c81145968" />

```sql
-- Paste your SQL code below for Question 6
SELECT DISTINCT job,
       SUBSTR(job, 1, 3) AS job_abbr
FROM emp;
```

**Output:**

<img width="1309" height="418" alt="image" src="https://github.com/user-attachments/assets/02cf6183-4f3a-47ac-806a-efe5c8cbd8c8" />

**Question 7**
---
<img width="1193" height="538" alt="image" src="https://github.com/user-attachments/assets/e4c66a90-70a4-40d4-9f7d-3811a01d0ec9" />

```sql
-- Paste your SQL code below for Question 7
UPDATE Products
SET reorder_lvl = reorder_lvl * 0.70
WHERE product_name LIKE '%cream%'
  AND quantity > reorder_lvl;
```

**Output:**

<img width="1233" height="898" alt="image" src="https://github.com/user-attachments/assets/e8f95941-42bf-418e-97f0-3bee815c4b86" />

**Question 8**
---
<img width="1085" height="487" alt="image" src="https://github.com/user-attachments/assets/e236eba0-5a61-4ba2-93e7-a72ad0f3b5b1" />

```sql
-- Paste your SQL code below for Question 8
DELETE FROM Doctors
WHERE specialization = 'Pediatrics'
  AND first_name = 'Michael';
```

**Output:**

<img width="1245" height="633" alt="image" src="https://github.com/user-attachments/assets/256b9351-dd3f-4335-b3a2-8368e529cb64" />

**Question 9**
---
<img width="1035" height="476" alt="image" src="https://github.com/user-attachments/assets/eb7bd40e-095f-40f6-ab99-10f97edb6c98" />

```sql
-- Paste your SQL code below for Question 9
select * from employeeposition where Salary between 50000 and 100000;
```

**Output:**

<img width="1245" height="597" alt="image" src="https://github.com/user-attachments/assets/bcd66a05-65e9-42e2-ad64-8ae1fadce6ee" />

**Question 10**
---
<img width="1142" height="430" alt="image" src="https://github.com/user-attachments/assets/dcdfaeec-5278-4714-b0ca-f9c7bb45f61f" />


```sql
-- Paste your SQL code below for Question 10
SELECT
    product_id,
    original_price,
    discount_percentage,
    original_price * (1 - discount_percentage) AS discounted_price,
    CAST((1 - discount_percentage) * 100 AS INT) || '%' AS discounted_price_percentage
FROM products;
```

**Output:**

<img width="1217" height="354" alt="image" src="https://github.com/user-attachments/assets/a65c7215-3967-4b57-a971-d07f7c0d2871" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
Footer
© 2026 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Community
Docs
Contact
Manage cookies
Do not share my personal information
