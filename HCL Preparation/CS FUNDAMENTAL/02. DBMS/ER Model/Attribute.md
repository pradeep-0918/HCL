---
type: concept
subject: dbms
topic: "Attribute"
parent: "ER Model"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - dbms
  - er-model
  - attribute
  - simple-attribute
  - composite-attribute
  - multivalued-attribute
  - derived-attribute
  - key-attribute
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
  - "[[Relationship]]"
  - "[[Cardinality]]"
  - "[[ER Diagram]]"
  - "[[Relational Model]]"
  - "[[Primary Key]]"
  - "[[Normalization]]"
---

# Attribute

## 1. Core Concept

> [!summary]
> An **Attribute** is a property or characteristic that describes an entity or relationship.

Simple idea:

~~~text
ENTITY
   ↓
What object?

ATTRIBUTE
   ↓
What information describes that object?
~~~

Example:

~~~text
STUDENT
   |
   +--- Student_ID
   +--- Name
   +--- Age
   +--- Email
   +--- CGPA
~~~

Here:

~~~text
Student
→ Entity

Student_ID
Name
Age
Email
CGPA
→ Attributes
~~~

The attribute tells us **what information we store about an entity**.

---

# 2. Basic Meaning

Consider a real-world student.

The student is an object.

We may want to store:

~~~text
Student ID
Name
Age
Department
CGPA
Email
Phone
Date of Birth
~~~

These characteristics are attributes of the `Student` entity.

Think:

~~~text
Entity
→ Object

Attribute
→ Property of the Object
~~~

---

# 3. Entity vs Attribute

This is one of the most important ER-model distinctions.

Example:

~~~text
STUDENT
---------
Student_ID
Name
CGPA
Department
~~~

Here:

~~~text
STUDENT
→ Entity

Student_ID
Name
CGPA
Department
→ Attributes
~~~

Shortcut:

> [!tip]
> Ask:
>
> **"What thing am I storing?"**
>
> → Entity
>
> **"What information am I storing about that thing?"**
>
> → Attribute

---

# 4. Real-Time Example — Employee

Entity:

~~~text
EMPLOYEE
~~~

Attributes:

~~~text
Employee_ID
Name
Email
Salary
Department
Joining_Date
Phone
~~~

Conceptually:

~~~text
             EMPLOYEE
                 |
       +---------+---------+
       |         |         |
      ID        Name     Salary
       |
   Department
       |
   Joining Date
~~~

The attributes describe employees.

---

# 5. Attribute in Relational Model

The ER-model concept of an attribute maps naturally to a column in a relational table.

ER Model:

~~~text
STUDENT
---------
Student_ID
Name
CGPA
~~~

Relational Model:

~~~text
+------------+--------+------+
| Student_ID | Name   | CGPA |
+------------+--------+------+
| 101        | Arun   | 8.2  |
| 102        | Priya  | 9.1  |
+------------+--------+------+
~~~

Therefore:

~~~text
ER Attribute
      ↓
Relational Column
~~~

This connection is extremely important.

---

# 6. Attribute Types

The major attribute types you must know are:

1. Simple Attribute
2. Composite Attribute
3. Single-Valued Attribute
4. Multivalued Attribute
5. Derived Attribute
6. Stored Attribute
7. Key Attribute
8. Optional / Null-Valued Attribute
9. Complex Attribute

The most important exam categories are:

~~~text
Simple
Composite
Single-Valued
Multivalued
Derived
Key
~~~

---

# 7. Simple Attribute

A **simple attribute** cannot be meaningfully divided into smaller attributes for the current database model.

Example:

~~~text
Age
Gender
Salary
CGPA
Student_ID
~~~

For example:

~~~text
CGPA
```

is normally treated as one value.

Similarly:

~~~text
Salary
```

can be treated as one attribute.

---

# 8. Composite Attribute

A **composite attribute** can be divided into smaller meaningful sub-attributes.

Classic example:

~~~text
Name
```

can be divided into:

~~~text
First_Name
Middle_Name
Last_Name
~~~

Another example:

~~~text
Address
```

can be divided into:

~~~text
House_No
Street
City
State
PIN
~~~

Therefore:

~~~text
Composite Attribute
→ Attribute made of meaningful sub-attributes
~~~

---

# 9. Composite Attribute Diagram

Conceptually:

~~~text
             Name
          /    |    \
         /     |     \
   First    Middle   Last
    Name      Name    Name
~~~

Another:

~~~text
              Address
           /     |      \
          /      |       \
      Street    City     State
                           |
                          PIN
~~~

The parent attribute is:

~~~text
Name
```

or:

~~~text
Address
```

The components are separate sub-attributes.

---

# 10. Simple vs Composite

