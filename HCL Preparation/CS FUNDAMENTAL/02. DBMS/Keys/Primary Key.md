---
type: concept
subject: dbms
topic: "Primary Key"
parent: "Keys"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - keys
  - primary-key
  - candidate-key
  - super-key
  - alternate-key
  - composite-key
  - constraints
  - relational-model
  - sql
  - database-design
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
  - "[[Candidate Key]]"
  - "[[Super Key]]"
  - "[[Foreign Key]]"
  - "[[Alternate Key]]"
  - "[[Composite Key]]"
  - "[[Constraints]]"
  - "[[ER Model]]"
  - "[[Normalization]]"
---

# Primary Key

## 1. Core Concept

> [!summary]
> A **Primary Key** is a column or set of columns that uniquely identifies every row in a relational table.

The simplest way to remember it:

**Primary Key = Unique Identity of a Row**

Example:

| Student_ID | Name | Department |
|---:|---|---|
| 101 | Arun | CSE |
| 102 | Priya | ECE |
| 103 | Ravi | CSE |

Here:

`Student_ID`

can uniquely identify every student.

Therefore:

`Student_ID → Primary Key`

The primary key answers:

> "Which value can I use to identify exactly one row?"

---

# 2. Basic Meaning

Suppose we have:

| Employee_ID | Name | Salary |
|---:|---|---:|
| 101 | Arun | 50000 |
| 102 | Priya | 60000 |
| 103 | Ravi | 55000 |

If we ask:

> Find employee 102.

The database can directly identify:

`Employee_ID = 102`

because it is unique.

A primary key therefore provides an identity for each tuple/row.

In relational terminology:

`Tuple = Row`

So:

`Primary Key → Uniquely identifies a tuple`

---

# 3. Main Properties of a Primary Key

A primary key has two fundamental properties:

1. **Uniqueness**
2. **NOT NULL**

Therefore:

`Primary Key → Unique + NOT NULL`

Example:

| Student_ID | Name |
|---:|---|
| 101 | Arun |
| 102 | Priya |
| 103 | Ravi |

Valid.

But:

| Student_ID | Name |
|---:|---|
| 101 | Arun |
| 101 | Priya |

Invalid because the primary key is duplicated.

And:

| Student_ID | Name |
|---|---|
| 101 | Arun |
| NULL | Priya |

Invalid because a primary-key value cannot be NULL.

---

# 4. Primary Key as a Constraint

A primary key is not merely a column name.

It represents a database constraint.

Example:

`Student_ID`

is a candidate key attribute.

When we designate it as the primary key, the database enforces the primary-key rules.

Conceptually:

`PRIMARY KEY`
→ Uniqueness
→ Non-nullability
→ Row identification

---

# 5. SQL Syntax

A primary key can be declared while creating a table.

Example:

    CREATE TABLE Student (
        Student_ID INT PRIMARY KEY,
        Name VARCHAR(100),
        Department VARCHAR(50)
    );

Here:

`Student_ID`

is the primary key.

---

# 6. Primary Key Example

Consider:

    CREATE TABLE Employee (
        Employee_ID INT PRIMARY KEY,
        Name VARCHAR(100),
        Salary DECIMAL(10,2)
    );

Possible data:

| Employee_ID | Name | Salary |
|---:|---|---:|
| 101 | Arun | 50000 |
| 102 | Priya | 60000 |
| 103 | Ravi | 55000 |

The following is invalid:

    INSERT INTO Employee
    VALUES (101, 'Kumar', 45000);

Why?

Because:

`Employee_ID = 101`

already exists.

Therefore:

> [!warning]
> A primary key cannot contain duplicate values.

---

# 7. Primary Key and NULL

Consider:

    INSERT INTO Employee
    VALUES (NULL, 'Kumar', 45000);

This is invalid because:

`Employee_ID`

is the primary key.

Primary key:

`→ NOT NULL`

Why?

Because a row must have a definite identity.

If the identity were NULL, the database could not use it as a valid unique identifier.

---

# 8. Why Does a Primary Key Need NOT NULL?

Suppose:

| Student_ID | Name |
|---|---|
| 101 | Arun |
| NULL | Priya |

Ask:

> What is Priya's unique identity?

There is no actual identifier.

Therefore, a primary key cannot permit NULL.

Memory:

> [!tip]
> **Primary Key = "Every row must have an identity."**

---

# 9. Primary Key vs UNIQUE

This is one of the most important DBMS interview questions.

Both can enforce uniqueness, but they are not identical.

| Property | PRIMARY KEY | UNIQUE |
|---|---|---|
| Duplicate values | Not allowed | Not allowed |
| NULL | Not allowed | DBMS-dependent NULL behavior |
| Number per table | At most one primary-key constraint | Multiple UNIQUE constraints possible |
| Main purpose | Row identity | Alternate uniqueness rule |
| Foreign-key target | Commonly used | Can be referenced when uniquely constrained, depending on DBMS |

The safest interview statement:

> A table has at most one primary key, while it can have multiple UNIQUE constraints.

---

# 10. Primary Key vs Candidate Key

A **candidate key** is a minimal attribute set that can uniquely identify rows.

A table may have multiple candidate keys.

One candidate key is selected as:

`PRIMARY KEY`

The remaining candidate keys become:

`ALTERNATE KEYS`

Example:

