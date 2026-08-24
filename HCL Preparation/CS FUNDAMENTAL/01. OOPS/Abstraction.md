---
type: concept
subject: aptitude
topic: "Abstraction"
parent: "OOP Basics"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - abstraction
  - object-oriented-programming
  - abstract-class
  - interface
wikilinks:
  - "[[OOP Basics]]"
  - "[[Class]]"
  - "[[Object]]"
  - "[[Encapsulation]]"
  - "[[Interfaces]]"
  - "[[Abstract Classes]]"
---

# Abstraction

## 1. Core Concept

> [!summary]
> **Abstraction** is the OOP concept of exposing only the essential features of an object while hiding unnecessary implementation details.

The central idea is:

$$
\boxed{\text{Show WHAT, Hide HOW}}
$$

When using an object, the user should know:

- What the object can do
- What operations are available
- How to use those operations

The user does not necessarily need to know:

- How the operation works internally
- Which algorithms are used
- Which internal data structures are used
- How the implementation is organized

### Simple Example

Consider a car.

You use:

- Steering
- Brake
- Accelerator
- Gear

You do not need to understand:

- Fuel injection
- Engine combustion
- Transmission mechanism
- Internal braking mechanism

You interact with the essential controls while the internal complexity remains hidden.

That is the basic idea of abstraction.

### Programming Example

Suppose we have:

    ~~~~java
    abstract class Vehicle {

        abstract void start();
    }
    ~~~~

The class tells us:

```text
Vehicle must have start()
```

But it does not specify how every vehicle starts.

A subclass provides the implementation:

    ~~~~java
    class Car extends Vehicle {

        @Override
        void start() {
            System.out.println("Car starts using engine");
        }
    }
    ~~~~

Here:

```text
Vehicle  → WHAT
Car      → HOW
```

---

## 2. Basic Meaning

Abstraction focuses on the **essential functionality** of an object rather than its internal implementation.

### Core Question

When you see an abstraction question, ask:

> **"What does the user need to know?"**

The answer represents the exposed abstraction.

Then ask:

> **"What does the user NOT need to know?"**

The answer represents the hidden implementation details.

### Example

An ATM provides:

- Withdraw
- Deposit
- Balance inquiry
- PIN verification

The user does not need to know:

- Database queries
- Server communication
- Transaction processing
- Encryption implementation
- Internal validation logic

Therefore:

$$
\boxed{\text{Abstraction reduces unnecessary complexity}}
$$

---

## 3. Main Formula

There is no mathematical formula for abstraction.

For technical interviews and aptitude questions, remember these conceptual formulas:

$$
\boxed{\text{Abstraction} = \text{Essential Features} + \text{Hidden Implementation}}
$$

More precisely:

$$
\boxed{\text{WHAT is exposed, HOW is hidden}}
$$

### Java Abstraction

Java commonly provides abstraction using:

1. Abstract classes
2. Interfaces

Therefore:

$$
\boxed{\text{Java Abstraction} \rightarrow \text{Abstract Class / Interface}}
$$

---

## 4. Why Abstraction Is Needed

Without abstraction, users may have to understand unnecessary internal complexity.

### Without Abstraction

Imagine a payment system requiring the programmer to directly manage:

```text
Database connection
Transaction validation
Encryption
Network communication
Payment gateway
Error handling
Logging
```

Every user would need to understand all these details.

This creates complexity.

### With Abstraction

The user can simply call:

    ~~~~java
    payment.pay(5000);
    ~~~~

The user only needs to know:

```text
pay(amount)
```

The internal implementation is hidden.

### Main Benefits

| Benefit | Meaning |
|---|---|
| Simplicity | Reduces visible complexity |
| Maintainability | Internal implementation can change |
| Security | Internal details can remain hidden |
| Flexibility | Different implementations can follow the same contract |
| Reusability | Common interfaces/abstract classes can be reused |
| Loose coupling | Code can depend on abstractions rather than implementations |

---

## 5. Real-World Examples

### Example 1 — ATM

User sees:

```text
Withdraw
Deposit
Check Balance
```

Hidden:

```text
Database
Bank server
Transaction processing
Encryption
Validation
```

Therefore:

$$
\boxed{\text{ATM interface = Abstraction}}
$$

---

### Example 2 — Car

User interacts with:

```text
start()
accelerate()
brake()
```

Hidden:

```text
Engine mechanism
Fuel injection
Transmission
Internal sensors
```

Therefore:

$$
\boxed{\text{Driving controls = Abstraction}}
$$

---

### Example 3 — Mobile Phone

User performs:

```text
call()
sendMessage()
takePhoto()
```

Hidden:

```text
Network protocols
Signal processing
Camera processing
Operating system internals
```

The user interacts with simple operations without knowing the implementation.

---

### Example 4 — Online Payment

User sees:

```text
Pay ₹500
```

Hidden:

```text
Authentication
Transaction validation
Bank communication
Encryption
Database updates
```

The payment interface provides abstraction.

---

## 6. Important Properties

### 6.1 Hides Unnecessary Implementation Details

Abstraction hides details that the user does not need.

Example:

    ~~~~java
    interface Payment {
        void pay(double amount);
    }
    ~~~~

The interface tells the user that payment can be performed.

It does not expose the internal implementation.

---

### 6.2 Shows Essential Functionality

Abstraction does not hide everything.

It exposes the operations required by the user.

For example:

    ~~~~java
    payment.pay(1000);
    ~~~~

The user knows:

```text
pay() exists
pay() accepts an amount
```

The user does not need to know how the payment is processed internally.

---

### 6.3 Abstract Classes Support Abstraction

An abstract class can contain abstract methods.

Example:

    ~~~~java
    abstract class Animal {

        abstract void sound();
    }
    ~~~~

The method:

    ~~~~java
    abstract void sound();
    ~~~~

specifies required behavior.

The implementation can be provided by subclasses.

---

### 6.4 Abstract Classes Can Contain Concrete Methods

An important interview point:

> [!important]
> An abstract class does **not** have to contain only abstract methods.

Example:

    ~~~~java
    abstract class Animal {

        abstract void sound();

        void sleep() {
            System.out.println("Sleeping");
        }
    }
    ~~~~

Here:

```text
sound() → Abstract method
sleep()  → Concrete method
```

---

### 6.5 Abstract Classes Cannot Be Directly Instantiated

Consider:

    ~~~~java
    abstract class Animal {
        abstract void sound();
    }
    ~~~~

This is invalid:

    ~~~~java
    Animal a = new Animal();
    ~~~~

Because `Animal` is abstract.

But this is valid:

    ~~~~java
    Animal a = new Dog();
    ~~~~

if `Dog` is a concrete subclass.

---

### 6.6 Interfaces Provide Abstraction

Example:

    ~~~~java
    interface Vehicle {
        void start();
    }
    ~~~~

A class can implement it:

    ~~~~java
    class Car implements Vehicle {

        public void start() {
            System.out.println("Car started");
        }
    }
    ~~~~

The interface defines the required behavior.

The implementing class provides the implementation.

---

### 6.7 Abstraction Provides a Contract

An interface can define a contract.

Example:

    ~~~~java
    interface Payment {
        void pay();
    }
    ~~~~

Any concrete class implementing `Payment` must provide the required method.

Examples:

```text
UPIPayment
CardPayment
CashPayment
WalletPayment
```

All can follow the same abstraction:

```text
pay()
```

But each can implement it differently.

---

### 6.8 Abstraction Supports Multiple Implementations

Consider:

    ~~~~java
    interface Payment {
        void pay();
    }
    ~~~~

Different implementations:

    ~~~~java
    class CardPayment implements Payment {

        public void pay() {
            System.out.println("Card payment");
        }
    }
    ~~~~

    ~~~~java
    class UPIPayment implements Payment {

        public void pay() {
            System.out.println("UPI payment");
        }
    }
    ~~~~

Both provide:

```text
pay()
```

but the internal implementation is different.

This is one of the major practical benefits of abstraction.

---

## 7. Abstract Class

An abstract class is declared using the `abstract` keyword.

Syntax:

    ~~~~java
    abstract class ClassName {

        abstract void methodName();

        void concreteMethod() {
            // implementation
        }
    }
    ~~~~

### Example

    ~~~~java
    abstract class Shape {

        abstract void draw();

        void display() {
            System.out.println("Shape");
        }
    }
    ~~~~

The class contains:

```text
draw()    → Abstract
display() → Concrete
```

### Key Points

- Declared using `abstract`
- Cannot normally be instantiated directly
- Can contain abstract methods
- Can contain concrete methods
- Can contain constructors
- Can contain instance variables
- Can be inherited by subclasses

---

## 8. Abstract Method

An abstract method is a method declared without an implementation body.

Syntax:

    ~~~~java
    abstract returnType methodName();
    ~~~~