| Simple Attribute | Composite Attribute |
|---|---|
| Cannot be meaningfully divided further | Can be divided into components |
| Single conceptual unit | Contains sub-attributes |
| Example: Age | Example: Address |
| Example: Salary | Example: Name |

Memory:

~~~text
Simple
→ One meaningful unit

Composite
→ Can Break
~~~

---

# 11. Important Recognition Trick

> [!important]
> If an attribute can be divided into **meaningful sub-parts**, think:
>
> **Composite Attribute**

Example:

~~~text
Address
→ Street
→ City
→ State
→ PIN
~~~

Therefore:

~~~text
Address
→ Composite
~~~

---

# 12. Single-Valued Attribute

A **single-valued attribute** has one value for a particular entity instance.

Example:

~~~text
Student_ID
```

A student has one Student ID.

Another example:

~~~text
Date_of_Birth
```

A student normally has one date of birth.

Therefore:

~~~text
Student_ID
→ Single-Valued
~~~

---

# 13. Multivalued Attribute

A **multivalued attribute** can have multiple values for one entity instance.

Example:

~~~text
Phone_Number
```

A student may have:

~~~text
9876543210
8765432109
~~~

Therefore:

~~~text
Phone_Number
→ Multivalued Attribute
~~~

Other examples:

~~~text
Email
Skills
Languages
Phone_Numbers
Previous_Degrees
~~~

depending on the application requirements.

---

# 14. Single-Valued vs Multivalued

| Single-Valued | Multivalued |
|---|---|
| One value per entity | Multiple values per entity |
| Student_ID | Phone_Numbers |
| Date_of_Birth | Skills |
| Aadhaar/ID-type identifier | Email addresses, if multiple are allowed |
| One primary email, if business rules enforce one | Multiple email addresses |

Memory:

~~~text
Single
→ One

Multi
→ Many
~~~

---

# 15. Multivalued Attribute Example

Suppose:

~~~text
STUDENT
---------
Student_ID = 101
Name = Arun
Phone = {9876, 8765}
~~~

The student has two phone numbers.

Therefore:

~~~text
Phone
→ Multivalued
~~~

Important:

A multivalued attribute is not necessarily a single cell containing a comma-separated list in a properly normalized relational implementation.

---

# 16. Derived Attribute

A **derived attribute** is calculated from other stored information.

Example:

~~~text
Date_of_Birth
       ↓
   Current Date
       ↓
      Age
~~~

Age can be calculated from the date of birth.

Therefore:

~~~text
Age
→ Derived Attribute
~~~

Another example:

~~~text
Quantity × Unit_Price
        ↓
       Total
~~~

`Total` can be derived from:

~~~text
Quantity
+
Unit_Price
~~~

---

# 17. Stored vs Derived Attribute

| Stored Attribute | Derived Attribute |
|---|---|
| Directly stored | Calculated from other data |
| Salary | Age from DOB |
| Date of Birth | Total Amount |
| Quantity | Tax amount, if computed from other stored values |
| Unit Price | Years of Service |

Memory:

~~~text
Stored
→ Save it

Derived
→ Calculate it
~~~

---

# 18. Important Derived Attribute Trick

> [!important]
> If the value can be calculated from other stored attributes, think:
>
> **Derived Attribute**

Examples:

~~~text
Age
← Date of Birth

Total Amount
← Quantity × Price

Years of Service
← Current Date − Joining Date
~~~

---

# 19. Stored Attribute

A **stored attribute** is an attribute whose value is directly stored in the database.

Example:

~~~text
Date_of_Birth
Joining_Date
Unit_Price
Quantity
~~~

Then another attribute may be derived.

Example:

~~~text
Date_of_Birth
     ↓
    Age
```

Usually:

~~~text
Date_of_Birth
→ Stored

Age
→ Derived
~~~

---

# 20. Key Attribute

A **key attribute** is an attribute that helps uniquely identify an entity instance.

Example:

~~~text
STUDENT
---------
Student_ID
Name
CGPA
~~~

If `Student_ID` uniquely identifies each student:

~~~text
Student_ID
→ Key Attribute
~~~

In conventional ER notation, the key attribute is represented using an **underline**.

Conceptually:

~~~text
Student_ID
-----------
Key
~~~

---

# 21. Key Attribute Example

Consider:

~~~text
EMPLOYEE
---------
Employee_ID
Name
Department
Salary
~~~

If:

~~~text
Employee_ID
```

is unique for every employee:

~~~text
Employee_ID
→ Key Attribute
~~~

Example:

~~~text
E101
E102
E103
```

Each identifies a different employee.

---

# 22. Candidate Key Connection

In database design, an entity may have more than one attribute or attribute combination capable of uniquely identifying instances.

Example:

~~~text
EMPLOYEE
---------
Employee_ID
Email
Name
Phone
~~~

Suppose:

~~~text
Employee_ID
Email
```

are both unique.

They may be candidate keys.

One may be selected as the primary key in the relational implementation.

This connects to:

[[Candidate Key]]

and:

[[Primary Key]]

---

# 23. Null-Valued / Optional Attribute

An attribute may not have a value for every entity instance.

Example:

~~~text
Student
---------
Student_ID
Name
Middle_Name
```

Some students may not have a middle name.

Therefore:

~~~text
Middle_Name
→ Optional / potentially NULL
~~~

Another example:

~~~text
Apartment_Number
```

may not apply to someone living in an independent house.

The important point is:

~~~text
No value
≠
Zero
≠
Empty string
```

The precise meaning depends on the database design.

---

# 24. Complex Attribute

A **complex attribute** combines composite and multivalued characteristics.

Example:

~~~text
Address
```

may have multiple addresses:

~~~text
Home Address
Work Address
```

and each address can itself be composite:

~~~text
Street
City
State
PIN
```

Conceptually:

~~~text
             Address
              /   \
             /     \
          Home     Work
           |         |
       +----+----+ +--+---+
       |    |    | |  |   |
     Street City PIN ...
~~~

This is a more advanced ER-model concept.

---

# 25. Attribute Classification Master Map

~~~text
ATTRIBUTE
    |
    +------------------+
    |                  |
    ↓                  ↓
Simple              Composite
    |
    |
    +------------------+
                       |
               Number of Values
                  /          \
                 ↓            ↓
              Single        Multi
                 |
                 |
          How Value Obtained
              /       \
             ↓         ↓
          Stored      Derived
~~~

An attribute can belong to multiple classifications.

For example:

~~~text
Address
→ Composite
→ Potentially Multivalued
```

The categories describe different properties.

---

# 26. Important Point — Classifications Can Overlap

Do not assume an attribute can have only one type.

For example:

~~~text
Address
```

can be:

~~~text
Composite
+
Multivalued
~~~

if a person can have multiple addresses and each address contains:

~~~text
Street
City
State
PIN
~~~

Similarly, an attribute can be:

~~~text
Simple
+
Single-Valued
+
Stored
~~~

Example:

~~~text
Age
```

if it is directly stored.

---

# 27. Attribute Notation in ER Diagram

Common Chen notation:

~~~text
Entity
→ Rectangle

Attribute
→ Oval

Relationship
→ Diamond
~~~

Example:

~~~text
        (Name)
           |
           |
      +---------+
      | STUDENT |
      +---------+
           |
        (CGPA)
~~~

The oval represents an attribute.

---

# 28. Key Attribute Notation

A key attribute is traditionally shown as an underlined attribute.

Conceptually:

~~~text
     (Student_ID)
      __________
           |
           |
      +---------+
      | STUDENT |
      +---------+
~~~

The underline indicates the identifying attribute.

---

# 29. Multivalued Attribute Notation

A multivalued attribute is traditionally represented using a **double oval**.

Conceptually:

~~~text
    ((Phone))
        |
        |
   +---------+
   | STUDENT |
   +---------+
~~~

Memory:

~~~text
Single Oval
→ Attribute

Double Oval
→ Multivalued Attribute
~~~

---

# 30. Derived Attribute Notation

A derived attribute is traditionally represented using a **dashed oval**.

Conceptually:

~~~text
    - - - - - -
   (    Age    )
    - - - - - -
          |
          |
     +---------+
     | STUDENT |
     +---------+
~~~

Memory:

~~~text
Normal Oval
→ Attribute

Double Oval
→ Multivalued

Dashed Oval
→ Derived
~~~

---

# 31. Composite Attribute Notation

A composite attribute is shown as an oval connected to smaller attribute ovals.

Example:

~~~text
                 (Address)
                 /   |   \
                /    |    \
          (Street) (City) (PIN)
~~~

This shows that:

~~~text
Address
→ Composite Attribute
```

---

# 32. Attribute Notation Master Table

| Attribute Type | Typical ER Notation |
|---|---|
| Simple | Single Oval |
| Composite | Oval connected to sub-ovals |
| Single-Valued | Single Oval |
| Multivalued | Double Oval |
| Derived | Dashed Oval |
| Key Attribute | Underlined |
| Composite + Multivalued | Combined notation |
| Complex | Combination of relevant notations |

---

# 33. Attribute Recognition Shortcut

> [!tip]
> Use the **B-V-C-D-K** shortcut:
>
> **B = Breakable**
>
> → Composite
>
> **V = Values**
>
> → Single / Multi
>
> **C = Calculated**
>
> → Derived
>
> **D = Directly Stored**
>
> → Stored
>
> **K = Key**
>
> → Identifies entity
>
> This lets you classify attributes quickly.

---

# 34. Pattern 1 — Simple Attribute

### How to Recognize

If the attribute is treated as one meaningful unit:

~~~text
Age
Salary
CGPA
~~~

Think:

**Simple Attribute**

### Example

~~~text
Student
→ CGPA
~~~

Answer:

~~~text
CGPA
→ Simple
~~~

---

# 35. Pattern 2 — Composite Attribute

### How to Recognize

If the attribute can be divided into meaningful components:

~~~text
Name
→ First + Middle + Last
~~~

Think:

**Composite Attribute**

### Example

~~~text
Address
→ Street + City + State + PIN
~~~

Answer:

**Composite Attribute**

---

# 36. Pattern 3 — Multivalued Attribute

### How to Recognize

If one entity can have multiple values:

~~~text
Student
→ Multiple phone numbers
~~~

Think:

**Multivalued Attribute**

Example:

~~~text
Phone = {9876, 8765}
~~~

---

# 37. Pattern 4 — Derived Attribute

### How to Recognize

If the value is calculated from another attribute:

~~~text
DOB
 ↓
Age
~~~

Think:

**Derived Attribute**

Another:

~~~text
Quantity × Price
 ↓
Total
~~~

---

# 38. Pattern 5 — Key Attribute

### How to Recognize

If the attribute uniquely identifies an entity:

~~~text
Student_ID
Employee_ID
Product_ID
Account_Number
~~~

Think:

**Key Attribute**

---

# 39. Pattern 6 — Stored Attribute

### How to Recognize

If the value is directly maintained rather than calculated:

~~~text
Date_of_Birth
Joining_Date
Product_Price
~~~

Think:

**Stored Attribute**

---

# 40. Pattern 7 — Optional Attribute

### How to Recognize

If some entity instances may legitimately not have a value:

~~~text
Middle_Name
Apartment_Number
Secondary_Email
~~~

Think:

**Optional / Null-Valued Attribute**

---

# 41. Pattern 8 — Complex Attribute

### How to Recognize

If an attribute is:

~~~text
Composite
+
Multivalued
~~~

think:

**Complex Attribute**

Example:

A person has multiple addresses, and each address contains:

~~~text
Street
City
State
PIN
~~~

---

# 42. Advanced Example — Student

Consider:

~~~text
STUDENT
---------
Student_ID
Name
Address
Phone
Date_of_Birth
Age
CGPA
~~~

Classify them.

### Student_ID

~~~text
Key
+
Simple
+
Single-Valued
+
Stored
~~~

### Name

Could be:

~~~text
Composite
```

if modeled as:

~~~text
First_Name
Middle_Name
Last_Name
~~~

### Address

Could be:

~~~text
Composite
```

if divided into:

~~~text
Street
City
State
PIN
~~~

### Phone

Could be:

~~~text
Multivalued
```

if multiple phone numbers are allowed.

### Date_of_Birth

~~~text
Stored
+
Single-Valued
~~~

### Age

~~~text
Derived
```

if calculated from DOB.

### CGPA

Usually:

~~~text
Simple
+
Single-Valued
+
Stored
~~~

depending on the application design.

---

# 43. Advanced Example — Employee

Consider:

~~~text
EMPLOYEE
---------
Employee_ID
Name
Address
Phone
DOB
Age
Salary
~~~

Classification:

~~~text
Employee_ID
→ Key

Name
→ Composite, if divided into components

Address
→ Composite, if divided into components

Phone
→ Multivalued, if multiple numbers are allowed

DOB
→ Stored

Age
→ Derived

Salary
→ Simple / Stored
~~~

This demonstrates that one entity can have many different attribute types.

---

# 44. Advanced Example — E-Commerce Product

Entity:

~~~text
PRODUCT
```

Attributes:

~~~text
Product_ID
Product_Name
Price
Weight
Dimensions
Images
Discount
Final_Price
```

Possible classification:

~~~text
Product_ID
→ Key

Dimensions
→ Composite
   Length
   Width
   Height

Images
→ Multivalued

Price
→ Stored

Discount
→ Stored

Final_Price
→ Derived
~~~

For example:

~~~text
Final_Price
=
Price − Discount
~~~

depending on the pricing rules.

---

# 45. Advanced Example — Bank Account

Entity:

~~~text
ACCOUNT
```

Attributes:

~~~text
Account_Number
Account_Type
Balance
Opening_Date
Branch_Code
```

Possible classification:

~~~text
Account_Number
→ Key

Balance
→ Stored

Opening_Date
→ Stored

Branch_Code
→ Simple / Stored

Account_Type
→ Simple / Stored
```

The exact classification depends on the chosen data model.

---

# 46. Advanced Example — Order

Entity:

~~~text
ORDER
```

Attributes:

~~~text
Order_ID
Order_Date
Quantity
Unit_Price
Total_Amount
Shipping_Address
```

Possible classification:

~~~text
Order_ID
→ Key

