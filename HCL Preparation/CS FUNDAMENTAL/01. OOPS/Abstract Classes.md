---
type: concept
subject: aptitude
topic: "Inheritance"
parent: "OOP Basics"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - inheritance
  - java
  - object-oriented-programming
  - is-a-relationship
wikilinks:
  - "[[OOP Basics]]"
  - "[[Class]]"
  - "[[Object]]"
  - "[[Encapsulation]]"
  - "[[Abstraction]]"
  - "[[Polymorphism]]"
---

# Inheritance

## 1. Core Concept

> [!summary]
> **Inheritance is an OOP mechanism where one class acquires properties and behaviors of another class. It promotes code reuse and allows classes to form hierarchical relationships.**

The simplest way to remember inheritance is:

$$
\boxed{\text{Inheritance} = \text{Reuse + Extension}}
$$

A child class can:

- Reuse existing fields
- Reuse existing methods
- Add new fields
- Add new methods
- Override inherited methods
- Specialize the behavior of the parent class

### Basic Idea

```text
Parent Class
     |
     | inherits
     ↓
Child Class
```

For example:

```text
Vehicle
   |
   +---- Car
   |
   +---- Bike
```

A `Car` is a `Vehicle`.

A `Bike` is a `Vehicle`.

This represents an:

$$
\boxed{\text{IS-A relationship}}
$$

### Java Example

    ~~~~java
    class Vehicle {

        void start() {
            System.out.println("Vehicle started");
        }
    }

    class Car extends Vehicle {

        void drive() {
            System.out.println("Car is driving");
        }
    }
    ~~~~

Now:

    ~~~~java
    Car car = new Car();

    car.start();
    car.drive();
    ~~~~

`Car` can use:

```text
start() → inherited from Vehicle
drive() → defined inside Car
```

---

# 2. Basic Meaning

Inheritance allows a new class to derive from an existing class.

The existing class is commonly called:

```text
Parent
Superclass
Base class
```

The new class is commonly called:

```text
Child
Subclass
Derived class
```

### Terminology

| Term | Meaning |
|---|---|
| Parent class | Existing class |
| Superclass | Parent class |
| Base class | Parent class |
| Child class | New derived class |
| Subclass | Child class |
| Derived class | Child class |

### Basic Syntax

    ~~~~java
    class Parent {
        // fields and methods
    }

    class Child extends Parent {
        // additional fields and methods
    }
    ~~~~

The keyword:

```java
extends
```

is used for class inheritance in Java.

---

# 3. Main Formula

There is no mathematical formula for inheritance.

For aptitude and interview questions, remember:

$$
\boxed{\text{Child} = \text{Parent Features} + \text{New Features}}
$$

Another useful model:

$$
\boxed{\text{Inheritance} = \text{Code Reuse} + \text{Specialization}}
$$

### Relationship

```text
Parent
  ↓
Inherited Features
  +
Child-Specific Features
  ↓
Child
```

### IS-A Formula

If:

```text
Car IS-A Vehicle
```

then inheritance may be appropriate.

If:

```text
Car HAS-A Engine
```

then composition/association may be more appropriate.

---

# 4. Why Do We Need Inheritance?

Imagine an application containing:

```text
Car
Bike
Truck
Bus
```

All of them may have:

```text
start()
stop()
speed
```

Without inheritance, the same code may be repeated.

### Without Inheritance

```text
Car
 ├── start()
 └── stop()

Bike
 ├── start()
 └── stop()

Truck
 ├── start()
 └── stop()
```

The same logic may be duplicated.

### With Inheritance

```text
             Vehicle
            /   |   \
           /    |    \
        Car    Bike   Truck
```

Common functionality can be placed in `Vehicle`.

    ~~~~java
    class Vehicle {

        void start() {
            System.out.println("Vehicle started");
        }

        void stop() {
            System.out.println("Vehicle stopped");
        }
    }
    ~~~~

Then:

    ~~~~java
    class Car extends Vehicle {
    }

    class Bike extends Vehicle {
    }

    class Truck extends Vehicle {
    }
    ~~~~

Now the child classes can reuse common behavior.

> [!important]
> **Put common features in the parent and specialized features in the child.**

