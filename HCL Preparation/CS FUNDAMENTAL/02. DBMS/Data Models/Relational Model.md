---
type: concept
subject: dbms
topic: "Relational Model"
parent: "Data Models"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - data-models
  - relational-model
  - relation
  - tuple
  - attribute
  - domain
  - table
  - hcl
  - tcs
  - infosys
  - zoho
  - accenture
  - cs-fundamentals
  - interview
wikilinks:
  - "[[Data Models]]"
  - "[[Hierarchical Model]]"
  - "[[Network Model]]"
  - "[[ER Model]]"
  - "[[Database]]"
  - "[[Primary Key]]"
  - "[[Foreign Key]]"
  - "[[Normalization]]"
  - "[[Constraints]]"
---

# Relational Model

## 1. Core Concept

> [!summary]
> The **Relational Model** represents data using **relations**, which are commonly implemented as **tables** containing rows and columns.

The simplest mental model is:

~~~text
RELATIONAL MODEL
       ↓
    TABLES
       ↓
Rows + Columns
~~~

For example:

~~~text
Student

+------------+----------+-----+
| Student_ID | Name     | CGPA|
+------------+----------+-----+
| 101        | Pradeep  | 8.5 |
| 102        | Arun     | 8.2 |
| 103        | Priya    | 9.1 |
+------------+----------+-----+
~~~

Here:

~~~text
Table
→ Relation

Row
→ Tuple

Column
→ Attribute

Allowed Values
→ Domain
~~~

The relational model is one of the most important DBMS topics because modern relational databases are widely used in software applications.

---

# 2. Basic Meaning

The relational model organizes data into relations.

In practical database terminology:

~~~text
Relation
≈ Table

Tuple
≈ Row

Attribute
≈ Column

Domain
≈ Allowed Set of Values
~~~

Example:

~~~text
Student
+----+---------+-----+
| ID | Name    | CGPA|
+----+---------+-----+
| 1  | Arun    | 8.2 |
| 2  | Priya   | 9.1 |
| 3  | Kiran   | 7.8 |
+----+---------+-----+
~~~

This table is a relation.

Each row is a tuple.

Each column is an attribute.

---

# 3. Why Is It Called a Relational Model?

The term **relation** comes from the mathematical concept of a relation.

A relation can be viewed as a set of tuples over defined attributes.

In practical DBMS learning, think:

~~~text
Relation
    ↓
Structured collection of tuples
    ↓
Table
~~~

The model provides a mathematical foundation for organizing and manipulating data.

---

# 4. Core Terminology

| Relational Term | Common SQL/Table Term |
|---|---|
| Relation | Table |
| Tuple | Row |
| Attribute | Column |
| Domain | Allowed set of values |
| Degree | Number of attributes/columns |
| Cardinality | Number of tuples/rows |
| Relation Schema | Table structure |
| Relation Instance | Current rows/data |

These mappings are extremely important for interviews and MCQs.

---

# 5. Relation

A **relation** is a collection of tuples having the same attributes.

Example:

~~~text
STUDENT

+----+---------+-----+
| ID | Name    | CGPA|
+----+---------+-----+
| 1  | Arun    | 8.2 |
| 2  | Priya   | 9.1 |
| 3  | Kiran   | 7.8 |
+----+---------+-----+
~~~

The complete table can be viewed as a relation.

> [!important]
> **Relation = Table** is the fastest placement-exam mapping.

---

# 6. Tuple

A **tuple** is one row in a relation.

Example:

~~~text
+----+---------+-----+
| ID | Name    | CGPA|
+----+---------+-----+
| 1  | Arun    | 8.2 |
| 2  | Priya   | 9.1 |
+----+---------+-----+
~~~

The tuple:

~~~text
(1, Arun, 8.2)
~~~

represents one student's data.

Therefore:

~~~text
Tuple
→ Row
→ Record
~~~

---

# 7. Attribute

An **attribute** is a property or column of a relation.

Example:

~~~text
Student(ID, Name, CGPA)
~~~

Attributes are:

~~~text
ID
Name
CGPA
~~~

Therefore:

~~~text
Attribute
→ Column
→ Field
~~~

---

# 8. Domain

A **domain** defines the set of valid values that an attribute can take.

Example:

~~~text
Age
→ Positive integers within an allowed range

CGPA
→ Numeric values such as 0.0 to 10.0

Gender
→ Values defined by the application's data model
~~~

The exact domain depends on the database design.

Example:

~~~text
CGPA Domain
= {0.0, 0.1, 0.2, ..., 10.0}
```

Conceptually, the domain tells us:

~~~text
"What values are allowed here?"
~~~

---

# 9. Domain Example

Consider:

~~~text
Student_ID
Name
CGPA
~~~

Possible domains:

~~~text
Student_ID
→ Positive Integer

Name
→ Character String

CGPA
→ Numeric value in an allowed range
~~~

The domain helps maintain valid data.

---

# 10. Degree

The **degree** of a relation is the number of attributes in the relation.

Example:

~~~text
Student(ID, Name, CGPA, Department)
~~~

Number of attributes:

~~~text
4
~~~

Therefore:

~~~text
Degree = 4
~~~

> [!important]
> **Degree = Number of Columns / Attributes**

---

# 11. Cardinality

The **cardinality** of a relation is the number of tuples in the relation.

Example:

~~~text
+----+-------+-----+
| ID | Name  | CGPA|
+----+-------+-----+
| 1  | Arun  | 8.2 |
| 2  | Priya | 9.1 |
| 3  | Kiran | 7.8 |
| 4  | Ravi  | 8.7 |
+----+-------+-----+
~~~

Number of rows:

~~~text
4
~~~

Therefore:

~~~text
Cardinality = 4
~~~

> [!important]
> **Cardinality = Number of Rows / Tuples**

---

# 12. Degree vs Cardinality

This is a very common MCQ trap.

| Concept | Means | Think |
|---|---|---|
| Degree | Number of attributes | Columns |
| Cardinality | Number of tuples | Rows |

Shortcut:

~~~text
DEGREE
→ D = Design dimensions / columns

CARDINALITY
→ C = Count of records
~~~

Even better:

~~~text
Degree → Columns
Cardinality → Rows
~~~

Memorize this exactly.

---

# 13. Example — Degree and Cardinality

Consider:

~~~text
Employee

+----+---------+----------+--------+
| ID | Name    | Dept     | Salary |
+----+---------+----------+--------+
| 1  | Arun    | CSE      | 50000  |
| 2  | Priya   | ECE      | 60000  |
| 3  | Kiran   | CSE      | 55000  |
+----+---------+----------+--------+
~~~

Number of columns:

~~~text
4
~~~

Therefore:

~~~text
Degree = 4
~~~

Number of rows:

~~~text
3
~~~

Therefore:

~~~text
Cardinality = 3
~~~

---

# 14. Relation Schema

A **relation schema** describes the structure of a relation.

Example:

~~~text
STUDENT(
    Student_ID,
    Name,
    Department,
    CGPA
)
~~~

It tells us:

- Relation name
- Attributes
- Structure

It does not represent the actual current rows.

Think:

~~~text
Schema
→ Structure
~~~

---

# 15. Relation Instance

A **relation instance** is the actual set of tuples present at a particular point in time.

Schema:

~~~text
STUDENT(
    ID,
    Name,
    CGPA
)
~~~

Instance:

~~~text
+----+--------+-----+
| ID | Name   | CGPA|
+----+--------+-----+
| 1  | Arun   | 8.2 |
| 2  | Priya  | 9.1 |
+----+--------+-----+
~~~

If another student is inserted, the instance changes.

The schema may remain unchanged.

---

# 16. Schema vs Instance

| Schema | Instance |
|---|---|
| Structure | Current data |
| Relatively stable | Changes frequently |
| Defines attributes | Contains tuples |
| Example: columns | Example: rows |

Shortcut:

~~~text
Schema
→ Structure

Instance
→ Current Contents
~~~

---

# 17. Important Properties of a Relation

In the classical relational model, a relation has important properties.

### Property 1 — Unique Tuples

A relation is mathematically treated as a set of tuples, so duplicate tuples are not part of the pure relational model.

### Property 2 — Atomic Values

Each attribute value is atomic in the classical relational model.

### Property 3 — Same Attribute Structure

Every tuple in a relation follows the same relation schema.

### Property 4 — Attribute Names

Attributes have names.

### Property 5 — Order Is Not Semantically Important

The order of tuples and attributes is not fundamentally important in the mathematical relational model.

These points are useful for interviews.

---

# 18. Atomic Values

A fundamental relational-model idea is:

**Each attribute should contain an atomic value.**

Example:

Good:

~~~text
Student_ID | Name   | Phone
101        | Arun   | 9876543210
~~~

A problematic non-atomic design:

~~~text
Student_ID | Phone_Numbers
101        | 9876, 8765, 7654
~~~

The `Phone_Numbers` cell contains multiple values.

This violates the idea of atomic values used by first normal form.

This concept connects directly to:

[[1NF]]

---

# 19. Atomicity Recognition Trick

> [!important]
> If one cell contains:
>
> **multiple independent values**
>
> think:
>
> **Atomicity / 1NF issue**

Example:

~~~text
Phone
----------------
9876, 8765, 7654
~~~

Better design:

~~~text
Student_ID | Phone
-----------+----------
101        | 9876
101        | 8765
101        | 7654
~~~

or use an appropriate separate relation depending on the requirements.

---

# 20. Null Values

A relational database may use `NULL` to represent missing, unknown, or not-applicable information.

Example:

~~~text
Student_ID | Name  | Email
-----------+-------+------
101        | Arun  | NULL
~~~

`NULL` does not simply mean:

~~~text
0
```

or:

~~~text
empty string
```

or:

~~~text
false
```

It represents absence or unknown/non-applicable information depending on context.

---

# 21. Important NULL Trick

> [!warning]
> Do not compare NULL using:
>
> `= NULL`
>
> or
>
> `!= NULL`
>
> in SQL.

Use:

~~~sql
IS NULL
~~~

or:

~~~sql
IS NOT NULL
~~~

Example:

~~~sql
SELECT *
FROM Student
WHERE Email IS NULL;
~~~

This is a frequent SQL interview connection.

---

# 22. Keys in the Relational Model

Keys are extremely important because they identify tuples and establish relationships between relations.

Major keys include:

- Super Key
- Candidate Key
- Primary Key
- Alternate Key
- Foreign Key
- Composite Key

These topics will be studied separately in the **Keys** section.

For now remember:

~~~text
Keys
→ Identify rows
→ Establish relationships
→ Enforce integrity
~~~

---

# 23. Primary Key Connection

A primary key uniquely identifies each tuple in a relation.

Example:

~~~text
Student

+------------+--------+------+
| Student_ID | Name   | CGPA |
+------------+--------+------+
| 101        | Arun   | 8.2  |
| 102        | Priya  | 9.1  |
+------------+--------+------+
~~~

Here:

~~~text
Student_ID
→ Candidate for Primary Key
~~~

