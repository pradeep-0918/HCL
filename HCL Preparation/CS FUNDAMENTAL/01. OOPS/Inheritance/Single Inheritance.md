---
type: concept
subject: aptitude
topic: "Single Inheritance"
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
  - single-inheritance
  - java
  - object-oriented-programming
wikilinks:
  - "[[OOP Basics]]"
  - "[[Inheritance]]"
  - "[[Multilevel Inheritance]]"
  - "[[Hierarchical Inheritance]]"
  - "[[Polymorphism]]"
  - "[[super Keyword]]"
---

# Single Inheritance

> [!summary]
> **Single Inheritance** is an inheritance relationship in which **one child class inherits properties and behaviors from exactly one parent class**.
>
> In Java, single inheritance is achieved using the `extends` keyword.

## 1. Core Concept

The simplest way to understand inheritance is:

$$
\boxed{\text{Child Class} \rightarrow \text{inherits from} \rightarrow \text{Parent Class}}
$$

In single inheritance:

```text
        Parent
           |
           ↓
         Child
```

There is:

```text
1 Parent
1 Child
1 Direct inheritance relationship
```

### Basic Java Example

    public class Animal {

        void eat() {
            System.out.println("Animal eats");
        }
    }

    public class Dog extends Animal {

        void bark() {
            System.out.println("Dog barks");
        }
    }

Here:

```text
Animal → Parent / Superclass
Dog    → Child / Subclass
```

`Dog` automatically gets access to the inherited `eat()` behavior.

Therefore:

    Dog d = new Dog();

    d.eat();
    d.bark();

Output:

```text
Animal eats
Dog barks
```

> [!important]
> **Single Inheritance = One parent → One child**

---

# 2. Basic Meaning

Inheritance allows one class to acquire accessible properties and behaviors of another class.

The existing class is called:

```text
Parent
Superclass
Base class
```

The new class is called:

```text
Child
Subclass
Derived class
```

### Syntax

    class Parent {
        // fields
        // methods
    }

    class Child extends Parent {
        // additional fields
        // additional methods
    }

The keyword:

    extends

creates the inheritance relationship.

---

# 3. Real-Time Understanding

Think about a real-world relationship:

```text
Vehicle
   |
   ↓
Car
```

A car is a type of vehicle.

A vehicle may have:

```text
start()
stop()
```

A car may additionally have:

```text
openTrunk()
```

So:

```text
Vehicle
   ├── start()
   └── stop()
        ↓
      Car
   └── openTrunk()
```

The child gets common functionality from the parent and can add its own specialized functionality.

---

# 4. Main Formula

There is no mathematical formula for inheritance.

For placement interviews, remember:

$$
\boxed{\text{Child} = \text{Inherited Features} + \text{New Features}}
$$

For single inheritance:

$$
\boxed{1\text{ Parent} \rightarrow 1\text{ Direct Child}}
$$

Another important relationship:

$$
\boxed{\text{Child IS-A Parent}}
$$

Example:

```text
Dog IS-A Animal
Car IS-A Vehicle
Manager IS-A Employee
Circle IS-A Shape
```

---

# 5. Why Do We Need Inheritance?

Inheritance is mainly useful for:

- Code reuse
- Extending existing functionality
- Creating logical class hierarchies
- Reducing duplication
- Supporting polymorphism
- Representing IS-A relationships

### Without Inheritance

Suppose:

    class Car {

        void start() {
            System.out.println("Starting");
        }

        void stop() {
            System.out.println("Stopping");
        }

        void drive() {
            System.out.println("Driving");
        }
    }

    class Bike {

        void start() {
            System.out.println("Starting");
        }

        void stop() {
            System.out.println("Stopping");
        }

        void ride() {
            System.out.println("Riding");
        }
    }

There is duplicated code:

```text
Car  → start(), stop()
Bike → start(), stop()
```

