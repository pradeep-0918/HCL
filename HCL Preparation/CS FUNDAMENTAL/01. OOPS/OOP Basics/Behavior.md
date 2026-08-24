---
type: concept
subject: aptitude
topic: "Behavior"
parent: "OOP Basics"
company: HCL
difficulty: easy
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - behavior
  - object-oriented-programming
  - quantitative-aptitude
wikilinks:
  - "[[OOP Basics]]"
  - "[[Class]]"
  - "[[Object]]"
  - "[[State]]"
  - "[[Identity]]"
---

# Behavior

## 1. Core Concept

> [!summary]
> **Behavior** describes the actions or operations that an object can perform. In OOP, behavior is mainly represented by methods.

An object has:

- **State** → what it has
- **Behavior** → what it does
- **Identity** → which object it is

Example:

~~~java
class Car {
    int speed;

    void accelerate() {
        speed += 10;
    }

    void brake() {
        speed -= 10;
    }
}
~~~

Here:

- `speed` → state
- `accelerate()` → behavior
- `brake()` → behavior

### Intuition

Think about a `BankAccount`.

It has data:

```text
balance
accountNumber
holderName
```

These represent its state.

It can perform actions:

```text
deposit()
withdraw()
checkBalance()
```

These represent its behavior.

> [!important]
> **State = What an object has**
>
> **Behavior = What an object does**

---

## 2. Basic Meaning

Behavior is the set of actions or operations that an object can perform.

In Java, behavior is commonly implemented using **methods**.

Example:

~~~java
class Student {

    void study() {
        System.out.println("Student is studying");
    }

    void attendClass() {
        System.out.println("Student is attending class");
    }
}
~~~

Here:

```text
study()       → Behavior
attendClass() → Behavior
```

An object can invoke these methods:

~~~java
Student s1 = new Student();

s1.study();
s1.attendClass();
~~~

### State vs Behavior

| Concept | Meaning | Example |
|---|---|---|
| State | Current data/values | `marks = 90` |
| Behavior | Actions/operations | `study()` |
| Identity | Distinguishes an object | `s1` |

---

## 3. Main Formula

There is no mathematical formula for behavior.

For OOP questions, remember:

$$
\text{Behavior} = \text{Actions an Object Can Perform}
$$

In Java:

$$
\text{Behavior} \approx \text{Methods}
$$

Example:

~~~java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }
}
~~~

Here:

```text
add() → behavior
```

The object can perform the `add()` operation.

---

## 4. Important Properties

### 4.1 Behavior Is Represented by Methods

Consider:

~~~java
class Car {

    void start() {
        System.out.println("Car started");
    }

    void stop() {
        System.out.println("Car stopped");
    }
}
~~~

The methods represent actions.

```text
start() → Behavior
stop()  → Behavior
```

---

### 4.2 Behavior Can Change Object State

Consider:

~~~java
class Counter {
    int count;

    void increment() {
        count++;
    }
}
~~~

Create an object:

~~~java
Counter c = new Counter();

c.count = 5;
c.increment();
~~~

Before:

```text
count = 5
```

After calling `increment()`:

```text
count = 6
```

Therefore:

$$
\boxed{\text{Behavior can change State}}
$$

---

### 4.3 Behavior Can Return a Result

A method may perform an operation and return a value.

~~~java
class Calculator {

    int multiply(int a, int b) {
        return a * b;
    }
}
~~~

Calling:

~~~java
Calculator c = new Calculator();

int result = c.multiply(5, 4);
~~~

Calculation:

$$
5 \times 4 = 20
$$

Therefore:

$$
\boxed{result=20}
$$

The operation `multiply()` represents behavior.

---

### 4.4 Behavior Can Accept Input

Methods can receive parameters.

~~~java
class BankAccount {

    void deposit(double amount) {
        System.out.println("Deposited: " + amount);
    }
}
~~~

Calling:

~~~java
BankAccount account = new BankAccount();

account.deposit(5000);
~~~

Here:

```text
deposit() → behavior
5000      → input to behavior
```

---

### 4.5 Behavior Can Depend on Object State

Consider:

~~~java
class Car {
    int speed;

    void displaySpeed() {
        System.out.println(speed);
    }
}
~~~

If:

~~~java
Car c = new Car();

c.speed = 80;
c.displaySpeed();
~~~

The behavior `displaySpeed()` uses the object's current state.

Therefore:

```text
State    → speed = 80
Behavior → displaySpeed()
```

---

### 4.6 Different Objects Can Perform the Same Behavior

Suppose:

~~~java
class Student {

    void study() {
        System.out.println("Studying");
    }
}
~~~

Create two objects:

~~~java
Student s1 = new Student();
Student s2 = new Student();

s1.study();
s2.study();
~~~

Both objects can perform the same behavior because both belong to the same class.

---

### 4.7 Behavior Can Be Different Depending on the Object

In object-oriented programming, the same method call can produce different behavior depending on the actual object involved. This becomes especially important with **polymorphism** and method overriding.

