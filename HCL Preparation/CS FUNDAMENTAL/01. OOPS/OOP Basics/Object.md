---
type: concept
subject: aptitude
topic: "Object"
parent: "OOP Basics"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - object
  - object-oriented-programming
  - quantitative-aptitude
wikilinks:
  - "[[OOP Basics]]"
  - "[[Class]]"
  - "[[Encapsulation]]"
  - "[[Inheritance]]"
---

# Object

## 1. Core Concept

> [!summary]
> An **object** is an instance of a class. It is a real runtime entity that has its own state, behavior, and identity.

A class defines the blueprint.

An object is created from that blueprint.

### Intuition

Think about a `Car` class.

```java
class Car {
    String color;
    int speed;

    void drive() {
        System.out.println("Car is moving");
    }
}
```

The class describes what every car can have and do.

Now create objects:

```java
Car c1 = new Car();
Car c2 = new Car();
```

Here:

- `Car` → class
- `c1` → reference variable referring to an object
- `c2` → reference variable referring to another object
- `new Car()` → creates an object

The two objects can have different states:

```java
c1.color = "Red";
c2.color = "Blue";
```

Therefore:

```text
c1 → Red
c2 → Blue
```

Both objects belong to the same class but maintain their own instance state.

---

## 2. Basic Meaning

An **object** is a concrete instance of a class.

An object generally has three important characteristics:

1. **State**
2. **Behavior**
3. **Identity**

### State

State represents the current values of an object's data.

Example:

```java
Car c1 = new Car();

c1.color = "Red";
c1.speed = 80;
```

Here:

```text
color = Red
speed = 80
```

These values represent the object's state.

---

### Behavior

Behavior represents what an object can do.

For example:

```java
c1.drive();
```

The method `drive()` represents the behavior of the object.

---

### Identity

Identity distinguishes one object from another.

For example:

```java
Car c1 = new Car();
Car c2 = new Car();
```

Even if both objects contain exactly the same data, they are still separate objects.

```text
c1 → Object 1
c2 → Object 2
```

> [!important]
> **Object = State + Behavior + Identity**

---

## 3. Main Formula

There is no mathematical formula for an object.

For technical aptitude questions, remember these relationships:

$$
\text{Object} = \text{Instance of a Class}
$$

$$
\text{Object} = \text{State} + \text{Behavior} + \text{Identity}
$$

Basic Java object creation syntax:

```java
ClassName objectName = new ClassName();
```

Example:

```java
Student s1 = new Student();
```

Here:

| Part | Meaning |
|---|---|
| `Student` | Class |
| `s1` | Reference variable |
| `new` | Creates a new object |
| `Student()` | Constructor invocation |

---

## 4. Important Properties

### 4.1 Object Is an Instance of a Class

If:

```java
class Student {
}
```

Then:

```java
Student s1 = new Student();
```

creates an object of `Student`.

Therefore:

$$
\boxed{\text{Student} \rightarrow \text{Class}}
$$

$$
\boxed{\text{s1} \rightarrow \text{Reference to Student Object}}
$$

---

### 4.2 Objects Have State

Consider:

```java
class Student {
    String name;
    int age;
}
```

Create an object:

```java
Student s1 = new Student();

s1.name = "Arun";
s1.age = 21;
```

The object's state is:

```text
name = Arun
age = 21
```

---

### 4.3 Objects Have Behavior

Consider:

```java
class Student {

    void study() {
        System.out.println("Studying");
    }
}
```

Then:

```java
Student s1 = new Student();

s1.study();
```

The method `study()` represents the behavior of the object.

---

### 4.4 Objects Have Identity

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
```

Even if:

```java
s1.name = "Arun";
s2.name = "Arun";
```

they are still two different objects.

Same data does not necessarily mean same object.

---

### 4.5 Multiple Objects Can Belong to One Class

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
```

Here:

```text
Class = Student
Objects = s1, s2, s3
```

One class can have many objects.

---

### 4.6 Each Object Can Have Different State

```java
Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s2.name = "Bala";

s1.age = 20;
s2.age = 22;
```

The objects have different states.

| Object | Name | Age |
|---|---|---:|
| `s1` | Arun | 20 |
| `s2` | Bala | 22 |

---

### 4.7 Object Uses Class-Defined Methods

A class defines methods, and objects can invoke those methods.

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }
}
```

Create an object:

```java
Calculator c = new Calculator();

int result = c.add(10, 20);
```

The object `c` uses the method `add()`.

Therefore:

$$
10 + 20 = 30
$$

---

### 4.8 Objects Are Created at Runtime

In Java:

```java
Student s1 = new Student();
```

The `new` operator creates a new object during program execution.

> [!important]
> **`new` is commonly associated with object creation in Java.**

---

## 5. Basic Examples

### Example 1 — Identify the Object

**Question**

Consider:

```java
class Car {
    String color;
}