With inheritance:

    class Vehicle {

        void start() {
            System.out.println("Starting");
        }

        void stop() {
            System.out.println("Stopping");
        }
    }

    class Car extends Vehicle {

        void drive() {
            System.out.println("Driving");
        }
    }

    class Bike extends Vehicle {

        void ride() {
            System.out.println("Riding");
        }
    }

Common behavior can be placed in the parent.

---

# 6. Real-Time Example 1 — Animal and Dog

A classic inheritance example:

```text
Animal
   |
   ↓
Dog
```

Parent:

    class Animal {

        void eat() {
            System.out.println("Eating");
        }
    }

Child:

    class Dog extends Animal {

        void bark() {
            System.out.println("Barking");
        }
    }

Now:

    Dog dog = new Dog();

    dog.eat();
    dog.bark();

The `Dog` object can use:

```text
Inherited:
eat()

Own:
bark()
```

### Key Idea

> [!important]
> The child class does not need to rewrite functionality that it inherits from the parent.

---

# 7. Real-Time Example 2 — Vehicle and Car

```text
Vehicle
   |
   ↓
Car
```

Parent:

    class Vehicle {

        void start() {
            System.out.println("Vehicle starts");
        }

        void stop() {
            System.out.println("Vehicle stops");
        }
    }

Child:

    class Car extends Vehicle {

        void openTrunk() {
            System.out.println("Trunk opened");
        }
    }

The car gets:

```text
start()
stop()
```

and adds:

```text
openTrunk()
```

This is a natural IS-A relationship:

$$
\boxed{\text{Car IS-A Vehicle}}
$$

---

# 8. Real-Time Example 3 — Employee and Manager

Consider an organization.

```text
Employee
   |
   ↓
Manager
```

An employee may have:

```text
name
salary
work()
```

A manager may additionally have:

```text
manageTeam()
```

Example:

    class Employee {

        String name;
        double salary;

        void work() {
            System.out.println("Employee is working");
        }
    }

    class Manager extends Employee {

        void manageTeam() {
            System.out.println("Managing team");
        }
    }

Now:

    Manager m = new Manager();

    m.work();
    m.manageTeam();

The manager inherits common employee functionality and adds specialized behavior.

---

# 9. Real-Time Example 4 — Account and SavingsAccount

Banking systems often have different account types.

```text
BankAccount
     |
     ↓
SavingsAccount
```

Parent:

    class BankAccount {

        double balance;

        void deposit(double amount) {
            balance += amount;
        }

        void displayBalance() {
            System.out.println(balance);
        }
    }

Child:

    class SavingsAccount extends BankAccount {

        void addInterest() {
            balance += balance * 0.05;
        }
    }

Now:

    SavingsAccount account = new SavingsAccount();

    account.deposit(10000);
    account.addInterest();
    account.displayBalance();

The child reuses the parent's account functionality.

---

# 10. Real-Time Example 5 — Shape and Circle

```text
Shape
  |
  ↓
Circle
```

Parent:

    class Shape {

        void display() {
            System.out.println("This is a shape");
        }
    }

Child:

    class Circle extends Shape {

        double radius;

        double area() {
            return Math.PI * radius * radius;
        }
    }

The circle inherits:

```text
display()
```

and provides:

```text
area()
```

This is another example of:

$$
\boxed{\text{Circle IS-A Shape}}
$$

---

# 11. Real-Time Example 6 — User and Admin

Consider an application with users.

```text
User
 |
 ↓
Admin
```

Parent:

    class User {

        String username;

        void login() {
            System.out.println("User logged in");
        }

        void logout() {
            System.out.println("User logged out");
        }
    }

Child:

    class Admin extends User {

        void deleteUser() {
            System.out.println("User deleted");
        }
    }

Admin gets:

```text
login()
logout()
```

and adds:

```text
deleteUser()
```

---

# 12. Real-Time Example 7 — Device and Smartphone

```text
Device
   |
   ↓
Smartphone
```

Parent:

    class Device {

        void powerOn() {
            System.out.println("Device powered on");
        }
    }