A primary key cannot contain `NULL`.

---

# 24. Foreign Key Connection

A foreign key represents a reference from one relation to another.

Example:

~~~text
Department

+--------+-------+
| DeptID | Name  |
+--------+-------+
| 10     | CSE   |
| 20     | ECE   |
+--------+-------+
~~~

Student:

~~~text
+----+-------+--------+
| ID | Name  | DeptID |
+----+-------+--------+
| 1  | Arun  | 10     |
| 2  | Priya | 20     |
+----+-------+--------+
~~~

`Student.DeptID` can reference `Department.DeptID`.

This creates a relationship between relations.

---

# 25. Relational Algebra

The relational model has a formal query foundation called:

**Relational Algebra**

It provides operations for manipulating relations.

Important operations include:

1. Selection
2. Projection
3. Union
4. Set Difference
5. Cartesian Product
6. Rename
7. Join

These are very important for DBMS interviews.

---

# 26. Selection

Selection chooses **rows** satisfying a condition.

Symbol:

~~~text
σ
~~~

Example:

~~~text
Student
```

Select students whose CGPA is greater than 8:

~~~text
σ CGPA > 8 (Student)
~~~

The result contains selected rows.

Shortcut:

> [!tip]
> **Selection = Rows**

Think:

~~~text
σ
↓
Filter Rows
~~~

---

# 27. Projection

Projection chooses specific **columns**.

Symbol:

~~~text
π
~~~

Example:

~~~text
π Name, CGPA (Student)
~~~

The result contains only:

~~~text
Name
CGPA
~~~

Shortcut:

> [!tip]
> **Projection = Columns**

Think:

~~~text
π
↓
Pick Columns
~~~

---

# 28. Selection vs Projection

This is one of the most important MCQ concepts.

| Operation | Selects | Memory |
|---|---|---|
| Selection | Rows | Filter |
| Projection | Columns | Pick columns |

Shortcut:

~~~text
Selection
→ WHERE-like filtering
→ Rows

Projection
→ SELECT columns
→ Columns
~~~

---

# 29. SQL Connection

Relational algebra and SQL are not identical, but a useful intuition is:

~~~sql
SELECT *
FROM Student
WHERE CGPA > 8;
~~~

Conceptually combines:

~~~text
Selection
→ CGPA > 8

Projection
→ Requested columns
~~~

This connection is very useful for learning SQL.

---

# 30. Union

Union combines compatible relations.

Symbol:

~~~text
∪
~~~

Example:

~~~text
CSE_Students
    ∪
ECE_Students
~~~

For union, the relations must be **union-compatible**.

Typically this means:

- Same number of attributes
- Corresponding attributes have compatible domains/types

Example:

~~~text
A(ID, Name)
B(ID, Name)
~~~

Then:

~~~text
A ∪ B
~~~

is valid.

---

# 31. Union Compatibility

Suppose:

~~~text
A(ID, Name)
B(Student_ID, Student_Name)
~~~

Even though attribute names differ, they may still be union-compatible if:

- Same number of attributes
- Corresponding domains are compatible

Attribute names do not necessarily have to be identical in a mathematical sense, depending on the formal operation and naming conventions.

For placement exams, remember:

~~~text
Union
→ Same degree
→ Compatible corresponding domains
~~~

---

# 32. Set Difference

Set difference is represented by:

~~~text
−
~~~

Example:

~~~text
A − B
~~~

means:

**Tuples present in A but not in B.**

Example:

~~~text
A = {1, 2, 3}
B = {2, 3}
```

Then:

~~~text
A − B = {1}
~~~

---

# 33. Cartesian Product

Cartesian product is represented by:

~~~text
×
~~~

Example:

~~~text
Student × Course
~~~

It combines every tuple from the first relation with every tuple from the second relation.

If:

~~~text
Student = 3 rows
Course = 4 rows
~~~

then:

~~~text
Student × Course
→ 3 × 4
→ 12 rows
~~~

This is a very important aptitude-style DBMS calculation.

---

# 34. Cartesian Product Shortcut

> [!tip]
> If relation A has `m` tuples and relation B has `n` tuples:
>
> **A × B has `m × n` tuples.**

Example:

~~~text
A = 5 rows
B = 7 rows

A × B
= 5 × 7
= 35 rows
~~~

---

# 35. Join

A join combines related tuples from multiple relations based on a condition.

Example:

~~~text
Student
    |
    | DeptID
    ↓
Department
~~~

SQL:

~~~sql
SELECT s.Name, d.Name
FROM Student s
JOIN Department d
  ON s.DeptID = d.DeptID;
~~~

The relational model uses joins to combine information stored in separate relations.

---

# 36. Why Joins Are Important

Relational databases often split data into multiple tables.

Example:

~~~text
Student
---------
ID
Name
DeptID
~~~

Department:

~~~text
Department
---------
DeptID
DeptName
~~~

Instead of storing:

~~~text
Student ID
Student Name
Department Name
Department Location
Department Head
...
~~`

repeatedly for every student, related information can be stored separately and combined when needed.

This is closely connected to normalization.

---

# 37. Rename

Rename changes the name of a relation or attributes for the purpose of an expression.

Symbol:

~~~text
ρ
~~~

Example:

~~~text
ρ S(Student)
~~~

This can rename the relation `Student` as `S`.

Rename becomes especially useful in self-joins.

---

# 38. Self-Join Connection

Suppose:

~~~text
Employee
---------------------
ID
Name
Manager_ID
```

The same relation may need to be referenced twice:

~~~text
Employee E
Employee M
~~~

One represents the employee.

The other represents the manager.

