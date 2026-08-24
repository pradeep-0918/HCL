---
type: concept
subject: dbms
topic: "Cardinality"
parent: "ER Model"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - er-model
  - cardinality
  - cardinality-ratio
  - participation
  - one-to-one
  - one-to-many
  - many-to-one
  - many-to-many
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
  - "[[ER Diagram]]"
  - "[[Primary Key]]"
  - "[[Foreign Key]]"
  - "[[Normalization]]"
---

# Cardinality

## 1. Core Concept

> [!summary]
> **Cardinality** specifies how many instances of one entity can be associated with instances of another entity through a relationship.

The four major cardinality patterns are:

~~~text
1 : 1
→ One-to-One

1 : N
→ One-to-Many

N : 1
→ Many-to-One

M : N
→ Many-to-Many
~~~

The most important question is:

> **"For one entity on this side, how many entities can be associated on the other side?"**

---

# 2. Basic Meaning

Consider:

~~~text
DEPARTMENT
     |
    has
     |
  EMPLOYEE
~~~

Suppose:

~~~text
One Department
→ Many Employees

One Employee
→ One Department
~~~

Then:

~~~text
DEPARTMENT
1 : N
EMPLOYEE
~~~

Cardinality describes the **maximum number of related instances** allowed by the relationship rules.

---

# 3. Cardinality vs Degree

This is one of the most important interview distinctions.

### Degree

Degree asks:

> **How many entity types participate in the relationship?**

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

### Cardinality

Cardinality asks:

> **How many instances can be related?**

Example:

~~~text
Student
M : N
Course
~~~

Therefore:

~~~text
Cardinality = M:N
~~~

Memory:

~~~text
Degree
→ Number of Entity Types

Cardinality
→ Number of Related Instances
~~~

---

# 4. The Four Major Cardinalities

| Cardinality | Meaning |
|---|---|
| 1:1 | One entity maps to one entity |
| 1:N | One entity maps to many entities |
| N:1 | Many entities map to one entity |
| M:N | Many entities map to many entities |

Important:

~~~text
1:N
and
N:1
```

can describe the same relationship from opposite perspectives.

---

# 5. One-to-One Relationship

A **1:1 relationship** means one instance of entity A is associated with at most one instance of entity B, and one instance of B is associated with at most one instance of A, according to the business rules.

Example:

~~~text
PERSON
   |
has
   |
PASSPORT
~~~

Possible rule:

~~~text
One Person
→ At most One Passport

One Passport
→ At most One Person
~~~

Therefore:

~~~text
PERSON
1 : 1
PASSPORT
~~~

---

# 6. Real-Time 1:1 Examples

Possible examples include:

~~~text
Person ↔ Passport
Employee ↔ Assigned Locker
Country ↔ Official Government Record
User ↔ Profile
```

But remember:

> [!warning]
> Never assume a relationship is 1:1 merely because the example sounds natural. The actual cardinality is determined by the system's business rules.

For example, an employee could potentially have multiple lockers in a real organization.

---

# 7. One-to-Many Relationship

A **1:N relationship** means one instance of entity A can be associated with many instances of entity B, while each B instance is associated with one A instance under the stated rules.

Example:

~~~text
DEPARTMENT
    |
   has
    |
 EMPLOYEE
~~~

Business rule:

~~~text
One Department
→ Many Employees

One Employee
→ One Department
~~~

Therefore:

~~~text
1 : N
~~~

---

# 8. Real-Time 1:N Examples

### Department and Employee

~~~text
Department
   |
   +--- Employee 1
   +--- Employee 2
   +--- Employee 3
~~~

### Customer and Orders

~~~text
Customer
   |
   +--- Order 101
   +--- Order 102
   +--- Order 103
~~~

### Publisher and Books

~~~text
Publisher
   |
   +--- Book 1
   +--- Book 2
   +--- Book 3
~~~

### Company and Employees

~~~text
Company
   |
   +--- Employee A
   +--- Employee B
   +--- Employee C
~~~

These are common 1:N patterns when the stated rules match.

---

# 9. Many-to-One Relationship

A **N:1 relationship** is the reverse perspective of a 1:N relationship.

Example:

~~~text
EMPLOYEE
    |
 works_for
    |
DEPARTMENT
~~~

From the Employee perspective:

~~~text
Many Employees
→ One Department
~~~

Therefore:

~~~text
N : 1
~~~

From the Department perspective:

~~~text
One Department
→ Many Employees
~~~

Therefore:

~~~text
1 : N
~~~

Same relationship, opposite viewpoint.

---

# 10. Important Shortcut

> [!tip]
> If you see:
>
> **Many A → One B**
>
> think:
>
> `N:1`
>
> If you reverse the direction:
>
> **One B → Many A**
>
> think:
>
> `1:N`

Example:

~~~text
Many Employees
→ One Department

Employee : Department
= N : 1
~~~

Reverse:

~~~text
Department : Employee
= 1 : N
~~~

---

# 11. Many-to-Many Relationship