Example:

~~~java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

Here, `sound()` represents behavior.

The exact behavior can depend on the object.

---

## 5. Basic Examples

### Example 1 — Identify Behavior

**Question**

Consider:

~~~java
class Car {
    String color;

    void drive() {
        System.out.println("Car is moving");
    }
}
~~~

Which represents behavior?

**Pattern**

Methods represent actions.

**Calculation**

```text
color → State
drive() → Behavior
```

**Therefore:**

$$
\boxed{\text{drive()}}
$$

---

### Example 2 — State or Behavior?

**Question**

Which represents behavior?

```text
A. speed = 80
B. color = "Red"
C. start()
D. fuel = 50
```

**Pattern**

Look for the action/method.

**Calculation**

```text
speed = 80      → State
color = "Red"   → State
start()         → Behavior
fuel = 50       → State
```

**Therefore:**

$$
\boxed{\text{C. start()}}
$$

---

### Example 3 — Identify Multiple Behaviors

**Question**

Consider:

~~~java
class BankAccount {

    void deposit(int amount) {
    }

    void withdraw(int amount) {
    }

    void displayBalance() {
    }
}
~~~

Identify the behaviors.

**Calculation**

All three are methods:

```text
deposit()
withdraw()
displayBalance()
```

**Therefore:**

$$
\boxed{\text{deposit(), withdraw(), displayBalance()}}
$$

---

### Example 4 — Behavior Changes State

**Question**

Consider:

~~~java
class Counter {
    int count;

    void increment() {
        count++;
    }
}
~~~

If:

~~~java
Counter c = new Counter();

c.count = 10;
c.increment();
~~~

What is the final state?

**Pattern**

The method changes the object's state.

**Calculation**

Initial:

```text
count = 10
```

After `increment()`:

```text
count = 11
```

**Therefore:**

$$
\boxed{count=11}
$$

---

## 6. Advanced Examples

### Example 5 — Method Uses Object State

**Question**

Consider:

~~~java
class Employee {
    int salary;

    void increaseSalary(int amount) {
        salary += amount;
    }
}
~~~

If:

~~~java
Employee e = new Employee();

e.salary = 40000;
e.increaseSalary(5000);
~~~

Find the final salary.

**Pattern**

The method modifies the object's state.

**Formula**

$$
\text{New Salary} = \text{Old Salary} + \text{Increase}
$$

**Calculation**

$$
40000 + 5000 = 45000
$$

**Therefore:**

$$
\boxed{45000}
$$

---

### Example 6 — Behavior With Return Value

**Question**

Consider:

~~~java
class Calculator {

    int square(int n) {
        return n * n;
    }
}
~~~

What is returned by:

~~~java
Calculator c = new Calculator();

int result = c.square(8);
~~~

**Pattern**

` square()` performs an operation and returns a value.

**Formula**

$$
n^2
$$

**Calculation**

$$
8^2 = 64
$$

**Therefore:**

$$
\boxed{64}
$$

---

### Example 7 — Multiple Behaviors

**Question**

Consider:

~~~java
class Door {

    void open() {
        System.out.println("Door opened");
    }

    void close() {
        System.out.println("Door closed");
    }

    void lock() {
        System.out.println("Door locked");
    }
}
~~~

How many behaviors are defined?

**Pattern**

Count the methods.

**Calculation**

```text
open()  → 1
close() → 2
lock()  → 3
```

**Therefore:**

$$
\boxed{3\text{ behaviors}}
$$

---

### Example 8 — Behavior and State Together

**Question**

Consider:

~~~java
class BankAccount {
    double balance;

    void deposit(double amount) {
        balance += amount;
    }

    void withdraw(double amount) {
        balance -= amount;
    }
}
~~~

If:

~~~java
BankAccount account = new BankAccount();

account.balance = 10000;

account.deposit(2000);
account.withdraw(3000);
~~~

Find the final state.

**Pattern**

Both behaviors modify the `balance` state.

**Calculation**

Initial:

$$
10000
$$

After deposit:

$$
10000+2000=12000
$$

After withdrawal:

$$
12000-3000=9000
$$

**Therefore:**

$$
\boxed{balance=9000}
$$

---

### Example 9 — Same Behavior, Different Implementation

**Question**

Consider:

~~~java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bark");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Meow");
    }
}
~~~

What concept is demonstrated when different objects provide different implementations of `sound()`?

**Pattern**

Same method name with different runtime behavior indicates polymorphism.

**Calculation**

```text
Dog.sound() → Bark
Cat.sound() → Meow
```

**Therefore:**

$$
\boxed{\text{Runtime Polymorphism / Method Overriding}}
$$

---

## 7. Shortcuts

> [!tip]
> **Shortcut 1: Action Test**
>
> If it describes something an object **does**, think:
>
> **Behavior**

> [!tip]
> **Shortcut 2: Parentheses Test**
>
> In basic Java questions, names followed by `()` are usually methods.
>
> Methods commonly represent behavior.
>
> Example:
>
> ```text
> drive()
> start()
> stop()
> deposit()
> ```
>
> → Behavior

