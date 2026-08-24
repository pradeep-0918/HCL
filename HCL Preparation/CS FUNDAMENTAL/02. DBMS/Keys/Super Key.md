---
type: concept
subject: dbms
topic: "Super Key"
parent: "Keys"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - dbms
  - keys
  - super-key
  - candidate-key
  - primary-key
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
  - "[[Candidate Key]]"
  - "[[Alternate Key]]"
  - "[[Composite Key]]"
  - "[[Functional Dependency]]"
  - "[[Normalization]]"
---

# Super Key

## 1. Core Concept

> [!summary]
> A **Super Key** is a set of one or more attributes that can uniquely identify every row in a relation.

The most important idea is:

**Super Key = Any attribute set that uniquely identifies a row.**

It does **not** need to be minimal.

Example:

| Student_ID | Email | Name |
|---:|---|---|
| 101 | arun@gmail.com | Arun |
| 102 | priya@gmail.com | Priya |
| 103 | ravi@gmail.com | Ravi |

If `Student_ID` is unique, then all of these can be super keys:

```text
{Student_ID}

{Student_ID, Name}

{Student_ID, Email}

{Student_ID, Name, Email}
```

Why?

Because every set contains `Student_ID`, which already uniquely identifies the row.

But only:

```text
{Student_ID}
```

is minimal.

Therefore:

```text
{Student_ID}
→ Candidate Key

{Student_ID, Name}
→ Super Key but NOT Candidate Key
```

---

# 2. Basic Meaning

A super key is any combination of attributes that is sufficient to uniquely identify tuples.

The word **super** means:

> It may contain more attributes than necessary.

For example:

```text
Student_ID
```

may uniquely identify a student.

Then:

```text
Student_ID + Name
```

also uniquely identifies the student.

But `Name` adds no identification power.

Therefore:

```text
Student_ID
→ Minimal

Student_ID + Name
→ Non-minimal
```

Both are super keys.

Only the first is a candidate key.

---

# 3. Main Formula

The most important relationship is:

```text
Super Key
=
Any Unique Attribute Set
```

And:

```text
Candidate Key
=
Minimal Super Key
```

Therefore:

```text
Candidate Key ⊆ Super Key
```

Every candidate key is a super key.

But:

```text
Not every Super Key is a Candidate Key.
```

---

# 4. Core Relationship

Memorize this hierarchy:

```text
SUPER KEY
    ↓
Remove unnecessary attributes
    ↓
CANDIDATE KEY
    ↓
Choose one
    ↓
PRIMARY KEY
```

Remaining candidate keys:

```text
CANDIDATE KEYS
    ↓
Not selected as Primary
    ↓
ALTERNATE KEYS
```

This hierarchy is one of the most important DBMS interview concepts.

---

# 5. Super Key Example

Consider:

| ID | Email | Name | Department |
|---:|---|---|---|
| 101 | a@gmail.com | Arun | CSE |
| 102 | p@gmail.com | Priya | ECE |
| 103 | r@gmail.com | Ravi | CSE |

Assume:

```text
ID
```

is unique.

Then:

```text
{ID}
```

is a super key.

Also:

```text
{ID, Name}
```

is a super key.

Also:

```text
{ID, Department}
```

is a super key.

Also:

```text
{ID, Email, Name}
```

is a super key.

Why?

Because each set contains `ID`.

---

# 6. Super Key vs Candidate Key

This is the most important distinction.

| Property | Super Key | Candidate Key |
|---|---|---|
| Uniquely identifies rows | Yes | Yes |
| Minimal | Not required | Required |
| Can contain extra attributes | Yes | No |
| Number possible | Usually many | Can be many |
| Example | `{ID, Name}` | `{ID}` |

Memory:

> [!tip]
> **Super Key asks: "Is it enough?"**
>
> **Candidate Key asks: "Is it enough and minimal?"**

---

# 7. Super Key vs Primary Key

A primary key is a selected candidate key.

Therefore:

```text
Super Key
    ↓
Candidate Key
    ↓
Primary Key
```

Example:

```text
Super Keys:
{ID}
{ID, Name}
{ID, Email}
{ID, Name, Email}
```

Candidate key:

```text
{ID}
```

Primary key:

```text
{ID}
```

if the designer chooses it.

---

# 8. Super Key vs Alternate Key

Suppose:

```text
Candidate Keys:

{Student_ID}
{Email}
```

Choose:

```text
Student_ID
```

as primary key.

Then:

```text
Email
→ Alternate Key
```

Both are candidate keys.

And both are also super keys.

This gives:

```text
Email
→ Candidate Key
→ Super Key
→ Alternate Key
```

---

# 9. Important Property

> [!important]
> **Every Candidate Key is a Super Key.**

But:

> [!warning]
> **Every Super Key is NOT necessarily a Candidate Key.**

Example:

```text
{Student_ID, Name}
```

may be a super key.

But if:

```text
Student_ID
```

alone is enough, then it is not minimal.

Therefore it is not a candidate key.

---

# 10. Why Is `{ID, Name}` a Super Key?

Suppose:

```text
ID
```

uniquely identifies rows.

If:

```text
ID = 101
```

already identifies one row, then adding:

```text
Name
```

cannot make the identification less unique.

Therefore:

```text
{ID, Name}
```

still uniquely identifies the row.

Hence:

```text
{ID, Name}
→ Super Key
```

---

# 11. Why Is `{ID, Name}` Not a Candidate Key?

Because:

```text
ID
```

alone is sufficient.

Therefore:

```text
Name
```

is unnecessary.

So:

```text
{ID, Name}
```

is not minimal.

Hence:

```text
Super Key
≠ Candidate Key
```

in this example.

---

# 12. Minimality Test

This is the fastest way to determine whether a super key is a candidate key.

Suppose:

```text
K = {A, B, C}
```

Check:

```text
Remove A → {B,C}
Remove B → {A,C}
Remove C → {A,B}
```

If any smaller subset still uniquely identifies all rows:

```text
ABC
→ Not Candidate Key
```

If removing any attribute breaks uniqueness:

```text
ABC
→ Candidate Key
```

---

# 13. Super Key Recognition Trick

> [!important]
> If the question says:
>
> "A set of attributes that uniquely identifies each tuple"
>
> think:
>
> **Super Key**

If it says:

> "A minimal set of attributes that uniquely identifies each tuple"

think:

**Candidate Key**

If it says:

> "The candidate key selected by the database designer"

think:

**Primary Key**

---

# 14. Simple Example

Table:

| Employee_ID | Name |
|---:|---|
| 1 | Arun |
| 2 | Priya |
| 3 | Ravi |

Assume `Employee_ID` is unique.

Possible super keys:

```text
{Employee_ID}

{Employee_ID, Name}
```

Both uniquely identify rows.

Candidate key:

```text
{Employee_ID}
```

Why?

Because it is minimal.

---

# 15. Example with Email

Suppose:

| Employee_ID | Email | Name |
|---:|---|---|
| 1 | a@x.com | Arun |
| 2 | p@x.com | Priya |
| 3 | r@x.com | Ravi |

Assume both:

```text
Employee_ID
Email
```

are unique.

Then possible candidate keys:

```text
{Employee_ID}
{Email}
```

Both are also super keys.

Additional super keys include:

```text
{Employee_ID, Email}
{Employee_ID, Name}
{Email, Name}
{Employee_ID, Email, Name}
```

The minimal ones are:

```text
{Employee_ID}
{Email}
```

---

# 16. Important Pattern

Suppose:

```text
Candidate Keys:
A
B
```

Then possible super keys include:

```text
A
B
AB
AC
AD
...
```

provided the added attributes do not destroy uniqueness.

General rule:

> [!tip]
> **Once a set is a super key, adding more attributes keeps it a super key.**

This is a powerful property.

---

# 17. Super Key Superset Property

