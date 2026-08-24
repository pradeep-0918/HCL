---
type: concept
subject: aptitude
topic: "Multilevel Inheritance"
parent: "Inheritance"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - inheritance
  - multilevel-inheritance
  - java
  - object-oriented-programming
wikilinks:
  - "[[OOP Basics]]"
  - "[[Inheritance]]"
  - "[[Single Inheritance]]"
  - "[[Hierarchical Inheritance]]"
  - "[[Polymorphism]]"
  - "[[super Keyword]]"
---

# Multilevel Inheritance

> [!summary]
> **Multilevel Inheritance** occurs when a class inherits from another class, and a third class inherits from that child class, forming an inheritance chain.
>
> The basic structure is:
>
> ```text
> Grandparent
>      ↓
>    Parent
>      ↓
>    Child
> ```
>
> In Java, multilevel inheritance is created using the `extends` keyword.

---

# 1. Core Concept

The easiest way to understand multilevel inheritance is:

$$
\boxed{A \rightarrow B \rightarrow C}
$$

Where:

```text
A = Grandparent
B = Parent
C = Child
```

For example:

```text
Animal
   ↓
Mammal
   ↓
Dog
```

Here:

```text
Animal → Parent of Mammal
Mammal → Child of Animal
Mammal → Parent of Dog
Dog    → Child of Mammal
```

Therefore, `Dog` indirectly inherits accessible features from `Animal` through `Mammal`.

### Java Example

    class Animal {

        void eat() {
            System.out.println("Eating");
        }
    }

    class Mammal extends Animal {

        void walk() {
            System.out.println("Walking");
        }
    }

    class Dog extends Mammal {

        void bark() {
            System.out.println("Barking");
        }
    }

Now:

    Dog d = new Dog();

    d.eat();
    d.walk();
    d.bark();

The `Dog` object can access:

```text
eat()  → Animal
walk() → Mammal
bark() → Dog
```

Output:

```text
Eating
Walking
Barking
```

> [!important]
> **Multilevel inheritance = inheritance through multiple levels.**

---

# 2. Basic Meaning

In multilevel inheritance, each class acts as both:

- A child of the previous class
- A parent of the next class

Example:

```text
        Animal
           ↓
        Mammal
           ↓
          Dog
```

Relationships:

```text
Mammal IS-A Animal
Dog IS-A Mammal
Dog IS-AN Animal
```

The last relationship is important.

Because `Dog` indirectly inherits from `Animal`, `Dog` can be considered a specialized form of `Animal`.

---

# 3. Main Formula

There is no mathematical formula for multilevel inheritance.

For aptitude and interviews, remember:

$$
\boxed{A \rightarrow B \rightarrow C}
$$

or:

$$
\boxed{\text{Grandparent} \rightarrow \text{Parent} \rightarrow \text{Child}}
$$

The child receives accessible inherited behavior through the inheritance chain.

Conceptually:

$$
\boxed{
C =
\text{Own Features}
+
\text{Inherited from B}
+
\text{Inherited from A}
}
$$

Subject to Java's access-control rules.

---

# 4. Visual Structure

## Basic Multilevel Structure

```text
        A
        |
        ↓
        B
        |
        ↓
        C
```

## Real Example

```text
       Vehicle
          |
          ↓
        Car
          |
          ↓
      ElectricCar
```

Here:

```text
Vehicle → Car
Car     → ElectricCar
```

Therefore:

```text
ElectricCar
      ↓
inherits from Car
      ↓
Car inherits from Vehicle
```

---

# 5. Real-Time Example 1 — Animal → Mammal → Dog

This is one of the easiest examples.

```text
Animal
   ↓
Mammal
   ↓
Dog
```

### Level 1 — Animal

    class Animal {

        void eat() {
            System.out.println("Eating");
        }
    }

### Level 2 — Mammal

    class Mammal extends Animal {

        void walk() {
            System.out.println("Walking");
        }
    }

### Level 3 — Dog

    class Dog extends Mammal {

        void bark() {
            System.out.println("Barking");
        }
    }

Now:

    Dog d = new Dog();

    d.eat();
    d.walk();
    d.bark();

The `Dog` object can use:

```text
Animal → eat()
Mammal → walk()
Dog → bark()
```

### Key Idea

```text
Dog
 ↓
Mammal
 ↓
Animal
```

The child can access accessible behavior inherited through the chain.

