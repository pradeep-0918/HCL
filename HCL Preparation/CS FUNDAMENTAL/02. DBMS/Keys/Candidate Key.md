---
type: concept
subject: dbms
topic: "Candidate Key"
parent: "Keys"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - keys
  - candidate-key
  - primary-key
  - super-key
  - alternate-key
  - composite-key
  - functional-dependency
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
  - "[[Foreign Key]]"
  - "[[Super Key]]"
  - "[[Alternate Key]]"
  - "[[Composite Key]]"
  - "[[Functional Dependency]]"
  - "[[Normalization]]"
---

# Candidate Key

## 1. Core Concept

> [!summary]
> A **Candidate Key** is a minimal set of one or more attributes that can uniquely identify every row in a relation.

The most important memory:

**Candidate Key = Unique + Minimal**

A candidate key must satisfy two conditions:

1. It must uniquely identify every row.
2. It must contain no unnecessary attribute.

Example:

| Student_ID | Email | Name |
|---:|---|---|
| 101 | arun@gmail.com | Arun |
| 102 | priya@gmail.com | Priya |
| 103 | ravi@gmail.com | Ravi |

Suppose both:

`Student_ID`

and:

`Email`

are unique.

Then:

`Student_ID`

is a candidate key.

`Email`

is also a candidate key.

Therefore:

```text
Candidate Keys
    ↓
{Student_ID}
{Email}
```

One of them can be selected as the:

`Primary Key`

---

# 2. Basic Meaning

The word **candidate** means:

> "This attribute set is a candidate for becoming the primary key."

A table can have multiple candidate keys.

Example:

```text
Student_ID
Email
Phone_Number
```

If all three are:

- Unique
- Minimal
- Non-null under the intended key definition

then all three can be candidate keys.

The database designer can select one of them as the primary key.

The remaining candidate keys become alternate keys.

---

# 3. Main Formula

There is no numerical formula for a candidate key, but there is a very important conceptual formula:

```text
Candidate Key
=
Super Key
+
Minimality
```

Or:

```text
Candidate Key
=
Unique
+
No Unnecessary Attributes
```

Another important relationship:

```text
Candidate Key → Primary Key
```

The primary key is one selected candidate key.

---

# 4. What Does "Unique" Mean?

Suppose:

| Student_ID | Name |
|---:|---|
| 101 | Arun |
| 102 | Priya |
| 103 | Ravi |

`Student_ID`

uniquely identifies every row.

Therefore:

```text
Student_ID → Unique identification
```

If two rows have the same value:

| Student_ID | Name |
|---:|---|
| 101 | Arun |
| 101 | Priya |

then `Student_ID` cannot be a candidate key.

---

# 5. What Does "Minimal" Mean?

Minimality is the most important part that students often miss.

Suppose:

```text
Student_ID
```

alone uniquely identifies every student.

Then:

```text
{Student_ID, Name}
```

also uniquely identifies every student.

But:

`Name`

is unnecessary.

Therefore:

```text
{Student_ID, Name}
```

is a super key.

It is NOT a candidate key.

Why?

Because it is not minimal.

> [!important]
> **Candidate Key = Minimal Super Key**

---

# 6. Super Key vs Candidate Key

This distinction is extremely important in DBMS interviews.

### Super Key

Any set of attributes that uniquely identifies rows.

### Candidate Key

A minimal super key.

Example:

Suppose:

`Student_ID`

is unique.

Then these are all super keys:

```text
{Student_ID}

{Student_ID, Name}

{Student_ID, Email}

{Student_ID, Name, Email}
```

But only:

```text
{Student_ID}
```

is minimal.

Therefore:

```text
Super Keys
    ↓
Remove unnecessary attributes
    ↓
Candidate Keys
```

---

# 7. Candidate Key Recognition Trick

> [!tip]
> If the question says:
>
> "Minimal set of attributes that uniquely identifies each tuple"
>
> immediately think:
>
> **Candidate Key**

If it says:

> "Any set of attributes that uniquely identifies a tuple"

think:

**Super Key**

If it says:

> "Candidate key selected to identify rows"

think:

**Primary Key**

---

# 8. Candidate Key and Primary Key