Suppose:

```text
{A}
```

is a super key.

Then:

```text
{A,B}
```

is also a super key.

And:

```text
{A,B,C}
```

is also a super key.

And:

```text
{A,B,C,D}
```

is also a super key.

Because every larger set still contains `A`.

This is called the **superset property** of super keys.

---

# 18. Superset Property

> [!important]
> If `K` is a super key, every superset of `K` is also a super key.

Example:

```text
K = {A}
```

If `A` uniquely identifies rows:

```text
{A}
{A,B}
{A,C}
{A,B,C}
{A,B,C,D}
```

are all super keys.

But only `{A}` may be a candidate key.

---

# 19. Candidate Key as Minimal Super Key

This can be visualized as:

```text
Super Keys
├── {A}
├── {A,B}
├── {A,C}
├── {A,B,C}
└── ...

Minimal Super Keys
└── {A}
       ↓
Candidate Key
```

If there are multiple minimal super keys:

```text
Super Keys
├── {A}
├── {B}
├── {A,B}
├── {A,C}
├── {B,C}
└── ...

Candidate Keys
├── {A}
└── {B}
```

---

# 20. Super Key and Functional Dependency

Functional dependencies provide a formal way to identify super keys.

For relation:

```text
R(A,B,C,D)
```

If:

```text
A → B
A → C
A → D
```

then:

```text
A → A,B,C,D
```

Therefore:

```text
A+
=
{A,B,C,D}
```

So:

```text
A
```

is a super key.

If `A` is minimal:

```text
A
→ Candidate Key
```

---

# 21. Attribute Closure

The closure of an attribute set tells us which attributes can be determined from it.

Notation:

```text
A+
```

means:

```text
Closure of A
```

If:

```text
A+ = all attributes of R
```

then:

```text
A
→ Super Key
```

Then check minimality to determine whether it is a candidate key.

---

# 22. Closure Example

Given:

```text
R(A,B,C,D)
```

FDs:

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

Apply:

```text
A → B
```

Now:

```text
A+ = {A,B}
```

Apply:

```text
B → C
```

Now:

```text
A+ = {A,B,C}
```

Apply:

```text
C → D
```

Now:

```text
A+ = {A,B,C,D}
```

Therefore:

```text
A
→ Super Key
```

Because `A` is a single attribute, it is also minimal.

Therefore:

```text
A
→ Candidate Key
```

---

# 23. Super Key Example with Composite Attributes

Given:

```text
R(A,B,C,D)
```

FDs:

```text
A → B
C → D
```

Calculate:

```text
AC+
```

Start:

```text
AC+
= {A,C}
```

Apply:

```text
A → B
```

Now:

```text
{A,B,C}
```

Apply:

```text
C → D
```

Now:

```text
{A,B,C,D}
```

Therefore:

```text
AC
→ Super Key
```

Check:

```text
A+
= {A,B}

C+
= {C,D}
```

Neither determines all attributes.

Therefore:

```text
AC
→ Candidate Key
```

---

# 24. Example of a Non-Minimal Super Key

Suppose:

```text
R(A,B,C,D)
```

and:

```text
A → B,C,D
```

Then:

```text
A+
= ABCD
```

So:

```text
A
→ Super Key
```

Now consider:

```text
AB
```

Because `A` already determines everything:

```text
AB+
= ABCD
```

Therefore:

```text
AB
→ Super Key
```

But:

```text
A
```

alone is enough.

Therefore:

```text
AB
→ NOT Candidate Key
```

---

# 25. Fast Exam Shortcut

> [!tip]
> If you already know that:
>
> `A` is a candidate key,
>
> then:
>
> `A + any other attributes`
>
> are automatically super keys.
>
> They are not candidate keys because they are not minimal.

Example:

```text
A = Candidate Key
```

Then:

```text
AB → Super Key
AC → Super Key
AD → Super Key
ABC → Super Key
ABD → Super Key
ABCD → Super Key
```

But:

```text
A
```

is the minimal one.

---

# 26. Super Key Count

A common theoretical question asks:

> How many super keys are possible if the only candidate key is a single attribute `A` in a relation with `n` attributes?

If `A` is mandatory and the remaining `n-1` attributes can be optionally added:

```text
Number of Super Keys
=
2^(n-1)
```

Why?

Each of the remaining attributes has two choices:

```text
Include
or
Do not include
```

Therefore:

```text
2 × 2 × ... × 2
=
2^(n-1)
```

---

# 27. Super Key Count Example

Suppose relation:

```text
R(A,B,C,D)
```

and:

```text
A
```

is the only candidate key.

There are:

```text
n = 4
```

attributes.

A super key must contain `A`.

Remaining attributes:

```text
B,C,D
```

Each can be included or excluded.

Therefore:

```text
Number of Super Keys
=
2^(4-1)
=
2^3
=
8
```

List:

```text
A
AB
AC
AD
ABC
ABD
ACD
ABCD
```

---

# 28. Important Formula

> [!summary]
> If there is **one candidate key containing one attribute** and the relation has `n` attributes:

```text
Number of Super Keys
=
2^(n-1)
```

Example:

```text
n = 5

Super Keys
=
2^4
=
16
```

This shortcut is useful for aptitude-style DBMS questions.

---

# 29. Composite Candidate Key and Super-Key Count

Suppose the only candidate key is:

```text
(A,B)
```

and relation has:

```text
n
```

attributes.

The mandatory attributes are:

```text
A,B
```

Remaining:

```text
n - 2
```

attributes.

Therefore:

```text
Number of Super Keys
=
2^(n-2)
```

assuming `(A,B)` is the only minimal key and every superset is considered.

---

# 30. Example — Composite Key Count

Relation:

```text
R(A,B,C,D,E)
```

Candidate key:

```text
AB
```

Only candidate key.

Number of remaining attributes:

```text
5 - 2
=
3
```

Therefore:

```text
Number of Super Keys
=
2^3
=
8
```

They are:

```text
AB
ABC
ABD
ABE
ABCD
ABCE
ABDE
ABCDE
```

---

# 31. Multiple Candidate Keys — Advanced Count

Suppose a relation has multiple candidate keys.

Then counting super keys becomes more complicated because their supersets can overlap.

Example:

```text
Candidate Keys:
A
B
```

Relation:

```text
R(A,B,C)
```

All super keys are sets containing either `A` or `B`.

Possible super keys:

```text
A
B
AB
AC
BC
ABC
```

So:

```text
6 Super Keys
```

Do not simply add:

```text
2^(n-1) + 2^(n-1)
```

because some super keys may be counted twice.

---

# 32. Common Counting Trap

Suppose:

```text
Candidate Keys:
A
B
```

and relation has:

```text
A,B,C,D
```

Super keys containing `A`:

```text
2^3 = 8
```

Super keys containing `B`:

```text
2^3 = 8
```

But sets containing both `A` and `B` are counted twice.

Number containing both:

```text
2^2 = 4
```

Therefore:

```text
Total
=
8 + 8 - 4
=
12
```

This is an inclusion-exclusion pattern.

---

# 33. Super Key Counting Pattern

> [!important] Exam Pattern

If one candidate key:

```text
K
```

has `k` attributes and relation has `n` attributes:

```text
Number of supersets of K
=
2^(n-k)
```

This counts all super keys containing that candidate key.

If there are multiple candidate keys, account for overlaps.

---

# 34. Real-Time Example — Employee Database

Consider:

```text
EMPLOYEE
----------------
Employee_ID
Email
Name
Department
Salary
```

Suppose:

```text
Employee_ID
```

is unique.

Then:

```text
Employee_ID
Employee_ID + Name
Employee_ID + Department
Employee_ID + Salary
Employee_ID + Email
...
```

can all be super keys.

But:

```text
Employee_ID
```

is the simplest candidate key.

---

