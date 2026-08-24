---
type: concept
subject: dbms
topic: "Entity"
parent: "ER Model"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - dbms
  - er-model
  - entity
  - database-design
  - conceptual-model
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
  - "[[Attribute]]"
  - "[[Relationship]]"
  - "[[Cardinality]]"
  - "[[ER Diagram]]"
  - "[[Relational Model]]"
  - "[[Primary Key]]"
  - "[[Database]]"
---

# Entity

## 1. Core Concept

> [!summary]
> An **Entity** is a real-world object, person, place, thing, event, or concept about which the database stores information.

Simple idea:

~~~text
Real-World Object
       ↓
    ENTITY
       ↓
Database stores information about it
~~~

Examples:

~~~text
Student
Employee
Customer
Product
Doctor
Patient
Course
Department
Bank Account
Book
Order
~~~

If something has information that the database needs to remember, it can potentially be modeled as an entity.

---

# 2. Basic Meaning

Suppose we are designing a college database.

Real world:

~~~text
Students
Teachers
Courses
Departments
Classrooms
Exams
~~~

The database may model these as entities:

~~~text
STUDENT
TEACHER
COURSE
DEPARTMENT
CLASSROOM
EXAM
~~~

Each entity represents a meaningful object or concept in the system.

---

# 3. Entity in Simple English

Think of an entity as:

> **"A thing about which I want to store data."**

For example:

~~~text
Student
```

We may want to store:

~~~text
Student ID
Name
Email
Department
CGPA
~~~

Therefore:

~~~text
Student
→ Entity

Student ID, Name, Email, Department, CGPA
→ Attributes
~~~

This distinction is extremely important.

---

# 4. Entity vs Attribute

A common beginner mistake is confusing an entity with an attribute.

Consider:

~~~text
Student
    |
    +--- Student_ID
    +--- Name
    +--- Email
    +--- CGPA
~~~

Here:

~~~text
Student
→ Entity

Student_ID
Name
Email
CGPA
→ Attributes
~~~

Memory:

~~~text
ENTITY
→ What object?

ATTRIBUTE
→ What information about the object?
~~~

---

# 5. Real-Time Example — College

Suppose the system manages students.

Entity:

~~~text
STUDENT
~~~

Attributes:

~~~text
Student_ID
Name
Age
Department
CGPA
Email
~~~

Possible entity instance:

~~~text
Student_ID = 101
Name = Pradeep
Age = 21
Department = CSE
CGPA = 8.5
~~~

The entity represents the concept `Student`.

The individual student is an **entity instance**.

---

# 6. Entity Type

An **Entity Type** defines a collection of similar entities that share the same attributes.

Example:

~~~text
ENTITY TYPE
    ↓
STUDENT
~~~

Possible instances:

~~~text
Student 101
Student 102
Student 103
Student 104
~~~

All of them belong to the same entity type:

~~~text
STUDENT
~~~

Think:

~~~text
Entity Type
→ Category / Definition

Entity Instance
→ Individual Object
~~~

---

# 7. Entity Instance

An **entity instance** is one specific occurrence of an entity type.

Example:

Entity Type:

~~~text
STUDENT
~~~

Instances:

~~~text
Student 101
Student 102
Student 103
~~~

Another example:

~~~text
Entity Type
→ EMPLOYEE

Instances
→ Employee E101
→ Employee E102
→ Employee E103
~~~

---

# 8. Entity Type vs Entity Instance

| Concept | Meaning | Example |
|---|---|---|
| Entity Type | General category | STUDENT |
| Entity Instance | Specific occurrence | Student 101 |
| Entity | Real-world object/concept | Student |
| Attribute | Property | Name, CGPA |

Shortcut:

~~~text
TYPE
→ Blueprint / category

INSTANCE
→ Actual object
~~~

---

# 9. Strong Entity

A **strong entity** is an entity that can exist independently and has its own key attribute to uniquely identify its instances.

Example:

~~~text
STUDENT
---------
Student_ID
Name
CGPA
~~~

`Student_ID` can uniquely identify a student.

Therefore:

~~~text
STUDENT
→ Strong Entity
~~~

A strong entity does not depend on another entity for its existence.

---

# 10. Strong Entity Example

Consider:

~~~text
EMPLOYEE
---------
Employee_ID
Name
Salary
Department
~~~

If `Employee_ID` uniquely identifies each employee:

~~~text
Employee
→ Strong Entity
~~~

The employee has its own identifying key.

---

# 11. Weak Entity

A **weak entity** cannot be uniquely identified using its own attributes alone and depends on another entity for identification and/or existence.

Example:

~~~text
EMPLOYEE
   |
   ↓
DEPENDENT
~~~

Suppose a dependent is identified using:

~~~text
Employee_ID
+
Dependent_Name
~~~

The dependent's identity depends partly on the owning employee.

Therefore:

~~~text
DEPENDENT
→ Weak Entity
~~~

---

# 12. Strong vs Weak Entity

| Feature | Strong Entity | Weak Entity |
|---|---|---|
| Independent existence | Yes | Depends on owner entity |
| Own complete key | Yes | No complete key of its own |
| Identification | Own key | Owner key + partial key |
| ER notation | Single rectangle | Double rectangle |
| Dependency | Independent | Dependent |

Memory:

~~~text
Strong
→ Stands Alone

Weak
→ Needs Owner
~~~

---

# 13. Weak Entity Real-Time Example

Consider an employee and their dependents.

~~~text
EMPLOYEE
---------
Employee_ID
Name

DEPENDENT
---------
Dependent_Name
Age
Relationship
~~~

Suppose two employees can both have a dependent named `Rahul`.

Then:

~~~text
Dependent_Name
```