Child:

    class Smartphone extends Device {

        void makeCall() {
            System.out.println("Calling");
        }

        void takePhoto() {
            System.out.println("Taking photo");
        }
    }

The smartphone inherits the common device functionality.

---

# 13. Structure of Single Inheritance

The structure is always:

```text
             Parent
                |
                |
                ↓
             Child
```

Example:

```text
       Vehicle
          |
          ↓
         Car
```

Not:

```text
Vehicle
  |
  +---- Car
  |
  +---- Bike
```

That structure contains multiple children and represents **hierarchical inheritance**, not single inheritance.

> [!important]
> For single inheritance questions, look for exactly **one direct parent-child relationship**.

---

# 14. Important Terminology

| Term | Meaning |
|---|---|
| Parent Class | Class being inherited from |
| Superclass | Another name for parent class |
| Base Class | Another name for parent class |
| Child Class | Class that inherits |
| Subclass | Another name for child class |
| Derived Class | Another name for child class |
| `extends` | Keyword used for class inheritance |
| IS-A | Inheritance relationship |

Example:

    class Dog extends Animal {
    }

Therefore:

```text
Animal → Parent / Superclass / Base
Dog    → Child / Subclass / Derived
```

---

# 15. What Does the Child Inherit?

A child class can use accessible members of the parent.

For example:

    class Parent {

        int x;

        void display() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        void show() {
            System.out.println(x);
            display();
        }
    }

The child can access the inherited members according to Java's access-control rules.

### Important

Do not say:

> "A child inherits everything from the parent."

That is too broad.

For example:

- `private` members are not directly accessible in the child.
- Constructors are not inherited.
- Static members belong to the class, although they can be accessed through an inherited context.
- Access depends on modifiers and package relationships.

---

# 16. Access Modifiers and Inheritance

Consider:

    class Parent {

        private int a;
        int b;
        protected int c;
        public int d;
    }

A child class does not have direct access to `private` member `a`.

The other members may be accessible depending on the access rules.

### Basic Placement View

| Modifier | Directly accessible in subclass? |
|---|---|
| `private` | No |
| default/package-private | Yes, within same package |
| `protected` | Yes, subject to Java's protected rules |
| `public` | Yes |

> [!important]
> **Private members are not directly accessible in a subclass.**

They may still exist as part of the parent portion of the object and can be accessed indirectly through suitable parent methods.

---

# 17. Constructor and Inheritance

A common interview trap:

> [!warning]
> **Constructors are not inherited.**

Consider:

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

Creating:

    Child c = new Child();

Output:

```text
Parent constructor
Child constructor
```

Why?

When a child object is created, the parent constructor is executed as part of object initialization.

But the constructor itself is not inherited as a child constructor.

---

# 18. `super` and Single Inheritance

The `super` keyword refers to the immediate parent-class context.

Example:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void display() {
            System.out.println(super.x);
        }
    }

Output:

```text
10
```

Here:

```text
x       → Child's variable
super.x → Parent's variable
```

### Calling Parent Method

    class Parent {

        void display() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        void displayChild() {
            super.display();
            System.out.println("Child");
        }
    }

`super.display()` calls the parent method.

---

# 19. Method Overriding and Single Inheritance

Single inheritance also creates the foundation for runtime polymorphism.

Parent:

    class Animal {

        void sound() {
            System.out.println("Animal sound");
        }
    }

Child:

    class Dog extends Animal {

        @Override
        void sound() {
            System.out.println("Bark");
        }
    }

The child provides a new implementation of an inherited method.

This is called:

$$
\boxed{\text{Method Overriding}}
$$

Inheritance provides the relationship.

Overriding changes the inherited behavior.

---

# 20. IS-A Relationship

The IS-A relationship is one of the most important ways to recognize inheritance.

Examples:

```text
Dog IS-A Animal
Car IS-A Vehicle
Manager IS-A Employee
Circle IS-A Shape
Admin IS-A User
```

If the statement makes logical sense, inheritance may be appropriate.

### Example