An **M:N relationship** means many instances of entity A can be associated with many instances of entity B.

Classic example:

~~~text
STUDENT
   |
enrolls
   |
COURSE
~~~

Business rules:

~~~text
One Student
→ Many Courses

One Course
→ Many Students
~~~

Therefore:

~~~text
M : N
~~~

This is one of the most frequently tested ER-model patterns.

---

# 12. Real-Time M:N Example — College

Suppose:

~~~text
Student A
→ DBMS
→ OS
→ Networks

Student B
→ DBMS
→ Java

Student C
→ OS
→ Java
```

Each student can take multiple courses.

Each course can have multiple students.

Therefore:

~~~text
STUDENT
M : N
COURSE
~~~

---

# 13. Real-Time M:N Example — Doctors and Patients

Suppose:

~~~text
Doctor A
→ Patient 1
→ Patient 2
→ Patient 3

Doctor B
→ Patient 2
→ Patient 4
```

A doctor can treat many patients.

A patient can be treated by many doctors.

Therefore:

~~~text
DOCTOR
M : N
PATIENT
~~~

---

# 14. Real-Time M:N Example — Products and Orders

Consider:

~~~text
ORDER
   ↕
PRODUCT
~~~

One order may contain many products.

One product can appear in many orders.

Therefore:

~~~text
ORDER
M : N
PRODUCT
~~~

In a relational database, this is commonly implemented using an associative entity such as:

~~~text
ORDER_ITEM
~~~

with attributes such as:

~~~text
Order_ID
Product_ID
Quantity
Unit_Price
Discount
~~~

---

# 15. Cardinality Recognition — The Two-Question Method

This is one of the fastest exam methods.

For any relationship:

### Question 1

For **one A**, how many B?

### Question 2

For **one B**, how many A?

Write the answers.

Example:

~~~text
Student ↔ Course
~~~

Question 1:

~~~text
One Student
→ Many Courses
~~~

Question 2:

~~~text
One Course
→ Many Students
~~~

Therefore:

~~~text
M:N
~~~

---

# 16. Cardinality Decision Tree

~~~text
START
  |
  ↓
Take ONE A
  |
  ↓
How many B?
  |
  +---- ONE
  |      |
  |      ↓
  |   Take ONE B
  |      |
  |      +---- ONE → 1:1
  |      |
  |      +---- MANY → N:1
  |
  +---- MANY
         |
         ↓
      Take ONE B
         |
         +---- ONE → 1:N
         |
         +---- MANY → M:N
~~~

This method prevents most cardinality mistakes.

---

# 17. Example — 1:1

### Question

Each person has at most one passport, and each passport belongs to at most one person.

### Step 1

One Person:

~~~text
→ One Passport
~~~

### Step 2

One Passport:

~~~text
→ One Person
~~~

### Answer

~~~text
1 : 1
~~~

---

# 18. Example — 1:N

### Question

One department contains many employees. Each employee belongs to one department.

### Step 1

One Department:

~~~text
→ Many Employees
~~~

### Step 2

One Employee:

~~~text
→ One Department
~~~

### Answer

~~~text
1 : N
~~~

---

# 19. Example — N:1

### Question

Many employees work for one department.

### Step 1

One Employee:

~~~text
→ One Department
~~~

### Step 2

One Department:

~~~text
→ Many Employees
~~~

If writing from Employee to Department:

~~~text
N : 1
~~~

If writing from Department to Employee:

~~~text
1 : N
~~~

---

# 20. Example — M:N

### Question

A student can take multiple courses, and each course can have multiple students.

### Step 1

One Student:

~~~text
→ Many Courses
~~~

### Step 2

One Course:

~~~text
→ Many Students
~~~

### Answer

~~~text
M : N
~~~

---

# 21. Minimum and Maximum Cardinality

Cardinality can be expressed more precisely using:

~~~text
(min, max)
~~~

The first value represents the minimum participation.

The second value represents the maximum participation.

Example:

~~~text
(1,1)
~~~

means:

~~~text
Minimum = 1
Maximum = 1
~~~

So the entity must participate exactly once.

---

# 22. Meaning of `(0,1)`

~~~text
(0,1)
~~~

means:

~~~text
Minimum = 0
Maximum = 1
~~~

Interpretation:

~~~text
Optional
+
At most one
~~~

Example:

An employee may manage zero or one department.

Under this specific business rule:

~~~text
Employee
(0,1)
→ manages
→ Department
~~~

---

# 23. Meaning of `(1,1)`

~~~text
(1,1)
~~~

means:

~~~text
Minimum = 1
Maximum = 1
~~~

Interpretation:

~~~text
Mandatory
+
Exactly One
~~~

Example:

Every employee must belong to exactly one department.

Then:

~~~text
Employee
(1,1)
→ works_for
→ Department
~~~

---

# 24. Meaning of `(0,N)`

~~~text
(0,N)
~~~

means:

~~~text
Minimum = 0
Maximum = Many
~~~

Interpretation:

~~~text
Optional
+
Many allowed
~~~

Example:

A department may have zero or many employees.

~~~text
Department
(0,N)
→ has
→ Employee
~~~

---

# 25. Meaning of `(1,N)`

~~~text
(1,N)
~~~

means:

~~~text
Minimum = 1
Maximum = Many
~~~

Interpretation:

~~~text
Mandatory
+
Many allowed
~~~

Example:

Every department must have at least one employee and can have many employees.

~~~text
Department
(1,N)
→ has
→ Employee
~~~

---

# 26. Min-Max Master Table

| Notation | Meaning |
|---|---|
| (0,1) | Optional, at most one |
| (1,1) | Exactly one |
| (0,N) | Optional, many possible |
| (1,N) | At least one, many possible |

Memory:

~~~text
First Number
→ Minimum

Second Number
→ Maximum
~~~

---

# 27. Cardinality vs Participation

This is one of the most frequently confused concepts.

### Cardinality

Describes:

~~~text
Maximum / multiplicity
~~~

Examples:

~~~text
1:1
1:N
M:N
~~~

### Participation

Describes whether participation is:

~~~text
Mandatory
or
Optional
~~~

Examples:

~~~text
Total
Partial
~~~

---

# 28. Example — Cardinality + Participation

Suppose:

> Every employee must belong to exactly one department, while a department may have zero or many employees.

Then:

Employee side:

~~~text
(1,1)
~~~

Department side:

~~~text
(0,N)
~~~

Therefore:

~~~text
EMPLOYEE
(1,1)
     |
  works_for
     |
DEPARTMENT
(0,N)
~~~

This represents:

~~~text
Cardinality:
1:N

Participation:
Employee → Total
Department → Partial
~~~

---

# 29. Important Pattern — "Every"

> [!important]
> Words such as:
>
> **Every**
>
> **Must**
>
> **Required**
>
> **Exactly**
>
> often indicate a minimum participation of `1`.

Example:

> Every employee must belong to a department.

Think:

~~~text
Employee
Minimum = 1
~~~

---

# 30. Important Pattern — "May"

> [!important]
> Words such as:
>
> **May**
>
> **Can**
>
> **Optional**
>
> **Not necessarily**
>
> often indicate a minimum participation of `0`.

Example:

> An employee may manage a department.

Think:

~~~text
Employee
Minimum = 0
~~~

The maximum still depends on the rest of the requirement.

---

# 31. Important Pattern — "At Most"

> [!important]
> **At most one**
>
> means:
>
> `Maximum = 1`

Example:

> A person can have at most one passport.

Think:

~~~text
Maximum = 1
~~~

Possible min-max:

~~~text
(0,1)
~~~

if the passport is optional.

---

# 32. Important Pattern — "Exactly One"

> [!important]
> **Exactly one**
>
> means:
>
> `Minimum = 1`
>
> `Maximum = 1`

Therefore:

~~~text
(1,1)
~~~

---

# 33. Important Pattern — "At Least One"

> [!important]
> **At least one**
>
> means:
>
> `Minimum = 1`
>
> Maximum can be many unless another constraint is stated.

Therefore:

~~~text
(1,N)
~~~

---

# 34. Important Pattern — "Zero or More"

> [!important]
> **Zero or more**
>
> means:
>
> `Minimum = 0`
>
> `Maximum = N`

Therefore:

~~~text
(0,N)
~~~

---

# 35. Important Pattern — "One or More"

> [!important]
> **One or more**
>
> means:
>
> `Minimum = 1`
>
> `Maximum = N`

Therefore:

~~~text
(1,N)
~~~

---

# 36. Relationship Direction Trick

Suppose:

~~~text
DEPARTMENT
1 : N
EMPLOYEE
~~~

If the question asks:

> How many employees can belong to one department?

Answer:

~~~text
Many
~~~

If it asks:

> How many departments can one employee belong to?

Answer:

~~~text
One
~~~

Do not memorize only `1:N`.

Always understand the direction.

---

# 37. Real-Time Example — College

Suppose:

> Every student belongs to one department. A department can have many students.

Then:

~~~text
STUDENT
(1,1)
   |
belongs_to
   |
DEPARTMENT
(0,N)
~~~

Interpretation:

Student:

~~~text
Exactly one Department
~~~

Department:

~~~text
Zero or Many Students
~~~

Cardinality:

~~~text
N:1
```

from Student to Department.

Equivalent:

~~~text
1:N
```

from Department to Student.

---

# 38. Real-Time Example — Customer and Order

Requirement:

> A customer may place zero or many orders. Every order belongs to exactly one customer.

Therefore:

~~~text
CUSTOMER
(0,N)
   |
places
   |
ORDER
(1,1)
~~~

Interpretation:

Customer:

~~~text
0 to many orders
~~~

Order:

~~~text
Exactly one customer
~~~

Cardinality:

~~~text
1:N
~~~

from Customer to Order.

---

# 39. Real-Time Example — Student and Course

Requirement:

> A student can enroll in many courses. A course can contain many students.

