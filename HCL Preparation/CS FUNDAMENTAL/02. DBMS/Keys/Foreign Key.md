---
type: concept
subject: dbms
topic: "Foreign Key"
parent: "Keys"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - keys
  - foreign-key
  - primary-key
  - referential-integrity
  - constraints
  - relational-model
  - sql
  - database-design
  - relationships
  - hcl
  - tcs
  - infosys
  - zoho
  - accenture
  - wipro
  - cognizant
  - capgemini
  - cs-fundamentals
  - interview
wikilinks:
  - "[[Keys]]"
  - "[[Primary Key]]"
  - "[[Candidate Key]]"
  - "[[Composite Key]]"
  - "[[Constraints]]"
  - "[[ER Model]]"
  - "[[ER Diagram]]"
  - "[[Normalization]]"
---

# Foreign Key

## 1. Core Concept

> [!summary]
> A **Foreign Key (FK)** is a column or set of columns in one table that references a key in another table, allowing the database to represent relationships between tables and enforce referential integrity.

The easiest memory:

**Primary Key = Identity**

**Foreign Key = Relationship**

Example:

~~~text
DEPARTMENT
-----------
Department_ID  ← Primary Key

        ↑
        |
        |
Department_ID  ← Foreign Key
EMPLOYEE
~~~

The foreign key connects:

~~~text
EMPLOYEE
   ↓
DEPARTMENT
~~~

It tells the database:

> "This employee belongs to this department."

---

# 2. Basic Meaning

Consider two tables.

### Department

| Department_ID | Department_Name |
|---:|---|
| 1 | CSE |
| 2 | ECE |
| 3 | EEE |

Here:

`Department_ID`

is the primary key.

### Employee

| Employee_ID | Employee_Name | Department_ID |
|---:|---|---:|
| 101 | Arun | 1 |
| 102 | Priya | 2 |
| 103 | Ravi | 1 |

Here:

`Employee_ID`

is the primary key of Employee.

`Department_ID`

is the foreign key.

It references:

`Department.Department_ID`

Therefore:

~~~text
Department
    1
    |
    | belongs to
    |
    N
Employee
~~~

---

# 3. Why Do We Need Foreign Keys?

Without foreign keys, the database could contain invalid references.

Example:

| Employee_ID | Name | Department_ID |
|---:|---|---:|
| 101 | Arun | 1 |
| 102 | Priya | 999 |

If department `999` does not exist, what does Priya belong to?

There is no valid answer.

A foreign-key constraint can prevent such invalid references.

Therefore:

> [!important]
> **Foreign Key → Maintains Referential Integrity**

---

# 4. Referential Integrity

Referential integrity means that a foreign-key value should refer to a valid key value in the referenced table, subject to the schema's NULL and action rules.

Example:

Parent table:

`DEPARTMENT`

| Department_ID |
|---:|
| 1 |
| 2 |
| 3 |

Child table:

`EMPLOYEE`

| Employee_ID | Department_ID |
|---:|---:|
| 101 | 1 |
| 102 | 2 |
| 103 | 3 |

Valid.

But:

| Employee_ID | Department_ID |
|---:|---:|
| 104 | 99 |

is invalid if department `99` does not exist and the foreign-key constraint is enforced.

---

# 5. Parent Table and Child Table

When a foreign key is involved, use these terms.

~~~text
Referenced Table
→ Parent Table

Referencing Table
→ Child Table
~~~

Example:

~~~text
DEPARTMENT
    ↓
Parent Table

EMPLOYEE
    ↓
Child Table
~~~

Why?

Because:

`Employee.Department_ID`

references:

`Department.Department_ID`

Memory:

> [!tip]
> **Parent owns the referenced key. Child contains the foreign key.**

---

# 6. Basic Relationship

Suppose:

~~~text
DEPARTMENT
1
|
|
N
EMPLOYEE
~~~

Implementation:

~~~text
DEPARTMENT
-----------
Department_ID PK

EMPLOYEE
-----------
Employee_ID PK
Department_ID FK
~~~

The foreign key goes on the:

**N-side**

for a normal `1:N` relationship.

This is one of the most important DBMS patterns.

---

# 7. Foreign Key SQL Syntax

Example:

~~~sql
CREATE TABLE Department (
    Department_ID INT PRIMARY KEY,
    Department_Name VARCHAR(100)
);

CREATE TABLE Employee (
    Employee_ID INT PRIMARY KEY,
    Employee_Name VARCHAR(100),
    Department_ID INT,
    FOREIGN KEY (Department_ID)
        REFERENCES Department(Department_ID)
);
~~~

Here:

~~~text
Department.Department_ID
→ Primary Key

Employee.Department_ID
→ Foreign Key
~~~

---

# 8. Foreign Key Recognition

> [!important]
> If the question says:
>
> "A column in one table references the primary key of another table"
>
> think:
>
> **Foreign Key**

Example:

~~~text
Customer.Customer_ID
        ↑
        |
Order.Customer_ID
~~~

`Order.Customer_ID`

is the foreign key.

---

# 9. Primary Key vs Foreign Key

