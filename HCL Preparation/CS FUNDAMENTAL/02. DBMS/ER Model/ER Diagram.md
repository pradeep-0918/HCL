---
type: concept
subject: dbms
topic: "ER Diagram"
parent: "ER Model"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - er-model
  - er-diagram
  - entity
  - attribute
  - relationship
  - cardinality
  - participation
  - weak-entity
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
  - "[[ER Model]]"
  - "[[Entity]]"
  - "[[Attribute]]"
  - "[[Relationship]]"
  - "[[Cardinality]]"
  - "[[Primary Key]]"
  - "[[Foreign Key]]"
  - "[[Normalization]]"
---

# ER Diagram

## 1. Core Concept

> [!summary]
> An **ER Diagram (Entity-Relationship Diagram)** is a visual representation of the entities, attributes, relationships, cardinalities, and constraints of a database system.

In simple words:

~~~text
ER Diagram
→ Visual Blueprint of a Database
~~~

Before creating actual database tables, we can first draw the system conceptually.

Example:

~~~text
STUDENT
   |
 enrolls
   |
COURSE
~~~

This simple diagram tells us:

~~~text
Student
→ Entity

Course
→ Entity

Enrolls
→ Relationship
~~~

A complete ER diagram can additionally show:

~~~text
Entities
Attributes
Relationships
Keys
Cardinality
Participation
Weak Entities
Specialization
Generalization
~~~

---

# 2. Why ER Diagrams Are Important

A database can contain hundreds or thousands of tables.

Before implementing those tables, we need to understand:

~~~text
What data exists?
       ↓
How is data connected?
       ↓
What constraints exist?
       ↓
How should the database be designed?
~~~

ER diagrams provide this conceptual view.

They are useful for:

- Database design
- Requirement analysis
- Communication between developers and clients
- System design interviews
- Converting requirements into tables
- Identifying relationships
- Detecting missing entities
- Understanding cardinality
- Designing normalized schemas

---

# 3. Real-Time Example

Imagine designing an online shopping system.

The system contains:

~~~text
CUSTOMER
PRODUCT
ORDER
PAYMENT
```

Relationships:

~~~text
Customer
   |
places
   |
Order
```

~~~text
Order
   |
contains
   |
Product
```

~~~text
Order
   |
has
   |
Payment
```

Instead of immediately writing SQL tables, we can first create an ER diagram.

This gives us a high-level blueprint.

---

# 4. Main Components of an ER Diagram

An ER diagram commonly contains:

1. Entity
2. Attribute
3. Relationship
4. Key Attribute
5. Cardinality
6. Participation
7. Weak Entity
8. Identifying Relationship
9. Role Names
10. Composite Attributes
11. Multivalued Attributes
12. Derived Attributes

The most important basic symbols are:

~~~text
Rectangle
→ Entity

Oval
→ Attribute

Diamond
→ Relationship

Underlined Attribute
→ Key Attribute

Double Rectangle
→ Weak Entity

Double Diamond
→ Identifying Relationship
~~~

---

# 5. ER Diagram Symbol Cheat Sheet

| Symbol | Represents |
|---|---|
| Rectangle | Strong Entity |
| Double Rectangle | Weak Entity |
| Oval | Attribute |
| Underlined Oval/Attribute | Key Attribute |
| Double Oval | Multivalued Attribute |
| Dashed Oval | Derived Attribute |
| Diamond | Relationship |
| Double Diamond | Identifying Relationship |
| Double Line | Total Participation |
| Single Line | Partial Participation |

This symbol table is extremely important for exams.

---

# 6. Entity Symbol

An entity is generally represented using a rectangle.

Example:

~~~text
+-----------+
|  STUDENT  |
+-----------+
~~~

The rectangle represents the entity type.

Examples:

~~~text
STUDENT
EMPLOYEE
CUSTOMER
PRODUCT
COURSE
DEPARTMENT
~~~

---

# 7. Attribute Symbol

An attribute is generally represented using an oval.

Example:

~~~text
       (Name)
          |
+----------------+
|    STUDENT     |
+----------------+
```

Here:

~~~text
Student
→ Entity

Name
→ Attribute
~~~

---

# 8. Multiple Attributes

An entity can have multiple attributes.

Example:

~~~text
             (Student_ID)
                  |
(Name) ---- +-------------+ ---- (CGPA)
            |   STUDENT   |
            +-------------+
                  |
              (Email)
~~~

Attributes:

~~~text
Student_ID
Name
CGPA
Email
~~~

---

# 9. Key Attribute

A key attribute uniquely identifies an entity instance.

In traditional Chen ER notation, the key attribute is usually underlined.

Example:

~~~text
          (Student_ID)
               |
               |
        +-------------+
        |   STUDENT   |
        +-------------+
```

If:

~~~text
Student_ID
```

uniquely identifies every student, it is the key attribute.

---

# 10. Primary Key Concept

In the relational database, the corresponding attribute may become the primary key.

Example:

~~~text
STUDENT
----------------
Student_ID
Name
Email
CGPA
```

Possible primary key:

~~~text
Student_ID
~~~

Important distinction:

~~~text
ER Model
→ Key Attribute

Relational Model
→ Primary Key
~~~

---

# 11. Composite Attribute

A composite attribute can be divided into smaller meaningful attributes.

Example:

~~~text
Name
```

may consist of:

~~~text
First_Name
Middle_Name
Last_Name
~~~

Diagram concept:

~~~text
                 (First_Name)
                       \
                        \
(Name) ---------------- STUDENT
                        /
                       /
                (Last_Name)
~~~

Another example:

~~~text
Address
→ Street
→ City
→ State
→ ZIP
~~~

---

# 12. Composite Attribute Recognition

> [!important]
> If an attribute can be meaningfully divided into smaller attributes, think:
>
> **Composite Attribute**

Examples:

~~~text
Name
→ First_Name + Last_Name

Address
→ Street + City + State + ZIP

Date
→ Day + Month + Year
~~~

Do not confuse:

~~~text
Composite Attribute
```

with:

~~~text
Composite Key
```

They are different concepts.

---

# 13. Multivalued Attribute

A multivalued attribute can have multiple values for one entity instance.

It is commonly represented using a **double oval**.

Example:

~~~text
             ((Phone_Number))
                    |
              +-----------+
              | EMPLOYEE  |
              +-----------+
~~~

One employee may have:

~~~text
Phone 1
Phone 2
Phone 3
~~~

Therefore:

~~~text
Phone_Number
→ Multivalued Attribute
~~~

---

# 14. Real-Time Multivalued Examples

Possible examples:

~~~text
Employee
→ Multiple Phone Numbers

Student
→ Multiple Email Addresses

Person
→ Multiple Skills

Customer
→ Multiple Addresses
~~~

However, whether an attribute should be modeled as multivalued depends on the actual database requirements.

---

# 15. Derived Attribute

A derived attribute is calculated from other stored information.

It is commonly represented using a dashed oval.

Example:

~~~text
Date_of_Birth
       |
    derives
       |
      Age
```