Order_Date
→ Stored

Quantity
→ Stored

Unit_Price
→ Stored

Total_Amount
→ Derived

Shipping_Address
→ Composite
~~~

Potential formula:

~~~text
Total_Amount
=
Quantity × Unit_Price
~~~

Real systems may include taxes, discounts, shipping fees, multiple order items, etc.

---

# 47. Advanced Example — Person

Entity:

~~~text
PERSON
```

Attributes:

~~~text
Name
Address
Phone
DOB
Age
Email
Skills
```

Possible classification:

~~~text
Name
→ Composite

Address
→ Composite

Phone
→ Multivalued

DOB
→ Stored

Age
→ Derived

Email
→ Single or Multivalued depending on requirements

Skills
→ Multivalued
~~~

---

# 48. Attribute Design Decision

When deciding how to model an attribute, ask these questions:

~~~text
Q1
Can it be divided?
        ↓
Composite?

Q2
Can one entity have multiple values?
        ↓
Multivalued?

Q3
Is it calculated?
        ↓
Derived?

Q4
Is it directly stored?
        ↓
Stored?

Q5
Does it uniquely identify?
        ↓
Key?

Q6
Can it be absent?
        ↓
Optional?
~~~

This is an excellent ER-design checklist.

---

# 49. Attribute vs Entity — Advanced Decision

Suppose we have:

~~~text
Student
Department
```

Question:

Should `Department` be an attribute or entity?

Ask:

~~~text
Does Department have its own attributes?
        ↓
Does it have its own identifier?
        ↓
Does it participate in relationships?
        ↓
Is it managed independently?
~~~

If yes, model it as an entity.

If not, it may be appropriate as an attribute.

---

# 50. Attribute vs Entity Example

### Simple System

~~~text
STUDENT
---------
Name
Department
```

Department may simply be an attribute.

### Complex System

~~~text
DEPARTMENT
---------
Department_ID
Department_Name
HOD
Office
Budget
```

Now Department is clearly a rich object.

It should generally be modeled as an entity.

---

# 51. Attribute vs Relationship — Advanced

Suppose:

~~~text
Student
   |
enrolls
   |
Course
```

Now suppose enrollment has:

~~~text
Enrollment_Date
Grade
Semester
```

Those properties describe the enrollment connection.

Therefore, depending on the modeling approach:

~~~text
ENROLLMENT
```

can become an associative entity.

This is an important interview design pattern.

---

# 52. Derived Attribute — Important Design Insight

Why might we avoid storing derived attributes?

Suppose:

~~~text
DOB = 10-01-2004
Age = 22
```

Age changes with time.

If we store:

~~~text
Age = 22
```

it can become outdated.

Instead, storing:

~~~text
DOB
```

allows age to be calculated when needed.

This reduces stale-data problems.

However, real systems may intentionally store derived values for performance, reporting, auditing, or business requirements.

The correct decision depends on the application.

---

# 53. Multivalued Attribute — Database Design Insight

Suppose:

~~~text
Student
---------
Phone = 9876, 8765, 7654
```

This can cause problems in relational design.

A normalized relational approach may separate phone numbers:

~~~text
STUDENT
---------
Student_ID
Name

STUDENT_PHONE
------------
Student_ID
Phone
```

This connects directly to:

[[1NF]]

and normalization.

---

# 54. Composite Attribute — Database Design Insight

Suppose:

~~~text
Name
```

is:

~~~text
First_Name
Middle_Name
Last_Name
~~~

Why keep the components separately?

Because queries may need:

~~~text
Last_Name = "Kumar"
```

or:

~~~text
First_Name = "Pradeep"
```

Separate components provide more flexibility.

Whether to store a combined name or separate components depends on requirements.

---

# 55. Attribute Domain

Every attribute has a domain of allowed values.

Example:

~~~text
CGPA
→ Numeric range

Student_ID
→ Identifier format

Date_of_Birth
→ Valid date values

Name
→ Character string
~~~

Therefore:

~~~text
Attribute
+
Domain
=
Allowed Values
~~~

This connects ER modeling with the relational model.

---

# 56. Attribute Constraints

Attributes may have constraints such as:

~~~text
NOT NULL
UNIQUE
CHECK
DEFAULT
PRIMARY KEY
FOREIGN KEY
```

Example:

~~~sql
CGPA DECIMAL(3,2)
CHECK (CGPA >= 0 AND CGPA <= 10)
```

The attribute concept therefore connects directly to database constraints.

---

# 57. Attribute Naming Best Practices

Use meaningful names.

Good:

~~~text
Student_ID
Date_of_Birth
Joining_Date
Department_ID
~~~

Avoid vague names:

~~~text
Data1
Value
Info
Thing
X
~~~

Good naming makes database schemas easier to understand and maintain.

---

# 58. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Attribute Is an Entity