# 35. Real-Time Example — E-Commerce

Table:

```text
PRODUCT
----------------
Product_ID
SKU
Name
Price
Category
```

Suppose:

```text
Product_ID
```

is unique.

Then:

```text
Product_ID
Product_ID + Name
Product_ID + Price
Product_ID + Category
Product_ID + Name + Price
...
```

are super keys.

If:

```text
SKU
```

is also guaranteed unique:

```text
SKU
```

is another candidate key.

---

# 36. Real-Time Example — University

Table:

```text
ENROLLMENT
----------------
Student_ID
Course_ID
Semester
Grade
```

Suppose:

```text
(Student_ID, Course_ID)
```

uniquely identifies each enrollment.

Then:

```text
(Student_ID, Course_ID)
```

is a candidate key.

Adding any extra attribute gives a super key:

```text
(Student_ID, Course_ID, Semester)
```

```text
(Student_ID, Course_ID, Grade)
```

```text
(Student_ID, Course_ID, Semester, Grade)
```

But these are not candidate keys.

---

# 37. Real-Time Example — Banking

Table:

```text
ACCOUNT
----------------
Account_Number
Customer_ID
Branch_ID
Balance
```

Suppose:

```text
Account_Number
```

is unique.

Then:

```text
Account_Number
Account_Number + Customer_ID
Account_Number + Branch_ID
Account_Number + Balance
...
```

are super keys.

The minimal identifier:

```text
Account_Number
```

can be a candidate key.

---

# 38. Super Key and Database Design

Super keys are useful conceptually because they tell us:

> "This set of attributes is sufficient to identify a row."

But when designing a database, we generally prefer a minimal candidate key as the primary key rather than carrying unnecessary attributes.

Why?

Because unnecessary attributes can make:

- Indexes larger
- Foreign keys larger
- Joins more complicated
- Storage less efficient
- Schema design harder to understand

Therefore:

```text
Super Key
→ Identification possibility

Candidate Key
→ Minimal identification

Primary Key
→ Selected implementation choice
```

---

# 39. Super Key and Foreign Key

A foreign key does not have to be a super key in its child table.

Example:

```text
Department
-----------
Department_ID PK
```

Employee:

```text
Employee_ID PK
Department_ID FK
```

`Department_ID`

is not unique in Employee.

Therefore:

```text
Department_ID
→ Foreign Key
→ Not necessarily Super Key
```

This is a very important distinction.

---

# 40. Super Key and Primary Key

A primary key is always a super key.

Why?

Because a primary key is a candidate key, and every candidate key is a super key.

Therefore:

```text
Primary Key
⊂ Candidate Key
⊂ Super Key
```

Conceptually.

---

# 41. Super Key and Composite Key

A super key may contain:

```text
One attribute
```

or:

```text
Multiple attributes
```

Therefore:

```text
A
```

can be a super key.

And:

```text
A,B
```

can also be a super key.

"Composite" simply means multiple attributes.

It does not automatically mean candidate key.

---

# 42. Candidate vs Super vs Primary

> [!important] Must Memorize

```text
SUPER KEY
→ Any unique attribute set

CANDIDATE KEY
→ Minimal unique attribute set

PRIMARY KEY
→ Selected candidate key
```

Example:

```text
Super Keys:
AB
ABC
ABCD

Candidate Key:
AB

Primary Key:
AB
```

if `AB` is selected.

---

# 43. Advanced Interview Question

## Q1. What is a super key?

### Strong Answer

> A super key is a set of one or more attributes that functionally determines all attributes of a relation, thereby uniquely identifying every tuple. It does not have to be minimal.

---

# 44. Interview Question

## Q2. Is every candidate key a super key?

### Answer

Yes.

A candidate key is a minimal super key.

---

# 45. Interview Question

## Q3. Is every super key a candidate key?

### Answer

No.

A super key may contain unnecessary attributes.

Example:

```text
Student_ID
```

is enough, so:

```text
(Student_ID, Name)
```