alone is not enough to uniquely identify the dependent.

We may need:

~~~text
Employee_ID
+
Dependent_Name
~~~

Therefore the dependent is modeled as a weak entity.

---

# 14. Partial Key

A weak entity commonly has a **partial key**, also called a discriminator.

Example:

~~~text
DEPENDENT
---------
Dependent_Name
Age
Relationship
~~~

`Dependent_Name` may distinguish dependents belonging to the same employee.

But it may not uniquely identify a dependent across the entire database.

Therefore:

~~~text
Partial Key
→ Helps identify a weak entity within its owner context
~~~

---

# 15. Owner Entity

The strong entity on which a weak entity depends is called its **owner entity**.

Example:

~~~text
EMPLOYEE
    |
    |
    ↓
DEPENDENT
~~~

Here:

~~~text
Employee
→ Owner Entity

Dependent
→ Weak Entity
~~~

---

# 16. Identifying Relationship

The relationship connecting a weak entity to its owner entity is called an **identifying relationship**.

Example:

~~~text
EMPLOYEE
    ||
    ||
    DEPENDENT
~~~

Conceptually:

~~~text
Employee
→ Owner

Dependent
→ Weak Entity

Their identifying relationship
→ Establishes dependency
~~~

---

# 17. ER Diagram Notation for Entity

In an ER diagram, a strong entity is commonly represented using a rectangle.

Example:

~~~text
+-------------+
|   STUDENT   |
+-------------+
~~~

The rectangle represents the entity type.

---

# 18. Weak Entity Notation

A weak entity is commonly represented using a double rectangle.

Example:

~~~text
+===============+
||  DEPENDENT  ||
+===============+
~~~

The exact visual style may vary by diagramming tool, but the exam convention is:

~~~text
Single Rectangle
→ Strong Entity

Double Rectangle
→ Weak Entity
~~~

---

# 19. Entity Recognition Trick

> [!important]
> Ask:
>
> **"Is this a thing/object/concept about which the database stores information?"**
>
> If yes, it is a strong candidate for an **Entity**.

Example:

~~~text
Student
→ Entity

Student Name
→ Attribute

Student studies Course
→ Relationship
~~~

---

# 20. Entity vs Relationship

Consider:

~~~text
STUDENT
    |
   enrolls
    |
   COURSE
~~~

Here:

~~~text
STUDENT
→ Entity

COURSE
→ Entity

ENROLLS
→ Relationship
~~~

The entities are the objects.

The relationship describes how they are connected.

Memory:

~~~text
NOUN
→ Often Entity

VERB
→ Often Relationship
~~~

Example:

~~~text
Student
   enrolls in
Course
~~~

`Student` and `Course` are entities.

`enrolls in` is a relationship.

This is a useful modeling trick, though context always matters.

---

# 21. Entity vs Attribute vs Relationship

> [!important]
> Use the **EAR** shortcut:
>
> **E = Entity**
>
> **A = Attribute**
>
> **R = Relationship**

Example:

~~~text
Student
   |
   +--- Name
   +--- CGPA
   |
   +--- enrolls in
             |
           Course
~~~

Therefore:

~~~text
Student
→ Entity

Name
CGPA
→ Attributes

enrolls in
→ Relationship

Course
→ Entity
~~~

---

# 22. Entity Identification Pattern

When designing an ER model from a paragraph:

### Step 1

Find important nouns.

### Step 2