---

# 5. Real-Time Example 1 — Vehicles

Consider a real transportation system.

Common vehicle properties:

```text
speed
brand
fuel
```

Common behaviors:

```text
start()
stop()
accelerate()
```

Specialized behavior:

```text
Car → openTrunk()
Bike → kickStart()
Truck → loadCargo()
```

The hierarchy can be:

```text
                 Vehicle
                    |
        +-----------+-----------+
        |           |           |
       Car         Bike        Truck
```

Example:

    ~~~~java
    class Vehicle {

        void start() {
            System.out.println("Vehicle starts");
        }

        void stop() {
            System.out.println("Vehicle stops");
        }
    }

    class Car extends Vehicle {

        void openTrunk() {
            System.out.println("Trunk opened");
        }
    }

    class Bike extends Vehicle {

        void kickStart() {
            System.out.println("Bike kick started");
        }
    }
    ~~~~

This is a classic inheritance example.

---

# 6. Real-Time Example 2 — Banking System

Suppose a banking application has:

```text
Account
   |
   +---- SavingsAccount
   |
   +---- CurrentAccount
   |
   +---- SalaryAccount
```

Common features:

```text
accountNumber
balance
deposit()
withdraw()
```

Specialized features:

```text
SavingsAccount → calculateInterest()
CurrentAccount → businessTransaction()
SalaryAccount  → salaryCredit()
```

Inheritance allows common banking functionality to be centralized.

---

# 7. Real-Time Example 3 — Employees

Consider an organization.

```text
Employee
   |
   +---- Developer
   |
   +---- Manager
   |
   +---- Tester
   |
   +---- HR
```

Common employee properties:

```text
name
id
salary
department
```

Common behavior:

```text
work()
login()
logout()
```

Specialized behavior:

```text
Developer → writeCode()
Tester    → testSoftware()
Manager   → manageTeam()
```

Example:

    ~~~~java
    class Employee {

        String name;
        double salary;

        void login() {
            System.out.println("Employee logged in");
        }
    }

    class Developer extends Employee {

        void writeCode() {
            System.out.println("Writing code");
        }
    }
    ~~~~

---

# 8. Real-Time Example 4 — E-Commerce

Consider an e-commerce system.

```text
Product
   |
   +---- Electronics
   |
   +---- Clothing
   |
   +---- Books
```

Common:

```text
productId
name
price
displayProduct()
```

Specialized:

```text
Electronics → warranty
Clothing    → size
Books       → author
```

This hierarchy can reduce duplicated code.

---

# 9. Real-Time Example 5 — University System

Consider:

```text
Person
  |
  +---- Student
  |
  +---- Professor
  |
  +---- Staff
```

Common properties:

```text
name
age
email
```

Specialized properties:

```text
Student   → registerCourse()
Professor → teach()
Staff     → manageOffice()
```

The parent contains common characteristics.

The child contains specialized characteristics.

---

# 10. Real-Time Example 6 — Online Food Delivery

Consider:

```text
User
 |
 +---- Customer
 |
 +---- DeliveryPartner
 |
 +---- RestaurantOwner
```

Common:

```text
name
phone
login()
logout()
```

Specialized:

```text
Customer         → placeOrder()
DeliveryPartner  → deliverOrder()
RestaurantOwner  → manageMenu()
```

Inheritance models the shared identity while allowing specialization.

---

# 11. Real-Time Example 7 — Game Development

A game may have:

```text
Character
    |
    +---- Warrior
    |
    +---- Mage
    |
    +---- Archer
```

Common:

```text
health
position
move()
attack()
```

Specialized:

```text
Warrior → swordAttack()
Mage    → castSpell()
Archer  → shootArrow()
```

This is a practical use of inheritance combined with polymorphism.

---

# 12. Important Properties

## 12.1 Inheritance Promotes Code Reuse

Example:

    ~~~~java
    class Animal {

        void eat() {
            System.out.println("Eating");
        }
    }

    class Dog extends Animal {
    }

    class Cat extends Animal {
    }
    ~~~~

Both `Dog` and `Cat` can use:

```text
eat()
```

without redefining it.

---

## 12.2 Child Can Add New Features