Car c1 = new Car();
```

What is the object?

**Pattern**

Look for object creation using `new`.

**Calculation**

```java
new Car()
```

creates an object of the `Car` class.

`c1` is the reference variable referring to that object.

**Therefore:**

$$
\boxed{\text{c1 refers to a Car object}}
$$

---

### Example 2 — Number of Objects

**Question**

How many objects are created?

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
Student s4 = new Student();
```

**Pattern**

Count the `new Student()` operations.

**Calculation**

```text
new Student() → 1
new Student() → 2
new Student() → 3
new Student() → 4
```

**Therefore:**

$$
\boxed{4\text{ objects}}
$$

---

### Example 3 — Identify Object State

**Question**

```java
class Employee {
    String name;
    int salary;
}

Employee e1 = new Employee();

e1.name = "Ravi";
e1.salary = 50000;
```

What is the state of `e1`?

**Pattern**

State = current values of the object's data.

**Calculation**

```text
name = Ravi
salary = 50000
```

**Therefore:**

$$
\boxed{\text{State = name: Ravi, salary: 50000}}
$$

---

### Example 4 — Identify Behavior

**Question**

```java
class Car {

    void start() {
        System.out.println("Car started");
    }
}
```

What represents the behavior?

**Pattern**

Methods represent behavior.

**Calculation**

```text
start() → method → behavior
```

**Therefore:**

$$
\boxed{\text{start()}}
$$

---

## 6. Advanced Examples

### Example 5 — Two Objects With Different States

**Question**

```java
class Student {
    String name;
    int marks;
}

Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s1.marks = 85;

s2.name = "Bala";
s2.marks = 92;
```

What are the states of `s1` and `s2`?

**Pattern**

Each object has its own instance variables.

**Calculation**

For `s1`:

```text
name = Arun
marks = 85
```

For `s2`:

```text
name = Bala
marks = 92
```

**Therefore:**

$$
\boxed{s1 = (Arun,85)}
$$

$$
\boxed{s2 = (Bala,92)}
$$

---

### Example 6 — Same Class, Different Objects

**Question**

Consider:

```java
class Car {
    String color;
}

Car c1 = new Car();
Car c2 = new Car();

c1.color = "Red";
c2.color = "Blue";
```

Are `c1` and `c2` the same object?

**Pattern**

Two separate `new` operations create two separate objects.

**Calculation**

```text
new Car() → Object 1
new Car() → Object 2
```

Therefore:

```text
c1 → Object 1
c2 → Object 2
```

**Answer:**

$$
\boxed{\text{No, they are different objects}}
$$

---

### Example 7 — Same Data Does Not Mean Same Object

**Question**

```java
class Student {
    String name;
}

Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s2.name = "Arun";
```

Are `s1` and `s2` the same object?

**Pattern**

Check how many times `new` is used.

**Calculation**

```text
new Student() → Object 1
new Student() → Object 2
```

Even though:

```text
s1.name = Arun
s2.name = Arun
```

the objects are separately created.

**Therefore:**

$$
\boxed{\text{s1 and s2 are different objects}}
$$

---

### Example 8 — Reference Variable vs Object

**Question**

Consider:

```java
Student s1 = new Student();
```

Identify:

1. Class
2. Reference variable
3. Object

**Pattern**

Break the statement into parts.

**Calculation**

```text
Student → class/type
s1 → reference variable
new Student() → object creation
```

**Therefore:**

$$
\boxed{\text{Class = Student}}
$$

$$
\boxed{\text{Reference = s1}}
$$

$$
\boxed{\text{Object = instance created by new Student()}}
$$

---

## 7. Shortcuts

> [!tip]
> **Shortcut 1: Instance Test**
>
> If the question says **"instance of a class"**, immediately think:
>
> **Object**

> [!tip]
> **Shortcut 2: Find Object Creation**
>
> In Java, search for:
>
> ```java
> new ClassName()
> ```
>
> This indicates creation of a new object.

> [!tip]
> **Shortcut 3: State Test**
>
> If the question asks **"current values of an object's variables"**, think:
>
> **State**

> [!tip]
> **Shortcut 4: Behavior Test**
>
> If the question asks **"what an object can do"**, think:
>
> **Methods / Behavior**

> [!tip]
> **Shortcut 5: Identity Test**
>
> If two objects are created using two separate `new` operations, treat them as separate objects unless the code explicitly makes references point to the same object.

> [!tip]
> **Shortcut 6: Count Objects**
>
> In simple Java questions:
>
> ```text
> Number of new operations → Number of objects created
> ```
>
> This shortcut is useful when each `new` expression is actually executed and no object creation occurs indirectly through another mechanism.