Possible conceptual constraints:

~~~text
STUDENT
(0,N)
   |
enrolls
   |
COURSE
(0,N)
~~~

Cardinality:

~~~text
M:N
~~~

Participation is optional on both sides in this example.

The exact minimum depends on the application requirements.

---

# 40. Real-Time Example — Employee and Project

Requirement:

> An employee may work on many projects, and a project may have many employees.

Therefore:

~~~text
EMPLOYEE
(0,N)
    |
 works_on
    |
PROJECT
(0,N)
~~~

Cardinality:

~~~text
M:N
~~~

Potential relationship attributes:

~~~text
Hours_Worked
Start_Date
Role
~~~

---

# 41. Real-Time Example — Doctor and Patient

Requirement:

> A doctor may treat many patients. A patient may be treated by many doctors.

Therefore:

~~~text
DOCTOR
(0,N)
   |
treats
   |
PATIENT
(0,N)
~~~

Cardinality:

~~~text
M:N
~~~

Potential relationship attributes:

~~~text
Treatment_Date
Diagnosis
Notes
~~~

---

# 42. Real-Time Example — Library

Requirement:

> A member can borrow many books, and a book can be borrowed by many members over time.

Conceptually:

~~~text
MEMBER
(0,N)
   |
borrows
   |
BOOK
(0,N)
~~~

Cardinality may be represented as:

~~~text
M:N
~~~

However, the actual database design often introduces a borrowing/loan entity because the relationship needs information such as:

~~~text
Issue_Date
Return_Date
Fine
Status
~~~

This is an important real-world modeling pattern.

---

# 43. Real-Time Example — E-Commerce

Entities:

~~~text
CUSTOMER
ORDER
PRODUCT
~~~

Relationships:

~~~text
Customer
   |
places
   |
Order

Order
   |
contains
   |
Product
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

The M:N relationship is commonly resolved using:

~~~text
ORDER_ITEM
~~~

---

# 44. Why M:N Is Important in Relational Databases

Relational tables commonly implement M:N relationships using an intermediate table.

Example:

~~~text
STUDENT
---------
Student_ID

COURSE
---------
Course_ID

ENROLLMENT
---------
Student_ID
Course_ID
Grade
Semester
```

Therefore:

~~~text
Student
M:N
Course
```

becomes:

~~~text
Student
   |
   |
Enrollment
   |
   |
Course
~~~

This is one of the most important ER-to-relational conversion patterns.

---

# 45. M:N Conversion Pattern

> [!tip]
> When you see:
>
> `M:N`
>
> think:
>
> **Associative Entity / Junction Table**
>
> Example:
>
> ```text
> Student M:N Course
> ```
>
> becomes:
>
> ```text
> Enrollment(Student_ID, Course_ID, ...)
> ```

This is extremely important for SQL and DBMS interviews.

---

# 46. 1:N Relational Mapping Shortcut

For a 1:N relationship:

~~~text
Department
1 : N
Employee
~~~

The foreign key is generally placed on the **N-side**.

Therefore:

~~~text
EMPLOYEE
---------
Employee_ID
Department_ID
Name
Salary
~~~

`Department_ID` references:

~~~text
DEPARTMENT
---------
Department_ID
~~~

Memory:

> [!tip]
> **1:N → Put the foreign key on the N-side.**

This is one of the most useful DBMS shortcuts.

---

# 47. 1:1 Relational Mapping

For a 1:1 relationship, the foreign key can often be placed on either side, but the choice depends on participation, optionality, semantics, and implementation requirements.

Example:

~~~text
PERSON
1:1
PASSPORT
~~~

Possible implementation:

~~~text
PERSON
---------
Person_ID
Passport_ID
~~~

or:

~~~text
PASSPORT
---------
Passport_ID
Person_ID
~~~

If one side has total participation, placing the foreign key there can often be advantageous.

---

# 48. M:N Relational Mapping

For M:N:

~~~text
STUDENT
M:N
COURSE
~~~

Create a separate relation:

~~~text
ENROLLMENT
---------
Student_ID
Course_ID
Grade
Semester
~~~

Common primary key:

~~~text
(Student_ID, Course_ID)
~~~

or another appropriate key if multiple enrollment records are allowed by the business rules.

---

# 49. Cardinality and Foreign Keys

Cardinality strongly influences relational design.

### 1:N

~~~text
Department
1:N
Employee
```

Foreign key:

~~~text
Employee.Department_ID
```

### M:N

~~~text
Student
M:N
Course
```

Create:

~~~text
Enrollment
```

### 1:1

Foreign key can generally be placed on one side with an appropriate uniqueness constraint.

This is a major connection between ER modeling and SQL.

---

# 50. Cardinality and UNIQUE Constraint

Suppose:

~~~text
Person
1:1
Passport
~~~

If `Passport.Person_ID` references `Person.Person_ID`, then to enforce 1:1, `Person_ID` in the Passport table generally needs a `UNIQUE` constraint.

Conceptually:

~~~sql
Person_ID UNIQUE
```

Without the uniqueness rule, multiple passports could potentially reference the same person, turning the relationship into 1:N.

This is an important interview-level insight.

---

# 51. Cardinality and Foreign Key — Interview Insight

> [!important]
> A foreign key alone does not always enforce a 1:1 relationship.

Example:

~~~text
Passport
---------
Passport_ID
Person_ID
```

If multiple rows can contain the same `Person_ID`, then:

~~~text
Person
1:N
Passport
```

could occur.

To enforce:

~~~text
1:1
```

the referencing key may need:

~~~text
UNIQUE
```

This distinction is commonly tested in DBMS interviews.

---

# 52. Cardinality and NULL

Consider:

~~~text
Customer
(0,N)
   |
places
   |
Order
(1,1)
~~~

If every order must belong to a customer, then:

~~~text
Order.Customer_ID
```

should generally be:

~~~text
NOT NULL
```

If the relationship is optional:

~~~text
(0,1)
```

then a nullable foreign key may be appropriate depending on the schema design.

This shows how conceptual constraints map to relational constraints.

---

# 53. Cardinality and Business Rules

Never decide cardinality based only on common sense.

Example:

~~~text
Customer ↔ Account
~~~

Possible models:

### Model A

~~~text
Customer
1:N
Account
~~~

if each account belongs to exactly one customer.

### Model B

~~~text
Customer
M:N
Account
~~~

if joint accounts are supported.

Therefore:

> **Requirements determine cardinality.**

---

# 54. Advanced Pattern — Historical Relationships

Sometimes a relationship appears to be 1:N at a current point in time but becomes M:N over history.

Example:

~~~text
Employee
Department
```

Current assignment:

~~~text
Employee
→ One Current Department
~~~

But over a career:

~~~text
Employee
→ Department A
→ Department B
→ Department C
~~~

If the database stores assignment history, we may model:

~~~text
EMPLOYEE
M:N
DEPARTMENT
```

through:

~~~text
EMPLOYEE_DEPARTMENT_HISTORY
```

with:

~~~text
Start_Date
End_Date
Role
```

This demonstrates that cardinality depends on the **time scope and business requirement**.

---

# 55. Advanced Pattern — Time-Dependent Cardinality

Suppose:

> A student can have only one active advisor at a time, but may have different advisors over different semesters.

Current state:

~~~text
Student
1:1
Active Advisor
~~~

Historical relationship:

~~~text
Student
M:N
Advisor
```

with:

~~~text
Semester
Start_Date
End_Date
~~~

Therefore:

> Cardinality must be interpreted within the scope defined by the requirements.

---

# 56. Advanced Pattern — Optional One-to-One

Suppose:

> Every employee may have at most one parking slot, but not every employee has one.

Then:

~~~text
EMPLOYEE
(0,1)
   |
assigned
   |
PARKING_SLOT
(0,1)
~~~

This is:

~~~text
1:1
```

with optional participation on both sides.

Important:

~~~text
1:1
≠
Mandatory 1:1
~~~

---

# 57. Advanced Pattern — Mandatory One-to-Many

Suppose:

> Every department must have at least one employee, and every employee belongs to exactly one department.

Then:

~~~text
DEPARTMENT
(1,N)
    |
   has
    |
EMPLOYEE
(1,1)
~~~

Cardinality:

~~~text
1:N
~~~

Participation:

~~~text
Department → Total
Employee → Total
~~~

This is a useful interview pattern.

---

# 58. Advanced Pattern — Optional One-to-Many

Suppose:

> A department may have zero or many employees, while every employee must belong to one department.

Then:

~~~text
DEPARTMENT
(0,N)
    |
   has
    |
EMPLOYEE
(1,1)
~~~

Cardinality:

~~~text
1:N
~~~

Participation:

~~~text
Department → Partial
Employee → Total
~~~

---

# 59. Advanced Pattern — Optional Many-to-Many

Suppose:

> Students may enroll in multiple courses, and courses may have multiple students. Some students may not yet be enrolled, and some courses may currently have no students.

Then:

~~~text
STUDENT
(0,N)
   |
enrolls
   |
COURSE
(0,N)
~~~

Cardinality:

~~~text
M:N
~~~

Participation:

~~~text
Partial on both sides
~~~

---

# 60. Advanced Pattern — Mandatory Many-to-Many

Suppose:

> Every project must have at least one employee, and every employee must work on at least one project.

Then:

~~~text
EMPLOYEE
(1,N)
    |
 works_on
    |
PROJECT
(1,N)
~~~

Cardinality:

~~~text
M:N
~~~

Participation:

~~~text
Total on both sides
~~~

---

# 61. Cardinality Matrix

| A → B | B → A | Result |
|---|---|---|
| One | One | 1:1 |
| One | Many | 1:N |
| Many | One | N:1 |
| Many | Many | M:N |

Use this whenever you are confused.

---

# 62. Recognition Trick — Read Both Directions

