---
type: concept
subject: dbms
topic: "Composite Key"
parent: "Keys"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - keys
  - composite-key
  - candidate-key
  - primary-key
  - alternate-key
  - super-key
  - foreign-key
  - functional-dependency
  - relational-model
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
  - "[[Foreign Key]]"
  - "[[Candidate Key]]"
  - "[[Super Key]]"
  - "[[Alternate Key]]"
  - "[[Functional Dependency]]"
  - "[[Normalization]]"
---

# Composite Key

## 1. Core Concept

> [!summary]
> A **Composite Key** is a key made up of two or more attributes that are used together to uniquely identify a row.

The most important idea is:

**Composite = Multiple Attributes**

Example:

```text
Student_ID + Course_ID
```

Suppose:

| Student_ID | Course_ID | Grade |
|---:|---:|---|
| 101 | C01 | A |
| 101 | C02 | B |
| 102 | C01 | A |
| 102 | C02 | C |

Neither:

```text
Student_ID
```

nor:

```text
Course_ID
```

alone uniquely identifies a row.

But:

```text
(Student_ID, Course_ID)
```

does.

Therefore:

```text
(Student_ID, Course_ID)
→ Composite Key
```

If it is minimal and uniquely identifies rows:

```text
(Student_ID, Course_ID)
→ Composite Candidate Key
```

If it is selected as the primary key:

```text
(Student_ID, Course_ID)
→ Composite Primary Key
```

---

# 2. Basic Meaning

A composite key contains **more than one attribute**.

For example:

```text
(A, B)
```

is composite.

```text
(A, B, C)
```

is also composite.

The important point is that the attributes work **together**.

Example:

```text
Student_ID
```

identifies a student.

```text
Course_ID
```

identifies a course.

But:

```text
(Student_ID, Course_ID)
```

identifies a particular student's enrollment in a particular course.

---

# 3. Main Formula

There is no numerical formula, but remember:

```text
Composite Key
=
Combination of 2 or more attributes
```

If the combination uniquely identifies rows:

```text
Composite Key
→ Unique
```

If the combination is also minimal:

```text
Composite Candidate Key
```

If selected as the primary identifier:

```text
Composite Primary Key
```

---

# 4. Most Important Distinction

Do not confuse:

```text
Composite Key
```

with:

```text
Candidate Key
```

They describe different properties.

**Composite** tells us:

```text
How many attributes?
→ More than one
```

**Candidate** tells us:

```text
Is it minimal and unique?
→ Yes
```

Therefore a key can be:

```text
Composite Candidate Key
```

or:

```text
Composite Primary Key
```

or:

```text
Composite Alternate Key
```

---

# 5. Simple Example

Consider:

```text
ENROLLMENT
```

| Student_ID | Course_ID | Grade |
|---:|---|---|
| 101 | CSE101 | A |
| 101 | CSE102 | B |
| 102 | CSE101 | A |

Check:

```text
Student_ID
```

alone:

```text
101
101
102
```

Not unique.

Check:

```text
Course_ID
```

alone:

```text
CSE101
CSE102
CSE101
```

Not unique.

Check:

```text
(Student_ID, Course_ID)
```

```text
(101,CSE101)
(101,CSE102)
(102,CSE101)
```

All are unique.

Therefore:

```text
(Student_ID, Course_ID)
→ Composite Candidate Key
```

---

# 6. Recognition Trick

> [!important]
> If the question says:
>
> "No single attribute can uniquely identify the row, but a combination of attributes can"
>
> think:
>
> **Composite Key**

Example:

```text
Student_ID + Course_ID
```

---

# 7. Composite Key vs Single-Attribute Key

| Feature | Single-Attribute Key | Composite Key |
|---|---|---|
| Number of attributes | 1 | 2 or more |
| Example | `Student_ID` | `(Student_ID, Course_ID)` |
| Can uniquely identify rows | Yes | Yes |
| Can be candidate key | Yes | Yes |
| Can be primary key | Yes | Yes |
| Can be alternate key | Yes | Yes |

---

# 8. Composite Key and Candidate Key

Suppose:

```text
Student_ID
Course_ID
```

are both non-unique individually.

But:

```text
(Student_ID, Course_ID)
```

is unique.

If neither attribute can be removed:

```text
(Student_ID, Course_ID)
→ Minimal
```

Therefore:

```text
(Student_ID, Course_ID)
→ Composite Candidate Key
```

---

# 9. Composite Key and Primary Key

Suppose:

```text
(Student_ID, Course_ID)
```

is a candidate key.

If the database designer selects it as the primary key:

```text
PRIMARY KEY
(Student_ID, Course_ID)
```

Then it is a:

**Composite Primary Key**

Example:

```sql
CREATE TABLE Enrollment (
    Student_ID INT,
    Course_ID INT,
    Grade CHAR(2),
    PRIMARY KEY (Student_ID, Course_ID)
);
```

---

# 10. Composite Key and Alternate Key

Suppose candidate keys are:

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

becomes:

```text
Composite Alternate Key
```

Therefore:

```text
Composite
→ Structure

Alternate
→ Role
```