Wrong.

~~~text
Student
→ Entity

Name
→ Attribute
~~~

---

### Mistake 2 — Every Attribute Is Simple

Wrong.

Some attributes can be composite.

Example:

~~~text
Address
→ Street + City + State + PIN
~~~

---

### Mistake 3 — Multiple Values Mean Composite

Wrong.

These are different concepts.

~~~text
Composite
→ One attribute split into components

Multivalued
→ Multiple values for one attribute
~~~

---

# 59. Composite vs Multivalued

This is a major interview trap.

### Composite

~~~text
Address
↓
Street
City
State
PIN
~~~

### Multivalued

~~~text
Phone
↓
9876
8765
7654
~~~

Memory:

~~~text
Composite
→ Break the Attribute

Multivalued
→ Multiple Values
~~~

---

# 60. Derived vs Stored

Another common trap.

### Stored

~~~text
Date_of_Birth
```

directly stored.

### Derived

~~~text
Age
```

calculated from DOB.

Memory:

~~~text
Stored
→ Save

Derived
→ Calculate
~~~

---

# 61. Key vs Derived

An attribute can theoretically have different classifications, but in standard ER design, key attributes are used for identification.

Example:

~~~text
Student_ID
```

is:

~~~text
Key
+
Usually Stored
+
Usually Simple
+
Usually Single-Valued
~~~

Do not confuse:

~~~text
Key
```

with:

~~~text
Derived
```

---

# 62. Attribute Classification Table

| Attribute | Type | Why |
|---|---|---|
| Student_ID | Key | Identifies student |
| Name | Composite | Can have first/middle/last |
| Age | Derived | Calculated from DOB |
| DOB | Stored | Directly stored |
| Phone | Multivalued | Multiple numbers possible |
| Address | Composite | Has components |
| CGPA | Simple | Single conceptual value |
| Skills | Multivalued | Multiple skills possible |

The exact classification always depends on system requirements.

---

# 63. Common Exam Patterns

> [!important] Must Master

1. Attribute definition
2. Entity vs attribute
3. Simple attribute
4. Composite attribute
5. Single-valued attribute
6. Multivalued attribute
7. Stored attribute
8. Derived attribute
9. Key attribute
10. Partial key
11. Optional attribute
12. Complex attribute
13. Attribute domain
14. Attribute constraints
15. ER notation
16. Composite vs multivalued
17. Stored vs derived
18. Key attribute notation
19. Multivalued attribute notation
20. Derived attribute notation
21. Attribute-to-column mapping
22. Entity vs attribute modeling decisions
23. Associative entity connection
24. Normalization connection

---

# 64. Interview Questions

## Q1. What is an attribute?

### Strong Answer

> An attribute is a property or characteristic that describes an entity or relationship.

Example:

~~~text
Student
→ Name
→ CGPA
→ Email
~~~

---

# 65. Interview Question — Simple Attribute

## Q2. What is a simple attribute?

> A simple attribute is an attribute that cannot be meaningfully divided into smaller components for the given model.

Examples:

~~~text
Age
Salary
CGPA
~~~

---

# 66. Interview Question — Composite Attribute

## Q3. What is a composite attribute?

> A composite attribute can be divided into smaller meaningful sub-attributes.

Example:

~~~text
Address
→ Street
→ City
→ State
→ PIN
~~~

---

# 67. Interview Question — Multivalued Attribute

## Q4. What is a multivalued attribute?

> A multivalued attribute can have multiple values for a single entity instance.

Example:

~~~text
Student
→ Phone_Numbers
→ {9876, 8765}
~~~

---

# 68. Interview Question — Derived Attribute

## Q5. What is a derived attribute?

> A derived attribute is calculated from one or more other attributes.

Example:

~~~text
DOB
↓
Age
~~~

---

# 69. Interview Question — Stored Attribute

## Q6. What is a stored attribute?

> A stored attribute is directly maintained in the database rather than calculated from other stored values.

Example:

~~~text
Date_of_Birth
~~~

---

# 70. Interview Question — Key Attribute

## Q7. What is a key attribute?

> A key attribute uniquely identifies an entity instance within an entity set.

Example:

~~~text
Student_ID
```

---

# 71. Advanced Interview Question

## Q8. What is the difference between composite and multivalued attributes?

### Strong Answer

> A composite attribute can be divided into smaller meaningful attributes, whereas a multivalued attribute can have multiple values for a single entity instance.

Example:

~~~text
Composite:
Address
→ City + State + PIN

Multivalued:
Phone
→ 9876, 8765
~~~

---

# 72. Advanced Interview Question

## Q9. What is the difference between stored and derived attributes?

### Answer

~~~text
Stored
→ Directly stored

Derived
→ Calculated from stored data
~~~

Example:

~~~text
DOB
→ Stored

