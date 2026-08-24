---
type: concept
subject: aptitude
topic: "Interfaces"
parent: "OOP Basics"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - interfaces
  - abstraction
  - java
  - object-oriented-programming
wikilinks:
  - "[[OOP Basics]]"
  - "[[Abstraction]]"
  - "[[Encapsulation]]"
  - "[[Inheritance]]"
  - "[[Polymorphism]]"
---

# Interfaces

> [!summary]
> **An interface is a contract that defines what a class must do without requiring the class to use a particular implementation.**
>
> In Java, interfaces are one of the most important tools for **abstraction, loose coupling, polymorphism, and multiple inheritance of type**.

## 1. Core Concept

The easiest way to understand an interface is:

$$
\boxed{\text{Interface} = \text{Contract}}
$$

A contract says:

> "If you want to use me, you must provide these operations."

For example, imagine a payment system.

Different payment methods can exist:

```text
UPI
Credit Card
Debit Card
Net Banking
Wallet
```

All of them need to perform a payment operation.

Instead of creating unrelated methods everywhere, we can define a common contract:

    ~~~~java
    interface Payment {

        void pay(double amount);
    }
    ~~~~

Now different classes can implement it:

    ~~~~java
    class UPIPayment implements Payment {

        public void pay(double amount) {
            System.out.println("Paid using UPI");
        }
    }
    ~~~~

    ~~~~java
    class CardPayment implements Payment {

        public void pay(double amount) {
            System.out.println("Paid using Card");
        }
    }
    ~~~~

Both classes must provide:

```text
pay()
```

But they can implement it differently.

### The Big Picture

```text
                    Payment
                       |
              +--------+--------+
              |                 |
         UPIPayment        CardPayment
              |                 |
          pay()             pay()
              |                 |
        UPI implementation  Card implementation
```

The interface defines **WHAT**.

The implementing class defines **HOW**.

> [!important]
> **Interface → WHAT**
>
> **Implementation → HOW**

---

# 2. Basic Meaning

An interface is a reference type in Java used to define a common contract for classes.

Basic syntax:

    ~~~~java
    interface Animal {

        void sound();
    }
    ~~~~

A class implements an interface using:

    ~~~~java
    class Dog implements Animal {

        public void sound() {
            System.out.println("Bark");
        }
    }
    ~~~~

Here:

```text
Animal → Interface
sound() → Contract
Dog → Implementing class
Dog.sound() → Implementation
```

The interface does not need to know how `Dog` produces its sound.

It only defines that a `Dog` implementing `Animal` must provide the required behavior.

---

# 3. Why Do We Need Interfaces?

Without interfaces, code can become tightly connected to specific implementations.

Suppose an application directly depends on:

```text
UPIPayment
```

Later, you want to switch to:

```text
CardPayment
```

If the entire application directly depends on `UPIPayment`, many parts of the code may need modification.

Instead, depend on:

```text
Payment
```

Then the implementation can change.

```text
Application
     |
     v
 Payment Interface
     |
 +---+---+
 |       |
UPI     Card
```

The application does not need to know the exact implementation.

This is called:

> [!important]
> **Programming to an interface rather than programming to an implementation.**

---

# 4. Main Formula

There is no mathematical formula for an interface.

For interviews, remember:

$$
\boxed{\text{Interface} = \text{Contract} + \text{Abstraction}}
$$

Another important relationship:

$$
\boxed{\text{Interface} \rightarrow \text{Common Behavior}}
$$

And:

$$
\boxed{\text{Different Classes} \rightarrow \text{Same Contract} \rightarrow \text{Different Implementations}}
$$

---

# 5. Basic Syntax

## Interface Declaration

    ~~~~java
    interface Vehicle {

        void start();

        void stop();
    }
    ~~~~

## Implementing an Interface

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

## Creating an Object

    ~~~~java
    Vehicle v = new Car();

    v.start();
    v.stop();
    ~~~~

Notice something important:

```text
Reference type → Vehicle
Actual object  → Car
```

This is very important for polymorphism.

---

# 6. Real-Time Example 1 — Payment System

Imagine an e-commerce application.

Customers can pay using:

```text
UPI
Credit Card
Debit Card
Net Banking
Wallet
```

Instead of writing separate application logic for every payment type, define:

    ~~~~java
    interface Payment {

        void pay(double amount);
    }
    ~~~~