| Student_ID | Email | Aadhaar_No | Name |
|---|---|---|---|
| 101 | a@gmail.com | X123 | Arun |
| 102 | p@gmail.com | X456 | Priya |

Suppose:

`Student_ID`

is unique.

`Email`

is also unique.

`Aadhaar_No`

is also unique.

Then:

`Candidate Keys = {Student_ID, Email, Aadhaar_No}`

If we choose:

`Student_ID`

as the primary key:

`Primary Key = Student_ID`

The others are alternate candidate keys:

`Email`
`Aadhaar_No`

---

# 11. Candidate Key → Primary Key Relationship

This is extremely important.

Think:

    Super Keys
        ↓
    Candidate Keys
        ↓
    Choose ONE
        ↓
    Primary Key

More precisely:

`Candidate Key ⊂ Super Key`

and:

`Primary Key = Selected Candidate Key`

The primary key is therefore not a completely different type of key.

It is a **chosen candidate key**.

---

# 12. Super Key → Candidate Key → Primary Key

Example table:

| Student_ID | Email | Name |
|---:|---|---|
| 101 | a@gmail.com | Arun |
| 102 | p@gmail.com | Priya |

Suppose both `Student_ID` and `Email` are unique.

Possible super keys include:

`{Student_ID}`

`{Email}`

`{Student_ID, Name}`

`{Email, Name}`

`{Student_ID, Email}`

Candidate keys:

`{Student_ID}`

`{Email}`

Why?

Because candidate keys must be **minimal**.

Choose:

`{Student_ID}`

as primary key.

Then:

`Student_ID → Primary Key`

`Email → Alternate Key`

---

# 13. Minimality

This is one of the most important concepts behind candidate keys.

Suppose:

`{Student_ID, Name}`

uniquely identifies a student.

It is a super key.

But if:

`Student_ID`

alone is enough, then:

`{Student_ID, Name}`

is not minimal.

Therefore:

`{Student_ID, Name}`

is not a candidate key.

Memory:

> [!important]
> **Candidate Key = Super Key + Minimality**

---

# 14. Primary Key Selection

If a table has multiple candidate keys, how should we select the primary key?

Common practical considerations:

- Uniqueness
- Stability
- Minimal size
- Non-nullability
- Simplicity
- Rarely changing value
- Easy indexing
- Appropriate semantics

Example:

Suppose:

`Student_ID`

and:

`Email`

are both candidate keys.

A system may choose:

`Student_ID`

because it is a stable internal identifier.

Email addresses can change.

Therefore:

`Student_ID → Primary Key`

`Email → Alternate Key`

---

# 15. Natural Key

A **natural key** is a key derived from real-world meaningful data.

Examples:

`Email`

`Passport_Number`

`ISBN`

`National_ID`

depending on the system requirements.

Example:

    Student(
        Email PRIMARY KEY,
        Name
    );

Here:

`Email`

has real-world meaning.

---

# 16. Surrogate Key

A **surrogate key** is an artificial identifier created specifically for database identification.

Examples:

`Student_ID`

`Employee_ID`

`Order_ID`

For example:

| Student_ID | Name |
|---:|---|
| 1001 | Arun |
| 1002 | Priya |

`Student_ID`

may have no real-world meaning.

It exists primarily to identify rows.

---

# 17. Natural Key vs Surrogate Key

| Feature | Natural Key | Surrogate Key |
|---|---|---|
| Meaning | Has real-world meaning | Artificial identifier |
| Example | Email | Student_ID |
| Stability | May change | Usually stable |
| Size | Can be larger | Often compact |
| Common use | Business identification | Database identity |

Important:

> [!tip]
> In real database design, surrogate keys are often preferred when natural identifiers are large, mutable, or complicated.

---

# 18. Integer Primary Keys

A common primary-key design is:

`INT`

Example:

    CREATE TABLE Student (
        Student_ID INT PRIMARY KEY,
        Name VARCHAR(100)
    );

Advantages:

- Compact
- Easy to index
- Easy to compare
- Efficient joins
- Simple to reference

But integer keys are not automatically best in every system.

---

# 19. String Primary Keys

A string can also be used as a primary key.

Example:

    CREATE TABLE Country (
        Country_Code CHAR(2) PRIMARY KEY,
        Country_Name VARCHAR(100)
    );

Here:

`Country_Code`

could be:

`IN`

`US`

`UK`

The important requirement is uniqueness and non-nullability.

---

# 20. UUID as Primary Key

Modern distributed systems sometimes use UUIDs.

Example concept:

`550e8400-e29b-41d4-a716-446655440000`

A UUID is useful when identifiers need to be generated independently across distributed services.

Advantages:

- Globally unique identifiers
- Useful in distributed systems
- No central sequence required

Potential disadvantages:

- Larger than integer IDs
- More storage
- Potential indexing considerations
- Less human-readable

---

# 21. Primary Key and Indexing

A primary key is commonly backed by an index in relational database systems.

This allows efficient lookup.

Example:

    SELECT *
    FROM Student
    WHERE Student_ID = 101;

Because `Student_ID` is a primary key, the database can efficiently locate the corresponding row using its index structure.

Important:

> [!warning]
> Do not say "primary key always means clustered index" as a universal DBMS rule.

Index implementation depends on the database system.

---

# 22. Primary Key and Foreign Key

The primary key of one table is frequently referenced by a foreign key in another table.