Age
→ Derived
~~~

---

# 73. Advanced Interview Question

## Q10. Can an attribute be both composite and multivalued?

### Answer

Yes.

For example, a person may have multiple addresses, and each address can contain:

~~~text
Street
City
State
PIN
```

So:

~~~text
Address
→ Multivalued
+
Composite
~~~

---

# 74. Advanced Interview Question

## Q11. Why is age often modeled as a derived attribute?

### Answer

Because age changes with time while date of birth does not.

Instead of storing a potentially outdated age:

~~~text
DOB
→ Store stable information

Age
→ Calculate when needed
~~~

---

# 75. Advanced Interview Question

## Q12. Why are multivalued attributes usually separated in relational design?

### Answer

Because relational tables are normally designed so that each field contains an atomic value.

A multivalued attribute can introduce repeating values and violate first normal form.

A separate relation can represent the multiple values cleanly.

Example:

~~~text
STUDENT
---------
Student_ID
Name

STUDENT_PHONE
-------------
Student_ID
Phone
~~~

---

# 76. Advanced Interview Question

## Q13. Can an attribute become an entity?

### Answer

Yes, depending on requirements.

If an attribute-like concept develops its own:

~~~text
Attributes
+
Identity
+
Relationships
+
Independent management
~~~

it may be better modeled as an entity.

Example:

~~~text
Department
```

may begin as a student attribute but become an entity when the system needs:

~~~text
Department_ID
Department_Name
HOD
Budget
Office
```

---

# 77. Advanced Interview Question

## Q14. What is a complex attribute?

### Answer

> A complex attribute combines composite and multivalued characteristics.

Example:

~~~text
Multiple Addresses
```

where each address contains:

~~~text
Street
City
State
PIN
~~~

---

# 78. IIT-Level Thinking Pattern

When an interviewer gives an attribute, classify it using:

~~~text
STEP 1
Can it be divided?
        ↓
Composite / Simple

STEP 2
Can it have multiple values?
        ↓
Multivalued / Single-Valued

STEP 3
Is it calculated?
        ↓
Derived / Stored

STEP 4
Does it identify the entity?
        ↓
Key / Non-Key

STEP 5
Can it be absent?
        ↓
Optional / Mandatory
~~~

This is the fastest systematic classification method.

---

# 79. Attribute Classification Decision Tree

~~~text
                    ATTRIBUTE
                        |
             +----------+----------+
             |                     |
       Can it be divided?     Cannot be divided
             |                     |
           YES                    SIMPLE
             |
         COMPOSITE
             
             
             ATTRIBUTE
                 |
       Multiple values?
          /          \
        YES          NO
         |            |
    MULTIVALUED    SINGLE-VALUED


             ATTRIBUTE
                 |
        Calculated from
        other attributes?
          /          \
        YES          NO
         |            |
      DERIVED       STORED


             ATTRIBUTE
                 |
       Uniquely identifies
       an entity instance?
          /          \
        YES          NO
         |            |
        KEY        NON-KEY
~~~

---

# 80. Real-Time Design Example

Consider an online shopping customer:

~~~text
CUSTOMER
---------
Customer_ID
Name
Phone
Email
Address
Date_of_Birth
Age
~~~

Classify:

~~~text
Customer_ID
→ Key

Name
→ Composite, if split into components

Phone
→ Multivalued, if multiple numbers allowed

Email
→ Single or multivalued depending on requirements

Address
→ Composite

Date_of_Birth
→ Stored

Age
→ Derived
~~~

This is exactly how you should think during system-design interviews.

---

# 81. Attribute Modeling Checklist

Before finalizing an ER diagram, ask:

~~~text
[ ] Is this really an attribute?

[ ] Should it be an entity?

[ ] Is it simple?

[ ] Is it composite?

[ ] Is it single-valued?

[ ] Is it multivalued?

[ ] Is it stored?

[ ] Is it derived?

[ ] Is it a key?

[ ] Can it be NULL?

[ ] What is its domain?

[ ] What constraints apply?

[ ] Will it create normalization problems?
~~~

This checklist prevents many ER-design mistakes.

---

# 82. Placement Exam Focus

### Very High Priority

- Attribute definition
- Simple attribute
- Composite attribute
- Multivalued attribute
- Derived attribute
- Key attribute
- Composite vs multivalued
- Stored vs derived
- ER notation

### High Priority

- Single-valued attribute
- Complex attribute
- Optional attribute
- Domain
- Attribute constraints
- Attribute-to-column mapping

### Interview Priority

- Entity vs attribute
- When attribute becomes entity
- Composite vs multivalued
- Stored vs derived
- Why derived attributes are useful
- Why multivalued attributes create normalization issues
- Attribute classification in real systems

---

# 83. Common Interview Traps