is a super key but not a candidate key.

---

# 46. Interview Question

## Q4. What is the difference between a super key and candidate key?

### Answer

The difference is minimality.

```text
Super Key
→ Unique

Candidate Key
→ Unique + Minimal
```

---

# 47. Interview Question

## Q5. What is the difference between candidate key and primary key?

### Answer

A table may have multiple candidate keys, but only one candidate key is selected as the primary key.

---

# 48. Interview Question

## Q6. Can a super key contain extra attributes?

### Answer

Yes.

That is the major difference between a super key and candidate key.

---

# 49. Interview Question

## Q7. Can a super key contain multiple attributes?

### Answer

Yes.

A super key can contain one or more attributes.

---

# 50. Interview Question

## Q8. Is a foreign key necessarily a super key?

### Answer

No.

A foreign key usually does not need to be unique in the child table.

For example:

```text
Department_ID
```

can appear in many Employee rows.

---

# 51. Interview Question

## Q9. How do you determine whether an attribute set is a super key?

### Answer

Calculate its attribute closure.

If:

```text
K+ = all attributes of the relation
```

then:

```text
K
```

is a super key.

---

# 52. Interview Question

## Q10. How do you determine whether a super key is a candidate key?

### Answer

Check minimality.

If no proper subset of the super key can determine all attributes, then it is a candidate key.

---

# 53. Interview Question

## Q11. What is the role of functional dependency in finding super keys?

### Answer

Functional dependencies determine which attributes can be derived from a given attribute set. Attribute closure uses these dependencies to determine whether the set can determine the complete relation.

---

# 54. Interview Question

## Q12. What is attribute closure?

### Answer

Attribute closure is the set of all attributes functionally determined by a given attribute set under the specified functional dependencies.

---

# 55. Interview Question

## Q13. If `A+` contains all attributes, what can you conclude?

### Answer

`A` is a super key.

If `A` is minimal, then it is a candidate key.

---

# 56. Interview Question

## Q14. If `AB` is a super key and `A` is also a super key, is `AB` a candidate key?

### Answer

No.

Because:

```text
A
```

alone is sufficient.

Therefore:

```text
AB
```

is not minimal.

---

# 57. Advanced Interview Question

## Q15. If `AB` is a candidate key, is `ABC` a super key?

### Answer

Yes.

Since every superset of a super key is also a super key, and every candidate key is a super key:

```text
AB
→ Super Key

ABC
→ Super Key
```

But `ABC` is not a candidate key because `C` is unnecessary.

---

# 58. Advanced Interview Question

## Q16. If a relation has 5 attributes and its only candidate key is A, how many super keys exist?

### Answer

Since the candidate key has one attribute:

```text
2^(5-1)
=
2^4
=
16
```

---

# 59. Advanced Interview Question

## Q17. If a relation has 6 attributes and its only candidate key is AB, how many super keys exist?

### Answer

Candidate key size:

```text
2
```

Remaining attributes:

```text
6 - 2
=
4
```

Therefore:

```text
2^4
=
16
```

super keys.

---

# 60. Advanced Interview Question

## Q18. Why does adding attributes to a super key keep it a super key?

### Answer

Because the original super key already uniquely identifies the row. Adding additional attributes cannot remove that uniqueness.

This is the superset property.

---

# 61. Advanced Interview Question

## Q19. Can there be many super keys?

### Answer

Yes.

In a relation with multiple attributes, there can be many super keys because any superset of a super key is also a super key.

---

# 62. Advanced Interview Question

## Q20. Can there be multiple candidate keys?

### Answer

Yes.

A relation may have multiple minimal attribute sets that uniquely identify tuples.

Example:

```text
Student_ID
Email
```

can both be candidate keys.

---

# 63. Advanced Interview Question

## Q21. Can there be multiple primary keys?

### Answer

No.

There can be multiple candidate keys, but only one primary-key constraint can be selected for a table.

---

# 64. Advanced Interview Question