UPI:

    ~~~~java
    class UPIPayment implements Payment {

        public void pay(double amount) {
            System.out.println("Processing UPI payment");
        }
    }
    ~~~~

Card:

    ~~~~java
    class CardPayment implements Payment {

        public void pay(double amount) {
            System.out.println("Processing card payment");
        }
    }
    ~~~~

Now the application can work with:

    ~~~~java
    Payment payment;
    ~~~~

It does not need to tightly depend on a particular payment method.

### Real-World Architecture

```text
                    Payment
                       |
       +---------------+---------------+
       |               |               |
      UPI             Card          Wallet
       |               |               |
    pay()            pay()           pay()
```

> [!important]
> The interface gives the application a **common language** for different payment systems.

---

# 7. Real-Time Example 2 — Notification System

A modern application may send notifications through:

```text
Email
SMS
WhatsApp
Push Notification
```

Create:

    ~~~~java
    interface Notification {

        void send(String message);
    }
    ~~~~

Email:

    ~~~~java
    class EmailNotification implements Notification {

        public void send(String message) {
            System.out.println("Sending Email");
        }
    }
    ~~~~

SMS:

    ~~~~java
    class SMSNotification implements Notification {

        public void send(String message) {
            System.out.println("Sending SMS");
        }
    }
    ~~~~

Now the application can use:

    ~~~~java
    Notification notification;
    ~~~~

The application does not need to care whether the notification is sent by email or SMS.

### Why This Is Powerful

Tomorrow, you can add:

```text
WhatsAppNotification
SlackNotification
PushNotification
```

without changing the basic contract.

---

# 8. Real-Time Example 3 — Food Delivery

Suppose a food delivery application supports:

```text
Swiggy
Zomato
Restaurant Delivery
Third-Party Delivery Partner
```

The application can define:

    ~~~~java
    interface DeliveryService {

        void deliver(Order order);
    }
    ~~~~

Every delivery provider implements:

```text
deliver()
```

The application depends on the interface rather than a specific delivery company.

This makes the system easier to extend.

---

# 9. Real-Time Example 4 — Ride Booking

A ride application may support:

```text
Bike
Auto
Mini Car
Sedan
SUV
```

Define:

    ~~~~java
    interface Ride {

        void book();

        double calculateFare();
    }
    ~~~~

Each ride type can implement the methods differently.

```text
Ride
 |
 +---- Bike
 |
 +---- Auto
 |
 +---- Sedan
 |
 +---- SUV
```

All rides follow the same contract.

---

# 10. Real-Time Example 5 — Database Connection

A software application may work with:

```text
MySQL
PostgreSQL
Oracle
MongoDB
```

A system can define a common abstraction:

    ~~~~java
    interface Database {

        void connect();

        void disconnect();

        void executeQuery(String query);
    }
    ~~~~

Different database implementations can provide their own behavior.

```text
                Database
                    |
        +-----------+-----------+
        |           |           |
      MySQL      PostgreSQL   Oracle
```

This is a very common software-engineering use case.

---

# 11. Real-Time Example 6 — Logging

A production application may send logs to:

```text
Console
File
Database
Cloud
Monitoring Service
```

An abstraction could be:

    ~~~~java
    interface Logger {

        void log(String message);
    }
    ~~~~

Implementations:

```text
ConsoleLogger
FileLogger
DatabaseLogger
CloudLogger
```

The application can work with:

```text
Logger
```

instead of depending on one specific logger.

---

# 12. Important Properties

## 12.1 Interface Defines a Contract

An interface can specify operations that implementing classes must provide.

Example:

    ~~~~java
    interface Printer {

        void print();
    }
    ~~~~

Any concrete class implementing `Printer` must provide the required behavior.

---

## 12.2 A Class Uses `implements`

Correct:

    ~~~~java
    class Car implements Vehicle {
    }
    ~~~~

Not:

    ~~~~java
    class Car extends Vehicle {
    }
    ~~~~

when `Vehicle` is an interface.

Remember:

```text
Class → extends Class
Class → implements Interface
Interface → extends Interface
```

---

## 12.3 A Class Can Implement Multiple Interfaces

This is one of the biggest advantages of interfaces.

