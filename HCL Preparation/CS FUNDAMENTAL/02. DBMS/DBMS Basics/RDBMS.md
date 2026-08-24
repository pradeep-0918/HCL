---
type: concept
subject: dbms
topic: "RDBMS"
parent: "DBMS Basics"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - rdbms
  - database
  - hcl
  - tcs
  - infosys
  - zoho
  - accenture
  - sql
  - relational-database
  - cs-fundamentals
  - interview
wikilinks:
  - "[[DBMS Basics]]"
  - "[[Database]]"
  - "[[DBMS]]"
  - "[[Relational Model]]"
  - "[[Keys]]"
  - "[[Constraints]]"
  - "[[Normalization]]"
  - "[[Transactions]]"
  - "[[Indexing]]"
  - "[[DBMS Architecture]]"
---

# RDBMS

## 1. Core Concept

> [!summary]
> **RDBMS stands for Relational Database Management System. It is a type of DBMS that organizes data using the relational model, where data is commonly represented as tables consisting of rows and columns.**

The easiest mental model:

```text
DBMS
  ↓
Different Database Models
  ↓
RDBMS
  ↓
Relational Model
  ↓
Tables
  ↓
Rows + Columns
```

Examples of widely used relational database systems include:

```text
MySQL
PostgreSQL
Oracle Database
Microsoft SQL Server
MariaDB
```

---

# 2. Basic Meaning

Break the word:

```text
Relational
+
Database
+
Management
+
System
```

### Relational

Data is organized using relations, commonly represented as tables.

### Database

The system stores organized data.

### Management

The system provides mechanisms for:

```text
Insert
Read
Update
Delete
Security
Transactions
Constraints
Concurrency
Recovery
```

### System

Software that provides these database-management capabilities.

Therefore:

```text
RDBMS
=
A DBMS based on the relational model
```

---

# 3. DBMS vs RDBMS

This distinction is extremely important.

```text
DBMS
→ General database management system

RDBMS
→ Relational database management system
```

An RDBMS is a type of DBMS.

Conceptually:

```text
                DBMS
                  |
       +----------+----------+
       |          |          |
       ↓          ↓          ↓
   Hierarchical Network   Relational
                            |
                            ↓
                          RDBMS
```

> [!important]
> **Every RDBMS is a DBMS, but not every DBMS is necessarily an RDBMS.**

---

# 4. What Is a Relation?

In the relational model, a relation is mathematically related to the concept of a table.

Example:

```text
Student
+----+----------+------+------+
| ID | Name     | Dept | CGPA |
+----+----------+------+------+
| 1  | Pradeep  | CSE  | 8.5  |
| 2  | Arun     | ECE  | 8.2  |
| 3  | Karthik  | CSE  | 9.1  |
+----+----------+------+------+
```

Here:

```text
Relation
→ Student

Attributes
→ ID, Name, Dept, CGPA

Tuples
→ Individual rows
```

In practical SQL usage:

```text
Relation ≈ Table
Tuple ≈ Row
Attribute ≈ Column
```

---

# 5. Relational Model

The relational model represents data using relations.

Simplified structure:

```text
Database
   ↓
Relations
   ↓
Tables
   ↓
Rows + Columns
```

Example:

```text
Student
Course
Faculty
Enrollment
```

Each can be represented as a relation/table.

---

# 6. Real-World Example — College

Suppose a college needs to manage:

```text
Students
Courses
Faculty
Enrollments
Marks
```

A relational database might contain:

```text
Student
+------------+----------+------------+
| student_id | name     | department |
+------------+----------+------------+

Course
+-----------+-------------+
| course_id | course_name |
+-----------+-------------+

Enrollment
+------------+-----------+
| student_id | course_id |
+------------+-----------+
```

The tables are connected using keys.

---

# 7. Real-World Example — Banking

A banking RDBMS might contain:

```text
Customer
Account
Transaction
Branch
Loan
```

Example:

```text
Customer
+-------------+----------+
| customer_id | name     |
+-------------+----------+

Account
+------------+---------+
| account_id | balance |
+------------+---------+

Transaction
+--------------+--------+
| transaction_id | amount |
+--------------+--------+
```

Relationships can be represented using keys.

---

# 8. Real-World Example — E-Commerce

An e-commerce application can use:

```text
Customer
Product
Order
OrderItem
Payment
Address
```

Example:

```text
Customer
     |
     ↓
Order
     |
     ↓
OrderItem
     |
     ↓
Product
```

This structured organization is a major strength of relational databases.

---

# 9. Real-World Example — Hospital

A hospital database may contain:

```text
Patient
Doctor
Appointment
Prescription
Billing
Department
```

Relationships:

```text
Patient
   |
   ↓
Appointment
   |
   ↓
Doctor
```

The relational model allows these entities to be represented through related tables.

---

# 10. Main Features of RDBMS

Important features include:

```text
1. Table-Based Data Organization
2. Relationships Between Tables
3. Primary Keys
4. Foreign Keys
5. Constraints
6. SQL Support
7. Transactions
8. ACID Properties
9. Concurrency Control
10. Security
11. Indexing
12. Backup and Recovery
13. Data Integrity
14. Query Optimization
15. Data Independence
```

---

# 11. Tables

The most recognizable feature of an RDBMS is table-based organization.

Example:

```text
Employee
+----+----------+--------+
| ID | Name     | Salary |
+----+----------+--------+
| 1  | Arun     | 50000  |
| 2  | Priya    | 60000  |
| 3  | Karthik  | 70000  |
+----+----------+--------+
```

The table contains:

```text
Rows
+
Columns
```

---

# 12. Rows

A row represents a record/tuple.

Example:

```text
1 | Arun | 50000
```

This represents one employee.

Memory:

```text
Row
→ One Record
→ One Tuple
```

---

# 13. Columns

A column represents an attribute.

Example:

```text
ID
Name
Salary
```

Memory:

```text
Column
→ Attribute
```

---

# 14. Table Terminology

| Relational Concept | Common SQL/Table Term |
|---|---|
| Relation | Table |
| Tuple | Row |
| Attribute | Column |
| Domain | Set of allowed values |
| Cardinality | Number of rows |
| Degree | Number of columns |

> [!important]
> **Cardinality and degree are common RDBMS interview traps.**

---

# 15. Degree

The **degree** of a relation is the number of attributes/columns.

Example:

```text
Student
+----+------+-------+------+
| ID | Name | Dept  | CGPA |
+----+------+-------+------+
```

Number of columns:

```text
4
```

Therefore:

```text
Degree = 4
```

---

# 16. Cardinality

The **cardinality** of a relation is the number of tuples/rows.

Example:

```text
Student
+----+--------+
| ID | Name   |
+----+--------+
| 1  | Arun   |
| 2  | Priya  |
| 3  | Ravi   |
+----+--------+
```

Number of rows:

```text
3
```

Therefore:

```text
Cardinality = 3
```

---

# 17. Degree vs Cardinality

| Concept | Means | Easy Memory |
|---|---|---|
| Degree | Number of columns | Vertical |
| Cardinality | Number of rows | Horizontal |

> [!tip]
> **Degree = Columns**
>
> **Cardinality = Rows**

---

# 18. Domain

A domain defines the valid set of values for an attribute.

Example:

```text
Age
```

could have a domain such as:

```text
Non-negative integers
```

Department:

```text
CSE
ECE
EEE
MECH
CIVIL
```

The domain specifies what values are considered valid.

---

# 19. NULL in RDBMS

`NULL` represents the absence of a value or an unknown/not-applicable value depending on context.

Example:

```text
Employee
+----+--------+------------+
| ID | Name   | Phone      |
+----+--------+------------+
| 1  | Arun   | 9876543210 |
| 2  | Priya  | NULL       |
+----+--------+------------+
```

`NULL` is not the same as:

```text
0
```

and is not the same as:

```text
''
```

or an empty string.

> [!warning]
> **NULL represents missing/unknown/not-applicable information; it is not simply zero or an empty string.**

---

# 20. Primary Key

A primary key uniquely identifies rows in a table.

Example:

```text
Student
+------------+----------+
| student_id | name     |
+------------+----------+
| 101        | Pradeep  |
| 102        | Arun     |
+------------+----------+
```

Here:

```text
student_id
```

can be the primary key.

Properties:

```text
Unique
Not NULL
Identifies each row
```

---

# 21. Foreign Key

A foreign key is used to represent a relationship by referencing a key in another table.

Example:

```text
Student
student_id
```

and:

```text
Enrollment
student_id
course_id
```

The `student_id` in Enrollment can reference the Student table.

Conceptually:

```text
Student
  |
  | student_id
  ↓
Enrollment
```

---

# 22. Relationship Between Tables

Suppose:

```text
Student
```

contains:

```text
student_id
```

and:

```text
Course
```

contains:

```text
course_id
```

Then:

```text
Enrollment
student_id
course_id
```

can connect the two.

```text
Student
   |
   ↓
Enrollment
   ↑
   |
Course
```

This allows relational databases to represent relationships between entities.

---

# 23. Referential Integrity

Referential integrity ensures that foreign-key relationships remain valid according to the defined constraints.

Example:

```text
Student
101
102
103
```

If Enrollment contains:

```text
student_id = 999
```

but student `999` does not exist, a foreign-key constraint may reject the operation.

Memory:

```text
Foreign Key
→ Must reference an appropriate existing key value
```

subject to the database's configured referential actions.

---

# 24. Constraints in RDBMS

Important constraints:

```text
NOT NULL
UNIQUE
PRIMARY KEY
FOREIGN KEY
CHECK
DEFAULT
```

Example:

~~~sql
CREATE TABLE Student (
    id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    age INT CHECK (age >= 17),
    department VARCHAR(50) DEFAULT 'CSE'
);
~~~

---

# 25. Entity Integrity

Entity integrity is commonly associated with primary keys.

Basic idea:

```text
Every row should have a valid unique identifier.
```

Therefore:

```text
Primary Key
→ Unique
→ Not NULL
```

---

# 26. Referential Integrity

Referential integrity is associated with foreign keys.

Basic idea:

```text
Child table reference
        ↓
Valid parent key
```

Example:

```text
Student
student_id = 101

Enrollment
student_id = 101
```

Valid relationship.

---

# 27. SQL in RDBMS

SQL stands for:

```text
Structured Query Language
```

It is commonly used to interact with relational databases.

Example:

~~~sql
SELECT name, cgpa
FROM Student
WHERE department = 'CSE'
AND cgpa > 8.0;
~~~

This retrieves matching students.

---

# 28. SQL Categories

Common classifications:

```text
DDL
DML
DQL
DCL
TCL
```

