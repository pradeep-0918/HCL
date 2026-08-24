---
type: concept
subject: dbms
topic: "Alternate Key"
parent: "Keys"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - keys
  - alternate-key
  - candidate-key
  - primary-key
  - super-key
  - unique-key
  - relational-model
  - sql
  - database-design
  - normalization
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
  - "[[Super Key]]"
  - "[[Foreign Key]]"
  - "[[Composite Key]]"
  - "[[Constraints]]"
  - "[[Functional Dependency]]"
  - "[[Normalization]]"
---

# Alternate Key

## 1. Core Concept

> [!summary]
> An **Alternate Key** is a candidate key that is not selected as the primary key.

This is the most important definition.

Suppose a table has three candidate keys:

```text
Student_ID
Email
Phone_Number
```

Choose:

```text
Student_ID
```

as the primary key.

Then:

```text
Email
Phone_Number
```

are alternate keys.

The relationship is:

```text
Candidate Keys
       |
       | choose one
       ↓
Primary Key

Remaining Candidate Keys
       ↓
Alternate Keys
```

Memory:

**Alternate Key = Candidate Key that was not chosen as Primary Key.**

---

# 2. Basic Meaning

A table can have multiple candidate keys.

Example:

| Student_ID | Email | Phone_Number | Name |
|---:|---|---|---|
| 101 | arun@gmail.com | 9876500001 | Arun |
| 102 | priya@gmail.com | 9876500002 | Priya |
| 103 | ravi@gmail.com | 9876500003 | Ravi |

Assume:

```text
Student_ID → Unique
Email → Unique
Phone_Number → Unique
```

Then:

```text
Candidate Keys:

{Student_ID}
{Email}
{Phone_Number}
```

If we select:

```text
Student_ID
```

as the primary key:

```text
Primary Key:
Student_ID

Alternate Keys:
Email
Phone_Number
```

---

# 3. Main Formula

There is no mathematical formula, but there is a very important conceptual relationship:

```text
Alternate Key
=
Candidate Key
-
Selected Primary Key
```

More precisely:

```text
Alternate Keys
=
Candidate Keys not selected as Primary Key
```

And:

```text
Primary Key
⊂
Candidate Keys
```

---

# 4. Key Hierarchy

The complete hierarchy is:

```text
SUPER KEY
    ↓
Minimal Super Key
    ↓
CANDIDATE KEY
    ↓
Choose One
    ↓
PRIMARY KEY

Remaining Candidate Keys
    ↓
ALTERNATE KEYS
```

This hierarchy should be memorized for interviews.

---

# 5. Candidate Key vs Alternate Key

A candidate key becomes an alternate key only after another candidate key is selected as the primary key.

Before selection:

```text
Student_ID
Email
Phone
```

are all:

```text
Candidate Keys
```

After selecting:

```text
Student_ID
```

as primary:

```text
Student_ID → Primary Key
Email      → Alternate Key
Phone      → Alternate Key
```

Therefore:

> [!important]
> **"Candidate Key" describes its ability to uniquely identify rows.**
>
> **"Alternate Key" describes its role after another candidate key has been selected as primary.**

---

# 6. Why Is It Called "Alternate"?

The word **alternate** means:

> "Another possible choice."

Suppose:

```text
Student_ID
Email
```

both uniquely identify students.

Either could potentially be selected as primary.

If:

```text
Student_ID
```

is selected:

```text
Email
```

becomes the alternate choice.

Therefore:

```text
Candidate
→ Possible Primary

Alternate
→ Possible Primary but not selected
```

---

# 7. Simple Example

Consider:

| Employee_ID | Email | Name |
|---:|---|---|
| 1 | a@company.com | Arun |
| 2 | p@company.com | Priya |
| 3 | r@company.com | Ravi |

Assume:

```text
Employee_ID
Email
```

are both candidate keys.

Choose:

```text
Employee_ID
```

as primary.

Therefore:

```text
Primary Key:
Employee_ID

Alternate Key:
Email
```

---

# 8. Important Property

> [!important]
> An alternate key is still a candidate key.

It does not stop being a candidate key.

It simply means:

```text
Candidate Key
+
Not selected as Primary
=
Alternate Key
```

Therefore:

```text
Alternate Key ⊆ Candidate Keys
```

---

# 9. Alternate Key vs Super Key

Suppose:

```text
Candidate Keys:
A
B
```