Example:

    DEPARTMENT
    ----------
    Department_ID PRIMARY KEY

    EMPLOYEE
    ----------
    Employee_ID PRIMARY KEY
    Department_ID FOREIGN KEY

Relationship:

`Department`

`1:N`

`Employee`

The foreign key:

`Employee.Department_ID`

references:

`Department.Department_ID`

---

# 23. Real-Time Example — College

Suppose:

`Department`

| Department_ID | Department_Name |
|---:|---|
| 1 | CSE |
| 2 | ECE |

Primary key:

`Department_ID`

Student table:

| Student_ID | Name | Department_ID |
|---:|---|---:|
| 101 | Arun | 1 |
| 102 | Priya | 2 |
| 103 | Ravi | 1 |

Here:

`Student_ID → Primary Key`

`Department_ID → Foreign Key`

---

# 24. Primary Key and Referential Integrity

Suppose:

`Department`

contains:

`Department_ID = 1`

Then:

`Student.Department_ID`

can reference:

`1`

If a student tries to reference:

`999`

and no department 999 exists, the foreign-key constraint can reject the operation.

Therefore:

`Primary Key`

often acts as the referenced identity.

`Foreign Key`

maintains the relationship.

---

# 25. Composite Primary Key

A primary key does not have to contain only one column.

It can contain multiple columns.

This is called a:

`Composite Primary Key`

Example:

`ENROLLMENT`

| Student_ID | Course_ID | Grade |
|---:|---:|---|
| 101 | 501 | A |
| 101 | 502 | B |
| 102 | 501 | A |

Possible primary key:

`(Student_ID, Course_ID)`

Together they identify an enrollment.

---

# 26. Why Composite Key?

Suppose:

`Student_ID`

is not unique in the Enrollment table.

Student 101 can enroll in multiple courses.

Similarly:

`Course_ID`

is not unique because many students can take the same course.

But:

`Student_ID + Course_ID`

can uniquely identify an enrollment.

Therefore:

`(Student_ID, Course_ID) → Primary Key`

---

# 27. Composite Primary Key Example

    CREATE TABLE Enrollment (
        Student_ID INT,
        Course_ID INT,
        Grade CHAR(2),
        PRIMARY KEY (Student_ID, Course_ID)
    );

Here:

`Student_ID`

alone:

`→ Not necessarily unique`

`Course_ID`

alone:

`→ Not necessarily unique`

Together:

`(Student_ID, Course_ID)`

`→ Unique`

---

# 28. Composite Key Recognition

> [!important]
> If the question says:
>
> "Neither column is unique individually, but their combination uniquely identifies each row"
>
> immediately think:
>
> **Composite Key**

Example:

`Student_ID + Course_ID`

---

# 29. Order of Columns in Composite Key

Suppose:

`PRIMARY KEY (Student_ID, Course_ID)`

The pair identifies the row.

Conceptually:

`(101, 501)`

is different from:

`(101, 502)`

and:

`(102, 501)`

The combination must be unique.

---

# 30. Composite Key and Partial Dependency

Composite keys become particularly important in normalization.

Suppose:

`Enrollment(Student_ID, Course_ID, Student_Name, Course_Name, Grade)`

Primary key:

`(Student_ID, Course_ID)`

Dependencies:

`Student_ID → Student_Name`

`Course_ID → Course_Name`

`Student_ID, Course_ID → Grade`

This contains partial dependencies.

That becomes important when studying:

`2NF`

Therefore:

> [!tip]
> **Composite Key → Think about 2NF and Partial Dependency.**

---

# 31. Primary Key and Entity Integrity

The **Entity Integrity Rule** states that the primary key of a relation cannot contain NULL values.

Therefore:

`Primary Key`

must provide a valid identity for every row.

Memory:

`Entity Integrity → Primary Key cannot be NULL`

This is a high-frequency DBMS interview point.

---

# 32. Entity Integrity vs Referential Integrity

Do not confuse these.

### Entity Integrity

Concerned with:

`Primary Key`

Rule:

`Primary Key ≠ NULL`

### Referential Integrity

Concerned with:

`Foreign Key`

Rule:

`Foreign Key value must reference a valid parent key`

unless NULL is allowed by the schema and DBMS rules.

Memory:

> [!tip]
> **Entity → Primary Key**
>
> **Reference → Foreign Key**

---

# 33. Primary Key and Duplicate Rows

Suppose:

| ID | Name |
|---:|---|
| 1 | Arun |
| 2 | Priya |

Trying to insert:

| ID | Name |
|---:|---|
| 1 | Ravi |

causes a primary-key violation.

Why?

Because:

`ID = 1`

already exists.

Therefore:

`PRIMARY KEY → Prevents duplicate key values`

---

# 34. Primary Key and NULL

Suppose:

| ID | Name |
|---|---|
| 1 | Arun |
| NULL | Priya |

This violates the primary-key rule.

Therefore:

`PRIMARY KEY → NOT NULL`

This is different from the general behavior of a `UNIQUE` constraint, whose NULL semantics can vary by DBMS.

---

# 35. Can a Table Have Multiple Primary Keys?

No.

A table can have:

`At most one PRIMARY KEY constraint`

But that primary key can contain multiple columns.

Example:

`PRIMARY KEY (A, B)`

is one primary key constraint.

Therefore:

> [!important]
> **One table → At most one Primary Key**
>
> **One Primary Key → One or more columns**