---

# 6. Real-Time Example 2 — Vehicle → Car → ElectricCar

This is a very practical software example.

```text
Vehicle
   ↓
Car
   ↓
ElectricCar
```

### Vehicle

    class Vehicle {

        void start() {
            System.out.println("Vehicle starts");
        }
    }

### Car

    class Car extends Vehicle {

        void drive() {
            System.out.println("Car is driving");
        }
    }

### ElectricCar

    class ElectricCar extends Car {

        void charge() {
            System.out.println("Charging battery");
        }
    }

Now:

    ElectricCar car = new ElectricCar();

    car.start();
    car.drive();
    car.charge();

The object can use:

```text
start()  → Vehicle
drive()  → Car
charge() → ElectricCar
```

### Real-World Interpretation

```text
Vehicle
→ General transportation behavior

Car
→ Vehicle + car-specific behavior

ElectricCar
→ Car + electric-specific behavior
```

Each level becomes more specialized.

---

# 7. Real-Time Example 3 — Employee → Developer → SeniorDeveloper

Consider a company hierarchy.

```text
Employee
    ↓
Developer
    ↓
SeniorDeveloper
```

### Employee

    class Employee {

        void login() {
            System.out.println("Employee login");
        }
    }

### Developer

    class Developer extends Employee {

        void writeCode() {
            System.out.println("Writing code");
        }
    }

### SeniorDeveloper

    class SeniorDeveloper extends Developer {

        void reviewCode() {
            System.out.println("Reviewing code");
        }
    }

Now:

    SeniorDeveloper s = new SeniorDeveloper();

    s.login();
    s.writeCode();
    s.reviewCode();

The senior developer gets:

```text
login()       → Employee
writeCode()   → Developer
reviewCode()  → SeniorDeveloper
```

This demonstrates specialization through multiple levels.

---

# 8. Real-Time Example 4 — Account → BankAccount → SavingsAccount

Consider a banking hierarchy.

```text
Account
   ↓
BankAccount
   ↓
SavingsAccount
```

### Account

    class Account {

        String accountNumber;

        void displayAccount() {
            System.out.println(accountNumber);
        }
    }

### BankAccount

    class BankAccount extends Account {

        double balance;

        void deposit(double amount) {
            balance += amount;
        }
    }

### SavingsAccount

    class SavingsAccount extends BankAccount {

        void addInterest() {
            balance += balance * 0.05;
        }
    }

A `SavingsAccount` can use accessible functionality from both higher levels.

```text
Account
  ↓
BankAccount
  ↓
SavingsAccount
```

---

# 9. Real-Time Example 5 — User → Customer → PremiumCustomer

Consider an e-commerce application.

```text
User
 ↓
Customer
 ↓
PremiumCustomer
```

### User

    class User {

        void login() {
            System.out.println("Login");
        }

        void logout() {
            System.out.println("Logout");
        }
    }

### Customer

    class Customer extends User {

        void placeOrder() {
            System.out.println("Order placed");
        }
    }

### PremiumCustomer

    class PremiumCustomer extends Customer {

        void getPremiumDiscount() {
            System.out.println("Premium discount");
        }
    }

Now:

    PremiumCustomer customer = new PremiumCustomer();

    customer.login();
    customer.placeOrder();
    customer.getPremiumDiscount();

The premium customer receives functionality from all appropriate levels.

---

# 10. Real-Time Example 6 — Device → Computer → Laptop

```text
Device
   ↓
Computer
   ↓
Laptop
```

### Device

    class Device {

        void powerOn() {
            System.out.println("Power ON");
        }
    }

### Computer

    class Computer extends Device {

        void processData() {
            System.out.println("Processing data");
        }
    }

### Laptop

    class Laptop extends Computer {

        void carry() {
            System.out.println("Laptop is portable");
        }
    }

The laptop is:

```text
Laptop
  ↓
Computer
  ↓
Device
```

It receives functionality through the hierarchy.

---

# 11. Real-Time Example 7 — Organization Hierarchy

Consider:

```text
Person
   ↓
Employee
   ↓
Manager
```

A person has:

```text
name
age
```

An employee has:

```text
employeeId
salary
```

A manager has:

```text
teamSize
manageTeam()
```

This can model increasing specialization:

```text
Person
  ↓
Employee
  ↓
Manager
```

---

# 12. Why Multilevel Inheritance Is Useful