Choose:

```text
A
```

as primary.

Then:

```text
B
→ Alternate Key
```

Now:

```text
BC
```

may be a super key.

But:

```text
BC
```

is not an alternate key if `B` alone is already a candidate key.

Why?

Because alternate keys must themselves be candidate keys.

Therefore:

```text
B
→ Candidate + Alternate

BC
→ Super Key only
```

---

# 10. Alternate Key vs Primary Key

| Feature | Primary Key | Alternate Key |
|---|---|---|
| Is a candidate key? | Yes | Yes |
| Selected as main identifier? | Yes | No |
| Minimal? | Yes | Yes |
| Unique? | Yes | Yes |
| Can be multiple? | One selected PK | Multiple alternate keys possible |
| Main purpose | Main row identity | Alternative unique identity |

Memory:

```text
Primary
→ Chosen

Alternate
→ Not chosen
```

---

# 11. Alternate Key vs UNIQUE Constraint

This is an important SQL distinction.

An alternate key is fundamentally a **relational database design concept**.

In SQL, its uniqueness is commonly enforced using a:

```sql
UNIQUE
```

constraint.

Example:

```sql
CREATE TABLE Student (
    Student_ID INT PRIMARY KEY,
    Email VARCHAR(100) UNIQUE
);
```

Here:

```text
Student_ID
→ Primary Key

Email
→ Alternate candidate identifier
→ Uniqueness enforced with UNIQUE
```

Exact NULL behavior for UNIQUE constraints can vary by DBMS.

---

# 12. Why Use UNIQUE for Alternate Keys?

Suppose:

```text
Student_ID
```

is primary.

But:

```text
Email
```

must also be unique.

We can enforce:

```sql
UNIQUE (Email)
```

This prevents duplicate email values.

Therefore:

```text
Primary Key
→ PRIMARY KEY

Alternate Key
→ Commonly enforced using UNIQUE
```

---

# 13. SQL Example

```sql
CREATE TABLE Student (
    Student_ID INT PRIMARY KEY,
    Email VARCHAR(100) UNIQUE,
    Phone_Number VARCHAR(20) UNIQUE,
    Name VARCHAR(100)
);
```

Conceptually:

```text
Student_ID
→ Primary Key

Email
→ Alternate Key

Phone_Number
→ Alternate Key
```

assuming both are intended candidate keys under the data model.

---

# 14. Alternate Key and Uniqueness

Suppose:

```text
Student_ID → Primary Key
Email → Alternate Key
```

Then duplicate email addresses should not be allowed if the alternate-key rule is enforced.

Invalid:

| Student_ID | Email |
|---:|---|
| 101 | a@gmail.com |
| 102 | a@gmail.com |

Why?

Because:

```text
Email
```

is intended to uniquely identify a student.

---

# 15. Alternate Key and NULL

Be careful here.

An alternate key is conceptually a candidate key and therefore represents a unique identifier.

However, SQL `UNIQUE` constraint behavior regarding NULL varies between database systems.

For example, some DBMSs allow multiple NULLs in a UNIQUE column, while others treat NULL uniqueness differently.

Therefore:

> [!warning]
> Do not use the simplified rule "UNIQUE always behaves exactly like a candidate key" in an interview.

A declared primary key is explicitly non-null.

---

# 16. Alternate Key and Candidate Key

Example:

```text
R(Student_ID, Email, Phone)
```

Suppose:

```text
Student_ID
Email
Phone
```

are candidate keys.

Choose:

```text
Student_ID
```

as primary.

Then:

```text
Email
Phone
```

become alternate keys.

The complete classification:

```text
Candidate Keys:
Student_ID
Email
Phone

Primary:
Student_ID

Alternate:
Email
Phone
```

---

# 17. Alternate Key and Business Requirements

Alternate keys are useful when users identify records using a business attribute other than the internal primary key.

Example:

An e-commerce system may internally use:

```text
Customer_ID
```

as primary key.

But customers may be searched using:

```text
Email
```

If email is guaranteed unique, it can serve as an alternate unique identifier.

Therefore:

```text
Customer_ID
→ Internal identity

Email
→ Business-facing alternate identifier
```

---

# 18. Real-Time Example — Employee System

Suppose:

```text
EMPLOYEE
Employee_ID
Company_Email
Employee_Name
Department
```

Assume:

```text
Employee_ID
Company_Email
```

are candidate keys.