---

# 11. Composite Key and Super Key

Suppose:

```text
(A,B)
```

uniquely identifies every row.

Then:

```text
(A,B)
→ Super Key
```

If it is minimal:

```text
(A,B)
→ Candidate Key
```

If we add:

```text
C
```

then:

```text
(A,B,C)
→ Super Key
```

but it may not be a candidate key.

Why?

Because:

```text
(A,B)
```

was already sufficient.

---

# 12. Minimality Is Critical

Suppose:

```text
(A,B)
```

uniquely identifies every row.

If:

```text
A
```

alone is also unique:

```text
(A,B)
→ Not a Candidate Key
```

It is only a super key.

Therefore:

> [!warning]
> **A composite key must not contain unnecessary attributes if you are calling it a composite candidate key.**

---

# 13. Composite Key Recognition Algorithm

Use this during exams:

```text
Step 1:
Check whether one attribute is enough.

If YES:
    Single-attribute key may exist.

If NO:
    Try combinations.

Step 2:
Find a combination that uniquely identifies rows.

Step 3:
Remove one attribute at a time.

Step 4:
If removing any attribute breaks uniqueness:
    Combination is minimal.

Step 5:
It is a Composite Candidate Key.
```

---

# 14. Example — Finding a Composite Key

Table:

| Student_ID | Subject_ID | Semester | Marks |
|---:|---|---|---:|
| 101 | CS01 | 5 | 85 |
| 101 | CS02 | 5 | 78 |
| 102 | CS01 | 5 | 90 |

Suppose:

```text
Student_ID
```

is not unique.

```text
Subject_ID
```

is not unique.

Try:

```text
(Student_ID, Subject_ID)
```

Values:

```text
(101,CS01)
(101,CS02)
(102,CS01)
```

Unique.

Therefore:

```text
(Student_ID, Subject_ID)
```

is a candidate key if no smaller subset works.

---

# 15. Composite Key with Three Attributes

A composite key can contain more than two attributes.

Example:

```text
(Student_ID, Course_ID, Semester)
```

Suppose:

```text
Student_ID + Course_ID
```

is not enough because the same student can take the same course in multiple semesters.

Then:

```text
Student_ID + Course_ID + Semester
```

may be necessary.

Therefore:

```text
(Student_ID, Course_ID, Semester)
→ Composite Candidate Key
```

if minimal and unique.

---

# 16. Real-Time Example — University Enrollment

Consider:

```text
ENROLLMENT
Student_ID
Course_ID
Semester
Grade
```

A student can enroll in the same course in different semesters.

Therefore:

```text
Student_ID + Course_ID
```

may not be unique.

Example:

```text
101 + DBMS + 5
101 + DBMS + 7
```

Both are different records.

So the key may need:

```text
(Student_ID, Course_ID, Semester)
```

This is a realistic example of why composite keys are based on business rules.

---

# 17. Real-Time Example — Order Items

Consider:

```text
ORDER_ITEM
Order_ID
Product_ID
Quantity
Price
```

Suppose an order can contain each product only once.

Then:

```text
(Order_ID, Product_ID)
```

may uniquely identify an order item.

Therefore:

```text
(Order_ID, Product_ID)
→ Composite Candidate Key
```

If the same product can appear multiple times as separate line items, this assumption may fail.

Then an:

```text
Order_Item_ID
```

may be preferable.

---

# 18. Real-Time Example — Movie Booking

Consider:

```text
BOOKING
Show_ID
Seat_Number
Customer_ID
```

Suppose a seat can be booked only once for a particular show.

Then:

```text
(Show_ID, Seat_Number)
```

can uniquely identify a booking.

Why not:

```text
Seat_Number
```

alone?

Because seat 10 can exist in many different shows.

Why not:

```text
Show_ID
```

alone?

Because a show has many seats.

Therefore:

```text
(Show_ID, Seat_Number)
→ Composite Candidate Key
```

---

# 19. Real-Time Example — Hotel Room Booking

Suppose:

```text
Hotel_ID
Room_Number
```

together identify a room.

Why not:

```text
Room_Number
```

alone?

Because different hotels can have room 101.

Therefore:

```text
(Hotel_ID, Room_Number)
→ Composite Candidate Key
```

This is a classic composite-key pattern.

---

# 20. Real-Time Example — Country and Phone Number

Suppose a phone number is unique only within a country.

Then:

```text
(Country_Code, Phone_Number)
```

may uniquely identify a number globally.

Example:

```text
(+91, 9876500000)
(+1, 9876500000)
```

The phone number alone is not enough.

Together:

```text
Country_Code + Phone_Number
```

can identify the record.

---

# 21. Real-Time Example — Warehouse Inventory

Suppose:

```text
Warehouse_ID
Product_ID
Quantity
```

A product can exist in many warehouses.

A warehouse contains many products.

Therefore:

```text
(Warehouse_ID, Product_ID)
```

can identify one inventory record.

This is a common many-to-many / relationship-table pattern.

---

# 22. Real-Time Example — Employee Project Assignment

Consider:

```text
Employee_ID
Project_ID
Hours
```

One employee can work on multiple projects.

One project can have multiple employees.

Therefore:

```text
(Employee_ID, Project_ID)
```

can identify one assignment.

This is a classic junction-table design.

---

# 23. Composite Keys in Many-to-Many Relationships

This is extremely important.

Suppose:

```text
STUDENT
COURSE
```

have a many-to-many relationship.

A student can take many courses.

A course can have many students.

Create:

```text
ENROLLMENT
```

with:

```text
Student_ID
Course_ID
```

Then:

```text
(Student_ID, Course_ID)
```

can identify each relationship.

Visual:

```text
STUDENT
   |
   | 1
   |
   | M
ENROLLMENT
   |
   | M
   |
   | 1
COURSE
```

The enrollment table often uses:

```text
(Student_ID, Course_ID)
```

as its composite primary key.

---

# 24. Junction Table Pattern

> [!important] Must Master

Whenever you see:

```text
Many-to-Many
```

think:

```text
Junction Table
```

Then think:

```text
Foreign Key 1
+
Foreign Key 2
```

Often:

```text
(FK1, FK2)
→ Composite Primary Key
```

Example:

```text
Student_ID FK
Course_ID FK

PRIMARY KEY:
(Student_ID, Course_ID)
```

---

# 25. Composite Primary Key Example

```sql
CREATE TABLE Enrollment (
    Student_ID INT,
    Course_ID INT,
    Enrollment_Date DATE,
    Grade VARCHAR(2),

    PRIMARY KEY (Student_ID, Course_ID)
);
```

This means:

```text
Student_ID alone
→ Not required to be unique

Course_ID alone
→ Not required to be unique

Student_ID + Course_ID
→ Must be unique
```

This is a very important SQL concept.

---

# 26. Important SQL Trick

Suppose:

```sql
PRIMARY KEY (A, B)
```

This does **not** mean:

```text
A must be unique
B must be unique
```

It means:

```text
(A,B)
→ Combination must be unique
```

Example:

| A | B |
|---|---|
| 1 | X |
| 1 | Y |
| 2 | X |

This is valid.

Because the combinations are:

```text
(1,X)
(1,Y)
(2,X)
```

all unique.

---

# 27. Common SQL Mistake

> [!warning]
> Students often think a composite primary key makes each column individually unique.

Wrong.

For:

```sql
PRIMARY KEY (Student_ID, Course_ID)
```

the database enforces uniqueness of:

```text
Student_ID + Course_ID
```

not necessarily:

```text
Student_ID
```

or:

```text
Course_ID
```

individually.

---

# 28. Composite Key and NULL

A primary key cannot contain NULL values.

Therefore:

```sql
PRIMARY KEY (A, B)
```

requires the key columns to participate in a non-null primary-key identity.

For a composite primary key:

```text
A
B
```

must both be present for the row's primary-key value.

> [!important]
> A composite **primary key** is different from an arbitrary composite UNIQUE constraint, whose NULL behavior can depend on the DBMS.

---

# 29. Composite Key and Foreign Keys

A foreign key can also be composite.

Parent:

```text
Enrollment
(Student_ID, Course_ID)
```

Child:

```text
Grade_History
(Student_ID, Course_ID, Updated_On)
```

The child can reference the composite key:

```text
FOREIGN KEY (Student_ID, Course_ID)
REFERENCES Enrollment(Student_ID, Course_ID)
```

The number and order of referenced columns must match the referenced key definition appropriately.

---

# 30. Composite Foreign Key Example

```sql
CREATE TABLE Enrollment (
    Student_ID INT,
    Course_ID INT,
    Grade CHAR(2),
    PRIMARY KEY (Student_ID, Course_ID)
);

CREATE TABLE Assignment (
    Assignment_ID INT PRIMARY KEY,
    Student_ID INT,
    Course_ID INT,

    FOREIGN KEY (Student_ID, Course_ID)
        REFERENCES Enrollment(Student_ID, Course_ID)
);
```

Here:

```text
Enrollment
→ Composite Primary Key

Assignment
→ Composite Foreign Key
```

---

# 31. Composite Key and Functional Dependency

Suppose:

```text
R(A,B,C,D)
```

and:

```text
AB → C
AB → D
```

Then:

```text
AB → A,B,C,D
```

Therefore:

```text
AB
→ Super Key
```

If neither:

```text
A+
```

nor:

```text
B+
```

contains all attributes:

```text
AB
→ Candidate Key
```

Because it is made of multiple attributes:

```text
AB
→ Composite Candidate Key
```

---

# 32. Closure Example

Given:

```text
R(A,B,C,D)
```

FDs:

```text
A → C
B → D
```

Find:

```text
(AB)+
```

Start:

```text
AB+
= {A,B}
```

Using:

```text
A → C
```

get:

```text
{A,B,C}
```

Using:

```text
B → D
```

get:

```text
{A,B,C,D}
```

Therefore:

```text
AB
→ Super Key
```

Check minimality:

```text
A+
= {A,C}

B+
= {B,D}
```

Neither is complete.