```text
Dog is an Animal → Yes
Car is a Vehicle → Yes
Manager is an Employee → Yes
```

But:

```text
Car is an Engine → No
House is a Room → No
```

These are not suitable IS-A inheritance relationships.

---

# 21. IS-A vs HAS-A

This is a very important interview distinction.

### IS-A

Represents inheritance.

```text
Dog IS-A Animal
```

Possible code:

    class Dog extends Animal {
    }

### HAS-A

Represents composition or aggregation.

```text
Car HAS-A Engine
```

Possible code:

    class Car {

        Engine engine;
    }

### Fast Rule

> [!important]
> **IS-A → Inheritance**
>
> **HAS-A → Composition/Aggregation**

---

# 22. Single Inheritance vs Hierarchical Inheritance

These are commonly confused.

### Single Inheritance

```text
      Animal
         |
         ↓
        Dog
```

One parent and one child.

### Hierarchical Inheritance

```text
        Animal
        /    \
       ↓      ↓
     Dog      Cat
```

One parent with multiple child classes.

| Single | Hierarchical |
|---|---|
| One parent → one child | One parent → multiple children |
| `Animal → Dog` | `Animal → Dog, Cat` |
| One direct child | Multiple direct children |

---

# 23. Single Inheritance vs Multilevel Inheritance

### Single

```text
A
|
B
```

### Multilevel

```text
A
|
B
|
C
```

In multilevel inheritance, one class inherits from another child class.

Example:

```text
Animal
   |
   ↓
Mammal
   |
   ↓
Dog
```

For single inheritance, focus on one direct parent-child relationship.

---

# 24. Java and Multiple Class Inheritance

Java does not support multiple inheritance of classes.

This is invalid:

    class C extends A, B {
    }

A Java class can directly extend only one class.

However, a class can implement multiple interfaces:

    class C implements A, B {
    }

where `A` and `B` are interfaces.

> [!important]
> **Java: One class can extend one class, but can implement multiple interfaces.**

---

# 25. Why Java Avoids Multiple Class Inheritance

Consider:

```text
        A
       / \
      B   C
       \ /
        D
```

Suppose both `B` and `C` inherit a method from `A` and provide different implementations.

Now `D` inherits from both.

Which implementation should `D` use?

This creates ambiguity.

This is commonly called the:

$$
\boxed{\text{Diamond Problem}}
$$

Java avoids this ambiguity by not allowing a class to extend multiple classes.

Interfaces provide a controlled way to support multiple inheritance of type.

---

# 26. Basic Examples

## Example 1 — Identify Single Inheritance

**Question**

Which diagram represents single inheritance?

```text
A. A → B
B. A → B → C
C. A → B and A → C
D. A ← B → C
```

**Pattern**

Single inheritance:

```text
One parent
One direct child
```

Therefore:

$$
\boxed{\text{A. A → B}}
$$

---

## Example 2 — Identify Parent and Child

**Question**

    class Animal {
    }

    class Dog extends Animal {
    }

Which is the parent?

**Pattern**

The class after `extends` is the parent.

```text
Dog extends Animal
```

Therefore:

$$
\boxed{\text{Animal}}
$$

---

## Example 3 — Identify Child

**Question**

    class Vehicle {
    }

    class Car extends Vehicle {
    }

Which class is the child?

**Pattern**

The class before `extends` is the child.

Therefore:

$$
\boxed{\text{Car}}
$$

---

## Example 4 — Count Direct Relationships

**Question**

Consider:

```text
Animal
   |
   ↓
Dog
```

How many direct inheritance relationships exist?

**Calculation**

```text
Animal → Dog
```

Therefore:

$$
\boxed{1}
$$

---

# 27. Medium Examples

## Example 5 — Inherited Method

**Question**

    class Animal {

        void eat() {
            System.out.println("Eat");
        }
    }

    class Dog extends Animal {

        void bark() {
            System.out.println("Bark");
        }
    }

    Dog d = new Dog();

    d.eat();
    d.bark();

What is printed?