Suppose a table has:

```text
Candidate Keys:
    Student_ID
    Email
    Phone_Number
```

The designer chooses:

```text
Student_ID
```

as the primary key.

Then:

```text
Primary Key
→ Student_ID

Alternate Keys
→ Email
→ Phone_Number
```

Therefore:

> [!summary]
> **Candidate Key = Possible primary key**
>
> **Primary Key = Selected candidate key**

---

# 9. Candidate Key and Alternate Key

Suppose:

```text
Candidate Keys:

{Student_ID}
{Email}
{Phone_Number}
```

Choose:

```text
{Student_ID}
```

as primary.

Then:

```text
Email
Phone_Number
```

are alternate keys.

So:

```text
Candidate Keys
        ↓
   Select one
        ↓
Primary Key

Remaining Candidate Keys
        ↓
Alternate Keys
```

---

# 10. Candidate Key and Super Key Hierarchy

The complete hierarchy is:

```text
SUPER KEYS
    ↓
Remove unnecessary attributes
    ↓
CANDIDATE KEYS
    ↓
Choose one
    ↓
PRIMARY KEY

Other candidate keys
    ↓
ALTERNATE KEYS
```

This hierarchy should be memorized.

---

# 11. Basic Example

### Example — Student Table

Consider:

| Student_ID | Email | Name |
|---:|---|---|
| 101 | a@gmail.com | Arun |
| 102 | p@gmail.com | Priya |
| 103 | r@gmail.com | Ravi |

Assume:

`Student_ID`

is unique.

`Email`

is unique.

Then:

```text
Candidate Keys:

{Student_ID}
{Email}
```

If we choose:

```text
Student_ID
```

as the primary key:

```text
Primary Key:
Student_ID

Alternate Key:
Email
```

---

# 12. Example — Name Is Not a Candidate Key

Consider:

| Student_ID | Name |
|---:|---|
| 101 | Arun |
| 102 | Arun |
| 103 | Priya |

Can `Name` be a candidate key?

No.

Because:

```text
Arun
```

appears twice.

Therefore:

```text
Name
→ Not unique
→ Not Candidate Key
```

---

# 13. Example — Roll Number

Suppose:

| Roll_No | Name |
|---:|---|
| 1 | Arun |
| 2 | Priya |
| 3 | Ravi |

If `Roll_No` is guaranteed unique:

```text
Roll_No
→ Candidate Key
```

If selected as primary:

```text
Roll_No
→ Primary Key
```

---

# 14. Example — Email

Suppose:

| Student_ID | Email |
|---:|---|
| 101 | a@gmail.com |
| 102 | p@gmail.com |
| 103 | r@gmail.com |

If email is guaranteed unique:

```text
Email
→ Candidate Key
```

If `Student_ID` is selected as primary:

```text
Email
→ Alternate Key
```

---

# 15. Advanced Example — Two Candidate Keys

Consider:

```text
EMPLOYEE
--------------------------
Employee_ID
Email
Name
Department
```

Assume:

```text
Employee_ID → Unique
Email → Unique
```

Then:

```text
Candidate Keys:

{Employee_ID}
{Email}
```

Choose:

```text
Employee_ID
```

as primary key.

Then:

```text
Email
→ Alternate Key
```

---

# 16. Advanced Example — Composite Candidate Key

Consider:

| Student_ID | Course_ID | Grade |
|---:|---:|---|
| 101 | 501 | A |
| 101 | 502 | B |
| 102 | 501 | A |

Neither:

```text
Student_ID
```

nor:

```text
Course_ID
```

is unique.

But:

```text
(Student_ID, Course_ID)
```

is unique.

Therefore:

```text
(Student_ID, Course_ID)
→ Candidate Key
```

Because it contains multiple attributes, it is a:

**Composite Candidate Key**

---

# 17. Composite Candidate Key Recognition

> [!important]
> If the question says:
>
> "No single attribute uniquely identifies the row, but a combination of attributes does"
>
> think:
>
> **Composite Candidate Key**

Example:

```text
Student_ID + Course_ID
```

---

# 18. Composite Candidate Key and Minimality

Suppose:

```text
(Student_ID, Course_ID)
```