Therefore:

```text
AB
→ Composite Candidate Key
```

---

# 33. Advanced Pattern — Attributes Not on RHS

Suppose:

```text
R(A,B,C,D,E)
```

FDs:

```text
A → B
C → D
```

RHS:

```text
B
D
```

Attributes not on RHS:

```text
A
C
E
```

These are strong candidates for being mandatory components.

Start:

```text
ACE
```

Closure:

```text
ACE+
= {A,C,E}

A → B
= {A,B,C,E}

C → D
= {A,B,C,D,E}
```

Therefore:

```text
ACE
→ Super Key
```

Check whether any attribute can be removed.

If none can be removed:

```text
ACE
→ Composite Candidate Key
```

---

# 34. Advanced Pattern — Redundant Attribute

Suppose:

```text
AB
```

is proposed as a composite candidate key.

Calculate:

```text
A+
```

If:

```text
A+
= all attributes
```

then:

```text
A
```

is already a candidate key.

Therefore:

```text
AB
→ Super Key
→ Not Candidate Key
```

This is a common exam trap.

---

# 35. Advanced Pattern — Three-Attribute Candidate Key

Suppose:

```text
R(A,B,C,D,E)
```

FDs:

```text
A → D
B → E
CD → A
```

Try:

```text
BCD
```

Start:

```text
BCD+
= {B,C,D}
```

Using:

```text
CD → A
```

get:

```text
{A,B,C,D}
```

Using:

```text
A → D
```

nothing new.

Using:

```text
B → E
```

get:

```text
{A,B,C,D,E}
```

Therefore:

```text
BCD
→ Super Key
```

Now test minimality.

Remove B:

```text
CD+
→ A,D,C
```

does not get E.

Remove C:

```text
BD+
→ B,D,E
```

does not get A or C.

Remove D:

```text
BC+
→ B,C,E
```

does not get A or D.

Therefore:

```text
BCD
→ Composite Candidate Key
```

---

# 36. Composite Key and Partial Dependency

This is extremely important for normalization.

Suppose:

```text
Candidate Key = (Student_ID, Course_ID)
```

and:

```text
Student_ID → Student_Name
```

Then:

```text
Student_Name
```

depends only on part of the composite key.

This is:

**Partial Dependency**

and can cause a **2NF violation**.

Therefore:

> [!tip]
> Whenever you see a composite candidate key, immediately check for partial dependencies.

---

# 37. 2NF Recognition Trick

> [!important]
> If the candidate key has multiple attributes and a non-prime attribute depends on only part of that key:

```text
Composite Key
+
Partial Dependency
→
2NF Violation
```

Example:

```text
(Student_ID, Course_ID) → Grade
Student_ID → Student_Name
```

`Student_Name` depends only on `Student_ID`.

Therefore:

```text
Partial Dependency
→ 2NF issue
```

---

# 38. Composite Key and 3NF

Suppose:

```text
(Student_ID, Course_ID) → Grade
Course_ID → Course_Name
```

Then:

```text
(Student_ID, Course_ID)
→ Course_ID
→ Course_Name
```

This may create a transitive dependency involving non-key attributes.

Therefore composite-key problems often lead directly into:

```text
2NF
3NF
BCNF
```

---

# 39. Composite Key and Prime Attributes

Suppose:

```text
Candidate Key:
(A,B)
```

Then:

```text
A
B
```

are prime attributes.

If:

```text
C
D
```

are not part of any candidate key:

```text
C,D
→ Non-prime
```

This distinction is important in normalization.

---

# 40. Composite Key vs Compound Key

In many database discussions, **composite key** and **compound key** are used similarly.

For placement exams:

```text
Composite Key
→ Key containing multiple attributes
```

is the safest terminology.

Some resources may use "compound key" for a key formed from multiple columns.

---

# 41. Composite Key vs Composite Attribute

Do not confuse these.

A:

```text
Composite Attribute
```

is an ER-model concept where one attribute can be divided into smaller attributes.

Example:

```text
Name
→ First_Name + Last_Name
```

A:

```text
Composite Key
```

is a key consisting of multiple attributes.

Example:

```text
Student_ID + Course_ID
```

These are completely different concepts.

---

# 42. Composite Key vs Composite Attribute

| Concept | Meaning | Example |
|---|---|---|
| Composite Key | Multiple attributes together form a key | `(Student_ID, Course_ID)` |
| Composite Attribute | Attribute divided into components | `Name → First_Name, Last_Name` |

> [!warning]
> The word "composite" does not always mean the same thing.

Always look at the context.

---

# 43. Composite Key vs Foreign Key

A composite key is about **identification**.

A foreign key is about **reference**.

Example:

```text
(Student_ID, Course_ID)
→ Composite Primary Key
```

A child table may have:

```text
(Student_ID, Course_ID)
→ Composite Foreign Key
```

The same columns can have both structural roles in different contexts.

---

# 44. Composite Key in Junction Tables

A very common interview question:

> How do you implement many-to-many relationships?

Answer:

```text
Create junction table.

Store both foreign keys.

Use their combination as a composite primary key,
if the business rule makes that combination unique.
```