Example:

    ~~~~java
    abstract void draw();
    ~~~~

The subclass provides the implementation:

    ~~~~java
    class Circle extends Shape {

        @Override
        void draw() {
            System.out.println("Drawing Circle");
        }
    }
    ~~~~

### Recognition Trick

> [!important]
> If you see:
>
> `abstract` + method declaration + no method body
>
> think:
>
> **Abstract Method**

---

## 9. Interface

An interface defines a contract that implementing classes agree to follow.

Example:

    ~~~~java
    interface Vehicle {

        void start();

        void stop();
    }
    ~~~~

Implementation:

    ~~~~java
    class Car implements Vehicle {

        public void start() {
            System.out.println("Car started");
        }

        public void stop() {
            System.out.println("Car stopped");
        }
    }
    ~~~~

Here:

```text
Vehicle → Abstraction / Contract
Car     → Implementation
```

### Important Java Point

Modern Java interfaces can also contain:

- Abstract methods
- Default methods
- Static methods
- Private methods

So do not memorize the outdated statement:

```text
Interface contains only abstract methods.
```

That is not generally correct for modern Java.

---

## 10. Abstract Class vs Interface

| Feature | Abstract Class | Interface |
|---|---|---|
| Keyword | `abstract class` | `interface` |
| Direct object creation | No | No |
| Abstract methods | Yes | Yes |
| Concrete methods | Yes | Yes, including default/static/private methods under Java rules |
| Instance variables | Yes | Fields are constants |
| Constructor | Yes | No constructor |
| Inheritance keyword | `extends` | `implements` |
| Multiple inheritance of type | A class extends one class | A class can implement multiple interfaces |
| Main purpose | Partial abstraction + shared implementation | Contract / abstraction |

### Fast Memory

> [!tip]
> **Abstract Class**
>
> Think:
>
> **Partial abstraction + shared code**

> [!tip]
> **Interface**
>
> Think:
>
> **Contract + abstraction + multiple type inheritance**

---

## 11. Abstraction vs Encapsulation

This is one of the most important OOP interview comparisons.

### Abstraction

Focuses on:

```text
What should be exposed?
What implementation details can be hidden?
```

### Encapsulation

Focuses on:

```text
How should data and behavior be bundled?
How should access be controlled?
```

| Abstraction | Encapsulation |
|---|---|
| Hides unnecessary implementation details | Controls access to internal members |
| Focuses on WHAT | Focuses on access and structure |
| Commonly uses abstract classes/interfaces | Commonly uses classes/access modifiers |
| Reduces complexity | Protects and controls state |
| Example: `payment.pay()` | Example: `private balance` |

> [!important]
> **Abstraction → Hide HOW**
>
> **Encapsulation → Control ACCESS**

---

## 12. Basic Examples

### Example 1 — Identify Abstraction

**Question**

Which OOP concept hides implementation details and exposes only essential functionality?

```text
A. Inheritance
B. Abstraction
C. Polymorphism
D. Composition
```

**Pattern**

Look for:

```text
Hide HOW
Show WHAT
```

**Therefore:**

$$
\boxed{\text{B. Abstraction}}
$$

---

### Example 2 — Identify Abstract Class

**Question**

Consider:

    ~~~~java
    abstract class Vehicle {
        abstract void start();
    }
    ~~~~

What is `Vehicle`?

**Pattern**

Look for:

```text
abstract class
```

**Therefore:**

$$
\boxed{\text{Vehicle is an abstract class}}
$$

---

### Example 3 — Identify Abstract Method

**Question**

Which method is abstract?

    ~~~~java
    abstract class Animal {

        abstract void sound();

        void sleep() {
            System.out.println("Sleeping");
        }
    }
    ~~~~

**Pattern**

Abstract method:

```text
Uses abstract keyword
+
No method body
```

**Therefore:**

$$
\boxed{\text{sound()}}
$$

---

### Example 4 — Identify Interface

**Question**

Consider:

    ~~~~java
    interface Payment {
        void pay();
    }
    ~~~~

What concept does this demonstrate?

**Pattern**

The `interface` defines a contract and hides implementation details.

**Therefore:**

$$
\boxed{\text{Abstraction}}
$$

---

## 13. Medium Examples

### Example 5 — Abstract Class Instantiation

**Question**

Which statement is invalid?

    ~~~~java
    abstract class Shape {
        abstract void draw();
    }

    class Circle extends Shape {
        void draw() {
            System.out.println("Circle");
        }
    }
    ~~~~

