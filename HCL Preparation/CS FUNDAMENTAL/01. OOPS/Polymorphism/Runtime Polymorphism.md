---
type: concept
subject: aptitude
topic: "Runtime Polymorphism"
parent: "Polymorphism"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - polymorphism
  - runtime-polymorphism
  - method-overriding
  - dynamic-binding
  - late-binding
  - java
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Polymorphism]]"
  - "[[Compile Time Polymorphism]]"
  - "[[Method Overloading]]"
  - "[[Method Overriding]]"
  - "[[Dynamic Method Dispatch]]"
---

# Runtime Polymorphism

> [!summary]
> **Runtime Polymorphism** is a form of polymorphism where the method that actually executes is determined at runtime based on the **actual object**, rather than only the reference type.
>
> In Java, runtime polymorphism is primarily achieved through **method overriding** and **dynamic method dispatch**.
>
> Core pattern:
>
> ```text
> Parent Reference
>       ↓
> Child Object
>       ↓
> Overridden Method
>       ↓
> Runtime decides
> ```
>
> Fast recognition:
>
> **Overriding → Runtime Polymorphism → Dynamic Binding**

---

# 1. Core Concept

Runtime polymorphism is one of the most important OOP concepts for Java interviews.

Consider:

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

Now:

    Animal a = new Dog();

    a.sound();

The reference type is:

```text
Animal
```

but the actual object is:

```text
Dog
```

The JVM executes:

```text
Dog.sound()
```

not:

```text
Animal.sound()
```

Output:

```text
Bark
```

This is runtime polymorphism.

---

# 2. The Most Important Idea

Remember this:

```text
Reference Type
     ↓
Controls what members are accessible

Actual Object Type
     ↓
Determines overridden method implementation at runtime
```

Example:

    Animal a = new Dog();

Here:

```text
Animal → reference type
Dog    → actual object type
```

For an overridden instance method:

```text
Dog's implementation
```

is selected at runtime.

Therefore:

$$
\boxed{\text{Actual Object Type} \rightarrow \text{Overridden Method Execution}}
$$

---

# 3. Basic Meaning

Runtime polymorphism means:

```text
One reference
+
Different possible objects
+
Same method call
+
Different behavior
```

Example:

    Animal a;

    a = new Dog();
    a.sound();

    a = new Cat();
    a.sound();

The same reference variable:

```text
a
```

can refer to different objects.

The same method call:

```text
a.sound()
```

can produce different behavior.

Output:

```text
Bark
Meow
```

This is the power of runtime polymorphism.

---

# 4. Main Formula

There is no mathematical formula, but the interview recognition formula is:

$$
\boxed{
\text{Parent Reference}
+
\text{Child Object}
+
\text{Overridden Method}
=
\text{Runtime Polymorphism}
}
$$

Another important formula:

$$
\boxed{
\text{Overriding}
\Rightarrow
\text{Dynamic Binding}
\Rightarrow
\text{Runtime Polymorphism}
}
$$

---

# 5. Why Is It Called Runtime Polymorphism?

Look at:

    Animal a = new Dog();

    a.sound();

At compile time, Java knows:

```text
a is an Animal reference
```

But the object created is:

```text
new Dog()
```

The actual overridden implementation is selected dynamically when the method is invoked.

Conceptually:

```text
Compile Time
     ↓
Check whether sound() is accessible
     ↓
Runtime
     ↓
Find actual object's implementation
     ↓
Execute Dog.sound()
```

Therefore:

$$
\boxed{\text{Method Selection for Overriding Happens Dynamically}}
$$

---

# 6. Runtime Polymorphism and Method Overriding

Runtime polymorphism depends primarily on overriding.

Example:

    class Vehicle {

        void start() {
            System.out.println("Vehicle starts");
        }
    }

    class Car extends Vehicle {

        @Override
        void start() {
            System.out.println("Car starts with key");
        }
    }

    class Bike extends Vehicle {

        @Override
        void start() {
            System.out.println("Bike starts with button");
        }
    }

Now:

    Vehicle v1 = new Car();

    Vehicle v2 = new Bike();

    v1.start();

    v2.start();

Output:

```text
Car starts with key
Bike starts with button
```

Same reference type:

```text
Vehicle
```

Different actual objects:

```text
Car
Bike
```

Different runtime behavior.

---

# 7. Parent Reference + Child Object

This is the most important pattern.

Example:

    Animal a = new Dog();

Break it into two parts:

```text
Animal
```

is the reference type.

```text
Dog
```

is the actual object type.

Therefore:

```text
Animal a = new Dog();
```

means:

```text
Reference → Animal
Object    → Dog
```

For overridden instance methods:

```text
Dog implementation
```

is selected.

> [!important]
> **When you see `Parent ref = new Child();`, immediately check for overriding and runtime polymorphism.**

---

# 8. Upcasting

The statement:

    Animal a = new Dog();

is an example of **upcasting**.

Why?

Because:

```text
Dog
  ↓
Animal
```

The child object is being referred to using a parent-class reference.

Conceptually:

```text
Child Object
     ↓
Parent Reference
```

Therefore:

$$
\boxed{\text{Child → Parent Reference} = \text{Upcasting}}
$$

Upcasting is very important for runtime polymorphism.

---

# 9. Why Upcasting Is Useful