| Feature | Primary Key | Foreign Key |
|---|---|---|
| Main purpose | Identifies rows | Creates/maintains relationship |
| Uniqueness | Must be unique | Need not be unique |
| NULL | Cannot be NULL | May be NULL if allowed |
| Number per table | At most one PK constraint | Multiple FKs possible |
| References another table | No | Yes |
| Referential integrity | Referenced key | Enforces reference |
| Example | Student_ID | Department_ID |

Memory:

~~~text
PK
→ "Who am I?"

FK
→ "Which parent am I connected to?"
~~~

---

# 10. Foreign Key Does Not Need to Be Unique

This is a very common interview trap.

Consider:

| Employee_ID | Name | Department_ID |
|---:|---|---:|
| 101 | Arun | 1 |
| 102 | Priya | 1 |
| 103 | Ravi | 1 |

All three employees belong to department `1`.

Therefore:

`Department_ID`

appears multiple times.

That is completely valid.

So:

> [!warning]
> **Foreign Key ≠ Unique Key**

A foreign key usually represents many child rows pointing to the same parent.

---

# 11. Why Foreign Keys Are Often Repeated

Suppose:

`Department 1 = CSE`

Employees:

~~~text
Arun → CSE
Priya → CSE
Ravi → CSE
~~~

Table:

| Employee_ID | Department_ID |
|---:|---:|
| 101 | 1 |
| 102 | 1 |
| 103 | 1 |

The repeated value:

`1`

is intentional.

It represents:

~~~text
One Department
      ↓
Many Employees
~~~

Therefore:

`1:N`

naturally produces repeated foreign-key values on the N-side.

---

# 12. Foreign Key and 1:N Relationship

This is one of the most important patterns.

Suppose:

~~~text
DEPARTMENT
    1
    |
    |
    N
EMPLOYEE
~~~

Then:

~~~text
EMPLOYEE.Department_ID
→ FK
~~~

because the foreign key is placed on the many side.

Memory:

> [!tip]
> **1:N → Put the FK on the N-side.**

---

# 13. Example — Department and Employee

Parent:

~~~text
Department
-----------
Department_ID PK
Department_Name
~~~

Child:

~~~text
Employee
-----------
Employee_ID PK
Employee_Name
Department_ID FK
~~~

Relationship:

~~~text
Department
1
|
N
Employee
~~~

The same department ID can appear in many Employee rows.

---

# 14. Foreign Key and 1:1 Relationship

Suppose:

~~~text
PERSON
1
|
1
PASSPORT
~~~

A possible design is:

~~~text
PERSON
-----------
Person_ID PK

PASSPORT
-----------
Passport_ID PK
Person_ID FK UNIQUE
~~~

Why `UNIQUE`?

Because without uniqueness, multiple passports could reference the same person.

With:

`Person_ID FK + UNIQUE`

we can enforce a one-to-one relationship under appropriate business rules.

---

# 15. Foreign Key and M:N Relationship

Suppose:

~~~text
STUDENT
M
|
|
N
COURSE
~~~

A relational database normally introduces an intermediate table:

~~~text
ENROLLMENT
-----------
Student_ID
Course_ID
~~~

Then:

~~~text
STUDENT
1
|
N
ENROLLMENT
N
|
1
COURSE
~~~

Foreign keys:

~~~text
Enrollment.Student_ID
→ Student.Student_ID

Enrollment.Course_ID
→ Course.Course_ID
~~~

This is one of the highest-value DBMS interview patterns.

---

# 16. M:N Transformation

Original:

~~~text
Student
M:N
Course
~~~

Transformation:

~~~text
Student
1:N
Enrollment
N:1
Course
~~~

SQL:

~~~sql
CREATE TABLE Enrollment (
    Student_ID INT,
    Course_ID INT,
    PRIMARY KEY (Student_ID, Course_ID),
    FOREIGN KEY (Student_ID)
        REFERENCES Student(Student_ID),
    FOREIGN KEY (Course_ID)
        REFERENCES Course(Course_ID)
);
~~~

---

# 17. Composite Foreign Key

A foreign key can contain multiple columns.

Example parent table:

~~~text
Enrollment
----------------
Student_ID
Course_ID
PRIMARY KEY (Student_ID, Course_ID)
~~~

Another table may reference both columns:

~~~text
Grade_Record
----------------
Student_ID
Course_ID
Grade
~~~

Foreign key:

~~~text
(Student_ID, Course_ID)
→ References Enrollment(Student_ID, Course_ID)
~~~

This is called a:

**Composite Foreign Key**

---

# 18. Composite Foreign Key SQL

~~~sql
CREATE TABLE Enrollment (
    Student_ID INT,
    Course_ID INT,
    PRIMARY KEY (Student_ID, Course_ID)
);

CREATE TABLE Grade_Record (
    Student_ID INT,
    Course_ID INT,
    Grade CHAR(2),

    FOREIGN KEY (Student_ID, Course_ID)
        REFERENCES Enrollment(Student_ID, Course_ID)
);
~~~

The number and ordering of referenced columns must match the referenced key definition as required by the DBMS.

---

# 19. Foreign Key and NULL

A foreign key can often contain NULL if the column is not declared `NOT NULL`.

Example:

| Employee_ID | Department_ID |
|---:|---:|
| 101 | 1 |
| 102 | NULL |

