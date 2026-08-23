---
type: concept
subject: aptitude
topic: "Class"
parent: "OOP Basics"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - class
  - object-oriented-programming
  - quantitative-aptitude
wikilinks:
  - "[[OOP Basics]]"
  - "[[Object]]"
  - "[[Encapsulation]]"
  - "[[Inheritance]]"
---

# Class

## 1. Core Concept

> [!summary]
> A **class** is a blueprint or template used to create objects. It defines the data an object can contain and the operations it can perform.

A class describes:

- What an object **has** → data / attributes
- What an object **does** → methods / behavior

Think of a class as a **design**, while an object is the actual thing created from that design.

### Intuition

Suppose we want to represent students in a program.

A student may have:

- name
- roll number
- age

A student may perform actions such as:

- `study()`
- `attendClass()`
- `writeExam()`

Instead of defining these separately for every student, we create one `Student` class.

```java
class Student {
    String name;
    int rollNo;
    int age;

    void study() {
        System.out.println("Student is studying");
    }
}
```

Objects can then be created from this class.

```java
Student s1 = new Student();
Student s2 = new Student();
```

Here:

- `Student` → class
- `s1` → object
- `s2` → object

---

## 2. Basic Meaning

A **class** is a user-defined blueprint that groups:

1. Data
2. Methods
3. Constructors
4. Other members

### Simple Example

```java
class Car {
    String color;
    int speed;

    void drive() {
        System.out.println("Car is moving");
    }
}
```

The class defines the structure of a car.

It does not represent one specific car.

When we create:

```java
Car c1 = new Car();
```

`c1` becomes an object of the `Car` class.

### Class vs Object

| Class | Object |
|---|---|
| Blueprint | Actual instance |
| Logical entity | Runtime entity |
| Defines properties | Contains actual values |
| Defines methods | Uses methods |
| Can create many objects | Represents one specific instance |
| Example: `Car` | Example: `c1` |

> [!important]
> **Class = Blueprint**
>
> **Object = Instance created from the blueprint**

---

## 3. Main Formula

Classes do not have mathematical formulas. For technical aptitude questions, remember the fundamental relationship:

$$
\text{Class} \rightarrow \text{Blueprint}
$$

$$
\text{Object} \rightarrow \text{Instance of Class}
$$

The basic creation syntax in Java is:

```java
ClassName objectName = new ClassName();
```

For example:

```java
Student s1 = new Student();
```

Here:

- `Student` → class type
- `s1` → reference variable
- `new Student()` → creates an object

---

## 4. Important Properties

### 4.1 Class Defines Structure

A class can define:

- Variables
- Methods
- Constructors
- Blocks
- Nested classes
- Interfaces

Example:

```java
class Employee {
    int id;
    String name;

    void display() {
        System.out.println(id + " " + name);
    }
}
```

---

### 4.2 Class Supports Encapsulation

A class can combine data and methods into one unit.

```java
class BankAccount {
    private double balance;

    void deposit(double amount) {
        balance += amount;
    }
}
```

Here:

- `balance` → data
- `deposit()` → behavior

The class groups them together.

---

### 4.3 Multiple Objects Can Be Created From One Class

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
```

All three objects belong to the same class.

But each object can have different data.

```java
s1.name = "Arun";
s2.name = "Bala";
s3.name = "Kiran";
```

---

### 4.4 Objects Have Their Own State

Suppose:

```java
class Student {
    String name;
    int age;
}
```

Then:

```java
Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s2.name = "Bala";
```

The two objects can contain different values.

| Object | Name |
|---|---|
| `s1` | Arun |
| `s2` | Bala |

---

### 4.5 Methods Define Behavior

A class can define what its objects can do.

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }
}
```

The method `add()` represents behavior associated with objects of the class.

---

### 4.6 Class Is a User-Defined Data Type

A class can be used to create a custom type.

```java
class Student {
    String name;
    int age;
}
```

Now `Student` can be used as a type:

```java
Student s1;
Student s2;
```

---

## 5. Basic Examples

### Example 1 — Identify the Class

**Question**

Consider:

```java
class Car {
    String color;

    void drive() {
        System.out.println("Driving");
    }
}
```

What is the class?

**Pattern**

Identify the keyword followed by the class name.

**Calculation**

```java
class Car
```

The keyword `class` defines a class.

**Therefore:**

$$
\boxed{\text{Car}}
$$

---

### Example 2 — Identify the Object

**Question**

```java
class Student {
    String name;
}

Student s1 = new Student();
```

What is the object?

**Pattern**

Look at the expression after `new`.

```java
new Student()
```

This creates an object of `Student`.

**Therefore:**

$$
\boxed{\text{s1 refers to a Student object}}
$$

---

### Example 3 — Number of Objects

**Question**

```java
class Employee {
    int id;
}

Employee e1 = new Employee();
Employee e2 = new Employee();
Employee e3 = new Employee();
```

How many objects are created?

**Pattern**

Count the number of `new ClassName()` expressions.

**Calculation**

```text
new Employee() → Object 1
new Employee() → Object 2
new Employee() → Object 3
```

**Therefore:**

$$
\boxed{3\text{ objects}}
$$

---

### Example 4 — Same Class, Different Objects

**Question**

```java
class Student {
    String name;
}

Student s1 = new Student();
Student s2 = new Student();

s1.name = "Arun";
s2.name = "Bala";
```

What is the value of `s1.name`?

**Pattern**

Each object maintains its own instance data.

**Calculation**

```text
s1.name = Arun
s2.name = Bala
```