uniquely identifies a row.

Suppose neither:

```text
Student_ID
```

nor:

```text
Course_ID
```

alone is unique.

Then:

```text
(Student_ID, Course_ID)
```

is minimal.

Therefore it is a candidate key.

But suppose:

```text
(Student_ID, Course_ID, Semester)
```

also uniquely identifies rows.

If:

```text
(Student_ID, Course_ID)
```

already uniquely identifies them, then:

```text
(Student_ID, Course_ID, Semester)
```

is not a candidate key.

It is a super key.

Why?

Because `Semester` is unnecessary.

---

# 19. Candidate Key Recognition Algorithm

Use this during exams.

```text
Step 1:
Find attributes that can identify rows.

Step 2:
Check uniqueness.

Step 3:
Try removing attributes.

Step 4:
If removal destroys uniqueness,
the set is minimal.

Step 5:
Mark it as Candidate Key.
```

Memory:

```text
UNIQUE?
   ↓
YES
   ↓
MINIMAL?
   ↓
YES
   ↓
CANDIDATE KEY
```

---

# 20. Candidate Key Finding Technique

Suppose the relation is:

```text
R(A, B, C, D)
```

Suppose:

```text
A → B
A → C
A → D
```

Then:

```text
A+
=
{A, B, C, D}
```

Therefore:

```text
A
```

can determine all attributes.

So:

```text
A
→ Candidate Key
```

provided no smaller subset exists.

---

# 21. Attribute Closure

Candidate-key problems often use **attribute closure**.

The closure of an attribute set is the collection of attributes functionally determined by it.

Notation:

```text
A+
```

means:

> Closure of A.

If:

```text
A+ = all attributes of R
```

then:

```text
A
```

is a super key.

Then check minimality.

If no attribute can be removed:

```text
A
→ Candidate Key
```

---

# 22. Closure Example

Given:

```text
R(A, B, C, D)
```

Functional dependencies:

```text
A → B
B → C
C → D
```

Find:

```text
A+
```

Start:

```text
A+ = {A}
```

Using:

```text
A → B
```

we get:

```text
A+ = {A, B}
```

Using:

```text
B → C
```

we get:

```text
A+ = {A, B, C}
```

Using:

```text
C → D
```

we get:

```text
A+ = {A, B, C, D}
```

Therefore:

```text
A+
= All attributes
```

So:

```text
A
→ Super Key
```

Since `A` is a single attribute, it is minimal.

Therefore:

```text
A
→ Candidate Key
```

---

# 23. Candidate Key from Functional Dependencies

This is a major DBMS interview pattern.

Given:

```text
R(A, B, C, D, E)
```

FDs:

```text
A → B
B → C
C → D
D → E
```

Find candidate key.

Start with:

```text
A+
```

Then:

```text
A → B
B → C
C → D
D → E
```

Therefore:

```text
A+ = {A, B, C, D, E}
```

So:

```text
A
→ Candidate Key
```

---

# 24. Candidate Key Using Closure — Shortcut

> [!tip]
> If an attribute can eventually determine **every attribute in the relation**, its closure contains all attributes.

Then check:

```text
Can anything be removed?
```

If it is a single attribute:

```text
Nothing can be removed
```

Therefore it is a candidate key.

For combinations, test each attribute's necessity.

---

# 25. Advanced Candidate Key Example

Given:

```text
R(A, B, C, D)
```

Functional dependencies:

```text
A → B
B → A
A → C
C → D
```

Find candidate keys.

### Find A+

```text
A+
= {A}

A → B
= {A, B}

A → C
= {A, B, C}

C → D
= {A, B, C, D}
```

Therefore:

```text
A
→ Candidate Key
```

### Find B+

```text
B+
= {B}

B → A
= {A, B}

A → C
= {A, B, C}

C → D
= {A, B, C, D}
```

Therefore:

```text
B
→ Candidate Key
```

So:

```text
Candidate Keys:

{A}
{B}
```

---

# 26. Advanced Example — Composite Candidate Key

Given:

```text
R(A, B, C, D)
```

FDs:

```text
A → B
C → D
```

Find candidate key.

Try:

```text
A+
= {A, B}
```