This can mean:

> The employee currently has no department assigned.

A NULL foreign key generally means:

> There is no referenced parent value for this row.

This is different from referencing a nonexistent value such as `999`.

---

# 20. NULL vs Invalid Foreign Key

Consider:

~~~text
Department IDs:
1
2
3
~~~

Child row:

~~~text
Department_ID = NULL
~~~

Potentially valid if NULL is allowed.

Child row:

~~~text
Department_ID = 999
~~~

Invalid if department `999` does not exist.

Therefore:

~~~text
NULL
→ No reference

999
→ Attempted reference to nonexistent parent
~~~

This distinction is important.

---

# 21. Foreign Key and DELETE

Suppose:

~~~text
Department 1
   ↓
Employees 101, 102, 103
~~~

Now execute:

~~~sql
DELETE FROM Department
WHERE Department_ID = 1;
~~~

What should happen to the employees?

The database needs a defined referential action or may reject the delete depending on the schema.

Common options include:

~~~text
RESTRICT / NO ACTION
CASCADE
SET NULL
SET DEFAULT
~~~

Exact behavior depends on the DBMS and constraint definition.

---

# 22. ON DELETE CASCADE

`CASCADE` means changes to the parent can automatically propagate to matching child rows.

Example:

~~~sql
CREATE TABLE Employee (
    Employee_ID INT PRIMARY KEY,
    Department_ID INT,
    FOREIGN KEY (Department_ID)
        REFERENCES Department(Department_ID)
        ON DELETE CASCADE
);
~~~

If department `1` is deleted, matching employee rows may also be deleted.

Conceptually:

~~~text
Delete Parent
      ↓
Delete Related Children
~~~

---

# 23. When Is CASCADE Dangerous?

Suppose:

~~~text
Customer
  ↓
Order
  ↓
Order_Item
  ↓
Payment
~~~

If cascading deletes are configured broadly, deleting one customer could potentially remove a large amount of related data.

Therefore:

> [!warning]
> Use `ON DELETE CASCADE` carefully.

It is appropriate when child data has no independent meaning without the parent.

---

# 24. ON DELETE SET NULL

Another option is:

~~~sql
ON DELETE SET NULL
~~~

If the parent row is deleted, the child foreign-key value becomes NULL.

Example:

~~~text
Employee
Department_ID = 1
```

Delete:

~~~text
Department 1
```

Then:

~~~text
Employee.Department_ID
→ NULL
~~~

This requires the FK column to permit NULL.

---

# 25. ON DELETE RESTRICT / NO ACTION

Depending on the DBMS, `RESTRICT` or `NO ACTION` can prevent deletion of a parent when matching child rows exist.

Conceptually:

~~~text
Parent has children
        ↓
Delete Parent
        ↓
Reject Delete
~~~

This protects referenced data.

---

# 26. ON DELETE Comparison

| Action | Effect |
|---|---|
| CASCADE | Delete related child rows |
| SET NULL | Set child FK to NULL |
| SET DEFAULT | Set child FK to default value if supported/valid |
| RESTRICT | Prevent delete when dependent rows exist |
| NO ACTION | Enforce referential constraint according to DBMS timing/rules |

---

# 27. Foreign Key and UPDATE

Foreign-key actions can also be defined for parent-key updates.

Example:

~~~sql
ON UPDATE CASCADE
~~~

Conceptually:

~~~text
Parent Key Changes
        ↓
Child FK Updates
```

This is supported by some DBMSs and depends on the database engine.

---

# 28. ON UPDATE CASCADE Example

Suppose:

~~~text
Department_ID = 10
```

Employee rows:

~~~text
Employee 101 → 10
Employee 102 → 10
~~~

If the parent key changes:

~~~text
10 → 20
~~~

with appropriate cascading behavior:

~~~text
Employee 101 → 20
Employee 102 → 20
~~~

The references remain consistent.

---

# 29. Foreign Key and Referential Actions

Remember:

~~~text
DELETE
→ What happens to children?

UPDATE
→ What happens to references?
~~~

Possible actions:

~~~text
CASCADE
SET NULL
SET DEFAULT
RESTRICT
NO ACTION
~~~

This is a common SQL interview topic.

---

# 30. Foreign Key and Parent-Child Terminology

Example:

~~~text
CUSTOMER
    ↓