Example:

```text
STUDENT
COURSE
ENROLLMENT
```

Enrollment:

```text
Student_ID FK
Course_ID FK

PRIMARY KEY:
(Student_ID, Course_ID)
```

---

# 45. Real-World Pattern — Social Media

Consider:

```text
USER
USER_ID

FOLLOW
Follower_ID
Following_ID
```

One user can follow many users.

A user can be followed by many users.

The relationship table can use:

```text
(Follower_ID, Following_ID)
```

as a composite key.

This prevents duplicate follow relationships.

Example:

```text
(101,205)
```

means:

```text
User 101 follows User 205
```

The same pair should not appear twice.

---

# 46. Real-World Pattern — Course Enrollment

```text
STUDENT
    |
    | many
    ↓
ENROLLMENT
    ↑
    | many
    |
COURSE
```

Enrollment:

```text
Student_ID
Course_ID
```

Composite key:

```text
(Student_ID, Course_ID)
```

This is one of the most common examples to remember for interviews.

---

# 47. Real-World Pattern — Product Order

```text
ORDER
    |
    ↓
ORDER_ITEM
    ↑
    |
PRODUCT
```

Potential key:

```text
(Order_ID, Product_ID)
```

if each product appears only once per order.

If multiple lines for the same product are allowed:

```text
Order_Item_ID
```

may be required.

This shows why key design depends on business rules.

---

# 48. Real-World Pattern — Employee Skills

Table:

```text
EMPLOYEE_SKILL
Employee_ID
Skill_ID
Level
```

One employee can have multiple skills.

One skill can belong to multiple employees.

Potential composite key:

```text
(Employee_ID, Skill_ID)
```

This prevents duplicate employee-skill relationships.

---

# 49. Composite Key and Surrogate Key

Instead of:

```text
(Student_ID, Course_ID)
```

a designer might introduce:

```text
Enrollment_ID
```

as a surrogate primary key.

Then:

```text
Enrollment_ID
→ Primary Key

(Student_ID, Course_ID)
→ UNIQUE constraint
```

if the business rule still requires the pair to be unique.

This creates:

```text
Surrogate Primary Key
+
Natural/Business Alternate Key
```

---

# 50. Why Use a Surrogate Key Instead?

Composite keys can become inconvenient when many child tables need to reference them.

Suppose:

```text
Enrollment_ID
```

is a single-column identifier.

A child table needs:

```text
Enrollment_ID
```

instead of:

```text
Student_ID
Course_ID
```

This can simplify:

- Foreign keys
- Joins
- URLs
- ORM mappings
- Application code

But the composite business uniqueness may still need enforcement.

---

# 51. Composite Key vs Surrogate Key

| Feature | Composite Key | Surrogate Key |
|---|---|---|
| Based on multiple attributes | Yes | Usually no |
| Has business meaning | Often | Usually none |
| Example | `(Student_ID, Course_ID)` | `Enrollment_ID` |
| Can be primary | Yes | Yes |
| May require UNIQUE business rule | Sometimes | Often |
| Foreign key size | Potentially larger | Often smaller |

---

# 52. When Composite Keys Are Excellent

Composite keys are especially natural when:

```text
The relationship itself is identified by multiple entities.
```

Examples:

```text
Student + Course
Employee + Project
Product + Warehouse
User + Role
Order + Product
```

These are classic relationship-table patterns.

---

# 53. When Composite Keys Can Become Awkward

They may become less convenient when:

```text
Many child tables reference the row.
```

A composite foreign key may require several columns everywhere.

In such cases, a surrogate key can simplify references while a UNIQUE constraint preserves business uniqueness.

---

# 54. Recognition Shortcut

> [!tip]
> If you see:

```text
Employee + Project
Student + Course
Order + Product
User + Role
Warehouse + Product
```

immediately ask:

```text
Is this a relationship table?
```

If yes:

```text
Combination of the two foreign keys
→ Often a Composite Candidate/Primary Key
```

Always verify the business rule.

---

# 55. Common Exam Patterns

> [!important] Must Master

### Pattern 1

No single attribute is unique.

```text
Combination is unique.
```

Think:

```text
Composite Key
```

### Pattern 2

Two foreign keys form a relationship table.

Think:

```text
Composite Primary Key
```

if the pair is unique.

### Pattern 3

A combination uniquely identifies rows but one component can be removed.

Think:

```text
Super Key
NOT Candidate Key
```

### Pattern 4

A composite candidate key has a partial dependency.

Think:

```text
2NF
```

### Pattern 5

A composite candidate key is not selected as primary.

Think:

```text
Composite Alternate Key
```

### Pattern 6

A child references two columns together.

Think:

```text
Composite Foreign Key
```

---

# 56. Pattern Recognition Table

| Question Clue | Think |
|---|---|
| Two or more attributes together identify row | Composite Key |
| Combination is minimal and unique | Composite Candidate Key |
| Combination selected as primary | Composite Primary Key |
| Combination is candidate but not selected | Composite Alternate Key |
| Two FKs identify a relationship | Composite Key |
| No single column is unique | Try Composite Key |
| Extra attribute can be removed | Super Key, not Candidate |
| Composite key + partial dependency | 2NF issue |
| Multiple columns referenced together | Composite Foreign Key |