Rename helps distinguish the two logical instances.

---

# 39. Relational Algebra Master Table

| Operation | Symbol | Main Purpose | Memory |
|---|---|---|---|
| Selection | σ | Select rows | Filter |
| Projection | π | Select columns | Pick |
| Union | ∪ | Combine compatible tuples | OR |
| Difference | − | Tuples in A not B | A minus B |
| Cartesian Product | × | All tuple combinations | Multiply |
| Rename | ρ | Rename relation/attributes | Rename |
| Join | ⋈ | Combine related relations | Connect |

---

# 40. Selection Recognition

> [!important]
> If the question says:
>
> "Find students whose CGPA > 8"
>
> Think:
>
> **Selection**

Because the condition filters rows.

---

# 41. Projection Recognition

> [!important]
> If the question says:
>
> "Display only student names and CGPA"
>
> Think:
>
> **Projection**

Because only columns are selected.

---

# 42. Cartesian Product Recognition

> [!important]
> If the question says:
>
> "Combine every row of A with every row of B"
>
> Think:
>
> **Cartesian Product**

Shortcut:

~~~text
m rows × n rows
→ m × n combinations
~~~

---

# 43. Union Recognition

> [!important]
> If the question says:
>
> "Combine tuples from two compatible relations"
>
> Think:
>
> **Union**

Remember:

~~~text
Union
→ Union-Compatible Relations
~~~

---

# 44. Difference Recognition

> [!important]
> If the question says:
>
> "Records in A but not in B"
>
> Think:
>
> **A − B**
~~~

---

# 45. Join Recognition

> [!important]
> If the question says:
>
> "Combine Student and Department using DeptID"
>
> Think:
>
> **Join**

---

# 46. Basic Example — Relation

### Question

Consider:

~~~text
Employee(ID, Name, Salary)
~~~

What is the relation?

### Answer

The relation is:

~~~text
Employee
~~~

It is commonly represented as a table.

---

# 47. Basic Example — Tuple

### Question

Consider:

~~~text
+----+-------+-------+
| ID | Name  | Salary|
+----+-------+-------+
| 1  | Arun  | 50000 |
+----+-------+-------+
~~~

What is:

~~~text
(1, Arun, 50000)
~~~

?

### Answer

**Tuple**

---

# 48. Basic Example — Attribute

### Question

In:

~~~text
Student(ID, Name, CGPA)
~~~

What are the attributes?

### Answer

~~~text
ID
Name
CGPA
~~~

---

# 49. Basic Example — Degree

### Question

Consider:

~~~text
Employee(
    ID,
    Name,
    Department,
    Salary,
    Location
)
~~~

Find the degree.

### Solution

Number of attributes:

~~~text
5
~~~

Therefore:

~~~text
Degree = 5
~~~

---

# 50. Basic Example — Cardinality

### Question

A relation contains 8 rows and 4 columns.

Find:

1. Degree
2. Cardinality

### Solution

Columns:

~~~text
Degree = 4
~~~

Rows:

~~~text
Cardinality = 8
~~~

### Answer

~~~text
Degree = 4
Cardinality = 8
~~~

---

# 51. Medium Example — Selection

### Question

Given:

~~~text
Student

+----+--------+-----+
| ID | Name   | CGPA|
+----+--------+-----+
| 1  | Arun   | 7.5 |
| 2  | Priya  | 8.8 |
| 3  | Kiran  | 9.2 |
+----+--------+-----+
~~~

Find students whose CGPA is greater than 8.

### Pattern

Condition filters rows.

Therefore:

**Selection**

Relational algebra:

~~~text
σ CGPA > 8 (Student)
~~~

Result:

~~~text
Priya
Kiran
~~~

---

# 52. Medium Example — Projection

### Question

From:

~~~text
Student(ID, Name, CGPA, Department)
~~~

display only:

~~~text
Name
CGPA
~~~

### Pattern

Choosing columns.

Therefore:

**Projection**

Relational algebra:

~~~text
π Name, CGPA (Student)
~~~

---

# 53. Medium Example — Cartesian Product

### Question

Relation A has 4 rows.

Relation B has 6 rows.

How many rows can:

~~~text
A × B
~~~

produce?

### Formula

~~~text
m × n
~~~

### Calculation

~~~text
4 × 6 = 24
~~~

### Answer

**24 tuples**

---

# 54. Medium Example — Degree After Projection

### Question

A relation has 6 attributes.

A projection selects 3 attributes.

What is the degree of the resulting relation?

### Calculation

~~~text
Selected attributes = 3
~~~

Therefore:

~~~text
Degree = 3
~~~

---

# 55. Advanced Example — Selection + Projection

### Question

Given:

~~~text
Employee(
    ID,
    Name,
    Department,
    Salary
)
~~~

Find the names of employees whose salary is greater than ₹50,000.

### Step 1 — Filter Rows

Condition:

~~~text
Salary > 50000
~~~

Use:

**Selection**

### Step 2 — Select Required Column

Required column:

~~~text
Name
~~~

Use:

**Projection**

Conceptually:

~~~text
π Name (
    σ Salary > 50000 (Employee)
)
~~~

This is an extremely important relational algebra pattern.

---

# 56. Advanced Example — Join

### Tables

~~~text
Student

+----+--------+--------+
| ID | Name   | DeptID |
+----+--------+--------+
| 1  | Arun   | 10     |
| 2  | Priya  | 20     |
+----+--------+--------+
~~~

Department:

~~~text
Department

+--------+---------+
| DeptID | DeptName|
+--------+---------+
| 10     | CSE     |
| 20     | ECE     |
+--------+---------+
~~~