Example:

    ~~~~java
    class Animal {

        void eat() {
            System.out.println("Eating");
        }
    }

    class Dog extends Animal {

        void bark() {
            System.out.println("Barking");
        }
    }
    ~~~~

`Dog` gets:

```text
eat() → inherited
bark() → own method
```

Therefore:

$$
\boxed{\text{Child = inherited features + new features}}
$$

---

## 12.3 Child Can Override Parent Behavior

Example:

    ~~~~java
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
    ~~~~

The parent defines general behavior.

The child provides specialized behavior.

This is called:

$$
\boxed{\text{Method Overriding}}
$$

---

# 13. Inheritance and Polymorphism

Inheritance and polymorphism often work together.

Example:

    ~~~~java
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
    ~~~~

Now:

    ~~~~java
    Animal a;

    a = new Dog();
    a.sound();

    a = new Cat();
    a.sound();
    ~~~~

Output:

```text
Bark
Meow
```

The reference type remains:

```text
Animal
```

but the actual object determines the overridden method.

This is runtime polymorphism.

> [!important]
> **Inheritance creates the relationship; polymorphism allows different behavior through the common parent type.**

---

# 14. Types of Inheritance

There are several common inheritance structures.

## 14.1 Single Inheritance

One parent → one child.

```text
A
|
B
```

Java:

    ~~~~java
    class A {
    }

    class B extends A {
    }
    ~~~~

---

## 14.2 Multilevel Inheritance

A → B → C

```text
A
|
B
|
C
```

Example:

    ~~~~java
    class Animal {
    }

    class Dog extends Animal {
    }

    class Puppy extends Dog {
    }
    ~~~~

`Puppy` indirectly inherits from `Animal`.

---

## 14.3 Hierarchical Inheritance

One parent → multiple children.

```text
       A
     / | \
    B  C  D
```

Example:

    ~~~~java
    class Animal {
    }

    class Dog extends Animal {
    }

    class Cat extends Animal {
    }

    class Horse extends Animal {
    }
    ~~~~

---

## 14.4 Multiple Inheritance

Multiple parents → one child.

```text
A     B
 \   /
   C
```

Java does **not** support multiple inheritance of classes.

This is invalid:

    ~~~~java
    class C extends A, B {
    }
    ~~~~

However, Java supports multiple interfaces:

    ~~~~java
    class C implements A, B {
    }
    ~~~~

when `A` and `B` are interfaces.

> [!important]
> **Java does not support multiple inheritance through classes, but a class can implement multiple interfaces.**

---

## 14.5 Hybrid Inheritance

Hybrid inheritance combines multiple inheritance structures.

For example:

```text
        A
       / \
      B   C
       \ /
        D
```

Java does not support arbitrary hybrid inheritance through classes because Java does not support multiple inheritance of classes.

Interfaces can be used to model multiple type relationships.

---

# 15. `extends` Keyword

For class inheritance:

    ~~~~java
    class Child extends Parent {
    }
    ~~~~

Meaning:

```text
Child IS-A Parent
```

Example:

    ~~~~java
    class Car extends Vehicle {
    }
    ~~~~

Means:

```text
Car IS-A Vehicle
```

---

# 16. `super` Keyword

The `super` keyword refers to the immediate parent class.

It can be used to:

1. Access parent fields
2. Call parent methods
3. Call parent constructors

---

## 16.1 Access Parent Variable

    ~~~~java
    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void display() {
            System.out.println(x);
            System.out.println(super.x);
        }
    }
    ~~~~

Output:

```text
20
10
```

Explanation:

```text
x       → Child's variable
super.x → Parent's variable
```

---