> [!tip]
> Never read only one sentence.
>
> Always construct:
>
> ```text
> One A → ?
> One B → ?
> ```
>
> Then determine cardinality.

Example:

> A company has many employees.

This alone suggests:

~~~text
Company → Many Employees
~~~

But to determine the complete relationship, ask:

~~~text
One Employee → How many Companies?
~~~

If one employee belongs to one company:

~~~text
1:N
~~~

---

# 63. Recognition Trick — "Each"

The word **each** often describes the reverse side.

Example:

> One department has many employees, and each employee belongs to one department.

Extract:

~~~text
One Department
→ Many Employees

Each Employee
→ One Department
~~~

Therefore:

~~~text
1:N
~~~

---

# 64. Recognition Trick — "Many"

Words such as:

~~~text
many
multiple
several
numerous
any number
~~~

usually indicate:

~~~text
Maximum = N
~~~

But do not automatically infer minimum.

For example:

> A department may have many employees.

could mean:

~~~text
(0,N)
```

if zero is allowed.

---

# 65. Recognition Trick — "At Least"

Words:

~~~text
at least one
one or more
minimum one
~~~

indicate:

~~~text
Minimum = 1
~~~

Therefore:

~~~text
(1,N)
```

if no upper bound other than many is given.

---

# 66. Recognition Trick — "At Most"

Words:

~~~text
at most one
maximum one
no more than one
~~~

indicate:

~~~text
Maximum = 1
~~~

Possible min-max:

~~~text
(0,1)
```

if participation is optional.

---

# 67. Recognition Trick — "Exactly"

Words:

~~~text
exactly one
exactly two
~~~

give a specific cardinality.

For one:

~~~text
(1,1)
~~~

For more specialized constraints such as exactly two, the simple 0/1/N notation may not be sufficient and a more detailed business rule is required.

---

# 68. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing 1:N with N:1

They may represent the same relationship from opposite directions.

Correct:

~~~text
Department → Employee = 1:N

Employee → Department = N:1
~~~

---

### Mistake 2 — Thinking Degree = Cardinality

Wrong.

~~~text
Degree
→ Number of Entity Types

Cardinality
→ Number of Related Instances
~~~

---

### Mistake 3 — Assuming M:N Means Ternary

Wrong.

~~~text
Student M:N Course
```

is:

~~~text
Degree = 2
→ Binary
~~~

and:

~~~text
Cardinality = M:N
~~~

---

### Mistake 4 — Assuming 1:1 Means Mandatory

Wrong.

You can have:

~~~text
(0,1)
```

on both sides.

That is optional 1:1.

---

### Mistake 5 — Ignoring Business Rules

Do not assume:

~~~text
Customer ↔ Account
```

is always 1:N.

Joint accounts may make it M:N.

---

### Mistake 6 — Ignoring Direction

Always ask:

~~~text
One A → How many B?

One B → How many A?
~~~

---

### Mistake 7 — Treating Minimum and Maximum as the Same

In:

~~~text
(0,N)
~~~

`0` means minimum.

`N` means maximum.

---

### Mistake 8 — Assuming "Many" Means "At Least One"

Not always.

~~~text
Many
```

normally addresses maximum.

If zero is allowed:

~~~text
(0,N)
~~~

If at least one is required:

~~~text
(1,N)
~~~

---

### Mistake 9 — Forgetting M:N Conversion

In relational implementation:

~~~text
M:N
→ Associative/Junction Table
~~~

Example:

~~~text
Student
M:N
Course
```

becomes:

~~~text
Enrollment
~~~

---

# 69. Common Exam Patterns

> [!important] Must Master

1. Definition of cardinality
2. Cardinality ratio
3. 1:1 relationship
4. 1:N relationship
5. N:1 relationship
6. M:N relationship
7. Minimum cardinality
8. Maximum cardinality
9. `(0,1)`
10. `(1,1)`
11. `(0,N)`
12. `(1,N)`
13. Cardinality vs degree
14. Cardinality vs participation
15. Identifying cardinality from statements
16. Direction of cardinality
17. Foreign key placement
18. M:N conversion
19. Associative entity
20. UNIQUE constraint for 1:1
21. NOT NULL and mandatory participation
22. Optional relationships
23. Historical cardinality
24. Relationship attributes

---

# 70. Interview Questions

## Q1. What is cardinality in DBMS?

### Strong Answer

> Cardinality in an ER model specifies how many instances of one entity can be associated with instances of another entity through a relationship.

Common forms:

~~~text
1:1
1:N
N:1
M:N
~~~

---

# 71. Interview Question — Cardinality vs Degree

## Q2. What is the difference between degree and cardinality?

### Strong Answer

> Degree is the number of participating entity types in a relationship, while cardinality describes how many instances of those entities can participate in the relationship.

Example:

~~~text
Student M:N Course
```

Here:

~~~text
Degree = 2
→ Binary

Cardinality = M:N
~~~

---

# 72. Interview Question — 1:N

## Q3. Explain one-to-many with an example.

### Answer

> In a one-to-many relationship, one instance of one entity can be associated with many instances of another entity, while each instance on the many side is associated with one instance on the one side according to the business rule.

Example:

~~~text
Department
1:N
Employee
~~~

---

# 73. Interview Question — M:N

## Q4. Explain many-to-many.

### Answer

> In an M:N relationship, many instances of one entity can be associated with many instances of another entity.

Example:

~~~text
Student
M:N
Course
~~~

One student can take many courses and one course can have many students.

---

# 74. Interview Question — M:N Implementation

## Q5. How is an M:N relationship implemented in a relational database?

### Strong Answer

> It is usually represented using an associative or junction table containing foreign keys referencing the participating entities.

Example:

~~~text
STUDENT
---------
Student_ID

COURSE
---------
Course_ID

ENROLLMENT
---------
Student_ID
Course_ID
Grade
Semester
~~~

---

# 75. Interview Question — 1:N Foreign Key

## Q6. Where is the foreign key generally placed in a 1:N relationship?

### Answer

> The foreign key is generally placed on the N-side.

Example:

~~~text
Department
1:N
Employee
```

Therefore:

~~~text
Employee.Department_ID
```

references:

~~~text
Department.Department_ID
~~~

---

# 76. Interview Question — 1:1 Implementation

## Q7. How can a 1:1 relationship be implemented?

### Answer

A foreign key can be placed on one side, often guided by participation and design requirements.

To enforce one-to-one semantics, the referencing foreign key generally needs a uniqueness constraint.

Example:

~~~text
PERSON
1:1
PASSPORT
```

Possible:

~~~text
PASSPORT
---------
Passport_ID
Person_ID UNIQUE
~~~

---

# 77. Interview Question — Participation

## Q8. What is total participation?

### Answer

> Total participation means every entity instance in the entity set must participate in the relationship.

Example:

> Every employee must belong to a department.

Therefore:

~~~text
Employee
→ Total Participation
~~~

---

# 78. Interview Question — Partial Participation

## Q9. What is partial participation?

### Answer

> Partial participation means some entity instances may participate in the relationship while others may not.

Example:

> Only some employees manage departments.

Therefore:

~~~text
Employee
→ Partial Participation
~~~

---

# 79. Advanced Interview Question

## Q10. Can a relationship be both M:N and total participation?

### Answer

Yes.

Example:

~~~text
Employee
(1,N)
   |
works_on
   |
Project
(1,N)
~~~

Cardinality:

~~~text
M:N
~~~

Participation:

~~~text
Total on both sides
~~~

---

# 80. Advanced Interview Question

## Q11. Can a 1:1 relationship have partial participation?

### Answer

Yes.

Example:

~~~text
Employee
(0,1)
   |
assigned
   |
Parking_Slot
(0,1)
~~~

Cardinality:

~~~text
1:1
~~~

Participation:

~~~text
Partial on both sides
~~~

---

# 81. Advanced Interview Question

## Q12. Why does cardinality matter when designing tables?

### Answer

Because cardinality affects how relationships are represented using foreign keys, junction tables, uniqueness constraints, and nullability.

Examples:

~~~text
1:N
→ Foreign key on N-side

M:N
→ Junction table

1:1
→ Foreign key + appropriate UNIQUE constraint
~~~

---

# 82. Advanced Interview Question

## Q13. Does a foreign key automatically enforce cardinality?

### Answer

No.

A foreign key primarily enforces referential integrity.

Additional constraints may be required to enforce specific cardinalities.

For example:

~~~text
1:1
```

may require:

~~~text
FOREIGN KEY
+
UNIQUE
~~~

---

# 83. Advanced Interview Question

## Q14. How do you determine cardinality from a problem statement?

### Strong Answer

Use two questions:

~~~text
1. For one A, how many B?

2. For one B, how many A?
~~~

Then map the result:

~~~text
One + One
→ 1:1

One + Many
→ 1:N

Many + One
→ N:1

Many + Many
→ M:N
~~~

---

# 84. Advanced Interview Question

## Q15. What does `(0,N)` mean?

### Answer

~~~text
Minimum = 0
Maximum = N
~~~

Therefore:

> The entity may participate zero times or many times.

---

# 85. Advanced Interview Question

## Q16. What does `(1,1)` mean?

### Answer

~~~text
Minimum = 1
Maximum = 1
~~~

Therefore:

> The entity must participate exactly once.

---

# 86. Advanced Interview Question

## Q17. What does `(0,1)` mean?

### Answer

~~~text
Minimum = 0
Maximum = 1
~~~

Therefore:

> Participation is optional, but at most one related instance is allowed.

---

# 87. Advanced Interview Question

## Q18. What does `(1,N)` mean?

### Answer

~~~text
Minimum = 1
Maximum = N
~~~

Therefore:

> At least one related instance is required, and many are allowed.

---

# 88. IIT-Level Problem-Solving Pattern

When you see an ER problem:

~~~text
STEP 1
Identify A and B
        ↓
STEP 2
Ask "One A → how many B?"
        ↓
STEP 3
Ask "One B → how many A?"
        ↓
STEP 4
Determine cardinality
        ↓
STEP 5
Look for "every", "must", "may"
        ↓
STEP 6
Determine minimum participation
        ↓
STEP 7
Determine maximum participation
        ↓
STEP 8
Check relationship attributes
        ↓
STEP 9
Check M:N conversion
        ↓
STEP 10
Map to foreign keys
~~~

This is the complete exam + interview workflow.

---

# 89. Master Cardinality Table

| Requirement | Cardinality | Typical Min-Max |
|---|---|---|
| One A → One B | 1:1 | (0,1)/(0,1) or stricter |
| One A → Many B | 1:N | (0,N) or (1,N) on many side |
| Many A → One B | N:1 | Reverse of 1:N |
| Many A → Many B | M:N | (0,N)/(0,N) or stricter |
| Exactly one | 1 | (1,1) |
| At most one | 0 or 1 | (0,1) |
| Zero or more | 0 to N | (0,N) |
| One or more | 1 to N | (1,N) |

The exact min-max pair depends on the complete business rule.

---

# 90. Real-Time System Design Pattern

Suppose an interviewer asks:

> Design a database for an online learning platform.

Entities:

~~~text
STUDENT
COURSE
INSTRUCTOR
CERTIFICATE
~~~

Relationships:

~~~text
Student
   |
enrolls
   |
Course
```

