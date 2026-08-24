---
type: concept
subject: dbms
topic: "Relationship"
parent: "ER Model"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - er-model
  - relationship
  - relationship-set
  - relationship-type
  - cardinality
  - participation
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
  - "[[Cardinality]]"
  - "[[ER Diagram]]"
  - "[[Relational Model]]"
  - "[[Primary Key]]"
  - "[[Foreign Key]]"
---

# Relationship

## 1. Core Concept

> [!summary]
> A **Relationship** represents an association or connection between two or more entities in an ER model.

Simple idea:

~~~text
ENTITY
   +
ENTITY
   ↓
RELATIONSHIP
~~~

Example:

~~~text
STUDENT
    |
  enrolls
    |
  COURSE
~~~

Here:

~~~text
Student
→ Entity

Course
→ Entity

Enrolls
→ Relationship
~~~

The relationship answers:

> **"How are these entities connected?"**

---

# 2. Basic Meaning

Consider a college database.

We have:

~~~text
Student
Course
Professor
Department
~~~

Simply knowing that these entities exist is not enough.

We also need to represent:

~~~text
Student → enrolls in → Course

Professor → teaches → Course

Student → belongs to → Department

Professor → works in → Department
~~~

The words:

~~~text
enrolls
teaches
belongs to
works in
~~~

represent relationships.

---

# 3. Entity vs Relationship vs Attribute

This is one of the most important ER-model concepts.

Consider:

~~~text
Student
   |
enrolls in
   |
Course
~~~

Here:

~~~text
Student
→ Entity

Course
→ Entity

enrolls in
→ Relationship
~~~

Now:

~~~text
Student
---------
Student_ID
Name
CGPA
~~~

Here:

~~~text
Student_ID
Name
CGPA
→ Attributes
~~~

Memory:

~~~text
ENTITY
→ Object

ATTRIBUTE
→ Property

RELATIONSHIP
→ Connection
~~~

---

# 4. Relationship Recognition Trick

> [!important]
> Ask:
>
> **"What action or association connects these entities?"**
>
> The answer is usually the relationship.

Example:

~~~text
Customer places Order
~~~

Therefore:

~~~text
Customer
→ Entity

Order
→ Entity

Places
→ Relationship
~~~

Another:

~~~text
Doctor treats Patient
~~~

Therefore:

~~~text
Doctor
→ Entity

Patient
→ Entity

Treats
→ Relationship
~~~

---

# 5. Relationship Type

A **relationship type** describes the general association between entity types.

Example:

~~~text
STUDENT
   |
ENROLLS
   |
COURSE
~~~

`ENROLLS` is the relationship type.

It describes the general rule:

~~~text
Student can enroll in Course
~~~

---

# 6. Relationship Instance

A **relationship instance** represents one specific occurrence of a relationship.

Suppose:

~~~text
Student 101
enrolls in
Course CSE101
~~~

This specific connection is a relationship instance.

Think:

~~~text
Relationship Type
→ General Definition

Relationship Instance
→ Specific Connection
~~~

---

# 7. Relationship Set

A **relationship set** is a collection of relationship instances of the same relationship type.

Example:

~~~text
STUDENT
   |
ENROLLS
   |
COURSE
~~~

Instances:

~~~text
Student 101 → CSE101
Student 101 → DBMS01
Student 102 → CSE101
Student 103 → OS101
~~~

Together these connections form the relationship set.

---

# 8. Relationship Type vs Relationship Set vs Instance

| Concept | Meaning | Example |
|---|---|---|
| Relationship Type | General association | ENROLLS |
| Relationship Instance | One specific association | Student 101 enrolls in CSE101 |
| Relationship Set | Collection of instances | All student-course enrollments |

Memory:

~~~text
TYPE
→ Definition

INSTANCE
→ One occurrence

SET
→ Collection
~~~

---

# 9. Relationship Degree

The **degree of a relationship** refers to the number of participating entity types.

Important relationship degrees include:

1. Unary
2. Binary
3. Ternary
4. N-ary

This is a very important exam topic.

---

# 10. Unary Relationship

A **unary relationship** involves one entity type.

It is also called a **recursive relationship**.

Example:

~~~text
EMPLOYEE
   |
manages
   ↺
EMPLOYEE
~~~

The same entity type participates twice in different roles.

Example:

~~~text
Employee
   |
manages
   |
Employee
~~~

One employee manages another employee.

Therefore:

~~~text
Degree = 1
→ Unary
~~~

---

# 11. Real-Time Example — Employee Management

Suppose:

~~~text
Employee A
   |
 manages
   ↓
Employee B
~~~

Both are instances of:

~~~text
EMPLOYEE
~~~

The relationship is:

~~~text
MANAGES
~~~

Because the same entity type participates:

~~~text
EMPLOYEE
↕
EMPLOYEE
~~~

This is a unary relationship.

---

# 12. Role Names in Unary Relationships

A unary relationship often needs **role names** to distinguish the different roles played by the same entity type.

Example:

~~~text
EMPLOYEE
   |
  manages
   |
EMPLOYEE
~~~

Roles:

~~~text
Manager
Employee
~~~

Both are instances of `EMPLOYEE`, but they play different roles.

This is an important interview concept.

---

# 13. Binary Relationship

A **binary relationship** involves two entity types.

Example:

~~~text
STUDENT
   |
enrolls
   |
COURSE
~~~

Entity types:

~~~text
Student
Course
~~~

Therefore:

~~~text
Degree = 2
→ Binary Relationship
~~~

Binary relationships are extremely common.

---

# 14. Real-Time Binary Examples

~~~text
Customer
   |
places
   |
Order
~~~

~~~text
Doctor
   |
treats
   |
Patient
~~~

~~~text
Employee
   |
works_for
   |
Department
~~~

~~~text
Student
   |
enrolls
   |
Course
~~~

All are binary relationships.

---

# 15. Ternary Relationship

A **ternary relationship** involves three entity types.

Example:

~~~text
Supplier
    \
     \
    Supplies
     /   \
    /     \
Product   Project
~~~

The relationship may represent:

> Supplier supplies a particular product to a particular project.

Entity types:

~~~text
Supplier
Product
Project
~~~

Therefore:

~~~text
Degree = 3
→ Ternary Relationship
~~~

---

# 16. N-ary Relationship

An **N-ary relationship** involves more than three entity types.

Example:

~~~text
Entity A
    \
Entity B ---- Relationship
    /
Entity C
    \
   Entity D
~~~

If four entity types participate:

~~~text
Degree = 4
~~~

This is an n-ary relationship.

---

# 17. Relationship Degree Table

| Degree | Name | Example |
|---:|---|---|
| 1 | Unary | Employee manages Employee |
| 2 | Binary | Student enrolls Course |
| 3 | Ternary | Supplier supplies Product to Project |
| >3 | N-ary | Multiple entity types participate |

Shortcut:

~~~text
1 → Unary
2 → Binary
3 → Ternary
4+ → N-ary
~~~

---

# 18. Most Important Exam Trick

> [!tip]
> **Relationship Degree = Number of Entity Types Participating**
>
> Not:
>
> - Number of attributes
> - Number of records
> - Number of relationship instances

Example:

~~~text
Student
   |
enrolls
   |
Course
~~~

Two entity types participate.

Therefore:

~~~text
Degree = 2
~~~

---

# 19. Cardinality

**Cardinality** describes how many instances of one entity can be associated with instances of another entity.

For binary relationships, common cardinalities are:

~~~text
1 : 1
1 : N
N : 1
M : N
~~~

These are extremely important.

---

# 20. One-to-One Relationship

A **1:1 relationship** means one entity instance can be associated with at most one entity instance on the other side, and vice versa, under the stated constraints.

Example:

~~~text
PERSON
   |
has
   |
PASSPORT
~~~

Conceptually:

~~~text
One Person
→ One Passport

One Passport
→ One Person
~~~

This is a one-to-one relationship if the business rules enforce that mapping.

---

# 21. Real-Time 1:1 Example

Consider:

~~~text
Employee
   |
assigned
   |
Locker
~~~

If each employee receives at most one locker and each locker belongs to at most one employee:

~~~text
Employee
1 : 1
Locker
~~~

Again, actual cardinality depends on business rules.

---

# 22. One-to-Many Relationship

A **1:N relationship** means one entity instance can be associated with many instances of another entity type, while each instance on the many side is associated with one entity on the one side under the stated relationship rules.

Example:

~~~text
DEPARTMENT
    |
    | has
    ↓
EMPLOYEE
~~~

One department can have many employees.

Each employee belongs to one department in this simplified model.

Therefore:

~~~text
Department
1 : N
Employee
~~~

---

# 23. Real-Time 1:N Examples

~~~text
Department
   |
   +--- Employee 1
   +--- Employee 2
   +--- Employee 3
~~~

Other examples:

~~~text
Customer
   |
   +--- Order 1
   +--- Order 2
   +--- Order 3
~~~

~~~text
Publisher
   |
   +--- Book 1
   +--- Book 2
   +--- Book 3
~~~

These are common 1:N patterns.

---

# 24. Many-to-One Relationship

A **N:1 relationship** is simply the reverse perspective of a 1:N relationship.

Example:

~~~text
Many Employees
       ↓
   Department
```

From Employee's perspective:

~~~text
Employee
N : 1
Department
~~~

From Department's perspective:

~~~text
Department
1 : N
Employee
~~~

Important:

~~~text
1:N
and
N:1
```

can describe the same relationship from opposite directions.

---

# 25. Many-to-Many Relationship

An **M:N relationship** means many instances of one entity type can be associated with many instances of another entity type.

Classic example:

~~~text
STUDENT
   ↕
COURSE
~~~

One student can enroll in many courses.

One course can have many students.

Therefore:

~~~text
Student
M : N
Course
~~~

This is one of the most important ER-model patterns.

---

# 26. Real-Time M:N Example

Suppose:

~~~text
Student A
→ DBMS
→ OS

Student B
→ DBMS
→ Networks

Student C
→ OS
→ Networks
~~~

Here:

~~~text
One Student
→ Many Courses

One Course
→ Many Students
~~~

Therefore:

~~~text
M:N
~~~

---

# 27. Relationship Cardinality Recognition

> [!important]
> If the question says:
>
> **"One department has many employees"**
>
> Think:
>
> `1:N`
>
> If it says:
>
> **"One student takes many courses and one course has many students"**
>
> Think:
>
> `M:N`
>
> If it says:
>
> **"One person has one passport"**
>
> Think:
>
> `1:1`
>
> Always check the complete business rule before deciding.

---

# 28. Participation Constraint

**Participation** tells us whether every entity instance must participate in a relationship.

There are two major types:

1. Total Participation
2. Partial Participation

This is different from cardinality.

---

# 29. Total Participation