### Question

Find each student's department name.

### Pattern

Two relations must be connected using:

~~~text
DeptID
~~~

Therefore:

**Join**

---

# 57. Advanced Example — Cartesian Product Calculation

### Question

Relation A has:

~~~text
8 tuples
```

Relation B has:

~~~text
5 tuples
```

Find the maximum number of tuples in:

~~~text
A × B
~~~

### Calculation

~~~text
8 × 5 = 40
~~~

### Answer

~~~text
40 tuples
~~~

---

# 58. Advanced Example — Union

Suppose:

~~~text
CSE_Students
= {101, 102, 103}

ECE_Students
= {103, 104, 105}
~~~

Then:

~~~text
CSE_Students ∪ ECE_Students
~~~

produces:

~~~text
{101, 102, 103, 104, 105}
~~~

Duplicate tuple `103` appears only once in pure set-based relational algebra.

---

# 59. Advanced Example — Difference

Given:

~~~text
A = {1, 2, 3, 4}

B = {3, 4, 5}
~~~

Find:

~~~text
A − B
~~~

The elements in A but not B are:

~~~text
{1, 2}
~~~

### Answer

~~~text
A − B = {1, 2}
~~~

---

# 60. Important Relational Algebra Trick

> [!tip]
> Remember:
>
> **Selection = Horizontal Filtering**
>
> **Projection = Vertical Filtering**

Visual:

~~~text
TABLE

+----+--------+------+
| ID | Name   | CGPA |
+----+--------+------+
| 1  | Arun   | 8.2  |
| 2  | Priya  | 9.1  |
| 3  | Kiran  | 7.8  |
+----+--------+------+

Selection
→ Remove unwanted ROWS

Projection
→ Remove unwanted COLUMNS
~~~

---

# 61. Important Relational Model Properties

### 1. Atomicity

Values are atomic.

### 2. Unique Tuples

The pure mathematical relation is a set, so duplicate tuples are not allowed.

### 3. Same Structure

Every tuple conforms to the same schema.

### 4. Attribute Names

Each attribute has a name.

### 5. Domain Constraints

Values belong to defined domains.

### 6. Order Independence

Tuple order has no logical significance.

### 7. Attribute Order

The logical meaning does not depend fundamentally on the order in which attributes are listed.

---

# 62. Order of Rows

Suppose:

~~~text
Student

101 Arun
102 Priya
103 Kiran
~~~

and:

~~~text
103 Kiran
101 Arun
102 Priya
~~~

The relational model does not assign semantic meaning to the order of tuples.

This is important because tables should be thought of as unordered relations, even though SQL may return rows in some order unless `ORDER BY` is specified.

---

# 63. SQL Ordering Trick

> [!warning]
> Do not assume SQL query results are guaranteed to appear in a particular order unless `ORDER BY` is specified.

Example:

~~~sql
SELECT *
FROM Student;
~~~

Do not rely on:

~~~text
101
102
103
~~~

being returned in that order.

If order matters:

~~~sql
SELECT *
FROM Student
ORDER BY Student_ID;
~~~

---

# 64. Relational Integrity

The relational model supports important integrity concepts.

Major categories include:

### Entity Integrity

A primary key should uniquely identify tuples and cannot be `NULL`.

### Referential Integrity

A foreign-key value must correspond to an appropriate referenced key value, subject to SQL's handling of `NULL` and constraint actions.

### Domain Integrity

Values should satisfy the defined domain and applicable constraints.

These topics will be studied in greater detail later.

---

# 65. Entity Integrity

Example:

~~~text
Student

Student_ID
-----------
101
102
103
```

If `Student_ID` is the primary key:

~~~text
No duplicate values
No NULL
~~~

This ensures each tuple can be uniquely identified.

---

# 66. Referential Integrity

Suppose:

~~~text
Department
-----------
10
20
30
```

Student:

~~~text
Student
----------------
ID | DeptID
1  | 10
2  | 20
~~~

`Student.DeptID` references `Department.DeptID`.

If a student has:

~~~text
DeptID = 99
~~~

and department 99 does not exist, the foreign-key constraint can reject the operation, depending on the database schema and operation.

---

# 67. Domain Integrity

Suppose:

~~~text
CGPA
```

must be within:

~~~text
0 to 10
~~~

Then:

~~~text
CGPA = 12
~~~

should not be accepted if the schema has a constraint enforcing that domain.

This maintains valid values.

---

# 68. Real-Time Example — E-Commerce

Consider:

~~~text
Customer
Product
Order
OrderItem
~~~

Relations:

~~~text
Customer
Product
Order
OrderItem
~~~

Instead of putting everything into one huge table, the relational model separates logically related data.

Relationships can then be represented using keys.

Example:

~~~text
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
~~~

This is the foundation of many real-world business systems.

---

# 69. Real-Time Example — Banking

Relations:

~~~text
Customer
Account
Transaction
Branch
Loan
~~~

Example:

~~~text
Customer
   ↓
Account
   ↓
Transaction
```

A bank can store each concept separately and connect them through keys.

This improves organization and reduces unnecessary duplication.

---

# 70. Real-Time Example — College Management

Relations:

~~~text
Student
Department
Course
Faculty
Enrollment
~~~

Relationships:

~~~text
Student
   ↓
Department

Student
   ↓
Enrollment
   ↓
Course

Faculty
   ↓
Course
~~~

This demonstrates how a relational database models real-world entities using multiple relations.

---

# 71. Real-Time Example — Hospital

Relations:

~~~text
Patient
Doctor
Appointment
Prescription
Billing
LabReport
~~~