**Therefore:**

$$
\boxed{\text{Arun}}
$$

---

## 6. Advanced Examples

### Example 5 — Class Members vs Object Data

**Question**

Consider:

```java
class Employee {
    int id;

    void display() {
        System.out.println(id);
    }
}
```

If two objects are created:

```java
Employee e1 = new Employee();
Employee e2 = new Employee();

e1.id = 10;
e2.id = 20;
```

What happens when `display()` is called on each object?

**Pattern**

`id` is an instance variable, so every object has its own value.

**Calculation**

For `e1`:

```text
id = 10
```

For `e2`:

```text
id = 20
```

Therefore:

```text
e1.display() → 10
e2.display() → 20
```

**Answer:**

$$
\boxed{e1.display() = 10,\quad e2.display() = 20}
$$

---

### Example 6 — One Class, Many Objects

**Question**

A `Car` class is used to create 50 cars. How many classes and objects are involved?

**Pattern**

One blueprint can create many objects.

**Calculation**

```text
Class = 1
Objects = 50
```

**Therefore:**

$$
\boxed{1\text{ class and }50\text{ objects}}
$$

---

### Example 7 — Identify Class Components

**Question**

Consider:

```java
class BankAccount {
    private double balance;

    void deposit(double amount) {
        balance += amount;
    }
}
```

Identify the data and behavior.

**Pattern**

Variables represent data/state.

Methods represent behavior.

**Calculation**

```text
balance → data
deposit() → behavior
```

**Therefore:**

$$
\boxed{\text{Data = balance,\quad Behavior = deposit()}}
$$

---

## 7. Shortcuts

> [!tip]
> **Shortcut 1: Find the Class**
>
> In Java, look for:
>
> ```java
> class ClassName
> ```
>
> The name after `class` is the class name.

> [!tip]
> **Shortcut 2: Find Object Creation**
>
> Look for:
>
> ```java
> new ClassName()
> ```
>
> Each execution of `new` creates an object.

> [!tip]
> **Shortcut 3: Blueprint Test**
>
> If something describes the structure or design of multiple similar entities, think **class**.

> [!tip]
> **Shortcut 4: Instance Test**
>
> If something is a concrete entity created from a class, think **object**.

> [!tip]
> **Shortcut 5: Count Objects**
>
> For basic code-output questions, count object-creation expressions:
>
> ```java
> new ClassName()
> ```

---

## 8. Recognition Tricks

### Pattern 1 — Blueprint

> [!important]
> If the question says **"blueprint", "template", or "design"**, think:
>
> **Class**

---

### Pattern 2 — Instance

> [!important]
> If the question says **"instance of a class"**, think:
>
> **Object**

---

### Pattern 3 — Object Creation

> [!important]
> If the question contains:
>
> ```java
> new ClassName()
> ```
>
> think:
>
> **Object creation**

---

### Pattern 4 — Data + Methods

> [!important]
> If the question asks about combining **data and methods into one unit**, think:
>
> **Class / Encapsulation**

---

### Pattern 5 — Different Values

> [!important]
> If multiple objects have different values for the same instance variable, think:
>
> **Each object has its own instance state.**

---

## 9. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Class Definition

Identify which part of a program defines a class.

### Pattern 2 — Object Creation

Identify which statement creates an object.

### Pattern 3 — Class vs Object

Differentiate between blueprint and instance.

### Pattern 4 — Number of Objects

Count `new` operations in simple code.

### Pattern 5 — Class Members

Identify variables and methods belonging to a class.

### Pattern 6 — Instance Variables

Determine whether different objects can have different values.

### Pattern 7 — Object State

Predict the value stored inside a particular object.

### Pattern 8 — User-Defined Type

Recognize when a class is being used as a custom data type.

---

## 10. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Treating Class and Object as the Same

Wrong:

```text
Class = Object
```

Correct:

```text
Class = Blueprint
Object = Instance
```

---

### Mistake 2 — Thinking One Class Means One Object

A single class can create many objects.

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
```

There is one class but three objects.

---

### Mistake 3 — Counting Reference Variables as Objects

Consider:

```java
Student s1;
```

No object is created here.

An object is created using:

```java
Student s1 = new Student();
```

The `new` operation is the important part for object creation.

---

### Mistake 4 — Assuming Instance Variables Are Shared

Consider:

```java
Student s1 = new Student();
Student s2 = new Student();
```

An instance variable belongs separately to each object.

They do not automatically share the same instance value.

---

### Mistake 5 — Confusing Class Definition With Object Creation

```java
class Student {
}
```

This defines a class.

```java
Student s = new Student();
```

This creates an object.

---

## 11. Formula Sheet

```text
Class = Blueprint / Template

Object = Instance of Class

Object Creation:
ClassName objectName = new ClassName();

Class → Defines structure
Object → Contains actual state

Instance Variable → Separate value for each object

One Class → Many Objects
```

---

## 12. Quick Revision

> [!summary] One-Minute Revision

- A **class** is a blueprint for creating objects.
- A **class** defines data and behavior.
- An **object** is an instance of a class.
- Multiple objects can be created from one class.
- Each object can have its own instance data.
- Variables represent data/state.
- Methods represent behavior.
- In Java, `new` is commonly used to create an object.
- `class Student { }` → class definition.
- `Student s = new Student();` → object creation.
- Class = design.
- Object = actual instance.

### Golden Memory Trick

**Class is the blueprint; object is the real thing built from it.**

### One-Line Recognition

**If you see "blueprint/template/design" → Class; if you see "instance/created entity" → Object.**