Suppose we have:

    class Animal {

        void sound() {
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {
        }
    }

    class Cat extends Animal {

        @Override
        void sound() {
        }
    }

Instead of:

    Dog d = new Dog();

    Cat c = new Cat();

we can use:

    Animal a1 = new Dog();

    Animal a2 = new Cat();

Now the same abstraction:

```text
Animal
```

can represent different concrete implementations.

This makes software more flexible.

---

# 10. Real-Time Example — Payment System

Imagine an application supporting:

```text
Credit Card
UPI
PayPal
Bank Transfer
```

We can define:

    class Payment {

        void pay() {
            System.out.println("Generic payment");
        }
    }

Then:

    class UPI extends Payment {

        @Override
        void pay() {
            System.out.println("Pay using UPI");
        }
    }

    class CreditCard extends Payment {

        @Override
        void pay() {
            System.out.println("Pay using Credit Card");
        }
    }

Now:

    Payment p;

    p = new UPI();
    p.pay();

    p = new CreditCard();
    p.pay();

Output:

```text
Pay using UPI
Pay using Credit Card
```

The caller does not need to know the exact implementation.

---

# 11. Real-Time Example — Notification System

Suppose an application supports:

```text
Email
SMS
Push Notification
```

Parent:

    class Notification {

        void send() {
            System.out.println("Sending notification");
        }
    }

Children:

    class EmailNotification extends Notification {

        @Override
        void send() {
            System.out.println("Sending Email");
        }
    }

    class SMSNotification extends Notification {

        @Override
        void send() {
            System.out.println("Sending SMS");
        }
    }

Now:

    Notification n;

    n = new EmailNotification();
    n.send();

    n = new SMSNotification();
    n.send();

The same method call:

```text
n.send()
```

produces different behavior.

---

# 12. Real-Time Example — Employee System

Suppose an organization has:

```text
Employee
    ↓
Developer
    ↓
Manager
    ↓
Tester
```

Parent:

    class Employee {

        void work() {
            System.out.println("Employee works");
        }
    }

Child:

    class Developer extends Employee {

        @Override
        void work() {
            System.out.println("Developer writes code");
        }
    }

    class Tester extends Employee {

        @Override
        void work() {
            System.out.println("Tester tests software");
        }
    }

Now:

    Employee e1 = new Developer();

    Employee e2 = new Tester();

    e1.work();

    e2.work();

Output:

```text
Developer writes code
Tester tests software
```

The parent reference allows a common interface while runtime determines the actual behavior.

---

# 13. Real-Time Example — Vehicle System

Parent:

    class Vehicle {

        void move() {
            System.out.println("Vehicle moves");
        }
    }

Children:

    class Car extends Vehicle {

        @Override
        void move() {
            System.out.println("Car moves on road");
        }
    }

    class Boat extends Vehicle {

        @Override
        void move() {
            System.out.println("Boat moves on water");
        }
    }

Now:

    Vehicle v1 = new Car();

    Vehicle v2 = new Boat();

    v1.move();

    v2.move();

Output:

```text
Car moves on road
Boat moves on water
```

Same method:

```text
move()
```

Different runtime behavior.

---

# 14. Real-Time Example — Shape System

This is one of the most common OOP examples.

Parent:

    class Shape {

        void draw() {
            System.out.println("Drawing shape");
        }
    }

Children:

    class Circle extends Shape {

        @Override
        void draw() {
            System.out.println("Drawing circle");
        }
    }

    class Rectangle extends Shape {

        @Override
        void draw() {
            System.out.println("Drawing rectangle");
        }
    }

Now:

    Shape s;

    s = new Circle();
    s.draw();

    s = new Rectangle();
    s.draw();

Output:

```text
Drawing circle
Drawing rectangle
```

---

# 15. Real-Time Example — Database Connection

Imagine an application supports:

```text
MySQL
PostgreSQL
Oracle
```

Parent:

    class Database {

        void connect() {
            System.out.println("Connecting");
        }
    }

Children:

    class MySQL extends Database {

        @Override
        void connect() {
            System.out.println("Connecting to MySQL");
        }
    }

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

The application can work with the general abstraction:

```text
Database
```

without hard-coding every implementation.

---

# 16. Real-Time Example — Storage System

Imagine:

```text
Storage
 ├── LocalStorage
 ├── CloudStorage
 └── DatabaseStorage
```

Parent:

    class Storage {

        void save(String data) {
            System.out.println("Saving data");
        }
    }

Child:

    class CloudStorage extends Storage {

        @Override
        void save(String data) {
            System.out.println("Saving to cloud");
        }
    }

Now:

    Storage storage = new CloudStorage();

    storage.save("File");

The caller only depends on:

```text
Storage
```

while the runtime object determines:

```text
CloudStorage.save()
```

---

# 17. Runtime Polymorphism Through Arrays

Runtime polymorphism becomes especially powerful with collections and arrays.

Example:

    class Animal {

        void sound() {
            System.out.println("Animal");
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

Now:

    Animal[] animals = {
        new Dog(),
        new Cat()
    };

    for (Animal a : animals) {
        a.sound();
    }

Output:

```text
Bark
Meow
```

One loop handles multiple child types.

This is a major practical advantage.

---

# 18. Runtime Polymorphism in Methods

A method can accept a parent type and work with different child objects.

Example:

    static void makeSound(Animal animal) {
        animal.sound();
    }

Now:

    makeSound(new Dog());

    makeSound(new Cat());

The same method:

```text
makeSound(Animal)
```

can work with multiple implementations.

This is one of the strongest practical uses of polymorphism.

---

# 19. High-Level Design Pattern

Think:

```text
             Parent
               |
       +-------+-------+
       |               |
     Child A         Child B
       |               |
   behavior A       behavior B
```

Then:

```text
Parent ref = new ChildA();
Parent ref = new ChildB();
```

The caller uses:

```text
Parent interface
```

but runtime executes:

```text
Child behavior
```

---

# 20. Dynamic Method Dispatch

**Dynamic Method Dispatch** is the mechanism through which Java determines the overridden method implementation at runtime.

Example:

    Animal a = new Dog();

    a.sound();

The compile-time reference is:

```text
Animal
```

The runtime object is:

```text
Dog
```

The overridden method:

```text
Dog.sound()
```

is dispatched dynamically.

Therefore:

$$
\boxed{\text{Dynamic Method Dispatch} \rightarrow \text{Runtime Polymorphism}}
$$

Dynamic method dispatch will be studied separately in greater depth.

---

# 21. Static Binding vs Dynamic Binding

This comparison must be memorized.

| Feature | Static Binding | Dynamic Binding |
|---|---|---|
| Decision | Compile time | Runtime |
| Main association | Overloading | Overriding |
| Also called | Early binding | Late binding |
| Based mainly on | Compile-time information | Runtime object |
| Typical methods | Overloaded methods | Overridden instance methods |

Memory:

```text
OVERLOAD → STATIC
OVERRIDE → DYNAMIC
```

---

# 22. Compile-Time Polymorphism vs Runtime Polymorphism

| Feature | Compile Time | Runtime |
|---|---|---|
| Main mechanism | Overloading | Overriding |
| Binding | Static | Dynamic |
| Decision | Compiler | Runtime |
| Inheritance required | No | Yes |
| Parameter list | Different | Same signature |
| Main object concept | Compile-time selection | Runtime object selection |
| Example | `add(int,int)` | `Animal a = new Dog()` |

### Golden Difference

$$
\boxed{\text{Overloading} \rightarrow \text{Compile Time}}
$$

$$
\boxed{\text{Overriding} \rightarrow \text{Runtime}}
$$

---

# 23. Example — Classic Interview Question

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

Then:

    Animal a = new Dog();

    a.sound();

Question:

What is printed?

### Step 1

Reference type:

```text
Animal
```

### Step 2

Actual object:

```text
Dog
```

### Step 3

Check whether `sound()` is overridden.

Yes.

### Step 4

Runtime selects:

```text
Dog.sound()
```

### Answer

```text
Dog
```

---

# 24. Example — Two Different Objects

    class Animal {

        void sound() {
            System.out.println("Animal");
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

Now:

    Animal a1 = new Dog();

    Animal a2 = new Cat();

    a1.sound();

    a2.sound();

Output:

```text
Bark
Meow
```

Recognition:

```text
Same reference type
Different objects
Same method call
Different behavior
```

This is a perfect runtime polymorphism pattern.

---

# 25. Important Rule — Method Must Be Overridden

Consider:

    class Animal {

        void sound() {
            System.out.println("Animal");
        }
    }

    class Dog extends Animal {
    }

Then:

    Animal a = new Dog();

    a.sound();

There is no override in `Dog`.

Therefore the inherited implementation executes:

```text
Animal
```

Runtime polymorphism becomes visible when the child provides an overriding implementation.

---

# 26. Important Rule — Instance Methods

Runtime polymorphism primarily applies to overridable instance methods.

Example:

    Animal a = new Dog();

    a.sound();

where `sound()` is an instance method.

This is different from static methods.

---

# 27. Static Method Trap

Consider:

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

This does not behave like normal overridden instance-method dispatch.

Static methods are associated with the class and are hidden rather than overridden.

The output is:

```text
Parent
```

> [!warning]
> **Do not apply runtime polymorphism rules to static method hiding.**

---

# 28. Field Hiding Trap

Fields do not participate in runtime polymorphism like overridden instance methods.

Example:

    class Parent {

        int value = 10;
    }

    class Child extends Parent {

        int value = 20;
    }

Now:

    Parent p = new Child();

    System.out.println(p.value);

The field access is based on the reference type.

Output:

```text
10
```

This differs from overridden instance methods.

> [!important]
> **Methods can be dynamically dispatched; fields are not dynamically overridden.**

---

# 29. Method vs Field

| Member | Runtime Dispatch? |
|---|---|
| Overridden instance method | Yes |
| Field | No |
| Static method | No dynamic overriding |
| Constructor | No |

This is a very useful interview table.

---

# 30. Private Method Trap

Private methods are not overridden because they are not inherited in the normal overriding sense.

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

These are separate private methods.

This is not runtime overriding.

---

# 31. Final Method Trap

A `final` instance method cannot be overridden.

Example:

    class Parent {

        final void show() {
            System.out.println("Parent");
        }
    }

A child cannot redefine `show()` as an override.

Therefore:

```text
final method
→ cannot be overridden
→ no runtime overriding for that method
```

---

# 32. Constructors and Runtime Polymorphism

Constructors are not overridden.

Example:

    class Parent {

        Parent() {
            System.out.println("Parent constructor");
        }
    }

    class Child extends Parent {

        Child() {
            System.out.println("Child constructor");
        }
    }

Constructors participate in object construction and constructor chaining, not runtime method overriding.

Therefore:

$$
\boxed{\text{Constructors are not polymorphically overridden}}
$$

---

# 33. Covariant Return Type

A child override may return a more specific type than the parent method.

Example:

    class Animal {
    }

    class Dog extends Animal {
    }

    class Parent {

        Animal create() {
            return new Animal();
        }
    }

    class Child extends Parent {

        @Override
        Dog create() {
            return new Dog();
        }
    }

Here:

```text
Animal
```

is the parent return type.

```text
Dog
```

is a subtype of `Animal`.

This is called a **covariant return type**.

It is allowed for overriding methods.

---

# 34. Access Modifier Rule

When overriding a method, a child cannot reduce the visibility of the inherited method.

Example:

    class Parent {

        public void show() {
        }
    }

The child cannot write:

    private void show() {
    }

because:

```text
public → private
```

reduces accessibility.

A child can maintain or increase accessibility where allowed.

Example:

```text
protected → public
```

is allowed.

---

# 35. `@Override` Annotation

Use:

    @Override

Example:

    class Dog extends Animal {

        @Override
        void sound() {
            System.out.println("Bark");
        }
    }

The annotation tells the compiler:

```text
I intend to override a parent method.
```

If the method does not actually override a superclass method, the compiler reports an error.

> [!tip]
> **Always prefer `@Override` when intentionally overriding an instance method.**

---

# 36. Why Runtime Polymorphism Is Powerful

Without runtime polymorphism, code may become tightly coupled.

Example:

    if (paymentType.equals("UPI")) {
        // UPI code
    } else if (paymentType.equals("CARD")) {
        // Card code
    } else if (paymentType.equals("PAYPAL")) {
        // PayPal code
    }

With polymorphism:

    Payment payment;

    payment.pay();

The specific implementation is supplied by the actual object.

This can make code:

- More extensible
- More modular
- Easier to maintain
- Easier to test
- Less tightly coupled

---

# 37. Runtime Polymorphism and Loose Coupling

Suppose:

    void processPayment(Payment payment) {
        payment.pay();
    }

We can pass:

    processPayment(new UPI());

    processPayment(new CreditCard());

    processPayment(new PayPal());

The method does not need to know the concrete implementation.

It only depends on:

```text
Payment
```

This is a major software-design advantage.

---

# 38. Real-Time Example — Food Delivery

Imagine:

```text
Delivery
   |
   +-- BikeDelivery
   |
   +-- CarDelivery
   |
   +-- DroneDelivery
```

Parent:

    class Delivery {

        void deliver() {
            System.out.println("Delivering");
        }
    }

Children override:

    class BikeDelivery extends Delivery {

        @Override
        void deliver() {
            System.out.println("Delivery by bike");
        }
    }

    class DroneDelivery extends Delivery {

        @Override
        void deliver() {
            System.out.println("Delivery by drone");
        }
    }

Now:

    Delivery d = new DroneDelivery();

    d.deliver();

The caller uses:

```text
Delivery
```

while the runtime object provides:

```text
DroneDelivery
```

---

# 39. Real-Time Example — Ride Booking

Imagine:

```text
Ride
 |
 +-- BikeRide
 |
 +-- CarRide
 |
 +-- AutoRide
```

Each class overrides:

    calculateFare()

Then:

    Ride ride = new BikeRide();

    ride.calculateFare();

or:

    ride = new CarRide();

    ride.calculateFare();

Same method call.

Different runtime behavior.

---

# 40. Real-Time Example — Authentication

Imagine:

```text
Authentication
 |
 +-- PasswordAuth
 |
 +-- GoogleAuth
 |
 +-- OTPAuth
```

Parent:

    class Authentication {

        void authenticate() {
            System.out.println("Authenticating");
        }
    }

Each child implements:

```text
authenticate()
```

Now the application can work with:

    Authentication auth;

    auth = new GoogleAuth();

    auth.authenticate();

The implementation is chosen by the runtime object.

---

# 41. Real-Time Example — Report Generation

Imagine:

```text
Report
 |
 +-- PDFReport
 +-- ExcelReport
 +-- CSVReport
```

Parent:

    class Report {

        void generate() {
            System.out.println("Generating report");
        }
    }

Children:

    class PDFReport extends Report {

        @Override
        void generate() {
            System.out.println("Generating PDF");
        }
    }

    class CSVReport extends Report {

        @Override
        void generate() {
            System.out.println("Generating CSV");
        }
    }

Now:

    Report report = new PDFReport();

    report.generate();

Output:

```text
Generating PDF
```

---

# 42. Real-Time Example — Machine Learning Models

A software system might define:

```text
Model
 |
 +-- LinearRegression
 +-- DecisionTree
 +-- NeuralNetwork
```

Each could implement:

    predict()

Then:

    Model model = new DecisionTree();

    model.predict();

The calling code does not need to know the internal prediction algorithm.

The actual object determines the implementation.

This is a useful conceptual example of polymorphic design.

---

# 43. Runtime Polymorphism and Interfaces

Runtime polymorphism is not limited to class inheritance.

Interfaces are extremely important.

Example:

    interface Payment {

        void pay();
    }

    class UPI implements Payment {

        @Override
        public void pay() {
            System.out.println("UPI payment");
        }
    }

    class Card implements Payment {

        @Override
        public void pay() {
            System.out.println("Card payment");
        }
    }

Now:

    Payment p = new UPI();

    p.pay();

Then:

    p = new Card();

    p.pay();

Output:

```text
UPI payment
Card payment
```

This is runtime polymorphism through interface references.

---

# 44. Parent Class vs Interface

Runtime polymorphism can be achieved using:

```text
Parent class reference
+
Child object
```

or:

```text
Interface reference
+
Implementing class object
```

Examples:

    Animal a = new Dog();

and:

    Payment p = new UPI();

Both demonstrate the same broad idea:

```text
General reference
+
Specific implementation
```

---

# 45. Recognition Pattern — Interface

If you see:

    Interface i = new Class();

followed by:

    i.method();

and the class provides the implementation:

Think:

```text
Runtime Polymorphism
```

Example:

    Runnable r = new MyTask();

    r.run();

The runtime object determines the implementation of the overridable instance method.

---

# 46. Upcasting vs Downcasting

### Upcasting

```text
Child → Parent reference
```

Example:

    Animal a = new Dog();

Usually safe when the inheritance relationship exists.

### Downcasting

```text
Parent reference → Child reference
```

Example:

    Dog d = (Dog) a;

This requires an explicit cast and is only valid when the actual object is compatible with the target type.

---

# 47. Downcasting Trap

Consider:

    Animal a = new Cat();

Then:

    Dog d = (Dog) a;

This compiles because the types are in the same inheritance hierarchy, but at runtime the actual object is a `Cat`.

Therefore a:

```text
ClassCastException
```

can occur.

> [!warning]
> **Compile-time cast compatibility does not guarantee runtime object compatibility.**

---

# 48. Safe Downcasting With `instanceof`

Example:

    Animal a = new Dog();

    if (a instanceof Dog) {
        Dog d = (Dog) a;
        d.specialMethod();
    }

The check confirms the runtime object is compatible.

Modern Java also supports pattern matching syntax in suitable language versions, but the core interview concept remains:

```text
Check actual type
↓
Then cast
```

---

# 49. Important Interview Pattern — Parent Reference

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

Then:

    Parent p = new Child();

    p.show();

Recognition:

```text
Parent reference
+
Child object
+
Overridden method
```

Answer:

```text
Child
```

---

# 50. Important Interview Pattern — Child Reference

Now:

    Child c = new Child();

    c.show();

The runtime result is also:

```text
Child
```

But the key runtime-polymorphism pattern becomes particularly important when the reference is generalized:

    Parent p = new Child();

This is where dynamic dispatch is clearly demonstrated.

---

# 51. Important Interview Pattern — No Override

If:

    class Parent {

        void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {
    }

and:

    Parent p = new Child();

    p.show();

There is no child override.

Therefore:

```text
Parent
```

is printed.

Recognition:

```text
No override
→ inherited implementation
```

---

# 52. Important Interview Pattern — Final Method

If:

    class Parent {

        final void show() {
            System.out.println("Parent");
        }
    }

the child cannot override `show()`.

Therefore:

```text
final method
→ no overriding
```

---

# 53. Important Interview Pattern — Private Method

Private methods are not inherited in the normal overriding sense.

Therefore:

```text
private method
→ cannot be overridden
```

If a child declares a private method with the same name, it is not runtime overriding.

---

# 54. Important Interview Pattern — Static Method

Static methods are hidden.

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

    Parent p = new Child();

    p.show();

Output:

```text
Parent
```

This is not dynamic dispatch.

---

# 55. Important Interview Pattern — Field

Consider:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;
    }

    Parent p = new Child();

    System.out.println(p.x);

Output:

```text
10
```

Why?

Fields are not overridden like instance methods.

Field access is resolved based on the reference type.

---

# 56. Method vs Field Trap

Remember:

```text
Overridden instance method
→ Runtime dispatch

Field
→ Reference type

Static method
→ Class-based / hidden

Constructor
→ Construction time
```

This distinction solves many Java output questions.

---

# 57. Runtime Polymorphism Decision Tree

Use this during interviews:

```text
START
  |
  ↓
Parent/Interface reference?
  |
  +-- YES
  |
  ↓
Actual object is child/implementation?
  |
  +-- YES
  |
  ↓
Is the method an overridable instance method?
  |
  +-- YES
  |
  ↓
Is it overridden?
  |
  +-- YES
  |
  ↓
Runtime chooses actual object's implementation
```

If the method is:

```text
static
private
final
```

the normal overriding/dynamic-dispatch rule does not apply.

---

# 58. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Parent reference + child object.

### Pattern 2
Method overriding.

### Pattern 3
Dynamic method dispatch.

### Pattern 4
Upcasting.

### Pattern 5
Interface reference + implementation object.

### Pattern 6
Multiple child objects using one parent reference.

### Pattern 7
Runtime method selection.

### Pattern 8
Static method hiding.

### Pattern 9
Field hiding.

### Pattern 10
Private method trap.

### Pattern 11
Final method trap.

### Pattern 12
Constructor trap.

### Pattern 13
Covariant return type.

### Pattern 14
Access modifier restrictions.

### Pattern 15
Downcasting.

### Pattern 16
`instanceof`.

### Pattern 17
Reference type vs actual object type.

### Pattern 18
Compile-time vs runtime binding.

### Pattern 19
Interface-based polymorphism.

### Pattern 20
Output prediction questions.

---

# 59. Shortcuts

> [!tip]
> **Shortcut 1 — RO**
>
> ```text
> R = Runtime
> O = Overriding
> ```
>
> If you see overriding, immediately check for runtime polymorphism.

---

> [!tip]
> **Shortcut 2 — R-O-A**
>
> Remember:
>
> ```text
> R = Reference
> O = Object
> A = Actual Method
> ```
>
> Example:
>
> ```text
> Animal a = new Dog();
> ```
>
> Reference:
>
> ```text
> Animal
> ```
>
> Object:
>
> ```text
> Dog
> ```
>
> Overridden method:
>
> ```text
> Dog.sound()
> ```

---

> [!tip]
> **Shortcut 3 — Parent Ref, Child Object**
>
> Whenever you see:
>
> ```text
> Parent p = new Child();
> ```
>
> immediately ask:
>
> ```text
> Is there an overridden instance method?
> ```
>
> If yes:
>
> **Runtime polymorphism is likely being tested.**

---

> [!tip]
> **Shortcut 4 — Static/FIP**
>
> Remember:
>
> ```text
> Static → not normal runtime overriding
>
> Field → not dynamic dispatch
>
> Instance overridden method → dynamic dispatch
> ```

---

> [!tip]
> **Shortcut 5 — Final/Private**
>
> ```text
> final method → cannot override
>
> private method → cannot override
> ```

---

> [!tip]
> **Shortcut 6 — Interface**
>
> If you see:
>
> ```text
> Interface i = new Implementation();
> ```
>
> followed by:
>
> ```text
> i.method();
> ```
>
> check for runtime polymorphism.

---

# 60. Advanced Output Question

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

    public class Main {

        public static void main(String[] args) {

            Animal a = new Dog();

            a.sound();
        }
    }

### Recognition

```text
Animal reference
+
Dog object
+
sound() overridden
```

Therefore runtime chooses:

```text
Dog.sound()
```

Output:

```text
Dog
```

---

# 61. Advanced Output Question — Multiple Objects

Consider:

    Animal a;

    a = new Dog();
    a.sound();

    a = new Cat();
    a.sound();

The reference variable remains:

```text
a
```

but the object changes.

First:

```text
Dog
```

Second:

```text
Cat
```

Therefore:

```text
Bark
Meow
```

This demonstrates the flexibility of runtime polymorphism.

---

# 62. Advanced Output Question — Static Method

Consider:

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

    Parent p = new Child();

    p.show();

Do not apply overriding rules.

`show()` is static.

Therefore the call is associated with the reference/class context.

Output:

```text
Parent
```

---

# 63. Advanced Output Question — Field

Consider:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;
    }

    Parent p = new Child();

    System.out.println(p.x);

Output:

```text
10
```

Reason:

```text
Fields are not dynamically dispatched.
```

---

# 64. Advanced Output Question — Parent Method Not Overridden

    class Parent {

        void show() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {
    }

    Parent p = new Child();

    p.show();

There is no child implementation.

Therefore:

```text
Parent
```

---

# 65. Advanced Output Question — Interface

Consider:

    interface Animal {

        void sound();
    }

    class Dog implements Animal {

        public void sound() {
            System.out.println("Bark");
        }
    }

    Animal a = new Dog();

    a.sound();

Reference:

```text
Animal
```

Actual object:

```text
Dog
```

Implementation:

```text
Dog.sound()
```

Output:

```text
Bark
```

---

# 66. Why Runtime Polymorphism Supports Extensibility

Suppose:

    void process(Payment payment) {
        payment.pay();
    }

Today:

    process(new UPI());

Tomorrow:

    process(new CreditCard());

Later:

    process(new PayPal());

The `process()` method itself does not need to know every implementation.

New implementations can be added while keeping the common abstraction.

This is a major object-oriented design advantage.

---

# 67. Runtime Polymorphism and Open/Closed Thinking

Polymorphic design can help software remain:

```text
Open for extension
Closed for unnecessary modification
```

For example:

```text
Payment
 ├── UPI
 ├── Card
 └── PayPal
```

A new payment type can implement the same abstraction.

The client code can continue to call:

```text
payment.pay()
```

This connects runtime polymorphism to good software design and the SOLID principles studied later.

---

# 68. Runtime Polymorphism and Loose Coupling

Tightly coupled:

```text
Client
 ↓
UPI implementation
```

More flexible:

```text
Client
 ↓
Payment abstraction
 ↓
UPI / Card / PayPal
```

The client depends on the abstraction rather than one concrete implementation.

This is one of the most important practical benefits of polymorphism.

---

# 69. Runtime Polymorphism and Dependency Injection

A common software design pattern is:

    class Checkout {

        private Payment payment;

        Checkout(Payment payment) {
            this.payment = payment;
        }

        void completePayment() {
            payment.pay();
        }
    }

Now:

    Checkout c1 = new Checkout(new UPI());

    Checkout c2 = new Checkout(new CreditCard());

Both use the same `Checkout` class.

The runtime object determines which `pay()` implementation executes.

This is a practical example of polymorphism supporting dependency injection.

---

# 70. Runtime Polymorphism and Collections

A collection can hold objects through a common parent type.

Example:

    List<Animal> animals = new ArrayList<>();

    animals.add(new Dog());
    animals.add(new Cat());

    for (Animal animal : animals) {
        animal.sound();
    }

Output:

```text
Bark
Meow
```

The collection does not need separate loops for every child class.

---

# 71. Runtime Polymorphism and Interfaces in Real Applications

A common architecture is:

```text
Interface
    ↓
Implementation A
Implementation B
Implementation C
```

Example:

```text
Payment
    ↓
UPIPayment
CardPayment
WalletPayment
```

Client code:

    Payment payment = new UPIPayment();

    payment.pay();

The client depends on the abstraction.

This makes replacing implementations easier.

---

# 72. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Looking Only at Reference Type

Wrong thinking:

```text
Animal a = new Dog();

a.sound();
```

"Reference is Animal, so Animal.sound() runs."

Correct:

```text
If sound() is overridden,
Dog.sound() runs.
```

---

### Mistake 2 — Applying Runtime Rules to Static Methods

Static methods are hidden, not overridden.

---

### Mistake 3 — Thinking Fields Are Polymorphic

Fields are not dynamically dispatched like overridden instance methods.

---

### Mistake 4 — Thinking Constructors Are Overridden

Constructors cannot be overridden.

---

### Mistake 5 — Forgetting `final`

A final method cannot be overridden.

---

### Mistake 6 — Forgetting `private`

A private method is not overridden in the normal inheritance sense.

---

### Mistake 7 — Confusing Upcasting and Downcasting

```text
Child → Parent
```

is upcasting.

```text
Parent → Child
```

requires explicit downcasting.

---

### Mistake 8 — Assuming Every Parent Reference Means Runtime Polymorphism

Not necessarily.

You need an applicable overridden instance method for dynamic dispatch to matter.

---

### Mistake 9 — Ignoring Actual Object Type

For overridden instance methods:

```text
Parent reference
```

does not erase the importance of the actual runtime object.

---

# 73. Interview Questions

## Beginner Level

### Q1. What is runtime polymorphism?

**Answer:**

Runtime polymorphism is a form of polymorphism where the implementation of an overridden instance method is selected dynamically based on the actual runtime object.

---

### Q2. How is runtime polymorphism achieved in Java?

**Answer:**

Primarily through method overriding, inheritance or interface implementation, and dynamic method dispatch.

---

### Q3. What is dynamic method dispatch?

**Answer:**

It is the runtime mechanism through which Java selects the overridden method implementation corresponding to the actual object.

---

### Q4. What is upcasting?

**Answer:**

Upcasting means referring to a child object using a parent-class reference.

Example:

    Animal a = new Dog();

---

### Q5. What is late binding?

**Answer:**

Late binding means the relevant overridden method implementation is determined dynamically at runtime.

---

# 74. Intermediate Interview Questions

### Q6. What is the difference between compile-time and runtime polymorphism?

**Answer:**

Compile-time polymorphism is primarily achieved through overloading and uses static binding.

Runtime polymorphism is primarily achieved through overriding and uses dynamic binding.

---

### Q7. What happens in `Parent p = new Child();`?

**Answer:**

A parent reference points to a child object. For overridden instance methods, the child's implementation is selected at runtime.

---

### Q8. Can static methods participate in runtime polymorphism?

**Answer:**

No. Static methods are hidden rather than dynamically overridden.

---

### Q9. Are fields polymorphic?

**Answer:**

Fields do not participate in runtime method dispatch. Field access is resolved based on the reference type.

---

### Q10. Can private methods be overridden?

**Answer:**

No. Private methods are not inherited in the normal sense and cannot be overridden.

---

### Q11. Can final methods be overridden?

**Answer:**

No.

---

### Q12. Can constructors be overridden?

**Answer:**

No.

---

# 75. Advanced Interview Questions

### Q13. Why does `Animal a = new Dog(); a.sound();` call `Dog.sound()`?

**Answer:**

Because `sound()` is an overridable instance method and the actual runtime object is a `Dog`. Dynamic dispatch selects the most specific overridden implementation.

---

### Q14. What is the difference between reference type and object type?

**Answer:**

In:

    Animal a = new Dog();

`Animal` is the reference type and `Dog` is the actual object type.

The reference type determines accessible members at compile time, while the actual object type determines the implementation of an overridden instance method at runtime.

---

### Q15. What is dynamic binding?

**Answer:**

Dynamic binding is the runtime association of an overridden method call with the implementation belonging to the actual object.

---

### Q16. Can runtime polymorphism occur through interfaces?

**Answer:**

Yes.

Example:

    Payment p = new UPI();

    p.pay();

The interface reference points to an implementing object.

---

### Q17. What is method hiding?

**Answer:**

Method hiding occurs when a child declares a static method with the same signature as a static method in the parent.

It is not runtime overriding.

---

### Q18. What is field hiding?

**Answer:**

When a child declares a field with the same name as an inherited field, the child field hides the parent field. Field access is not dynamically dispatched like overridden methods.

---

### Q19. What is covariant return type?

**Answer:**

When an overriding child method returns a subtype of the parent method's return type, the return type is called covariant.

---

### Q20. Why is `@Override` recommended?

**Answer:**

It allows the compiler to verify that the method actually overrides a superclass or interface method, reducing accidental mistakes.

---

# 76. High-Level Interview Question

### Question

Why is runtime polymorphism important in real software?

### Strong Answer

> Runtime polymorphism allows client code to work with a common abstraction while different concrete implementations provide their own behavior. A parent or interface reference can point to different objects, and the appropriate overridden method is selected dynamically. This reduces coupling and makes systems easier to extend, maintain, test, and replace.

---

# 77. High-Level Interview Question

### Question

Explain this statement:

    Payment p = new UPI();

### Answer

```text
Payment
↓
Reference type

UPI
↓
Actual object type
```

The `Payment` reference provides access to members available through the abstraction.

If `pay()` is overridden by `UPI`, then:

    p.pay();

executes the `UPI` implementation at runtime.

---

# 78. High-Level Interview Question

### Question

Why doesn't this behave polymorphically?

    Parent p = new Child();

    p.staticMethod();

### Answer

Because static methods belong to the class rather than being dynamically dispatched based on the runtime object. If the child declares a static method with the same signature, it hides the parent method rather than overriding it.

---

# 79. Output Prediction Strategy

For Java output questions involving polymorphism, follow these steps.

```text
STEP 1
Identify reference type.

        ↓

STEP 2
Identify actual object type.

        ↓

STEP 3
Check whether the method is:
instance / static / final / private

        ↓

STEP 4
If instance method,
check whether child overrides it.

        ↓

STEP 5
If overridden:
choose actual object's implementation.

        ↓

STEP 6
If not overridden:
use inherited implementation.

        ↓

STEP 7
For fields/static methods:
do NOT apply normal dynamic method dispatch.
```

---

# 80. Ultimate Recognition Table

| Pattern | Think |
|---|---|
| `Parent p = new Child()` | Upcasting |
| Parent reference + overridden instance method | Runtime polymorphism |
| Same signature in parent and child | Overriding |
| Overriding | Dynamic binding |
| `Interface i = new Implementation()` | Runtime polymorphism candidate |
| Actual object determines instance-method implementation | Dynamic dispatch |
| Static method with same signature | Method hiding |
| Same field name in child | Field hiding |
| `final` method | Cannot override |
| `private` method | Cannot override |
| Constructor | Cannot override |
| `Child → Parent` | Upcasting |
| `Parent → Child` explicit cast | Downcasting |
| Wrong downcast | Possible `ClassCastException` |
| `@Override` | Compiler verifies overriding |
| Child return type is subtype | Covariant return |

---

# 81. Formula Sheet

```text
RUNTIME POLYMORPHISM
=
OVERRIDING
+
DYNAMIC BINDING

Parent Reference
+
Child Object
+
Overridden Instance Method
=
Runtime Polymorphism

Example:
Animal a = new Dog();

Reference Type:
Animal

Actual Object Type:
Dog

Overridden method:
Dog implementation

UPCASTING:
Child object → Parent reference

DOWNCASTING:
Parent reference → Child reference

STATIC METHOD:
Hidden, not overridden

FIELD:
Not dynamically dispatched

PRIVATE METHOD:
Cannot be overridden

FINAL METHOD:
Cannot be overridden

CONSTRUCTOR:
Cannot be overridden

INTERFACE POLYMORPHISM:
Interface reference + implementation object

OVERLOADING:
Compile Time

OVERRIDING:
Runtime

STATIC BINDING:
Compile Time

DYNAMIC BINDING:
Runtime
```

---

# 82. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Runtime polymorphism occurs when an overridden instance method is selected dynamically according to the actual runtime object.**

### Core Pattern

```text
Parent Reference
      +
Child Object
      +
Overridden Method
      ↓
Runtime Polymorphism
```

### Example

    Animal a = new Dog();

    a.sound();

If `Dog` overrides `sound()`:

```text
Dog.sound()
```

executes.

### Main Mechanism

```text
Method Overriding
```

### Binding

```text
Dynamic Binding
Late Binding
Runtime Binding
```

### Upcasting

```text
Dog → Animal reference
```

Example:

    Animal a = new Dog();

### Interface Version

    Payment p = new UPI();

    p.pay();

The implementation is selected according to the runtime object.

### Do Not Confuse

```text
Overloading → Compile Time

Overriding → Runtime

Static methods → Hidden

Fields → Not dynamically dispatched

Private methods → Cannot be overridden

Final methods → Cannot be overridden

Constructors → Cannot be overridden
```

### Most Important Interview Rule

```text
Reference Type
→ Controls accessible members

Actual Object Type
→ Controls overridden instance-method behavior
```

### Golden Memory Trick

**Parent reference tells you what can be called; the actual child object tells you which overridden instance-method implementation runs.**

### One-Line Recognition

**Whenever you see `Parent ref = new Child()` followed by an overridden instance-method call, immediately think Runtime Polymorphism and Dynamic Method Dispatch.**