---

# 57. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking each column must be unique

Wrong.

For:

```text
PRIMARY KEY (A,B)
```

the combination must be unique.

---

### Mistake 2 — Thinking composite means only two columns

Wrong.

Composite means:

```text
2 or more
```

So:

```text
(A,B)
(A,B,C)
(A,B,C,D)
```

can all be composite.

---

### Mistake 3 — Thinking every multi-column unique set is a candidate key

Wrong.

Check minimality.

---

### Mistake 4 — Ignoring business rules

A combination may look unique in sample data but may not be guaranteed unique.

---

### Mistake 5 — Confusing composite key with composite attribute

They are different DBMS/ER concepts.

---

### Mistake 6 — Forgetting 2NF

Composite candidate keys should immediately make you check for partial dependency.

---

### Mistake 7 — Assuming foreign keys are always single-column

Foreign keys can also be composite.

---

### Mistake 8 — Assuming a composite key is always a primary key

No.

It can be:

```text
Candidate
Primary
Alternate
Super
Foreign
```

depending on context.

---

### Mistake 9 — Assuming `(A,B)` means A and B are individually unique

Wrong.

Only the combination needs to be unique.

---

### Mistake 10 — Adding an artificial ID without preserving business uniqueness

If:

```text
(Student_ID, Course_ID)
```

must be unique, adding:

```text
Enrollment_ID
```

does not automatically enforce that business rule.

You may still need:

```sql
UNIQUE (Student_ID, Course_ID)
```

---

# 58. Interview Questions

## Q1. What is a composite key?

### Strong Answer

> A composite key is a key consisting of two or more attributes that together identify a row. If the combination is minimal and unique, it is a composite candidate key.

---

# 59. Interview Question

## Q2. Give a real-world example of a composite key.

### Answer

A student enrollment table can use:

```text
(Student_ID, Course_ID)
```

because a student can enroll in multiple courses and a course can have multiple students.

---

# 60. Interview Question

## Q3. Can a composite key be a primary key?

### Answer

Yes.

Example:

```sql
PRIMARY KEY (Student_ID, Course_ID)
```

---

# 61. Interview Question

## Q4. Can a composite key be an alternate key?

### Answer

Yes.

If a composite candidate key is not selected as the primary key, it can be an alternate key.

---

# 62. Interview Question

## Q5. Can a composite key be a foreign key?

### Answer

Yes.

A foreign key can consist of multiple columns and reference a suitable composite key in another table.

---

# 63. Interview Question

## Q6. Does a composite primary key require each column to be unique?

### Answer

No.

The combination must be unique.

---

# 64. Interview Question

## Q7. Why is `(Student_ID, Course_ID)` useful as a key?

### Answer

Because neither attribute alone identifies an enrollment, but their combination identifies a particular student's enrollment in a particular course.

---

# 65. Interview Question

## Q8. What happens if one attribute of a composite key is removed?

### Answer

If the remaining attributes no longer uniquely identify rows, the original composite key is minimal and can be a candidate key.

If the remaining attributes still uniquely identify rows, the original key was not minimal.

---

# 66. Interview Question

## Q9. What is the relationship between composite and candidate keys?

### Answer

Composite describes the number of attributes, while candidate describes uniqueness and minimality.

A composite key can be a candidate key if it is minimal and unique.

---

# 67. Interview Question

## Q10. What is a composite foreign key?

### Answer

A foreign key consisting of multiple columns that references a corresponding composite key or suitable unique key in another table.

---

# 68. Interview Question

## Q11. What is a common use of composite keys?

### Answer

Junction tables representing many-to-many relationships.

Examples:

```text
Student-Course
Employee-Project
User-Role
Order-Product
```

---

# 69. Interview Question

## Q12. What is the relationship between composite keys and 2NF?

### Answer

2NF is especially relevant when a candidate key is composite. A non-prime attribute depending on only part of a composite candidate key creates a partial dependency and can violate 2NF.

---

# 70. Interview Question

## Q13. Can a composite key have three attributes?

### Answer

Yes.

Example:

```text
(Student_ID, Course_ID, Semester)
```

---

# 71. Interview Question

## Q14. Can a composite key contain foreign keys?

### Answer

Yes.

This is very common in relationship tables.

For example:

```text
(Student_ID, Course_ID)
```

where both columns are foreign keys.

---

# 72. Interview Question

## Q15. Why might a designer replace a composite primary key with a surrogate key?

### Answer

To simplify foreign-key references, joins, application code, ORM mappings, and external identifiers. The original business uniqueness can still be enforced with a UNIQUE constraint.

---

# 73. Advanced Interview Question

## Q16. Is every composite key a candidate key?

### Answer

No.

A multi-column set can be a super key without being minimal.

---

# 74. Advanced Interview Question

## Q17. Is every candidate key composite?

### Answer

No.

A candidate key can contain one attribute or multiple attributes.