Choose:

```text
Employee_ID
```

as primary.

Then:

```text
Company_Email
```

is an alternate key.

Why is this useful?

A system may use:

```text
Employee_ID
```

internally while administrators search by:

```text
Company_Email
```

---

# 19. Real-Time Example — Product Catalog

Suppose:

```text
PRODUCT
Product_ID
SKU
Barcode
Name
Price
```

Assume:

```text
Product_ID
SKU
Barcode
```

are candidate keys.

Choose:

```text
Product_ID
```

as primary.

Then:

```text
SKU
Barcode
```

are alternate keys.

Possible usage:

```text
Product_ID
→ Internal database identity

SKU
→ Business/product identifier

Barcode
→ External scanning identifier
```

---

# 20. Real-Time Example — Book Database

Suppose:

```text
BOOK
Book_ID
ISBN
Title
Author
```

If both:

```text
Book_ID
ISBN
```

are candidate keys:

Choose:

```text
Book_ID
```

as primary.

Then:

```text
ISBN
→ Alternate Key
```

A library system may internally use `Book_ID` while external users search by ISBN.

---

# 21. Real-Time Example — Banking

Suppose:

```text
ACCOUNT
Account_ID
Account_Number
Customer_ID
Balance
```

If:

```text
Account_ID
Account_Number
```

are both candidate keys:

```text
Account_ID
→ Primary

Account_Number
→ Alternate
```

The database can internally use the ID while business users interact with the account number.

---

# 22. Real-Time Example — E-Commerce

Suppose:

```text
CUSTOMER
Customer_ID
Email
Phone
Name
```

Potential candidate keys:

```text
Customer_ID
Email
Phone
```

Choose:

```text
Customer_ID
```

as primary.

Then:

```text
Email
Phone
```

can be alternate keys if business rules guarantee uniqueness.

This is common in real-world systems.

---

# 23. Real-Time Example — University

Suppose:

```text
STUDENT
Student_ID
Register_Number
Email
Name
```

If:

```text
Student_ID
Register_Number
Email
```

are unique and minimal:

```text
Candidate Keys:
Student_ID
Register_Number
Email
```

Choose:

```text
Student_ID
```

as primary.

Then:

```text
Register_Number
Email
```

are alternate keys.

---

# 24. Why Not Make Every Candidate Key Primary?

A table has only one primary-key constraint.

Why?

Because the database needs one designated primary identity for the relation.

Other candidate keys can still enforce uniqueness and provide alternative ways to identify rows.

Therefore:

```text
One Primary Key
+
Zero or More Alternate Keys
```

---

# 25. Can There Be Zero Alternate Keys?

Yes.

If a table has only one candidate key:

```text
Candidate Keys:
A
```

and `A` is selected as primary:

```text
Primary Key:
A

Alternate Keys:
None
```

Therefore:

> [!important]
> A table does not have to have an alternate key.

---

# 26. Can There Be Multiple Alternate Keys?

Yes.

Example:

```text
Candidate Keys:

Student_ID
Email
Phone
Register_Number
```

Choose:

```text
Student_ID
```

as primary.

Then:

```text
Email
Phone
Register_Number
```

are alternate keys.

So:

```text
1 Primary Key
+
3 Alternate Keys
```

is possible.

---

# 27. Can an Alternate Key Be Composite?

Yes.

An alternate key is a candidate key not selected as primary.

A candidate key can be composite.

Therefore an alternate key can also be composite.

Example:

Candidate keys:

```text
A
(B,C)
```

Choose:

```text
A
```

as primary.

Then:

```text
(B,C)
```

is a:

**Composite Alternate Key**

---

# 28. Composite Alternate Key Example

Consider:

```text
BOOKING
Customer_ID
Flight_ID
Seat_No
```

Suppose:

```text
Booking_ID
```

is primary.

And business rules guarantee:

```text
(Customer_ID, Flight_ID, Seat_No)
```

is unique and minimal.

Then:

```text
Booking_ID
→ Primary Key

(Customer_ID, Flight_ID, Seat_No)
→ Composite Alternate Key
```

---

# 29. Alternate Key and Composite Key

Remember:

```text
Composite
→ Describes number of attributes.

Alternate
→ Describes role relative to Primary Key.
```

Therefore a key can be:

```text
Composite Primary Key
```

or:

```text
Composite Alternate Key
```

or:

```text
Composite Candidate Key
```

depending on context.

---

# 30. Alternate Key and Foreign Key

An alternate key can sometimes be referenced by a foreign key if the DBMS permits referencing the corresponding UNIQUE/candidate key.

Example:

Parent:

```text
CUSTOMER
Customer_ID PRIMARY KEY
Email UNIQUE
```

Child:

```text
SUBSCRIPTION
Email FOREIGN KEY
```

Possible relationship:

```text
Subscription.Email
→ Customer.Email
```

subject to the DBMS's referenced-key rules.

Therefore:

> [!tip]
> A foreign key does not conceptually have to reference only the primary key.

---

# 31. Alternate Key and Indexing

Alternate keys are frequently enforced through unique indexes or unique constraints.

Example:

```sql
CREATE TABLE Customer (
    Customer_ID INT PRIMARY KEY,
    Email VARCHAR(255) UNIQUE
);
```

The database may use a unique index to enforce uniqueness.

However:

> [!warning]
> Constraint implementation and index behavior depend on the DBMS.

The important conceptual point is:

```text
Alternate Key
→ Unique identification
→ Commonly enforced using UNIQUE
```

---

# 32. Alternate Key and Performance

Alternate keys can make lookups efficient when the database maintains suitable unique indexes.

Example:

```sql
SELECT *
FROM Customer
WHERE Email = 'arun@gmail.com';
```

If email has a unique index:

```text
Email
→ Fast lookup
```

But the primary purpose of the alternate-key constraint is uniqueness/integrity, not merely speed.

---

# 33. Alternate Key and Functional Dependency

Suppose:

```text
Student_ID
```

and:

```text
Email
```

are candidate keys.

Then:

```text
Student_ID → all student attributes

Email → all student attributes
```

If:

```text
Student_ID
```

is selected as primary:

```text
Email
→ Alternate Key
```

This shows that an alternate key is still functionally capable of identifying the complete tuple.

---

# 34. Alternate Key and Normalization

Candidate keys are important in normalization.

Since alternate keys are candidate keys:

```text
Alternate Key
→ Candidate Key
→ Important for normalization
```

In particular, candidate keys help identify:

- Prime attributes
- Non-prime attributes
- Partial dependencies
- Transitive dependencies
- BCNF determinants

---

# 35. Prime Attributes and Alternate Keys

Suppose candidate keys are:

```text
{A}
{B,C}
```

Choose:

```text
A
```

as primary.

Then:

```text
A
→ Primary

(B,C)
→ Composite Alternate
```

Prime attributes are:

```text
A
B
C
```

Why?

Because all three belong to at least one candidate key.

---

# 36. Advanced Example — Candidate and Alternate Keys

Relation:

```text
R(A,B,C,D)
```

Suppose candidate keys are:

```text
{A}
{B,C}
```

Choose:

```text
A
```

as primary.

Then:

```text
Primary Key:
A

Alternate Key:
(B,C)
```

Both uniquely identify rows.

Difference:

```text
A
→ Selected

(B,C)
→ Not selected
```

---

# 37. Alternate Key Recognition Algorithm

Use this in exams:

```text
Step 1:
Find all candidate keys.

Step 2:
Identify which candidate key is selected as primary.

Step 3:
All remaining candidate keys are alternate keys.
```

Memory:

```text
Find Candidates
      ↓
Choose Primary
      ↓
Remaining
      ↓
Alternate
```

---

# 38. Alternate Key Recognition Trick

> [!important]
> If a question says:
>
> "Which candidate key is not selected as the primary key?"
>
> answer:
>
> **Alternate Key**

If it says:

> "Which key is selected from the candidate keys?"

answer:

**Primary Key**

If it says:

> "Minimal unique attribute set?"

answer:

**Candidate Key**

---

# 39. Fast Key Mapping

> [!tip]

```text
"Any unique set"
→ Super Key

"Minimal unique set"
→ Candidate Key

"Selected candidate"
→ Primary Key

"Unselected candidate"
→ Alternate Key

"References another table"
→ Foreign Key

"Multiple attributes"
→ Composite Key
```

This mapping can solve many DBMS MCQs within seconds.

---

# 40. Advanced Example — Multiple Candidate Keys

Suppose:

```text
Candidate Keys:

K1 = A
K2 = B
K3 = C
```

Choose:

```text
A
```

as primary.

Then:

```text
B
→ Alternate

C
→ Alternate
```