ORDER
```

`CUSTOMER`

is:

`Parent`

`ORDER`

is:

`Child`

Because:

`Order.Customer_ID`

references:

`Customer.Customer_ID`

Memory:

> [!tip]
> **The table containing the referenced key is the parent.**
>
> **The table containing the foreign key is the child.**

---

# 31. Foreign Key Can Reference a Unique Key

A common oversimplification is:

> "A foreign key can only reference a primary key."

More accurately, a foreign key references a candidate/unique key that the DBMS permits as a referenced key.

Example:

~~~text
Customer
-----------
Customer_ID PK
Email UNIQUE
~~~

A child table may be able to reference:

`Email`

when the DBMS permits a UNIQUE constraint as the referenced key.

The exact requirements vary by database system.

---

# 32. Foreign Key Does Not Have to Reference a Primary Key

Example concept:

~~~text
CUSTOMER
-----------
Customer_ID PRIMARY KEY
Email UNIQUE
~~~

Child:

~~~text
SUBSCRIPTION
-----------
Email FOREIGN KEY
~~~

If the DBMS allows referencing the unique key:

~~~text
Subscription.Email
→ Customer.Email
~~~

The important requirement is that the referenced columns form an appropriate candidate/unique key according to the DBMS.

---

# 33. Foreign Key and Data Type

The foreign-key columns should be compatible with the referenced columns.

Example:

Parent:

~~~sql
Department_ID INT PRIMARY KEY
~~~

Child:

~~~sql
Department_ID INT
~~~

Good.

Do not casually use incompatible types.

The exact compatibility requirements depend on the DBMS.

---

# 34. Foreign Key Column Name

The foreign key does not have to have the same column name as the referenced key.

Example:

Parent:

~~~text
Department
-----------
Department_ID
~~~

Child:

~~~text
Employee
-----------
Dept_ID
~~~

Possible relationship:

~~~text
Employee.Dept_ID
→ Department.Department_ID
~~~

The names can differ.

What matters is the defined reference.

---

# 35. Foreign Key and JOIN

Foreign keys are commonly used in joins.

Example:

~~~sql
SELECT
    e.Employee_ID,
    e.Employee_Name,
    d.Department_Name
FROM Employee e
JOIN Department d
    ON e.Department_ID = d.Department_ID;
~~~

The relationship:

~~~text
Employee.Department_ID
=
Department.Department_ID
~~~

allows the tables to be combined logically.

---

# 36. Foreign Key Does Not Automatically Create a JOIN

Important distinction:

A foreign key defines a relationship and integrity constraint.

A `JOIN` is a query operation.

Therefore:

~~~text
Foreign Key
→ Defines/Enforces relationship

JOIN
→ Retrieves combined data
~~~

One does not automatically execute the other.

---

# 37. Foreign Key and Indexing

A foreign-key column is often a good candidate for an index, especially when it is frequently used in:

- Joins
- Parent-row lookups
- Updates
- Deletes

However:

> [!warning]
> A foreign key does not universally imply that an index is automatically created on the child column.

Index behavior depends on the DBMS.

---

# 38. Why Index Foreign Keys?

Suppose:

~~~text
Department
1
↓
100,000 Employees
~~~

A query:

~~~sql
SELECT *
FROM Employee
WHERE Department_ID = 10;
~~~

can benefit from an index on:

`Employee.Department_ID`

Likewise, parent deletes/updates may need to locate matching child rows efficiently.

---

# 39. Foreign Key and Performance

Foreign keys provide data integrity, but they also create additional constraint-checking work.

When inserting a child row, the database may need to verify that the parent key exists.

Example:

~~~text
INSERT Employee
Department_ID = 10
        ↓
Check Department 10
        ↓
Exists?
        ↓
YES → Allow
NO  → Reject
~~~

Therefore, foreign keys are primarily an integrity feature, not a performance feature.

---

# 40. Real-Time Example — Banking

Tables:

~~~text
CUSTOMER
-----------
Customer_ID PK
Name

ACCOUNT
-----------
Account_ID PK
Customer_ID FK
Balance
~~~

Relationship:

~~~text
Customer
1:N
Account
~~~

One customer may own multiple accounts under the business rules.

The foreign key:

`Account.Customer_ID`

connects the account to its owner.

---

# 41. Real-Time Example — E-Commerce

Tables:

~~~text
CUSTOMER
-----------
Customer_ID PK

ORDER
-----------
Order_ID PK
Customer_ID FK

PRODUCT
-----------
Product_ID PK

ORDER_ITEM
-----------
Order_ID FK
Product_ID FK
Quantity
Price
~~~

Relationships:

~~~text
Customer
1:N
Order
```

and:

~~~text
Order
1:N
Order_Item
```

and:

~~~text
Product
1:N
Order_Item
~~~

The original:

`Order M:N Product`

is represented through:

`Order_Item`

---

# 42. Real-Time Example — Social Media

Consider:

~~~text
USER
-----------
User_ID PK

POST
-----------
Post_ID PK
User_ID FK
```

Relationship:

~~~text
User
1:N
Post
~~~

One user can create many posts.

The foreign key:

`Post.User_ID`

identifies the user who owns the post.

---

# 43. Real-Time Example — Food Delivery

Tables:

~~~text
CUSTOMER
RESTAURANT
ORDER
DELIVERY_PARTNER
```

Possible relationships:

~~~text
Customer
1:N
Order

Restaurant
1:N
Order

Delivery_Partner
1:N
Order
~~~

Then:

~~~text
Order.Customer_ID
→ Customer.Customer_ID

Order.Restaurant_ID
→ Restaurant.Restaurant_ID

Order.Delivery_Partner_ID
→ Delivery_Partner.Delivery_Partner_ID
~~~

One table can therefore contain multiple foreign keys.

---

# 44. Multiple Foreign Keys in One Table

Example:

~~~sql
CREATE TABLE Order_Table (
    Order_ID INT PRIMARY KEY,
    Customer_ID INT,
    Restaurant_ID INT,
    Delivery_Partner_ID INT,

    FOREIGN KEY (Customer_ID)
        REFERENCES Customer(Customer_ID),

    FOREIGN KEY (Restaurant_ID)
        REFERENCES Restaurant(Restaurant_ID),

    FOREIGN KEY (Delivery_Partner_ID)
        REFERENCES Delivery_Partner(Delivery_Partner_ID)
);
~~~

Here:

`Order_Table`

contains three foreign keys.

This is perfectly valid.

---

# 45. Foreign Key to the Same Table

A foreign key can reference the same table.

This is called a:

**Self-Referencing / Recursive Foreign Key**

Example:

~~~text
EMPLOYEE
-----------
Employee_ID PK
Manager_ID FK
~~~

where:

`Manager_ID`

references:

`Employee_ID`

---

# 46. Self-Referencing Foreign Key Example

~~~sql
CREATE TABLE Employee (
    Employee_ID INT PRIMARY KEY,
    Employee_Name VARCHAR(100),
    Manager_ID INT,

    FOREIGN KEY (Manager_ID)
        REFERENCES Employee(Employee_ID)
);
~~~

Conceptually:

~~~text
Employee
   |
   | Manager_ID
   ↓
Employee
```

This represents:

~~~text
Employee
→ reports to
→ another Employee
~~~

---

# 47. Real-Time Example — Organization Hierarchy

| Employee_ID | Name | Manager_ID |
|---:|---|---:|
| 1 | CEO | NULL |
| 2 | Arun | 1 |
| 3 | Priya | 1 |
| 4 | Ravi | 2 |

Interpretation:

~~~text
CEO
├── Arun
│   └── Ravi
└── Priya
~~~

Here:

`Manager_ID`

is a foreign key referencing:

`Employee_ID`

in the same table.

---

# 48. Foreign Key and Weak Entity

Foreign keys are also important when implementing weak entities.

Conceptually:

~~~text
EMPLOYEE
   |
   |
DEPENDENT
~~~

Possible table:

~~~text
DEPENDENT
-----------
Employee_ID FK
Dependent_Name
...
~~~

If:

`Employee_ID + Dependent_Name`

is the primary key:

~~~text
PRIMARY KEY (Employee_ID, Dependent_Name)
```

then:

`Employee_ID`

is both:

`FK`

and part of:

`Composite PK`

This is a common advanced pattern.

---

# 49. Foreign Key as Part of Primary Key

A column can simultaneously be:

~~~text
Foreign Key
+
Primary Key
~~~

Example:

~~~text
EMPLOYEE
Employee_ID PK

EMPLOYEE_DETAILS
Employee_ID PK + FK
```

This is especially useful in:

~~~text
1:1 relationships
```

and:

~~~text
Dependent/weak-entity style designs
~~~

---

# 50. Foreign Key and Cascading Actions — Real-Time

Imagine:

~~~text
Customer
   ↓
Order
   ↓
Order_Item
~~~

If a customer is deleted:

### Option 1

Reject deletion.

~~~text
Customer has orders
→ Cannot delete
~~~

### Option 2

Cascade.

~~~text
Delete Customer
↓
Delete Orders
↓
Delete Order Items
~~~

### Option 3

Set references to NULL where appropriate.

The correct choice depends on business requirements.

---

# 51. Common Exam Pattern — Parent and Child

### Question

Table `Employee` contains `Department_ID`, which references `Department.Department_ID`.

Which is the parent table?

### Answer

`Department`

Why?

Because:

`Department.Department_ID`

is the referenced key.

---

# 52. Common Exam Pattern — FK Uniqueness

### Question

Can a foreign key contain duplicate values?

### Answer

Yes.

Example:

~~~text
Employee 101 → Department 1
Employee 102 → Department 1
Employee 103 → Department 1
~~~

All are valid.

---

# 53. Common Exam Pattern — FK NULL

### Question

Can a foreign key contain NULL?

### Answer

Yes, if the foreign-key column permits NULL.

NULL generally means the row has no specified reference.

---

# 54. Common Exam Pattern — FK Count

### Question

Can one table contain multiple foreign keys?

### Answer

Yes.

Example:

~~~text
Order
→ Customer_ID FK
→ Restaurant_ID FK
→ Delivery_Partner_ID FK
~~~

---

# 55. Common Exam Pattern — Self Reference

### Question

Can a foreign key reference the same table?

### Answer

Yes.

Example:

~~~text
Employee.Manager_ID
→ Employee.Employee_ID
~~~

This represents a recursive relationship.

---

# 56. Common Exam Pattern — M:N

### Question

How is M:N represented in a relational database?

### Answer

Usually using an intermediate/junction table containing foreign keys to both participating tables.

Example:

~~~text
Student
M:N
Course
```

becomes:

~~~text
Enrollment
Student_ID FK
Course_ID FK
~~~

---

# 57. Common Exam Pattern — Referential Integrity

### Question

Which integrity constraint prevents a child row from referencing a nonexistent parent?

### Answer

`Foreign Key / Referential Integrity`

---

# 58. Common Exam Pattern — CASCADE

### Question

What does `ON DELETE CASCADE` do?

### Answer

It allows deletion of matching child rows when the referenced parent row is deleted, according to the defined foreign-key action.