Multilevel inheritance is useful when classes naturally become more specialized step by step.

For example:

```text
Vehicle
   ↓
Car
   ↓
ElectricCar
```

Instead of putting everything into one class:

```text
Vehicle:
    start()
    drive()
    charge()
```

we can organize behavior according to specialization.

```text
Vehicle
    ↓
General vehicle behavior

Car
    ↓
Car-specific behavior

ElectricCar
    ↓
Electric-specific behavior
```

### Benefits

- Code reuse
- Logical hierarchy
- Specialization
- Reduced duplication
- Supports polymorphism
- Easier conceptual modeling when the hierarchy is natural

---

# 13. Important Properties

## 13.1 Multiple Levels Exist

The defining characteristic is:

```text
A → B → C
```

At least three levels are commonly used to illustrate multilevel inheritance.

---

## 13.2 Each Class Can Have Its Own Members

Example:

    class A {

        void methodA() {
        }
    }

    class B extends A {

        void methodB() {
        }
    }

    class C extends B {

        void methodC() {
        }
    }

Each class can define its own functionality.

```text
A → methodA()
B → methodB()
C → methodC()
```

---

## 13.3 Lower-Level Classes Can Access Inherited Accessible Members

A `C` object can access accessible members inherited from `B` and `A`.

Example:

    C obj = new C();

    obj.methodA();
    obj.methodB();
    obj.methodC();

---

## 13.4 The Child Becomes More Specialized

The hierarchy usually moves from:

```text
General
  ↓
More specific
  ↓
Very specific
```

Example:

```text
Vehicle
  ↓
Car
  ↓
ElectricCar
```

---

## 13.5 Method Overriding Can Occur at Any Level

Example:

    class Animal {

        void sound() {
            System.out.println("Animal");
        }
    }

    class Mammal extends Animal {

        @Override
        void sound() {
            System.out.println("Mammal");
        }
    }

    class Dog extends Mammal {

        @Override
        void sound() {
            System.out.println("Dog");
        }
    }

Now:

    Dog d = new Dog();

    d.sound();

Output:

```text
Dog
```

The most specific overridden implementation is used for the actual object.

---

# 14. Multilevel Inheritance and `super`

The `super` keyword refers to the immediate parent context.

Example:

    class A {

        void show() {
            System.out.println("A");
        }
    }

    class B extends A {

        void showB() {
            super.show();
            System.out.println("B");
        }
    }

    class C extends B {

        void showC() {
            super.showB();
            System.out.println("C");
        }
    }

Here:

```text
C → super → B
B → super → A
```

### Important

`super` refers to the **immediate parent**, not directly to any ancestor you choose.

> [!important]
> **super = immediate parent**

---

# 15. Constructor Execution in Multilevel Inheritance

This is a very common output-based interview question.

Consider:

    class A {

        A() {
            System.out.println("A");
        }
    }

    class B extends A {

        B() {
            System.out.println("B");
        }
    }

    class C extends B {

        C() {
            System.out.println("C");
        }
    }

Now:

    C obj = new C();

What happens?

### Execution Order

```text
C object creation
      ↓
A constructor
      ↓
B constructor
      ↓
C constructor
```

Output:

```text
A
B
C
```

Therefore:

$$
\boxed{\text{Grandparent Constructor} \rightarrow \text{Parent Constructor} \rightarrow \text{Child Constructor}}
$$

---

# 16. Why Does the Parent Constructor Execute First?

When creating a child object, Java must initialize the parent portion of the object before initializing the child-specific portion.

Conceptually:

```text
Initialize A
   ↓
Initialize B
   ↓
Initialize C
```

Therefore, constructors execute from the top of the inheritance hierarchy toward the actual class being instantiated.

---

# 17. Constructor Example With `super()`

Consider:

    class A {

        A() {
            System.out.println("A constructor");
        }
    }

    class B extends A {

        B() {
            super();
            System.out.println("B constructor");
        }
    }

    class C extends B {

        C() {
            super();
            System.out.println("C constructor");
        }
    }

Creating:

    C obj = new C();

Output:

```text
A constructor
B constructor
C constructor
```

The parent constructor is executed before the child constructor.

---

# 18. Method Overriding in Multilevel Inheritance

Consider:

    class A {

        void display() {
            System.out.println("A");
        }
    }

    class B extends A {

        @Override
        void display() {
            System.out.println("B");
        }
    }

    class C extends B {

        @Override
        void display() {
            System.out.println("C");
        }
    }