`Age` can be calculated from:

~~~text
Current Date
-
Date of Birth
~~~

Therefore:

~~~text
Age
→ Derived Attribute
~~~

---

# 16. Real-Time Derived Attribute Examples

Examples:

~~~text
Date_of_Birth
→ Age
```

~~~text
Quantity × Unit_Price
→ Total_Price
```

~~~text
Joining_Date
→ Years_of_Service
```

~~~text
Date_of_Birth
→ Eligibility_Status
```

Derived values often do not need to be physically stored if they can be calculated reliably.

---

# 17. Attribute Type Master Table

| Attribute Type | Meaning | Common Symbol |
|---|---|---|
| Simple | Cannot be meaningfully divided | Single Oval |
| Composite | Can be divided | Oval with sub-attributes |
| Single-Valued | One value per entity | Single Oval |
| Multivalued | Multiple values | Double Oval |
| Stored | Physically stored | Normal Oval |
| Derived | Calculated | Dashed Oval |
| Key | Uniquely identifies entity | Underlined |

---

# 18. Relationship Symbol

A relationship is commonly represented by a diamond.

Example:

~~~text
+----------+       <ENROLLS>       +----------+
| STUDENT  |-----------------------|  COURSE  |
+----------+                       +----------+
~~~

In traditional Chen notation:

~~~text
+----------+       /---------\
| STUDENT  |------< ENROLLS >------| COURSE |
+----------+       \---------/
~~~

The relationship name should describe the association.

Examples:

~~~text
ENROLLS
WORKS_FOR
MANAGES
TEACHES
PLACES
CONTAINS
OWNS
~~~

---

# 19. Entity + Attribute + Relationship

A complete basic ER structure may look conceptually like:

~~~text
                    (Name)
                       |
                       |
+-------------+   <ENROLLS>   +-------------+
|   STUDENT   |---------------|   COURSE    |
+-------------+               +-------------+
      |
 (Student_ID)
~~~

Here:

~~~text
STUDENT
→ Entity

COURSE
→ Entity

ENROLLS
→ Relationship

Name
→ Attribute

Student_ID
→ Key Attribute
~~~

---

# 20. Cardinality in ER Diagram

Cardinality can be shown using notation such as:

~~~text
1:1
1:N
N:1
M:N
~~~

Example:

~~~text
DEPARTMENT
     |
     | 1:N
     |
  EMPLOYEE
~~~

Meaning:

~~~text
One Department
→ Many Employees
~~~

---

# 21. ER Diagram with 1:N

Conceptually:

~~~text
+-------------+       <HAS>       +-------------+
| DEPARTMENT  |-------------------|  EMPLOYEE   |
+-------------+       1 : N       +-------------+
~~~

Interpretation:

~~~text
Department
1
→
N Employees
~~~

---

# 22. ER Diagram with M:N

Example:

~~~text
+-------------+       <ENROLLS>       +-------------+
|   STUDENT   |-----------------------|   COURSE    |
+-------------+        M : N          +-------------+
~~~

Interpretation:

~~~text
One Student
→ Many Courses

One Course
→ Many Students
~~~

---

# 23. ER Diagram with 1:1

Example:

~~~text
+-------------+       <HAS>       +-------------+
|   PERSON    |-------------------|  PASSPORT   |
+-------------+       1 : 1       +-------------+
~~~

Under the stated business rules:

~~~text
One Person
→ One Passport

One Passport
→ One Person
~~~

---

# 24. Participation in ER Diagram

Participation tells whether every entity instance must participate.

Two types:

~~~text
Total Participation
Partial Participation
~~~

In traditional Chen notation:

~~~text
Double Line
→ Total Participation

Single Line
→ Partial Participation
~~~

---

# 25. Total Participation

Suppose:

> Every employee must belong to a department.

Conceptually:

~~~text
EMPLOYEE
  ||
  ||
WORKS_FOR
  |
DEPARTMENT
~~~

The double line indicates total participation of the relevant entity set.

Meaning:

~~~text
Every Employee
→ Must participate
~~~

---

# 26. Partial Participation

Suppose:

> Only some employees manage departments.

Conceptually:

~~~text
EMPLOYEE
  |
  |
MANAGES
  |
DEPARTMENT
~~~

Single line:

~~~text
→ Partial Participation
~~~

Meaning:

~~~text
Some Employees
→ Participate

Some Employees
→ Do Not Participate
~~~

---

# 27. Cardinality vs Participation in Diagram

This distinction is essential.

Cardinality:

~~~text
1:1
1:N
M:N
~~~

answers:

> How many?

Participation:

~~~text
Total
Partial
~~~

answers:

> Must it participate?

Example:

~~~text
DEPARTMENT
1:N
EMPLOYEE
~~~

and:

~~~text
Every Employee must belong to a Department
~~~

Therefore:

~~~text
Cardinality
→ 1:N

Employee Participation
→ Total
~~~

---

# 28. Weak Entity

A weak entity does not have a sufficient key of its own to uniquely identify its instances independently of its owner entity.

It is commonly represented using a double rectangle.

Example:

~~~text
+-------------+
|| DEPENDENT ||
+-------------+
~~~

Suppose a dependent is identified using:

~~~text
Employee_ID
+
Dependent_Name
~~~

The dependent depends on an employee.

---

# 29. Identifying Relationship

The relationship connecting a weak entity with its owner entity is called an identifying relationship.

It is commonly represented using a double diamond.

Conceptually:

~~~text
+-------------+       <<HAS>>       ||-------------||
|  EMPLOYEE   |---------------------||  DEPENDENT  ||
+-------------+                     ||-------------||
~~~

Here:

~~~text
EMPLOYEE
→ Strong / Owner Entity

DEPENDENT
→ Weak Entity

HAS
→ Identifying Relationship
~~~

---

# 30. Weak Entity Recognition

> [!important]
> If an entity:
>
> - Cannot be uniquely identified using its own attributes
> - Depends on another entity
> - Uses an owner key as part of its identification
>
> think:
>
> **Weak Entity**

Classic example:

~~~text
Employee
   |
has
   |
Dependent
~~~