## 16.2 Call Parent Method

    ~~~~java
    class Animal {

        void sound() {
            System.out.println("Animal sound");
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {
            super.sound();
            System.out.println("Bark");
        }
    }
    ~~~~

Output:

```text
Animal sound
Bark
```

The child calls the parent implementation using:

```java
super.sound();
```

---

## 16.3 Call Parent Constructor

    ~~~~java
    class Parent {

        Parent() {
            System.out.println("Parent constructor");
        }
    }

    class Child extends Parent {

        Child() {
            super();
            System.out.println("Child constructor");
        }
    }
    ~~~~

Output:

```text
Parent constructor
Child constructor
```

> [!important]
> A parent constructor executes before the child constructor.

---

# 17. Constructor and Inheritance

Constructors are **not inherited** by child classes.

However, when a child object is created, the parent constructor participates in object initialization.

Example:

    ~~~~java
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
    ~~~~

Creating:

    ~~~~java
    Child c = new Child();
    ~~~~

Output:

```text
Parent
Child
```

The parent constructor executes first.

---

# 18. Method Overriding

Method overriding occurs when a subclass provides its own implementation of an inherited method with the same method signature.

Example:

    ~~~~java
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
    ~~~~

Here:

```text
Animal.sound() → Parent implementation
Dog.sound()    → Child implementation
```

### Important Conditions

For a basic overriding question, remember:

```text
Same method name
Same parameter list
Compatible return type
Subclass relationship
```

The `@Override` annotation is strongly recommended because the compiler can detect accidental signature mistakes.

---

# 19. Inheritance and Access Modifiers

Inheritance does not mean every parent member becomes directly accessible.

Example:

```text
private
```

members belong to the parent class and are not directly accessible in the child class.

Example:

    ~~~~java
    class Parent {

        private int x = 10;
    }

    class Child extends Parent {

        void display() {
            // System.out.println(x);  // Not directly accessible
        }
    }
    ~~~~

The child inherits the class relationship, but it cannot directly access the parent's private member.

### Quick Comparison

| Modifier | Child Access |
|---|---|
| `private` | No direct access |
| default | Accessible depending on package |
| `protected` | Accessible in subclasses, subject to Java rules |
| `public` | Accessible subject to normal access rules |

---

# 20. `final` and Inheritance

A `final` class cannot be extended.

Example:

    ~~~~java
    final class Vehicle {
    }
    ~~~~

This is invalid:

    ~~~~java
    class Car extends Vehicle {
    }
    ~~~~

because `Vehicle` is final.

### Final Method

A `final` method cannot be overridden.

Example:

    ~~~~java
    class Parent {

        final void display() {
            System.out.println("Parent");
        }
    }
    ~~~~

A child cannot override `display()`.

> [!important]
> ```text
> final class   → Cannot be inherited
> final method  → Cannot be overridden
> ```

---

# 21. `Object` Class and Inheritance

In Java, every class ultimately derives from the `Object` class, directly or indirectly, except in the sense that `Object` is the root class of the class hierarchy.

Example:

```text
Object
  |
Animal
  |
Dog
```

If:

    ~~~~java
    class Animal {
    }

    class Dog extends Animal {
    }
    ~~~~

then:

```text
Dog → Animal → Object
```

This means methods defined by `Object`, such as `toString()`, `equals()`, and `hashCode()`, are available through the Java object hierarchy, subject to overriding.

---

# 22. IS-A vs HAS-A

This is extremely important in interviews.

## IS-A

Represents inheritance.

```text
Dog IS-A Animal
Car IS-A Vehicle
Manager IS-A Employee
```

Usually modeled using inheritance.

    ~~~~java
    class Dog extends Animal {
    }
    ~~~~

---

## HAS-A

Represents composition/association.

```text
Car HAS-A Engine
House HAS-A Room
Computer HAS-A Processor
```

Example:

    ~~~~java
    class Engine {
    }

    class Car {

        Engine engine;
    }
    ~~~~

Here:

```text
Car HAS-A Engine
```

not:

```text
Car IS-A Engine
```

> [!important]
> **IS-A → Inheritance**
>
> **HAS-A → Composition/Association**

---

# 23. Real-Time Design Example — Car

Wrong relationship:

```text
Car IS-A Engine
```

This does not make sense.

Correct:

```text
Car HAS-A Engine
```

Therefore:

    ~~~~java
    class Engine {
    }

    class Car {

        private Engine engine;
    }
    ~~~~

But:

```text
Car IS-A Vehicle
```

Therefore:

    ~~~~java
    class Car extends Vehicle {
    }
    ~~~~

This distinction is a common interview question.

---

# 24. Inheritance vs Composition

| Inheritance | Composition |
|---|---|
| IS-A | HAS-A |
| Strong parent-child relationship | Whole-part relationship |
| Uses `extends` | Uses object references |
| Child inherits parent members | Object contains another object |
| Can support polymorphism | Often provides greater flexibility |
| Example: `Dog extends Animal` | Example: `Car has Engine` |

### Design Rule

> [!tip]
> Prefer inheritance when the relationship is genuinely **IS-A** and the child is a true specialization of the parent.

Do not use inheritance simply to reuse a few methods.

---

# 25. Advanced Real-Time Example — E-Commerce Payment

Suppose:

```text
Payment
   |
   +---- CardPayment
   +---- UPIPayment
   +---- WalletPayment
```

This can model an IS-A relationship:

```text
CardPayment IS-A Payment
UPIPayment IS-A Payment
WalletPayment IS-A Payment
```

Then:

    ~~~~java
    Payment payment = new UPIPayment();
    ~~~~

The application can work with the common parent type.

This combines:

```text
Inheritance
+
Abstraction
+
Polymorphism
```

---

# 26. Interview Questions

## Interview Question 1

**What is inheritance?**

### Strong Answer

Inheritance is an OOP mechanism where a subclass acquires accessible properties and behaviors from a superclass and can extend or specialize them. It promotes code reuse and models an IS-A relationship.

---

## Interview Question 2

**Why is inheritance used?**

### Answer

Main reasons:

- Code reuse
- Specialization
- Hierarchical classification
- Method overriding
- Runtime polymorphism
- Modeling IS-A relationships

---

## Interview Question 3

**What is the difference between superclass and subclass?**

### Answer

```text
Superclass → Parent/base class
Subclass   → Child/derived class
```

The subclass extends the superclass and can add or specialize functionality.

---

## Interview Question 4

**Which keyword is used for inheritance in Java?**

### Answer

For class inheritance:

```java
extends
```

Example:

    ~~~~java
    class Dog extends Animal {
    }
    ~~~~

---

## Interview Question 5

**Does Java support multiple inheritance?**

### Strong Answer

Java does not support multiple inheritance of classes.

This is invalid:

    ~~~~java
    class C extends A, B {
    }
    ~~~~

However, a class can implement multiple interfaces:

    ~~~~java
    class C implements A, B {
    }
    ~~~~

where `A` and `B` are interfaces.

---

## Interview Question 6

**What is an IS-A relationship?**

### Answer

An IS-A relationship represents inheritance.

Examples:

```text
Dog IS-A Animal
Car IS-A Vehicle
Manager IS-A Employee
```

---

## Interview Question 7

**What is a HAS-A relationship?**

### Answer

HAS-A represents a composition or association relationship.

Examples:

```text
Car HAS-A Engine
Computer HAS-A Processor
House HAS-A Room
```

---

## Interview Question 8

**What is method overriding?**

### Answer

Method overriding occurs when a subclass provides its own implementation of an inherited method using the same method signature, subject to Java's overriding rules.

---

## Interview Question 9

**Can constructors be inherited?**

### Answer

No.

Constructors are not inherited.

However, a parent constructor participates in initialization when a child object is created.

---

## Interview Question 10

**What is the purpose of `super`?**

### Answer

`super` refers to the immediate parent class.

It can be used to:

- Access parent members
- Call parent methods
- Invoke parent constructors

---

## Interview Question 11

**Can a private method be overridden?**

### Answer

No.

A private method is not accessible to the subclass and therefore is not overridden in the normal Java overriding sense.

---

## Interview Question 12

**Can a final method be overridden?**

### Answer

No.

A method declared `final` cannot be overridden by a subclass.

---

## Interview Question 13

**Can a final class be inherited?**

### Answer

No.

A final class cannot be extended.

---

## Interview Question 14

**What is multilevel inheritance?**

### Answer

When inheritance occurs through multiple levels:

```text
A
|
B
|
C
```

For example:

```java
class Animal {
}

class Dog extends Animal {
}

class Puppy extends Dog {
}
```

`Puppy` indirectly inherits from `Animal`.

---

## Interview Question 15

**What is hierarchical inheritance?**

### Answer

When multiple child classes inherit from the same parent:

```text
       Animal
       /    \
     Dog    Cat
```

---

# 27. Output-Based Interview Questions

## Question 1

What is the output?

    ~~~~java
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
    ~~~~

### Pattern

```text
Reference type → Animal
Actual object  → Dog
```

The overridden method in `Dog` executes.

### Answer

```text
Dog
```

$$
\boxed{\text{Dog}}
$$

---

## Question 2

What is the output?

    ~~~~java
    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void display() {
            System.out.println(x);
            System.out.println(super.x);
        }
    }

    public class Main {

        public static void main(String[] args) {

            Child c = new Child();

            c.display();
        }
    }
    ~~~~