---

# 36. Can a Table Have Multiple Candidate Keys?

Yes.

Example:

`Student_ID`

`Email`

`Phone_Number`

may all uniquely identify a student.

Then:

`Candidate Keys = 3`

But only one candidate key is selected as:

`Primary Key`

The rest are:

`Alternate Keys`

---

# 37. Can a Primary Key Be a Foreign Key?

Yes.

A column can participate in both constraints.

This is especially common in certain 1:1 or identifying relationships.

Example:

`Employee`

| Employee_ID |
|---:|
| 101 |
| 102 |

`Employee_Details`

| Employee_ID | Address |
|---:|---|
| 101 | Chennai |
| 102 | Trichy |

If:

`Employee_Details.Employee_ID`

is both:

`PRIMARY KEY`

and:

`FOREIGN KEY`

referencing `Employee.Employee_ID`, then it creates a one-to-one style relationship under appropriate constraints.

---

# 38. Shared Primary Key Pattern

Example:

    CREATE TABLE Employee (
        Employee_ID INT PRIMARY KEY,
        Name VARCHAR(100)
    );

    CREATE TABLE EmployeeDetails (
        Employee_ID INT PRIMARY KEY,
        Address VARCHAR(200),
        FOREIGN KEY (Employee_ID)
            REFERENCES Employee(Employee_ID)
    );

Here:

`EmployeeDetails.Employee_ID`

is:

`PRIMARY KEY`

and:

`FOREIGN KEY`

This is called a shared-primary-key pattern.

---

# 39. Can a Primary Key Change?

Technically, yes, depending on the DBMS and constraints.

But from a database-design perspective:

> [!tip]
> Prefer a primary key that is stable and rarely changes.

Why?

Because other tables may reference it through foreign keys.

If the primary key changes, related references may also need to change.

Therefore:

`Stable Key → Easier Maintenance`

---

# 40. Primary Key Selection — Interview Thinking

Suppose:

`Employee_ID`

and:

`Email`

are both unique.

Which should be primary?

Prefer the key that is:

- Stable
- Compact
- Simple
- Non-null
- Rarely changed
- Suitable for relationships
- Appropriate for system design

Often:

`Employee_ID`

is better than:

`Email`

because an employee's email may change.

---

# 41. Primary Key vs Employee Name

Suppose:

| Employee_ID | Name |
|---:|---|
| 101 | Arun |
| 102 | Arun |

Can `Name` be the primary key?

No.

Because:

`Name`

is not unique.

This is why real-world attributes should not automatically be considered keys.

---

# 42. Primary Key vs Phone Number

Suppose a system requires phone numbers to be unique.

Then phone number could technically serve as a candidate key.

But if phone numbers can change or may be reassigned, a stable surrogate key may be preferable.

Therefore:

> [!important]
> **Uniqueness alone is not the only practical consideration when selecting a primary key.**

---

# 43. Primary Key vs Email

Suppose:

`Email`

is unique today.

Can it be a candidate key?

Yes, if the business rules guarantee uniqueness and non-nullability.

Can it be a primary key?

Yes.

But whether it is the best primary key depends on system requirements.

---

# 44. Natural Key vs Surrogate Key — Interview Pattern

Question:

> Which is better, natural key or surrogate key?

Best answer:

> Neither is universally better. The choice depends on the application's requirements. Natural keys carry business meaning but may change or be large, while surrogate keys are usually stable and simple but have no business meaning.

This is stronger than saying:

"Surrogate keys are always better."

---

# 45. Primary Key and Business Meaning

A primary key does not necessarily need business meaning.

Example:

`Order_ID = 100023`

The number may simply identify the order internally.

This is completely valid.

The purpose of a primary key is:

`Identity`

not necessarily:

`Business Meaning`

---

# 46. Primary Key and NULL — Important SQL Trick

Suppose:

    CREATE TABLE Student (
        Student_ID INT PRIMARY KEY,
        Name VARCHAR(100)
    );

The following is invalid:

    INSERT INTO Student
    VALUES (NULL, 'Arun');

Because:

`Student_ID`

is a primary key.

But:

    CREATE TABLE Student (
        Student_ID INT,
        Name VARCHAR(100),
        UNIQUE(Student_ID)
    );

has different semantics because `UNIQUE` and NULL behavior are DBMS-specific.

Therefore:

> [!warning]
> Never say "UNIQUE and PRIMARY KEY are exactly the same." They are not.

---

# 47. Primary Key and Auto Increment

Many systems provide automatic ID generation.

Example syntax varies by DBMS.

Conceptually:

    Student_ID
    → Automatically Generated
    → PRIMARY KEY

Possible values:

`1`

`2`

`3`

`4`

This is a common surrogate-key strategy.

But automatic generation is **not part of the definition of a primary key**.

A primary key can be manually assigned as well.

---

# 48. Primary Key vs Auto Increment

Very important distinction:

`PRIMARY KEY`

means:

`Unique + NOT NULL`

`AUTO_INCREMENT / IDENTITY / SEQUENCE`

means:

`How values are generated`

Therefore:

`Primary Key ≠ Auto Increment`

They are separate concepts.

---

# 49. Real-Time Example — Banking

Consider:

`ACCOUNT`

| Account_ID | Customer_Name | Balance |
|---:|---|---:|
| 10001 | Arun | 50000 |
| 10002 | Priya | 70000 |