---

# 75. Advanced Interview Question

## Q18. Can a table have multiple composite candidate keys?

### Answer

Yes.

A relation can have multiple candidate keys, and several of them may be composite.

---

# 76. Advanced Interview Question

## Q19. If `(A,B)` is a candidate key, is `(A,B,C)` a candidate key?

### Answer

No, assuming `(A,B)` already determines all attributes.

`(A,B,C)` is a super key but is not minimal.

---

# 77. Advanced Interview Question

## Q20. If `(A,B)` is a primary key, can `A` repeat?

### Answer

Yes.

Example:

```text
A B
1 X
1 Y
2 X
```

is valid because each `(A,B)` combination is unique.

---

# 78. Advanced Interview Question

## Q21. Can the same value of B repeat?

### Answer

Yes.

For:

```text
PRIMARY KEY (A,B)
```

`B` can repeat as long as the complete pair is unique.

---

# 79. Advanced Interview Question

## Q22. Can `(A,B)` be a composite candidate key if A is unique?

### Answer

No.

If `A` alone uniquely identifies every row, then `(A,B)` is not minimal.

It is a super key.

---

# 80. Advanced Interview Question

## Q23. What is the difference between composite primary key and surrogate primary key?

### Answer

A composite primary key uses multiple meaningful attributes.

A surrogate primary key is usually a single artificial identifier with no business meaning.

Example:

```text
Composite:
(Student_ID, Course_ID)

Surrogate:
Enrollment_ID
```

---

# 81. Advanced Interview Question

## Q24. Is a composite key always preferable?

### Answer

No.

It is appropriate when the combination naturally represents row identity. In other designs, a surrogate primary key may simplify relationships while a UNIQUE constraint preserves natural uniqueness.

---

# 82. Advanced Interview Question

## Q25. What is the fastest way to identify a composite key question?

### Answer

Look for wording such as:

```text
"Together"
"Combination"
"No single attribute is sufficient"
"Two columns uniquely identify"
"Many-to-many relationship"
"Junction table"
```

These strongly suggest a composite key.

---

# 83. Advanced Exam Problem

### Question

Consider:

```text
R(A,B,C,D)
```

FDs:

```text
A → C
B → D
```

Find a candidate key.

### Step 1

Try:

```text
A+
= A,C
```

Not complete.

Try:

```text
B+
= B,D
```

Not complete.

Try:

```text
AB+
```

Using:

```text
A → C
B → D
```

we get:

```text
ABCD
```

Therefore:

```text
AB
→ Super Key
```

Check:

```text
A+
≠ ABCD

B+
≠ ABCD
```

Therefore:

```text
AB
→ Composite Candidate Key
```

---

# 84. Advanced Exam Problem

### Question

Relation:

```text
R(A,B,C,D,E)
```

FDs:

```text
A → B
B → C
CD → E
```

Find the candidate key.

### Solution

Attributes not on RHS:

```text
A,D
```

Start:

```text
AD
```

Closure:

```text
AD+
= A,D

A → B
= A,B,D

B → C
= A,B,C,D

CD → E
= A,B,C,D,E
```

Therefore:

```text
AD
→ Super Key
```

Check minimality:

```text
A+
= A,B,C

D+
= D
```

Neither is complete.

Therefore:

```text
AD
→ Composite Candidate Key
```

---

# 85. Advanced Exam Problem

### Question

A relation has:

```text
R(A,B,C,D)
```

and:

```text
A → B,C,D
```

Is `(A,B)` a candidate key?

### Answer

No.

Because:

```text
A+
= A,B,C,D
```

So `A` alone is already a candidate key.

Therefore:

```text
(A,B)
→ Super Key
→ Not Candidate Key
```

---

# 86. Advanced Exam Problem

### Question

A relation has a composite primary key:

```text
(A,B)
```

and:

```text
A → C
```

What should you immediately investigate?

### Answer

A possible:

```text
Partial Dependency
```

Therefore investigate:

```text
2NF
```

---

# 87. Advanced Exam Problem

### Question

A student-course table has:

```text
Student_ID
Course_ID
Marks
```

Student_ID is repeated and Course_ID is repeated, but their combination is unique.

What is the likely key?

### Answer

```text
(Student_ID, Course_ID)
```

This is a composite candidate key if the combination is minimal.

---

# 88. Advanced Exam Problem

### Question

A movie theater has multiple shows and each show has many seats. A seat number is unique only within a show.

What key can identify a booking?

### Answer

```text
(Show_ID, Seat_Number)
```

This is a composite key.

---

# 89. Advanced Exam Problem

### Question

An order can contain many products and a product can appear in many orders. Each product appears only once per order.

What key can identify an order-item relationship?

### Answer

```text
(Order_ID, Product_ID)
```

This is a natural composite candidate key.

---

# 90. Shortcut Sheet

> [!tip] Fast Recognition

