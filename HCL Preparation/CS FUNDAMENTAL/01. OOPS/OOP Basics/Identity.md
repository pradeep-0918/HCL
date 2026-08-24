---
type: concept
subject: aptitude
topic: "Identity"
parent: "OOP Basics"
company: HCL
difficulty: easy
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - identity
  - object-oriented-programming
  - quantitative-aptitude
wikilinks:
  - "[[OOP Basics]]"
  - "[[Class]]"
  - "[[Object]]"
  - "[[State]]"
  - "[[Behavior]]"
---

# Identity

## 1. Core Concept

> [!summary]
> **Identity** is the unique characteristic that distinguishes one object from another object, even when both objects have the same state and behavior.

An object has three fundamental characteristics:

- **State** → What it has
- **Behavior** → What it does
- **Identity** → Which object it is

Example:

```java
class Student {
    String name;
    int marks;
}

Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s1.marks = 90;

s2.name = "Arun";
s2.marks = 90;
```

Both objects have the same state:

```text
name = Arun
marks = 90
```

But they are still two different objects.

Why?

Because they were created separately:

```java
new Student();
new Student();
```

Therefore:

```text
s1 → Object 1
s2 → Object 2
```

> [!important]
> **Same state does not mean same identity.**

---

## 2. Basic Meaning

Identity tells us **which particular object** we are dealing with.

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
```

Both objects belong to the same class.

They may even have exactly the same values:

```java
s1.name = "Arun";
s1.marks = 90;

s2.name = "Arun";
s2.marks = 90;
```

Still:

```text
s1 → Object 1
s2 → Object 2
```

Their identities are different.

### Simple Analogy

Imagine two identical books.

Both books may have:

```text
Title = Java
Pages = 500
```

Their content and properties may be identical.

But they are still two physical books.

That distinction represents **identity**.

---

## 3. Main Formula

There is no mathematical formula for identity.

For OOP questions, remember:

$$
\text{Identity} = \text{Uniqueness of an Object}
$$

Or:

$$
\text{Identity} \rightarrow \text{Which Object It Is}
$$

The three basic characteristics of an object are:

$$
\text{Object} = \text{State} + \text{Behavior} + \text{Identity}
$$

### Java Reference Example

```java
Student s1 = new Student();
Student s2 = new Student();
```

This creates:

```text
2 reference variables
2 objects
2 distinct identities
```

But:

```java
Student s2 = s1;
```

creates no new object.

Now:

```text
2 reference variables
1 object
1 object identity
```

---

## 4. Important Properties

### 4.1 Identity Distinguishes Objects

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
```

Even if both objects contain the same data, they are separate objects.

Therefore:

$$
\boxed{\text{Different objects} \rightarrow \text{Different identities}}
$$

---

### 4.2 Same State Does Not Mean Same Identity

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();

s1.marks = 90;
s2.marks = 90;
```

Both have:

```text
marks = 90
```

But:

```text
s1 → Object 1
s2 → Object 2
```

Therefore:

$$
\boxed{\text{Same State} \neq \text{Same Identity}}
$$

---

### 4.3 One Object Can Have Multiple References

Consider:

```java
Student s1 = new Student();
Student s2 = s1;
```

Here:

```text
s1 ─┐
    ├──→ Same Student Object
s2 ─┘
```

There are two references but only one object.

Therefore:

$$
\boxed{2\text{ references} \rightarrow 1\text{ object}}
$$

Both references refer to the same object identity.

---

### 4.4 Two `new` Operations Create Separate Objects

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
```

Each `new` expression creates a separate object.

Therefore:

```text
new Student() → Object 1
new Student() → Object 2
```

Hence:

$$
\boxed{2\text{ new operations} \rightarrow 2\text{ objects}}
$$

---

### 4.5 Identity Is Different From Object State

State can change:

```java
s1.marks = 80;
s1.marks = 90;
```

The state changes from:

```text
marks = 80
```

to:

```text
marks = 90
```

The object is still the same object.

Therefore:

> [!important]
> **State can change while object identity remains the same.**

---

### 4.6 Identity Is Different From Class

Consider:

```java
class Student {
}
```

`Student` is the class.

Now:

```java
Student s1 = new Student();
Student s2 = new Student();
```

There is:

```text
1 class
2 objects
2 object identities
```

A class defines the type.

An object has its own identity.

---

### 4.7 Identity Is Different From Reference Variable

Consider:

```java
Student s1 = new Student();
```

Here:

```text
Student → Type/Class
s1      → Reference variable
new Student() → Object
```

The reference variable provides a way to access the object.

The reference itself is not the object's identity.

---

## 5. Basic Examples

### Example 1 — Identify Different Objects

**Question**

Consider:

```java
class Car {
    String color;
}

Car c1 = new Car();
Car c2 = new Car();
```

Are `c1` and `c2` the same object?

**Pattern**

Look at the number of object-creation expressions.

**Calculation**