Ask whether they represent objects/concepts about which data is stored.

### Step 3

Candidate entities emerge.

Example:

> A college has students and courses. Students enroll in courses.

Important nouns:

~~~text
College
Students
Courses
~~~

Potential entities:

~~~text
COLLEGE
STUDENT
COURSE
~~~

Relationship:

~~~text
ENROLLS
~~~

---

# 23. Real-Time Example — E-Commerce

Suppose:

> Customers place orders. Orders contain products.

Candidate entities:

~~~text
CUSTOMER
ORDER
PRODUCT
~~~

Relationships:

~~~text
CUSTOMER
    |
  places
    |
   ORDER

ORDER
   |
 contains
   |
 PRODUCT
~~~

Attributes might include:

~~~text
Customer
→ Customer_ID
→ Name
→ Email

Order
→ Order_ID
→ Order_Date

Product
→ Product_ID
→ Product_Name
→ Price
~~~

---

# 24. Real-Time Example — Banking

Potential entities:

~~~text
CUSTOMER
ACCOUNT
BRANCH
LOAN
TRANSACTION
```

Relationships:

~~~text
Customer
   |
owns
   |
Account

Account
   |
has
   |
Transaction
```

Attributes:

~~~text
Customer
→ Customer_ID
→ Name

Account
→ Account_Number
→ Balance
```

This is the basic thought process behind ER modeling.

---

# 25. Real-Time Example — Hospital

Potential entities:

~~~text
PATIENT
DOCTOR
APPOINTMENT
MEDICINE
LAB_REPORT
```

Relationships:

~~~text
Patient
   |
books
   |
Appointment

Doctor
   |
handles
   |
Appointment
~~~

The key is to identify what the system must store information about.

---

# 26. Real-Time Example — Online Learning Platform

Potential entities:

~~~text
STUDENT
COURSE
INSTRUCTOR
LESSON
CERTIFICATE
EXAM
```

Relationships:

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

Course
   |
contains
   |
Lesson
~~~

Each entity can have its own attributes.

---

# 27. Real-Time Example — Food Delivery

Potential entities:

~~~text
CUSTOMER
RESTAURANT
ORDER
DELIVERY_PARTNER
FOOD_ITEM
PAYMENT
```

Relationships:

~~~text
Customer
   |
places
   |
Order

Restaurant
   |
prepares
   |
Order

Delivery Partner
   |
delivers
   |
Order
~~~

This demonstrates how real-world nouns become candidate entities.

---

# 28. Real-Time Example — Library

Potential entities:

~~~text
BOOK
MEMBER
LIBRARIAN
AUTHOR
PUBLISHER
LOAN
```

Relationships:

~~~text
Member
   |
borrows
   |
Book

Author
   |
writes
   |
Book
~~~

A library system is a classic ER-modeling example.

---

# 29. Entity Set

An **entity set** is a collection of entities of the same type.

Example:

~~~text
STUDENT ENTITY SET

Student 101
Student 102
Student 103
Student 104
~~~

All these students belong to the same entity set.

Similarly:

~~~text
EMPLOYEE ENTITY SET

Employee 1
Employee 2
Employee 3
~~~

---

# 30. Entity Set vs Entity

This distinction is important.

~~~text
Student 101
→ Individual Entity Instance

Student 102
→ Individual Entity Instance

Student 103
→ Individual Entity Instance
~~~

Together:

~~~text
STUDENT
→ Entity Set
~~~

Think:

~~~text
Entity
→ One Object

Entity Set
→ Collection of Similar Objects
~~~

---

# 31. Entity Type vs Entity Set

These concepts can be confusing.

### Entity Type

Describes the structure/category.

~~~text
STUDENT
---------
Student_ID
Name
CGPA
~~~

### Entity Set

Collection of current entity instances.

~~~text
Student 101
Student 102
Student 103
~~~

Memory:

~~~text
Entity Type
→ Definition

Entity Set
→ Collection
~~~

---

# 32. Entity Attribute Connection

An entity is described using attributes.

Example:

~~~text
STUDENT
---------
Student_ID
Name
Email
CGPA
Department
~~~

Here:

~~~text
Entity
→ STUDENT

Attributes
→ Student_ID
→ Name
→ Email
→ CGPA
→ Department
~~~

The entity tells us **what object**.

The attributes tell us **what properties**.

---

# 33. Key Attribute

An entity often has an attribute that uniquely identifies its instances.

Example:

~~~text
STUDENT
---------
Student_ID
Name
CGPA
~~~

If:

~~~text
Student_ID
```

is unique, it acts as the identifying key.