If the table has no other candidate keys:

```text
Total Candidate Keys = 3
Primary Keys = 1
Alternate Keys = 2
```

General relationship:

```text
Number of Alternate Keys
=
Number of Candidate Keys - 1
```

when a primary key has been selected.

---

# 41. Example — Four Candidate Keys

Suppose a relation has:

```text
Candidate Keys:
A
B
C
D
```

Choose:

```text
A
```

as primary.

Then:

```text
Alternate Keys:
B
C
D
```

Therefore:

```text
4 Candidate Keys
1 Primary
3 Alternate
```

---

# 42. Placement Exam Pattern

### Question

A relation has 5 candidate keys. One is selected as the primary key. How many alternate keys are there?

### Calculation

```text
Alternate Keys
=
Candidate Keys - Primary Key

= 5 - 1

= 4
```

### Answer

```text
4 Alternate Keys
```

---

# 43. Placement Exam Pattern

### Question

Which key is a candidate key that is not chosen as the primary key?

### Answer

```text
Alternate Key
```

---

# 44. Placement Exam Pattern

### Question

A table has only one candidate key. Can it have an alternate key?

### Answer

No.

There is no remaining candidate key after selecting the only candidate as primary.

---

# 45. Placement Exam Pattern

### Question

A table has three candidate keys. Can it have three primary keys?

### Answer

No.

It has:

```text
3 Candidate Keys
1 Primary Key
2 Alternate Keys
```

---

# 46. Placement Exam Pattern

### Question

If `A` and `B` are candidate keys and `A` is selected as primary, what is `B`?

### Answer

```text
Alternate Key
```

---

# 47. Placement Exam Pattern

### Question

If `A` is a primary key and `(B,C)` is another candidate key, what is `(B,C)`?

### Answer

```text
Composite Alternate Key
```

---

# 48. Placement Exam Pattern

### Question

Can an alternate key contain multiple attributes?

### Answer

Yes.

If a composite candidate key is not selected as primary, it becomes a composite alternate key.

---

# 49. Placement Exam Pattern

### Question

Is an alternate key unique?

### Answer

Conceptually, yes.

It is a candidate key, so it is a minimal unique identifier.

In SQL, the intended uniqueness is commonly enforced with a `UNIQUE` constraint or equivalent mechanism.

---

# 50. Placement Exam Pattern

### Question

Is an alternate key a super key?

### Answer

Yes.

Because:

```text
Alternate Key
→ Candidate Key
→ Super Key
```

---

# 51. Placement Exam Pattern

### Question

Is every unique column an alternate key?

### Answer

Not necessarily.

It must be a candidate key, meaning it must be unique and minimal under the intended data model.

Also, it must not be the selected primary key.

---

# 52. Placement Exam Pattern

### Question

If `A` and `B` together form a candidate key and `A` alone is also a candidate key, can `(A,B)` be an alternate key?

### Answer

No.

If `A` alone is a candidate key, then `(A,B)` is not minimal.

Therefore:

```text
(A,B)
→ Super Key

(A,B)
→ Not Candidate Key

(A,B)
→ Not Alternate Key
```

---

# 53. Advanced Interview Question

## Q1. What is an alternate key?

### Strong Answer

> An alternate key is a candidate key that is not selected as the primary key. It remains a minimal unique identifier and can be enforced as an additional uniqueness constraint.

---

# 54. Interview Question

## Q2. Is an alternate key a candidate key?

### Answer

Yes.

An alternate key is a candidate key that was not chosen as the primary key.

---

# 55. Interview Question

## Q3. Is an alternate key a super key?

### Answer

Yes.

Because every candidate key is a super key.

---

# 56. Interview Question

## Q4. Can a table have multiple alternate keys?

### Answer

Yes.

If the table has multiple candidate keys and one is selected as primary, all remaining candidate keys are alternate keys.

---

# 57. Interview Question

## Q5. Can a table have zero alternate keys?

### Answer

Yes.

If it has only one candidate key and that key becomes the primary key, there are no alternate keys.

---

# 58. Interview Question

## Q6. Can an alternate key be composite?

### Answer

Yes.

If a composite candidate key is not selected as primary, it becomes a composite alternate key.

---

# 59. Interview Question

## Q7. How is an alternate key commonly implemented in SQL?

### Answer

Usually with a `UNIQUE` constraint or equivalent unique mechanism.