Example:

    ~~~~java
    interface Camera {
        void takePhoto();
    }

    interface GPS {
        void navigate();
    }

    class Smartphone implements Camera, GPS {

        public void takePhoto() {
            System.out.println("Photo taken");
        }

        public void navigate() {
            System.out.println("Navigation started");
        }
    }
    ~~~~

A class can implement multiple interfaces.

Therefore:

$$
\boxed{\text{One class} \rightarrow \text{Multiple interfaces}}
$$

---

# 13. Real-Time Example — Smartphone

A smartphone can have multiple capabilities:

```text
Camera
GPS
Bluetooth
WiFi
Payment
```

Instead of placing everything into one massive inheritance hierarchy, interfaces can represent capabilities.

    ~~~~java
    interface Camera {
        void takePhoto();
    }
    ~~~~

    ~~~~java
    interface GPS {
        void navigate();
    }
    ~~~~

    ~~~~java
    class Smartphone implements Camera, GPS {

        public void takePhoto() {
            System.out.println("Taking photo");
        }

        public void navigate() {
            System.out.println("Navigating");
        }
    }
    ~~~~

This models real-world capabilities naturally.

---

# 14. Interface Variables

An interface can be used as a reference type.

Example:

    ~~~~java
    interface Animal {

        void sound();
    }

    class Dog implements Animal {

        public void sound() {
            System.out.println("Bark");
        }
    }
    ~~~~

Now:

    ~~~~java
    Animal animal = new Dog();
    ~~~~

This is valid.

Why?

Because `Dog` implements `Animal`.

The reference can therefore use the interface contract.

---

# 15. Interface Reference and Polymorphism

This is one of the most important interview concepts.

Consider:

    ~~~~java
    interface Payment {

        void pay();
    }
    ~~~~

    ~~~~java
    class UPIPayment implements Payment {

        public void pay() {
            System.out.println("UPI");
        }
    }
    ~~~~

    ~~~~java
    class CardPayment implements Payment {

        public void pay() {
            System.out.println("Card");
        }
    }
    ~~~~

Now:

    ~~~~java
    Payment p = new UPIPayment();
    p.pay();
    ~~~~

Output:

```text
UPI
```

Change the object:

    ~~~~java
    Payment p = new CardPayment();
    p.pay();
    ~~~~

Output:

```text
Card
```

The same interface reference can refer to different implementations.

This demonstrates:

$$
\boxed{\text{Interface + Polymorphism}}
$$

---

# 16. Interface and Loose Coupling

Loose coupling means reducing dependency between components.

### Tight Coupling

    ~~~~java
    class OrderService {

        private UPIPayment payment;

        void makePayment() {
            payment.pay();
        }
    }
    ~~~~

This directly depends on `UPIPayment`.

Changing payment methods may require changes in `OrderService`.

### Loose Coupling

    ~~~~java
    class OrderService {

        private Payment payment;

        OrderService(Payment payment) {
            this.payment = payment;
        }

        void makePayment() {
            payment.pay();
        }
    }
    ~~~~

Now:

```text
OrderService
      |
      v
   Payment
      |
 +----+----+
 |         |
UPI       Card
```

The service depends on the abstraction.

This is a major reason interfaces are used in professional software.

---

# 17. Dependency Injection Connection

Interfaces are frequently used with **Dependency Injection**.

Example:

    ~~~~java
    interface Payment {
        void pay();
    }
    ~~~~

    ~~~~java
    class OrderService {

        private Payment payment;

        OrderService(Payment payment) {
            this.payment = payment;
        }

        void checkout() {
            payment.pay();
        }
    }
    ~~~~

Now:

    ~~~~java
    Payment payment = new UPIPayment();

    OrderService service = new OrderService(payment);
    ~~~~

The dependency is provided from outside.

This makes the code:

- Flexible
- Testable
- Maintainable
- Loosely coupled

> [!important]
> **Interface + Dependency Injection = Very common professional design pattern**

---

# 18. Interface Methods in Modern Java

For interview preparation, know the major types.

## 18.1 Abstract Method

    ~~~~java
    interface Vehicle {

        void start();
    }
    ~~~~

The method has no implementation body.

---

## 18.2 Default Method

Modern Java interfaces can have default methods.

    ~~~~java
    interface Vehicle {

        default void display() {
            System.out.println("Vehicle");
        }
    }
    ~~~~