> [!tip]
> **Shortcut 3: State Change**
>
> If a method changes an object's field value:
>
> **Behavior → changes State**

> [!tip]
> **Shortcut 4: Return Value**
>
> If a method performs a calculation and returns a result, it still represents behavior.
>
> Example:
>
> ```java
> calculate()
> ```
>
> → Behavior

> [!tip]
> **Shortcut 5: Fast OOP Memory**
>
> ```text
> State    → What it has
> Behavior → What it does
> Identity → Which one it is
> ```

---

## 8. Recognition Tricks

### Pattern 1 — "What Can It Do?"

> [!important]
> If the question says:
>
> **"What can the object do?"**
>
> Think:
>
> **Behavior**

---

### Pattern 2 — "Action"

> [!important]
> If the question describes an **action or operation**, think:
>
> **Behavior / Method**

Examples:

```text
start()
stop()
drive()
withdraw()
deposit()
```

---

### Pattern 3 — "Method"

> [!important]
> If the question asks:
>
> **"Which members represent the actions of an object?"**
>
> Think:
>
> **Methods → Behavior**

---

### Pattern 4 — "Changes Data"

> [!important]
> If a method modifies a field:
>
> ```java
> balance += amount;
> ```
>
> Think:
>
> **Behavior changes State**

---

### Pattern 5 — "Different Implementations"

> [!important]
> If the same method produces different behavior for different object types, think:
>
> **Polymorphism / Method Overriding**

---

### Pattern 6 — State vs Behavior

> [!important]
> Use this two-second test:
>
> **"What does it have?" → State**
>
> **"What does it do?" → Behavior**

---

## 9. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Identify Behavior

Find which member represents an object's action.

### Pattern 2 — State vs Behavior

Differentiate variables from methods.

### Pattern 3 — Method as Behavior

Recognize methods as the primary representation of behavior in Java.

### Pattern 4 — Behavior Changes State

Trace methods that modify instance variables.

### Pattern 5 — Method Return Value

Determine the result produced by a behavioral method.

### Pattern 6 — Multiple Behaviors

Count or identify multiple methods in a class.

### Pattern 7 — Behavior Using State

Understand methods that read the current state.

### Pattern 8 — Polymorphic Behavior

Recognize different implementations of the same method.

### Pattern 9 — Method Overriding

Identify when a subclass changes inherited behavior.

### Pattern 10 — Object Interaction

Recognize behavior when one object invokes another object's method.

---

## 10. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing State With Behavior

Wrong:

```text
speed = 80 → Behavior
```

Correct:

```text
speed = 80 → State
drive() → Behavior
```

---

### Mistake 2 — Assuming Every Variable Is Behavior

A variable stores data.

A method performs an operation.

```text
balance → State
deposit() → Behavior
```

---

### Mistake 3 — Thinking Behavior Cannot Change State

A method can modify the object's data.

Example:

~~~java
void increase() {
    count++;
}
~~~

Calling `increase()` changes `count`.

Therefore:

```text
Behavior → State change
```

---

### Mistake 4 — Confusing Method Name With Its Return Value

Consider:

~~~java
int add(int a, int b) {
    return a + b;
}
~~~

`add()` is behavior.

The returned number is the result of that behavior.

---

### Mistake 5 — Assuming Same Method Means Same Implementation

Inheritance and polymorphism can allow different classes to implement the same method differently.

Example:

```text
Dog.sound() → Bark
Cat.sound() → Meow
```

Same method concept, different runtime behavior.

---

### Mistake 6 — Confusing Method Overloading With Overriding

**Overloading:**

Same method name, different parameter list.

**Overriding:**

Subclass provides a new implementation of an inherited method.

These are important when studying polymorphic behavior.

---

## 11. Formula Sheet

```text
Behavior = Actions an Object Can Perform

Behavior ≈ Methods

State → What an object has

Behavior → What an object does

Behavior can read State

Behavior can change State

Method:
returnType methodName(parameters)

Same Method + Different Runtime Implementation
→ Polymorphic Behavior

Overloading
→ Same method name + different parameter list

Overriding
→ Subclass provides a different implementation
```

---

## 12. Quick Revision

> [!summary] One-Minute Revision

- **Behavior** means what an object can do.
- In Java, behavior is mainly represented by methods.
- `drive()` → behavior.
- `deposit()` → behavior.
- `balance = 5000` → state.
- A method can read an object's state.
- A method can change an object's state.
- A method can accept parameters.
- A method can return a value.
- Different classes can implement the same method differently.
- Method overriding can produce different runtime behavior.
- Remember:
  - **State → What it has**
  - **Behavior → What it does**
  - **Identity → Which object it is**

### Golden Memory Trick

**Behavior is the action an object performs; methods are the main way objects perform those actions.**

### One-Line Recognition

**If the question asks "what can the object do?" or shows an action/method, think Behavior.**