Not all attributes.

Try:

```text
C+
= {C, D}
```

Not all attributes.

Try:

```text
(A,C)+
```

Start:

```text
{A,C}
```

Using:

```text
A → B
```

get:

```text
{A,B,C}
```

Using:

```text
C → D
```

get:

```text
{A,B,C,D}
```

Therefore:

```text
(A,C)
→ Super Key
```

Neither `A` nor `C` alone is enough.

Therefore:

```text
(A,C)
→ Candidate Key
```

---

# 27. Candidate Key Shortcut — Attributes Not on RHS

This is a powerful functional-dependency trick.

Suppose:

```text
R(A, B, C, D, E)
```

FDs:

```text
A → B
B → C
CD → E
```

Look at attributes appearing on the RHS:

```text
B
C
E
```

Attributes not appearing on RHS:

```text
A
D
```

These attributes cannot be derived from other attributes using the given dependencies.

Therefore, they are strong candidates to appear in every candidate key.

Start with:

```text
AD
```

Then calculate closure.

---

# 28. Why RHS Trick Works

If an attribute never appears on the right-hand side of any functional dependency, the given dependencies cannot derive it from other attributes.

Therefore, to determine all attributes, the key must contain that attribute.

This gives a powerful starting point.

> [!tip]
> **Attributes never appearing on RHS are usually mandatory components of every candidate key under the given FDs.**

This is an exam shortcut, not a replacement for closure verification.

---

# 29. Example — RHS Shortcut

Given:

```text
R(A, B, C, D, E)
```

FDs:

```text
A → B
B → C
CD → E
```

RHS attributes:

```text
B, C, E
```

Not on RHS:

```text
A, D
```

Therefore start with:

```text
AD
```

Calculate closure:

```text
AD+
= {A,D}

A → B
= {A,B,D}

B → C
= {A,B,C,D}

CD → E
= {A,B,C,D,E}
```

Therefore:

```text
AD
→ Candidate Key
```

---

# 30. Important Candidate-Key Shortcut

> [!tip]
> In functional-dependency problems:
>
> **First inspect RHS attributes.**
>
> Attributes that never occur on RHS are strong candidates for being mandatory in every key.
>
> Then calculate closure to confirm.

Do not blindly declare them as the complete key.

---

# 31. Candidate Key vs Primary Key — Deep Understanding

Suppose:

```text
Candidate Keys:

K1
K2
K3
```

The database designer chooses:

```text
K1
```

Then:

```text
K1 → Primary Key
K2 → Alternate Key
K3 → Alternate Key
```

Important:

`K2`

does not stop being a candidate key.

It remains a candidate key conceptually.

It is simply not the selected primary key.

---

# 32. Candidate Key vs Unique Constraint

A candidate key is a **relational-design concept**.

A `UNIQUE` constraint is an SQL mechanism for enforcing uniqueness.

They are related but should not be treated as exactly the same thing.

Example:

```text
Email
```

may be a candidate key under the relational design.

The SQL implementation might enforce it using:

```sql
UNIQUE (Email)
```

while another candidate key is chosen as the primary key.

---

# 33. Candidate Key and NULL

In relational theory, a candidate key is intended to uniquely identify tuples and therefore represents mandatory identifying information.

In SQL implementation, exact NULL behavior depends on how constraints are declared.

A declared primary key is explicitly non-null.

A `UNIQUE` constraint can have DBMS-specific NULL behavior.

Therefore:

> [!warning]
> Do not blindly equate "candidate key" with every SQL `UNIQUE` column without considering the schema and DBMS semantics.

---

# 34. Candidate Key and Functional Dependency

If:

```text
K
```

is a candidate key for relation:

```text
R
```

then:

```text
K → all attributes of R
```

and no proper subset of `K` should have the same property.

Therefore:

```text
Candidate Key
→ Determines the complete tuple
→ Is minimal
```

---

# 35. Candidate Key and Functional Dependency Example

Relation:

```text
STUDENT(
    Student_ID,
    Email,
    Name,
    Department
)
```

Suppose:

```text
Student_ID → Email
Student_ID → Name
Student_ID → Department
```

Then:

```text
Student_ID
→ Determines all attributes
```

Therefore:

```text
Student_ID
→ Super Key
```

If it is minimal:

```text
Student_ID
→ Candidate Key
```

---

# 36. Candidate Key and Normalization

Candidate keys are essential in normalization.

Why?

Because normal forms often ask whether non-key attributes depend on:

- the whole key
- part of the key
- another non-key attribute

For example:

```text
2NF
→ No partial dependency on a candidate key

3NF
→ Deals with transitive dependency involving non-prime attributes

BCNF
→ Every determinant must be a candidate key
```

Therefore:

> [!important]
> **Candidate keys are foundational to understanding 2NF, 3NF, and BCNF.**

---

# 37. Prime Attribute

A **prime attribute** is an attribute that belongs to at least one candidate key.

Example:

```text
Candidate Keys:

{A,B}
{C,D}
```

Prime attributes:

```text
A
B
C
D
```

Non-prime attributes are attributes that do not belong to any candidate key.

This concept becomes important in 3NF.

---

# 38. Prime vs Non-Prime Attribute

Suppose:

```text
R(A,B,C,D)
```

Candidate keys:

```text
{A,B}
{C,D}
```

Then:

```text
Prime Attributes:
A, B, C, D
```

If relation were:

```text
R(A,B,C,D,E)
```

with the same candidate keys:

```text
A,B,C,D
```

then:

```text
E
→ Non-prime attribute
```

---

# 39. Candidate Key and BCNF

BCNF rule:

> For every non-trivial functional dependency `X → Y`, `X` must be a super key.

Since every candidate key is a super key:

```text
Candidate Key
→ Super Key
```

candidate keys are central to BCNF analysis.

A determinant that is not a super key can cause a BCNF violation.

---

# 40. Candidate Key and 2NF

2NF mainly matters when the candidate key is composite.

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

depends only on part of the composite candidate key.

This is a:

**Partial Dependency**

and can violate 2NF.

Therefore:

> [!tip]
> **Whenever you see a composite candidate key, immediately think about partial dependency and 2NF.**

---

# 41. Candidate Key and 3NF

Suppose:

```text
Student_ID → Department_ID
Department_ID → Department_Name
```

Then:

```text
Student_ID → Department_Name
```

through Department_ID.

This is a transitive dependency pattern.

Candidate keys help determine whether the dependent attributes are prime or non-prime.

Therefore:

```text
Candidate Keys
→ Important for 2NF
→ Important for 3NF
→ Important for BCNF
```

---

# 42. Real-Time Example — Student Database

Table:

```text
STUDENT
Student_ID
Email
Phone
Name
Department
```

Suppose:

```text
Student_ID
Email
Phone
```

are all unique.

Candidate keys:

```text
{Student_ID}
{Email}
{Phone}
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
```

are alternate keys.

---

# 43. Real-Time Example — Employee System

Suppose:

```text
EMPLOYEE
Employee_ID
Company_Email
Name
Department
```

If:

```text
Employee_ID
```

and:

```text
Company_Email
```

are both unique:

```text
Candidate Keys:

Employee_ID
Company_Email
```

A company might select:

```text
Employee_ID
```

as the primary key because it is a stable internal identifier.

---

# 44. Real-Time Example — Product Catalog

Consider:

```text
PRODUCT
Product_ID
SKU
Barcode
Product_Name
Price
```

Suppose:

```text
Product_ID
SKU
Barcode
```

are unique.

Potential candidate keys:

```text
{Product_ID}
{SKU}
{Barcode}
```

Choose:

```text
Product_ID
```

as primary.

Others can be alternate unique identifiers.

---

# 45. Real-Time Example — Books

Consider:

```text
BOOK
ISBN
Title
Author
Price
```

If ISBN uniquely identifies each edition:

```text
ISBN
→ Candidate Key
```

If selected:

```text
ISBN
→ Primary Key
```

But the correct key depends on the business definition of what one row represents.

For example, different editions may have different ISBNs.

---

# 46. Real-Time Example — Bank Account

Possible attributes:

```text
Account_ID
Account_Number
Customer_Name
Balance
```

If:

```text
Account_ID
```

and:

```text
Account_Number
```