**Pattern**

`eat()` is inherited.

`bark()` belongs to `Dog`.

**Calculation**

```text
d.eat()  → Eat
d.bark() → Bark
```

**Answer:**

```text
Eat
Bark
```

---

## Example 6 — Parent Constructor

**Question**

    class Parent {

        Parent() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        Child() {
            System.out.println("Child");
        }
    }

    Child c = new Child();

What is the output?

**Pattern**

Parent constructor executes before child constructor.

**Answer:**

```text
Parent
Child
```

$$
\boxed{\text{Parent → Child}}
$$

---

## Example 7 — `super`

**Question**

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void show() {
            System.out.println(super.x);
        }
    }

What is printed?

**Pattern**

`super.x` refers to the parent field.

**Therefore:**

$$
\boxed{10}
$$

---

## Example 8 — Inherited and Own Methods

**Question**

    class Employee {

        void work() {
            System.out.println("Work");
        }
    }

    class Manager extends Employee {

        void manage() {
            System.out.println("Manage");
        }
    }

Which methods can a `Manager` object call?

**Calculation**

Inherited:

```text
work()
```

Own:

```text
manage()
```

Therefore:

$$
\boxed{\text{work() and manage()}}
$$

---

# 28. Advanced Examples

## Example 9 — Method Overriding

**Question**

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

    Dog d = new Dog();
    d.sound();

What is printed?

**Pattern**

`Dog` overrides the inherited `sound()` method.

**Therefore:**

```text
Dog
```

$$
\boxed{\text{Dog}}
$$

---

## Example 10 — Parent Reference, Child Object

**Question**

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

    Animal a = new Dog();

    a.sound();

What is printed?

**Pattern**

Reference:

```text
Animal
```

Actual object:

```text
Dog
```

The overridden method is selected at runtime.

Therefore:

```text
Dog
```

$$
\boxed{\text{Dog}}
$$

This connects inheritance with runtime polymorphism.

---

## Example 11 — Private Member

**Question**

    class Parent {

        private int x = 10;

        void show() {
            System.out.println(x);
        }
    }

    class Child extends Parent {

        void test() {
            // System.out.println(x);
        }
    }

Can `Child` directly access `x`?

**Pattern**

`x` is private to `Parent`.

Therefore:

$$
\boxed{\text{No, Child cannot directly access x}}
$$

However, `Child` can call inherited accessible methods such as `show()`.

---

## Example 12 — Single Inheritance Identification

**Question**

Which of the following is single inheritance?

```text
A.

Animal
   |
   ↓
Dog


B.

Animal
  / \
 ↓   ↓
Dog Cat


C.

Animal
   |
   ↓
Mammal
   |
   ↓
Dog
```

**Analysis**

```text
A → Single
B → Hierarchical
C → Multilevel
```

**Answer:**

$$
\boxed{\text{A}}
$$

---

## Example 13 — IS-A Test

**Question**

Which relationship is suitable for inheritance?

```text
A. Car IS-A Vehicle
B. Car HAS-A Engine
C. House HAS-A Room
D. Computer HAS-A Keyboard
```

**Pattern**

Inheritance represents IS-A.

**Therefore:**

$$
\boxed{\text{A. Car IS-A Vehicle}}
$$

---

# 29. Real-World Design Example

Consider an e-commerce application.

```text
                 User
                  |
                  ↓
              Customer
```

The parent `User` may contain:

```text
login()
logout()
username
email
```

The child `Customer` may add:

```text
placeOrder()
viewOrders()
addToCart()
```

Example:

    class User {

        void login() {
            System.out.println("Login");
        }

        void logout() {
            System.out.println("Logout");
        }
    }

    class Customer extends User {

        void placeOrder() {
            System.out.println("Order placed");
        }
    }

Now:

    Customer customer = new Customer();

    customer.login();
    customer.placeOrder();
    customer.logout();

The customer gets common user functionality and adds specialized behavior.

---

# 30. Real-World Software Engineering Example