> [!warning]
> **Trap 1**
>
> `Address` is always simple.
>
> Wrong.
>
> It can be composite:
>
> ```text
> Address
> → Street
> → City
> → State
> → PIN
> ```

> [!warning]
> **Trap 2**
>
> Multiple values mean composite.
>
> Wrong.
>
> ```text
> Composite
> → Components
>
> Multivalued
> → Multiple Values
> ```

> [!warning]
> **Trap 3**
>
> Age must always be stored.
>
> Wrong.
>
> Age can be derived from DOB.

> [!warning]
> **Trap 4**
>
> Weak entity has no attributes.
>
> Wrong.
>
> A weak entity can have several attributes, including a partial key.

> [!warning]
> **Trap 5**
>
> Every attribute must have exactly one value.
>
> Not necessarily in conceptual ER modeling. Multivalued attributes are allowed, although relational implementations commonly normalize them.

---

# 84. Master Comparison Table

| Type | Main Question | Example |
|---|---|---|
| Simple | Can it be meaningfully divided? No | Age |
| Composite | Can it be divided? Yes | Address |
| Single-Valued | One value? | DOB |
| Multivalued | Multiple values? | Phone |
| Stored | Directly stored? | DOB |
| Derived | Calculated? | Age |
| Key | Identifies entity? | Student_ID |
| Optional | Can value be absent? | Middle_Name |
| Complex | Composite + Multivalued | Multiple Addresses |

---

# 85. Golden Classification Examples

~~~text
Student_ID
→ Simple + Single-Valued + Stored + Key

Name
→ Potentially Composite + Single-Valued + Stored

Address
→ Potentially Composite

Phone
→ Potentially Multivalued

DOB
→ Simple + Single-Valued + Stored

Age
→ Derived

Skills
→ Multivalued

Department_ID
→ Simple + Single-Valued + Stored + Potential Key/Foreign Key depending on context
~~~

---

# 86. Formula Sheet

~~~text
ATTRIBUTE
→ Property describing an entity or relationship


SIMPLE
→ Cannot be meaningfully divided


COMPOSITE
→ Can be divided into meaningful sub-attributes


SINGLE-VALUED
→ One value per entity instance


MULTIVALUED
→ Multiple values per entity instance


STORED
→ Directly stored


DERIVED
→ Calculated from other attributes


KEY ATTRIBUTE
→ Uniquely identifies entity instance


PARTIAL KEY
→ Identifies weak entity within owner context


COMPLEX ATTRIBUTE
→ Composite + Multivalued


ER NOTATION

Attribute
→ Single Oval

Composite
→ Parent Oval + Sub-Ovals

Multivalued
→ Double Oval

Derived
→ Dashed Oval

Key Attribute
→ Underlined


MEMORY

Composite
→ Break

Multivalued
→ Many

Derived
→ Calculate

Stored
→ Save

Key
→ Identify
~~~

---

# 87. Quick Revision

> [!summary] One-Minute Revision

~~~text
ATTRIBUTE
→ Property/characteristic describing an entity or relationship.

ENTITY
→ Object

ATTRIBUTE
→ Information about the object


MAIN TYPES

SIMPLE
→ Cannot be meaningfully divided.

COMPOSITE
→ Can be divided into meaningful components.

SINGLE-VALUED
→ One value.

MULTIVALUED
→ Multiple values.

STORED
→ Directly stored.

DERIVED
→ Calculated.

KEY
→ Identifies entity instance.

OPTIONAL
→ May have no value.

COMPLEX
→ Composite + Multivalued.


EXAMPLES

Student_ID
→ Key + Simple + Single-Valued + Stored

Name
→ Composite, if First/Middle/Last are modeled separately

Address
→ Composite

Phone
→ Multivalued, if multiple numbers are allowed

DOB
→ Stored

Age
→ Derived

Skills
→ Multivalued


ER NOTATION

Single Oval
→ Attribute

Double Oval
→ Multivalued

Dashed Oval
→ Derived

Underline
→ Key

Parent Oval + Child Ovals
→ Composite


FAST RECOGNITION

Can break?
→ Composite

Multiple values?
→ Multivalued

Calculated?
→ Derived

Directly saved?
→ Stored

Unique identifier?
→ Key


IMPORTANT DISTINCTIONS

Composite
→ Components

Multivalued
→ Multiple values

Stored
→ Save

Derived
→ Calculate

Entity
→ Object

Attribute
→ Property


DESIGN FLOW

Entity
↓
Attributes
↓
Classify Attributes
↓
Identify Keys
↓
Identify Relationships
↓
Determine Cardinality
↓
Build ER Diagram
~~~

---

# 88. Golden Memory Trick

**Attribute = What information do I need to store about this entity?**

# 89. One-Line Recognition

**If something describes the properties, characteristics, identity, or state of an entity, think Attribute.**