Relationships can be represented using keys:

~~~text
Patient
   ↓
Appointment
   ↓
Doctor
```

and:

~~~text
Appointment
   ↓
Prescription
```

The relational model allows complex real-world systems to be represented using multiple connected tables.

---

# 72. Why Relational Model Became Popular

Important reasons include:

### 1. Simple Table Representation

Data is easy to visualize.

### 2. Declarative Querying

SQL lets users specify what data they want.

### 3. Mathematical Foundation

Relational algebra and relational calculus provide formal foundations.

### 4. Flexible Relationships

Tables can be connected using keys and joins.

### 5. Normalization

Data can be organized to reduce redundancy.

### 6. Data Independence

Logical and physical separation can be maintained through DBMS architecture.

### 7. Mature Ecosystem

Relational databases have extensive tools, standards, and industry adoption.

---

# 73. Relational Model vs Hierarchical Model

| Feature | Hierarchical | Relational |
|---|---|---|
| Structure | Tree | Tables |
| Main Unit | Record | Relation |
| Relationships | Parent-child | Keys / joins |
| Many-to-Many | Difficult | Well supported |
| Access | Navigational | Declarative SQL |
| Flexibility | Lower | Higher |
| Data Organization | Hierarchical | Tabular |

Memory:

~~~text
Tree → Hierarchical
Table → Relational
~~~

---

# 74. Relational Model vs Network Model

| Feature | Network | Relational |
|---|---|---|
| Structure | Graph-like | Tables |
| Access | Navigational | Declarative |
| Relationships | Links/Sets | Keys/Joins |
| Querying | Path-oriented | SQL |
| Flexibility | High | Very high |
| Logical Simplicity | Lower | Higher |

---

# 75. Relational Model vs ER Model

These are often confused.

### ER Model

Used primarily for conceptual database design.

~~~text
Entity
Attribute
Relationship
~~~

### Relational Model

Represents the database logically using:

~~~text
Relations
Attributes
Tuples
Keys
~~~

A common design flow is:

~~~text
Real World
    ↓
ER Model
    ↓
Relational Schema
    ↓
Database Tables
~~~

---

# 76. ER to Relational Intuition

Suppose ER model contains:

~~~text
Student
   |
enrolls
   |
Course
~~~

The relational design may become:

~~~text
Student
---------
Student_ID
Name

Course
---------
Course_ID
Course_Name

Enrollment
---------
Student_ID
Course_ID
~~~

The many-to-many relationship becomes an associative relation.

This connection is very important for DBMS interviews.

---

# 77. Common Exam Patterns

> [!important] Must Master

1. Definition of relational model
2. Relation
3. Tuple
4. Attribute
5. Domain
6. Degree
7. Cardinality
8. Relation schema
9. Relation instance
10. Schema vs instance
11. Atomic values
12. NULL
13. Keys
14. Entity integrity
15. Referential integrity
16. Domain integrity
17. Relational algebra
18. Selection
19. Projection
20. Union
21. Difference
22. Cartesian product
23. Join
24. Rename
25. Selection vs projection
26. Degree vs cardinality
27. Relational vs hierarchical
28. Relational vs network
29. Relational vs ER model
30. Many-to-many relationships
31. Cartesian-product tuple calculations
32. SQL and relational algebra connection

---

# 78. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Degree Means Rows

Wrong.

~~~text
Degree
→ Number of Attributes
→ Columns
~~~

---

### Mistake 2 — Cardinality Means Columns

Wrong.

~~~text
Cardinality
→ Number of Tuples
→ Rows
~~~

---

### Mistake 3 — Selection Means Columns

Wrong.

~~~text
Selection
→ Rows
~~~

---

### Mistake 4 — Projection Means Rows

Wrong.

~~~text
Projection
→ Columns
~~~

---

### Mistake 5 — Cartesian Product Adds Rows

Not generally.

If:

~~~text
A = m rows
B = n rows
~~~

then:

~~~text
A × B
= m × n rows
~~~

---

### Mistake 6 — NULL Means Zero

Wrong.

`NULL` represents missing, unknown, or not-applicable information depending on context.

---

### Mistake 7 — `= NULL` Is Correct SQL

Wrong.

Use:

~~~sql
IS NULL
~~~

---

### Mistake 8 — Relation Always Means Relationship

In relational-model terminology:

~~~text
Relation
→ Table
~~~

Do not confuse it with the general English meaning of relationship.

---

### Mistake 9 — Row Order Is Meaningful

The pure relational model treats tuples as unordered.

SQL result order should not be relied upon without:

~~~sql
ORDER BY
~~~

---

### Mistake 10 — Relational Model Means Only SQL

SQL is the dominant language for relational database systems, but the relational model itself is a mathematical/logical data model.

---

# 79. Interview Questions

## Q1. What is the relational model?

### Strong Answer

> The relational model represents data as relations, which are commonly implemented as tables. Each relation consists of tuples, represented as rows, and attributes, represented as columns. Relationships between tables can be represented using keys and queried using operations such as selection, projection, and joins.

---

## Q2. What is a relation?

### Answer

> A relation is a set of tuples defined over a collection of attributes. In practical DBMS terminology, it is commonly represented as a table.

---

## Q3. What is a tuple?

### Answer

> A tuple is an individual row or record in a relation.

---

## Q4. What is an attribute?

### Answer

> An attribute is a named property or column of a relation.

---

## Q5. What is a domain?

### Answer

> A domain defines the set of valid values that an attribute can take.

---

# 80. Interview Questions — Degree and Cardinality