Options:

```text
A. Shape s;
B. Shape s = null;
C. Shape s = new Shape();
D. Shape s = new Circle();
```

**Pattern**

An abstract class cannot be directly instantiated.

**Calculation**

```text
Shape s               → Valid
Shape s = null        → Valid
new Shape()           → Invalid
new Circle()          → Valid
```

**Therefore:**

$$
\boxed{\text{C. Shape s = new Shape();}}
$$

---

### Example 6 — Abstract and Concrete Methods

**Question**

How many abstract and concrete methods exist?

    ~~~~java
    abstract class Vehicle {

        abstract void start();

        void stop() {
            System.out.println("Stopped");
        }

        void display() {
            System.out.println("Vehicle");
        }
    }
    ~~~~

**Calculation**

```text
start()   → Abstract
stop()    → Concrete
display() → Concrete
```

Therefore:

$$
\boxed{1\text{ abstract method and }2\text{ concrete methods}}
$$

---

### Example 7 — Interface Implementation

**Question**

Consider:

    ~~~~java
    interface Payment {
        void pay();
    }

    class UPI implements Payment {

        public void pay() {
            System.out.println("UPI Payment");
        }
    }
    ~~~~

Which class provides the implementation?

**Pattern**

The class after `implements` provides the implementation.

**Therefore:**

$$
\boxed{\text{UPI}}
$$

---

### Example 8 — What vs How

**Question**

Consider:

    ~~~~java
    interface Printer {
        void print();
    }
    ~~~~

and:

    ~~~~java
    class LaserPrinter implements Printer {

        public void print() {
            System.out.println("Printing using laser technology");
        }
    }
    ~~~~

Which represents the abstraction?

**Pattern**

The interface defines what operation is available.

The implementation defines how it works.

**Therefore:**

$$
\boxed{\text{Printer interface = Abstraction}}
$$

$$
\boxed{\text{LaserPrinter = Implementation}}
$$

---

## 14. Advanced Examples

### Example 9 — Multiple Implementations

**Question**

Consider:

    ~~~~java
    interface Payment {
        void pay(int amount);
    }

    class CardPayment implements Payment {

        public void pay(int amount) {
            System.out.println("Card: " + amount);
        }
    }

    class UPIPayment implements Payment {

        public void pay(int amount) {
            System.out.println("UPI: " + amount);
        }
    }
    ~~~~

What is the main advantage of the abstraction?

**Pattern**

Both classes follow the same contract but have different implementations.

**Calculation**

```text
Payment
   ↓
pay()
   ↓
CardPayment
UPIPayment
```

Therefore:

$$
\boxed{\text{Different implementations can follow the same abstraction}}
$$

---

### Example 10 — Runtime Polymorphism Through Abstraction

**Question**

Consider:

    ~~~~java
    interface Payment {
        void pay();
    }

    class CardPayment implements Payment {

        public void pay() {
            System.out.println("Card");
        }
    }

    class UPIPayment implements Payment {

        public void pay() {
            System.out.println("UPI");
        }
    }
    ~~~~

Now:

    ~~~~java
    Payment p = new CardPayment();
    p.pay();
    ~~~~

What is printed?

**Pattern**

The reference type is `Payment`, but the actual object is `CardPayment`.

At runtime, the implementation belonging to the actual object is used.

**Calculation**

```text
Reference type → Payment
Actual object  → CardPayment
Called method  → CardPayment.pay()
```

Therefore:

$$
\boxed{\text{Card}}
$$

This demonstrates how abstraction can work together with runtime polymorphism.

---

### Example 11 — Abstraction Hides Internal Algorithm

**Question**

Consider:

    ~~~~java
    interface Sorter {
        void sort(int[] arr);
    }
    ~~~~

Suppose one implementation uses Quick Sort and another uses Merge Sort.

The caller simply does:

    ~~~~java
    sorter.sort(arr);
    ~~~~

What is hidden?

**Pattern**

The caller only uses the common operation.

**Calculation**

```text
Exposed:
sort()

Hidden:
Sorting algorithm
Implementation details
Internal steps
```

**Therefore:**

$$
\boxed{\text{The sorting implementation is hidden}}
$$

---

### Example 12 — Abstraction Through a Reference

**Question**

Consider:

    ~~~~java
    abstract class Shape {
        abstract double area();
    }

    class Circle extends Shape {

        double radius;

        Circle(double radius) {
            this.radius = radius;
        }

        double area() {
            return Math.PI * radius * radius;
        }
    }
    ~~~~