---

# 59. Common Exam Pattern — SET NULL

### Question

What does `ON DELETE SET NULL` do?

### Answer

It changes matching child foreign-key values to NULL when the referenced parent is deleted, provided the column can contain NULL.

---

# 60. Common Exam Pattern — FK Location

### Question

For a `1:N` relationship, where is the foreign key normally placed?

### Answer

On the:

**N-side**

Example:

~~~text
Department
1
|
N
Employee

Employee.Department_ID
→ FK
~~~

---

# 61. Foreign Key Recognition Tricks

> [!tip]
> **Pattern 1**
>
> "References another table"
>
> → Foreign Key

> [!tip]
> **Pattern 2**
>
> "Maintains relationship between tables"
>
> → Foreign Key

> [!tip]
> **Pattern 3**
>
> "Prevents invalid parent reference"
>
> → Referential Integrity / Foreign Key

> [!tip]
> **Pattern 4**
>
> "1:N relationship"
>
> → FK generally on N-side

> [!tip]
> **Pattern 5**
>
> "M:N relationship"
>
> → Junction table + two FKs

> [!tip]
> **Pattern 6**
>
> "Employee reports to Employee"
>
> → Self-referencing FK

---

# 62. Fast DBMS Key Recognition

> [!important]
> Use this mental mapping:

~~~text
"Identifies row"
→ PRIMARY KEY

"Minimal unique identifier"
→ CANDIDATE KEY

"Any unique attribute set"
→ SUPER KEY

"Unused candidate key"
→ ALTERNATE KEY

"References another table"
→ FOREIGN KEY

"Multiple columns together"
→ COMPOSITE KEY
~~~

---

# 63. Advanced Interview Question

## Q1. What is a foreign key?

### Strong Answer

> A foreign key is a column or set of columns in a relation that references a candidate/unique key of another relation or an appropriate key in the same relation. It is used to represent relationships and enforce referential integrity.

---

# 64. Interview Question

## Q2. Is a foreign key unique?

### Answer

No.

Multiple child rows can contain the same foreign-key value.

Example:

~~~text
Department_ID = 1
```

may appear in hundreds of Employee rows.

---

# 65. Interview Question

## Q3. Can a foreign key be NULL?

### Answer

Yes, if the foreign-key column allows NULL.

NULL means that no parent reference is specified for that row.

---

# 66. Interview Question

## Q4. Can a foreign key reference a unique key instead of a primary key?

### Answer

Yes, in systems that permit referencing a suitable UNIQUE/candidate key.

The referenced columns must satisfy the DBMS's requirements for a referenced key.

---

# 67. Interview Question

## Q5. Can a foreign key reference the same table?

### Answer

Yes.

Example:

~~~text
Employee.Manager_ID
→ Employee.Employee_ID
~~~

This is called a self-referencing or recursive foreign key.

---

# 68. Interview Question

## Q6. Can a table have multiple foreign keys?

### Answer

Yes.

A table can have multiple foreign-key constraints referencing different tables or even different keys.

---

# 69. Interview Question

## Q7. Can a foreign key be part of a primary key?

### Answer

Yes.

This occurs commonly in:

- Associative entities
- Weak entities
- Shared-primary-key designs

---

# 70. Interview Question

## Q8. What is referential integrity?

### Strong Answer

> Referential integrity ensures that foreign-key references remain valid according to the database constraints and configured actions, preventing inconsistent references between related tables.

---

# 71. Interview Question

## Q9. What happens if we delete a referenced parent row?

### Answer

It depends on the foreign-key action.

Possible behavior:

~~~text
RESTRICT / NO ACTION
→ Reject deletion

CASCADE
→ Delete matching children

SET NULL
→ Set child FK to NULL

SET DEFAULT
→ Set child FK to default where supported
~~~

---

# 72. Interview Question

## Q10. What is a cascading delete?

### Answer

> A cascading delete automatically deletes matching child rows when the referenced parent row is deleted, according to an `ON DELETE CASCADE` foreign-key rule.

---

# 73. Interview Question

## Q11. What is the difference between CASCADE and SET NULL?

### Answer

~~~text
CASCADE
→ Child row is deleted

SET NULL
→ Child row remains
→ FK becomes NULL
~~~

---

# 74. Advanced Interview Question

## Q12. Why is the foreign key usually placed on the N-side of a 1:N relationship?

### Answer

Because each child row needs to identify its single parent, while many child rows can reference the same parent.

Example:

~~~text
Department
1
|
N
Employee
~~~

Therefore:

~~~text
Employee.Department_ID
→ FK
~~~

---

# 75. Advanced Interview Question

## Q13. Why do we need a junction table for M:N?

### Answer

A relational table represents relationships using rows and keys. A junction table decomposes the M:N relationship into two 1:N relationships and stores the foreign keys of both entities.

---

# 76. Advanced Interview Question

## Q14. Does adding a foreign key automatically create an index?

### Answer

Not universally.

Some DBMSs may automatically index certain keys, but a foreign-key constraint itself does not universally guarantee an index on the child column.

---

# 77. Advanced Interview Question

## Q15. Does a foreign key improve performance?

### Answer

Its primary purpose is data integrity, not performance.

A foreign key can introduce constraint-checking work, while an appropriate index on the foreign-key column can improve joins and parent-row modification checks.

---

# 78. Advanced Interview Question

## Q16. What is the difference between foreign key and JOIN?

### Answer

~~~text
Foreign Key
→ Schema-level relationship and integrity constraint

JOIN
→ Query operation that combines rows
~~~

A foreign key does not automatically perform a join.

---

# 79. Advanced Interview Question

## Q17. What is a self-referencing foreign key?

### Answer

A foreign key that references a key within the same table.

Example:

~~~text
Employee.Manager_ID
→ Employee.Employee_ID
~~~

It is commonly used for hierarchical data.

---

# 80. Advanced Interview Question

## Q18. Can a foreign key reference a composite key?

### Answer

Yes.

If the parent has:

~~~text
PRIMARY KEY (A, B)
~~~

the child can use:

~~~text
FOREIGN KEY (A, B)
REFERENCES Parent(A, B)
~~~

subject to the DBMS's referenced-key requirements.

---

# 81. Advanced Interview Question

## Q19. What happens if a child references a nonexistent parent?

### Answer

If the foreign-key constraint is enforced, the insert/update is rejected because it violates referential integrity.

---

# 82. Advanced Interview Question

## Q20. What is the difference between NULL and invalid FK?

### Answer

~~~text
NULL
→ No reference is specified
→ Can be valid if NULL is allowed

Invalid value
→ Claims to reference a parent that does not exist
→ Rejected under the FK constraint
~~~

---

# 83. Advanced Design Pattern — Customer and Order

Requirement:

> A customer can place many orders. Every order belongs to one customer.

Identify:

~~~text
CUSTOMER
1
|
N
ORDER
~~~

Implementation:

~~~text
CUSTOMER
-----------
Customer_ID PK

ORDER
-----------
Order_ID PK
Customer_ID FK
~~~

Recognition:

`1:N`

→ FK on N-side.

---

# 84. Advanced Design Pattern — Student and Course

Requirement:

> A student can enroll in many courses and each course can contain many students.

Identify:

~~~text
STUDENT
M:N
COURSE
~~~

Implementation:

~~~text
ENROLLMENT
-----------
Student_ID FK
Course_ID FK
~~~

Possible primary key:

~~~text
(Student_ID, Course_ID)
~~~

This is the standard M:N pattern.

---

# 85. Advanced Design Pattern — Employee Hierarchy

Requirement:

> An employee may report to another employee.

Entity:

~~~text
EMPLOYEE
~~~

Relationship:

~~~text
REPORTS_TO
~~~

Implementation:

~~~text
Employee_ID PK
Manager_ID FK
```