Primary key:

`Account_ID`

Why not:

`Customer_Name`?

Because multiple customers can have the same name.

Why not:

`Balance`?

Because balances are not unique.

Therefore:

`Account_ID → Primary Key`

---

# 50. Real-Time Example — E-Commerce

`ORDER`

| Order_ID | Customer_ID | Amount |
|---:|---:|---:|
| 5001 | 101 | 1500 |
| 5002 | 101 | 2500 |

Primary key:

`Order_ID`

Foreign key:

`Customer_ID`

Relationship:

`Customer 1:N Order`

This is a classic real-world key pattern.

---

# 51. Real-Time Example — Hospital

`PATIENT`

| Patient_ID | Name | DOB |
|---:|---|---|
| 101 | Arun | 2003-01-01 |
| 102 | Arun | 2004-05-10 |

Primary key:

`Patient_ID`

Not:

`Name`

because names can repeat.

Not necessarily:

`DOB`

because dates of birth may repeat.

---

# 52. Real-Time Example — University Enrollment

`ENROLLMENT`

| Student_ID | Course_ID | Semester | Grade |
|---:|---:|---|---|
| 101 | 501 | Sem 5 | A |
| 101 | 502 | Sem 5 | B |
| 102 | 501 | Sem 5 | A |

Possible composite primary key:

`(Student_ID, Course_ID)`

But if a student can enroll in the same course again in a later semester, then the key may need to include semester or use a separate enrollment identifier, depending on the business rules.

This is an important real-world modeling insight.

---

# 53. Advanced Pattern — Repeated Enrollment

Suppose:

`Student 101`

takes:

`Course 501`

in:

`2026`

and again in:

`2027`

Then:

`(Student_ID, Course_ID)`

is no longer unique across history.

Possible key:

`(Student_ID, Course_ID, Semester)`

or:

`Enrollment_ID`

depending on the requirements.

This teaches an important lesson:

> [!important]
> **The correct primary key depends on what one row represents.**

---

# 54. Grain of a Table

A high-level database-design concept is **grain**.

Grain means:

> What does one row represent?

Example:

`Enrollment`

One row represents:

`One Student + One Course + One Enrollment Event`

Therefore, the primary key must uniquely identify that unit.

This is why:

`Student_ID + Course_ID`

may work in one design, while:

`Student_ID + Course_ID + Semester`

may be required in another.

---

# 55. Primary Key and Table Grain

Before choosing a primary key, ask:

> [!important]
> **What exactly does one row represent?**

Example:

`ORDER_ITEM`

One row represents:

`One Product inside One Order`

Therefore:

`Order_ID + Product_ID`

may identify the row.

Example:

`PAYMENT`

One row may represent:

`One Payment Transaction`

Therefore:

`Payment_ID`

may be sufficient.

This is a powerful professional database-design habit.

---

# 56. Primary Key and Functional Dependency

Suppose:

`Student_ID`

is the primary key.

Then:

`Student_ID → Student_Name`

`Student_ID → Email`

`Student_ID → Department_ID`

In other words:

> The primary key functionally determines the non-key attributes of the row.

This becomes extremely important in normalization.

---

# 57. Primary Key and Functional Dependency Example

Relation:

`STUDENT(Student_ID, Name, Email, Department_ID)`

Primary key:

`Student_ID`

Functional dependencies:

`Student_ID → Name`

`Student_ID → Email`

`Student_ID → Department_ID`

This indicates that each Student_ID identifies exactly one student's other stored properties.

---

# 58. Candidate Key, Primary Key, Alternate Key

Suppose:

`Employee_ID`

`Email`

`Phone_Number`

are all unique and minimal.

Then:

`Candidate Keys:`

`{Employee_ID}`

`{Email}`

`{Phone_Number}`

Choose:

`{Employee_ID}`

as:

`Primary Key`

Remaining:

`{Email}`

`{Phone_Number}`

become:

`Alternate Keys`

---

# 59. Key Hierarchy

> [!summary]
> Think of keys as a hierarchy:

    Super Keys
        ↓
    Minimal Super Keys
        ↓
    Candidate Keys
        ↓
    Selected Candidate Key
        ↓
    Primary Key

Additional candidate keys:

    Remaining Candidate Keys
        ↓
    Alternate Keys

This hierarchy is one of the most important DBMS interview concepts.

---

# 60. Super Key Example

Relation:

`STUDENT(Student_ID, Email, Name)`

Assume:

`Student_ID`

and:

`Email`

are unique.

Super keys can include:

`{Student_ID}`

`{Email}`

`{Student_ID, Name}`

`{Email, Name}`

`{Student_ID, Email}`

`{Student_ID, Email, Name}`

Candidate keys:

`{Student_ID}`

`{Email}`

because they are minimal.

---

# 61. Candidate Key Recognition Trick

> [!tip]
> To find a candidate key:
>
> 1. Check whether it uniquely identifies rows.
> 2. Remove unnecessary attributes.
> 3. If it still uniquely identifies rows, the original set was not minimal.
> 4. If removing any attribute breaks uniqueness, it is minimal.

Memory:

`Candidate Key = Unique + Minimal`

---

# 62. Primary Key Recognition Trick