### DDL

```text
CREATE
ALTER
DROP
TRUNCATE
```

### DML

```text
INSERT
UPDATE
DELETE
```

### DQL

```text
SELECT
```

### DCL

```text
GRANT
REVOKE
```

### TCL

```text
COMMIT
ROLLBACK
SAVEPOINT
```

Classification details can vary somewhat by textbook or DBMS documentation.

---

# 29. RDBMS and CRUD

RDBMS supports CRUD operations through SQL.

```text
Create
→ INSERT

Read
→ SELECT

Update
→ UPDATE

Delete
→ DELETE
```

Example:

~~~sql
INSERT INTO Student
VALUES (101, 'Pradeep', 'CSE', 8.5);
~~~

~~~sql
SELECT *
FROM Student;
~~~

~~~sql
UPDATE Student
SET cgpa = 8.7
WHERE id = 101;
~~~

~~~sql
DELETE FROM Student
WHERE id = 101;
~~~

---

# 30. Relationships in RDBMS

Common relationship types:

```text
One-to-One
One-to-Many
Many-to-One
Many-to-Many
```

---

# 31. One-to-One

One record in A is associated with one record in B.

Example:

```text
Person
   |
   | 1 : 1
   ↓
Passport
```

One person may have one passport in a simplified model.

---

# 32. One-to-Many

One record in A can be related to many records in B.

Example:

```text
Department
     |
     | 1 : N
     ↓
Employees
```

One department can have many employees.

---

# 33. Many-to-One

Many records in A can belong to one record in B.

Example:

```text
Employees
    |
    | N : 1
    ↓
Department
```

Many employees can belong to one department.

---

# 34. Many-to-Many

Many records in A can relate to many records in B.

Example:

```text
Students
    |
    | M : N
    ↓
Courses
```

A student can take many courses.

A course can have many students.

Usually a junction/associative table is used:

```text
Student
   |
Enrollment
   |
Course
```

---

# 35. Why Junction Tables Are Important

Suppose:

```text
Student
Course
```

have a many-to-many relationship.

Instead of directly storing multiple values in one cell, use:

```text
Enrollment
+------------+-----------+
| student_id | course_id |
+------------+-----------+
| 101        | C01       |
| 101        | C02       |
| 102        | C01       |
+------------+-----------+
```

This fits the relational model and supports normalization.

---

# 36. Normalization in RDBMS

Normalization is the process of structuring relations to reduce undesirable redundancy and anomalies.

Common forms:

```text
1NF
2NF
3NF
BCNF
```

Basic flow:

```text
Poor Design
   ↓
Normalization
   ↓
Better Structured Relations
```

---

# 37. First Normal Form Preview

A relation is generally in 1NF when each attribute contains atomic values under the chosen relational model.

Bad design:

```text
Student | Phone
101     | 9876, 8765
```

Better design may represent phone values separately depending on requirements.

Detailed normalization will be covered in:

```text
[[Normalization]]
```

---

# 38. Transactions in RDBMS

RDBMSs commonly support transactions.

Example:

```text
Transfer ₹500
```

Operations:

```text
Debit Account A
Credit Account B
```

The transaction should be managed according to ACID properties.

```text
Atomicity
Consistency
Isolation
Durability
```

---

# 39. ACID in RDBMS

## Atomicity

All required operations of a transaction succeed together, or the transaction does not partially commit.

## Consistency

The transaction preserves defined database constraints and correctness rules.

## Isolation

Concurrent transactions are controlled so their intermediate effects are appropriately isolated according to the isolation level.

## Durability

Committed changes survive appropriate system failures according to the DBMS's durability guarantees.

---

# 40. Concurrency Control

RDBMSs are often multi-user systems.

Example:

```text
User A → UPDATE Account
User B → UPDATE Account
User C → SELECT Account
```

The database must coordinate these operations.

Important mechanisms/concepts:

```text
Locks
Isolation Levels
Serializability
MVCC
Deadlocks
```

Specific mechanisms vary by RDBMS.

---

# 41. Locking

A DBMS can use locks to coordinate access.

Common lock concepts:

```text
Shared Lock
Exclusive Lock
```

### Shared Lock

Generally associated with reading.

Multiple compatible shared locks may coexist depending on the DBMS lock manager.

### Exclusive Lock

Generally associated with modifications.

An exclusive lock conflicts with other incompatible access.

Detailed locking will be covered in:

```text
[[Concurrency Control]]
```

---

# 42. Indexing

RDBMSs commonly support indexes to improve retrieval performance.

Example:

~~~sql
CREATE INDEX idx_student_name
ON Student(name);
~~~

Conceptually:

```text
Table
 ↓
Index
 ↓
Faster suitable lookup
```

But:

```text
More indexes
→ More storage
→ More write maintenance
```

---

# 43. Clustered vs Non-Clustered Index Preview

Different database systems use different indexing terminology and implementations.

At a high level:

```text
Clustered
→ Data organization is closely tied to index ordering

Non-Clustered
→ Separate index structure points toward table data
```

Exact behavior depends on the RDBMS.

Detailed indexing will be covered separately.

---

# 44. Views

A view is a virtual table defined by a query.

Example:

~~~sql
CREATE VIEW CSE_Students AS
SELECT id, name, cgpa
FROM Student
WHERE department = 'CSE';
~~~

Then:

~~~sql
SELECT *
FROM CSE_Students;
~~~