```text
"Combination uniquely identifies"
→ Composite Key

"Two or more columns"
→ Composite Key

"Together"
→ Think Composite Key

"No single column is enough"
→ Try Composite Key

"Many-to-many relationship"
→ Junction Table
→ Often Composite Key

"Two foreign keys"
→ Often Composite Key

"Composite key + partial dependency"
→ Think 2NF

"Composite key + extra unnecessary column"
→ Super Key, not Candidate Key

"Composite candidate not selected as primary"
→ Composite Alternate Key
```

---

# 91. Professional Design Pattern

A common database design can look like:

```text
Customer
---------
Customer_ID PK
Email UNIQUE
```

Then:

```text
Order
---------
Order_ID PK
Customer_ID FK
```

For order items:

```text
Order_Item
---------
Order_ID FK
Product_ID FK
Quantity

PRIMARY KEY:
(Order_ID, Product_ID)
```

This demonstrates:

```text
Single Primary Key
+
Alternate Key
+
Composite Primary Key
+
Foreign Keys
```

all working together.

---

# 92. Composite Key Design Checklist

Before declaring a composite key, ask:

```text
1. Does one attribute alone work?
2. If not, what combination works?
3. Is the combination guaranteed unique?
4. Is every attribute necessary?
5. Can any attribute be removed?
6. Is it a candidate key?
7. Is it selected as primary?
8. Is it an alternate key?
9. Is it also used as a foreign key elsewhere?
10. Does it create partial dependencies?
11. Is a surrogate key more practical?
12. Does business uniqueness still need a UNIQUE constraint?
```

---

# 93. Key Classification Master Table

| Key | Number of Columns | Unique | Minimal | Can Be Primary | Can Be Foreign |
|---|---:|---|---|---|---|
| Super Key | 1 or more | Yes | Not required | No direct concept | Not relevant |
| Candidate Key | 1 or more | Yes | Yes | Yes | Can be referenced |
| Primary Key | 1 or more | Yes | Yes | Yes | Can be referenced |
| Alternate Key | 1 or more | Yes | Yes | Not selected | Can be referenced |
| Composite Key | 2 or more | Depends on context | Depends on context | Yes | Yes |
| Foreign Key | 1 or more | Not necessarily | Not necessarily | No | Yes |

---

# 94. Key Hierarchy

```text
                    KEY
                     |
          ┌──────────┴──────────┐
          |                     |
      Single                Composite
      Attribute             Multiple Attributes
          |                     |
          └──────────┬──────────┘
                     |
              Unique + Minimal
                     ↓
              Candidate Key
                     |
          ┌──────────┴──────────┐
          ↓                     ↓
       Selected              Not Selected
          ↓                     ↓
     Primary Key          Alternate Key
```

Important:

```text
Composite
```

is a structural property.

```text
Candidate / Primary / Alternate
```

are role/classification properties.

---

# 95. Formula Sheet

> [!summary] Formula Sheet

```text
Composite Key
=
Key containing 2 or more attributes

Composite Candidate Key
=
Composite + Unique + Minimal

Composite Primary Key
=
Composite Candidate Key selected as Primary Key

Composite Alternate Key
=
Composite Candidate Key not selected as Primary Key

If:
K+ = all relation attributes
→ K is a Super Key

If:
K+ = all relation attributes
and no proper subset of K has the same closure
→ K is a Candidate Key

For:
PRIMARY KEY (A,B)

Required:
(A,B) must be unique

Not necessarily:
A unique
B unique
```

---

# 96. Quick Revision

> [!summary] One-Minute Revision

```text
COMPOSITE KEY
→ Key containing 2 or more attributes.

CORE IDEA
→ Multiple columns work together to identify a row.

Example:
(Student_ID, Course_ID)

If:
Student_ID alone is not unique
Course_ID alone is not unique
but:
(Student_ID, Course_ID) is unique

Then:
(Student_ID, Course_ID)
→ Composite Candidate Key
if minimal.

COMPOSITE PRIMARY KEY
→ Composite candidate key selected as primary.

COMPOSITE ALTERNATE KEY
→ Composite candidate key not selected as primary.

COMPOSITE FOREIGN KEY
→ Foreign key containing multiple columns.

MOST COMMON USE
→ Many-to-many junction tables.

Examples:
Student + Course
Employee + Project
User + Role
Order + Product
Product + Warehouse

SQL:

PRIMARY KEY (A,B)

means:
(A,B) must be unique.

It does NOT mean:
A must be unique.
B must be unique.

IMPORTANT

Composite
→ Multiple attributes

Candidate
→ Minimal + Unique

Primary
→ Selected Candidate

Alternate
→ Unselected Candidate

Super
→ Any Unique Set

2NF

Composite Candidate Key
+
Partial Dependency
→ Possible 2NF Violation

FAST RECOGNITION

"No single attribute is enough"
→ Try Composite Key

"Together they uniquely identify"
→ Composite Key

"Many-to-many"
→ Junction Table
→ Often Composite Key

"Two foreign keys together"
→ Often Composite Key
```

# 97. Golden Memory Trick

**Composite Key = "Two or more pieces of information must work together to identify one row."**

# 98. One-Line Recognition

**If no single attribute is enough but a combination of two or more attributes uniquely identifies the row, think Composite Key.**