A class can inherit this implementation.

---

## 18.3 Static Method

An interface can contain static methods.

    ~~~~java
    interface MathUtil {

        static int square(int n) {
            return n * n;
        }
    }
    ~~~~

Called using the interface name:

    ~~~~java
    int result = MathUtil.square(5);
    ~~~~

---

## 18.4 Private Method

Modern Java interfaces can also contain private methods for internal reuse among interface methods.

Example:

    ~~~~java
    interface Logger {

        default void info() {
            format();
            System.out.println("INFO");
        }

        private void format() {
            System.out.println("Formatting");
        }
    }
    ~~~~

A private interface method cannot be directly called by implementing classes.

---

# 19. Interface Variables and Constants

Fields declared in an interface are implicitly:

```text
public
static
final
```

Example:

    ~~~~java
    interface Constants {

        int MAX_USERS = 100;
    }
    ~~~~

Conceptually:

    ~~~~java
    public static final int MAX_USERS = 100;
    ~~~~

Therefore:

```text
Interface field
→ public
→ static
→ final
```

It behaves like a constant.

---

# 20. Can an Interface Have a Constructor?

No.

An interface cannot have a constructor.

Why?

Because an interface is not directly instantiated as an object.

Invalid:

    ~~~~java
    interface Vehicle {
    }

    Vehicle v = new Vehicle();
    ~~~~

The interface defines a contract/type.

A concrete implementing class creates the object.

---

# 21. Interface Inheritance

An interface can extend another interface.

Example:

    ~~~~java
    interface Animal {

        void eat();
    }
    ~~~~

    ~~~~java
    interface Dog extends Animal {

        void bark();
    }
    ~~~~

A class implementing `Dog` must satisfy the inherited contract as well.

    ~~~~java
    class Labrador implements Dog {

        public void eat() {
            System.out.println("Eating");
        }

        public void bark() {
            System.out.println("Barking");
        }
    }
    ~~~~

Remember:

```text
Interface → extends → Interface
Class     → implements → Interface
Class     → extends → Class
```

---

# 22. Multiple Interface Inheritance

An interface can extend multiple interfaces.

Example:

    ~~~~java
    interface Camera {
        void takePhoto();
    }

    interface GPS {
        void navigate();
    }

    interface SmartDevice extends Camera, GPS {
        void connect();
    }
    ~~~~

This is valid.

Therefore:

$$
\boxed{\text{Interface can extend multiple interfaces}}
$$

---

# 23. Default Method Conflict

This is an important interview-level topic.

Suppose:

    ~~~~java
    interface A {

        default void show() {
            System.out.println("A");
        }
    }
    ~~~~

    ~~~~java
    interface B {

        default void show() {
            System.out.println("B");
        }
    }
    ~~~~

Now:

    ~~~~java
    class C implements A, B {
    }
    ~~~~

This creates a conflict because both interfaces provide a default implementation of `show()`.

The class must resolve the conflict.

Example:

    ~~~~java
    class C implements A, B {

        public void show() {
            System.out.println("C");
        }
    }
    ~~~~

Now the class provides its own implementation.

> [!important]
> If two interfaces provide conflicting default methods, the implementing class must resolve the ambiguity.

---

# 24. Interface vs Abstract Class

This is a very common interview question.

| Feature | Interface | Abstract Class |
|---|---|---|
| Declaration | `interface` | `abstract class` |
| Object creation | Not directly | Not directly |
| Abstract methods | Yes | Yes |
| Concrete methods | Yes in modern Java | Yes |
| Instance variables | No normal instance fields; fields are constants | Yes |
| Constructors | No | Yes |
| Multiple implementation/inheritance | A class can implement multiple interfaces | A class can extend only one class |
| Main use | Contract / abstraction | Shared base behavior + abstraction |
| Keyword in class | `implements` | `extends` |

### Fast Memory

> [!tip]
> **Interface**
>
> Think:
>
> ```text
> Contract
> Multiple interfaces
> Loose coupling
> Abstraction
> ```

> [!tip]
> **Abstract Class**
>
> Think:
>
> ```text
> Common base
> Shared implementation
> Partial abstraction
> State + behavior
> ```

---

# 25. Interface vs Class