Now:

    ~~~~java
    Shape s = new Circle(5);
    ~~~~

What does the reference type `Shape` provide?

**Pattern**

The reference uses the abstraction defined by `Shape`.

**Calculation**

```text
Shape → Defines area()
Circle → Implements area()
```

The caller can work with:

```java
s.area();
```

without needing to depend directly on the internal implementation details of `Circle`.

**Therefore:**

$$
\boxed{\text{Shape provides the abstraction}}
$$

---

## 15. Shortcuts

> [!tip]
> **Shortcut 1: WHAT vs HOW**
>
> This is the fastest abstraction trick:
>
> ```text
> WHAT → Abstraction
> HOW  → Implementation
> ```

> [!tip]
> **Shortcut 2: Interface**
>
> If the question contains:
>
> ```java
> interface
> ```
>
> strongly consider:
>
> **Abstraction / Contract**

> [!tip]
> **Shortcut 3: Abstract Class**
>
> If you see:
>
> ```java
> abstract class
> ```
>
> think:
>
> **Abstraction**

> [!tip]
> **Shortcut 4: Abstract Method**
>
> If you see:
>
> ```java
> abstract void method();
> ```
>
> think:
>
> **Required behavior without implementation**

> [!tip]
> **Shortcut 5: Cannot Instantiate**
>
> If a class is abstract:
>
> ```java
> new AbstractClass()
> ```
>
> is invalid.

> [!tip]
> **Shortcut 6: Same Contract, Different Implementation**
>
> If several classes implement the same interface:
>
> ```text
> One abstraction
> +
> Multiple implementations
> ```

> [!tip]
> **Shortcut 7: Encapsulation vs Abstraction**
>
> ```text
> Encapsulation → ACCESS
> Abstraction   → IMPLEMENTATION DETAILS
> ```

---

## 16. Recognition Tricks

### Pattern 1 — "Hide Implementation"

> [!important]
> If the question says:
>
> **"Hide implementation details"**
>
> Think:
>
> **Abstraction**

---

### Pattern 2 — "Essential Features"

> [!important]
> If the question says:
>
> **"Expose only essential features"**
>
> Think:
>
> **Abstraction**

---

### Pattern 3 — "What Instead of How"

> [!important]
> If the question asks:
>
> **"What does it do rather than how does it work?"**
>
> Think:
>
> **Abstraction**

---

### Pattern 4 — "Interface"

> [!important]
> If you see:

    ~~~~java
    interface Vehicle {
        void start();
    }
    ~~~~

Think:

**Interface → Abstraction / Contract**

---

### Pattern 5 — "Abstract Class"

> [!important]
> If you see:

    ~~~~java
    abstract class Shape {
    }
    ~~~~

Think:

**Abstract class → Abstraction**

---

### Pattern 6 — "No Implementation"

> [!important]
> If you see:

    ~~~~java
    abstract void draw();
    ~~~~

Think:

**Abstract method**

---

### Pattern 7 — "Cannot Create Object"

> [!important]
> If you see:

    ~~~~java
    abstract class Animal
    ~~~~

and the question asks whether:

    ~~~~java
    new Animal()
    ~~~~

is allowed:

**No.**

---

### Pattern 8 — "Different Classes, Same Operation"

> [!important]
> If several classes provide the same operation through one common interface:

```text
Common operation
        ↓
Common abstraction
        ↓
Different implementations
```

Think:

**Abstraction + Polymorphism**

---

## 17. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Definition

Identify abstraction as hiding unnecessary implementation details.

### Pattern 2 — WHAT vs HOW

Recognize the difference between exposed functionality and internal implementation.

### Pattern 3 — Abstract Class

Identify an abstract class using the `abstract` keyword.

### Pattern 4 — Abstract Method

Identify a method declared without implementation.

### Pattern 5 — Interface

Recognize an interface as a common mechanism for abstraction in Java.

### Pattern 6 — Abstract Class Instantiation

Remember that an abstract class cannot be directly instantiated.

### Pattern 7 — Concrete Subclass

Understand how subclasses provide implementations of abstract methods.

### Pattern 8 — Abstract + Concrete Methods

Remember that an abstract class can contain both.

### Pattern 9 — Multiple Implementations

Recognize when different classes implement the same abstraction.

### Pattern 10 — Contract

Understand interfaces as contracts defining required operations.

### Pattern 11 — Abstraction vs Encapsulation

Differentiate implementation hiding from access control.