In ER diagrams, a key attribute is commonly shown as an **underlined attribute**.

Conceptually:

~~~text
Student_ID
-----------
KEY
~~~

---

# 34. Entity Identification

To uniquely identify an entity instance, ask:

> "What value distinguishes this object from every other object of the same entity type?"

For students:

~~~text
Student_ID
~~~

For employees:

~~~text
Employee_ID
~~~

For products:

~~~text
Product_ID
~~~

For bank accounts:

~~~text
Account_Number
~~~

---

# 35. Strong Entity Recognition

> [!important]
> If the entity:
>
> 1. Has its own identifying key
> 2. Can exist independently
>
> think:
>
> **Strong Entity**

Example:

~~~text
STUDENT
---------
Student_ID
Name
~~~

---

# 36. Weak Entity Recognition

> [!important]
> If the entity:
>
> 1. Cannot be uniquely identified by its own attributes
> 2. Depends on another entity
>
> think:
>
> **Weak Entity**

Example:

~~~text
EMPLOYEE
   |
   ↓
DEPENDENT
~~~

---

# 37. Strong Entity vs Weak Entity — Exam Table

| Feature | Strong Entity | Weak Entity |
|---|---|---|
| Independent existence | Yes | No / existence-dependent |
| Own complete key | Yes | No |
| Identification | Own key | Owner key + partial key |
| Diagram | Single rectangle | Double rectangle |
| Owner dependency | No | Yes |
| Identifying relationship | Not required | Required |

---

# 38. Important Weak Entity Pattern

Memorize:

~~~text
Owner Entity
     ↓
Identifying Relationship
     ↓
Weak Entity
```

Identification:

~~~text
Owner Primary Key
+
Weak Entity Partial Key
=
Weak Entity Identification
~~~

This is one of the most important ER-model interview concepts.

---

# 39. Entity Modeling Trick

When given a real-world problem, use:

~~~text
NOUNS
→ Candidate Entities

PROPERTIES
→ Candidate Attributes

VERBS
→ Candidate Relationships
~~~

Example:

> Students enroll in courses.

Nouns:

~~~text
Students
Courses
~~~

Entities:

~~~text
STUDENT
COURSE
~~~

Verb:

~~~text
enroll
~~~

Relationship:

~~~text
ENROLLS
~~~

This trick is extremely useful during ER-diagram design questions.

---

# 40. Advanced Entity Identification

Not every noun should automatically become an entity.

Consider:

> A student has a name.

Possible interpretation:

~~~text
Student
→ Entity

Name
→ Attribute
~~~

Why is `Name` not necessarily an entity?

Because it is simply a property describing the student.

---

# 41. When Does an Attribute Become an Entity?

Suppose a simple design contains:

~~~text
Student
---------
Department
```

If the system only needs the department name, `Department` might be represented as an attribute.

But if the system needs to store:

~~~text
Department_ID
Department_Name
HOD
Location
Budget
Courses
```

then `Department` is clearly a meaningful object with its own information.

It should generally be modeled as an entity.

This is an important modeling judgment.

---

# 42. Entity or Attribute?

Ask:

~~~text
Does it have its own properties?
        ↓
Does it need independent identification?
        ↓
Does the system manage it separately?
        ↓
Can it participate in relationships?
~~~

If several answers are yes:

**Consider modeling it as an entity.**

Example:

~~~text
Student
   |
Department
```

If department has:

~~~text
Department_ID
Name
HOD
Location
Budget
~~~

then `Department` is likely an entity.

---

# 43. Entity or Attribute — Example

### Question

In a student database, should `Department` be an attribute or entity?

### Case 1

Only need:

~~~text
Student
---------
Name
Department
```

Then:

~~~text
Department
→ Could be an attribute
~~~

### Case 2

Need:

~~~text
Department
---------
Department_ID
Name
HOD
Office
Budget
```

Then:

~~~text
Department
→ Entity
~~~

The correct answer depends on the requirements.

---

# 44. Entity or Relationship?

Consider:

~~~text
Student enrolls in Course
~~~

Candidate entities:

~~~text
Student
Course
~~~

Relationship:

~~~text
Enrolls
~~~

But suppose enrollment itself has important information:

~~~text
Enrollment_Date
Grade
Semester
Status
```

Then:

~~~text
ENROLLMENT
```

may be modeled as an associative entity or relationship with attributes, depending on the ER modeling approach.

This is an important advanced design pattern.

---

# 45. Associative Entity

An associative entity is commonly used to represent a many-to-many relationship as a separate entity.

Example:

~~~text
STUDENT
   |
   |
   ↓
ENROLLMENT
   ↑
   |
   |
COURSE
~~~

Enrollment may contain:

~~~text
Student_ID
Course_ID
Enrollment_Date
Grade
Semester
```

This is extremely common in relational database design.

---

# 46. Why Associative Entities Matter

Suppose:

~~~text
Student
   ↕
Course
~~~

is many-to-many.

A relational implementation often uses:

~~~text
Student
Course
Enrollment
~~~

The `Enrollment` relation connects the two.

This is one of the most important bridges between:

~~~text
ER Model
        ↓
Relational Model
~~~

---

# 47. Entity Lifecycle Thinking

A useful advanced modeling question is:

> "Can this object exist independently?"

Example:

~~~text
Employee
```

An employee can exist independently.

But:

~~~text
Dependent
```

may depend on an employee.

Therefore:

~~~text
Employee
→ Strong Entity

Dependent
→ Weak Entity
```

This is a powerful way to recognize weak entities.

---

# 48. Entity Independence Test

> [!tip]
> Ask:
>
> **"If I remove the parent/owner, can this object still logically exist in this database context?"**

If yes:

~~~text
Possibly Strong Entity
~~~

If no:

~~~text
Possibly Weak Entity
~~~

This is a useful heuristic, but the final classification depends on the database requirements and identification rules.

---

# 49. Entity Identification Test

Use the **K-I-R test**:

~~~text
K → Does it have its own key?

I → Can it exist independently?

R → Does it have its own relationships/properties?
~~~

If:

~~~text
K = Yes
I = Yes
```

strong entity is likely.

If:

~~~text
K = No
I = No
```

weak entity is likely.

---

# 50. Common Entity Types in Applications

| Application | Possible Entities |
|---|---|
| College | Student, Course, Faculty, Department |
| Banking | Customer, Account, Loan, Branch |
| Hospital | Patient, Doctor, Appointment |
| E-commerce | Customer, Product, Order |
| Library | Book, Member, Author, Loan |
| Airline | Passenger, Flight, Airport, Ticket |
| Hotel | Guest, Room, Booking |
| Food Delivery | Customer, Restaurant, Order |
| Job Portal | Candidate, Company, Job, Application |
| Online Course | Student, Course, Instructor, Exam |

---

# 51. Entity Recognition in Interviews

If an interviewer gives:

> "Design a database for Amazon-like shopping."

Do not immediately create tables.

First identify entities:

~~~text
Customer
Product
Order
Payment
Address
Cart
Seller
Shipment
Review
```

Then identify:

~~~text
Attributes
+
Relationships
+
Cardinalities
+
Keys
~~~

This is the professional ER-design approach.

---

# 52. Entity Identification Workflow

Use this process:

~~~text
STEP 1
Read the requirements
        ↓
STEP 2
Find important nouns
        ↓
STEP 3
Identify candidate entities
        ↓
STEP 4
Remove things that are only attributes
        ↓
STEP 5
Identify keys
        ↓
STEP 6
Identify relationships
        ↓
STEP 7
Check strong/weak dependency
        ↓
STEP 8
Determine cardinality
        ↓
STEP 9
Draw ER diagram
~~~

This workflow is extremely useful for interviews.

---

# 53. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Every Noun Is an Entity

Wrong.

A noun may be:

~~~text
Entity
Attribute
Relationship
```

Example:

~~~text
Student Name
```

`Name` is usually an attribute.

---

### Mistake 2 — Entity and Attribute Are the Same

Wrong.

~~~text
Student
→ Entity

Name
→ Attribute
~~~

---

### Mistake 3 — Entity and Entity Instance Are the Same

Not exactly.

~~~text
STUDENT
→ Entity Type

Student 101
→ Entity Instance
~~~

---

### Mistake 4 — Weak Entity Has No Attributes

Wrong.

A weak entity can have its own attributes.

The key issue is its identification/existence dependency.

---

### Mistake 5 — Weak Entity Has No Key Information

A weak entity does not have a complete key of its own, but it typically has a partial key that combines with the owner's key for identification.

---

### Mistake 6 — Weak Entity Means Unimportant Entity

Wrong.

"Weak" refers to dependency in identification/existence, not importance.

---

### Mistake 7 — Every Department Must Be an Entity

Not necessarily.

It depends on the requirements.

If department has its own properties and relationships, modeling it as an entity is usually appropriate.

---

### Mistake 8 — Every Relationship Must Become an Entity

Not always.

A relationship can be represented directly unless it needs independent attributes/identity or the modeling requirements call for an associative entity.

---

# 54. Common Exam Patterns

> [!important] Must Master

1. Definition of entity
2. Entity type
3. Entity instance
4. Entity set
5. Strong entity
6. Weak entity
7. Owner entity
8. Partial key
9. Identifying relationship
10. Entity vs attribute
11. Entity vs relationship
12. Entity type vs entity instance
13. Entity set vs entity
14. Strong vs weak entity
15. Entity identification
16. Key attribute
17. ER diagram notation
18. Associative entity
19. Real-world entity identification
20. Noun-based ER modeling
21. Entity lifecycle
22. Independent vs dependent entities
23. Many-to-many relationship modeling
24. Entity-to-relational mapping

---

# 55. Interview Questions

## Q1. What is an entity?

### Strong Answer

> An entity is a distinguishable real-world object, person, place, event, or concept about which the database stores information.

Example:

~~~text
Student
Employee
Product
Customer
~~~

---

## Q2. What is an entity type?

### Answer

> An entity type defines a collection of similar entities that share the same attributes.

Example:

~~~text
STUDENT
---------
Student_ID
Name
CGPA
~~~

---

## Q3. What is an entity instance?

### Answer

> An entity instance is one specific occurrence of an entity type.

Example:

~~~text
Student_ID = 101
Name = Pradeep
~~~

is one instance of:

~~~text
STUDENT
~~~

---

# 56. Interview Questions — Entity Set

## Q4. What is an entity set?

### Answer

> An entity set is a collection of entities of the same entity type.

Example:

~~~text
Student 101
Student 102
Student 103
~~~

together form the:

~~~text
STUDENT ENTITY SET
~~~

---

# 57. Interview Questions — Strong Entity

## Q5. What is a strong entity?

### Answer

> A strong entity can exist independently and has its own key that uniquely identifies its instances.

Example:

~~~text
STUDENT
---------
Student_ID
Name
~~~

---

# 58. Interview Questions — Weak Entity

## Q6. What is a weak entity?

### Strong Answer

> A weak entity is an entity whose identification and/or existence depends on another owner entity. It does not have a complete identifying key of its own and typically uses a partial key together with the owner's key.

Example:

~~~text
EMPLOYEE
   |
   ↓
DEPENDENT
~~~

---

# 59. Interview Questions — Strong vs Weak

## Q7. Difference between strong and weak entity?

### Answer

~~~text
Strong Entity
→ Independent
→ Own key
→ Single rectangle

Weak Entity
→ Dependent
→ Partial key + owner key
→ Double rectangle
~~~

---

# 60. Interview Questions — Entity vs Attribute

## Q8. How do you decide whether something should be an entity or attribute?

### Strong Answer

> I check whether it represents an independently managed object with its own properties, identity, or relationships. If it only describes another object and does not need independent management, it is usually modeled as an attribute.

Example:

~~~text
Student
   |
   +--- Name
   +--- CGPA
~~~

Here:

~~~text
Student
→ Entity

Name
CGPA
→ Attributes
~~~

---

# 61. Advanced Interview Question

## Q9. Can an entity become an attribute in another design?

### Answer

Yes.

The modeling decision depends on requirements.

For example:

~~~text
Student
---------
Name
Department
```

If only the department name is needed, `Department` may be represented as an attribute.

But if department has:

~~~text
Department_ID
Name
HOD
Budget
Office
```

then it is likely better represented as an entity.

The key principle is:

> **Model according to the information and relationships the system needs to manage.**

---

# 62. Advanced Interview Question

## Q10. What is a partial key?

### Answer

> A partial key is an attribute or set of attributes that helps distinguish weak-entity instances belonging to the same owner, but does not uniquely identify the weak entity globally by itself.

Example:

~~~text
Employee_ID + Dependent_Name
~~~

can identify a dependent.

---

# 63. Advanced Interview Question

## Q11. What is an identifying relationship?

### Answer

> It is the relationship that connects a weak entity to its owner entity and participates in identifying the weak entity.

Conceptually:

~~~text
Owner Entity
      ||
      ||
Weak Entity
~~~

---

# 64. Advanced Interview Question

## Q12. Why is a weak entity called "weak"?

### Answer

Because its identification and/or existence depends on another entity.

It does not mean the entity is less important.

Memory:

~~~text
Weak
→ Dependency
NOT
→ Importance
~~~

---

# 65. Advanced Interview Question

## Q13. Give a real-world example of a weak entity.

### Answer

An employee's dependent is a common example.

~~~text
EMPLOYEE
   |
   ↓
DEPENDENT
~~~

A dependent may be identified using:

~~~text
Employee_ID
+
Dependent_Name
~~~

---

# 66. Advanced Interview Question

## Q14. What is an associative entity?

### Answer

> An associative entity is used to represent a many-to-many relationship as a separate entity, often storing relationship-specific attributes.

Example:

~~~text
STUDENT
   |
   ↓
ENROLLMENT
   ↑
   |
COURSE
~~~

Attributes:

~~~text
Student_ID
Course_ID
Enrollment_Date
Grade
Semester
~~~

---

# 67. Advanced Interview Question

## Q15. How do you identify entities from a problem statement?

### Strong Answer

> I first identify important nouns, then determine which nouns represent independently managed objects or concepts. I separate attributes from entities, identify keys, and then identify relationships and cardinalities.

Shortcut:

~~~text
Nouns
→ Candidate Entities

Properties
→ Attributes

Verbs
→ Relationships
~~~

---

# 68. Advanced Interview Question — Design Thinking

## Question

Design an ER model for an online shopping system. What entities would you identify first?

### Answer

Possible entities:

~~~text
Customer
Product
Order
Payment
Address
Seller
Shipment
Review
Cart
~~~

Then identify:

~~~text
Attributes
+
Keys
+
Relationships
+
Cardinality
+
Constraints
~~~

The exact model depends on the requirements.

---

# 69. IIT-Level Thinking Pattern

When given any database design problem, use:

~~~text
REAL WORLD
    ↓
What objects exist?
    ↓
ENTITIES
    ↓
What describes them?
    ↓
ATTRIBUTES
    ↓
How are they connected?
    ↓
RELATIONSHIPS
    ↓
How many participate?
    ↓
CARDINALITY
    ↓
Can every entity exist independently?
    ↓
STRONG / WEAK
    ↓
How is each identified?
    ↓
KEYS
~~~

This is the core ER-modeling mindset.

---

# 70. Entity Recognition Master Table

| Question | Think |
|---|---|
| What object does the system manage? | Entity |
| What property describes it? | Attribute |
| How are two objects connected? | Relationship |
| How many objects participate? | Cardinality |
| Can it exist independently? | Strong/Weak |
| What uniquely identifies it? | Key |
| Collection of similar entities? | Entity Set |
| General definition/category? | Entity Type |
| Specific occurrence? | Entity Instance |
| Dependent object? | Weak Entity |
| Owner of weak entity? | Strong/Owner Entity |
| Partial identifier? | Partial Key |
| Relationship identifying weak entity? | Identifying Relationship |

---

# 71. Fast Entity Identification Shortcut

> [!tip]
> Use the **O-P-C test**:
>
> **O = Object**
>
> **P = Properties**
>
> **C = Connection**
>
> Ask:
>
> What is the **Object**?
>
> What are its **Properties**?
>
> What is its **Connection** to other objects?
>
> Therefore:
>
> Object → Entity
>
> Properties → Attributes
>
> Connection → Relationship

---

# 72. Strong vs Weak Shortcut

> [!tip]
> Remember:
>
> **Strong = Stand Alone**
>
> **Weak = Needs Owner**

Example:

~~~text
Employee
→ Strong

Dependent
→ Weak
~~~

---

# 73. Entity vs Attribute Shortcut

> [!tip]
> Ask:
>
> **"Can this thing have its own information and relationships?"**
>
> If yes:
>
> Consider an Entity.
>
> If it simply describes another object:
>
> Consider an Attribute.

---

# 74. Entity vs Relationship Shortcut

> [!tip]
> Think:
>
> **Noun → Entity**
>
> **Verb → Relationship**
>
> Example:
>
> Student
> enrolls
> Course
>
> Student → Entity
>
> Course → Entity
>
> Enrolls → Relationship

This is a heuristic, not an absolute grammatical rule.

---

# 75. Common Entity Modeling Patterns

## Pattern 1 — Independent Object

~~~text
STUDENT
EMPLOYEE
PRODUCT
CUSTOMER
~~~

Usually strong entities.

---

## Pattern 2 — Dependent Object

~~~text
EMPLOYEE
   ↓
DEPENDENT
~~~

Potential weak entity.

---

## Pattern 3 — Many-to-Many

~~~text
STUDENT
   ↕
COURSE
~~~

Potential associative entity:

~~~text
ENROLLMENT
~~~

---

## Pattern 4 — Object With Rich Properties

~~~text
DEPARTMENT
---------
ID
Name
HOD
Location
Budget
~~~

Strong candidate for an entity.

---

## Pattern 5 — Simple Property

~~~text
STUDENT
---------
Name
Age
CGPA
~~~

These are attributes.

---

# 76. Placement Exam Focus

### Very High Priority

- Entity definition
- Entity type
- Entity instance
- Entity set
- Strong entity
- Weak entity
- Strong vs weak
- Partial key
- Owner entity
- Identifying relationship
- Entity vs attribute

### High Priority

- ER notation
- Entity identification
- Associative entity
- Real-world examples
- Entity modeling patterns

### Interview Priority

- How to identify entities
- Entity vs attribute decision
- Entity vs relationship
- Strong vs weak entity
- Weak entity example
- Associative entity
- ER-to-relational conversion

---

# 77. Common Interview Trap Questions

## Trap 1

**Is every noun an entity?**

Answer:

No.

A noun can represent an entity, attribute, or even part of a relationship depending on the requirements.

---

## Trap 2

**Is every entity strong?**

Answer:

No.

Weak entities exist and depend on owner entities.

---

## Trap 3

**Does weak mean unimportant?**

Answer:

No.

Weak refers to identification/existence dependency.

---

## Trap 4

**Can an entity have attributes?**

Answer:

Yes.

Attributes describe entities.

---

## Trap 5

**Can an entity participate in multiple relationships?**

Answer:

Yes.

For example:

~~~text
Student
   |
   +--- enrolls → Course
   |
   +--- belongs → Department
   |
   +--- lives → Hostel
~~~

---

# 78. Formula Sheet

~~~text
ENTITY
→ Real-world object/concept about which data is stored


ENTITY TYPE
→ General definition/category


ENTITY INSTANCE
→ Specific occurrence


ENTITY SET
→ Collection of similar entity instances


STRONG ENTITY
→ Independent + own identifying key


WEAK ENTITY
→ Depends on owner entity


PARTIAL KEY
→ Identifies weak entity within owner context


OWNER ENTITY
→ Entity on which weak entity depends


IDENTIFYING RELATIONSHIP
→ Connects weak entity to owner


ER IDENTIFICATION

Noun
→ Candidate Entity

Property
→ Attribute

Verb/Connection
→ Relationship


STRONG vs WEAK

Strong
→ Stand Alone

Weak
→ Needs Owner


COMMON ER NOTATION

Strong Entity
→ Single Rectangle

Weak Entity
→ Double Rectangle

Key Attribute
→ Underlined Attribute
~~~

---

# 79. Quick Revision

> [!summary] One-Minute Revision

~~~text
ENTITY
→ Real-world object, person, place, event, or concept about which data is stored.

ENTITY TYPE
→ General category/definition.

ENTITY INSTANCE
→ One specific occurrence.

ENTITY SET
→ Collection of similar instances.

EXAMPLE

STUDENT
→ Entity Type

Student 101
→ Entity Instance

Student 101, 102, 103
→ Entity Set


STRONG ENTITY
→ Can exist independently.
→ Has its own identifying key.
→ Single rectangle.


WEAK ENTITY
→ Depends on owner entity.
→ No complete key of its own.
→ Uses partial key + owner key.
→ Double rectangle.


OWNER ENTITY
→ Strong entity on which weak entity depends.


PARTIAL KEY
→ Identifies weak entity within its owner's context.


IDENTIFYING RELATIONSHIP
→ Connects weak entity to owner.


ENTITY vs ATTRIBUTE

Student
→ Entity

Name
CGPA
Email
→ Attributes


ENTITY vs RELATIONSHIP

Student
→ Entity

Course
→ Entity

Enrolls
→ Relationship


MODELING SHORTCUT

Nouns
→ Candidate Entities

Properties
→ Attributes

Verbs
→ Relationships


STRONG/WEAK SHORTCUT

Strong
→ Stand Alone

Weak
→ Needs Owner


DESIGN WORKFLOW

Requirements
↓
Candidate Entities
↓
Attributes
↓
Keys
↓
Relationships
↓
Cardinality
↓
Strong/Weak Analysis
↓
ER Diagram


REAL-WORLD EXAMPLES

College
→ Student, Course, Department

Bank
→ Customer, Account, Loan

Hospital
→ Patient, Doctor, Appointment

E-Commerce
→ Customer, Product, Order

Library
→ Book, Member, Author, Loan
~~~

---

# 80. Golden Memory Trick

**Entity = A meaningful real-world object or concept about which the database needs to remember information.**

# 81. One-Line Recognition

**When you see a real-world object that has its own information, identity, or relationships in a database design, think Entity.**