Example:

```sql
CREATE TABLE Student (
    Student_ID INT PRIMARY KEY,
    Email VARCHAR(100) UNIQUE
);
```

---

# 60. Interview Question

## Q8. What is the difference between UNIQUE and alternate key?

### Strong Answer

> Alternate key is a relational-design concept referring to an unselected candidate key. `UNIQUE` is an SQL constraint used to enforce uniqueness. A UNIQUE constraint may implement an alternate-key requirement, but the concepts are not identical.

---

# 61. Interview Question

## Q9. Can a foreign key reference an alternate key?

### Answer

Yes, where the DBMS permits a suitable UNIQUE/candidate key to be referenced.

The referenced columns must satisfy the DBMS's rules.

---

# 62. Interview Question

## Q10. Why are alternate keys useful?

### Answer

They allow the database to maintain multiple valid unique identifiers.

For example:

```text
Customer_ID
Email
```

The system may internally use `Customer_ID` while users search using `Email`.

---

# 63. Advanced Interview Question

## Q11. Why not make an alternate key the primary key?

### Answer

It could potentially have been selected as primary, but the designer may prefer another candidate key because of:

- Stability
- Size
- Simplicity
- Business semantics
- Indexing considerations
- Foreign-key relationships
- Application architecture

---

# 64. Advanced Interview Question

## Q12. Is an alternate key necessarily a natural key?

No.

An alternate key can be natural or surrogate depending on the data model.

However, in many practical designs, alternate keys are business-facing identifiers such as:

```text
Email
SKU
ISBN
```

---

# 65. Advanced Interview Question

## Q13. Can a primary key also be an alternate key?

No.

Once a candidate key is selected as primary, it is called the primary key, not an alternate key.

---

# 66. Advanced Interview Question

## Q14. If a candidate key is not selected as primary, what does it become?

```text
Alternate Key
```

This is one of the easiest direct interview questions.

---

# 67. Advanced Interview Question

## Q15. Does an alternate key have to be minimal?

Yes.

Because it is a candidate key.

```text
Alternate Key
→ Candidate Key
→ Minimal
```

---

# 68. Advanced Interview Question

## Q16. Is a super key that is not minimal an alternate key?

No.

An alternate key must be a candidate key.

Therefore:

```text
Non-minimal Super Key
→ Not Candidate
→ Not Alternate
```

---

# 69. Advanced Interview Question

## Q17. What is the relationship between primary and alternate keys?

Both are candidate keys.

The difference is selection:

```text
Selected Candidate
→ Primary

Unselected Candidate
→ Alternate
```

---

# 70. Advanced Interview Question

## Q18. Can an alternate key contain NULL in SQL?

The conceptual key should identify rows uniquely, but SQL `UNIQUE` constraint behavior for NULL is DBMS-specific.

Therefore, do not give a universal SQL NULL rule without specifying the DBMS.

---

# 71. Advanced Interview Question

## Q19. Can an alternate key be referenced by a foreign key?

Yes, when the DBMS allows the referenced candidate/unique key.

Example:

```text
Customer.Email
→ UNIQUE

Subscription.Email
→ FK
```

subject to DBMS rules.

---

# 72. Advanced Interview Question

## Q20. How many alternate keys can a table have?

Potentially many.

If there are `n` candidate keys and one is selected as primary:

```text
Alternate Keys = n - 1
```

---

# 73. Advanced Interview Question

## Q21. If a table has 6 candidate keys, how many alternate keys are possible?

Assuming one candidate key is selected as primary:

```text
6 - 1
=
5
```

Therefore:

```text
5 Alternate Keys
```

---

# 74. Advanced Interview Question

## Q22. If a table has no primary key, can we call the remaining candidate keys alternate keys?

For standard terminology, "alternate key" is normally used relative to a designated primary key. If no primary key is selected, the safest description is simply "candidate keys."

---

# 75. Advanced Interview Question

## Q23. Can alternate keys improve data quality?

Yes.

If alternate identifiers are enforced as unique, they prevent duplicate business identifiers.

Example:

```text
Email UNIQUE
```

prevents two rows from using the same email when the business rule requires uniqueness.

---

# 76. Advanced Interview Question

## Q24. Can alternate keys be indexed?

Yes.

A DBMS may implement a UNIQUE constraint using a unique index or another mechanism.

The exact implementation depends on the DBMS.

---