Views can provide:

```text
Abstraction
Security
Simplification
Reusable query logic
```

---

# 45. Stored Procedures

A stored procedure is database-side program logic stored under a database object.

Conceptually:

```text
Application
   ↓
CALL Procedure
   ↓
Database
   ↓
Execute Logic
```

Syntax and capabilities differ across RDBMS products.

---

# 46. Triggers

A trigger automatically executes in response to specified database events.

Conceptually:

```text
INSERT / UPDATE / DELETE
          ↓
       Trigger
          ↓
    Automatic Action
```

Example use case:

```text
Employee Salary Updated
          ↓
      Audit Trigger
          ↓
      History Record
```

---

# 47. RDBMS Security

Important mechanisms:

```text
Authentication
Authorization
Roles
Privileges
Views
Encryption
Auditing
```

Example:

```text
Student
→ SELECT own permitted data

Faculty
→ SELECT / UPDATE permitted academic data

Admin
→ Broader permissions
```

Actual permissions depend on application and database configuration.

---

# 48. RDBMS Advantages

### 1. Structured Data

Tables provide clear organization.

### 2. Relationships

Tables can be related through keys.

### 3. Integrity

Constraints help prevent invalid data.

### 4. SQL

Powerful declarative querying.

### 5. Transactions

Supports reliable multi-step operations.

### 6. Concurrency

Supports multiple users and transactions.

### 7. Security

Roles and privileges can control access.

### 8. Indexing

Indexes can improve suitable query performance.

### 9. Normalization

Supports structured relational design.

### 10. Backup and Recovery

Provides database-aware recovery mechanisms.

---

# 49. RDBMS Limitations

RDBMS is not ideal for every workload.

Potential limitations include:

```text
Schema rigidity
Complex joins for some workloads
Horizontal scaling complexity in some architectures
Object-relational mismatch
Operational overhead
Performance challenges with highly unstructured data
```

Modern relational systems can address many of these concerns through advanced features, but workload and design still matter.

---

# 50. RDBMS vs File System

| Feature | File System | RDBMS |
|---|---|---|
| Data organization | Files | Relations/Tables |
| Relationships | Usually application-managed | Keys and relational structures |
| Query language | Usually application-specific | SQL |
| Constraints | Limited | Strong database constraints |
| Transactions | Not inherently DB transactions | Supported |
| Concurrency | Application-dependent | Database mechanisms |
| Indexing | Application-dependent | Database indexes |
| Security | Mainly OS/application | Database roles/privileges |
| Recovery | External/application mechanisms | Database recovery mechanisms |
| Data integrity | Application-dependent | Database-enforced constraints |

---

# 51. DBMS vs RDBMS

| Feature | DBMS | RDBMS |
|---|---|---|
| Meaning | Database Management System | Relational Database Management System |
| Scope | General | Relational |
| Data model | May vary | Relational |
| Tables | Not universally required | Core representation |
| Relationships | Model-dependent | Keys/relational structures |
| Foreign keys | Not a universal DBMS requirement | Common relational feature |
| SQL | Product/model dependent | Commonly supported |
| Normalization | Relational concept | Central design concept |
| Transactions | Depends on system | Commonly supported |
| Example | Broad category | MySQL, PostgreSQL, Oracle Database |

> [!important]
> The exact capabilities of a particular DBMS depend on the product. Avoid memorizing overly rigid statements such as "DBMS does not support relationships" or "DBMS does not support transactions."

---

# 52. RDBMS vs Spreadsheet

| RDBMS | Spreadsheet |
|---|---|
| Database management system | Productivity/analysis tool |
| Multi-user data management | Primarily document-oriented |
| Strong relational modeling | Limited relational modeling |
| SQL | Formulas/functions |
| Transactions | Database transaction support |
| Constraints | Database constraints |
| Large-scale applications | Small/medium analysis use cases |
| Fine-grained access control | Usually more limited |

---

# 53. RDBMS Recognition Tricks

> [!important]
> If the question says:
>
> **"Data stored in tables"**
>
> Think:
>
> **Relational Model / RDBMS**

> [!important]
> If the question says:
>
> **"Rows and columns"**
>
> Think:
>
> **Relation / Table**

> [!important]
> If the question says:
>
> **"Unique identification of a row"**
>
> Think:
>
> **Primary Key**

> [!important]
> If the question says:
>
> **"Connect two tables"**
>
> Think:
>
> **Foreign Key / Relationship**

> [!important]
> If the question says:
>
> **"Many students take many courses"**
>
> Think:
>
> **Many-to-Many + Junction Table**

> [!important]
> If the question says:
>
> **"Number of columns"**
>
> Think:
>
> **Degree**

> [!important]
> If the question says:
>
> **"Number of rows"**
>
> Think:
>
> **Cardinality**

> [!important]
> If the question says:
>
> **"Set of valid values"**
>
> Think:
>
> **Domain**

> [!important]
> If the question says:
>
> **"Automatic response to INSERT/UPDATE/DELETE"**
>
> Think:
>
> **Trigger**

> [!important]
> If the question says:
>
> **"Virtual table"**
>
> Think:
>
> **View**

---

# 54. Pattern Recognition — Degree vs Cardinality

### How to Recognize

If the question asks:

```text
Number of attributes
Number of columns
```

Think:

```text
Degree
```

If the question asks:

```text
Number of tuples
Number of rows
```

Think:

```text
Cardinality
```

