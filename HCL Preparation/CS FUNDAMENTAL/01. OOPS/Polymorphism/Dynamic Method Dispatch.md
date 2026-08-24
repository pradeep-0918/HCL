---
type: concept
subject: aptitude
topic: "Dynamic Method Dispatch"
parent: "Polymorphism"
company: HCL
difficulty: hard
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - polymorphism
  - runtime-polymorphism
  - dynamic-method-dispatch
  - dynamic-binding
  - late-binding
  - java
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Polymorphism]]"
  - "[[Runtime Polymorphism]]"
  - "[[Method Overriding]]"
  - "[[Compile Time Polymorphism]]"
  - "[[Inheritance]]"
---

# Dynamic Method Dispatch

> [!summary]
> **Dynamic Method Dispatch** is the runtime mechanism through which Java determines which overridden instance method should execute based on the **actual object**, not merely the reference type.
>
> Core pattern:
>
>     Parent reference
>          +
>     Child object
>          +
>     Overridden instance method
>          ↓
>     Runtime checks actual object
>          ↓
>     Child implementation executes
>
> Fast recognition:
>
> **`Parent ref = new Child();` + overridden instance method + method call → Dynamic Method Dispatch**

# 1. Core Concept

Consider:

    class Animal {

        void sound() {
            System.out.println("Animal sound");
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {
            System.out.println("Dog barks");
        }
    }

Now:

    Animal animal = new Dog();

    animal.sound();

There are two important types:

    Reference Type  = Animal
    Object Type     = Dog

At compile time, Java checks whether `Animal` has:

    sound()

Yes.

At runtime, Java asks:

    "What is the actual object?"

The actual object is:

    Dog

Therefore:

    Dog.sound()

executes.

Output:

    Dog barks

This runtime selection is called:

    Dynamic Method Dispatch

# 2. Basic Meaning

Dynamic Method Dispatch means:

    Method call
        ↓
    Runtime
        ↓
    Actual object identified
        ↓
    Most specific overridden implementation selected

It is the mechanism that makes runtime polymorphism work.

Relationship:

    Inheritance
         ↓
    Method Overriding
         ↓
    Dynamic Method Dispatch
         ↓
    Runtime Polymorphism

# 3. Main Formula

The most important conceptual formula is:

$$
\boxed{
\text{Parent Reference}
+
\text{Child Object}
+
\text{Overridden Instance Method}
=
\text{Dynamic Method Dispatch}
}
$$

And:

$$
\boxed{
\text{Dynamic Method Dispatch}
\Rightarrow
\text{Runtime Polymorphism}
}
$$

Another important rule:

$$
\boxed{
\text{Instance Method Selection}
\rightarrow
\text{Actual Object at Runtime}
}
$$

# 4. The Most Important Pattern

Memorize:

    Parent reference = new Child();

Example:

    Animal animal = new Dog();

Then:

    animal.sound();

If `Dog` overrides `sound()`:

    Dog.sound()

executes.

This is the single most important pattern for output-based Java interview questions.

# 5. Reference Type vs Object Type

This distinction is extremely important.

Consider:

    Animal animal = new Dog();

### Reference Type

    Animal

This determines what members are available through the reference at compile time.

### Actual Object Type

    Dog

This determines the implementation of an overridden instance method at runtime.

Remember:

    Reference Type
        ↓
    Compile-Time View

    Actual Object
        ↓
    Runtime Behavior

# 6. Compile Time vs Runtime

Dynamic dispatch involves two stages.

## Stage 1 — Compile Time

Java checks:

    Does Animal have sound()?

If yes, the code is valid.

## Stage 2 — Runtime

Java checks:

    What object does animal actually refer to?

Answer:

    Dog

Therefore:

    Dog.sound()

executes.

This distinction is frequently tested in interviews.

# 7. Basic Example

## Question

What is the output?

    class Animal {

        void sound() {
            System.out.println("Animal");
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {
            System.out.println("Dog");
        }
    }

    public class Main {

        public static void main(String[] args) {

            Animal animal = new Dog();

            animal.sound();
        }
    }

## Step 1

Reference:

    Animal

## Step 2

Actual object:

    Dog

## Step 3

Is `sound()` overridden?

Yes.

## Step 4

Runtime selects:

    Dog.sound()

## Answer

    Dog

# 8. Why Is It Called "Dynamic"?

Because the method implementation is determined dynamically at runtime.

The same reference can point to different objects.

Example:

    Animal animal;

    animal = new Dog();
    animal.sound();

    animal = new Cat();
    animal.sound();

The same method call:

    animal.sound();

can produce different results.

Output:

    Dog
    Cat

The behavior changes according to the runtime object.

# 9. Why Is It Called "Dispatch"?

"Dispatch" means selecting which implementation should execute.

So:

    Dynamic Method Dispatch

means:

    Runtime Selection
    of
    Method Implementation

# 10. Real-Time Example — Payment System

Suppose an application supports multiple payment methods.

    Payment
       |
       +--- UPI
       +--- Card
       +--- Wallet

Parent:

    class Payment {

        void pay() {
            System.out.println("Generic payment");
        }
    }

UPI:

    class UPI extends Payment {

        @Override
        void pay() {
            System.out.println("Payment through UPI");
        }
    }

Card:

    class Card extends Payment {

        @Override
        void pay() {
            System.out.println("Payment through Card");
        }
    }

Wallet:

    class Wallet extends Payment {

        @Override
        void pay() {
            System.out.println("Payment through Wallet");
        }
    }

Now:

    Payment payment;

    payment = new UPI();
    payment.pay();

    payment = new Card();
    payment.pay();

    payment = new Wallet();
    payment.pay();

Output:

    Payment through UPI
    Payment through Card
    Payment through Wallet

The reference remains:

    Payment

but the actual object changes.

Therefore the implementation changes dynamically.

# 11. Real-Time Example — Notification System

Parent:

    class Notification {

        void send() {
            System.out.println("Sending notification");
        }
    }

Email:

    class Email extends Notification {

        @Override
        void send() {
            System.out.println("Sending Email");
        }
    }

SMS:

    class SMS extends Notification {

        @Override
        void send() {
            System.out.println("Sending SMS");
        }
    }

Push:

    class Push extends Notification {

        @Override
        void send() {
            System.out.println("Sending Push Notification");
        }
    }

Now:

    Notification notification;

    notification = new Email();
    notification.send();

    notification = new SMS();
    notification.send();

    notification = new Push();
    notification.send();

Output:

    Sending Email
    Sending SMS
    Sending Push Notification

One reference.

Multiple possible runtime behaviors.

# 12. Real-Time Example — Employee System

Parent:

    class Employee {

        void work() {
            System.out.println("Employee works");
        }
    }

Developer:

    class Developer extends Employee {

        @Override
        void work() {
            System.out.println("Developer writes code");
        }
    }

Tester:

    class Tester extends Employee {

        @Override
        void work() {
            System.out.println("Tester tests software");
        }
    }

Manager:

    class Manager extends Employee {

        @Override
        void work() {
            System.out.println("Manager manages the team");
        }
    }

Now:

    Employee employee;

    employee = new Developer();
    employee.work();

    employee = new Tester();
    employee.work();

    employee = new Manager();
    employee.work();

Output:

    Developer writes code
    Tester tests software
    Manager manages the team

This is dynamic method dispatch.

# 13. Real-Time Example — Vehicle System

Parent:

    class Vehicle {

        void move() {
            System.out.println("Vehicle moves");
        }
    }

Car:

    class Car extends Vehicle {

        @Override
        void move() {
            System.out.println("Car moves on road");
        }
    }

Boat:

    class Boat extends Vehicle {

        @Override
        void move() {
            System.out.println("Boat moves on water");
        }
    }

Airplane:

    class Airplane extends Vehicle {

        @Override
        void move() {
            System.out.println("Airplane moves in air");
        }
    }

Now:

    Vehicle vehicle;

    vehicle = new Car();
    vehicle.move();

    vehicle = new Boat();
    vehicle.move();

    vehicle = new Airplane();
    vehicle.move();

Output:

    Car moves on road
    Boat moves on water
    Airplane moves in air

# 14. Real-Time Example — Database

Parent:

    class Database {

        void connect() {
            System.out.println("Generic database connection");
        }
    }

MySQL:

    class MySQL extends Database {

        @Override
        void connect() {
            System.out.println("Connecting to MySQL");
        }
    }

PostgreSQL:

    class PostgreSQL extends Database {

        @Override
        void connect() {
            System.out.println("Connecting to PostgreSQL");
        }
    }

Now:

    Database db;

    db = new MySQL();
    db.connect();

    db = new PostgreSQL();
    db.connect();

The application can depend on:

    Database

while the actual implementation can change.

# 15. Real-Time Example — Storage

    class Storage {

        void save() {
            System.out.println("Saving data");
        }
    }

    class CloudStorage extends Storage {

        @Override
        void save() {
            System.out.println("Saving to cloud");
        }
    }

    class LocalStorage extends Storage {

        @Override
        void save() {
            System.out.println("Saving locally");
        }
    }

Now:

    Storage storage = new CloudStorage();

    storage.save();

Output:

    Saving to cloud

The client does not need to know the exact implementation.

# 16. Real-Time Example — Ride Booking

Parent:

    class Ride {

        void book() {
            System.out.println("Booking ride");
        }
    }

Bike:

    class BikeRide extends Ride {

        @Override
        void book() {
            System.out.println("Booking bike ride");
        }
    }

Car:

    class CarRide extends Ride {

        @Override
        void book() {
            System.out.println("Booking car ride");
        }
    }

Auto:

    class AutoRide extends Ride {

        @Override
        void book() {
            System.out.println("Booking auto ride");
        }
    }

Now:

    Ride ride = new CarRide();

    ride.book();

Output:

    Booking car ride

# 17. Dynamic Dispatch with Multiple Objects

Consider:

    class Animal {

        void sound() {
            System.out.println("Animal");
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {
            System.out.println("Dog");
        }
    }

    class Cat extends Animal {

        @Override
        void sound() {
            System.out.println("Cat");
        }
    }

Now:

    Animal[] animals = {
        new Dog(),
        new Cat(),
        new Dog()
    };

    for (Animal animal : animals) {
        animal.sound();
    }

Output:

    Dog
    Cat
    Dog

This is a powerful example because the same loop works with different implementations.

# 18. Why This Is Powerful

Without polymorphism, we might write:

    if (type == DOG) {
        dogSound();
    }
    else if (type == CAT) {
        catSound();
    }

With dynamic dispatch:

    animal.sound();

Each object knows how to perform its own behavior.

Therefore:

    Client
      ↓
    Common Parent
      ↓
    Runtime Object
      ↓
    Correct Implementation

# 19. Dynamic Dispatch and Loose Coupling

Suppose a method accepts:

    void processPayment(Payment payment) {
        payment.pay();
    }

Now the method can accept:

    new UPI()
    new Card()
    new Wallet()

Example:

    processPayment(new UPI());

    processPayment(new Card());

    processPayment(new Wallet());

The method does not need:

    if UPI
    if Card
    if Wallet

This reduces coupling.

# 20. High-Level Design Example

A clean architecture may look like:

    Payment
       |
       +-------------+-------------+
       |             |             |
      UPI           Card         Wallet
       |             |             |
      pay()         pay()         pay()

Client:

    Payment payment = getPaymentMethod();

    payment.pay();

The client knows:

    Payment

The client does not need to know the internal implementation.

This is one of the major benefits of polymorphism.

# 21. Method Selection Rules

For normal overridden instance methods:

    Actual Object
          ↓
    Determines Implementation

Example:

    Parent p = new Child();

    p.show();

If `Child` overrides `show()`:

    Child.show()

executes.

# 22. Important Exception — Static Methods

Static methods do not participate in dynamic method dispatch.

Example:

    class Parent {

        static void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        static void show() {
            System.out.println("Child");
        }
    }

Now:

    Parent p = new Child();

    p.show();

Output:

    Parent

Why?

Static method selection is based on the reference/class context rather than runtime object dispatch.

This is called:

    Method Hiding

# 23. Important Exception — Fields

Fields are not dynamically dispatched.

Example:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;
    }

    Parent p = new Child();

    System.out.println(p.x);

Output:

    10

Therefore:

    Instance Method
    → Dynamic Dispatch

    Field
    → Reference Type

# 24. Important Exception — Private Methods

Private methods cannot be overridden.

Therefore dynamic dispatch does not apply to them as overridden methods.

Example:

    class Parent {

        private void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        private void show() {
            System.out.println("Child");
        }
    }

These are separate methods.

# 25. Important Exception — Final Methods

A final method cannot be overridden.

Therefore:

    final method
         ↓
    no child override
         ↓
    no runtime selection between parent/child overrides

# 26. `super` and Dynamic Dispatch

Consider:

    class Parent {

        void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        @Override
        void show() {
            System.out.println("Child");

            super.show();
        }
    }

Now:

    Parent p = new Child();

    p.show();

Output:

    Child
    Parent

Why?

Normal call:

    p.show()

uses dynamic dispatch and selects:

    Child.show()

Inside `Child.show()`:

    super.show()

explicitly selects:

    Parent.show()

Important distinction:

    p.show()
    → Dynamic dispatch

    super.show()
    → Explicit parent call

# 27. Dynamic Dispatch vs `super`

| Call | Selection |
|---|---|
| `p.show()` | Runtime object |
| `this.show()` | Current object's overridden behavior |
| `super.show()` | Parent implementation |
| `Parent.show()` for static context | Class-based |
| `p.field` | Reference type |
| `p.staticMethod()` | Class/reference-based, not dynamic |

# 28. Dynamic Dispatch with Multilevel Inheritance

Consider:

    class A {

        void show() {
            System.out.println("A");
        }
    }

    class B extends A {

        @Override
        void show() {
            System.out.println("B");
        }
    }

    class C extends B {

        @Override
        void show() {
            System.out.println("C");
        }
    }

Now:

    A obj = new C();

    obj.show();

Runtime object:

    C

Therefore:

    C.show()

Output:

    C

The runtime chooses the most specific applicable implementation.

# 29. Multilevel Dispatch with `super`

    class A {

        void show() {
            System.out.println("A");
        }
    }

    class B extends A {

        @Override
        void show() {
            super.show();
            System.out.println("B");
        }
    }

    class C extends B {

        @Override
        void show() {
            super.show();
            System.out.println("C");
        }
    }

    A obj = new C();

    obj.show();

Execution:

    C.show()
       ↓
    B.show()
       ↓
    A.show()

Output:

    A
    B
    C

# 30. Dynamic Dispatch Through a Method Parameter

Consider:

    class Animal {

        void sound() {
            System.out.println("Animal");
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {
            System.out.println("Dog");
        }
    }

    class Cat extends Animal {

        @Override
        void sound() {
            System.out.println("Cat");
        }
    }

    static void makeSound(Animal animal) {

        animal.sound();
    }

Now:

    makeSound(new Dog());

    makeSound(new Cat());

Output:

    Dog
    Cat

The method accepts one general type:

    Animal

but runtime dispatch selects the correct implementation.

# 31. Dynamic Dispatch Through Collections

Consider:

    List<Animal> animals = new ArrayList<>();

    animals.add(new Dog());
    animals.add(new Cat());

    for (Animal animal : animals) {
        animal.sound();
    }

Output:

    Dog
    Cat

This is very common in real applications.

Collections often store parent/interface references while containing different concrete objects.

# 32. Interface-Based Dynamic Dispatch

Dynamic dispatch is not limited to class inheritance.

Example:

    interface Payment {

        void pay();
    }

    class UPI implements Payment {

        @Override
        public void pay() {
            System.out.println("UPI");
        }
    }

    class Card implements Payment {

        @Override
        public void pay() {
            System.out.println("Card");
        }
    }

Now:

    Payment payment = new UPI();

    payment.pay();

Output:

    UPI

Change:

    payment = new Card();

    payment.pay();

Output:

    Card

The reference is:

    Payment

The runtime object determines the implementation.

# 33. Interface Example — Notification

    interface Notification {

        void send();
    }

    class Email implements Notification {

        @Override
        public void send() {
            System.out.println("Email");
        }
    }

    class SMS implements Notification {

        @Override
        public void send() {
            System.out.println("SMS");
        }
    }

Now:

    Notification notification = new Email();

    notification.send();

Output:

    Email

Then:

    notification = new SMS();

    notification.send();

Output:

    SMS

# 34. Abstract Class Example

    abstract class Shape {

        abstract void draw();
    }

    class Circle extends Shape {

        @Override
        void draw() {
            System.out.println("Circle");
        }
    }

    class Rectangle extends Shape {

        @Override
        void draw() {
            System.out.println("Rectangle");
        }
    }

Now:

    Shape shape = new Circle();

    shape.draw();

Output:

    Circle

Then:

    shape = new Rectangle();

    shape.draw();

Output:

    Rectangle

# 35. Dynamic Dispatch vs Compile-Time Binding

| Feature | Compile-Time Binding | Dynamic Dispatch |
|---|---|---|
| Decision time | Compile time | Runtime |
| Main idea | Compiler determines target | Runtime determines target |
| Common example | Overloading | Overriding |
| Actual object important | Usually no | Yes |
| Instance overridden method | No | Yes |
| Static methods | Class-based | Not dynamic |
| Polymorphism | Compile-time | Runtime |

# 36. Dynamic Dispatch vs Method Overriding

These concepts are related but not identical.

### Method Overriding

Describes the relationship between methods.

    Parent.show()
    Child.show()

Same signature, different implementation.

### Dynamic Method Dispatch

Describes what happens when calling the method through a polymorphic reference.

    Parent p = new Child();

    p.show();

Therefore:

    Overriding
    → Creates alternative implementations

    Dynamic Dispatch
    → Selects the correct implementation at runtime

# 37. Dynamic Dispatch vs Runtime Polymorphism

These terms are closely connected.

    Method Overriding
          ↓
    Dynamic Method Dispatch
          ↓
    Runtime Polymorphism

Think:

    Overriding
    = Method relationship

    Dynamic Dispatch
    = Runtime selection mechanism

    Runtime Polymorphism
    = Resulting OOP behavior

# 38. Advanced Output Question

Consider:

    class Parent {

        void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        @Override
        void show() {
            System.out.println("Child");
        }
    }

    class GrandChild extends Child {

        @Override
        void show() {
            System.out.println("GrandChild");
        }
    }

Now:

    Parent p = new GrandChild();

    p.show();

### Identification

Reference:

    Parent

Actual object:

    GrandChild

Most specific override:

    GrandChild.show()

### Answer

    GrandChild

# 39. Advanced Output Question — Different References

Consider:

    Parent p1 = new Parent();

    Parent p2 = new Child();

    Child c = new Child();

Assume `Child` overrides `show()`.

Then:

    p1.show();

uses:

    Parent.show()

because actual object is `Parent`.

But:

    p2.show();

uses:

    Child.show()

because actual object is `Child`.

And:

    c.show();

uses:

    Child.show()

because both reference and object are `Child`.

# 40. Advanced Output Question — Same Reference, Different Objects

    Animal animal;

    animal = new Dog();

    animal.sound();

    animal = new Cat();

    animal.sound();

Output:

    Dog
    Cat

Important:

The variable did not change its declared type.

Only the object it refers to changed.

# 41. Advanced Output Question — Array

Consider:

    Animal[] animals = {
        new Dog(),
        new Cat(),
        new Dog()
    };

    for (Animal animal : animals) {
        animal.sound();
    }

Output:

    Dog
    Cat
    Dog

Pattern:

    One Parent Type
        +
    Multiple Child Objects
        +
    Overridden Method
        ↓
    Dynamic Dispatch

# 42. Advanced Output Question — `super`

Consider:

    class Parent {

        void show() {
            System.out.println("P");
        }
    }

    class Child extends Parent {

        @Override
        void show() {
            System.out.println("C");
            super.show();
        }
    }

    Parent p = new Child();

    p.show();

Execution:

    p.show()
       ↓
    Child.show()
       ↓
    print C
       ↓
    super.show()
       ↓
    Parent.show()
       ↓
    print P

Output:

    C
    P

# 43. Advanced Output Question — Field + Method

Consider:

    class Parent {

        int x = 10;

        void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        int x = 20;

        @Override
        void show() {
            System.out.println("Child");
        }
    }

    Parent p = new Child();

    System.out.println(p.x);

    p.show();

Output:

    10
    Child

Memory:

    Field
    → Reference Type

    Overridden Instance Method
    → Actual Object

# 44. Advanced Output Question — Static + Instance

    class Parent {

        static void test() {
            System.out.println("Parent Static");
        }

        void show() {
            System.out.println("Parent Instance");
        }
    }

    class Child extends Parent {

        static void test() {
            System.out.println("Child Static");
        }

        @Override
        void show() {
            System.out.println("Child Instance");
        }
    }

    Parent p = new Child();

    p.test();

    p.show();

Output:

    Parent Static
    Child Instance

This is one of the most important interview traps.

# 45. Pattern Recognition

> [!important]
> **Pattern 1 — `Parent ref = new Child()`**
>
> If you see:
>
>     Parent p = new Child();
>
> immediately check for overridden instance methods.

> [!important]
> **Pattern 2 — Same Method Call**
>
> If:
>
>     p.show();
>
> appears with different runtime objects, expect different implementations.

> [!important]
> **Pattern 3 — `@Override`**
>
> If the child contains:
>
>     @Override
>
> the method is intended to participate in overriding.

> [!important]
> **Pattern 4 — Interface Reference**
>
> If you see:
>
>     Interface i = new Implementation();
>
> and the implementation provides the method:
>
> think:
>
> **Runtime polymorphism / dynamic dispatch**

> [!important]
> **Pattern 5 — Array or Collection of Parent Type**
>
> If you see:
>
>     Animal[] animals
>
> containing:
>
>     new Dog()
>     new Cat()
>
> and then:
>
>     animal.sound()
>
> think:
>
> **Dynamic Dispatch**

> [!important]
> **Pattern 6 — Static**
>
> If the method is static:
>
> do not apply normal dynamic dispatch.

> [!important]
> **Pattern 7 — Field**
>
> If the question accesses:
>
>     object.variable
>
> remember:
>
> **Field selection follows reference type, not overridden-method dispatch.**

> [!important]
> **Pattern 8 — `super.method()`**
>
> Think:
>
> **Explicit parent implementation**

# 46. Shortcuts

> [!tip]
> **Shortcut 1 — R-O-R**
>
>     Reference
>       ↓
>     Object
>       ↓
>     Runtime
>
> For:
>
>     Parent p = new Child();
>
> remember:
>
> **Reference checks availability, Object decides overridden behavior.**

> [!tip]
> **Shortcut 2 — A-D-R**
>
>     Actual
>     ↓
>     Dispatch
>     ↓
>     Runtime
>
> Actual object → Runtime dispatch.

> [!tip]
> **Shortcut 3 — Parent Reference Does Not Mean Parent Method**
>
> Never memorize:
>
>     Parent reference → Parent implementation
>
> Instead memorize:
>
>     Parent reference
>     +
>     Child object
>     +
>     overridden instance method
>     →
>     Child implementation

> [!tip]
> **Shortcut 4 — Same Variable, Different Objects**
>
> If you see:
>
>     Animal a = new Dog();
>     a.sound();
>
>     a = new Cat();
>     a.sound();
>
> expect:
>
>     Dog
>     Cat
>
> assuming both override `sound()`.

> [!tip]
> **Shortcut 5 — Static/Field Trap**
>
> Memorize:
>
>     Method → Object
>     Field  → Reference
>     Static → Class/Reference Context

> [!tip]
> **Shortcut 6 — `super`**
>
>     normal overridden call
>     → runtime object
>
>     super.method()
>     → parent implementation

# 47. Common Exam Patterns

> [!important] Must Master

1. `Parent p = new Child()`
2. Method overriding
3. Runtime polymorphism
4. Dynamic binding
5. Late binding
6. Upcasting
7. Interface reference
8. Abstract class reference
9. Parent reference with multiple child objects
10. Array of parent references
11. Collection of parent references
12. Method parameter using parent type
13. Multilevel inheritance
14. Most specific override
15. `super.method()`
16. Static method hiding
17. Field hiding
18. Private methods
19. Final methods
20. Output prediction
21. Reference type vs object type
22. Compile-time availability vs runtime implementation

# 48. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Reference Type Always Determines Method

Wrong:

    Parent p = new Child();

    p.show();

"Parent method must execute."

Correct:

    Check whether Child overrides show().

If yes:

    Child.show()

executes.

---

### Mistake 2 — Applying Dynamic Dispatch to Static Methods

Static methods are not dynamically dispatched.

---

### Mistake 3 — Applying Dynamic Dispatch to Fields

Fields are not overridden.

---

### Mistake 4 — Forgetting Actual Object

Always identify:

    new ______()

That is the actual runtime object.

---

### Mistake 5 — Confusing Overriding and Overloading

Different parameter list:

    Overloading

Same signature + child implementation:

    Overriding

---

### Mistake 6 — Forgetting `super`

`super.method()` explicitly calls the parent implementation.

---

### Mistake 7 — Assuming Every Parent Reference Uses Dynamic Dispatch

Dynamic dispatch applies to overridden instance methods.

It does not apply to:

    static methods
    fields
    private methods
    final methods

in the same way.

---

### Mistake 8 — Ignoring Multilevel Inheritance

If:

    A → B → C

and all override the same method, an object of `C` normally uses the most specific override:

    C.method()

# 49. Interview Questions

## Beginner

### Q1. What is Dynamic Method Dispatch?

**Answer:**

Dynamic Method Dispatch is the runtime mechanism that selects the implementation of an overridden instance method based on the actual object.

### Q2. When does dynamic method dispatch occur?

**Answer:**

It occurs when an overridden instance method is invoked through a parent class or interface reference that refers to a child/concrete implementation object.

### Q3. What type of polymorphism uses dynamic method dispatch?

**Answer:**

Runtime polymorphism.

### Q4. What is late binding?

**Answer:**

Late binding means the implementation of an overridden instance method is determined at runtime rather than compile time.

### Q5. What is dynamic binding?

**Answer:**

Dynamic binding is another term for runtime method resolution of overridden instance methods.

# 50. Intermediate Interview Questions

### Q6. What happens here?

    Animal animal = new Dog();

    animal.sound();

**Answer:**

The compiler verifies that `Animal` provides `sound()`. At runtime, because the actual object is `Dog`, the overridden `Dog.sound()` implementation executes.

### Q7. Does the reference type matter?

**Answer:**

Yes. The reference type determines which members can be accessed at compile time. However, for overridden instance methods, the actual runtime object determines which implementation executes.

### Q8. Are static methods dynamically dispatched?

**Answer:**

No. Static methods are hidden rather than overridden.

### Q9. Are fields dynamically dispatched?

**Answer:**

No. Field access is based on the reference type.

### Q10. What is the difference between overriding and dynamic dispatch?

**Answer:**

Overriding is the child defining a new implementation of an inherited method. Dynamic dispatch is the runtime mechanism that chooses which overridden implementation executes.

# 51. Advanced Interview Questions

### Q11. Why is dynamic method dispatch important?

**Answer:**

It allows a program to work with general parent or interface types while automatically executing the appropriate concrete implementation at runtime. This supports extensibility, loose coupling, and runtime polymorphism.

### Q12. Explain `Parent p = new Child()`.

**Answer:**

The reference is of type `Parent`, while the actual object is `Child`. This is upcasting. If `Child` overrides an instance method, a call through `p` is dynamically dispatched to the child implementation.

### Q13. What does the compiler determine and what does the runtime determine?

**Answer:**

The compiler checks whether the reference type provides the requested accessible method. At runtime, dynamic dispatch selects the implementation based on the actual object for overridden instance methods.

### Q14. What is the role of the actual object?

**Answer:**

The actual object determines which overridden instance-method implementation executes.

### Q15. What happens in multilevel inheritance?

**Answer:**

If a class hierarchy contains multiple overrides, runtime dispatch selects the most specific applicable implementation belonging to the actual object.

# 52. High-Level Interview Question

### Question

Explain dynamic method dispatch using a real-world example.

### Strong Answer

Consider a payment system with a common `Payment` abstraction and implementations such as `UPI`, `Card`, and `Wallet`. A variable can be declared as `Payment`, while the actual object can be any concrete payment implementation. When `pay()` is called, runtime dispatch selects the implementation corresponding to the actual object. This allows the application to use a common interface while supporting different payment behaviors.

# 53. High-Level Interview Question

### Question

Why does Java need dynamic dispatch?

### Strong Answer

Dynamic dispatch allows code to depend on abstractions rather than concrete implementations. A parent or interface reference can work with many concrete objects, and the appropriate behavior is selected automatically at runtime. This improves flexibility, extensibility, maintainability, and supports runtime polymorphism.

# 54. High-Level Interview Question

### Question

Why is dynamic dispatch associated with loose coupling?

### Strong Answer

Because the client can depend on a parent class or interface instead of directly depending on a concrete child class. New implementations can often be introduced without changing the client logic, as long as they follow the same contract.

# 55. Ultimate Recognition Framework

When solving an interview question, use this exact sequence:

    STEP 1
    Find the reference type.

         ↓

    STEP 2
    Find the actual object after new.

         ↓

    STEP 3
    Check whether the method is an instance method.

         ↓

    STEP 4
    Check whether the child overrides it.

         ↓

    STEP 5
    If overridden:
    choose the implementation of the actual object.

         ↓

    STEP 6
    If super.method() appears:
    execute parent implementation.

         ↓

    STEP 7
    If static:
    do not use dynamic dispatch.

         ↓

    STEP 8
    If field:
    use reference-type field.

         ↓

    STEP 9
    If multilevel:
    choose the most specific override.

# 56. Master Decision Table

| Question Pattern | Correct Thinking |
|---|---|
| `Parent p = new Child()` | Upcasting |
| `p.overriddenMethod()` | Dynamic dispatch |
| Actual object = Child | Child implementation |
| Method not overridden | Inherited parent implementation |
| `super.method()` | Parent implementation |
| Static method | Method hiding |
| Field | Reference type |
| Private method | No overriding |
| Final method | No overriding |
| Different parameters | Overloading |
| Same signature in child | Overriding |
| Interface reference + implementation object | Runtime polymorphism |
| Abstract reference + concrete object | Runtime polymorphism |
| Multiple child objects | Dynamic dispatch |
| Multilevel inheritance | Most specific override |

# 57. Formula Sheet

```text
DYNAMIC METHOD DISPATCH

Parent Reference
+
Child Object
+
Overridden Instance Method
=
Dynamic Method Dispatch

Dynamic Method Dispatch
→ Runtime Method Selection
→ Runtime Polymorphism
→ Dynamic Binding
→ Late Binding

Example:

Parent p = new Child();

p.show();

If Child overrides show():

Child.show()

Reference Type
→ Compile-Time Accessibility

Actual Object Type
→ Runtime Implementation

Method Overriding
→ Same Signature + Child Implementation

Overloading
→ Different Parameters + Compile-Time Selection

super.method()
→ Explicit Parent Implementation

static method
→ No Dynamic Dispatch

field
→ No Dynamic Dispatch

private method
→ Cannot Be Overridden

final method
→ Cannot Be Overridden
```

# 58. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Dynamic Method Dispatch is the runtime mechanism that selects the overridden instance method based on the actual object.**

### Core Pattern

    Parent p = new Child();

    p.show();

If `Child` overrides `show()`:

    Child.show()

executes.

### Three Things to Check

    1. Reference Type
    2. Actual Object Type
    3. Whether Method Is Overridden

### Golden Rule

    Reference Type
    → What can I access?

    Actual Object
    → Which overridden implementation runs?

### Runtime Flow

    Parent Reference
          ↓

  - java
  - interview    Child Object
          ↓
    Method Call
          ↓
    Runtime Checks Object
          ↓
    Child Override Executes

### Important Exceptions

    static
    → not dynamically dispatched

    field
    → reference type

    private
    → cannot be overridden

    final
    → cannot be overridden

    super.method()
    → parent implementation

### Most Important Interview Pattern

    Parent p = new Child();

    p.show();

If `show()` is overridden:

    Child.show()

### Golden Memory Trick

**Reference tells Java what method is available; the actual object tells Java which overridden instance implementation should run.**

### One-Line Recognition

**Whenever you see `Parent reference = new Child()` followed by an overridden instance-method call, think Dynamic Method Dispatch → Runtime Polymorphism.**