## Q22. Is every primary key a candidate key?

### Answer

Yes.

By definition, the primary key is selected from the candidate keys.

---

# 65. Advanced Interview Question

## Q23. Is every primary key a super key?

### Answer

Yes.

Because:

```text
Primary Key
→ Candidate Key
→ Super Key
```

---

# 66. Advanced Interview Question

## Q24. Can a super key be empty?

In the normal relational model, a key must provide identification of tuples, and practical key definitions involve one or more attributes. For placement and interview questions, treat a super key as a non-empty set of attributes unless the problem explicitly introduces unusual theoretical assumptions.

---

# 67. Advanced Interview Question

## Q25. What is the biggest difference between super key and candidate key?

### Answer

**Minimality.**

That single word solves many DBMS MCQs.

```text
Super Key
→ Unique

Candidate Key
→ Unique + Minimal
```

---

# 68. Exam Pattern — Direct Definition

### Question

Which key can contain redundant attributes?

### Answer

**Super Key**

Reason:

A super key does not require minimality.

---

# 69. Exam Pattern — Minimality

### Question

Which key is a minimal super key?

### Answer

**Candidate Key**

---

# 70. Exam Pattern — Selected Key

### Question

Which candidate key is selected to uniquely identify tuples?

### Answer

**Primary Key**

---

# 71. Exam Pattern — Superset

### Question

If `A` is a super key, what about `AB`?

### Answer

`AB` is also a super key.

---

# 72. Exam Pattern — Candidate Test

### Question

`AB` uniquely identifies tuples. `A` also uniquely identifies tuples. Is `AB` a candidate key?

### Answer

No.

It is a super key but not minimal.

---

# 73. Exam Pattern — Closure

### Question

If `AB+ = ABCDE`, what can you conclude?

### Answer

`AB` is a super key.

To determine whether it is a candidate key, test whether `A+` or `B+` or other proper subsets also determine all attributes.

---

# 74. Exam Pattern — Composite

### Question

If no single attribute identifies rows but `(A,B)` does, what is `(A,B)`?

### Answer

It is a candidate key if neither `A` nor `B` alone is sufficient.

It is also a composite key.

---

# 75. Exam Pattern — Prime Attribute

### Question

If candidate keys are `{A,B}` and `{C}`, which attributes are prime?

### Answer

```text
A
B
C
```

All belong to at least one candidate key.

---

# 76. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Super Key must be minimal

Wrong.

Minimality is required for candidate keys.

---

### Mistake 2 — Thinking every super key is a candidate key

Wrong.

Example:

```text
AB
```

may be a super key while:

```text
A
```

is already enough.

---

### Mistake 3 — Forgetting the superset property

If:

```text
A
```

is a super key, then:

```text
AB
ABC
ABCD
```

are also super keys.

---

### Mistake 4 — Confusing super key with primary key

Primary key is one selected candidate key.

Super keys can be numerous.

---

### Mistake 5 — Assuming foreign key is a super key

Wrong.

A foreign key does not need to be unique.

---

### Mistake 6 — Ignoring attribute closure

For theoretical questions, do not judge keys merely from the visible attribute names.

Use functional dependencies.

---

### Mistake 7 — Forgetting minimality after closure

If:

```text
AB+
= all attributes
```

you know `AB` is a super key.

You do not yet know whether it is a candidate key.

You must test subsets.

---

### Mistake 8 — Counting super keys independently for multiple candidate keys

If candidate keys overlap, naive addition double-counts some super keys.

Use inclusion-exclusion where appropriate.

---

# 77. Must-Master Patterns

> [!important] Must Master

1. Super key definition
2. Super key vs candidate key
3. Super key vs primary key
4. Super key vs foreign key
5. Minimality
6. Superset property
7. Attribute closure
8. Functional dependencies
9. Finding super keys
10. Finding candidate keys
11. Composite super keys
12. Number of super keys
13. Multiple candidate keys
14. Inclusion-exclusion in super-key counting
15. Prime attributes
16. Non-prime attributes
17. Candidate key hierarchy
18. Primary key hierarchy
19. Super keys in normalization
20. Interview definitions