### Shortcut

```text
Degree → Columns

Cardinality → Rows
```

---

# 55. Pattern Recognition — Primary vs Foreign Key

### How to Recognize

If the question says:

```text
Uniquely identifies a row
```

Think:

```text
Primary Key
```

If the question says:

```text
References another table
```

Think:

```text
Foreign Key
```

Shortcut:

```text
PRIMARY
→ Identify

FOREIGN
→ Reference
```

---

# 56. Pattern Recognition — Relationship Type

### How to Recognize

```text
One department → Many employees
```

Think:

```text
1 : N
One-to-Many
```

```text
Many employees → One department
```

Think:

```text
N : 1
Many-to-One
```

```text
Many students ↔ Many courses
```

Think:

```text
M : N
Many-to-Many
```

and usually:

```text
Junction Table
```

---

# 57. Pattern Recognition — NULL

### How to Recognize

If the question says:

```text
Unknown value
Missing value
No applicable value
```

Think:

```text
NULL
```

Do not confuse it with:

```text
0
Empty String
False
```

---

# 58. Pattern Recognition — Constraints

### How to Recognize

```text
Value must exist
→ NOT NULL

No duplicates
→ UNIQUE

Unique row identity
→ PRIMARY KEY

Reference another table
→ FOREIGN KEY

Condition on values
→ CHECK

Automatic value
→ DEFAULT
```

---

# 59. Basic Examples

## Example 1 — Degree

### Question

Consider:

```text
Student
+----+--------+------+------+
| ID | Name   | Dept | CGPA |
+----+--------+------+------+
```

Find the degree.

### Pattern

```text
Number of columns
```

### Calculation

```text
ID
Name
Dept
CGPA

Total = 4
```

### Answer

```text
Degree = 4
```

---

# 60. Example 2 — Cardinality

### Question

```text
Student
+----+--------+
| ID | Name   |
+----+--------+
| 1  | Arun   |
| 2  | Priya  |
| 3  | Ravi   |
| 4  | Kiran  |
+----+--------+
```

Find the cardinality.

### Pattern

```text
Number of rows
```

### Calculation

```text
4 rows
```

### Answer

```text
Cardinality = 4
```

---

# 61. Example 3 — Identify the Relationship

### Question

One department has 50 employees.

What is the relationship between Department and Employee?

### Pattern

```text
One Department
→ Many Employees
```

### Answer

```text
One-to-Many
1 : N
```

---

# 62. Example 4 — Many-to-Many

### Question

A student can enroll in many courses, and a course can have many students. How should this relationship be modeled?

### Pattern

```text
Many Students
↔
Many Courses
```

### Answer

```text
Many-to-Many
```

Use:

```text
Enrollment(StudentID, CourseID)
```

as a junction/associative table.

---

# 63. Example 5 — Primary Key

### Question

A Student table contains:

```text
student_id
name
department
```

Which attribute is suitable as a primary key if every student has a unique ID?

### Pattern

```text
Unique row identification
```

### Answer

```text
student_id
```

---

# 64. Example 6 — Foreign Key

### Question

`Enrollment.student_id` references `Student.student_id`. What is `Enrollment.student_id`?

### Pattern

```text
References another table
```

### Answer

```text
Foreign Key
```

---

# 65. Medium Example — Complete Design

### Question

Design tables for:

```text
Students
Courses
Students can enroll in multiple courses
Courses can contain multiple students
```

### Step 1 — Student

```text
Student(
    student_id,
    name
)
```

### Step 2 — Course

```text
Course(
    course_id,
    course_name
)
```

### Step 3 — Many-to-Many Relationship

Create:

```text
Enrollment(
    student_id,
    course_id
)
```

### Final Design

```text
Student
    |
    ↓
Enrollment
    ↑
    |
Course
```

### Pattern

```text
M : N
→ Junction Table
```

---

# 66. Medium Example — Constraints

### Question

Create a Student table where:

```text
ID must be unique
Name cannot be NULL
Age must be >= 17
Department defaults to CSE
```

### Solution

~~~sql
CREATE TABLE Student (
    id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT CHECK (age >= 17),
    department VARCHAR(50) DEFAULT 'CSE'
);
~~~

### Pattern

```text
Unique
→ PRIMARY KEY

Required
→ NOT NULL

Condition
→ CHECK

Automatic value
→ DEFAULT
```

---

# 67. Advanced Example — Relational Design

### Question

An e-commerce system needs:

```text
Customers
Products
Orders
```

A customer can create many orders.

An order can contain many products.

How can the database be designed?

### Solution

```text
Customer
customer_id
name
```

```text
Product
product_id
name
price
```

```text
Order
order_id
customer_id
order_date
```

```text
OrderItem
order_id
product_id
quantity
```

Relationships:

```text
Customer
   |
   | 1 : N
   ↓
Order
   |
   | 1 : N
   ↓
OrderItem
   ↑
   |
Product
```

This avoids storing multiple products in a single cell and provides a scalable relational design.

---

# 68. Advanced Example — Query

### Question

Find all CSE students with CGPA greater than 8.5.

### Pattern

```text
Filtering
```

### Query

~~~sql
SELECT *
FROM Student
WHERE department = 'CSE'
AND cgpa > 8.5;
~~~

### Answer

The DBMS returns only rows satisfying both conditions.

---

# 69. Advanced Example — Join

Suppose:

```text
Student
+----+---------+------------+
| ID | Name    | CourseID   |
+----+---------+------------+

Course
+----------+-------------+
| CourseID | CourseName  |
+----------+-------------+
```

Question:

Find student names along with course names.

### Pattern

```text
Information stored across multiple tables
```

### Query

~~~sql
SELECT s.name, c.course_name
FROM Student s
JOIN Course c
ON s.course_id = c.course_id;
~~~

### Key Idea

```text
JOIN
→ Combine related rows from tables
```

Detailed joins belong to SQL, but understanding their relational purpose is important for RDBMS interviews.

---

# 70. Advanced Example — Transaction

### Question

Transfer ₹1000 from Account A to Account B.

### Operations

```text
1. Debit A by ₹1000
2. Credit B by ₹1000
```

### Pattern

```text
Multiple operations
+
One logical unit
```

### Concept

```text
Transaction
```

### Expected result

If:

```text
A = ₹5000
B = ₹3000
```

After transfer:

```text
A = ₹4000
B = ₹4000
```

The DBMS transaction system helps ensure the operation is handled correctly.

---

# 71. Advanced Example — Indexing

### Question

A table contains 10 million student records and this query runs frequently:

~~~sql
SELECT *
FROM Student
WHERE student_id = 5000000;
~~~

What could improve lookup performance?

### Pattern

```text
Frequent equality search
+
Large table
```

### Possible Solution

A suitable index on:

```text
student_id
```

### Example

~~~sql
CREATE INDEX idx_student_id
ON Student(student_id);
~~~

### Important

This does not guarantee a faster plan in every situation. The optimizer decides whether using the index is beneficial.

---

# 72. Real-Time System Design Example

Imagine building a food delivery application.

Entities:

```text
Customer
Restaurant
Food
Order
Payment
Delivery
```

Possible relationships:

```text
Customer
   |
   ↓
Order
   |
   ↓
Food

Restaurant
   |
   ↓
Food

Order
   |
   ↓
Payment

Order
   |
   ↓
Delivery
```

The relational model allows these concepts to be represented through tables and keys.

---

# 73. Real-Time Banking Design

Possible tables:

```text
Customer
Account
CustomerAccount
Transaction
Branch
```

Potential relationships:

```text
Customer
   |
CustomerAccount
   |
Account
   |
Transaction
```

This design can support:

```text
Account ownership
Transactions
Balances
Branch relationships
```

---

# 74. Real-Time College Design

Possible tables:

```text
Student
Department
Faculty
Course
Enrollment
Exam
Marks
```

Relationships:

```text
Department
   |
   +------ Student
   |
   +------ Faculty
   |
   +------ Course

Student
   |
Enrollment
   |
Course

Student
   |
Marks
   |
Exam
```

This demonstrates how a real application can be decomposed into relational tables.

---

# 75. Real-Time Social Media Design

Possible tables:

```text
User
Post
Comment
Like
Follow
Message
```

Example:

```text
User
 |
 +---- Post
 |
 +---- Comment
 |
 +---- Follow
 |
 +---- Message
```

A many-to-many relationship such as:

```text
User ↔ User
```

for following can be represented using a relationship table:

```text
Follow(
    follower_id,
    following_id
)
```

---

# 76. RDBMS Design Thinking

When given a real-world system, use this process:

```text
Step 1
Identify Entities

        ↓

Step 2
Identify Attributes

        ↓

Step 3
Choose Keys

        ↓

Step 4
Identify Relationships

        ↓

Step 5
Choose Cardinalities

        ↓

Step 6
Create Tables

        ↓

Step 7
Add Foreign Keys

        ↓

Step 8
Add Constraints

        ↓

Step 9
Normalize

        ↓

Step 10
Consider Indexes
```

This is a powerful interview pattern.

---

# 77. RDBMS Interview Pattern — Design a College Database

### Step 1

Identify entities:

```text
Student
Course
Faculty
Department
```

### Step 2

Identify relationships:

```text
Student → Enrollment
Course → Enrollment
Faculty → Course
Department → Student
```

### Step 3

Choose keys:

```text
student_id
course_id
faculty_id
department_id
```

### Step 4

Create relationship tables where needed.

### Step 5

Add constraints.

### Step 6

Normalize.

### Step 7

Add indexes based on query workload.

---

# 78. Common Exam Patterns

> [!important] Must Master

```text
1. Define RDBMS.

2. Difference between DBMS and RDBMS.

3. What is a relation?

4. What is a tuple?

5. What is an attribute?

6. What is degree?

7. What is cardinality?

8. Degree vs cardinality.

9. What is a domain?

10. What is primary key?

11. What is foreign key?

12. What is referential integrity?

13. What is entity integrity?

14. What is normalization?

15. What is a one-to-one relationship?

16. What is one-to-many?

17. What is many-to-many?

18. Why is a junction table used?

19. What is NULL?

20. Why are constraints needed?

21. What is SQL?

22. What is a view?

23. What is a trigger?

24. What is an index?

25. What is a transaction?

26. What are ACID properties?

27. What is concurrency control?

28. Why is RDBMS useful for multi-user systems?

29. How does RDBMS maintain data integrity?

30. How would you design a relational database for a real-world system?
```

---

# 79. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Degree and Cardinality

Wrong:

```text
Degree = Rows
```

Correct:

```text
Degree = Columns
Cardinality = Rows
```

---

