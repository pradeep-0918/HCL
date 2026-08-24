---
type: concept
subject: aptitude
topic: "State"
parent: "OOP Basics"
company: HCL
difficulty: easy
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - state
  - object-oriented-programming
  - quantitative-aptitude
wikilinks:
  - "[[OOP Basics]]"
  - "[[Class]]"
  - "[[Object]]"
  - "[[Behavior]]"
---

# State

## 1. Core Concept

> [!summary]
> **State** is the current data or values stored inside an object at a particular point in time.

An object can have different values during its lifetime.

For example:

```java
class Student {
    String name;
    int marks;
}
```

Create an object:

```java
Student s1 = new Student();

s1.name = "Arun";
s1.marks = 80;
```

The current state of `s1` is:

```text
name = Arun
marks = 80
```

If the marks change:

```java
s1.marks = 95;
```

The object's state changes:

```text
Before:
marks = 80

After:
marks = 95
```

### Intuition

Think of an object as a person.

The person's:

- Name
- Age
- Height
- Salary

represent information about the person's current state.

If the person's age changes from 20 to 21, the state changes.

> [!important]
> **State = What an object currently has.**
>
> **Behavior = What an object can do.**

---

## 2. Basic Meaning

State represents the **current condition of an object**.

In object-oriented programming, state is usually represented by the values stored in an object's **instance variables / fields**.

Example:

```java
class Car {
    String color;
    int speed;
    boolean engineOn;
}
```

Suppose:

```java
Car c1 = new Car();

c1.color = "Red";
c1.speed = 80;
c1.engineOn = true;
```

The state of `c1` is:

```text
color = Red
speed = 80
engineOn = true
```

### State vs Behavior

| Concept | Meaning | Example |
|---|---|---|
| State | Current data/values | `speed = 80` |
| Behavior | Action performed by object | `drive()` |
| Identity | Distinguishes object | `c1` |

> [!important]
> When an object's field values change, its **state changes**.

---

## 3. Main Formula

There is no mathematical formula for state.

For OOP questions, remember:

$$
\text{State} = \text{Current Values of Object's Data}
$$

For an object with multiple fields:

$$
\text{Object State} = \{v_1, v_2, v_3, \ldots, v_n\}
$$

where each $v_i$ represents the current value of a field.

Example:

```java
Student s1 = new Student();

s1.name = "Arun";
s1.age = 21;
s1.marks = 90;
```

Therefore:

$$
\text{State}(s1)=\{\text{name=Arun,\ age=21,\ marks=90}\}
$$

---

## 4. Important Properties

### 4.1 State Is Represented by Data

Consider:

```java
class Employee {
    String name;
    int salary;
}
```

The fields:

```text
name
salary
```

represent information that can form the object's state.

---

### 4.2 State Can Change

Suppose:

```java
Employee e1 = new Employee();

e1.salary = 40000;
```

Current state:

```text
salary = 40000
```

Later:

```java
e1.salary = 50000;
```

New state:

```text
salary = 50000
```

Therefore:

$$
\boxed{\text{State can change during the object's lifetime}}
$$

---

### 4.3 Different Objects Can Have Different States

```java
Student s1 = new Student();
Student s2 = new Student();

s1.marks = 80;
s2.marks = 95;
```

The objects belong to the same class but have different states.

| Object | Marks |
|---|---:|
| `s1` | 80 |
| `s2` | 95 |

---

### 4.4 Same State Does Not Necessarily Mean Same Object

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();

s1.marks = 90;
s2.marks = 90;
```

Both objects currently have:

```text
marks = 90
```

But they are still separate objects because they were created separately.

> [!important]
> **Same state ≠ same object**

---

### 4.5 Behavior Can Change State

A method can modify an object's state.

Example:

```java
class BankAccount {
    int balance;

    void deposit(int amount) {
        balance += amount;
    }
}
```

Suppose:

```java
BankAccount account = new BankAccount();

account.balance = 1000;
account.deposit(500);
```

Before `deposit()`:

```text
balance = 1000
```

After `deposit()`:

```text
balance = 1500
```

The behavior changed the object's state.

---

### 4.6 State Is Usually Object-Specific

Consider:

```java
class Student {
    String name;
    int marks;
}
```

Each object can store different values:

```java
Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s1.marks = 80;

s2.name = "Bala";
s2.marks = 90;
```

Therefore:

```text
s1 → Arun, 80
s2 → Bala, 90
```

---

### 4.7 State Can Be Viewed as a Snapshot

At any particular moment, the values stored in an object form its state.

For example:

```text
Time 1:
speed = 0
engineOn = false
```

After starting:

```text
Time 2:
speed = 0
engineOn = true
```

After moving:

```text
Time 3:
speed = 60
engineOn = true
```

The object's state changes over time.

---

## 5. Basic Examples

### Example 1 — Identify the State

**Question**

Consider:

```java
class Student {
    String name;
    int marks;
}

Student s1 = new Student();

s1.name = "Arun";
s1.marks = 85;
```

What is the state of `s1`?

**Pattern**

State means the current values of the object's fields.

**Calculation**

```text
name = Arun
marks = 85
```

**Therefore:**

$$
\boxed{\text{State of }s1=\{\text{name=Arun,\ marks=85}\}}
$$

---

### Example 2 — State Change

**Question**

```java
class Account {
    int balance;
}

Account a = new Account();

a.balance = 1000;
a.balance = 1500;
```

What is the final state of `a`?

**Pattern**

Look at the latest value assigned to the field.

**Calculation**

Initial assignment:

```text
balance = 1000
```

Later:

```text
balance = 1500
```

Therefore:

$$
\boxed{\text{balance}=1500}
$$

---

### Example 3 — Different Object States

**Question**

```java
class Car {
    String color;
}

Car c1 = new Car();
Car c2 = new Car();

c1.color = "Red";
c2.color = "Blue";
```

What are the states of the two objects?

**Pattern**

Each object has its own instance variable.

**Calculation**

```text
c1 → color = Red
c2 → color = Blue
```

**Therefore:**

$$
\boxed{c1=\text{Red},\quad c2=\text{Blue}}
$$

---

### Example 4 — State or Behavior?

**Question**

Which of the following represents state?

```text
A. speed = 80
B. drive()
C. brake()
D. start()
```

**Pattern**

State represents data/value.

**Calculation**

```text
speed = 80 → data/value
drive()    → behavior
brake()    → behavior
start()    → behavior
```

**Therefore:**

$$
\boxed{\text{A. speed = 80}}
$$

---

## 6. Advanced Examples

### Example 5 — Method Changes State

**Question**

Consider:

```java
class Counter {
    int count;

    void increment() {
        count++;
    }
}
```

Now:

```java
Counter c = new Counter();

c.count = 5;
c.increment();
c.increment();
```

What is the final state?

**Pattern**

The method `increment()` changes the value of `count`.

**Calculation**

Initial:

```text
count = 5
```

First `increment()`:

```text
count = 6
```

Second `increment()`:

```text
count = 7
```

**Therefore:**

$$
\boxed{\text{count}=7}
$$

---

### Example 6 — Multiple Fields

**Question**

Consider:

```java
class Employee {
    String name;
    int age;
    double salary;
}

Employee e = new Employee();

e.name = "Ravi";
e.age = 25;
e.salary = 45000;
```

What is the state of `e`?

**Pattern**

Combine the current values of all relevant instance fields.

**Calculation**

```text
name = Ravi
age = 25
salary = 45000
```

**Therefore:**

$$
\boxed{\text{State}=\{\text{name=Ravi,\ age=25,\ salary=45000}\}}
$$

---

### Example 7 — Same Class, Same State

**Question**

```java
class Student {
    int marks;
}

Student s1 = new Student();
Student s2 = new Student();

s1.marks = 90;
s2.marks = 90;
```

Do `s1` and `s2` represent the same object?

**Pattern**

Check object creation, not just field values.

**Calculation**

```java
new Student() → Object 1
new Student() → Object 2
```

Both currently have:

```text
marks = 90
```

But they were separately created.

**Therefore:**

$$
\boxed{\text{They are different objects with the same current state}}
$$

---

### Example 8 — State Transition

**Question**

A traffic-light object has:

```text
state = RED
```

After a method changes it:

```text
state = GREEN
```

What happened?

**Pattern**

A change in the object's data represents a state transition.

**Calculation**

```text
Before → RED
After  → GREEN
```

Therefore:

$$
\boxed{\text{The object's state changed from RED to GREEN}}
$$

---

## 7. Shortcuts

> [!tip]
> **Shortcut 1: "What Does It Have?"**
>
> If the question asks what an object **has**, think:
>
> **State**

> [!tip]
> **Shortcut 2: "What Can It Do?"**
>
> If the question asks what an object **does**, think:
>
> **Behavior**

> [!tip]
> **Shortcut 3: Look for Values**
>
> Expressions such as:
>
> ```text
> age = 21
> salary = 50000
> color = "Red"
> ```
>
> usually describe state.

> [!tip]
> **Shortcut 4: Latest Assignment**
>
> In code-output questions, track the latest value assigned to each field to determine the final state.

> [!tip]
> **Shortcut 5: Method That Changes Data**
>
> If a method modifies an instance variable, think:
>
> **Behavior changes State**

---

## 8. Recognition Tricks

### Pattern 1 — "Current Values"

> [!important]
> If the question says **"current values of an object"**, think:
>
> **State**

---

### Pattern 2 — "Condition of Object"

> [!important]
> If the question says **"current condition/condition of an object"**, think:
>
> **State**

---

### Pattern 3 — "What Object Has"

> [!important]
> If the question asks:
>
> **"What information does the object contain?"**
>
> Think:
>
> **State**

---

### Pattern 4 — "Changes Over Time"

> [!important]
> If the object's field values change over time, think:
>
> **State transition / state change**

---

### Pattern 5 — "Action Changes Value"

> [!important]
> If a method performs an action and modifies an object's data, think:
>
> **Behavior changes state**

Example:

```java
account.deposit(500);
```

The behavior `deposit()` changes the state `balance`.

---

### Pattern 6 — State vs Behavior

> [!important]
> Remember:
>
> **State → Data**
>
> **Behavior → Methods**

Example:

```text
speed = 100 → State
drive()     → Behavior
```

---

## 9. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Identify State

Find which values represent the current state of an object.

### Pattern 2 — State vs Behavior

Distinguish fields from methods.

### Pattern 3 — State Change

Track how an object's state changes after assignments.

### Pattern 4 — Method-Induced State Change

Determine how calling a method changes object data.

### Pattern 5 — Multiple Object States

Compare the states of two or more objects.

### Pattern 6 — Same State, Different Objects

Understand that two separate objects can have identical values.

### Pattern 7 — Final State

Trace code and determine the final values of an object's fields.

### Pattern 8 — State Transition

Identify the before-and-after state of an object.

### Pattern 9 — Instance State

Recognize values stored separately for each object.

### Pattern 10 — State Snapshot

Treat the object's current field values as its state at a particular moment.

---

## 10. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing State With Behavior

Wrong:

```text
State = drive()
```

Correct:

```text
State = speed = 80
Behavior = drive()
```

Methods describe actions; values describe state.

---

### Mistake 2 — Thinking State Never Changes

Wrong:

```text
Object state is fixed forever.
```

Correct:

```text
Object state can change during its lifetime.
```

Example:

```text
balance = 1000
↓
deposit()
↓
balance = 1500
```

---

### Mistake 3 — Thinking Same State Means Same Object

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();

s1.marks = 90;
s2.marks = 90;
```

Both have the same current state for `marks`, but they are different objects.

---

### Mistake 4 — Looking Only at Initial Values

Consider:

```java
a.balance = 1000;
a.balance = 2000;
```

The final state is:

```text
balance = 2000
```

Always track the latest assignment when asked for the final state.

---

### Mistake 5 — Ignoring Methods That Modify State

Consider:

```java
void increase() {
    count++;
}
```

Calling:

```java
c.increase();
```

changes the state of `c`.

Do not treat the method as unrelated to state.

---

### Mistake 6 — Confusing Class State With Object State

Instance variables normally belong separately to each object.

```java
Student s1 = new Student();
Student s2 = new Student();
```

Their instance fields can have different values.

---

## 11. Formula Sheet

```text
State = Current Values of Object's Data

State → What an object currently has

Behavior → What an object can do

State is usually represented by instance variables / fields

Object State:
{field1=value1, field2=value2, ...}

State can change during an object's lifetime

Behavior can change State

Same State ≠ Same Object

Different Objects → Can Have Different States
```

---

## 12. Quick Revision

> [!summary] One-Minute Revision

- **State** means the current condition of an object.
- State is represented by the current values of its data/fields.
- `marks = 90` is state.
- `study()` is behavior.
- State can change during an object's lifetime.
- A method can change an object's state.
- Different objects can have different states.
- Two different objects can have the same state.
- Same state does not mean same object.
- To find the final state, track the latest field values.
- Think:
  - **State → What it has**
  - **Behavior → What it does**
  - **Identity → Which object it is**

### Golden Memory Trick

**State is the object's current data snapshot — what it has right now.**

### One-Line Recognition

**If the question asks for an object's current values or condition, think State.**