## Q6. What is the degree of a relation?

> The degree is the number of attributes or columns in a relation.

---

## Q7. What is the cardinality of a relation?

> The cardinality is the number of tuples or rows in a relation.

---

## Q8. A table has 5 columns and 100 rows. What are its degree and cardinality?

~~~text
Degree = 5
Cardinality = 100
~~~

---

# 81. Interview Questions — Relational Algebra

## Q9. What is selection?

> Selection chooses tuples that satisfy a specified condition.

Symbol:

~~~text
σ
~~~

Memory:

~~~text
Selection
→ Rows
~~~

---

## Q10. What is projection?

> Projection selects specific attributes or columns from a relation.

Symbol:

~~~text
π
~~~

Memory:

~~~text
Projection
→ Columns
~~~

---

## Q11. What is Cartesian product?

> Cartesian product combines every tuple of one relation with every tuple of another relation.

If A has `m` tuples and B has `n` tuples:

~~~text
|A × B| = m × n
~~~

---

## Q12. What is a join?

> A join combines related tuples from two or more relations based on a matching or specified condition.

---

# 82. Interview Questions — Properties

## Q13. Are duplicate tuples allowed in a pure relational model?

> A mathematical relation is a set of tuples, so duplicate tuples are not part of the pure relational model. SQL, however, uses bag/multiset semantics by default in many query contexts unless `DISTINCT` is used.

This distinction is important for advanced interviews.

---

## Q14. Is the order of rows important in the relational model?

> No. The relational model treats a relation as a set, so tuple order has no semantic significance.

---

## Q15. Are values in a relation atomic?

> In the classical relational model, attribute values are atomic. This idea is central to first normal form.

---

# 83. Advanced Interview Question — Selection vs Projection

### Question

What is the difference between selection and projection?

### Strong Answer

> Selection filters rows based on a condition, while projection selects specific columns.

Example:

~~~text
Selection:
σ CGPA > 8 (Student)

Projection:
π Name, CGPA (Student)
~~~

Memory:

~~~text
Selection
→ Horizontal filtering
→ Rows

Projection
→ Vertical filtering
→ Columns
~~~

---

# 84. Advanced Interview Question — Degree vs Cardinality

### Question

A relation has 10 tuples and 6 attributes. What are its degree and cardinality?

### Answer

~~~text
Degree = 6
Cardinality = 10
~~~

Memory:

~~~text
Columns → Degree
Rows → Cardinality
~~~

---

# 85. Advanced Interview Question — Cartesian Product

### Question

Relation A contains 20 tuples and relation B contains 15 tuples. How many tuples can their Cartesian product contain?

### Formula

~~~text
|A × B| = |A| × |B|
~~~

### Calculation

~~~text
20 × 15 = 300
~~~

### Answer

**300 tuples**

---

# 86. Advanced Interview Question — Why Normalize?

### Question

Why are relations often decomposed into multiple tables?

### Answer

To reduce:

- Data redundancy
- Update anomalies
- Insertion anomalies
- Deletion anomalies

and improve:

- Data consistency
- Maintainability
- Logical organization

This leads directly to:

[[Normalization]]

---

# 87. Advanced Interview Question — Relational Model Strength

### Question

Why is the relational model suitable for general-purpose database applications?

### Answer

Because it provides:

~~~text
Simple tabular representation
+
Declarative querying
+
Flexible relationships
+
Keys
+
Constraints
+
Normalization
+
Strong mathematical foundation
~~~

---

# 88. Advanced Interview Question — Relational vs Hierarchical

### Question

Why is the relational model more flexible than the classical hierarchical model?

### Answer

The relational model stores data in separate relations and connects them using keys and operations such as joins.

It does not require the entire database to follow a single tree structure.

Therefore, complex relationships such as many-to-many relationships can be represented naturally through appropriate relational designs.

---

# 89. Advanced Interview Question — ER to Relational

### Question

How can an ER model be converted into a relational model?

### Basic Mapping

~~~text
Entity
→ Relation / Table

Simple Attribute
→ Column

Key Attribute
→ Primary Key

1:N Relationship
→ Foreign Key on the N-side

M:N Relationship
→ New Relation containing foreign keys
~~~

Example:

~~~text
Student
   ↕
Course
~~~

becomes:

~~~text
Student
---------
Student_ID

Course
---------
Course_ID

Enrollment
---------
Student_ID
Course_ID
~~~

---

# 90. IIT-Level Thinking Pattern

When you see a relational-model question, first identify what the question is asking.

~~~text
TABLE?
   ↓
Relation

ROW?
   ↓
Tuple

COLUMN?
   ↓
Attribute

ALLOWED VALUES?
   ↓
Domain

NUMBER OF COLUMNS?
   ↓
Degree

NUMBER OF ROWS?
   ↓
Cardinality

FILTER ROWS?
   ↓
Selection

SELECT COLUMNS?
   ↓
Projection

ALL COMBINATIONS?
   ↓
Cartesian Product

COMBINE RELATED TABLES?
   ↓
Join

COMBINE COMPATIBLE RELATIONS?
   ↓
Union

A BUT NOT B?
   ↓
Difference
~~~

This decision tree is extremely powerful for DBMS MCQs.

---

# 91. Master Recognition Table

| Clue | Answer |
|---|---|
| Table | Relation |
| Row | Tuple |
| Column | Attribute |
| Valid value set | Domain |
| Number of columns | Degree |
| Number of rows | Cardinality |
| Structure | Schema |
| Current data | Instance |
| Filter rows | Selection |
| Select columns | Projection |
| Combine every row | Cartesian Product |
| A but not B | Difference |
| Combine compatible relations | Union |
| Combine related tables | Join |
| Rename relation | Rename |
| Unique row identifier | Primary Key |
| Reference another relation | Foreign Key |
| Missing/unknown value | NULL |