| Interface | Class |
|---|---|
| Defines a contract | Defines object structure/behavior |
| Cannot be directly instantiated | Can usually be instantiated if concrete |
| Implemented using `implements` | Extended using `extends` |
| Supports multiple implementation by a class | A class extends only one class |
| Used heavily for abstraction | Used to create objects |
| Fields are constants | Fields can be mutable instance variables |

---

# 26. Interface vs Encapsulation

Do not confuse them.

### Interface

Focuses on:

```text
What operations are available?
```

### Encapsulation

Focuses on:

```text
How is internal data protected and access controlled?
```

Example:

    ~~~~java
    interface BankAccount {

        void deposit(double amount);

        void withdraw(double amount);
    }
    ~~~~

This defines a contract.

Inside an implementation:

    ~~~~java
    class BankAccountImpl implements BankAccount {

        private double balance;

        public void deposit(double amount) {
            balance += amount;
        }

        public void withdraw(double amount) {
            balance -= amount;
        }
    }
    ~~~~

Here:

```text
Interface → Abstraction
private balance → Encapsulation
```

---

# 27. Interview Questions

## Interview Question 1

**What is an interface in Java?**

### Strong Answer

An interface is a reference type that defines a contract for implementing classes. It is commonly used for abstraction, loose coupling, polymorphism, and multiple inheritance of type. A class implements an interface and provides the required behavior.

---

## Interview Question 2

**Why do we use interfaces?**

### Answer

Interfaces are used to:

- Define contracts
- Achieve abstraction
- Reduce coupling
- Support polymorphism
- Allow a class to implement multiple interfaces
- Make code easier to extend and test
- Separate what a component does from how it does it

---

## Interview Question 3

**Can we create an object of an interface?**

### Answer

No, we cannot directly instantiate an interface.

Invalid:

    ~~~~java
    Payment p = new Payment();
    ~~~~

But we can use an interface as a reference:

    ~~~~java
    Payment p = new UPIPayment();
    ~~~~

---

## Interview Question 4

**Can a class implement multiple interfaces?**

### Answer

Yes.

Example:

    ~~~~java
    class Smartphone implements Camera, GPS {
    }
    ~~~~

A class can implement multiple interfaces.

---

## Interview Question 5

**Can an interface extend another interface?**

### Answer

Yes.

    ~~~~java
    interface A {
        void methodA();
    }

    interface B extends A {
        void methodB();
    }
    ~~~~

An interface can also extend multiple interfaces.

---

## Interview Question 6

**Can an interface extend a class?**

### Answer

No.

Correct relationships are:

```text
Class extends Class
Class implements Interface
Interface extends Interface
```

---

## Interview Question 7

**Can an abstract class implement an interface?**

### Answer

Yes.

Example:

    ~~~~java
    interface Vehicle {
        void start();
    }

    abstract class Car implements Vehicle {
    }
    ~~~~

Because `Car` is abstract, it does not necessarily have to provide implementations for all interface methods immediately.

A concrete subclass can complete the implementation.

---

## Interview Question 8

**Can an interface contain variables?**

### Answer

Yes.

Interface fields are implicitly:

```text
public
static
final
```

Therefore they behave as constants.

---

## Interview Question 9

**Can an interface have a constructor?**

### Answer

No.

An interface cannot be directly instantiated, so it does not have a constructor.

---

## Interview Question 10

**Can an interface have implemented methods?**

### Answer

Yes.

Modern Java interfaces can contain:

- Default methods
- Static methods
- Private methods

In addition to abstract methods.

---

## Interview Question 11

**What is the difference between `extends` and `implements`?**

### Answer

```text
extends
→ Class extends class
→ Interface extends interface

implements
→ Class implements interface
```

Example:

    ~~~~java
    class Dog extends Animal {
    }

    class Dog implements Pet {
    }

    interface SmartDog extends Pet {
    }
    ~~~~

---

## Interview Question 12

**Why is an interface useful for loose coupling?**

### Answer

Because the client can depend on the interface instead of a concrete implementation.

For example:

```text
OrderService
     ↓
 Payment
     ↓
 +---+---+
 |       |
 UPI    Card
```

The `OrderService` does not need to know the specific payment implementation.

---

## Interview Question 13

**What happens if two interfaces have the same default method?**

### Answer

If a class implements both interfaces and both provide conflicting default implementations, the class must resolve the conflict by overriding the method.

---

## Interview Question 14