---

# 31. Partial Key of Weak Entity

A weak entity can have a **partial key** that distinguishes weak-entity instances belonging to the same owner.

Example:

~~~text
Employee_ID
Dependent_Name
~~~

Suppose:

~~~text
Employee 101
→ Ravi

Employee 102
→ Ravi
~~~

`Dependent_Name` alone is not globally unique.

But:

~~~text
Employee_ID + Dependent_Name
```

may uniquely identify a dependent.

This is why weak entities depend on their owner entity.

---

# 32. Recursive Relationship in ER Diagram

A recursive relationship occurs when an entity participates in a relationship with itself.

Example:

~~~text
+-------------+
|  EMPLOYEE   |
+-------------+
       |
     MANAGES
       |
       ↺
   EMPLOYEE
~~~

More precisely, the same entity type participates in two roles:

~~~text
Manager
Employee
~~~

---

# 33. Role Names

Role names clarify how the same entity participates in a recursive relationship.

Example:

~~~text
EMPLOYEE
   |
 MANAGES
   |
EMPLOYEE
~~~

Roles:

~~~text
Manager
Subordinate
~~~

Without role names, the relationship may be ambiguous.

---

# 34. Composite Key in ER Diagram

A composite key contains multiple attributes that together uniquely identify an entity.

Example:

~~~text
ENROLLMENT
----------------
Student_ID
Course_ID
Semester
~~~

Possible key:

~~~text
Student_ID + Course_ID
~~~

depending on whether a student can enroll in the same course more than once.

Important:

~~~text
Composite Attribute
≠
Composite Key
~~~

---

# 35. Composite Attribute vs Composite Key

| Concept | Meaning |
|---|---|
| Composite Attribute | One attribute divided into components |
| Composite Key | Multiple attributes together identify a record |

Example:

~~~text
Address
→ Street + City + State
```

is a composite attribute.

Example:

~~~text
Student_ID + Course_ID
```

is a composite key.

---

# 36. ER Diagram Example — College Database

Suppose the requirements are:

> Students enroll in courses. Each student has a name and student ID. Each course has a course ID and course name. Students can enroll in multiple courses and each course can have multiple students.

Entities:

~~~text
STUDENT
COURSE
~~~

Attributes:

~~~text
STUDENT
→ Student_ID
→ Name

COURSE
→ Course_ID
→ Course_Name
~~~

Relationship:

~~~text
ENROLLS
~~~

Cardinality:

~~~text
M:N
~~~

Conceptual diagram:

~~~text
STUDENT
   |
 ENROLLS
   |
COURSE
~~~

Relationship attributes could include:

~~~text
Grade
Semester
Enrollment_Date
~~~

---

# 37. ER Diagram Example — Banking System

Requirements:

> Customers can own accounts. An account may be jointly owned by multiple customers.

Entities:

~~~text
CUSTOMER
ACCOUNT
~~~

Relationship:

~~~text
OWNS
~~~

Cardinality:

~~~text
M:N
~~~

Conceptual structure:

~~~text
CUSTOMER
   |
  OWNS
   |
ACCOUNT
```

Possible relationship attributes:

~~~text
Ownership_Date
Ownership_Type
~~~

This example demonstrates why business rules determine cardinality.

---

# 38. ER Diagram Example — Hospital

Entities:

~~~text
PATIENT
DOCTOR
~~~

Relationship:

~~~text
TREATS
~~~

Possible cardinality:

~~~text
M:N
~~~

Relationship attributes:

~~~text
Treatment_Date
Diagnosis
Notes
~~~

Conceptually:

~~~text
+-----------+       <TREATS>       +-----------+
|  DOCTOR   |----------------------|  PATIENT  |
+-----------+         M : N        +-----------+
```

---

# 39. ER Diagram Example — E-Commerce

Entities:

~~~text
CUSTOMER
ORDER
PRODUCT
~~~

Relationships:

~~~text
CUSTOMER
   |
 PLACES
   |
ORDER
```

~~~text
ORDER
   |
CONTAINS
   |
PRODUCT
~~~

Possible cardinalities:

~~~text
Customer
1:N
Order
```

~~~text
Order
M:N
Product
~~~

The M:N relationship can be represented using:

~~~text
ORDER_ITEM
~~~

---

# 40. ER Diagram Example — Company

Entities:

~~~text
EMPLOYEE
DEPARTMENT
PROJECT
```

Relationships:

~~~text
EMPLOYEE
   |
WORKS_FOR
   |
DEPARTMENT
```

~~~text
EMPLOYEE
   |
WORKS_ON
   |
PROJECT
```

Possible cardinalities:

~~~text
Department
1:N
Employee

Employee
M:N
Project
~~~

Relationship attributes:

~~~text
Hours_Worked
Role
Start_Date
~~~

---

# 41. ER Diagram Example — Library

Entities:

~~~text
MEMBER
BOOK
```

Relationship:

~~~text
BORROWS
```

Potential attributes:

~~~text
Issue_Date
Return_Date
Fine
```

Conceptually:

~~~text
MEMBER
   |
BORROWS
   |
BOOK
~~~

If a book can be borrowed many times by different members over time, the conceptual model must distinguish individual copies and/or loan transactions depending on the requirements.

This is a good example of why careful requirement analysis matters.

---

# 42. ER Diagram Construction Process

Use this workflow for any real-world problem.

~~~text
STEP 1
Read the requirements
        ↓
STEP 2
Identify nouns
        ↓
STEP 3
Candidate nouns become entities
        ↓
STEP 4
Identify properties
        ↓
STEP 5
Properties become attributes
        ↓
STEP 6
Identify verbs
        ↓
STEP 7
Verbs often become relationships
        ↓
STEP 8
Determine keys
        ↓
STEP 9
Determine cardinality
        ↓
STEP 10
Determine participation
        ↓
STEP 11
Identify weak entities
        ↓
STEP 12
Identify relationship attributes
        ↓
STEP 13
Validate the model
        ↓
STEP 14
Convert to relational schema
~~~

This is the most useful practical workflow.

---

# 43. Noun-Verb Recognition Trick

> [!tip]
> During requirement analysis:
>
> **Nouns → Candidate Entities**
>
> **Properties of nouns → Attributes**
>
> **Verbs connecting nouns → Candidate Relationships**

Example:

> A student enrolls in a course.

Nouns:

~~~text
Student
Course
~~~

Entities:

~~~text
STUDENT
COURSE
~~~

Verb:

~~~text
enrolls
~~~

Relationship:

~~~text
ENROLLS
~~~

This is a powerful database-design shortcut.

---

# 44. Example — Noun-Verb Analysis

Requirement:

> A customer places orders. Each order contains products.

Identify:

Nouns:

~~~text
Customer
Order
Product
~~~

Entities:

~~~text
CUSTOMER
ORDER
PRODUCT
~~~

Verbs:

~~~text
places
contains
~~~

Relationships:

~~~text
PLACES
CONTAINS
~~~

Possible cardinalities:

~~~text
Customer
1:N
Order

Order
M:N
Product
~~~

---

# 45. ER Diagram Validation Questions

After creating the diagram, ask:

~~~text
1. Does every important noun have a representation?

2. Does every important relationship have a representation?

3. Does every entity have a key?

4. Are relationship cardinalities correct?

5. Are optional relationships represented?

6. Are relationship attributes placed correctly?

7. Are weak entities identified correctly?

8. Are recursive relationships using role names?

9. Are derived values unnecessarily stored?

10. Does the model match the actual business rules?
~~~

---

# 46. Avoid Overloading Entities

Bad design:

~~~text
STUDENT
---------
Student_ID
Name
Course1
Course2
Course3
Course4
~~~

Why is this problematic?

Because course enrollment is a relationship between:

~~~text
Student
Course
~~~

Better conceptual model:

~~~text
STUDENT
   |
ENROLLS
   |
COURSE
~~~

with M:N cardinality.

---

# 47. Avoid Storing Repeating Groups

Bad:

~~~text
EMPLOYEE
---------
Employee_ID
Phone1
Phone2
Phone3
~~~

If the number of phone numbers is variable, this is usually a sign that the data should be modeled differently.

Conceptually:

~~~text
EMPLOYEE
   |
HAS_PHONE
   |
PHONE
~~~

or represented as a multivalued attribute at the conceptual level, depending on the modeling approach.

---

# 48. Avoid Incorrect Relationship Attributes

Suppose:

~~~text
STUDENT
   |
ENROLLS
   |
COURSE
~~~

`Student_Name` should not be an attribute of `ENROLLS`.

It belongs to:

~~~text
STUDENT
~~~

`Course_Name` belongs to:

~~~text
COURSE
~~~

But:

~~~text
Grade
Semester
Enrollment_Date
~~~

may belong to:

~~~text
ENROLLS
~~~

because they describe the specific association.

---

# 49. ER Diagram vs Database Table

An ER diagram is a conceptual model.

A table is part of the relational implementation.

Example:

ER:

~~~text
STUDENT
M:N
COURSE
~~~

Relational implementation:

~~~text
STUDENT
---------
Student_ID
Name
~~~

~~~text
COURSE
---------
Course_ID
Course_Name
~~~

~~~text
ENROLLMENT
---------
Student_ID
Course_ID
Grade
Semester
~~~

Therefore:

~~~text
ER Diagram
→ Conceptual Design

Tables
→ Relational Implementation
~~~

---

# 50. ER Diagram vs Relational Schema

| ER Diagram | Relational Schema |
|---|---|
| Entity | Table |
| Attribute | Column |
| Key Attribute | Primary Key |
| Relationship | Foreign Key / Junction Table / constraints |
| M:N Relationship | Junction Table |
| Cardinality | Constraints / schema design |
| Participation | NOT NULL / constraints / business logic |

This mapping is extremely useful for interviews.

---

# 51. Common Conversion Patterns

### Entity

~~~text
STUDENT
~~~

becomes:

~~~text
STUDENT(...)
~~~

### 1:N Relationship

~~~text
Department
1:N
Employee
~~~

becomes:

~~~text
Employee.Department_ID
→ Foreign Key
~~~

### M:N Relationship

~~~text
Student
M:N
Course
~~~

becomes:

~~~text
Enrollment(Student_ID, Course_ID)
~~~

### 1:1 Relationship

~~~text
Person
1:1
Passport
~~~

can become:

~~~text
Passport.Person_ID UNIQUE
~~~

depending on the design.

---

# 52. Important Interview Trick — Diagram to SQL

If an interviewer gives:

~~~text
DEPARTMENT
1:N
EMPLOYEE
~~~

Immediately think:

~~~sql
CREATE TABLE Department (
    Department_ID INT PRIMARY KEY
);

CREATE TABLE Employee (
    Employee_ID INT PRIMARY KEY,
    Department_ID INT,
    FOREIGN KEY (Department_ID)
        REFERENCES Department(Department_ID)
);
~~~

The key insight:

~~~text
1:N
→ FK on N-side
~~~

---

# 53. Important Interview Trick — M:N to SQL

If interviewer gives:

~~~text
STUDENT
M:N
COURSE
~~~

Immediately think:

~~~sql
CREATE TABLE Enrollment (
    Student_ID INT,
    Course_ID INT,
    PRIMARY KEY (Student_ID, Course_ID)
);
~~~

and:

~~~text
Student_ID
→ FK to Student

Course_ID
→ FK to Course
~~~

This is one of the highest-value DBMS interview patterns.

---

# 54. Important Interview Trick — 1:1 to SQL

If:

~~~text
PERSON
1:1
PASSPORT
~~~

possible design:

~~~sql
CREATE TABLE Passport (
    Passport_ID INT PRIMARY KEY,
    Person_ID INT UNIQUE,
    FOREIGN KEY (Person_ID)
        REFERENCES Person(Person_ID)
);
~~~

The important concept is:

~~~text
FOREIGN KEY
+
UNIQUE
→ helps enforce 1:1
~~~

---

# 55. ER Diagram and Normalization

ER modeling and normalization solve related but different problems.

ER modeling asks:

~~~text
What entities exist?
How are they related?
What constraints exist?
~~~

Normalization asks:

~~~text
How should relational data be organized
to reduce redundancy and anomalies?
~~~

Example:

~~~text
Student
M:N
Course
```

may become:

~~~text
Student
Course
Enrollment
```

This separation can improve relational design.

---

# 56. ER Diagram and Functional Dependency

Functional dependencies become especially important after conceptual modeling.

Example:

~~~text
Student_ID
→ Student_Name
```

This means:

~~~text
Student_ID
```

determines:

~~~text
Student_Name
```

But:

~~~text
Student_ID + Course_ID
→ Grade
```

because Grade may depend on a particular enrollment.

This connects ER modeling with normalization.

---

# 57. High-Level Design Thinking

A strong database designer does not start with:

~~~text
CREATE TABLE
~~~

Instead:

~~~text
Requirements
↓
Conceptual Model
↓
ER Diagram
↓
Logical Relational Model
↓
Normalization
↓
Physical Design
↓
Indexes / Performance
↓
SQL Implementation
~~~

This is the professional database-design pipeline.

---

# 58. Common Exam Question — Identify Symbols

### Question

Which symbol represents an entity in the traditional ER model?

### Answer

~~~text
Rectangle
~~~

---

# 59. Common Exam Question — Attribute

### Question

Which symbol represents an attribute?

### Answer

~~~text
Oval
~~~

---

# 60. Common Exam Question — Relationship

### Question

Which symbol represents a relationship?

### Answer

~~~text
Diamond
~~~

---

# 61. Common Exam Question — Multivalued Attribute

### Question

Which symbol represents a multivalued attribute?

### Answer

~~~text
Double Oval
~~~

---

# 62. Common Exam Question — Derived Attribute

### Question

Which symbol represents a derived attribute?

### Answer

~~~text
Dashed Oval
~~~

---

# 63. Common Exam Question — Weak Entity

### Question

Which symbol represents a weak entity?

### Answer

~~~text
Double Rectangle
~~~

---

# 64. Common Exam Question — Identifying Relationship

### Question

Which symbol traditionally represents an identifying relationship?

### Answer

~~~text
Double Diamond
~~~

---

# 65. Common Exam Question — Total Participation

### Question

What does a double line between an entity and relationship generally indicate in Chen notation?

### Answer

~~~text
Total Participation
~~~

Meaning:

~~~text
Every entity instance must participate.
~~~

---

# 66. Common Exam Question — Key Attribute

### Question

How is a key attribute commonly represented in a Chen ER diagram?

### Answer

~~~text
Underlined Attribute
~~~

---

# 67. Common Interview Question — What Is ER Modeling?

### Strong Answer

> ER modeling is a conceptual database-design technique used to represent entities, their attributes, relationships, and constraints before implementing the database.

---

# 68. Common Interview Question — Why Use ER Diagrams?

### Strong Answer

> ER diagrams provide a visual representation of database requirements. They help identify entities, relationships, cardinalities, constraints, and missing requirements before implementing tables.

---

# 69. Common Interview Question — Entity vs Attribute

### Answer

~~~text
Entity
→ Independent object

Attribute
→ Property of an entity
~~~

Example:

~~~text
STUDENT
→ Entity

Student_Name
→ Attribute
~~~

---

# 70. Common Interview Question — Entity vs Relationship

### Answer

~~~text
Entity
→ Object

Relationship
→ Association between objects
~~~

Example:

~~~text
STUDENT
→ Entity

COURSE
→ Entity

ENROLLS
→ Relationship
~~~

---

# 71. Common Interview Question — Composite Attribute

### Answer

> A composite attribute can be divided into smaller meaningful attributes.

Example:

~~~text
Address
→ Street
→ City
→ State
→ ZIP
~~~

---

# 72. Common Interview Question — Multivalued Attribute

### Answer

> A multivalued attribute can contain multiple values for one entity instance.

Example:

~~~text
Employee
→ Multiple Phone Numbers
~~~

---

# 73. Common Interview Question — Derived Attribute

### Answer

> A derived attribute is calculated from other stored attributes or data.

Example:

~~~text
Date_of_Birth
→ Age
~~~

---

# 74. Common Interview Question — Weak Entity

### Strong Answer

> A weak entity cannot be uniquely identified independently using only its own attributes and depends on an owner entity for identification.

Example:

~~~text
Employee
→ Dependent
~~~

---

# 75. Common Interview Question — ER Diagram and SQL

### Question

Why do we create ER diagrams before tables?

### Answer

> Because the ER diagram captures the conceptual structure and business rules first. It allows us to validate entities, attributes, relationships, and cardinality before implementing the relational schema.

---

# 76. Advanced Interview Question — M:N

### Question

Why can't a standard relational table directly represent M:N without an additional structure?

### Answer

A many-to-many relationship is generally represented using an associative/junction table.

Example:

~~~text
Student
M:N
Course
```

becomes:

~~~text
Enrollment
---------
Student_ID
Course_ID
~~~

This converts the M:N relationship into two 1:N relationships.

---

# 77. M:N Transformation

Original:

~~~text
STUDENT
       M:N
        |
      COURSE
~~~

After transformation:

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

This is a very important conceptual transformation.

---

# 78. Interview Trick — M:N Becomes Two 1:N

> [!important]
> When an M:N relationship is converted into an associative entity:
>
> ```text
> A M:N B
> ```
>
> becomes:
>
> ```text
> A 1:N AssociativeEntity
>
> AssociativeEntity N:1 B
> ```

Example:

~~~text
Student
M:N
Course
~~~

becomes:

~~~text
Student
1:N
Enrollment
N:1
Course
~~~

---

# 79. Advanced Real-Time Example — Food Delivery

Entities:

~~~text
CUSTOMER
RESTAURANT
ORDER
DELIVERY_PARTNER
```

Relationships:

~~~text
Customer
1:N
Order
```

~~~text
Restaurant
1:N
Order
```

~~~text
Delivery_Partner
1:N
Order
```

depending on business rules.

A detailed design may also include:

~~~text
ORDER_ITEM
```

for:

~~~text
Order
M:N
Menu_Item
~~~

This demonstrates how real systems use multiple ER patterns together.

---

# 80. Advanced Real-Time Example — YouTube-Like Platform

Entities:

~~~text
USER
VIDEO
CHANNEL
COMMENT
```

Possible relationships:

~~~text
User
1:N
Video
```

~~~text
Channel
1:N
Video
```

~~~text
User
1:N
Comment
```

~~~text
Video
1:N
Comment
```

Additional relationships:

~~~text
User
M:N
Video
```

for likes, subscriptions, or playlists depending on the exact model.

The key lesson:

> A real system usually contains many different cardinality patterns simultaneously.

---

# 81. Advanced Real-Time Example — University

Entities:

~~~text
STUDENT
DEPARTMENT
COURSE
FACULTY
PROJECT
```

Relationships:

~~~text
Department
1:N
Student
```

~~~text
Department
1:N
Faculty
```

~~~text
Student
M:N
Course
```

~~~text
Faculty
1:N
Course
```