Consider an employee management system.

```text
Employee
   |
   ↓
Developer
```

Parent:

    class Employee {

        String name;
        double salary;

        void login() {
            System.out.println("Employee login");
        }

        void logout() {
            System.out.println("Employee logout");
        }
    }

Child:

    class Developer extends Employee {

        void writeCode() {
            System.out.println("Writing code");
        }
    }

This allows common employee functionality to be reused.

However, inheritance should not be used merely because code can be reused.

The relationship should make logical sense.

> [!important]
> **Use inheritance when there is a genuine IS-A relationship, not just because two classes share code.**

---

# 31. When Should You Use Single Inheritance?

Use single inheritance when:

### Condition 1 — Strong IS-A Relationship

Example:

```text
Dog IS-A Animal
```

### Condition 2 — Common Functionality Exists

Example:

```text
Animal → eat()
Dog    → bark()
```

### Condition 3 — Child Is a Specialized Version

Example:

```text
Employee
   ↓
Manager
```

Manager is a specialized employee.

### Condition 4 — Shared Behavior Makes Sense

Common functionality should logically belong to the parent.

---

# 32. When Should You NOT Use Inheritance?

Do not use inheritance simply because two classes have similar code.

Example:

```text
Car HAS-A Engine
```

Do not model:

```text
class Car extends Engine
```

Instead:

    class Car {

        Engine engine;
    }

This represents composition.

> [!warning]
> **Code reuse alone is not enough to justify inheritance.**

---

# 33. Shortcuts

> [!tip]
> **Shortcut 1 — `extends`**
>
> If you see:
>
> `class B extends A`
>
> immediately think:
>
> ```text
> A → Parent
> B → Child
> ```

> [!tip]
> **Shortcut 2 — IS-A**
>
> If:
>
> ```text
> B IS-A A
> ```
>
> inheritance may be appropriate.
>
> Example:
>
> ```text
> Dog IS-A Animal
> ```

> [!tip]
> **Shortcut 3 — Single vs Hierarchical**
>
> ```text
> A → B
> ```
>
> Single.
>
> ```text
> A → B
> A → C
> ```
>
> Hierarchical.

> [!tip]
> **Shortcut 4 — Single vs Multilevel**
>
> ```text
> A → B
> ```
>
> Single.
>
> ```text
> A → B → C
> ```
>
> Multilevel.

> [!tip]
> **Shortcut 5 — Parent Constructor**
>
> When a child object is created:
>
> ```text
> Parent constructor
> ↓
> Child constructor
> ```

> [!tip]
> **Shortcut 6 — `super`**
>
> Think:
>
> ```text
> super → Immediate Parent
> ```

> [!tip]
> **Shortcut 7 — Multiple Classes**
>
> Java does not allow:
>
> `class C extends A, B`
>
> But allows:
>
> `class C implements A, B`
>
> when `A` and `B` are interfaces.

---

# 34. Recognition Tricks

### Pattern 1 — `extends`

> [!important]
> If you see:
>
> `class Child extends Parent`
>
> think:
>
> **Inheritance**

---

### Pattern 2 — One Parent, One Child

> [!important]
> If the hierarchy looks like:
>
> ```text
> A
> |
> B
> ```
>
> think:
>
> **Single Inheritance**

---

### Pattern 3 — IS-A

> [!important]
> If the statement says:
>
> ```text
> Dog is an Animal
> ```
>
> think:
>
> **Inheritance**

---

### Pattern 4 — HAS-A

> [!important]
> If the statement says:
>
> ```text
> Car has an Engine
> ```
>
> think:
>
> **Composition/Aggregation**
>
> Not inheritance.

---

### Pattern 5 — Parent + Child Methods

> [!important]
> If a child object calls a method defined in the parent:
>
> think:
>
> **Inherited behavior**

---

### Pattern 6 — `super`

> [!important]
> If you see:
>
> `super.method()`
>
> or:
>
> `super.variable`
>
> think:
>
> **Immediate parent class**

---