---

## 8. Recognition Tricks

### Pattern 1 — "Instance"

> [!important]
> If the question says:
>
> **"Which is an instance of a class?"**
>
> Think:
>
> **Object**

---

### Pattern 2 — "Current Values"

> [!important]
> If the question says:
>
> **"What are the current values of the object's variables?"**
>
> Think:
>
> **State**

---

### Pattern 3 — "What Object Can Do"

> [!important]
> If the question says:
>
> **"What actions can an object perform?"**
>
> Think:
>
> **Behavior / Methods**

---

### Pattern 4 — "Different Objects"

> [!important]
> If you see:

```java
A a1 = new A();
A a2 = new A();
```

Think:

**Two separate object instances.**

---

### Pattern 5 — "Same Object"

> [!important]
> If two reference variables point to the same object:

```java
Student s1 = new Student();
Student s2 = s1;
```

Think:

**Two references, one object.**

This is different from:

```java
Student s1 = new Student();
Student s2 = new Student();
```

which creates:

**Two references, two objects.**

---

### Pattern 6 — Object vs Reference

> [!important]
> If the question asks whether `s1` itself is the object or the reference to the object, remember:
>
> In:
>
> ```java
> Student s1 = new Student();
> ```
>
> `s1` is a **reference variable** and `new Student()` creates the object.

---

## 9. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Identify an Object

Determine which part of a program represents an object.

### Pattern 2 — Class vs Object

Differentiate between a blueprint and an actual instance.

### Pattern 3 — Object Creation

Identify statements that create objects.

### Pattern 4 — Count Objects

Determine how many objects are created.

### Pattern 5 — State

Identify the current data stored in an object.

### Pattern 6 — Behavior

Identify methods that represent object behavior.

### Pattern 7 — Identity

Understand why separately created objects are different.

### Pattern 8 — Reference Variables

Distinguish a reference variable from the actual object.

### Pattern 9 — Shared Reference

Determine when two references point to the same object.

### Pattern 10 — Object Lifetime

Understand that an object exists as a runtime entity after it is created and can become eligible for garbage collection when it is no longer reachable in Java.

---

## 10. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking the Reference Variable Is the Object

Consider:

```java
Student s1 = new Student();
```

Do not simply treat `s1` as the object itself.

More precisely:

```text
s1 → reference variable
new Student() → object
```

---

### Mistake 2 — Thinking One Class Creates Only One Object

Wrong:

```text
One class = One object
```

Correct:

```text
One class → Can create many objects
```

Example:

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
```

---

### Mistake 3 — Confusing Same Data With Same Object

Consider:

```java
s1.name = "Arun";
s2.name = "Arun";
```

This does not mean `s1` and `s2` refer to the same object.

Check the object creation statements.

---

### Mistake 4 — Missing the Difference Between One Object and Two Objects

Compare:

```java
Student s1 = new Student();
Student s2 = s1;
```

with:

```java
Student s1 = new Student();
Student s2 = new Student();
```

First case:

```text
2 references → 1 object
```

Second case:

```text
2 references → 2 objects
```

---

### Mistake 5 — Confusing State With Behavior

```text
State → Data / current values
Behavior → Methods / actions
```

For example:

```text
speed = 80 → State
drive() → Behavior
```

---

### Mistake 6 — Assuming Every Declaration Creates an Object

This:

```java
Student s1;
```

only declares a reference variable.

It does not create a `Student` object.

Object creation happens here:

```java
Student s1 = new Student();
```

---

## 11. Formula Sheet

```text
Object = Instance of a Class

Object = State + Behavior + Identity

State → Current values of object's data

Behavior → Actions performed through methods

Identity → Distinguishes one object from another

Object Creation:
ClassName objectName = new ClassName();

One Class → Many Objects

new ClassName() → Creates a new object

Two separate new operations → Two separate objects

Student s2 = s1;
→ Two references can refer to one object
```

---

## 12. Quick Revision

> [!summary] One-Minute Revision

- An **object** is an instance of a class.
- A class is the blueprint; an object is the actual runtime instance.
- An object has **state, behavior, and identity**.
- State = current values of its data.
- Behavior = actions represented by methods.
- Identity = distinguishes one object from another.
- `new` is commonly used to create an object in Java.
- `Student s1;` → reference declaration only.
- `Student s1 = new Student();` → object creation.
- One class can create many objects.
- Different objects can have different states.
- Two references can point to the same object.
- Two separate `new` operations create separate objects.

### Golden Memory Trick

**Class is the blueprint; object is the real instance with its own state, behavior, and identity.**

### One-Line Recognition

**If the question says "instance", "state", "behavior", or "identity", think about the Object.**