### Analysis

```text
x       → Child's x = 20
super.x → Parent's x = 10
```

### Answer

```text
20
10
```

---

## Question 3

What is the output?

    ~~~~java
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

    public class Main {

        public static void main(String[] args) {

            new Child();
        }
    }
    ~~~~

### Pattern

Parent constructor executes before child constructor.

### Answer

```text
Parent
Child
```

---

# 28. Pattern Recognition

### Pattern 1 — "IS-A"

> [!important]
> If the question says:
>
> ```text
> Dog IS-A Animal
> Car IS-A Vehicle
> ```
>
> Think:
>
> **Inheritance**

---

### Pattern 2 — "Reuse Parent Code"

> [!important]
> If the question says:
>
> **"Reuse properties and methods of an existing class"**
>
> Think:
>
> **Inheritance**

---

### Pattern 3 — `extends`

> [!important]
> If you see:
>
> ```java
> class Child extends Parent
> ```
>
> Think:
>
> **Class inheritance**

---

### Pattern 4 — `super`

> [!important]
> If you see:
>
> ```java
> super.method();
> ```
>
> Think:
>
> **Parent class member**

---

### Pattern 5 — Multiple Children

> [!important]
> If one parent has several children:
>
> ```text
> A
> /|\
> B C D
> ```
>
> Think:
>
> **Hierarchical inheritance**