> [!important]
> If the question says:
>
> "The attribute chosen to uniquely identify each row"
>
> think:
>
> **Primary Key**
>
> If it says:
>
> "A minimal attribute set that can uniquely identify rows"
>
> think:
>
> **Candidate Key**
>
> If it says:
>
> "Any attribute set that uniquely identifies rows"
>
> think:
>
> **Super Key**

---

# 63. Interview Recognition Table

| Question Wording | Think |
|---|---|
| Uniquely identifies a row | Key |
| Minimal unique identifier | Candidate Key |
| Selected candidate key | Primary Key |
| Any unique attribute set | Super Key |
| Candidate key not selected | Alternate Key |
| Multiple columns together | Composite Key |
| References another table | Foreign Key |

This table is extremely useful for MCQs.

---

# 64. Advanced Interview Question

## Q1. What is a primary key?

### Strong Answer

> A primary key is a minimal unique identifier selected from the candidate keys of a relation to uniquely identify each tuple. It cannot contain NULL values, and a relation has at most one primary-key constraint.

---

# 65. Interview Question

## Q2. What are the properties of a primary key?

### Answer

The key properties are:

- Unique
- NOT NULL
- Identifies each row
- At most one primary-key constraint per table
- Can consist of one or multiple columns

---

# 66. Interview Question

## Q3. Can a primary key contain multiple columns?

### Answer

Yes.

This is called a:

`Composite Primary Key`

Example:

`PRIMARY KEY (Student_ID, Course_ID)`

---

# 67. Interview Question

## Q4. Can a table have two primary keys?

### Answer

No.

A table can have only one primary-key constraint.

However, that one primary key may contain multiple columns.

Example:

`PRIMARY KEY (A, B)`

is one composite primary key.

---

# 68. Interview Question

## Q5. Can a primary key contain NULL?

### Answer

No.

A primary key must satisfy entity integrity, so its values cannot be NULL.

---

# 69. Interview Question

## Q6. Can a primary key have duplicate values?

### Answer

No.

Duplicate primary-key values violate the uniqueness requirement.

---

# 70. Interview Question

## Q7. Can a primary key be a foreign key?

### Answer

Yes.

A column can be both a primary key and a foreign key.

This is common in shared-primary-key designs and certain one-to-one relationships.

---

# 71. Interview Question

## Q8. What is the difference between primary key and foreign key?

### Answer

`Primary Key`

→ Uniquely identifies rows in its own table.

`Foreign Key`

→ References a key in another table and represents a relationship between tables.

Memory:

`PK → Identity`

`FK → Relationship`

---

# 72. Interview Question

## Q9. Primary key vs candidate key?

### Answer

A table can have multiple candidate keys, but one candidate key is selected as the primary key.

Example:

`Candidate Keys = Student_ID, Email`

If:

`Student_ID`

is selected:

`Primary Key = Student_ID`

`Email = Alternate Key`

---

# 73. Interview Question

## Q10. Primary key vs super key?

### Answer

A super key is any set of attributes that uniquely identifies rows.

A candidate key is a minimal super key.

The primary key is the candidate key selected for the table.

Therefore:

`Primary Key ⊂ Candidate Keys ⊂ Super Keys`

Conceptually, the primary key is one selected minimal unique identifier.

---

# 74. Interview Question

## Q11. What is a composite primary key?

### Answer

> A composite primary key consists of two or more columns that together uniquely identify a row.

Example:

`PRIMARY KEY (Student_ID, Course_ID)`

---

# 75. Interview Question

## Q12. What is entity integrity?

### Answer

> Entity integrity requires the primary key of a relation to contain no NULL values, ensuring that every row has a valid identity.

---

# 76. Interview Question

## Q13. What happens if we insert a duplicate primary key?

### Answer

The database rejects the operation because it violates the primary-key uniqueness constraint.

---

# 77. Interview Question

## Q14. What happens if we insert NULL into a primary-key column?

### Answer

The database rejects the operation because primary-key values cannot be NULL.

---

# 78. Interview Question

## Q15. Can a primary key be changed?

### Answer

Technically yes, but it should generally be stable. Changing it can affect foreign-key references and relationships in other tables.

---

# 79. Interview Question

## Q16. What is a surrogate primary key?

### Answer

> A surrogate primary key is an artificial identifier created primarily for database identity rather than representing a real-world business attribute.

Example:

`Employee_ID`

---

# 80. Interview Question

## Q17. What is a natural primary key?

### Answer

A natural key uses meaningful real-world data that is unique under the business rules.

Examples:

`ISBN`

`Country_Code`

`Email`

depending on requirements.

---

# 81. Advanced Interview Question

## Q18. Why might a surrogate key be preferred over an email as a primary key?

### Strong Answer

> Email may change, can be relatively large, and may have business-specific semantics. A surrogate numeric identifier can be smaller, stable, and easier to reference from other tables.

---

# 82. Advanced Interview Question

## Q19. Does every table need a primary key?

A strong practical answer:

> A well-designed relational table generally should have a key that uniquely identifies its rows, and a primary key is the conventional way to enforce that identity. However, the SQL standard and individual DBMSs may allow tables without an explicitly declared primary key.

For production database design:

`Prefer a clear primary key.`

---

# 83. Advanced Interview Question

## Q20. Can a UNIQUE column be a primary key later?

Yes.

If the column satisfies the requirements for a candidate key, it can be selected as the primary key.

Example:

`Email`

may be unique and non-null.

It could potentially become:

`PRIMARY KEY`

depending on the design.

---