~~~text
Instructor
   |
teaches
   |
Course
```

~~~text
Student
   |
earns
   |
Certificate
```

Possible cardinalities:

~~~text
Student M:N Course

Instructor 1:N Course
```

depending on whether multiple instructors per course are allowed.

Then ask:

~~~text
Participation?
Relationship Attributes?
Keys?
Foreign Keys?
~~~

This is how cardinality becomes useful in real system design.

---

# 91. Formula Sheet

~~~text
CARDINALITY
→ Number of entity instances that can participate in a relationship.


MAJOR TYPES

1:1
→ One-to-One

1:N
→ One-to-Many

N:1
→ Many-to-One

M:N
→ Many-to-Many


MIN-MAX

(0,1)
→ Zero or One

(1,1)
→ Exactly One

(0,N)
→ Zero or Many

(1,N)
→ One or More


FAST METHOD

One A → ?
One B → ?

One + One
→ 1:1

One + Many
→ 1:N

Many + One
→ N:1

Many + Many
→ M:N


IMPORTANT DISTINCTION

Degree
→ Number of Entity Types

Cardinality
→ Number of Related Instances

Participation
→ Mandatory / Optional


RELATIONAL MAPPING

1:N
→ FK on N-side

M:N
→ Junction / Associative Table

1:1
→ FK + UNIQUE as needed


KEYWORDS

Every / Must / Required
→ Minimum often 1

May / Optional
→ Minimum often 0

At most one
→ Maximum 1

At least one
→ Minimum 1

Zero or more
→ (0,N)

One or more
→ (1,N)
~~~

---

# 92. Quick Revision

> [!summary] One-Minute Revision

~~~text
CARDINALITY
→ How many instances can be related?


FOUR MAIN TYPES

1:1
→ One A ↔ One B

1:N
→ One A ↔ Many B

N:1
→ Many A ↔ One B

M:N
→ Many A ↔ Many B


FASTEST METHOD

Ask:

1. One A → how many B?
2. One B → how many A?


MIN-MAX

(0,1)
→ Optional, maximum one

(1,1)
→ Exactly one

(0,N)
→ Optional, many possible

(1,N)
→ At least one, many possible


IMPORTANT DIFFERENCE

Degree
→ How many entity types?

Cardinality
→ How many instances?

Participation
→ Is participation mandatory?


EXAMPLES

Department → Employee
→ 1:N

Employee → Department
→ N:1

Student → Course
→ M:N

Person → Passport
→ 1:1, if business rules enforce it


REAL-WORLD MAPPING

1:N
→ FK generally on N-side

M:N
→ Junction table

1:1
→ FK on one side + UNIQUE when required


IMPORTANT KEYWORDS

Every
→ Usually minimum 1

Must
→ Usually minimum 1

May
→ Usually minimum 0

At most one
→ Maximum 1

At least one
→ Minimum 1


MASTER FORMULA

Cardinality
=
Relationship multiplicity

Minimum
=
Mandatory/Optional lower bound

Maximum
=
Allowed upper bound


CORE MINDSET

Requirements
↓
Entities
↓
Relationship
↓
One A → ?
↓
One B → ?
↓
Cardinality
↓
Minimum/Maximum
↓
Participation
↓
Relational Mapping
~~~

---

# 93. Golden Memory Trick

**Cardinality asks "How many?" — ask in both directions: One A connects to how many B, and one B connects to how many A.**

# 94. One-Line Recognition

**Whenever a question describes how many instances of one entity can be associated with another, determine the Cardinality using 1:1, 1:N, N:1, or M:N.**