---

### Pattern 6 — Chain

> [!important]
> If inheritance forms:
>
> ```text
> A → B → C
> ```
>
> Think:
>
> **Multilevel inheritance**

---

### Pattern 7 — Multiple Parents

> [!important]
> If one child has multiple parent classes:
>
> ```text
> A   B
>  \ /
>   C
> ```
>
> Think:
>
> **Multiple inheritance**
>
> In Java, this is not supported through classes.

---

### Pattern 8 — HAS-A

> [!important]
> If the relationship is:
>
> ```text
> Car HAS-A Engine
> ```
>
> Think:
>
> **Composition/Association, not inheritance**

---

# 29. Common Exam Patterns

> [!important] Must Master

### Pattern 1

Definition of inheritance.

### Pattern 2

Superclass vs subclass.

### Pattern 3

`extends` keyword.

### Pattern 4

IS-A relationship.

### Pattern 5

Code reuse.

### Pattern 6

Single inheritance.

### Pattern 7

Multilevel inheritance.

### Pattern 8

Hierarchical inheritance.

### Pattern 9

Multiple inheritance restriction in Java.

### Pattern 10

Multiple interfaces as an alternative for multiple type inheritance.

### Pattern 11

Method overriding.

### Pattern 12

Runtime polymorphism.

### Pattern 13

`super` keyword.

### Pattern 14

Constructor execution order.

### Pattern 15

Private members and inheritance.

### Pattern 16

Final classes and methods.

### Pattern 17

Object class hierarchy.

### Pattern 18

IS-A vs HAS-A.

### Pattern 19

Inheritance vs composition.

### Pattern 20

Output-based inheritance questions.

---

# 30. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing IS-A and HAS-A

Wrong:

```text
Car IS-A Engine
```

Correct:

```text
Car HAS-A Engine
```

And:

```text
Car IS-A Vehicle
```

---

### Mistake 2 — Thinking Child Gets Everything From Parent

A child does not gain direct access to private members simply because it extends the parent.

Remember:

```text
private → not directly accessible in subclass
```

---

### Mistake 3 — Thinking Constructors Are Inherited

Constructors are not inherited.

They participate in object initialization.

---