# 84. Advanced Interview Question

## Q21. Why should a primary key be minimal?

A primary key is selected from candidate keys, which are minimal super keys.

Using unnecessary columns can:

- Increase storage
- Make foreign keys larger
- Make joins more cumbersome
- Complicate indexing
- Reduce simplicity

Therefore:

> [!tip]
> Prefer a minimal, stable, appropriate primary key.

---

# 85. Advanced Interview Question

## Q22. Can a primary key be a string?

Yes.

Example:

`Country_Code CHAR(2) PRIMARY KEY`

The primary-key requirement is uniqueness and non-nullability, not a specific data type.

---

# 86. Advanced Interview Question

## Q23. Can a primary key contain multiple data types?

A composite primary key can contain columns of different compatible data types.

Example conceptually:

`Country_Code + Account_Number`

The exact SQL type compatibility and indexing behavior depend on the DBMS.

---

# 87. Advanced Interview Question

## Q24. Why is primary-key choice important for performance?

Because primary keys are frequently indexed and referenced by other tables.

A poor key can cause:

- Larger indexes
- Larger foreign keys
- More expensive joins
- More storage
- More complicated updates

A good key is usually:

`Stable + Compact + Unique + Appropriate`

---

# 88. Advanced Interview Question

## Q25. What is the relationship between primary key and normalization?

A primary key is essential when reasoning about functional dependencies and normal forms.

Example:

`Student_ID → Student_Name`

The primary key helps determine whether non-key attributes depend correctly on the key.

Composite primary keys are especially important for identifying partial dependencies in 2NF.

---

# 89. Placement Exam Pattern — Direct MCQ

### Question

Which constraint uniquely identifies every record in a table?

### Answer

`PRIMARY KEY`

---

# 90. Placement Exam Pattern — NULL

### Question

Which constraint does not allow NULL values and uniquely identifies each row?

### Answer

`PRIMARY KEY`

---

# 91. Placement Exam Pattern — Multiple Keys

### Question

A table has three candidate keys. How many can be selected as the primary key?

### Answer

`One`

The others can remain alternate keys.

---

# 92. Placement Exam Pattern — Composite Key

### Question

Neither `A` nor `B` uniquely identifies a row, but `(A,B)` does. What type of key is `(A,B)`?

### Answer

`Composite Candidate Key`

If selected as the table's primary key:

`Composite Primary Key`

---

# 93. Placement Exam Pattern — Minimality

### Question

`{A,B}` uniquely identifies a row. `A` alone also uniquely identifies it. Is `{A,B}` a candidate key?

### Answer

No.

Why?

Because:

`A`

alone is sufficient.

Therefore:

`{A,B}`

is a super key but not a minimal candidate key.

---

# 94. Placement Exam Pattern — Super Key

### Question

If `A` uniquely identifies rows, is `{A,B}` a super key?

### Answer

Yes.

If `A` alone is unique, adding extra attributes still leaves the set unique.

Therefore:

`{A}` → Super Key

`{A,B}` → Super Key

But:

`{A,B}` → Not candidate if `A` alone is sufficient.

---

# 95. Placement Exam Pattern — Candidate Key

### Question

What is the defining property of a candidate key?

### Answer

`Uniqueness + Minimality`

---

# 96. Placement Exam Pattern — Primary Key

### Question

Which candidate key is selected to uniquely identify tuples?

### Answer

`Primary Key`

---

# 97. Placement Exam Pattern — Alternate Key

### Question

What happens to candidate keys that are not selected as the primary key?

### Answer

They are called:

`Alternate Keys`

---

# 98. Placement Exam Pattern — Entity Integrity

### Question

Which integrity rule ensures that the primary key cannot be NULL?

### Answer

`Entity Integrity`

---

# 99. Placement Exam Pattern — Referential Integrity

### Question

Which integrity rule ensures valid references between related tables?

### Answer

`Referential Integrity`

---

# 100. Advanced Real-Time Design Pattern

Consider an e-commerce system.

Tables:

`CUSTOMER`

`ORDER`

`ORDER_ITEM`

`PRODUCT`

Keys:

`Customer_ID → PK`

`Order_ID → PK`

`Product_ID → PK`

`(Order_ID, Product_ID) → Composite PK`

Relationships:

`Customer 1:N Order`

`Order 1:N Order_Item`

`Product 1:N Order_Item`

This is a classic transformation of an original:

`Order M:N Product`

relationship.

---

# 101. Primary Key Design Pattern

When designing a table:

    TABLE
    ↓
    Ask:
    What does one row represent?
    ↓
    Find unique identity
    ↓
    Check uniqueness
    ↓
    Check minimality
    ↓
    Check stability
    ↓
    Select primary key
    ↓
    Add foreign-key relationships
    ↓
    Add other constraints

This is a professional workflow.

---

# 102. Primary Key Decision Tree

> [!important]
> When searching for a primary key, use this:

    START
      ↓
    Does an attribute uniquely identify each row?
      ↓
    YES
      ↓
    Is it minimal?
      ↓
    YES
      ↓
    Is it stable and appropriate?
      ↓
    YES
      ↓
    Candidate Key
      ↓
    Select as Primary Key

If no single attribute works:

    Try combinations
      ↓
    Composite Candidate Key
      ↓
    Select appropriate candidate
      ↓
    Composite Primary Key

---

# 103. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking primary key means only one column