### Pattern 7 — Constructor Output

> [!important]
> If a child object is created and both parent and child have constructors:
>
> think:
>
> **Parent constructor first, child constructor second**

---

# 35. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Identify single inheritance from a class hierarchy.

### Pattern 2
Identify parent and child classes.

### Pattern 3
Understand the `extends` keyword.

### Pattern 4
Identify inherited methods.

### Pattern 5
Understand the IS-A relationship.

### Pattern 6
Differentiate IS-A and HAS-A.

### Pattern 7
Trace parent and child constructors.

### Pattern 8
Understand the `super` keyword.

### Pattern 9
Identify overridden methods.

### Pattern 10
Understand private member accessibility.

### Pattern 11
Differentiate single, multilevel, and hierarchical inheritance.

### Pattern 12
Understand Java's restriction on multiple class inheritance.

### Pattern 13
Understand inheritance with interfaces.

### Pattern 14
Trace output-based inheritance questions.

### Pattern 15
Recognize inheritance in real-world class design.

---

# 36. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing Single and Multilevel Inheritance

```text
A → B
```

is single inheritance.

```text
A → B → C
```

is multilevel inheritance.

---

### Mistake 2 — Confusing Single and Hierarchical Inheritance

```text
A → B
```

is single.

```text
   B
  /
 A
  \
   C
```

or:

```text
A → B
A → C
```

is hierarchical.

---

### Mistake 3 — Thinking Private Members Are Directly Accessible

A subclass cannot directly access a parent's private field.

---

### Mistake 4 — Thinking Constructors Are Inherited

Constructors are not inherited.

The parent constructor executes during child-object construction, but it remains the parent's constructor.

---

### Mistake 5 — Using Inheritance for Every Reuse Problem

Shared code does not automatically mean inheritance.

Ask:

```text
Is it IS-A?
```

If not, consider composition or aggregation.

---

### Mistake 6 — Thinking Java Supports Multiple Class Inheritance

This is invalid:

    class C extends A, B {
    }

Java supports one direct superclass for a class.

---

### Mistake 7 — Confusing `extends` and `implements`

```text
Class → extends → Class
Class → implements → Interface
Interface → extends → Interface
```

---

### Mistake 8 — Ignoring Runtime Behavior

If a parent reference points to a child object and the method is overridden, runtime dispatch can select the child's implementation.

---

# 37. Interview Questions

## Beginner

### Q1. What is inheritance?

**Answer:**

Inheritance is an OOP mechanism in which a child class acquires accessible properties and behaviors from a parent class.

---

### Q2. What is single inheritance?

**Answer:**

Single inheritance is a relationship where one child class directly inherits from one parent class.

Example:

    class Dog extends Animal {
    }

---

### Q3. Which keyword is used for inheritance in Java?

**Answer:**

`extends` is used when a class inherits from another class.

---

### Q4. What is a superclass?

**Answer:**

A superclass is the parent/base class from which another class inherits.

---

### Q5. What is a subclass?

**Answer:**

A subclass is the child/derived class that inherits from a superclass.

---

## Intermediate

### Q6. What is an IS-A relationship?

**Answer:**

IS-A represents inheritance.

Examples:

```text
Dog IS-A Animal
Car IS-A Vehicle
Manager IS-A Employee
```

---

### Q7. Are constructors inherited?

**Answer:**

No. Constructors are not inherited, although the parent constructor is invoked during child-object construction.

---

### Q8. Can a child access private members of the parent directly?

**Answer:**

No. Private members are accessible only within the class that declares them.

---

### Q9. Can Java support multiple inheritance?

**Answer:**

Java does not support multiple inheritance of classes. A class can directly extend only one class, but it can implement multiple interfaces.

---

### Q10. Why does Java not support multiple class inheritance?

**Answer:**

One major reason is avoiding ambiguity such as the diamond problem, where a class could inherit conflicting implementations from multiple parent classes.

---

## Advanced

### Q11. What is the difference between inheritance and composition?

**Answer:**