**Total participation** means every entity instance in the entity set must participate in the relationship.

Example:

~~~text
EMPLOYEE
   |
works_for
   |
DEPARTMENT
~~~

Suppose every employee must belong to a department.

Then:

~~~text
Employee
→ Total Participation
~~~

In Chen notation, total participation is commonly represented by a **double line** between the entity and relationship.

---

# 30. Partial Participation

**Partial participation** means some entity instances may participate, while others may not.

Example:

~~~text
EMPLOYEE
   |
manages
   |
DEPARTMENT
~~~

Not every employee is necessarily a manager.

Therefore:

~~~text
Employee
→ Partial Participation
~~~

In Chen notation, partial participation is commonly represented by a **single line**.

---

# 31. Cardinality vs Participation

This is a major interview distinction.

### Cardinality

Answers:

> **"How many?"**

Example:

~~~text
1:1
1:N
M:N
~~~

### Participation

Answers:

> **"Must it participate?"**

Example:

~~~text
Total
Partial
~~~

Memory:

~~~text
Cardinality
→ HOW MANY?

Participation
→ MUST PARTICIPATE?
~~~

---

# 32. Cardinality + Participation

These concepts can occur together.

Example:

~~~text
EMPLOYEE
   |
works_for
   |
DEPARTMENT
~~~

Suppose:

~~~text
Every employee must belong to exactly one department.

A department may have many employees.
~~~

Then:

~~~text
Cardinality
→ 1:N

Employee Participation
→ Total
~~~

This is a common interview-style question.

---

# 33. Minimum and Maximum Cardinality

A more precise way to describe participation is using minimum and maximum constraints.

Example:

~~~text
Employee
(1,1)
   |
works_for
   |
Department
(0,N)
~~~

Interpretation:

For Employee:

~~~text
Minimum = 1
Maximum = 1
~~~

So each employee must belong to exactly one department.

For Department:

~~~text
Minimum = 0
Maximum = N
~~~

So a department may have zero or many employees.

---

# 34. `(0,1)` Meaning

If an entity has:

~~~text
(0,1)
~~~

it means:

~~~text
Minimum = 0
Maximum = 1
~~~

Interpretation:

The entity may participate in the relationship, but at most once.

Example:

~~~text
Employee
(0,1)
   |
manages
   |
Department
~~~

An employee may manage zero or one department under this simplified business rule.

---

# 35. `(1,N)` Meaning

~~~text
(1,N)
~~~

means:

~~~text
Minimum = 1
Maximum = N
~~~

Interpretation:

At least one and potentially many relationship instances.

Example:

~~~text
Department
(1,N)
   |
has
   |
Employee
~~~

This would mean every department must have at least one employee and can have many.

Again, the exact business rule determines the constraint.

---

# 36. Cardinality vs Degree

Another common trap.

### Degree

Number of participating entity types.

Example:

~~~text
Student
   |
enrolls
   |
Course
~~~

Degree:

~~~text
2
→ Binary
~~~

### Cardinality

How many entity instances can participate.

Example:

~~~text
Student
M:N
Course
~~~

Cardinality:

~~~text
M:N
~~~

Memory:

~~~text
Degree
→ Number of Entity Types

Cardinality
→ Number of Instances
~~~

---

# 37. Relationship Attributes

Sometimes a relationship itself has attributes.

Example:

~~~text
STUDENT
   |
enrolls
   |
COURSE
~~~

Suppose we need:

~~~text
Enrollment_Date
Grade
Semester
```

These attributes describe the **enrollment relationship**, not merely the student or course.

Conceptually:

~~~text
Student
    \
     \ 
     ENROLLS
     /     \
    /       \
Course     Grade
          Date
```

This is an important advanced ER concept.

---

# 38. Why Relationship Attributes Matter

Consider:

~~~text
Student
Course
```

Student has:

~~~text
Name
CGPA
~~~

Course has:

~~~text
Course_Name
Credits
~~~

But:

~~~text
Grade
```

belongs to the student's enrollment in a particular course.

The same student may have different grades for different courses.

Therefore:

~~~text
Grade
→ Relationship Attribute
~~~

---

# 39. Real-Time Example — Employee Project

~~~text
EMPLOYEE
    |
works_on
    |
PROJECT
~~~

Suppose we need:

~~~text
Hours_Worked
Start_Date
Role
```

These values describe the employee's participation in a specific project.

Therefore they can be relationship attributes.

---

# 40. Real-Time Example — Product Order

~~~text
ORDER
   |
contains
   |
PRODUCT
~~~

Relationship attributes may include:

~~~text
Quantity
Unit_Price_At_Purchase
Discount
```

Why?

Because:

~~~text
Quantity
```

belongs to the specific product's occurrence within the specific order.

The same product can have different quantities in different orders.

---

# 41. Relationship Attribute vs Entity Attribute

This is a major interview question.

Example:

~~~text
Student
   |
enrolls
   |
Course
```

`CGPA` belongs to:

~~~text
Student
```

`Course_Name` belongs to:

~~~text
Course
```

But:

~~~text
Grade
```

belongs to:

~~~text
Student-Course enrollment
```

Therefore:

~~~text
CGPA
→ Entity Attribute

Course_Name
→ Entity Attribute

Grade
→ Relationship Attribute
~~~

---

# 42. Identifying Relationship

An identifying relationship connects a weak entity to its owner entity.

Example:

~~~text
EMPLOYEE
   ||
   ||