### Mistake 2 — Primary Key vs Foreign Key

Wrong:

```text
Foreign key uniquely identifies its own table.
```

Better:

```text
Primary key
→ Identifies rows in its table

Foreign key
→ Represents a reference to a key in another table
```

---

### Mistake 3 — NULL = 0

Wrong.

```text
NULL ≠ 0
```

NULL represents missing, unknown, or not-applicable information depending on context.

---

### Mistake 4 — NULL = Empty String

Wrong.

```text
NULL ≠ ''
```

They have different meanings and behavior.

---

### Mistake 5 — Every Many-to-Many Relationship Uses One Cell

Wrong.

Do not store:

```text
Courses = "C, Java, Python"
```

inside one field when the data model requires proper relational representation.

Prefer a relationship table:

```text
Enrollment
student_id
course_id
```

---

### Mistake 6 — Every RDBMS Is Identical

Wrong.

Different RDBMS products have different:

```text
Features
Syntax
Storage engines
Transaction behavior
Index implementations
Isolation implementations
Extensions
```

---

### Mistake 7 — More Indexes Always Mean Better Performance

Wrong.

Indexes can improve reads but increase:

```text
Storage
INSERT cost
UPDATE cost
DELETE cost
Maintenance
```

---

### Mistake 8 — Normalization Means No Duplicate Values Anywhere

Wrong.

Normalization reduces undesirable redundancy and anomalies.

It does not mean:

```text
Every value must appear only once
```

---

### Mistake 9 — RDBMS Is Only About Tables

Incomplete.

RDBMS also involves:

```text
Keys
Constraints
Relationships
Transactions
Concurrency
Security
Indexes
Recovery
Query Processing
```

---

# 80. Interview Questions

## Q1. What is RDBMS?

### Strong Answer

> RDBMS stands for Relational Database Management System. It is a type of DBMS based on the relational model, where data is represented using relations commonly implemented as tables consisting of rows and columns. It supports concepts such as keys, constraints, relationships, SQL, transactions, concurrency control, and data integrity.

---

## Q2. Difference between DBMS and RDBMS?

### Strong Answer

> DBMS is the broader category of database management systems, while RDBMS is a DBMS based specifically on the relational model. RDBMSs commonly organize data using tables and use keys and constraints to represent relationships and maintain integrity.

---

## Q3. What is a relation?

### Strong Answer

> A relation is the fundamental structure in the relational model and is commonly represented as a table in practical RDBMS systems.

---

## Q4. What is a tuple?

> A tuple represents a row or record in a relation.

---

## Q5. What is an attribute?

> An attribute represents a property of an entity and corresponds to a column in a relational table.

---

## Q6. What is degree?

> Degree is the number of attributes or columns in a relation.

---

## Q7. What is cardinality?

> Cardinality is the number of tuples or rows in a relation.

---

## Q8. What is a primary key?

> A primary key is a chosen key that uniquely identifies each row in a table and cannot contain NULL values under standard relational primary-key semantics.

---

## Q9. What is a foreign key?

> A foreign key is an attribute or set of attributes used to reference a key in another table and establish referential relationships.

---

## Q10. What is referential integrity?

> Referential integrity ensures that references represented through foreign keys remain valid according to the defined referential constraints and actions.

---

# 81. Advanced Interview Questions

## Q11. Why is RDBMS called relational?

Because data is modeled using relations.

In practical SQL systems:

```text
Relation
≈ Table
```

and relationships between entities can be represented through relational structures and keys.

---

## Q12. Why are primary and foreign keys important?

They help provide:

```text
Unique Identification
+
Relationships
+
Referential Integrity
```

---

## Q13. Why is normalization important in RDBMS?

Normalization helps structure relations to reduce undesirable redundancy and anomalies.

---

## Q14. Why is a many-to-many relationship usually represented using a separate table?

Because a relational design typically represents the relationship as individual rows rather than storing multiple values in one attribute.

Example:

```text
Student
Course
Enrollment
```

---

## Q15. What is the difference between degree and cardinality?

```text
Degree
→ Number of columns

Cardinality
→ Number of rows
```

---

## Q16. What happens when a foreign-key value does not have a matching parent key?

If the foreign-key constraint is enforced and no permitted referential action applies, the database can reject the operation.

---

## Q17. Why is NULL special?

Because SQL uses three-valued logic in many expressions involving NULL:

```text
TRUE
FALSE
UNKNOWN
```

This is why:

```sql
WHERE age = NULL
```

does not correctly test for NULL.

Use:

~~~sql
WHERE age IS NULL;
~~~

This is a very important SQL interview trap.

---

# 82. Tricky SQL Example — NULL

### Question

What is wrong with:

~~~sql
SELECT *
FROM Student
WHERE phone = NULL;
~~~

### Answer

`NULL` is not compared using `=`.

Correct:

~~~sql
SELECT *
FROM Student
WHERE phone IS NULL;
~~~

Memory:

```text
NULL
→ IS NULL

NOT NULL
→ IS NOT NULL
```

---

# 83. Tricky Interview Question — Cardinality

Consider:

```text
Employee
+----+--------+--------+
| ID | Name   | Salary |
+----+--------+--------+
| 1  | Arun   | 50000  |
| 2  | Priya  | 60000  |
| 3  | Ravi   | 55000  |
| 4  | Kiran  | 70000  |
| 5  | Meena  | 65000  |
+----+--------+--------+
```

### Question