---

# 92. Quick Calculation Tricks

> [!tip]
> **Shortcut 1 — Degree**
>
> Count columns.

~~~text
A | B | C | D
```

Degree:

~~~text
4
~~~

---

> [!tip]
> **Shortcut 2 — Cardinality**
>
> Count rows.

~~~text
4 records
→ Cardinality = 4
~~~

---

> [!tip]
> **Shortcut 3 — Cartesian Product**

~~~text
m × n
~~~

If:

~~~text
A = 12 rows
B = 8 rows
~~~

then:

~~~text
A × B = 96 rows
~~~

---

> [!tip]
> **Shortcut 4 — Selection**

Condition?

~~~text
Selection
~~~

---

> [!tip]
> **Shortcut 5 — Projection**

Columns?

~~~text
Projection
~~~

---

> [!tip]
> **Shortcut 6 — Join**

Matching relationship?

~~~text
Join
~~~

---

# 93. Placement-Level MCQ Examples

## MCQ 1

A relation has 7 attributes and 50 tuples. What is its degree?

A. 7  
B. 50  
C. 57  
D. 350

### Answer

**A. 7**

Reason:

~~~text
Degree = Number of Attributes
```

---

## MCQ 2

A relation contains 20 rows and 5 columns. Its cardinality is:

A. 5  
B. 20  
C. 25  
D. 100

### Answer

**B. 20**

---

## MCQ 3

Which relational algebra operation selects rows?

A. Projection  
B. Selection  
C. Union  
D. Rename

### Answer

**B. Selection**

---

## MCQ 4

Which operation selects columns?

A. Selection  
B. Projection  
C. Difference  
D. Product

### Answer

**B. Projection**

---

## MCQ 5

A relation has 10 tuples and another has 6 tuples. The Cartesian product has:

A. 16  
B. 60  
C. 10  
D. 6

### Answer

**B. 60**

Because:

~~~text
10 × 6 = 60
~~~

---

# 94. Placement-Level MCQ — Advanced

## MCQ 6

Which statement is correct?

A. Degree is number of rows  
B. Cardinality is number of columns  
C. Degree is number of attributes  
D. Degree is number of tuples

### Answer

**C. Degree is number of attributes**

---

## MCQ 7

Which operation is primarily used to combine related tuples from different relations?

A. Selection  
B. Projection  
C. Join  
D. Rename

### Answer

**C. Join**

---

## MCQ 8

Which operation returns tuples present in A but not B?

A. A ∪ B  
B. A × B  
C. A − B  
D. A ⋈ B

### Answer

**C. A − B**

---

# 95. Formula Sheet

~~~text
RELATIONAL MODEL

Relation
→ Table

Tuple
→ Row

Attribute
→ Column

Domain
→ Allowed Set of Values


DEGREE
→ Number of Attributes / Columns


CARDINALITY
→ Number of Tuples / Rows


SCHEMA
→ Structure


INSTANCE
→ Current Data


RELATIONAL ALGEBRA

Selection
→ σ
→ Rows

Projection
→ π
→ Columns

Union
→ ∪

Difference
→ −

Cartesian Product
→ ×

Rename
→ ρ

Join
→ ⋈


CARTESIAN PRODUCT

If:
A = m tuples
B = n tuples

Then:
|A × B| = m × n


MEMORY

Selection
→ Rows

Projection
→ Columns

Degree
→ Columns

Cardinality
→ Rows
~~~

---

# 96. Quick Revision

> [!summary] One-Minute Revision

~~~text
RELATIONAL MODEL
→ Represents data using relations/tables.

RELATION
→ Table

TUPLE
→ Row

ATTRIBUTE
→ Column

DOMAIN
→ Allowed set of values

DEGREE
→ Number of columns

CARDINALITY
→ Number of rows

SCHEMA
→ Structure

INSTANCE
→ Current contents

IMPORTANT PROPERTIES
→ Atomic values
→ Same schema for tuples
→ Duplicate tuples excluded in pure relational model
→ Tuple order has no semantic significance
→ Attribute order has no fundamental semantic significance

RELATIONAL ALGEBRA

SELECTION
→ Rows
→ σ

PROJECTION
→ Columns
→ π

UNION
→ Compatible relations
→ ∪

DIFFERENCE
→ A but not B
→ −

CARTESIAN PRODUCT
→ Every combination
→ ×

RENAME
→ Rename relation/attributes
→ ρ

JOIN
→ Combine related relations
→ ⋈

IMPORTANT INTEGRITY

Entity Integrity
→ Primary key uniqueness + no NULL

Referential Integrity
→ Foreign key references valid referenced key values

Domain Integrity
→ Values follow valid domains/constraints

FAST RECOGNITION

Table
→ Relation

Row
→ Tuple

Column
→ Attribute

Allowed Values
→ Domain

Columns Count
→ Degree

Rows Count
→ Cardinality

Filter Rows
→ Selection

Choose Columns
→ Projection

Every Combination
→ Cartesian Product

Related Tables
→ Join

A but not B
→ Difference

Compatible Tables
→ Union
~~~

---

# 97. Golden Memory Trick

**Relational Model = Tables, Rows, Columns, Keys, and Relationships through Joins.**

# 98. One-Line Recognition

**Whenever a DBMS question talks about tables, tuples, attributes, degree, cardinality, selection, projection, or joins, think Relational Model.**