### Mistake 4 — Thinking Java Supports Multiple Class Inheritance

Wrong:

    ~~~~java
    class C extends A, B {
    }
    ~~~~

Java does not allow this.

Use interfaces when multiple contracts are needed.

---

### Mistake 5 — Confusing Overloading and Overriding

```text
Overloading
→ Same class/related context
→ Same method name
→ Different parameter list

Overriding
→ Parent-child relationship
→ Same method signature
→ Child provides new implementation
```

---

### Mistake 6 — Forgetting `super`

If a child hides a parent field or overrides a method, `super` can explicitly refer to the immediate parent implementation/member.

---

### Mistake 7 — Assuming `final` Methods Can Be Overridden

They cannot.

```text
final method → No overriding
final class  → No inheritance
```

---

### Mistake 8 — Using Inheritance Only for Code Reuse

Inheritance should represent a meaningful IS-A relationship.

If the relationship is HAS-A, composition is often more appropriate.

---

# 31. High-Level Design Perspective

Inheritance is not just a syntax feature.

It is a **modeling decision**.

Suppose we have:

```text
Employee
```

and:

```text
Developer
```

Ask:

> Is every Developer an Employee?

If yes, inheritance may make sense.

```text
Developer IS-A Employee
```

But suppose we have:

```text
Car
Engine
```

Ask:

> Is every Car an Engine?

No.

Instead:

```text
Car HAS-A Engine
```

Therefore composition is more appropriate.

### Professional Design Rule

> [!important]
> **Use inheritance for genuine specialization. Use composition when an object is made up of other objects.**

---

# 32. Inheritance and Software Architecture

In professional applications, inheritance is often combined with:

```text
Abstraction
Polymorphism
Interfaces
Composition
Dependency Injection
```

For example:

```text
Payment
   |
   +---- CardPayment
   +---- UPIPayment
   +---- WalletPayment
```

The system can depend on:

```text
Payment
```

rather than concrete implementations.

This gives:

```text
Abstraction
     +
Inheritance / Implementation
     +
Polymorphism
     +
Loose Coupling
```

This is much more powerful than simply copying code from one class to another.

---

# 33. Formula Sheet

```text
Inheritance
= Reuse + Extension + Specialization

Child
= Parent Features + Child-Specific Features

Parent
= Superclass / Base Class

Child
= Subclass / Derived Class

Class inheritance:
class Child extends Parent

IS-A
→ Inheritance

HAS-A
→ Composition / Association

Single:
A → B

Multilevel:
A → B → C

Hierarchical:
    A
   /|\
  B C D

Multiple:
A   B
 \ /
  C

Java:
→ No multiple inheritance of classes
→ Multiple interfaces are allowed

super
→ Refers to immediate parent

final class
→ Cannot be extended

final method
→ Cannot be overridden

Constructors
→ Not inherited

Inheritance + Overriding
→ Runtime Polymorphism
```

---

# 34. Quick Revision

> [!summary] One-Minute Revision

### Core Idea

```text
Parent
  ↓
Child
```

The child can:

```text
Reuse
+
Extend
+
Specialize
```

### Remember

- Inheritance allows one class to derive from another.
- Parent = superclass/base class.
- Child = subclass/derived class.
- Java uses `extends` for class inheritance.
- Inheritance usually represents an IS-A relationship.
- It promotes code reuse.
- Child classes can add new functionality.
- Child classes can override inherited methods.
- `super` refers to the immediate parent.
- Constructors are not inherited.
- Parent constructors execute before child constructor code.
- Java does not support multiple inheritance of classes.
- A class can implement multiple interfaces.
- `final` class cannot be extended.
- `final` method cannot be overridden.
- `private` parent members are not directly accessible in the child.
- Every Java class ultimately belongs to the `Object` hierarchy.
- Use inheritance for genuine specialization.
- Use composition for HAS-A relationships.

### Golden Memory Trick

**Inheritance means: "I am a specialized version of you."**

Example:

```text
Dog IS-A Animal
Car IS-A Vehicle
Developer IS-A Employee
```

### One-Line Recognition

**If the question says "IS-A", "extends", "reuse parent functionality", "parent-child class", or "subclass", think Inheritance.**