```text
new Car() → Object 1
new Car() → Object 2
```

Therefore:

$$
\boxed{\text{c1 and c2 are different objects}}
$$

---

### Example 2 — Same State, Different Identity

**Question**

Consider:

```java
class Student {
    String name;
}

Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s2.name = "Arun";
```

Do the two objects have the same identity?

**Pattern**

Same values do not imply the same object.

**Calculation**

```text
s1 → Object 1
s2 → Object 2
```

Although:

```text
s1.name = Arun
s2.name = Arun
```

they were created separately.

**Therefore:**

$$
\boxed{\text{Different identities}}
$$

---

### Example 3 — Two References, One Object

**Question**

Consider:

```java
Student s1 = new Student();
Student s2 = s1;
```

How many objects exist?

**Pattern**

Only one `new Student()` expression appears.

**Calculation**

```text
new Student() → 1 object

s2 = s1 → no new object
```

Therefore:

$$
\boxed{1\text{ object}}
$$

There are two references:

```text
s1
s2
```

but both refer to the same object.

---

### Example 4 — Count Objects and References

**Question**

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = s1;
```

How many objects and references exist?

**Pattern**

Count `new` expressions for objects.

**Calculation**

```text
new Student() → Object 1
new Student() → Object 2
```

So:

```text
Objects = 2
```

References:

```text
s1
s2
s3
```

So:

```text
References = 3
```

` s3 ` refers to the same object as `s1`.

**Therefore:**

$$
\boxed{2\text{ objects and }3\text{ references}}
$$

---

## 6. Advanced Examples

### Example 5 — State Changes, Identity Remains

**Question**

Consider:

```java
class Account {
    int balance;
}

Account a = new Account();

a.balance = 1000;
a.balance = 2000;
```

Did the identity of `a` change?

**Pattern**

Only the field value changed.

**Calculation**

State:

```text
Before → balance = 1000
After  → balance = 2000
```

The same object is being modified.

No new object was created.

**Therefore:**

$$
\boxed{\text{Identity remains the same}}
$$

---

### Example 6 — Assignment vs Object Creation

**Question**

Consider:

```java
Student s1 = new Student();
Student s2 = s1;
Student s3 = s1;
```

How many distinct objects exist?

**Pattern**

Only the first line uses `new`.

**Calculation**

```text
new Student() → Object 1

s2 = s1 → same object
s3 = s1 → same object
```

Therefore:

```text
s1 ─┐
s2 ─┼──→ Object 1
s3 ─┘
```

**Answer:**

$$
\boxed{1\text{ distinct object}}
$$

---

### Example 7 — Three Objects With Identical State

**Question**

Consider:

```java
class Employee {
    String name;
    int salary;
}

Employee e1 = new Employee();
Employee e2 = new Employee();
Employee e3 = new Employee();

e1.name = "Ravi";
e2.name = "Ravi";
e3.name = "Ravi";

e1.salary = 50000;
e2.salary = 50000;
e3.salary = 50000;
```

How many distinct object identities exist?

**Pattern**

Count separate object creations.

**Calculation**

```text
new Employee() → Object 1
new Employee() → Object 2
new Employee() → Object 3
```

All have:

```text
name = Ravi
salary = 50000
```

But they are separately created.

Therefore:

$$
\boxed{3\text{ distinct object identities}}
$$

---

### Example 8 — Reference Comparison

**Question**

Consider:

```java
Student s1 = new Student();
Student s2 = s1;
Student s3 = new Student();
```

Which references point to the same object?

**Pattern**

Track assignments.

**Calculation**

```text
s1 → Object 1
s2 = s1 → Object 1
s3 → Object 2
```

Therefore:

```text
s1 ─┐
s2 ─┘ → Object 1

s3 → Object 2
```

**Answer:**

$$
\boxed{s1\text{ and }s2\text{ refer to the same object}}
$$

---

### Example 9 — Java Identity Comparison

**Question**

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = s1;
```

What are the results of:

```java
s1 == s2
s1 == s3
```

**Pattern**

For object references, `==` checks whether the references refer to the same object.

**Calculation**

```text
s1 → Object 1
s2 → Object 2
s3 → Object 1
```

Therefore:

```text
s1 == s2 → false
s1 == s3 → true
```

**Answer:**

$$
\boxed{s1 == s2 \rightarrow false}
$$

$$
\boxed{s1 == s3 \rightarrow true}
$$

> [!important]
> This is a Java-specific identity/reference comparison. It should not be confused with checking whether two objects merely contain equal data.

---

## 7. Shortcuts

> [!tip]
> **Shortcut 1: Count `new`**
>
> In basic Java questions, count object-creation expressions:
>
> ```java
> new ClassName()
> ```
>
> Each executed `new` creates a separate object.

> [!tip]
> **Shortcut 2: Assignment Is Not Creation**
>
> Remember:
>
> ```java
> s2 = s1;
> ```
>
> does not create a new object.
>
> It makes `s2` refer to the object already referenced by `s1`.