Now:

    C obj = new C();

    obj.display();

Output:

```text
C
```

Because `C` provides the most specific override.

---

# 19. Parent Reference and Multilevel Polymorphism

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

What is the output?

### Analyze

Reference type:

```text
A
```

Actual object:

```text
C
```

Overridden method:

```text
C.show()
```

Therefore:

```text
C
```

$$
\boxed{\text{C}}
$$

This is a classic runtime polymorphism question.

---

# 20. Multilevel Inheritance and Polymorphism

Inheritance creates the relationship:

```text
A
↓
B
↓
C
```

Polymorphism allows a parent reference to refer to a child object.

Example:

    A obj = new C();

If `show()` is overridden at multiple levels, runtime dispatch selects the appropriate implementation.

Therefore:

$$
\boxed{\text{Inheritance + Overriding} \rightarrow \text{Runtime Polymorphism}}
$$

---

# 21. Multilevel vs Single Inheritance

This is one of the most important distinctions.

## Single Inheritance

```text
A
|
↓
B
```

There is one direct inheritance level.

## Multilevel Inheritance

```text
A
|
↓
B
|
↓
C
```

There are multiple inheritance levels.

| Feature | Single | Multilevel |
|---|---|---|
| Structure | A → B | A → B → C |
| Levels | One parent-child level | Multiple levels |
| Example | Animal → Dog | Animal → Mammal → Dog |
| Complexity | Lower | Higher |

> [!tip]
> If you see **A → B → C**, immediately think **Multilevel Inheritance**.

---

# 22. Multilevel vs Hierarchical Inheritance

## Multilevel

```text
A
|
B
|
C
```

## Hierarchical

```text
    A
   / \
  B   C
```

### Recognition

```text
Vertical chain → Multilevel
Branches from one parent → Hierarchical
```

| Multilevel | Hierarchical |
|---|---|
| A → B → C | A → B and A → C |
| Chain | Branch |
| Multiple levels | Multiple children |

---

# 23. Multilevel vs Multiple Inheritance

These terms sound similar but are completely different.

### Multilevel

```text
A
↓
B
↓
C
```

A class inherits through levels.

### Multiple

```text
A   B
 \ /
  C
```

A class has multiple parents.

Java does not support multiple inheritance of classes.

But Java supports multilevel inheritance.

> [!important]
> **Multilevel ≠ Multiple**

---

# 24. Java Support

Java supports multilevel inheritance.

Example:

    class A {
    }

    class B extends A {
    }

    class C extends B {
    }

This is valid.

Therefore:

$$
\boxed{\text{Java supports multilevel inheritance}}
$$

---

# 25. Access Control Through the Chain

Consider:

    class A {

        private int a = 10;
        protected int b = 20;
        public int c = 30;
    }

    class B extends A {
    }

    class C extends B {

        void show() {
            System.out.println(b);
            System.out.println(c);
        }
    }

`C` can access the appropriate inherited members based on Java's access rules.

But:

```text
private a
```

cannot be directly accessed from `C`.

> [!warning]
> Never assume that every field from every ancestor is directly accessible.

Access modifiers still apply at every level.

---

# 26. Real-World Architecture Example

Consider an application with:

```text
Payment
   ↓
OnlinePayment
   ↓
UPIPayment
```

The levels can represent increasing specialization.

```text
Payment
→ Common payment concept

OnlinePayment
→ Online-specific behavior

UPIPayment
→ UPI-specific behavior
```

Example:

    class Payment {

        void process() {
            System.out.println("Processing payment");
        }
    }

    class OnlinePayment extends Payment {

        void authenticate() {
            System.out.println("Authenticating");
        }
    }

    class UPIPayment extends OnlinePayment {

        void verifyUPI() {
            System.out.println("Verifying UPI");
        }
    }

This demonstrates specialization.

---

# 27. Real-Time Example — Educational System

Consider:

```text
Person
   ↓
Student
   ↓
EngineeringStudent
```

### Person

```text
name
age
```

### Student

```text
rollNumber
study()
```

### EngineeringStudent

```text
branch
code()
```

Hierarchy:

```text
Person
   ↓
Student
   ↓
EngineeringStudent
```

The lower-level class becomes increasingly specialized.

---

# 28. Real-Time Example — Banking System