DEPENDENT
~~~

The weak entity depends on the owner for identification.

Therefore:

~~~text
Employee
→ Owner Entity

Dependent
→ Weak Entity

Their connection
→ Identifying Relationship
~~~

---

# 43. Recursive Relationship

A recursive relationship occurs when an entity type participates in a relationship with itself.

Example:

~~~text
EMPLOYEE
    |
  manages
    ↺
EMPLOYEE
~~~

This is:

~~~text
Unary Relationship
```

Roles:

~~~text
Manager
Employee
~~~

Both are instances of the same entity type.

---

# 44. Recursive Relationship Example — Social Network

~~~text
PERSON
   |
follows
   ↺
PERSON
~~~

One person follows another person.

Both are instances of:

~~~text
PERSON
```

This is a recursive relationship.

---

# 45. Recursive Relationship Example — Prerequisite

~~~text
COURSE
   |
prerequisite_of
   ↺
COURSE
~~~

One course can be a prerequisite for another course.

Both are instances of the same entity type.

This is also unary/recursive.

---

# 46. Binary Relationship — Master Pattern

Most common ER relationships are binary.

Examples:

~~~text
Customer
   |
places
   |
Order
~~~

~~~text
Employee
   |
works_for
   |
Department
~~~

~~~text
Student
   |
enrolls
   |
Course
~~~

When exactly two entity types participate:

~~~text
Binary
→ Degree 2
~~~

---

# 47. Ternary Relationship — Important Warning

Do not automatically replace every ternary relationship with three binary relationships.

Consider:

~~~text
Supplier
Product
Project
```

Relationship:

~~~text
Supplier supplies Product to Project
```

The meaning depends on the combination of all three participants.

Three separate binary relationships may not preserve the same semantics.

This is an important database-design interview concept.

---

# 48. Binary vs Ternary

### Binary

~~~text
Student
   |
enrolls
   |
Course
~~~

Two entity types.

### Ternary

~~~text
Supplier
    \
     Supplies
      /    \
 Product   Project
~~~

Three entity types.

Shortcut:

~~~text
2 → Binary
3 → Ternary
~~~

---

# 49. Relationship Naming

A good relationship name should clearly describe the association.

Good:

~~~text
Student
→ enrolls_in
→ Course
~~~

~~~text
Customer
→ places
→ Order
~~~

~~~text
Employee
→ works_for
→ Department
~~~

Avoid vague names:

~~~text
related_to
connected_to
has_relation
~~~

unless the domain genuinely requires such generic semantics.

---

# 50. Relationship Direction

In conceptual ER modeling, relationships do not necessarily imply a directional flow like a programming function.

For example:

~~~text
Student
   |
enrolls
   |
Course
~~~

The relationship connects the entity types.

Natural language may describe it directionally, but the underlying association can be considered from either side.

This becomes important when discussing cardinality.

---

# 51. Relationship Roles

Role names become especially important when the same entity type participates multiple times.

Example:

~~~text
EMPLOYEE
   |
manages
   |
EMPLOYEE
~~~

Without role names, the diagram is ambiguous.

Use:

~~~text
Manager
Employee
~~~

Both are roles of the `EMPLOYEE` entity type.

---

# 52. Relationship Degree Recognition

> [!important]
> If one entity type participates:
>
> **Unary**

If two:

~~~text
Binary
~~~

If three:

~~~text
Ternary
~~~

If more than three:

~~~text
N-ary
~~~

Do not count:

~~~text
Attributes
```

Count:

~~~text
Entity Types
~~~

---

# 53. Cardinality Recognition

> [!important]
> Ask:
>
> **"For one instance on this side, how many instances can exist on the other side?"**

Example:

~~~text
Department → Employees
~~~

One department:

~~~text
Many employees
~~~

Therefore:

~~~text
1:N
~~~

---

# 54. Participation Recognition

> [!important]
> Ask:
>
> **"Is participation mandatory for every entity instance?"**

If yes:

~~~text
Total Participation
~~~

If no:

~~~text
Partial Participation
~~~

---

# 55. Relationship Attribute Recognition

> [!important]
> Ask:
>
> **"Does this value describe the entity itself or the connection between entities?"**

Example:

~~~text
Student
→ Name

Course
→ Course_Name

Enrollment
→ Grade
~~~

`Grade` depends on the specific Student-Course connection.

Therefore:

~~~text
Grade
→ Relationship Attribute
~~~

---

# 56. Basic Example — Identify Relationship

### Question

A student enrolls in a course.

Identify the entities and relationship.

### Solution

Entities:

~~~text
Student
Course
~~~

Relationship:

~~~text
Enrolls
~~~

Therefore:

~~~text
Student
   |
enrolls
   |
Course
~~~

---

# 57. Basic Example — Degree

### Question

A student enrolls in a course.

What is the degree of the relationship?

### Solution

Participating entity types:

~~~text
Student
Course
~~~

Count:

~~~text
2
~~~

Therefore:

~~~text
Binary Relationship
~~~

---

# 58. Basic Example — Cardinality

### Question

A student can enroll in many courses, and a course can have many students.

What is the cardinality?

### Solution

~~~text
Student → Many Courses
Course → Many Students
~~~

Therefore:

~~~text
M:N
~~~

---

# 59. Basic Example — 1:N

### Question

One department has many employees, while each employee belongs to one department.

Find the cardinality.

### Solution

~~~text
Department → Many Employees
Employee → One Department
~~~

Therefore:

~~~text
1:N
~~~

---

# 60. Basic Example — 1:1

### Question

Each person has at most one passport, and each passport belongs to at most one person.

What is the relationship cardinality?

### Solution

~~~text
Person → One Passport
Passport → One Person
~~~

Therefore:

~~~text
1:1
~~~

This assumes the stated business rules.

---

# 61. Medium Example — Participation

### Question

Every employee must belong to a department.

What type of participation does Employee have in the `works_for` relationship?

### Solution

The word:

~~~text
Every
~~~

means participation is mandatory.

Therefore:

~~~text
Employee
→ Total Participation
~~~

---

# 62. Medium Example — Partial Participation

### Question

A company has employees, but only some employees manage departments.

What is the participation of Employee in the `manages` relationship?

### Solution

Not every employee participates.

Therefore:

~~~text
Employee
→ Partial Participation
~~~

---

# 63. Medium Example — Relationship Attribute

### Question

A student enrolls in a course. The database stores the grade obtained by the student in that course.

Where should `Grade` belong?

### Solution

The grade depends on:

~~~text
Student
+
Course
+
Specific Enrollment
~~~

Therefore:

~~~text
Grade
→ Relationship Attribute
~~~

---

# 64. Medium Example — Unary Relationship

### Question

An employee can manage another employee.

What type of relationship is this?

### Solution

Both participants belong to:

~~~text
EMPLOYEE
~~~

Therefore:

~~~text
Degree = 1
~~~

Answer:

**Unary / Recursive Relationship**

Roles:

~~~text
Manager
Employee
~~~

---

# 65. Medium Example — Ternary Relationship

### Question

A supplier supplies a product to a project.

If the relationship depends on all three participants together, what type of relationship is it?

### Solution

Entity types:

~~~text
Supplier
Product
Project
~~~

Count:

~~~text
3
~~~

Therefore:

**Ternary Relationship**

---

# 66. Advanced Example — Student Enrollment

Suppose:

~~~text
STUDENT
---------
Student_ID
Name

COURSE
---------
Course_ID
Name
```

Relationship:

~~~text
ENROLLS
```

Attributes:

~~~text
Enrollment_Date
Grade
Semester
```

Cardinality:

~~~text
M:N
~~~

because:

~~~text
Student → Many Courses
Course → Many Students
~~~

Relationship attributes:

~~~text
Enrollment_Date
Grade
Semester
~~~

This is a classic ER-model example.

---

# 67. Advanced Example — Employee Project

Entities:

~~~text
EMPLOYEE
PROJECT
~~~

Relationship:

~~~text
WORKS_ON
~~~

Attributes:

~~~text
Hours_Worked
Start_Date
Role
```

Why are these relationship attributes?

Because the same employee may work:

~~~text
20 hours → Project A
10 hours → Project B
```

The values depend on the particular employee-project association.

---

# 68. Advanced Example — Order and Product

Entities:

~~~text
ORDER
PRODUCT
```

Relationship:

~~~text
CONTAINS
```

Suppose:

~~~text
Quantity
Unit_Price
Discount
```

are associated with the specific product in the specific order.

These are naturally modeled as relationship-specific information or, in relational implementation, attributes of an associative entity such as `OrderItem`.

---

# 69. Advanced Example — Recursive Employee Hierarchy

Entity:

~~~text
EMPLOYEE
```

Relationship:

~~~text
MANAGES
```

Structure:

~~~text
CEO
 |
 +--- Manager A
 |      |
 |      +--- Employee 1
 |      +--- Employee 2
 |
 +--- Manager B
        |
        +--- Employee 3
~~~

This is a recursive relationship because:

~~~text
EMPLOYEE
→ MANAGES
→ EMPLOYEE
~~~

Roles:

~~~text
Manager
Subordinate
~~~

---

# 70. Advanced Example — Course Prerequisites

Entity:

~~~text
COURSE
```

Relationship:

~~~text
PREREQUISITE_OF
```

Example:

~~~text
Programming Basics
       |
 prerequisite for
       ↓
Data Structures
       |
 prerequisite for
       ↓
Advanced Algorithms
~~~

Both sides are instances of the same entity type:

~~~text
COURSE
```

Therefore:

~~~text
Unary / Recursive Relationship
~~~

---

# 71. Advanced Example — Hospital

Entities:

~~~text
PATIENT
DOCTOR
```

Relationship:

~~~text
TREATS
```

Cardinality may be:

~~~text
M:N
~~~

if a doctor treats many patients and a patient can be treated by many doctors.

Relationship attributes could include:

~~~text
Treatment_Date
Diagnosis
Notes
```

depending on requirements.

This demonstrates:

~~~text
Entities
+
Relationship
+
Cardinality
+
Relationship Attributes
~~~

---

# 72. Advanced Example — Banking

Entities:

~~~text
CUSTOMER
ACCOUNT
```

Relationship:

~~~text
OWNS
```

Possible cardinality:

~~~text
M:N
```

if:

~~~text
Customer → Multiple Accounts
Account → Multiple Customers
```

such as joint accounts.

But if the business rules say every account has exactly one customer, it would instead be:

~~~text
1:N
~~~

This demonstrates why **business requirements determine cardinality**.

---

# 73. Advanced Example — E-Commerce

Entities:

~~~text
CUSTOMER
ORDER
```

Relationship:

~~~text
PLACES
```

Typical rule:

~~~text
One Customer
→ Many Orders

One Order
→ One Customer
```