> [!tip]
> **Shortcut 3: Same Values ≠ Same Identity**
>
> Two objects may contain identical data and still be different objects.
>
> Always check how they were created.

> [!tip]
> **Shortcut 4: Reference Diagram**
>
> When confused, draw arrows:
>
> ```text
> s1 ─┐
> s2 ─┴──→ Object 1
> ```
>
> If two references point to the same box, they refer to the same object.

> [!tip]
> **Shortcut 5: State Can Change**
>
> If field values change but no new object is created:
>
> **Same identity, new state.**

> [!tip]
> **Shortcut 6: Fast OOP Memory**
>
> ```text
> State    → What it has
> Behavior → What it does
> Identity → Which object it is
> ```

---

## 8. Recognition Tricks

### Pattern 1 — "Unique Object"

> [!important]
> If the question says:
>
> **"What distinguishes one object from another?"**
>
> Think:
>
> **Identity**

---

### Pattern 2 — "Same Values"

> [!important]
> If two objects have the same values but were separately created:
>
> Think:
>
> **Same state, different identity**

---

### Pattern 3 — "Same Reference"

> [!important]
> If you see:

```java
Student s2 = s1;
```

Think:

**Both references point to the same object.**

---

### Pattern 4 — "New Object"

> [!important]
> If you see:

```java
new Student()
```

Think:

**A new object with a distinct identity is being created.**

---

### Pattern 5 — "Identity Comparison"

> [!important]
> In Java, if the question uses:

```java
s1 == s2
```

for object references, think:

**Do both references point to the same object?**

---

### Pattern 6 — State vs Identity

> [!important]
> If values change:

```text
State changes
Identity remains the same
```

unless a different object is being referenced.

---

## 9. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Identify Object Identity

Determine whether two references refer to the same object.

### Pattern 2 — Same State vs Same Identity

Understand that equal field values do not necessarily mean the same object.

### Pattern 3 — Count Distinct Objects

Count actual object-creation operations.

### Pattern 4 — Reference Assignment

Understand statements such as:

```java
s2 = s1;
```

### Pattern 5 — Multiple References

Determine how many references point to the same object.

### Pattern 6 — State Change Without Identity Change

Track field updates without assuming a new object is created.

### Pattern 7 — Object Comparison

Understand reference comparison using `==` in Java.

### Pattern 8 — Class vs Object Identity

Differentiate the class definition from the identities of its instances.

### Pattern 9 — Reference Diagram

Trace object relationships using references.

### Pattern 10 — Aliasing

Recognize when multiple reference variables point to the same object.

---

## 10. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Same Data Means Same Object

Wrong:

```text
Same values → Same object
```

Correct:

```text
Same values → Objects may still be different
```

---

### Mistake 2 — Counting References as Objects

Consider:

```java
Student s1 = new Student();
Student s2 = s1;
Student s3 = s1;
```

There are:

```text
3 references
1 object
```

Do not count `s2` and `s3` as new objects.

---

### Mistake 3 — Assuming Assignment Creates an Object

This:

```java
s2 = s1;
```

does not create an object.

This does:

```java
s2 = new Student();
```

---

### Mistake 4 — Thinking State Change Creates a New Object

Consider:

```java
s1.marks = 80;
s1.marks = 90;
```

Only the state changes.

The object identity remains the same.

---

### Mistake 5 — Confusing `==` With Content Equality

For Java object references:

```java
s1 == s2
```

checks whether the references refer to the same object.

It does not generally mean that the objects contain the same data.

---

### Mistake 6 — Forgetting Aliasing

Consider:

```java
Student s1 = new Student();
Student s2 = s1;
```

Changing the object through `s1` can be observed through `s2` because both references refer to the same object.

---

## 11. Formula Sheet

```text
Identity = Uniqueness of an Object

Object = State + Behavior + Identity

State → What the object currently has

Behavior → What the object can do

Identity → Which particular object it is

new ClassName()
→ Creates a new object

s2 = s1
→ No new object
→ Both references point to the same object

Same State ≠ Same Identity

Two separate new operations
→ Two distinct objects

Java object reference:
s1 == s2
→ true if both references point to the same object
```

---

## 12. Quick Revision

> [!summary] One-Minute Revision

- **Identity** distinguishes one object from another.
- An object has:
  - State
  - Behavior
  - Identity
- State can change while identity remains unchanged.
- Two separately created objects can have identical state but different identities.
- `new` creates a new object.
- Assignment such as `s2 = s1` does not create a new object.
- Multiple references can point to one object.
- One object can therefore have multiple references.
- In Java, `==` on object references checks whether they refer to the same object.
- Remember:
  - **State → What it has**
  - **Behavior → What it does**
  - **Identity → Which object it is**

### Golden Memory Trick

**Identity tells you which particular object it is, even when another object looks exactly the same.**

### One-Line Recognition

**If the question asks whether two references point to the same object, think Identity.**