Consider:

```text
Account
   ↓
BankAccount
   ↓
CurrentAccount
```

Possible responsibilities:

```text
Account
→ account number
→ account holder

BankAccount
→ deposit()
→ withdraw()

CurrentAccount
→ overdraft()
```

This allows each level to contain logically related functionality.

---

# 29. Real-Time Example — Technology

Consider:

```text
Device
   ↓
Computer
   ↓
GamingLaptop
```

```text
Device
→ powerOn()

Computer
→ process()

GamingLaptop
→ runGame()
```

The hierarchy moves from general to specialized.

---

# 30. Real-Time Example — Company Roles

Consider:

```text
Employee
   ↓
Developer
   ↓
SeniorDeveloper
```

Common:

```text
login()
logout()
```

Developer-specific:

```text
writeCode()
```

Senior-specific:

```text
reviewCode()
mentor()
```

The model represents increasing responsibility.

---

# 31. When Should You Use Multilevel Inheritance?

Use it when:

### 1. There is a genuine hierarchy

```text
Animal → Mammal → Dog
```

### 2. Each level adds specialization

```text
Vehicle → Car → ElectricCar
```

### 3. The inheritance chain remains understandable

A hierarchy should not become unnecessarily deep.

### 4. The IS-A relationship remains true at every level

For:

```text
Animal → Mammal → Dog
```

we have:

```text
Mammal IS-A Animal
Dog IS-A Mammal
Dog IS-AN Animal
```

---

# 32. When Should You Avoid Deep Inheritance?

Very deep inheritance can create:

- Tight coupling
- Difficult debugging
- Complex dependencies
- Fragile designs
- Hard-to-understand class hierarchies

Example:

```text
A
↓
B
↓
C
↓
D
↓
E
↓
F
↓
G
```

This can become difficult to maintain.

> [!warning]
> **Inheritance should represent a meaningful relationship, not just a desire to reuse code.**

In many designs, composition can provide more flexibility.

---

# 33. Shortcuts

> [!tip]
> **Shortcut 1 — The Chain Rule**
>
> If you see:
>
> ```text
> A → B → C
> ```
>
> immediately think:
>
> **Multilevel Inheritance**

> [!tip]
> **Shortcut 2 — Vertical = Multilevel**
>
> ```text
> A
> ↓
> B
> ↓
> C
> ```
>
> Vertical chain → Multilevel.

> [!tip]
> **Shortcut 3 — Branch = Hierarchical**
>
> ```text
>     A
>    / \
>   B   C
> ```
>
> Branching → Hierarchical.

> [!tip]
> **Shortcut 4 — Multiple Parents**
>
> ```text
> A   B
> \   /
>   C
> ```
>
> Multiple parents → Multiple inheritance.

> [!tip]
> **Shortcut 5 — Constructor Order**
>
> For:
>
> ```text
> A → B → C
> ```
>
> creating `C` executes:
>
> ```text
> A constructor
> B constructor
> C constructor
> ```

> [!tip]
> **Shortcut 6 — `super`**
>
> `super` always refers to the **immediate parent context**.

> [!tip]
> **Shortcut 7 — Runtime Override**
>
> If:
>
> ```text
> A → B → C
> ```
>
> and all override the same method, a `C` object normally uses `C`'s implementation for an overridden instance method.

---

# 34. Recognition Tricks

### Pattern 1 — Three-Level Chain

> [!important]
> If you see:
>
> ```text
> A
> ↓
> B
> ↓
> C
> ```
>
> Think:
>
> **Multilevel Inheritance**

---

### Pattern 2 — Grandparent / Parent / Child

> [!important]
> If the question contains:
>
> **Grandparent → Parent → Child**
>
> Think:
>
> **Multilevel Inheritance**

---

### Pattern 3 — `extends` Chain

> [!important]
> If you see:
>
> ```java
> class B extends A
> class C extends B
> ```
>
> Think:
>
> **Multilevel Inheritance**

---

### Pattern 4 — Constructor Output

> [!important]
> If the question asks constructor execution in:
>
> ```text
> A → B → C
> ```
>
> Think:
>
> **A → B → C**

---

### Pattern 5 — Parent Reference

> [!important]
> If you see:
>
> ```java
> A obj = new C();
> ```
>
> check:
>
> 1. Actual object
> 2. Overridden method
> 3. Runtime dispatch

---