Therefore:

~~~text
1:N
~~~

Possible participation:

~~~text
Customer
→ Partial, if a customer can exist without orders

Order
→ Total, if every order must belong to a customer
~~~

This is a common real-world ER pattern.

---

# 74. Relationship Design Workflow

Use this process:

~~~text
STEP 1
Identify entities
        ↓
STEP 2
Find how they interact
        ↓
STEP 3
Name the relationship
        ↓
STEP 4
Determine degree
        ↓
STEP 5
Determine cardinality
        ↓
STEP 6
Determine participation
        ↓
STEP 7
Identify relationship attributes
        ↓
STEP 8
Check whether a weak entity is involved
        ↓
STEP 9
Convert to relational design if needed
~~~

This is the professional approach.

---

# 75. Cardinality Decision Tree

~~~text
START
  |
  ↓
For one A, how many B?
  |
  +---- One
  |      |
  |      ↓
  |   For one B,
  |   how many A?
  |      |
  |      +---- One → 1:1
  |      |
  |      +---- Many → N:1
  |
  +---- Many
         |
         ↓
      For one B,
      how many A?
         |
         +---- One → 1:N
         |
         +---- Many → M:N
~~~

This is one of the most useful recognition patterns.

---

# 76. Cardinality Shortcut

> [!tip]
> Ask two questions:
>
> **Q1:** One A can connect to how many B?
>
> **Q2:** One B can connect to how many A?
>
> Then write the pair.

Example:

~~~text
One Student → Many Courses
One Course → Many Students
~~~

Therefore:

~~~text
M:N
~~~

Example:

~~~text
One Department → Many Employees
One Employee → One Department
~~~

Therefore:

~~~text
1:N
~~~

---

# 77. Degree Shortcut

> [!tip]
> Count entity types, not instances.
>
> ```text
> 1 Entity Type
> → Unary
>
> 2 Entity Types
> → Binary
>
> 3 Entity Types
> → Ternary
>
> 4+
> → N-ary
> ```

---

# 78. Participation Shortcut

> [!tip]
> Look for words:
>
> **Every / Must / Required**
>
> → Total Participation
>
> **Some / May / Optional**
>
> → Partial Participation
>
> This is a recognition heuristic. Always confirm the complete business rule.

---

# 79. Relationship Attribute Shortcut

> [!tip]
> Ask:
>
> **"Can this value change depending on which two entities are connected?"**
>
> If yes, it may be a relationship attribute.

Example:

~~~text
Student + Course
→ Grade
~~~

One student can have:

~~~text
DBMS → A
OS → B
Networks → A+
~~~

Therefore:

~~~text
Grade
→ Relationship-specific
~~~

---

# 80. Cardinality vs Participation — Master Comparison

| Concept | Question | Examples |
|---|---|---|
| Degree | How many entity types? | Unary, Binary, Ternary |
| Cardinality | How many instances? | 1:1, 1:N, M:N |
| Participation | Must every instance participate? | Total, Partial |
| Role | What part does an entity play? | Manager, Employee |
| Relationship Attribute | What describes the association? | Grade, Hours |

This table is extremely important for interviews.

---

# 81. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Degree Means Cardinality

Wrong.

~~~text
Degree
→ Number of Entity Types

Cardinality
→ Number of Entity Instances
~~~

---

### Mistake 2 — 1:N Means Degree 2

Wrong.

`1:N` describes cardinality.

The relationship may be binary, but these are different concepts.

---

### Mistake 3 — Every Relationship Is Binary

Wrong.

Relationships can be:

~~~text
Unary
Binary
Ternary
N-ary
~~~

---

### Mistake 4 — Every Many-to-Many Relationship Is Automatically Ternary

Wrong.

A many-to-many relationship can be binary:

~~~text
Student
M:N
Course
~~~

Degree:

~~~text
2
→ Binary
~~~

Cardinality:

~~~text
M:N
~~~

---

### Mistake 5 — Relationship Attribute Belongs to an Entity

Not necessarily.

Example:

~~~text
Grade
```

may belong to the Student-Course enrollment rather than Student alone.

---

### Mistake 6 — Total Participation Means 1:1

Wrong.

Participation and cardinality are different.

A relationship can be:

~~~text
1:N
```

and one side can have:

~~~text
Total Participation
~~~

---

### Mistake 7 — Every Employee Must Be a Manager

Wrong.

If only some employees manage others:

~~~text
Manager participation
→ Partial
~~~

---

### Mistake 8 — Cardinality Is Always Fixed

Wrong.

Cardinality depends on business requirements.

Example:

~~~text
Customer ↔ Account
```

could be:

~~~text
1:N
```

or:

~~~text
M:N
```

depending on whether joint accounts are allowed.

---

# 82. Common Exam Patterns

> [!important] Must Master

1. Relationship definition
2. Relationship type
3. Relationship instance
4. Relationship set
5. Relationship degree
6. Unary relationship
7. Binary relationship
8. Ternary relationship
9. N-ary relationship
10. Recursive relationship
11. Role names
12. Cardinality
13. 1:1
14. 1:N
15. N:1
16. M:N
17. Participation
18. Total participation
19. Partial participation
20. Minimum and maximum cardinality
21. Relationship attributes
22. Identifying relationship
23. Degree vs cardinality
24. Cardinality vs participation
25. Relationship vs attribute
26. Relationship vs entity
27. ER-to-relational mapping
28. Associative entities

---

# 83. Interview Questions

## Q1. What is a relationship in an ER model?

### Strong Answer

> A relationship represents an association between two or more entity types. For example, Student enrolls in Course, where Student and Course are entities and Enrolls is the relationship.

---

# 84. Interview Question — Relationship Type

## Q2. What is a relationship type?

### Answer

> A relationship type defines the general association between entity types.

Example:

~~~text
STUDENT
   |
ENROLLS
   |
COURSE
~~~

`ENROLLS` is the relationship type.

---

# 85. Interview Question — Relationship Instance

## Q3. What is a relationship instance?

### Answer

> A relationship instance is one specific occurrence of a relationship between entity instances.

Example:

~~~text
Student 101
→ enrolls in
Course CSE101
~~~

---

# 86. Interview Question — Relationship Set

## Q4. What is a relationship set?

### Answer

> A relationship set is the collection of relationship instances belonging to the same relationship type.

Example:

~~~text
Student 101 → CSE101
Student 101 → DBMS
Student 102 → CSE101
~~~

Together these form the enrollment relationship set.

---

# 87. Interview Question — Degree

## Q5. What is the degree of a relationship?

### Strong Answer

> The degree of a relationship is the number of entity types participating in that relationship.

Examples:

~~~text
1 → Unary
2 → Binary
3 → Ternary
4+ → N-ary
~~~

---

# 88. Interview Question — Unary

## Q6. What is a unary relationship?

### Answer

> A unary relationship involves one entity type participating in a relationship with itself.

Example:

~~~text
EMPLOYEE
   |
manages
   ↺
EMPLOYEE
~~~

It is also called a recursive relationship.

---

# 89. Interview Question — Binary

## Q7. What is a binary relationship?

### Answer

> A binary relationship involves two entity types.

Example:

~~~text
Student
   |
enrolls
   |
Course
~~~

---

# 90. Interview Question — Ternary

## Q8. What is a ternary relationship?

### Answer

> A ternary relationship involves three entity types.

Example:

~~~text
Supplier
Product
Project
```

participating in:

~~~text
Supplies
~~~

---

# 91. Interview Question — Cardinality

## Q9. What is cardinality?

### Strong Answer

> Cardinality specifies how many instances of one entity type can be associated with instances of another entity type.

Common forms:

~~~text
1:1
1:N
N:1
M:N
~~~

---

# 92. Interview Question — Participation

## Q10. What is participation constraint?

### Answer

> Participation specifies whether every entity instance must participate in a relationship.

Types:

~~~text
Total
Partial
~~~

---

# 93. Interview Question — Cardinality vs Participation

## Q11. What is the difference?

### Answer

~~~text
Cardinality
→ How many?

Participation
→ Must participate?
~~~

Example:

~~~text
Department
1:N
Employee
```

and:

~~~text
Every Employee must belong to a Department
```

So:

~~~text
Cardinality
→ 1:N

Employee Participation
→ Total
~~~

---

# 94. Advanced Interview Question

## Q12. Can a relationship have attributes?

### Answer

Yes.

If an attribute describes the association rather than one entity, it can be a relationship attribute.

Example:

~~~text
Student
   |
enrolls
   |
Course
```

Relationship attributes:

~~~text
Grade
Semester
Enrollment_Date
~~~

---

# 95. Advanced Interview Question

## Q13. What is a recursive relationship?

### Answer

> A recursive relationship occurs when the same entity type participates more than once in a relationship.

Example:

~~~text
EMPLOYEE
   |
manages
   |
EMPLOYEE
~~~

Role names:

~~~text
Manager
Subordinate
~~~

---

# 96. Advanced Interview Question

## Q14. Why are role names required in recursive relationships?

### Answer

Because the same entity type participates in multiple roles.

Example:

~~~text
EMPLOYEE
   |
manages
   |
EMPLOYEE
~~~

We need to distinguish:

~~~text
Manager
```

from:

~~~text
Subordinate
```

Both are employees but have different roles.

---

# 97. Advanced Interview Question

## Q15. What is the difference between a relationship type and relationship set?

### Answer

~~~text
Relationship Type
→ General definition

Relationship Set
→ Collection of actual relationship instances
~~~

Example:

~~~text
ENROLLS
→ Relationship Type

Student 101 → CSE101
Student 102 → CSE101
Student 103 → DBMS
→ Relationship Instances
~~~

Together:

~~~text
Enrollment Relationship Set
~~~

---

# 98. Advanced Interview Question

## Q16. Can a binary relationship be M:N?

### Answer

Yes.

Binary means:

~~~text
Two entity types
```

M:N means:

~~~text
Many-to-many cardinality
```

Example:

~~~text
Student
M:N
Course
```

Therefore:

~~~text
Degree = 2
Cardinality = M:N
~~~

---

# 99. Advanced Interview Question

## Q17. Can a relationship be 1:N and have total participation?

### Answer

Yes.

These describe different properties.

Example:

~~~text
Department
1:N
Employee
~~~

If every employee must belong to a department:

~~~text
Employee
→ Total Participation
~~~

The relationship remains:

~~~text
1:N
~~~

---

# 100. Advanced Interview Question

## Q18. Why shouldn't every ternary relationship automatically be replaced with binary relationships?

### Answer

Because the ternary relationship may encode information that depends on the combination of all three participating entities.

Breaking it into independent binary relationships can lose the original semantics.

Example:

~~~text
Supplier
supplies
Product
to
Project
~~~

The fact that a supplier supplies a specific product to a specific project may depend on all three together.