are unique:

```text
Candidate Keys:
Account_ID
Account_Number
```

But:

```text
Customer_Name
```

is not necessarily unique.

And:

```text
Balance
```

is not an identifier.

---

# 47. Real-Time Example — Flight Booking

Suppose:

```text
BOOKING
Booking_ID
Passenger_ID
Flight_ID
Seat_No
```

Depending on business rules, a booking may be uniquely identified by:

```text
Booking_ID
```

Alternatively, certain combinations may be unique under specific rules.

The important lesson:

> [!important]
> **Candidate keys come from business rules and functional dependencies, not from guessing which column "looks unique."**

---

# 48. Real-Time Example — Order Items

Consider:

```text
ORDER_ITEM
Order_ID
Product_ID
Quantity
Price
```

If one product can occur only once per order:

```text
(Order_ID, Product_ID)
```

can be a candidate key.

If the same product can appear multiple times as separate line items, then that combination may not be unique.

A separate:

```text
Order_Item_ID
```

may be required.

Therefore:

> [!tip]
> Always understand the real-world rule before declaring a candidate key.

---

# 49. Candidate Key and Business Rules

Suppose:

```text
Email
```

is currently unique.

Does that automatically make it a candidate key?

Not necessarily.

Ask:

> Is email guaranteed to remain unique under the business rules?

If yes:

```text
Email
→ Candidate Key
```

If not:

it may not be an appropriate candidate key.

This is an important database-design mindset.

---

# 50. Candidate Key and Stability

Uniqueness is necessary but practical key selection also considers stability.

Example:

```text
Email
```

may be unique but can change.

```text
Employee_ID
```

may be artificial but stable.

Therefore:

```text
Candidate Key
→ Theoretical possibility

Primary Key selection
→ Design decision
```

These are not exactly the same question.

---

# 51. Candidate Key Finding — Exam Algorithm

> [!important] Must Master

When given a relation and functional dependencies:

### Step 1

Write all attributes.

### Step 2

List attributes that never occur on RHS.

### Step 3

Use them as a starting set.

### Step 4

Calculate closure.

### Step 5

If closure contains all attributes:

```text
Super Key
```

### Step 6

Check whether any attribute can be removed.

### Step 7

If no attribute can be removed:

```text
Candidate Key
```

### Step 8

Search for other minimal keys.

---

# 52. Candidate Key Closure Example

Given:

```text
R(A,B,C,D,E)
```

FDs:

```text
A → B
B → C
CD → E
```

Find candidate key.

### Step 1 — RHS

RHS:

```text
B
C
E
```

Not on RHS:

```text
A
D
```

Start:

```text
AD
```

### Step 2 — Closure

```text
AD+
= {A,D}
```

Use:

```text
A → B
```

Now:

```text
{A,B,D}
```

Use:

```text
B → C
```

Now:

```text
{A,B,C,D}
```

Use:

```text
CD → E
```

Now:

```text
{A,B,C,D,E}
```

Therefore:

```text
AD
→ Super Key
```

### Step 3 — Minimality

Remove A:

```text
D+
= {D}
```

Not all attributes.

Remove D:

```text
A+
= {A,B,C}
```

Not all attributes.

Therefore:

```text
AD
→ Candidate Key
```

---

# 53. Advanced Pattern — Multiple Candidate Keys

Suppose:

```text
R(A,B,C,D)
```

FDs:

```text
A → B
B → A
A → C
B → C
C → D
```

Find candidate keys.

`A+`:

```text
A
→ B
→ C
→ D
```

So:

```text
A+
= ABCD
```

Therefore:

```text
A
→ Candidate Key
```

`B+`:

```text
B
→ A
→ C
→ D
```

So:

```text
B+
= ABCD
```

Therefore:

```text
B
→ Candidate Key
```

Candidate keys:

```text
{A}
{B}
```

---

# 54. Advanced Pattern — No Single Attribute Works

Suppose:

```text
R(A,B,C,D)
```

FDs:

```text
A → B
B → A
C → D
```

Check:

```text
A+
= A,B
```

Not enough.

```text
C+
= C,D
```

Not enough.

Try:

```text
AC+
```

Then:

```text
A → B
C → D
```

Therefore:

```text
AC+
= A,B,C,D
```

Neither `A` nor `C` alone is sufficient.

Therefore:

```text
AC
→ Candidate Key
```

---

# 55. Advanced Pattern — Redundant Composite Key

Suppose:

```text
A
```

already determines everything.

Then:

```text
AB
```

is not a candidate key.

It is only a super key.

Why?

Because:

```text
A
```

is enough.

Therefore:

> [!warning]
> **Never call a larger unique set a candidate key without checking minimality.**

---

# 56. Candidate Key Shortcut

> [!tip]
> **Fast test:**
>
> If a key contains multiple attributes, remove one attribute at a time.
>
> If the remaining set still determines all attributes, the original set is not a candidate key.

Example:

```text
ABC
```

Remove `A`:

```text
BC
```

If `BC+ = all attributes`:

```text
ABC
→ Not Candidate
```

---

# 57. Candidate Key Recognition Table

| Question Phrase | Answer |
|---|---|
| Minimal unique identifier | Candidate Key |
| Any unique identifier set | Super Key |
| Selected candidate key | Primary Key |
| Candidate key not selected | Alternate Key |
| Multiple attributes needed | Composite Candidate Key |
| Determines all attributes | Super Key candidate |
| No unnecessary attributes | Candidate Key |

---

# 58. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Candidate key means any unique column

Not exactly.

A candidate key must be:

```text
Unique + Minimal
```

---

### Mistake 2 — Candidate key and primary key are identical

Wrong.

There can be multiple candidate keys but only one selected primary-key constraint.

---

### Mistake 3 — Ignoring minimality

This is the most common mistake.

If:

```text
A
```

is enough, then:

```text
AB
```

is not a candidate key.

---

### Mistake 4 — Thinking every super key is a candidate key

Wrong.

Every candidate key is a super key.

But not every super key is a candidate key.

Relationship:

```text
Candidate Keys ⊂ Super Keys
```

---

### Mistake 5 — Assuming a candidate key must be one column

Wrong.

A candidate key can be composite.

Example:

```text
(A,B)
```

---

### Mistake 6 — Ignoring business rules

A column appearing unique in sample data does not automatically prove it is a candidate key.

The uniqueness must be guaranteed by the intended data model/business rules.

---

### Mistake 7 — Forgetting functional dependencies

In theoretical DBMS questions, candidate keys are often determined using functional dependencies and attribute closure.

---

### Mistake 8 — Confusing alternate key with non-key

An alternate key is still a candidate key.

It is simply not selected as the primary key.

---

### Mistake 9 — Assuming candidate keys are only SQL constraints

Candidate key is fundamentally a relational-model concept.

SQL constraints are implementation mechanisms.

---

### Mistake 10 — Forgetting prime attributes

An attribute belonging to at least one candidate key is a prime attribute.

This matters in normalization.

---

# 59. Must-Master Patterns

> [!important] Must Master

1. Candidate key definition
2. Unique + minimal
3. Candidate key vs super key
4. Candidate key vs primary key
5. Candidate key vs alternate key
6. Composite candidate key
7. Minimality testing
8. Attribute closure
9. Functional dependencies
10. RHS shortcut
11. Attributes not on RHS
12. Multiple candidate keys
13. Prime attributes
14. Non-prime attributes
15. Candidate keys and 2NF
16. Candidate keys and 3NF
17. Candidate keys and BCNF
18. Natural candidate keys
19. Surrogate key vs candidate key
20. Candidate key selection
21. Candidate key from business rules
22. Candidate key in M:N tables
23. Candidate key in junction tables
24. Candidate key and functional dependency
25. Candidate key exam problems

---

# 60. Master Key Comparison

| Concept | Definition | Example |
|---|---|---|
| Super Key | Any attribute set that uniquely identifies rows | `{A,B}` |
| Candidate Key | Minimal super key | `{A}` |
| Primary Key | Selected candidate key | `{A}` |
| Alternate Key | Candidate key not selected | `{B}` |
| Composite Key | Key containing multiple attributes | `{A,B}` |
| Foreign Key | References another table's key | `Dept_ID` |

Important:

**Composite** describes the structure of a key.

Therefore a key can be:

```text
Composite Candidate Key
```

or:

```text
Composite Primary Key
```

---

# 61. Candidate Key Hierarchy

```text
                    SUPER KEY
                       |
          Remove unnecessary attributes
                       ↓
                 CANDIDATE KEY
                  /          \
                 /            \
        Selected             Not selected
           ↓                      ↓
     PRIMARY KEY             ALTERNATE KEY
```

This is the most important conceptual diagram for keys.

---

# 62. Candidate Key Decision Tree

> [!important]
> Use this during an exam:

```text
Can this attribute set uniquely identify every row?
                |
              NO
                ↓
          Not a Super Key

              YES
                ↓
       Can any attribute be removed
       while keeping uniqueness?
                |
          ┌─────┴─────┐
         YES          NO
          ↓            ↓
     Super Key     Candidate Key
                       |
                 Choose one
                       ↓
                  Primary Key
```

---

# 63. Functional Dependency Recognition

> [!tip]
> If you see:

```text
A → B
B → C
C → D
```

think:

```text
A → B
A → C
A → D
```

through transitivity.

Therefore:

```text
A+
```

may contain:

```text
A,B,C,D
```

If that is the complete relation:

```text
A
→ Candidate Key
```

after checking minimality.

---

# 64. Fast Closure Method

For aptitude-style DBMS questions:

```text
1. Start with the suspected key.
2. Write its attributes.
3. Apply every FD whose left side is available.
4. Add newly determined attributes.
5. Repeat until nothing changes.
6. Compare closure with relation attributes.
7. Check minimality.
```

Memory:

```text
Closure = "What can this set reach?"
```

---

# 65. Candidate Key Formula Sheet

> [!summary] Formula Sheet

```text
Candidate Key
=
Minimal Super Key

Candidate Key
=
Unique + Minimal

Primary Key
=
Selected Candidate Key

Alternate Key
=
Candidate Key not selected as Primary Key

Candidate Key K
→ K+ = All attributes

Prime Attribute
=
Attribute belonging to at least one Candidate Key

Non-Prime Attribute
=
Attribute belonging to no Candidate Key

Candidate Key
⊆
Super Key

Primary Key
⊆
Candidate Keys
```

For functional dependency problems:

```text
If K+ = R
→ K is a Super Key

If K+ = R
and no proper subset of K has closure R
→ K is a Candidate Key
```

---

# 66. Quick Revision

> [!summary] One-Minute Revision

```text
CANDIDATE KEY
→ Minimal set of attributes that uniquely identifies every row.

CORE RULE
→ Unique + Minimal

SUPER KEY
→ Any set that uniquely identifies rows.

CANDIDATE KEY
→ Minimal Super Key.

PRIMARY KEY
→ One selected Candidate Key.

ALTERNATE KEY
→ Candidate Key not selected as Primary Key.

COMPOSITE CANDIDATE KEY
→ Candidate Key containing multiple attributes.

FUNCTIONAL DEPENDENCY
→ Used to determine what attributes can be derived.

ATTRIBUTE CLOSURE
→ K+ tells what attributes K can determine.

If K+ = all attributes
→ K is a Super Key.

If no proper subset of K determines all attributes
→ K is a Candidate Key.

RHS SHORTCUT
→ Attributes never appearing on RHS are strong candidates
  to be included in every key.

PRIME ATTRIBUTE
→ Belongs to at least one Candidate Key.

NON-PRIME ATTRIBUTE
→ Belongs to no Candidate Key.

NORMALIZATION
→ Candidate keys are essential for 2NF, 3NF and BCNF analysis.

FAST RECOGNITION

"Minimal unique identifier"
→ Candidate Key

"Any unique attribute set"
→ Super Key

"Selected candidate"
→ Primary Key

"Candidate not selected"
→ Alternate Key

"Multiple columns together"
→ Composite Key
```

# 67. Golden Memory Trick

**Candidate Key = A minimal identity candidate: remove anything from it and it stops uniquely identifying the row.**

# 68. One-Line Recognition

**If a question says "minimal set of attributes that uniquely identifies every row," immediately think Candidate Key.**