Wrong.

A primary key can be:

`Single Column`

or:

`Multiple Columns`

---

### Mistake 2 — Thinking candidate key and primary key are identical

Wrong.

A table may have multiple candidate keys.

Only one is selected as the primary key.

---

### Mistake 3 — Forgetting minimality

A super key does not automatically qualify as a candidate key.

Candidate key:

`Unique + Minimal`

---

### Mistake 4 — Thinking every unique column is automatically the primary key

Wrong.

A unique column may be a candidate key.

The designer chooses which candidate key becomes primary.

---

### Mistake 5 — Thinking primary key means auto-increment

Wrong.

`AUTO_INCREMENT`

is a value-generation mechanism.

`PRIMARY KEY`

is an identity constraint.

---

### Mistake 6 — Thinking primary key must be numeric

Wrong.

A primary key can be:

`INT`

`CHAR`

`VARCHAR`

`UUID`

or another suitable type.

---

### Mistake 7 — Confusing primary key with foreign key

`PK`

→ Identifies rows in its own table.

`FK`

→ References a key in another table.

---

### Mistake 8 — Assuming a foreign key must reference only a primary key

A foreign key commonly references a primary key, and in many SQL systems it can also reference an appropriate UNIQUE key subject to DBMS rules.

---

### Mistake 9 — Choosing a mutable business value without thinking

Email may be unique but can change.

Always consider:

`Stability`

---

### Mistake 10 — Ignoring the grain

Before selecting the primary key, ask:

> What exactly does one row represent?

This prevents many database-design mistakes.

---

# 104. Must-Master Patterns

> [!important] Must Master

1. Primary key definition
2. Primary key properties
3. Primary key vs candidate key
4. Primary key vs super key
5. Primary key vs foreign key
6. Candidate key vs alternate key
7. Super key vs candidate key
8. Minimality
9. Composite primary key
10. Entity integrity
11. Referential integrity
12. Natural key
13. Surrogate key
14. Primary key and NULL
15. Primary key and duplicates
16. Multiple candidate keys
17. Shared primary key
18. Primary key as foreign key
19. Primary key and indexing
20. Primary key and normalization
21. Primary key selection
22. Stable vs mutable keys
23. Table grain
24. M:N relationship keys
25. Foreign-key references

---

# 105. Master Key Comparison

| Key | Unique? | Minimal? | Main Purpose |
|---|---|---|---|
| Super Key | Yes | Not necessarily | Identify rows |
| Candidate Key | Yes | Yes | Minimal unique identity |
| Primary Key | Yes | Yes | Selected candidate key |
| Alternate Key | Yes | Yes | Candidate key not selected |
| Foreign Key | Not necessarily | Not necessarily | Reference another table |
| Composite Key | Depends on context | Depends | Multiple columns together form key |

Important:

`Composite`

describes the number of columns.

It is not a completely separate logical category from candidate/primary keys.

For example:

`(Student_ID, Course_ID)`

can be:

`Composite Candidate Key`

or:

`Composite Primary Key`

---

# 106. Key Relationship Diagram

    SUPER KEY
        |
        | remove unnecessary attributes
        ↓
    CANDIDATE KEY
        |
        | choose one
        ↓
    PRIMARY KEY

Remaining candidate keys:

    CANDIDATE KEYS
        |
        | not selected
        ↓
    ALTERNATE KEYS

Separate concept:

    FOREIGN KEY
        ↓
    References another table's key

---

# 107. One-Minute Revision

> [!summary] One-Minute Revision

    PRIMARY KEY
    → Selected candidate key
    → Uniquely identifies every row
    → Cannot contain NULL
    → No duplicate values
    → At most one primary-key constraint per table
    → Can contain multiple columns

    CANDIDATE KEY
    → Minimal unique identifier

    SUPER KEY
    → Any unique attribute set

    ALTERNATE KEY
    → Candidate key not selected as primary

    COMPOSITE KEY
    → Key containing multiple columns

    FOREIGN KEY
    → References another table's key

    ENTITY INTEGRITY
    → Primary key cannot be NULL

    REFERENTIAL INTEGRITY
    → Foreign-key references must be valid according to constraints

    NATURAL KEY
    → Real-world meaningful identifier

    SURROGATE KEY
    → Artificial database identifier

    PRIMARY KEY FORMULA

    Primary Key
    =
    Selected Candidate Key

    CANDIDATE KEY

    Candidate Key
    =
    Super Key
    +
    Minimality

    FAST RECOGNITION

    "Uniquely identifies each row"
    → Primary Key

    "Minimal unique identifier"
    → Candidate Key

    "Any attribute set that uniquely identifies"
    → Super Key

    "Candidate key not selected"
    → Alternate Key

    "Two or more columns together"
    → Composite Key

    "References another table"
    → Foreign Key

    "Cannot contain NULL"
    → Primary Key / Entity Integrity

    "What does one row represent?"
    → Determine table grain before choosing the key

    MOST IMPORTANT MEMORY

    PK → Identity
    FK → Relationship
    Candidate → Minimal
    Super → Any unique set
    Alternate → Unselected candidate
    Composite → Multiple columns
---

# 108. Golden Memory Trick

**Primary Key = one stable, minimal, unique identity for every row, with no NULL values.**

# 109. One-Line Recognition

**If the question asks which column or combination uniquely identifies every row of a table, think Primary Key.**