~~~text
Student
M:N
Project
```

Possible relationship attributes:

~~~text
Enrollment:
Grade
Semester

Project:
Role
Start_Date
Hours_Worked
~~~

This is a strong practice model.

---

# 82. How to Read an ER Diagram Quickly

During an exam or interview, scan in this order:

~~~text
1. Find rectangles
   ↓
   Entities

2. Find ovals
   ↓
   Attributes

3. Find underlined attributes
   ↓
   Keys

4. Find diamonds
   ↓
   Relationships

5. Check numbers
   ↓
   Cardinality

6. Check single/double lines
   ↓
   Participation

7. Check double rectangles
   ↓
   Weak entities

8. Check double ovals
   ↓
   Multivalued attributes

9. Check dashed ovals
   ↓
   Derived attributes
~~~

This is an excellent exam-scanning strategy.

---

# 83. Fast Symbol Memory Trick

> [!tip]
> Remember:
>
> ```text
> Rectangle
> → Entity
>
> Oval
> → Attribute
>
> Diamond
> → Relationship
>
> Double Rectangle
> → Weak Entity
>
> Double Oval
> → Multivalued Attribute
>
> Dashed Oval
> → Derived Attribute
>
> Underline
> → Key
>
> Double Line
> → Total Participation
> ```

---

# 84. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing Entity and Relationship

~~~text
Student
→ Entity

Enrolls
→ Relationship
~~~

Do not represent `ENROLLS` as an entity unless the domain requires it to be modeled as an associative entity with its own identity and attributes.

---

### Mistake 2 — Confusing Attribute and Entity

Example:

~~~text
Student
Name
~~~

`Name` is normally an attribute, not an entity.

---

### Mistake 3 — Treating Every Noun as an Entity

A noun may be:

~~~text
Entity
Attribute
Relationship-related concept
```

You must analyze its role in the requirements.

---

### Mistake 4 — Ignoring Cardinality

An ER diagram without correct cardinality may fail to represent the business rules.

Always ask:

~~~text
One A → ?
One B → ?
~~~

---

### Mistake 5 — Ignoring Participation

Cardinality alone may not tell whether participation is mandatory.

Example:

~~~text
(0,N)
```

is different from:

~~~text
(1,N)
~~~

---

### Mistake 6 — Treating Derived Data as Mandatory Stored Data

Example:

~~~text
Date_of_Birth
→ Age
~~~

Age can usually be calculated.

Do not automatically store every derived value.

---

### Mistake 7 — Confusing Composite Attribute with Composite Key

~~~text
Address
→ Street + City
```

is composite attribute.

~~~text
Student_ID + Course_ID
```

can be composite key.

---

### Mistake 8 — Forgetting Weak Entity Dependency

A weak entity cannot normally be identified independently from its owner.

---

### Mistake 9 — Incorrect M:N Conversion

Do not simply put one foreign key into either entity table and assume that represents arbitrary many-to-many associations.

Use a junction/associative table.

---

### Mistake 10 — Ignoring Business Requirements

Do not decide:

~~~text
1:1
1:N
M:N
```

from intuition alone.

Requirements determine the relationship.

---

# 85. Common Exam Patterns

> [!important] Must Master

1. Identify entity symbols
2. Identify attribute symbols
3. Identify relationship symbols
4. Identify key attributes
5. Identify weak entities
6. Identify identifying relationships
7. Identify multivalued attributes
8. Identify derived attributes
9. Identify composite attributes
10. Identify cardinality
11. Identify participation
12. Read an ER diagram
13. Convert requirements to ER diagram
14. Convert ER diagram to relational schema
15. Determine foreign key placement
16. Convert M:N to junction table
17. Identify relationship attributes
18. Identify recursive relationships
19. Identify role names
20. Distinguish entity vs attribute
21. Distinguish entity vs relationship
22. Distinguish composite attribute vs composite key
23. Determine total vs partial participation
24. Identify weak entity dependency
25. Map ER design to SQL

---

# 86. Interview Questions

## Q1. What is an ER diagram?

### Strong Answer

> An ER diagram is a graphical representation of entities, attributes, relationships, and constraints used to model the conceptual structure of a database.

---

# 87. Interview Question — Why ER Diagram?

## Q2. Why do we use ER diagrams?

### Answer

> ER diagrams help translate business requirements into a visual database model before creating actual tables. They make relationships, cardinality, constraints, and missing requirements easier to identify.

---

# 88. Interview Question — Main Components

## Q3. What are the main components of an ER diagram?

### Answer

The main components are:

~~~text
Entities
Attributes
Relationships
Keys
Cardinality
Participation
~~~

Advanced diagrams may also contain:

~~~text
Weak Entities
Composite Attributes
Multivalued Attributes
Derived Attributes
Specialization
Generalization
~~~

---

# 89. Interview Question — Symbols

## Q4. What are the common ER diagram symbols?

### Answer

~~~text
Rectangle
→ Entity

Oval
→ Attribute

Diamond
→ Relationship

Double Rectangle
→ Weak Entity

Double Oval
→ Multivalued Attribute

Dashed Oval
→ Derived Attribute

Underlined Attribute
→ Key
~~~

---

# 90. Interview Question — Weak Entity

## Q5. What is a weak entity?

### Answer

> A weak entity is an entity that cannot be uniquely identified using only its own attributes and depends on an owner entity for identification.

---

# 91. Interview Question — Composite Attribute

## Q6. What is a composite attribute?

### Answer

> A composite attribute is an attribute that can be divided into smaller meaningful attributes.

Example:

~~~text
Address
→ Street
→ City
→ State
→ ZIP
~~~

---

# 92. Interview Question — Multivalued Attribute

## Q7. What is a multivalued attribute?

### Answer

> A multivalued attribute can contain multiple values for a single entity instance.

Example:

~~~text
Employee
→ Multiple Phone Numbers
~~~

---

# 93. Interview Question — Derived Attribute

## Q8. What is a derived attribute?

### Answer

> A derived attribute is calculated from other data.

Example:

~~~text
Date_of_Birth
→ Age
~~~

---

# 94. Interview Question — ER Diagram to Tables

## Q9. How do you convert an ER diagram into relational tables?

### Strong Answer

Use these general rules:

~~~text
Strong Entity
→ Table

Attribute
→ Column

Key Attribute
→ Primary Key

1:N
→ FK generally on N-side

M:N
→ Junction Table

1:1
→ FK on an appropriate side + UNIQUE if required

Weak Entity
→ Table including owner key
~~~

---

# 95. Interview Question — M:N Conversion

## Q10. How do you convert an M:N relationship?

### Answer

Create an associative/junction table.

Example:

~~~text
Student
M:N
Course
~~~

becomes:

~~~text
Enrollment
---------
Student_ID
Course_ID
~~~

Relationship attributes can also be stored there.

---

# 96. Interview Question — ER Diagram vs Schema

## Q11. What is the difference between ER diagram and relational schema?

### Answer

~~~text
ER Diagram
→ Conceptual representation