# 77. Advanced Interview Question

## Q25. What is the one-word difference between candidate and alternate key?

**Selection.**

Both are candidate keys.

```text
Selected
→ Primary

Not selected
→ Alternate
```

---

# 78. Real-Time Design Pattern — Customer

Suppose:

```text
CUSTOMER
----------------
Customer_ID
Email
Phone
Name
```

Candidate keys:

```text
Customer_ID
Email
Phone
```

Select:

```text
Customer_ID
```

Then:

```text
Customer_ID
→ Primary Key

Email
→ Alternate Key

Phone
→ Alternate Key
```

SQL:

```sql
CREATE TABLE Customer (
    Customer_ID INT PRIMARY KEY,
    Email VARCHAR(255) UNIQUE,
    Phone VARCHAR(20) UNIQUE,
    Name VARCHAR(100)
);
```

---

# 79. Real-Time Design Pattern — Product

Suppose:

```text
PRODUCT
----------------
Product_ID
SKU
Barcode
Name
Price
```

Candidate keys:

```text
Product_ID
SKU
Barcode
```

Select:

```text
Product_ID
```

Then:

```text
SKU
→ Alternate

Barcode
→ Alternate
```

Possible SQL:

```sql
CREATE TABLE Product (
    Product_ID INT PRIMARY KEY,
    SKU VARCHAR(50) UNIQUE,
    Barcode VARCHAR(100) UNIQUE,
    Name VARCHAR(200),
    Price DECIMAL(10,2)
);
```

---

# 80. Real-Time Design Pattern — Employee

Suppose:

```text
EMPLOYEE
----------------
Employee_ID
Company_Email
Employee_Code
Name
```

Candidate keys:

```text
Employee_ID
Company_Email
Employee_Code
```

Choose:

```text
Employee_ID
```

Primary.

Then:

```text
Company_Email
→ Alternate

Employee_Code
→ Alternate
```

---

# 81. Real-Time Design Pattern — Enrollment

Suppose:

```text
ENROLLMENT
----------------
Enrollment_ID
Student_ID
Course_ID
Semester
```

Candidate keys might be:

```text
Enrollment_ID
(Student_ID, Course_ID, Semester)
```

depending on the business rules.

Choose:

```text
Enrollment_ID
```

as primary.

Then:

```text
(Student_ID, Course_ID, Semester)
→ Composite Alternate Key
```

if the business rule guarantees its uniqueness and minimality.

---

# 82. Advanced Pattern — Business Identifier

A common professional design is:

```text
Surrogate Primary Key
+
Business Alternate Key
```

Example:

```text
Customer_ID
→ Primary

Email
→ Alternate
```

This gives:

```text
Stable Internal Identity
+
Business-Level Unique Identifier
```

This pattern is common in practical database design.

---

# 83. Why This Pattern Is Useful

Suppose:

```text
Customer_ID = 1001
```

is stable.

Email:

```text
arun@gmail.com
```

is unique but may change.

Use:

```text
Customer_ID
→ Internal references

Email
→ Unique business lookup
```

This separates:

```text
Database Identity
```

from:

```text
Business Identity
```

---

# 84. Alternate Key Recognition Tree

> [!important]

```text
Does the attribute set uniquely identify rows?
                |
               YES
                ↓
Is it minimal?
          /             \
        NO               YES
        ↓                 ↓
   Super Key        Candidate Key
                         |
                  Is it selected
                  as Primary?
                    /       \
                  YES        NO
                   ↓          ↓
              Primary Key  Alternate Key
```

This is the fastest conceptual route.

---

# 85. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking alternate key is any UNIQUE column

Not necessarily.

It should correspond to a candidate key under the intended data model.

---

### Mistake 2 — Thinking alternate key is not a candidate key

Wrong.

An alternate key is a candidate key that was not selected as primary.

---

### Mistake 3 — Thinking a table can have only one alternate key

Wrong.

A table can have multiple alternate keys.

---

### Mistake 4 — Thinking every super key can be alternate

Wrong.

It must be minimal.

Therefore:

```text
Super Key
+
Minimality
=
Candidate Key
```

Only an unselected candidate key can be alternate.

---

### Mistake 5 — Thinking primary and alternate keys are completely different key types

They are both candidate keys.

The difference is selection.

---

### Mistake 6 — Assuming UNIQUE and Alternate Key are identical

Not exactly.