where:

`Manager_ID`

references:

`Employee_ID`

This is a self-referencing foreign key.

---

# 86. Advanced Design Pattern — Product and Category

Requirement:

> Each product belongs to one category. A category can contain many products.

~~~text
CATEGORY
1
|
N
PRODUCT
~~~

Implementation:

~~~text
CATEGORY
-----------
Category_ID PK

PRODUCT
-----------
Product_ID PK
Category_ID FK
~~~

Again:

`1:N → FK on N-side`

---

# 87. Advanced Design Pattern — Multiple Relationships

Suppose:

> An order is placed by a customer, shipped from a warehouse, and assigned to a delivery partner.

Then:

~~~text
ORDER
-----------
Order_ID PK
Customer_ID FK
Warehouse_ID FK
Delivery_Partner_ID FK
~~~

One table can therefore have several foreign keys.

The key insight:

> [!important]
> A foreign key represents one defined reference. A table may contain many such references.

---

# 88. Foreign Key and Data Consistency

Without foreign-key constraints:

~~~text
Customer
101

Order
999 → Customer_ID 5000
~~~

The database may contain an orphaned order.

With a foreign-key constraint:

~~~text
Order.Customer_ID
→ Customer.Customer_ID
~~~

the database can reject the invalid reference.

Thus:

`FK → Prevents orphan references`

---

# 89. Orphan Record

An **orphan record** is a child row whose referenced parent does not exist.

Example:

~~~text
Customer
---------
101
102
```

Order:

~~~text
Order_ID | Customer_ID
5001     | 999
~~~

Customer `999` does not exist.

Therefore:

`Order 5001`

is an orphan with respect to the intended relationship.

Foreign keys help prevent this.

---

# 90. Foreign Key and Data Lifecycle

When designing a database, ask:

~~~text
What happens when parent is deleted?
What happens when parent key changes?
What happens when child is deleted?
What happens when child is inserted?
~~~

These questions lead to:

~~~text
ON DELETE
ON UPDATE
Foreign Key Constraints
~~~

This is how professional database design handles lifecycle rules.

---

# 91. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking FK must be unique

Wrong.

A foreign key can repeat.

Example:

~~~text
1
1
1
2
2
3
~~~

is perfectly normal.

---

### Mistake 2 — Thinking FK cannot be NULL

Wrong.

A foreign key may be NULL if the column allows NULL and the relationship is optional.

---

### Mistake 3 — Thinking FK always references PK only

Oversimplified.

A foreign key can reference an appropriate candidate/unique key when supported by the DBMS.

---

### Mistake 4 — Putting FK on the 1-side

For a normal 1:N relationship, the FK is generally placed on the N-side.

~~~text
1:N
→ FK on N
~~~

---

### Mistake 5 — Confusing FK with JOIN

FK:

`Schema relationship`

JOIN:

`Query operation`

---

### Mistake 6 — Assuming FK automatically creates an index

Not universally true.

Check the DBMS.

---

### Mistake 7 — Using CASCADE everywhere

Cascading deletes can remove large amounts of related data.

Use them only when appropriate.

---

### Mistake 8 — Ignoring NULL semantics

NULL is not the same as:

`0`

`''`

or:

`Nonexistent Parent ID`

---

### Mistake 9 — Forgetting M:N transformation

Do not try to represent arbitrary M:N relationships using only one FK column in one of the two entity tables.

Use an associative/junction table.

---

### Mistake 10 — Ignoring business rules

The database structure should reflect the actual relationship.

Do not assume every relationship is 1:N.

---

# 92. Must-Master Patterns

> [!important] Must Master

1. Foreign key definition
2. Parent table
3. Child table
4. Referential integrity
5. Primary key vs foreign key
6. FK uniqueness
7. FK NULL
8. FK on N-side of 1:N
9. M:N junction table
10. Composite foreign key
11. Self-referencing foreign key
12. Multiple foreign keys
13. FK as part of primary key
14. Shared primary key
15. `ON DELETE CASCADE`
16. `ON DELETE SET NULL`
17. `RESTRICT / NO ACTION`
18. `ON UPDATE CASCADE`
19. Orphan records
20. Foreign key and indexing
21. Foreign key and joins
22. Foreign key and normalization
23. Foreign key and weak entities
24. Foreign key and candidate keys
25. Referential actions

---

# 93. Master Comparison

| Concept | Main Question |
|---|---|
| Primary Key | Who is this row? |
| Foreign Key | Which parent/key does this row reference? |
| Candidate Key | What minimal set can uniquely identify it? |
| Super Key | What set can uniquely identify it? |
| Alternate Key | Which candidate key was not selected? |
| Composite Key | Are multiple columns needed? |

---

# 94. Master Relationship Mapping

~~~text
1:1
→ FK on an appropriate side
→ UNIQUE may be needed

1:N
→ FK on N-side

M:N
→ Junction Table
→ Two FKs

Recursive
→ FK references same table

Weak Entity
→ Owner PK commonly becomes FK
→ May be part of weak entity PK
~~~

---

# 95. Foreign Key Decision Tree

> [!important]
> Use this during interviews:

~~~text
Does one table need to reference another?
          |
         YES
          ↓
Identify Parent Key
          ↓
Create FK in Child
          ↓
What is the relationship?
          |
     ┌────┼────┐
     ↓    ↓    ↓
    1:1  1:N  M:N
     |    |    |
     ↓    ↓    ↓
 FK +   FK on  Junction
 UNIQUE N-side  Table
              ↓
            Two FKs
~~~

---

# 96. Fast SQL Recognition

When you see:

~~~sql
FOREIGN KEY (Department_ID)
REFERENCES Department(Department_ID)
~~~

Immediately translate it mentally:

~~~text
Employee.Department_ID
        ↓
references
        ↓
Department.Department_ID
```

Therefore:

~~~text
Employee
→ Child

Department
→ Parent

Department_ID
→ FK in Employee

Department_ID
→ Referenced key in Department
~~~

---

# 97. One-Minute Revision

> [!summary] One-Minute Revision

~~~text
FOREIGN KEY
→ Column/set of columns that references a suitable key
  in another or the same table.

MAIN PURPOSE
→ Represent relationships
→ Enforce referential integrity

PARENT
→ Referenced table

CHILD
→ Table containing FK

PRIMARY KEY
→ Identity

FOREIGN KEY
→ Relationship

1:N
→ FK normally on N-side

M:N
→ Junction table
→ Two FKs

1:1
→ FK on suitable side
→ UNIQUE may be required

FK
→ Can repeat

FK
→ Can be NULL if allowed

FK
→ Does not automatically have to be unique

SELF-REFERENCE
→ FK references same table

COMPOSITE FK
→ Multiple columns reference a composite key

REFERENTIAL ACTIONS

CASCADE
→ Propagate change/delete

SET NULL
→ Set FK to NULL

SET DEFAULT
→ Set FK to default where supported

RESTRICT
→ Prevent operation

NO ACTION
→ Enforce according to DBMS rules

IMPORTANT DISTINCTIONS

PK
→ Unique identity

FK
→ Reference

PK
→ Entity Integrity

FK
→ Referential Integrity

JOIN
→ Query operation

FK
→ Schema constraint

M:N
→ Junction table

1:N
→ FK on N-side

MOST IMPORTANT INTERVIEW MEMORY

Parent owns referenced key.
Child stores foreign key.
~~~

# 98. Golden Memory Trick

**Foreign Key = the child table's reference that tells the database which parent row it belongs to.**

# 99. One-Line Recognition

**Whenever one table contains a column that references a key in another table, think Foreign Key and Referential Integrity.**