### Pattern 6 — Vertical vs Horizontal

> [!important]
> Remember:
>
> ```text
> Vertical chain → Multilevel
> Horizontal branches → Hierarchical
> Multiple parents → Multiple
> ```

---

# 35. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Identify multilevel inheritance from a diagram.

### Pattern 2
Identify grandparent, parent, and child.

### Pattern 3
Understand the `extends` chain.

### Pattern 4
Trace inherited methods across multiple levels.

### Pattern 5
Trace constructor execution order.

### Pattern 6
Understand `super` in multilevel inheritance.

### Pattern 7
Trace method overriding across multiple levels.

### Pattern 8
Solve parent-reference output questions.

### Pattern 9
Differentiate single, multilevel, and hierarchical inheritance.

### Pattern 10
Differentiate multilevel and multiple inheritance.

### Pattern 11
Understand IS-A relationships at multiple levels.

### Pattern 12
Understand access modifiers across inheritance levels.

### Pattern 13
Identify Java's support for multilevel inheritance.

### Pattern 14
Identify runtime polymorphism in a multilevel hierarchy.

### Pattern 15
Recognize real-world hierarchical designs.

---

# 36. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing Multilevel With Multiple

```text
A → B → C
```

is multilevel.

```text
A   B
 \ /
  C
```

is multiple.

---

### Mistake 2 — Confusing Multilevel With Hierarchical

```text
A
↓
B
↓
C
```

is multilevel.

```text
A
├── B
└── C
```

is hierarchical.

---

### Mistake 3 — Thinking `super` Can Directly Access Any Ancestor

`super` refers to the immediate parent context.

---

### Mistake 4 — Forgetting Constructor Order

For:

```text
A → B → C
```

creating `C` normally results in:

```text
A constructor
B constructor
C constructor
```

---

### Mistake 5 — Thinking Constructors Are Inherited

They are not.

They are invoked as part of object initialization.

---

### Mistake 6 — Ignoring Access Modifiers

A private member of `A` cannot simply be accessed directly from `C`.

---

### Mistake 7 — Creating Unnecessarily Deep Hierarchies

Deep inheritance can make code difficult to maintain.

---

### Mistake 8 — Assuming Inheritance Is Always Better Than Composition

Inheritance should represent a genuine IS-A relationship.

---

# 37. Interview Questions

## Beginner Level

### Q1. What is multilevel inheritance?

**Answer:**

Multilevel inheritance is an inheritance structure where a class inherits from another class, and another class inherits from that child, forming a chain such as:

```text
A → B → C
```

---

### Q2. Does Java support multilevel inheritance?

**Answer:**

Yes. Java supports multilevel inheritance between classes.

Example:

    class A {
    }

    class B extends A {
    }

    class C extends B {
    }

---

### Q3. What is the basic structure of multilevel inheritance?

**Answer:**

```text
Grandparent
     ↓
Parent
     ↓
Child
```

---

### Q4. Which keyword is used?

**Answer:**

`extends`.

---

### Q5. What is inherited through multiple levels?

**Answer:**

A lower-level subclass can access accessible inherited members from its ancestors according to Java's access-control rules.

---

## Intermediate Level

### Q6. What is the difference between single and multilevel inheritance?

**Answer:**

Single inheritance has one direct parent-child relationship:

```text
A → B
```

Multilevel inheritance has a chain:

```text
A → B → C
```

---

### Q7. What is the difference between multilevel and hierarchical inheritance?

**Answer:**

Multilevel forms a chain:

```text
A → B → C
```

Hierarchical inheritance has multiple children from one parent:

```text
    A
   / \
  B   C
```

---

### Q8. What happens when a child object is created in multilevel inheritance?

**Answer:**

Constructors execute from the highest superclass toward the actual child class.

For:

```text
A → B → C
```

creating `C` executes:

```text
A constructor
B constructor
C constructor
```

---

### Q9. What does `super` refer to?

**Answer:**

`super` refers to the immediate parent-class context.

---

### Q10. Can a child override a method inherited through multiple levels?

**Answer:**

Yes. A subclass can override an inherited instance method, subject to Java's overriding rules.

---

## Advanced Level

### Q11. What happens here?

    A obj = new C();

If `A → B → C` and all override `show()`?

**Answer:**

If `show()` is an overridden instance method, runtime dispatch uses the implementation corresponding to the actual object, `C`.

---