**What is programming to an interface?**

### Answer

It means writing code that depends on an abstraction rather than a specific implementation.

Instead of:

    ~~~~java
    UPIPayment payment = new UPIPayment();
    ~~~~

prefer:

    ~~~~java
    Payment payment = new UPIPayment();
    ~~~~

when the design requires flexibility.

---

## Interview Question 15

**How does an interface support polymorphism?**

### Answer

A reference of interface type can refer to objects of different implementing classes.

Example:

    ~~~~java
    Payment p;

    p = new UPIPayment();
    p.pay();

    p = new CardPayment();
    p.pay();
    ~~~~

The same interface reference can produce different behavior depending on the actual object.

---

# 28. Output-Based Interview Questions

## Question 1

What is the output?

    ~~~~java
    interface Animal {

        void sound();
    }

    class Dog implements Animal {

        public void sound() {
            System.out.println("Bark");
        }
    }

    public class Main {

        public static void main(String[] args) {

            Animal a = new Dog();

            a.sound();
        }
    }
    ~~~~

### Analysis

```text
Reference → Animal
Object    → Dog
Method    → sound()
```

Runtime implementation:

```text
Dog.sound()
```

### Answer

```text
Bark
```

$$
\boxed{\text{Bark}}
$$

---

## Question 2

What is the output?

    ~~~~java
    interface Payment {

        void pay();
    }

    class UPI implements Payment {

        public void pay() {
            System.out.println("UPI");
        }
    }

    class Card implements Payment {

        public void pay() {
            System.out.println("Card");
        }
    }

    public class Main {

        public static void main(String[] args) {

            Payment p = new UPI();
            p.pay();

            p = new Card();
            p.pay();
        }
    }
    ~~~~

### Analysis

First:

```text
p → UPI
```

Output:

```text
UPI
```

Then:

```text
p → Card
```

Output:

```text
Card
```

### Answer

```text
UPI
Card
```

---

# 29. Pattern Recognition

### Pattern 1 — Contract

> [!important]
> If the question says:
>
> **"Defines a contract that classes must follow"**
>
> Think:
>
> **Interface**

---

### Pattern 2 — Multiple Interfaces

> [!important]
> If you see:
>
> `implements A, B`
>
> Think:
>
> **A class implementing multiple interfaces**

---

### Pattern 3 — Loose Coupling

> [!important]
> If the question says:
>
> **"Reduce dependency on concrete implementations"**
>
> Think:
>
> **Interface**

---

### Pattern 4 — WHAT vs HOW

> [!important]
> If the question says:
>
> **"Define what should happen but leave implementation to subclasses"**
>
> Think:
>
> **Interface / Abstraction**

---

### Pattern 5 — `implements`

> [!important]
> If you see:
>
> `class A implements B`
>
> Think:
>
> **B is an interface**

---

### Pattern 6 — `extends` Between Interfaces

> [!important]
> If you see:
>
> `interface B extends A`
>
> Think:
>
> **Interface inheritance**

---

### Pattern 7 — Interface Reference

> [!important]
> If you see:
>
> `Animal a = new Dog();`
>
> and `Dog implements Animal`
>
> Think:
>
> **Interface reference + Polymorphism**

---

# 30. Common Exam Patterns

> [!important] Must Master

### Pattern 1

Definition of interface.

### Pattern 2

Purpose of interfaces.

### Pattern 3

Interface vs abstract class.

### Pattern 4

Interface vs class.

### Pattern 5

`extends` vs `implements`.

### Pattern 6

Multiple interface implementation.

### Pattern 7

Interface inheritance.

### Pattern 8

Interface reference.

### Pattern 9

Runtime polymorphism.

### Pattern 10

Default methods.

### Pattern 11

Static methods in interfaces.

### Pattern 12

Private methods in interfaces.

### Pattern 13

Interface variables.

### Pattern 14

Interface constructors.

### Pattern 15

Default method conflict.

### Pattern 16

Loose coupling.

### Pattern 17

Dependency injection.

### Pattern 18

Programming to an interface.

### Pattern 19

Real-world design examples.

### Pattern 20

Output-based interface questions.

---

# 31. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Using `extends` for a Class Implementing an Interface