Inheritance represents an IS-A relationship.

Composition represents a HAS-A relationship.

```text
Dog IS-A Animal
Car HAS-A Engine
```

---

### Q12. Why should we prefer composition over inheritance in some situations?

**Answer:**

Composition can provide more flexibility because objects can be assembled from components without creating a rigid inheritance hierarchy.

Inheritance should be used when the relationship is genuinely IS-A.

---

### Q13. What happens when a child overrides a parent method?

**Answer:**

The child provides its own implementation of the inherited method. When the method is invoked on a child object, runtime polymorphism can select the child's implementation.

---

### Q14. What does `super` mean?

**Answer:**

`super` refers to the immediate parent-class context and can be used to access parent members or invoke the parent constructor.

---

### Q15. Can an abstract class be the parent in single inheritance?

**Answer:**

Yes.

Example:

    abstract class Animal {
        abstract void sound();
    }

    class Dog extends Animal {

        void sound() {
            System.out.println("Bark");
        }
    }

---

# 38. Output-Based Interview Challenge

## Challenge 1

What is the output?

    class A {

        void show() {
            System.out.println("A");
        }
    }

    class B extends A {

        void display() {
            System.out.println("B");
        }
    }

    public class Main {

        public static void main(String[] args) {

            B obj = new B();

            obj.show();
            obj.display();
        }
    }

### Think

```text
B inherits show()
B owns display()
```

### Answer

```text
A
B
```

---

## Challenge 2

What is the output?

    class Parent {

        Parent() {
            System.out.println("P");
        }
    }

    class Child extends Parent {

        Child() {
            System.out.println("C");
        }
    }

    public class Main {

        public static void main(String[] args) {

            new Child();
        }
    }

### Think

```text
Parent constructor
        ↓
Child constructor
```

### Answer

```text
P
C
```

---

## Challenge 3

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

            Animal a = new Dog();

            a.sound();
        }
    }

### Think

```text
Reference → Animal
Object    → Dog
Overridden method → Dog
```

### Answer

```text
Dog
```

---

# 39. Formula Sheet

```text
Inheritance
= Child acquires accessible features from Parent

Single Inheritance
= One Parent → One Direct Child

Syntax:
class Child extends Parent {
}

Parent:
Superclass / Base Class

Child:
Subclass / Derived Class

IS-A:
Dog IS-A Animal
Car IS-A Vehicle

HAS-A:
Car HAS-A Engine

Single:
A → B

Multilevel:
A → B → C

Hierarchical:
A → B
A → C

Java:
One class → One direct superclass

Class → extends → Class

Class → implements → Interface

Interface → extends → Interface

super
→ Immediate Parent

Constructors
→ Not inherited

Private Parent Members
→ Not directly accessible in Child

Method Overriding
→ Child provides a new implementation
```

# 40. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Single inheritance means one child class directly inherits from one parent class.**

### Visual

```text
      Parent
         |
         ↓
       Child
```

### Java Syntax

    class Child extends Parent {
    }

### Remember

- Parent = Superclass
- Child = Subclass
- `extends` = class inheritance
- Single inheritance = one parent → one direct child
- Inheritance represents IS-A
- `Dog IS-A Animal`
- Child can use accessible inherited members
- Private members are not directly accessible
- Constructors are not inherited
- Parent constructor executes before child constructor
- `super` refers to the immediate parent
- Method overriding can occur in a child class
- Java does not support multiple inheritance of classes
- Java supports multiple interfaces
- Use inheritance for genuine IS-A relationships
- Use composition/aggregation for HAS-A relationships

### High-Level OOP Connection

```text
Parent Class
     ↓
Inheritance
     ↓
Child Class
     ↓
Reuse + Extension
     ↓
Method Overriding
     ↓
Runtime Polymorphism
```

### Golden Memory Trick

**Single inheritance = one child gets reusable functionality from one parent.**

### One-Line Recognition

**If you see `class Child extends Parent` with one direct parent, think Single Inheritance.**