Relational Schema
→ Logical table-based representation
~~~

ER diagrams focus on entities and relationships.

Relational schemas focus on tables, columns, keys, and constraints.

---

# 97. Advanced Interview Question

## Q12. Can an attribute become an entity?

### Answer

Yes, depending on the requirements.

For example, initially:

~~~text
Employee
→ Phone_Number
```

If phone numbers need their own properties or relationships:

~~~text
Employee
   |
HAS_PHONE
   |
Phone
~~~

Then `Phone` may be modeled as a separate entity.

The correct model depends on business requirements.

---

# 98. Advanced Interview Question

## Q13. When should a relationship become an associative entity?

### Answer

A relationship is often represented as an associative entity when:

- It is M:N.
- The relationship has several attributes.
- It needs its own identity or lifecycle.
- It participates in other relationships.

Example:

~~~text
Student
M:N
Course
```

becomes:

~~~text
Enrollment
```

with:

~~~text
Grade
Semester
Enrollment_Date
~~~

---

# 99. Advanced Interview Question

## Q14. Why is cardinality important in an ER diagram?

### Answer

> Cardinality captures an important business rule about how many instances can participate in a relationship. It also influences how the relationship is implemented using foreign keys, junction tables, and constraints.

---

# 100. Advanced Interview Question

## Q15. Why is participation important?

### Answer

> Participation specifies whether an entity must participate in a relationship or whether participation is optional.

Example:

~~~text
Every Employee must belong to Department
→ Total participation

Some Employee may manage Department
→ Partial participation
~~~

---

# 101. IIT-Level Problem-Solving Framework

When given a long database problem, do not randomly draw boxes.

Use:

~~~text
REQUIREMENTS
     ↓
NOUNS
     ↓
CANDIDATE ENTITIES
     ↓
PROPERTIES
     ↓
ATTRIBUTES
     ↓
VERBS
     ↓
RELATIONSHIPS
     ↓
KEYS
     ↓
CARDINALITY
     ↓
PARTICIPATION
     ↓
RELATIONSHIP ATTRIBUTES
     ↓
WEAK ENTITIES
     ↓
VALIDATE
     ↓
RELATIONAL SCHEMA
     ↓
SQL
~~~

This turns a complicated database question into a systematic process.

---

# 102. Full Worked Example — University System

## Requirement

> A university has departments. Each department offers many courses. Students belong to departments and can enroll in many courses. A course can have many students. Each enrollment stores grade and semester.

---

## Step 1 — Identify Entities

Nouns:

~~~text
University
Department
Course
Student
Grade
Semester
~~~

Candidate entities:

~~~text
UNIVERSITY
DEPARTMENT
COURSE
STUDENT
~~~

`Grade` and `Semester` are likely relationship attributes.

---

## Step 2 — Identify Relationships

Verbs:

~~~text
has
offers
belongs_to
enrolls
~~~

Relationships:

~~~text
UNIVERSITY
→ has
→ DEPARTMENT

DEPARTMENT
→ offers
→ COURSE

STUDENT
→ belongs_to
→ DEPARTMENT

STUDENT
→ enrolls
→ COURSE
~~~

---

## Step 3 — Determine Cardinality

University:

~~~text
University
1:N
Department
~~~

Department:

~~~text
Department
1:N
Course
~~~

Student:

~~~text
Department
1:N
Student
~~~

Enrollment:

~~~text
Student
M:N
Course
~~~

---

## Step 4 — Relationship Attributes

Enrollment-specific data:

~~~text
Grade
Semester
~~~

Therefore:

~~~text
ENROLLS
→ Grade
→ Semester
~~~

---

## Step 5 — Conceptual Structure

~~~text
UNIVERSITY
    |
   1:N
    |
DEPARTMENT
   /      \
 1:N      1:N
 /          \
COURSE     STUDENT
   \          /
    \        /
       M:N
      ENROLLS
~~~

This is the type of thinking expected in database-design interviews.

---

# 103. Full Worked Example — E-Commerce

## Requirement

> A customer can place many orders. Each order belongs to one customer. An order contains multiple products, and a product can appear in multiple orders. The quantity and price for each product in an order must be stored.

### Entities

~~~text
CUSTOMER
ORDER
PRODUCT
~~~

### Relationships

~~~text
CUSTOMER
→ PLACES
→ ORDER

ORDER
→ CONTAINS
→ PRODUCT
~~~

### Cardinality

~~~text
Customer
1:N
Order

Order
M:N
Product
~~~

### Relationship Attributes

~~~text
Quantity
Price
~~~

### Associative Entity

~~~text
ORDER_ITEM
~~~

Possible structure:

~~~text
ORDER_ITEM
----------------
Order_ID
Product_ID
Quantity
Price
~~~

This is a classic real-world ER design.

---

# 104. Full Worked Example — Employee System

## Requirement

> Every employee works for one department. A department can have many employees. Employees can work on multiple projects. Projects can have multiple employees. The system stores the number of hours an employee works on each project.

### Entities

~~~text
EMPLOYEE
DEPARTMENT
PROJECT
~~~

### Relationships

~~~text
EMPLOYEE
→ WORKS_FOR
→ DEPARTMENT

EMPLOYEE
→ WORKS_ON
→ PROJECT
~~~

### Cardinality

~~~text
Department
1:N
Employee

Employee
M:N
Project
~~~

### Relationship Attribute

~~~text
Hours_Worked
~~~

Because:

~~~text
Employee + Project
→ Hours_Worked
~~~

---

# 105. Full Worked Example — Hospital

## Requirement

> Doctors treat patients. A doctor can treat many patients, and a patient can be treated by many doctors. The hospital records treatment date and diagnosis.

### Entities

~~~text
DOCTOR
PATIENT
~~~

### Relationship

~~~text
TREATS
~~~

### Cardinality

~~~text
M:N
~~~

### Relationship Attributes

~~~text
Treatment_Date
Diagnosis
~~~

Possible associative entity:

~~~text
TREATMENT
---------
Doctor_ID
Patient_ID
Treatment_Date
Diagnosis
~~~

This is a very common real-world pattern.

---

# 106. Diagram Reading Strategy for MCQs

If an exam gives a large ER diagram:

### First

Find rectangles.

~~~text
→ Entities
~~~

### Second

Find diamonds.

~~~text
→ Relationships
~~~

### Third

Find underlined attributes.

~~~text
→ Keys
~~~

### Fourth

Find numbers:

~~~text
1
N
M
~~~

~~~text
→ Cardinality
~~~

### Fifth

Find double lines.

~~~text
→ Total Participation
~~~

### Sixth

Find double rectangles.

~~~text
→ Weak Entities
~~~

### Seventh

Find double ovals.

~~~text
→ Multivalued Attributes
~~~

This sequence saves time.

---

# 107. Exam Shortcut — Symbol Matching

> [!tip]
> Memorize the visual hierarchy:
>
> ```text
> BOX
> → Entity
>
> OVAL
> → Attribute
>
> DIAMOND
> → Relationship
>
> DOUBLE BOX
> → Weak Entity
>
> DOUBLE OVAL
> → Multivalued Attribute
>
> DASHED OVAL
> → Derived Attribute
>
> UNDERLINE
> → Key
>
> DOUBLE LINE
> → Total Participation
> ```

---

# 108. Exam Shortcut — Requirement to ER Diagram

> [!tip]
> Use:
>
> ```text
> Nouns
> → Entities
>
> Adjectives / properties
> → Attributes
>
> Verbs
> → Relationships
>
> Numbers / words like many, one
> → Cardinality
>
> Every / must
> → Total participation
>
> May / optional
> → Partial participation
> ```

This is not an absolute grammar rule, but it is an excellent starting heuristic.

---

# 109. Common Exam Traps

> [!warning] High-Frequency Traps

### Trap 1

`M:N` does not mean ternary.

Correct:

~~~text
Student M:N Course
→ Binary relationship
```