`UNIQUE` is an SQL constraint.

Alternate key is a relational-design concept.

---

### Mistake 7 — Forgetting composite alternate keys

An alternate key can contain multiple attributes.

---

### Mistake 8 — Forgetting that alternate keys can be referenced

A suitable alternate/unique key may be referenced by a foreign key depending on DBMS rules.

---

### Mistake 9 — Assuming there must be an alternate key

There may be none.

If there is only one candidate key, there is no alternate key after selecting it as primary.

---

### Mistake 10 — Ignoring business rules

A value appearing unique in a sample does not automatically make it a candidate key.

Uniqueness must be guaranteed by the intended model.

---

# 86. Must-Master Patterns

> [!important] Must Master

1. Alternate key definition
2. Candidate key vs alternate key
3. Primary key vs alternate key
4. Super key vs alternate key
5. Alternate key and UNIQUE constraint
6. Multiple alternate keys
7. Zero alternate keys
8. Composite alternate key
9. Alternate key and foreign key
10. Alternate key and indexing
11. Alternate key and normalization
12. Business identifiers
13. Surrogate primary + alternate business key
14. Candidate-key selection
15. Alternate-key counting
16. Prime attributes
17. Functional dependencies
18. SQL implementation
19. NULL behavior
20. Interview recognition patterns

---

# 87. Master Key Comparison

| Key | Unique | Minimal | Selected as Primary | Main Meaning |
|---|---|---|---|---|
| Super Key | Yes | Not required | Not necessarily | Any unique set |
| Candidate Key | Yes | Yes | Maybe | Possible primary |
| Primary Key | Yes | Yes | Yes | Selected identity |
| Alternate Key | Yes | Yes | No | Unselected candidate |
| Foreign Key | Not necessarily | Not necessarily | No | Reference |
| Composite Key | Depends | Depends | Depends | Multiple columns |

---

# 88. Master Relationship

```text
SUPER KEY
    ↓
Minimality
    ↓
CANDIDATE KEY
    ↓
Selection
    ├───────────────┐
    ↓               ↓
PRIMARY         ALTERNATE
```

Remember:

```text
Primary + Alternate
        ↓
   Candidate Keys
```

---

# 89. Formula Sheet

> [!summary] Formula Sheet

```text
Candidate Key
=
Minimal Super Key

Primary Key
=
Selected Candidate Key

Alternate Key
=
Candidate Key not selected as Primary Key

Number of Alternate Keys
=
Number of Candidate Keys - 1

if a Primary Key has been selected

Candidate Key
⊆
Super Key

Alternate Key
⊆
Candidate Key

Primary Key
⊆
Candidate Key

Candidate Key
→ Unique + Minimal
```

---

# 90. Quick Revision

> [!summary] One-Minute Revision

```text
ALTERNATE KEY
→ A candidate key that is not selected as the primary key.

CANDIDATE KEY
→ Minimal unique identifier.

PRIMARY KEY
→ Selected candidate key.

SUPER KEY
→ Any unique attribute set.

ALTERNATE KEY
→ Unselected candidate key.

EXAMPLE

Candidate Keys:
Student_ID
Email
Phone

Choose:
Student_ID

Therefore:

Student_ID
→ Primary Key

Email
→ Alternate Key

Phone
→ Alternate Key

IMPORTANT

One table:
→ At most one Primary Key

One table:
→ Zero or more Alternate Keys

If only one Candidate Key exists:
→ No Alternate Key

If 5 Candidate Keys exist:
→ 1 Primary + 4 Alternate

COMPOSITE

If:
(A,B)
is a candidate key

and another candidate is selected as primary:

(A,B)
→ Composite Alternate Key

SQL

PRIMARY KEY
→ Commonly identifies the main row identity

UNIQUE
→ Commonly used to enforce alternate-key uniqueness

FOREIGN KEY
→ May reference a suitable alternate/unique key
  depending on DBMS rules

FAST RECOGNITION

"Selected candidate"
→ Primary Key

"Candidate not selected"
→ Alternate Key

"Minimal unique set"
→ Candidate Key

"Any unique set"
→ Super Key

"Multiple columns"
→ Composite Key
```

# 91. Golden Memory Trick

**Alternate Key = "I could have been the Primary Key, but another Candidate Key was chosen."**

# 92. One-Line Recognition

**If a candidate key is not selected as the primary key, immediately recognize it as an Alternate Key.**