---

# 101. IIT-Level Thinking Pattern

When solving any ER relationship problem, think:

~~~text
ENTITIES
   ↓
What objects?
   ↓
RELATIONSHIP
   ↓
How connected?
   ↓
DEGREE
   ↓
How many entity types?
   ↓
CARDINALITY
   ↓
How many instances?
   ↓
PARTICIPATION
   ↓
Mandatory or optional?
   ↓
ROLES
   ↓
Are different roles involved?
   ↓
ATTRIBUTES
   ↓
Does the relationship itself have information?
~~~

This sequence is powerful for both exams and interviews.

---

# 102. Master Recognition Table

| Clue | Think |
|---|---|
| Association between entities | Relationship |
| Same entity with itself | Unary / Recursive |
| Two entity types | Binary |
| Three entity types | Ternary |
| More than three | N-ary |
| One-to-one | 1:1 |
| One-to-many | 1:N |
| Many-to-one | N:1 |
| Many-to-many | M:N |
| Every entity must participate | Total |
| Some entities may not participate | Partial |
| Attribute describes connection | Relationship Attribute |
| Same entity in different roles | Role Names |
| Weak entity connection | Identifying Relationship |

---

# 103. Real-Time Interview Design Pattern

Suppose the interviewer asks:

> Design an ER model for a college course registration system.

Start with:

~~~text
Entities:
Student
Course
Instructor
Department
~~~

Then relationships:

~~~text
Student
   |
enrolls
   |
Course

Instructor
   |
teaches
   |
Course

Student
   |
belongs_to
   |
Department
~~~

Then ask:

~~~text
Cardinality?
Participation?
Relationship Attributes?
~~~

For enrollment:

~~~text
Student
M:N
Course
~~~

Possible relationship attributes:

~~~text
Grade
Semester
Enrollment_Date
~~~

This is the correct structured thinking process.

---

# 104. Relationship Design Checklist

Before finalizing a relationship, verify:

~~~text
[ ] What entities participate?

[ ] What is the relationship name?

[ ] What is its degree?

[ ] What is its cardinality?

[ ] What is the participation constraint?

[ ] Are role names required?

[ ] Does the relationship have attributes?

[ ] Is it recursive?

[ ] Is it identifying a weak entity?

[ ] Does it need an associative entity in relational design?

[ ] Does the design preserve the real-world meaning?
~~~

---

# 105. Formula Sheet

~~~text
RELATIONSHIP
→ Association between entities


RELATIONSHIP TYPE
→ General association


RELATIONSHIP INSTANCE
→ Specific occurrence


RELATIONSHIP SET
→ Collection of relationship instances


DEGREE

1
→ Unary

2
→ Binary

3
→ Ternary

4+
→ N-ary


CARDINALITY

1:1
→ One-to-One

1:N
→ One-to-Many

N:1
→ Many-to-One

M:N
→ Many-to-Many


PARTICIPATION

Total
→ Every entity instance must participate

Partial
→ Participation is optional for some instances


MEMORY

Degree
→ How many entity types?

Cardinality
→ How many entity instances?

Participation
→ Must participate?


RELATIONSHIP ATTRIBUTES

Examples:
→ Grade
→ Enrollment_Date
→ Hours_Worked
→ Quantity
→ Role


RECURSIVE

Same entity type
→ Relationship with itself


ROLE NAMES

Same entity type
+
Different roles
→ Manager / Employee
~~~

---

# 106. Quick Revision

> [!summary] One-Minute Revision

~~~text
RELATIONSHIP
→ Association between two or more entities.

ENTITY
→ Object

ATTRIBUTE
→ Property

RELATIONSHIP
→ Connection


RELATIONSHIP TYPE
→ General definition

RELATIONSHIP INSTANCE
→ One specific connection

RELATIONSHIP SET
→ Collection of instances


DEGREE

1
→ Unary / Recursive

2
→ Binary

3
→ Ternary

4+
→ N-ary


CARDINALITY

1:1
→ One-to-One

1:N
→ One-to-Many

N:1
→ Many-to-One

M:N
→ Many-to-Many


PARTICIPATION

Total
→ Every instance participates

Partial
→ Some instances may not participate


RELATIONSHIP ATTRIBUTE
→ Describes the connection itself.

Example:
Student + Course
→ Grade


RECURSIVE RELATIONSHIP
→ Entity relates to itself.

Example:
Employee
→ manages
→ Employee


ROLE NAMES
→ Distinguish different roles in recursive relationships.

Example:
Manager
Employee


MOST IMPORTANT DISTINCTION

Degree
→ Number of Entity Types

Cardinality
→ Number of Entity Instances

Participation
→ Mandatory or Optional


FAST RECOGNITION

Student enrolls Course
→ Binary Relationship

Employee manages Employee
→ Unary / Recursive

Supplier supplies Product to Project
→ Ternary

One Department has many Employees
→ 1:N

Many Students take many Courses
→ M:N

Every Employee must belong to a Department
→ Total Participation

Some Employees manage Departments
→ Partial Participation

Grade for a Student in a Course
→ Relationship Attribute
~~~

---

# 107. Golden Memory Trick

**Relationship = How entities are connected; Degree tells how many entity types, Cardinality tells how many instances, and Participation tells whether the connection is mandatory.**

# 108. One-Line Recognition

**Whenever a question asks how two or more entities are associated, think Relationship and then determine its degree, cardinality, participation, and relationship attributes.**