### Q12. Why can deep inheritance be problematic?

**Answer:**

Deep hierarchies can increase coupling and make behavior harder to understand, test, and maintain.

---

### Q13. Is multilevel inheritance the same as multiple inheritance?

**Answer:**

No.

```text
Multilevel:
A → B → C

Multiple:
A   B
 \ /
  C
```

---

### Q14. Can multilevel inheritance involve an abstract class?

**Answer:**

Yes.

Example:

    abstract class A {
        abstract void show();
    }

    class B extends A {

        void show() {
            System.out.println("B");
        }
    }

    class C extends B {
    }

---

### Q15. Can an interface participate in a multilevel hierarchy?

**Answer:**

Yes. Interfaces can extend other interfaces, and classes can implement interfaces. However, the terminology and inheritance relationships should be described accurately.

---

# 38. Output-Based Interview Questions

## Question 1

What is the output?

    class A {

        A() {
            System.out.println("A");
        }
    }

    class B extends A {

        B() {
            System.out.println("B");
        }
    }

    class C extends B {

        C() {
            System.out.println("C");
        }
    }

    public class Main {

        public static void main(String[] args) {

            new C();
        }
    }

### Recognition

```text
C creation
↓
A constructor
↓
B constructor
↓
C constructor
```

### Answer

```text
A
B
C
```

---

## Question 2

What is the output?

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

    public class Main {

        public static void main(String[] args) {

            A obj = new C();

            obj.show();
        }
    }

### Recognition

```text
Reference → A
Object → C
Method overridden → C
```

### Answer

```text
C
```

---

## Question 3

What is the output?

    class A {

        int x = 10;
    }

    class B extends A {

        int x = 20;
    }

    class C extends B {

        int x = 30;

        void show() {
            System.out.println(x);
            System.out.println(super.x);
        }
    }

    public class Main {

        public static void main(String[] args) {

            C obj = new C();

            obj.show();
        }
    }

### Recognition

```text
x       → C.x
super.x → B.x
```

### Answer

```text
30
20
```

> [!important]
> `super` refers to the immediate parent level, which is `B`.

---

# 39. Formula Sheet

```text
Multilevel Inheritance
= Multiple inheritance levels in a chain

Basic Structure:
A → B → C

A = Grandparent
B = Parent
C = Child

Java:
class B extends A {
}

class C extends B {
}

Child Features:
= Own Features
+ Accessible Features inherited from Parent
+ Accessible Features inherited through Ancestors

Constructor Order:
Grandparent
↓
Parent
↓
Child

super
→ Immediate Parent

Single:
A → B

Multilevel:
A → B → C

Hierarchical:
A → B
A → C

Multiple:
A   B
 \ /
  C

IS-A:
Dog IS-A Animal

HAS-A:
Car HAS-A Engine

Runtime Polymorphism:
Parent Reference → Child Object
```

# 40. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Multilevel inheritance is an inheritance chain where one class inherits from another class, and a further class inherits from that class.**

### Visual

```text
Grandparent
     ↓
   Parent
     ↓
   Child
```

### Java Example

    class A {
    }

    class B extends A {
    }

    class C extends B {
    }

### Remember

- Multilevel inheritance forms a chain.
- The common structure is `A → B → C`.
- Java supports multilevel inheritance.
- `extends` creates class inheritance.
- A child can access accessible inherited members through the chain.
- Constructors are not inherited.
- Parent constructors execute before child constructors.
- `super` refers to the immediate parent.
- Method overriding can occur at multiple levels.
- Multilevel inheritance can support runtime polymorphism.
- Single inheritance = `A → B`.
- Multilevel inheritance = `A → B → C`.
- Hierarchical inheritance = `A → B` and `A → C`.
- Multiple inheritance = one class with multiple parent classes.
- Java does not support multiple inheritance of classes.
- Java supports multiple interfaces.
- Use inheritance for genuine IS-A relationships.
- Avoid unnecessarily deep inheritance hierarchies.

### High-Level Mental Model

```text
General
   ↓
More Specific
   ↓
Highly Specific
```

Example:

```text
Vehicle
   ↓
Car
   ↓
ElectricCar
```

### Golden Memory Trick

**Multilevel inheritance is a vertical chain: Grandparent → Parent → Child.**

### One-Line Recognition

**Whenever you see `A extends B` and `B extends C` forming a chain, think Multilevel Inheritance.**