---

# 78. Master Comparison

| Property | Super Key | Candidate Key | Primary Key |
|---|---|---|---|
| Unique | Yes | Yes | Yes |
| Minimal | Not required | Yes | Yes |
| Extra attributes allowed | Yes | No | No |
| Can be multiple | Yes | Yes | One selected |
| Determines all attributes | Yes | Yes | Yes |
| Main idea | Any unique set | Minimal unique set | Selected candidate |
| Example | `{A,B}` | `{A}` | `{A}` |

---

# 79. Key Hierarchy

```text
                SUPER KEYS
             /      |      \
            /       |       \
          {A}      {AB}     {AC}
           |
           ↓
    Minimal Super Key
           |
           ↓
      CANDIDATE KEY
           |
           ↓
     Selected Candidate
           |
           ↓
      PRIMARY KEY
```

---

# 80. Super Key Decision Tree

> [!important]
> Use this in exams:

```text
Does the attribute set uniquely identify every row?
                |
             NO | YES
                |
                ↓
          Is it minimal?
             /     \
           NO       YES
           ↓         ↓
      SUPER KEY   CANDIDATE KEY
                     |
                     ↓
              Selected as PK?
                 /       \
               YES        NO
                ↓          ↓
          PRIMARY KEY   ALTERNATE KEY
```

Important correction to the flow:

If the answer to "Is it minimal?" is **NO**, it is still a **Super Key**, not something outside the key hierarchy.

---

# 81. Super Key Formula Sheet

> [!summary] Formula Sheet

```text
Super Key
=
Any set of attributes that uniquely identifies every tuple

Candidate Key
=
Minimal Super Key

Primary Key
=
Selected Candidate Key

Candidate Key
⊆
Super Key

Primary Key
→ Candidate Key
→ Super Key

If K+ = R
→ K is a Super Key

If K+ = R
and no proper subset of K has closure R
→ K is a Candidate Key

If K is a Super Key
→ Every superset of K is also a Super Key

If only candidate key has k attributes
and relation has n attributes:

Number of Super Keys
=
2^(n-k)

Special case:
Single-attribute candidate key

Number of Super Keys
=
2^(n-1)
```

---

# 82. Quick Revision

> [!summary] One-Minute Revision

```text
SUPER KEY
→ Any set of one or more attributes that uniquely identifies
  every row.

CORE RULE
→ Unique is required.
→ Minimality is NOT required.

CANDIDATE KEY
→ Minimal Super Key.

PRIMARY KEY
→ Selected Candidate Key.

ALTERNATE KEY
→ Candidate Key not selected as Primary Key.

SUPerset PROPERTY
→ If K is a Super Key,
  every superset of K is also a Super Key.

ATTRIBUTE CLOSURE
→ K+ tells what K can determine.

If:
K+ = all attributes
→ K is a Super Key.

If:
K+ = all attributes
and no proper subset works
→ K is a Candidate Key.

COUNTING

If only candidate key has k attributes
and relation has n attributes:

Super Keys = 2^(n-k)

If candidate key is A
and relation has n attributes:

Super Keys = 2^(n-1)

MOST IMPORTANT DIFFERENCE

Super Key
→ Unique

Candidate Key
→ Unique + Minimal

Primary Key
→ Selected Candidate Key

FAST RECOGNITION

"Any set that uniquely identifies"
→ Super Key

"Minimal unique set"
→ Candidate Key

"Selected candidate"
→ Primary Key

"Candidate not selected"
→ Alternate Key

"Multiple columns"
→ Composite Key
```

# 83. Golden Memory Trick

**Super Key = "Enough to identify"; Candidate Key = "Enough and nothing extra."**

# 84. One-Line Recognition

**If an attribute set uniquely identifies every row, it is a Super Key; if it is also minimal, it becomes a Candidate Key.**