Wrong:

    ~~~~java
    class Car extends Vehicle {
    ~~~~

when `Vehicle` is an interface.

Correct:

    ~~~~java
    class Car implements Vehicle {
    ~~~~

---

### Mistake 2 — Thinking an Interface Can Be Instantiated

Wrong:

    ~~~~java
    Vehicle v = new Vehicle();
    ~~~~

Correct:

    ~~~~java
    Vehicle v = new Car();
    ~~~~

---

### Mistake 3 — Thinking Interface Means Only Abstract Methods

This is an outdated simplification.

Modern Java interfaces can contain:

```text
Abstract methods
Default methods
Static methods
Private methods
```

---

### Mistake 4 — Confusing Interface With Abstract Class

Remember:

```text
Interface
→ Contract
→ Multiple interfaces can be implemented

Abstract Class
→ Shared base implementation
→ Can contain instance state
```

---

### Mistake 5 — Ignoring the Actual Object

Consider:

    ~~~~java
    Payment p = new CardPayment();
    ~~~~

Do not think:

```text
Object = Payment
```

The actual object is:

```text
CardPayment
```

The reference type is:

```text
Payment
```

This matters for polymorphism.

---

### Mistake 6 — Confusing Interface With Encapsulation

```text
Interface
→ Defines contract

Encapsulation
→ Controls access to internal data
```

They can work together but represent different concepts.

---

### Mistake 7 — Forgetting Default Method Conflicts

If two interfaces provide conflicting default methods, the implementing class must resolve the conflict.

---

# 32. Interview Rapid-Fire Revision

> [!tip]
> **Q: What is an interface?**
>
> A: A contract/reference type used for abstraction and polymorphism.

> [!tip]
> **Q: Can we instantiate an interface?**
>
> A: No, not directly.

> [!tip]
> **Q: Can a class implement multiple interfaces?**
>
> A: Yes.

> [!tip]
> **Q: Can an interface extend another interface?**
>
> A: Yes.

> [!tip]
> **Q: Can an interface extend a class?**
>
> A: No.

> [!tip]
> **Q: Can an interface contain concrete methods?**
>
> A: Yes, through default, static, and private methods.

> [!tip]
> **Q: Can an interface have a constructor?**
>
> A: No.

> [!tip]
> **Q: What keyword does a class use to use an interface?**
>
> A: `implements`.

> [!tip]
> **Q: What keyword is used when one interface inherits another?**
>
> A: `extends`.

> [!tip]
> **Q: Why are interfaces useful?**
>
> A: Abstraction, loose coupling, polymorphism, flexibility, and multiple type inheritance.

---

# 33. Formula Sheet

```text
Interface = Contract + Abstraction

Class implements Interface

Interface extends Interface

Class extends Class

One Class → Multiple Interfaces

Interface → Cannot be directly instantiated

Interface Field → public static final

Interface → No Constructor

Interface can contain:
- Abstract methods
- Default methods
- Static methods
- Private methods

Interface Reference:
Interface ref = new Implementation();

Interface
     ↓
Different Implementations
     ↓
Polymorphism

Interface → WHAT
Implementation → HOW

Interface → Loose Coupling
```

---

# 34. Quick Revision

> [!summary] One-Minute Revision

```text
INTERFACE
    ↓
Contract
    ↓
Defines WHAT
    ↓
Classes provide HOW
```

### Remember

- Interface is a reference type.
- It is commonly used for abstraction.
- A class implements an interface using `implements`.
- A class can implement multiple interfaces.
- An interface can extend another interface.
- An interface can extend multiple interfaces.
- An interface cannot be directly instantiated.
- An interface has no constructor.
- Interface fields are implicitly `public static final`.
- Modern interfaces can contain:
  - Abstract methods
  - Default methods
  - Static methods
  - Private methods
- Interface references enable polymorphism.
- Interfaces help achieve loose coupling.
- Interfaces are heavily used in real-world application architecture.
- Interfaces are commonly used with dependency injection.

### OOP Connection

```text
Abstraction
     ↓
Interface
     ↓
Contract
     ↓
Multiple Implementations
     ↓
Polymorphism
     ↓
Loose Coupling
```

### Golden Memory Trick

**An interface is a contract: it tells a class WHAT it must do, while the class decides HOW to do it.**

### One-Line Recognition

**If you see `interface`, `implements`, common contracts, loose coupling, or multiple implementations of the same operation, think Interface.**