because there are two entity types.

---

### Trap 2

`1:N` does not mean two entities.

It describes cardinality, not degree.

---

### Trap 3

A double oval is not a weak entity.

~~~text
Double Oval
→ Multivalued Attribute

Double Rectangle
→ Weak Entity
~~~

---

### Trap 4

A dashed oval is not a key.

~~~text
Dashed Oval
→ Derived Attribute
~~~

---

### Trap 5

Underline does not mean relationship.

~~~text
Underline
→ Key Attribute
~~~

---

### Trap 6

Double diamond is not total participation.

~~~text
Double Diamond
→ Identifying Relationship

Double Line
→ Total Participation
~~~

---

### Trap 7

An attribute is not automatically stored.

Derived attributes may be calculated.

---

### Trap 8

A relationship does not automatically become a table in every case.

Implementation depends on:

~~~text
Cardinality
Attributes
Keys
Business Rules
~~~

---

# 110. Master Comparison Table

| Concept | Question to Ask | Example |
|---|---|---|
| Entity | What object exists? | Student |
| Attribute | What property does it have? | Name |
| Relationship | How are objects connected? | Enrolls |
| Key | How is it uniquely identified? | Student_ID |
| Degree | How many entity types? | Binary |
| Cardinality | How many instances? | M:N |
| Participation | Is participation mandatory? | Total |
| Weak Entity | Does it depend on an owner? | Dependent |
| Composite Attribute | Can it be split? | Address |
| Multivalued Attribute | Can it have multiple values? | Phone |
| Derived Attribute | Can it be calculated? | Age |
| Role | What role does the entity play? | Manager |

---

# 111. Formula Sheet

~~~text
ER DIAGRAM
→ Visual representation of database requirements.


MAIN SYMBOLS

Rectangle
→ Entity

Oval
→ Attribute

Diamond
→ Relationship

Double Rectangle
→ Weak Entity

Double Diamond
→ Identifying Relationship

Double Oval
→ Multivalued Attribute

Dashed Oval
→ Derived Attribute

Underlined Attribute
→ Key Attribute

Double Line
→ Total Participation

Single Line
→ Partial Participation


CARDINALITY

1:1
→ One-to-One

1:N
→ One-to-Many

N:1
→ Many-to-One

M:N
→ Many-to-Many


ATTRIBUTE TYPES

Simple
→ Cannot be meaningfully divided

Composite
→ Can be divided

Single-Valued
→ One value

Multivalued
→ Multiple values

Stored
→ Physically stored

Derived
→ Calculated


M:N MAPPING

A M:N B
→ Associative/Junction Entity

A 1:N B
→ FK generally on N-side

1:1
→ FK on appropriate side
→ UNIQUE when needed


DESIGN PIPELINE

Requirements
→ Entities
→ Attributes
→ Relationships
→ Keys
→ Cardinality
→ Participation
→ Validation
→ Relational Schema
→ SQL
~~~

---

# 112. Quick Revision

> [!summary] One-Minute Revision

~~~text
ER DIAGRAM
→ Visual blueprint of a database.


CORE COMPONENTS

Entity
→ Rectangle

Attribute
→ Oval

Relationship
→ Diamond

Key
→ Underlined Attribute

Weak Entity
→ Double Rectangle

Multivalued Attribute
→ Double Oval

Derived Attribute
→ Dashed Oval

Identifying Relationship
→ Double Diamond

Total Participation
→ Double Line


ATTRIBUTE TYPES

Simple
→ Cannot be divided

Composite
→ Can be divided

Single-Valued
→ One value

Multivalued
→ Multiple values

Derived
→ Calculated


CARDINALITY

1:1
→ One-to-One

1:N
→ One-to-Many

N:1
→ Many-to-One

M:N
→ Many-to-Many


FAST DESIGN METHOD

Nouns
→ Candidate Entities

Properties
→ Attributes

Verbs
→ Relationships

Unique identifier
→ Key

One / Many
→ Cardinality

Every / Must
→ Total Participation

May / Optional
→ Partial Participation


RELATIONAL MAPPING

Entity
→ Table

Attribute
→ Column

Key
→ Primary Key

1:N
→ FK on N-side

M:N
→ Junction Table

1:1
→ FK + UNIQUE when required


M:N EXAMPLE

Student
M:N
Course

↓

Enrollment
Student_ID
Course_ID
Grade
Semester


MOST IMPORTANT DISTINCTIONS

Entity
→ Object

Attribute
→ Property

Relationship
→ Connection

Degree
→ Number of Entity Types

Cardinality
→ Number of Instances

Participation
→ Mandatory or Optional


MASTER WORKFLOW

Requirements
↓
Entities
↓
Attributes
↓
Relationships
↓
Keys
↓
Cardinality
↓
Participation
↓
Relationship Attributes
↓
Validation
↓
Relational Schema
↓
SQL
~~~

---

# 113. Golden Memory Trick

**ER Diagram = Database Blueprint: Box the objects, oval their properties, diamond their connections, underline their keys, and mark how many and whether participation is required.**

# 114. One-Line Recognition

**Whenever you are given a real-world database requirement and asked to visualize its entities, attributes, relationships, keys, and constraints, use an ER Diagram.**