### Pattern 12 — Runtime Polymorphism

Recognize abstraction combined with dynamic method dispatch.

### Pattern 13 — Code Identification

Choose which code correctly demonstrates abstraction.

### Pattern 14 — Real-World Abstraction

Identify examples such as ATM, payment systems, car controls, and remote controls.

### Pattern 15 — Implementation Independence

Understand that callers can use an abstraction without depending on the implementation details.

---

## 18. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Abstraction Means Hiding Everything

Wrong:

```text
Abstraction = Hide everything
```

Correct:

```text
Abstraction = Hide unnecessary details
              + expose essential functionality
```

---

### Mistake 2 — Confusing Abstraction With Encapsulation

Remember:

```text
Abstraction
→ Focuses on WHAT
→ Hides unnecessary HOW

Encapsulation
→ Focuses on controlling ACCESS
→ Bundles data and behavior
```

---

### Mistake 3 — Thinking Abstract Class Contains Only Abstract Methods

Wrong:

```text
Abstract class = only abstract methods
```

Correct:

```text
Abstract class can contain:
- Abstract methods
- Concrete methods
- Fields
- Constructors
- Other members
```

---

### Mistake 4 — Trying to Instantiate an Abstract Class

Wrong:

    ~~~~java
    abstract class Animal {
    }

    Animal a = new Animal();
    ~~~~

Correct:

    ~~~~java
    Animal a = new Dog();
    ~~~~

when `Dog` is a concrete subclass.

---

### Mistake 5 — Assuming Every Interface Method Has No Implementation

For modern Java, interfaces can contain default, static, and private methods with implementations.

Do not use the oversimplified rule:

```text
Interface = only abstract methods
```

---

### Mistake 6 — Confusing Abstract Class and Interface

Both can support abstraction, but they are not identical.

Remember:

```text
Abstract Class → Shared state/implementation + abstraction
Interface      → Contract/type abstraction
```

---

### Mistake 7 — Thinking Abstraction and Polymorphism Are the Same

They often work together, but they are different concepts.

```text
Abstraction  → Hides implementation details
Polymorphism → Same interface, different behavior
```

---

### Mistake 8 — Forgetting the Actual Object

Consider:

    ~~~~java
    Payment p = new UPIPayment();
    ~~~~

The reference type is:

```text
Payment
```

The actual object is:

```text
UPIPayment
```

For overridden methods, runtime behavior depends on the actual object.

---

## 19. Formula Sheet

```text
Abstraction
= Essential Features
+ Hidden Unnecessary Implementation Details

Core Idea:
WHAT → Exposed
HOW  → Hidden

Java Abstraction:
→ Abstract Classes
→ Interfaces

Abstract Class:
abstract class ClassName {
}

Abstract Method:
abstract void methodName();

Abstract Class:
→ Cannot be directly instantiated

Concrete Subclass:
→ Provides implementation of abstract methods

Interface:
interface InterfaceName {
}

Implementation:
class ClassName implements InterfaceName {
}

Abstraction vs Encapsulation:

Abstraction → Hide implementation details
Encapsulation → Control access to internal members

Abstraction + Polymorphism:
→ Common abstraction
→ Different implementations
```

---

## 20. Quick Revision

> [!summary] One-Minute Revision

### Core Idea

```text
Abstraction = Show WHAT + Hide HOW
```

### Remember

- Abstraction hides unnecessary implementation details.
- It exposes essential functionality.
- Java commonly uses abstract classes and interfaces.
- Abstract classes use the `abstract` keyword.
- Abstract methods do not provide an implementation in their declaration.
- Abstract classes cannot be directly instantiated.
- Abstract classes can contain concrete methods.
- Interfaces define contracts.
- Different classes can implement the same interface differently.
- Abstraction reduces complexity.
- Abstraction improves flexibility and maintainability.
- Abstraction often works together with polymorphism.

### Fast Comparison

```text
Class
→ Blueprint

Object
→ Instance

State
→ What it has

Behavior
→ What it does

Identity
→ Which object it is

Encapsulation
→ Controls ACCESS

Abstraction
→ Hides unnecessary HOW

Inheritance
→ Reuses/extends existing structure

Polymorphism
→ Same interface, different behavior
```

### Golden Memory Trick

**Abstraction means showing what an object can do while hiding the unnecessary details of how it does it.**

### One-Line Recognition

**If the question contains "hide implementation", "essential features", "WHAT instead of HOW", abstract class, or interface, think Abstraction.**