Find:

```text
Degree
Cardinality
```

### Solution

Columns:

```text
ID
Name
Salary
```

Therefore:

```text
Degree = 3
```

Rows:

```text
5
```

Therefore:

```text
Cardinality = 5
```

---

# 84. Tricky Interview Question — Many-to-Many

### Question

A student can enroll in multiple courses, and each course can contain multiple students.

How would you model this?

### Recognition

```text
Many ↔ Many
```

### Solution

```text
Student
Course
Enrollment
```

with:

```text
Enrollment(
    student_id,
    course_id
)
```

---

# 85. Tricky Interview Question — Index Trade-Off

### Question

Why not create indexes on every column?

### Answer

Because indexes:

```text
Consume storage
Need maintenance
Can increase INSERT cost
Can increase UPDATE cost
Can increase DELETE cost
May not be useful for every query
```

Therefore:

```text
Index based on workload.
```

---

# 86. Tricky Interview Question — RDBMS Choice

### Question

When would an RDBMS be a strong choice?

### Think

Use RDBMS when the system needs:

```text
Structured data
Relationships
Strong integrity
Transactions
Complex queries
Consistent schemas
SQL
```

Examples:

```text
Banking
ERP
College Management
Payroll
Order Management
Inventory
```

---

# 87. RDBMS Design Shortcut

> [!tip]
> When an interviewer gives you a system-design-style database question, use:

```text
E → Entities
A → Attributes
K → Keys
R → Relationships
C → Cardinality
T → Tables
F → Foreign Keys
N → Normalization
I → Indexes
S → Security
```

Memory:

```text
EAKRCTFNIS
```

The exact order can be adapted based on the problem.

---

# 88. Real-Time Interview Framework

If asked:

> "Design a database for an online shopping system."

Immediately think:

```text
Entities
↓
Customer
Product
Order
Payment
Address
OrderItem

Keys
↓
customer_id
product_id
order_id
payment_id

Relationships
↓
Customer → Orders
Order → OrderItems
Product → OrderItems
Order → Payment

Constraints
↓
Primary Keys
Foreign Keys
CHECK
NOT NULL
UNIQUE

Normalization
↓
Avoid repeating product/order/customer information

Indexes
↓
Frequently searched columns

Transactions
↓
Order + Payment + Inventory updates

Security
↓
User permissions
```

This demonstrates much stronger understanding than merely defining RDBMS.

---

# 89. High-Level RDBMS Mental Model

```text
                    RDBMS
                      |
       +--------------+--------------+
       |              |              |
       ↓              ↓              ↓
     Tables        Relationships    SQL
       |              |              |
       ↓              ↓              ↓
 Rows + Columns   Keys + FKs       Queries
       |              |              |
       +--------------+--------------+
                      |
                      ↓
                 Constraints
                      |
                      ↓
                Data Integrity
                      |
                      ↓
                 Transactions
                      |
                      ↓
                Concurrency
                      |
                      ↓
                   Recovery
                      |
                      ↓
                  Indexing
                      |
                      ↓
                 Performance
```

---

# 90. Formula Sheet

```text
Degree
= Number of Columns

Cardinality
= Number of Rows

RDBMS
⊂ DBMS

One-to-One
= 1 : 1

One-to-Many
= 1 : N

Many-to-One
= N : 1

Many-to-Many
= M : N

CRUD
= Create + Read + Update + Delete

ACID
= Atomicity + Consistency + Isolation + Durability

Primary Key
→ Unique Row Identification

Foreign Key
→ Reference to Key in Related Table

NULL
→ Missing / Unknown / Not Applicable Value
```

---

# 91. Quick Revision

> [!summary] One-Minute Revision

```text
RDBMS
→ Relational Database Management System.

RDBMS
→ A type of DBMS.

RELATIONAL MODEL
→ Represents data using relations.

RELATION
→ Commonly represented as a table.

TUPLE
→ Row.

ATTRIBUTE
→ Column.

DEGREE
→ Number of columns.

CARDINALITY
→ Number of rows.

DOMAIN
→ Valid set of values.

PRIMARY KEY
→ Unique row identification.

FOREIGN KEY
→ Reference between related tables.

ENTITY INTEGRITY
→ Primary-key based row identification.

REFERENTIAL INTEGRITY
→ Valid foreign-key relationships.

1 : 1
→ One-to-One.

1 : N
→ One-to-Many.

N : 1
→ Many-to-One.

M : N
→ Many-to-Many.

M : N
→ Usually represented using a junction table.

SQL
→ Language used to interact with relational databases.

CONSTRAINTS
→ Rules for maintaining valid data.

NORMALIZATION
→ Reduces undesirable redundancy and anomalies.

TRANSACTION
→ Logical unit of database work.

ACID
→ Atomicity, Consistency, Isolation, Durability.

INDEX
→ Auxiliary structure that can improve suitable data retrieval.

VIEW
→ Virtual table defined by a query.

TRIGGER
→ Automatic action in response to specified database events.

NULL
→ Missing/unknown/not-applicable value depending on context.

DBMS
→ General category.

RDBMS
→ Relational category.
```

---

# 92. Golden Memory Trick

**RDBMS = Tables + Relationships + Keys + Constraints + SQL + Transactions.**

# 93. One-Line Recognition

**Whenever you see tables connected through keys, rows and columns, relational constraints, SQL, and transaction-based data management, think RDBMS.**