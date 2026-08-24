---
type: concept
subject: aptitude
topic: "Hierarchical Inheritance"
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
  - hierarchical-inheritance
  - java
  - object-oriented-programming
  - interview
wikilinks:
  - "[[OOP Basics]]"
  - "[[Inheritance]]"
  - "[[Single Inheritance]]"
  - "[[Multilevel Inheritance]]"
  - "[[Multiple Inheritance]]"
  - "[[Polymorphism]]"
  - "[[Method Overriding]]"
---

# Hierarchical Inheritance

> [!summary]
> **Hierarchical Inheritance** occurs when **multiple child classes inherit from the same parent class**.
>
> The easiest visual pattern is:
>
> ```text
>             Parent
>            /      \
>           ↓        ↓
>        Child A   Child B
> ```
>
> The key recognition rule is:
>
> **ONE PARENT → MULTIPLE CHILDREN**

---

# 1. Core Concept

Suppose we have a common parent:

```text
             Vehicle
             /     \
            ↓       ↓
          Car      Bike
```

Both `Car` and `Bike` inherit common functionality from `Vehicle`.

For example:

    class Vehicle {

        void start() {
            System.out.println("Vehicle starts");
        }

        void stop() {
            System.out.println("Vehicle stops");
        }
    }

    class Car extends Vehicle {

        void drive() {
            System.out.println("Car drives");
        }
    }

    class Bike extends Vehicle {

        void ride() {
            System.out.println("Bike rides");
        }
    }

Now:

    Car car = new Car();

    car.start();
    car.stop();
    car.drive();

And:

    Bike bike = new Bike();

    bike.start();
    bike.stop();
    bike.ride();

The common functionality:

```text
start()
stop()
```

comes from `Vehicle`.

The specialized functionality:

```text
drive() → Car
ride()  → Bike
```

belongs to the respective child classes.

> [!important]
> **Hierarchical Inheritance = One Parent + Multiple Direct Child Classes**

---

# 2. Basic Meaning

The word **hierarchical** means that classes are arranged in a hierarchy.

Example:

```text
                    Animal
                 /    |    \
                /     |     \
               ↓      ↓      ↓
             Dog     Cat    Cow
```

Here:

```text
Animal → Parent
Dog    → Child
Cat    → Child
Cow    → Child
```

All three classes inherit from the same parent.

This is hierarchical inheritance.

---

# 3. Main Formula

There is no mathematical formula for inheritance.

For exam recognition, remember:

$$
\boxed{\text{One Parent} \rightarrow \text{Multiple Children}}
$$

Another useful representation:

$$
\boxed{P \rightarrow C_1,\ C_2,\ C_3,\ldots}
$$

Where:

```text
P  = Parent
C1 = Child 1
C2 = Child 2
C3 = Child 3
```

### Mental Formula

```text
COMMON FEATURES
       ↓
    Parent
    /  |  \
   /   |   \
Child Child Child
```

The parent contains functionality common to multiple child classes.

---

# 4. The Most Important Recognition Trick

> [!important]
> **If multiple classes directly extend the SAME class, think HIERARCHICAL INHERITANCE.**

Example:

    class A {
    }

    class B extends A {
    }

    class C extends A {
    }

    class D extends A {
    }

Immediately recognize:

```text
        A
      / | \
     B  C  D
```

Therefore:

$$
\boxed{\text{Hierarchical Inheritance}}
$$

---

# 5. Why Is It Called Hierarchical?

Because the classes form a tree-like hierarchy.

Example:

```text
                 Employee
                /        \
               /          \
              ↓            ↓
         Developer       Manager
```

The parent is at the top.

Specialized classes appear below it.

This resembles a tree structure:

```text
                 Root
                /    \
              Node   Node
```

That visual similarity makes hierarchical inheritance easy to recognize.

---

# 6. Real-Time Example 1 — Animal Hierarchy

One of the simplest real-world examples is:

```text
                    Animal
                  /   |   \
                 /    |    \
                ↓     ↓     ↓
              Dog    Cat    Cow
```

Common functionality:

```text
eat()
sleep()
```

Specific functionality:

```text
Dog  → bark()
Cat  → meow()
Cow  → moo()
```

Java:

    class Animal {

        void eat() {
            System.out.println("Eating");
        }

        void sleep() {
            System.out.println("Sleeping");
        }
    }

    class Dog extends Animal {

        void bark() {
            System.out.println("Barking");
        }
    }

    class Cat extends Animal {

        void meow() {
            System.out.println("Meowing");
        }
    }

    class Cow extends Animal {

        void moo() {
            System.out.println("Mooing");
        }
    }

### Object Usage

    Dog dog = new Dog();

    dog.eat();
    dog.sleep();
    dog.bark();

    Cat cat = new Cat();

    cat.eat();
    cat.sleep();
    cat.meow();

Notice:

```text
Dog → Animal functionality + Dog functionality

Cat → Animal functionality + Cat functionality

Cow → Animal functionality + Cow functionality
```

---

# 7. Real-Time Example 2 — Vehicle System

Consider a transportation application.

```text
                    Vehicle
                   /       \
                  ↓         ↓
                Car        Bike
```

Common behavior:

```text
start()
stop()
```

Car-specific:

```text
openTrunk()
```

Bike-specific:

```text
kickStart()
```

Java:

    class Vehicle {

        void start() {
            System.out.println("Vehicle started");
        }

        void stop() {
            System.out.println("Vehicle stopped");
        }
    }

    class Car extends Vehicle {

        void openTrunk() {
            System.out.println("Trunk opened");
        }
    }

    class Bike extends Vehicle {

        void kickStart() {
            System.out.println("Kick start");
        }
    }

The parent provides common vehicle functionality.

The children specialize it.

---

# 8. Real-Time Example 3 — Employee Management System

Consider a company.

```text
                    Employee
                   /        \
                  ↓          ↓
             Developer     Manager
```

Common employee functionality:

```text
login()
logout()
calculateSalary()
```

Developer-specific:

```text
writeCode()
debug()
```

Manager-specific:

```text
manageTeam()
conductMeeting()
```

Java:

    class Employee {

        void login() {
            System.out.println("Login");
        }

        void logout() {
            System.out.println("Logout");
        }
    }

    class Developer extends Employee {

        void writeCode() {
            System.out.println("Writing code");
        }
    }

    class Manager extends Employee {

        void manageTeam() {
            System.out.println("Managing team");
        }
    }

The parent represents common employee behavior.

The child classes represent specialized roles.

---

# 9. Real-Time Example 4 — Banking System

Consider:

```text
                     BankAccount
                    /           \
                   ↓             ↓
             SavingsAccount   CurrentAccount
```

Common behavior:

```text
deposit()
withdraw()
displayBalance()
```

Savings-specific:

```text
calculateInterest()
```

Current-account-specific:

```text
overdraft()
```

This is a natural hierarchical structure.

---

# 10. Real-Time Example 5 — E-Commerce Users

Consider an e-commerce platform:

```text
                       User
                    /       \
                   ↓         ↓
              Customer      Admin
```

Common functionality:

```text
login()
logout()
```

Customer:

```text
placeOrder()
addToCart()
```

Admin:

```text
addProduct()
removeProduct()
manageUsers()
```

Java:

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

    class Admin extends User {

        void manageUsers() {
            System.out.println("Managing users");
        }
    }

---

# 11. Real-Time Example 6 — Shape System

Consider a graphics application.

```text
                     Shape
                  /    |    \
                 ↓     ↓     ↓
              Circle  Square  Triangle
```

Common:

```text
draw()
display()
```

Specific:

```text
Circle   → calculateCircleArea()
Square   → calculateSquareArea()
Triangle → calculateTriangleArea()
```

This is useful when multiple specialized objects share common characteristics.

---

# 12. Real-Time Example 7 — Payment System

A payment platform may have:

```text
                    Payment
                  /    |     \
                 ↓     ↓      ↓
               UPI    Card   Wallet
```

Common operation:

```text
pay()
```

Specific implementations:

```text
UPI    → UPI processing
Card   → Card processing
Wallet → Wallet processing
```

This is particularly useful when combined with polymorphism.

Example:

    interface Payment {
        void pay();
    }

Strictly speaking, an interface hierarchy is not the same terminology as class-based hierarchical inheritance, so identify the exact relationship shown in the question.

For class inheritance:

    class Payment {
    }

    class UPI extends Payment {
    }

    class Card extends Payment {
    }

    class Wallet extends Payment {
    }

The structure is:

```text
             Payment
          /     |     \
        UPI   Card   Wallet
```

---

# 13. Real-Time Example 8 — Device System

Consider:

```text
                     Device
                  /    |     \
                 ↓     ↓      ↓
               Phone  Tablet Laptop
```

Common:

```text
powerOn()
powerOff()
```

Specific:

```text
Phone  → makeCall()
Tablet → useStylus()
Laptop → runIDE()
```

Again:

```text
Common functionality → Parent
Specialized functionality → Children
```

---

# 14. Real-Time Example 9 — University System

Consider:

```text
                    Person
                   /      \
                  ↓        ↓
              Student    Teacher
```

Common:

```text
name
age
login()
```

Student:

```text
attendClass()
writeExam()
```

Teacher:

```text
teach()
gradeExam()
```

This models a common base entity with specialized roles.

---

# 15. Real-Time Example 10 — Notification System

Consider:

```text
                   Notification
                 /      |       \
                ↓       ↓        ↓
              Email     SMS     Push
```

Common operation:

```text
send()
```

Specific implementation:

```text
Email → email server
SMS   → telecom gateway
Push  → push notification service
```

This is a very realistic software design use case.

---

# 16. Real-Time Example 11 — Media System

Consider:

```text
                    Media
                  /   |    \
                 ↓    ↓     ↓
               Audio Video  Image
```

Common:

```text
open()
close()
```

Specific:

```text
Audio → play()
Video → play()
Image → render()
```

This is a useful example for understanding common and specialized behavior.

---

# 17. Real-Time Example 12 — Transport System

Consider:

```text
                   Transport
                 /     |      \
                ↓      ↓       ↓
              Bus     Train    Flight
```

Common:

```text
start()
stop()
```

Specific:

```text
Bus    → pickupPassengers()
Train  → operateRailway()
Flight → fly()
```

Again, the parent captures common behavior.

---

# 18. The Core Design Idea

The most important design idea behind hierarchical inheritance is:

> [!important]
> **Put common functionality in the parent and specialized functionality in the child classes.**

Example:

```text
                    Employee
                       |
            +----------+----------+
            |                     |
            ↓                     ↓
        Developer              Manager
            |                     |
        writeCode()           manageTeam()
```

Common:

```text
login()
logout()
salary()
```

Specific:

```text
Developer → coding behavior
Manager   → management behavior
```

This avoids repeating common code.

---

# 19. Parent and Child Responsibility

A good hierarchy separates responsibility.

### Parent

Should contain:

- Common state
- Common behavior
- General functionality

### Child

Should contain:

- Specialized state
- Specialized behavior
- Additional functionality
- Overrides when required

Example:

```text
Vehicle
│
├── start()
├── stop()
│
├── Car
│   └── openTrunk()
│
└── Bike
    └── kickStart()
```

This creates a clean separation.

---

# 20. Inheritance Tree

A hierarchy can contain many levels.

Example:

```text
                    Animal
                 /    |    \
                /     |     \
              Dog     Cat    Cow
             /   \
            ↓     ↓
        Bulldog  Labrador
```

The top-level relationship:

```text
Animal → Dog
Animal → Cat
Animal → Cow
```

is hierarchical.

Then:

```text
Dog → Bulldog
Dog → Labrador
```

adds another level.

This means a real hierarchy can combine inheritance patterns.

> [!important]
> A class structure does not always belong to only one simple inheritance category. Different portions of the hierarchy can exhibit different patterns.

---

# 21. Hierarchical + Multilevel Together

Consider:

```text
                    Animal
                  /       \
                 ↓         ↓
               Dog        Cat
              /   \
             ↓     ↓
          Bulldog Labrador
```

Here:

```text
Animal → Dog
Animal → Cat
```

is hierarchical.

And:

```text
Animal → Dog → Bulldog
```

is multilevel.

Therefore, the overall hierarchy combines multiple inheritance patterns.

This is a common interview trick.

> [!important]
> **Do not classify the entire diagram blindly. Analyze the exact relationship being asked.**

---

# 22. Method Overriding in Hierarchical Inheritance

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

    class Cat extends Animal {

        @Override
        void sound() {
            System.out.println("Meow");
        }
    }

Now:

    Dog dog = new Dog();
    dog.sound();

    Cat cat = new Cat();
    cat.sound();

Output:

```text
Bark
Meow
```

The same inherited method name:

```text
sound()
```

has different behavior in different child classes.

This connects hierarchical inheritance with polymorphism.

---

# 23. Parent Reference + Child Object

This is extremely important for interviews.

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

    Animal a1 = new Dog();
    Animal a2 = new Cat();

    a1.sound();
    a2.sound();

Output:

```text
Dog
Cat
```

Why?

Because the actual object determines the overridden instance method implementation at runtime.

```text
a1
 ↓
Dog object
 ↓
Dog.sound()

a2
 ↓
Cat object
 ↓
Cat.sound()
```

Therefore:

$$
\boxed{\text{Hierarchical Inheritance + Overriding} \rightarrow \text{Runtime Polymorphism}}
$$

---

# 24. High-Level Mental Model

Think of hierarchical inheritance like a company.

```text
                    Company
                  /         \
                 /           \
                ↓             ↓
          Engineering       HR
             /   \           |
            ↓     ↓          ↓
       Development Testing Recruitment
```

The company provides common organizational rules.

Each department specializes in different responsibilities.

Similarly:

```text
Parent
 ↓
Common functionality

Child
 ↓
Specialized functionality
```

---

# 25. Hierarchical Inheritance vs Multiple Inheritance

This is one of the most frequently confused concepts.

### Hierarchical

```text
       A
      / \
     B   C
```

One parent.

Multiple children.

### Multiple

```text
     A   B
      \ /
       C
```

Multiple parents.

One child.

### Golden Difference

> [!important]
> **Look at the arrows.**
>
> ```text
> One → Many = Hierarchical
> Many → One = Multiple
> ```

This is one of the fastest exam tricks.

---

# 26. Hierarchical vs Single Inheritance

### Single

```text
A
|
B
```

One parent.

One child.

### Hierarchical

```text
   A
  / \
 B   C
```

One parent.

Multiple children.

### Shortcut

```text
1 → 1 = Single
1 → Many = Hierarchical
```

---

# 27. Hierarchical vs Multilevel

### Hierarchical

```text
      A
     / \
    B   C
```

Think:

```text
Branch
```

### Multilevel

```text
A
|
B
|
C
```

Think:

```text
Chain
```

### Fast Trick

> [!tip]
> **Branch = Hierarchical**
>
> **Chain = Multilevel**

---

# 28. Hierarchical vs Hybrid

A hybrid hierarchy combines two or more inheritance patterns.

Example:

```text
             A
           /   \
          B     C
          |
          D
```

Here:

```text
A → B
A → C
B → D
```

This combines:

```text
Hierarchical
+
Multilevel
```

Therefore it can be considered a hybrid structure.

---

# 29. Constructor Execution in Hierarchical Inheritance

Consider:

    class Parent {

        Parent() {
            System.out.println("Parent");
        }
    }

    class ChildA extends Parent {

        ChildA() {
            System.out.println("ChildA");
        }
    }

    class ChildB extends Parent {

        ChildB() {
            System.out.println("ChildB");
        }
    }

Now:

    ChildA a = new ChildA();

Output:

```text
Parent
ChildA
```

And:

    ChildB b = new ChildB();

Output:

```text
Parent
ChildB
```

### Key Idea

Each child object initializes its own parent portion first.

> [!important]
> Hierarchical inheritance does **not** mean all child constructors execute together.

Only the constructor chain belonging to the object being created executes.

---

# 30. Static Members in Hierarchical Inheritance

Suppose:

    class Parent {

        static int count = 10;
    }

    class ChildA extends Parent {
    }

    class ChildB extends Parent {
    }

Both child classes can access the inherited static member through the class hierarchy.

Conceptually:

```text
             Parent
               |
       +-------+-------+
       |               |
    ChildA           ChildB
       |               |
       +------ count --+
```

The static field belongs to the class where it is declared, not to separate copies automatically created for every child.

This is an important interview distinction.

---

# 31. `super` in Hierarchical Inheritance

Consider:

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

The output is:

```text
Animal sound
Bark
```

Here:

```text
super.sound()
→ Parent's implementation
```

---

# 32. Access Modifiers in Hierarchical Inheritance

Suppose:

    class Parent {

        private int a = 10;
        protected int b = 20;
        public int c = 30;
    }

    class ChildA extends Parent {

    }

    class ChildB extends Parent {

    }

Both subclasses can access members according to Java's access rules.

The important rule:

```text
private → not directly accessible
protected → accessible according to protected rules
public → accessible
package-private → package dependent
```

Do not confuse inheritance with unrestricted access.

---

# 33. Real Software Architecture Connection

In professional software, inheritance is often used to model:

```text
Common abstraction
       ↓
Specialized implementations
```

For example:

```text
                Employee
              /         \
             ↓           ↓
        Developer      Manager
```

The parent can define:

```text
name
id
login()
logout()
```

The children define specialized responsibilities.

However, modern software design often prefers interfaces and composition when they provide more flexibility.

> [!important]
> **Inheritance is a design tool, not simply a code-reuse shortcut.**

---

# 34. IS-A Relationship

Hierarchical inheritance is based on multiple IS-A relationships.

Example:

```text
Dog IS-A Animal
Cat IS-A Animal
Cow IS-A Animal
```

Therefore:

```text
Animal
 / | \
Dog Cat Cow
```

All child classes must logically be a type of the parent.

If the relationship does not make sense, inheritance is probably the wrong design.

---

# 35. HAS-A Relationship Trap

Suppose:

```text
Car HAS-A Engine
```

Do not create:

    class Car extends Engine {
    }

That says:

```text
Car IS-A Engine
```

which is logically incorrect.

Instead:

    class Car {

        Engine engine;
    }

This represents composition.

> [!warning]
> **IS-A → Inheritance**
>
> **HAS-A → Composition/Aggregation**

---

# 36. Basic Examples

## Example 1 — Identify the Pattern

**Question**

What type of inheritance is this?

```text
        Animal
        /    \
       Dog   Cat
```

### Pattern

One parent has multiple children.

### Answer

$$
\boxed{\text{Hierarchical Inheritance}}
$$

---

## Example 2 — Identify the Parent

**Question**

    class A {
    }

    class B extends A {
    }

    class C extends A {
    }

Which class is the common parent?

### Analysis

Both `B` and `C` extend `A`.

Therefore:

$$
\boxed{A}
$$

---

## Example 3 — Identify Child Classes

**Question**

    class Vehicle {
    }

    class Car extends Vehicle {
    }

    class Bike extends Vehicle {
    }

Which classes are children?

### Answer

```text
Car
Bike
```

$$
\boxed{\text{Car and Bike}}
$$

---

# 37. Medium Examples

## Example 4 — Inherited Method

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

    class Cat extends Animal {

        void meow() {
            System.out.println("Meow");
        }
    }

Can a `Cat` object call `eat()`?

### Analysis

```text
Cat extends Animal
Animal contains eat()
```

Therefore:

```text
cat.eat()
```

is valid subject to the method's access level.

### Answer

$$
\boxed{\text{Yes}}
$$

---

## Example 5 — Output

**Question**

    class Parent {

        Parent() {
            System.out.println("P");
        }
    }

    class A extends Parent {

        A() {
            System.out.println("A");
        }
    }

    class B extends Parent {

        B() {
            System.out.println("B");
        }
    }

    public class Main {

        public static void main(String[] args) {

            B obj = new B();
        }
    }

### Analysis

Only the constructor chain for `B` executes.

```text
Parent
  ↓
B
```

### Answer

```text
P
B
```

---

## Example 6 — Overriding

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

    class Cat extends Animal {

        @Override
        void sound() {
            System.out.println("Cat");
        }
    }

What is printed?

    Animal a = new Cat();
    a.sound();

### Analysis

```text
Reference → Animal
Object → Cat
```

The overridden method in `Cat` is selected.

### Answer

```text
Cat
```

---

# 38. Advanced Examples

## Example 7 — Multiple Child Objects

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

    class Cat extends Animal {

        void meow() {
            System.out.println("Meow");
        }
    }

Now:

    Dog d = new Dog();
    Cat c = new Cat();

    d.eat();
    c.eat();

What is the output?

### Analysis

Both children inherit `eat()`.

Therefore:

```text
Eat
Eat
```

### Answer

$$
\boxed{\text{Eat, Eat}}
$$

---

## Example 8 — Parent Reference

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

    class Cat extends Animal {

        @Override
        void sound() {
            System.out.println("Cat");
        }
    }

    Animal a;

    a = new Dog();
    a.sound();

    a = new Cat();
    a.sound();

### Analysis

First:

```text
a → Dog
```

Output:

```text
Dog
```

Then:

```text
a → Cat
```

Output:

```text
Cat
```

### Answer

```text
Dog
Cat
```

---

## Example 9 — Identify All Patterns

**Question**

Consider:

```text
             Animal
            /      \
           Dog     Cat
           |
        Labrador
```

What inheritance patterns are present?

### Analysis

```text
Animal → Dog
Animal → Cat
```

This is hierarchical.

And:

```text
Animal → Dog → Labrador
```

This is multilevel.

Therefore the structure combines:

$$
\boxed{\text{Hierarchical + Multilevel}}
$$

This can be viewed as a hybrid inheritance structure.

---

## Example 10 — Constructor Trap

**Question**

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

    class C extends A {

        C() {
            System.out.println("C");
        }
    }

    B obj = new B();

What is the output?

### Common Wrong Answer

```text
A
B
C
```

This is wrong.

Why?

Because creating a `B` object does not create a `C` object.

Only the relevant inheritance chain executes.

### Correct Chain

```text
B
↓
A
```

### Answer

```text
A
B
```

> [!important]
> **Only the selected object's constructor chain executes.**

---

# 39. Shortcut Master Table

| Diagram | Pattern | Memory Trick |
|---|---|---|
| `A → B` | Single | One-to-one |
| `A → B → C` | Multilevel | Chain |
| `A → B` and `A → C` | Hierarchical | Branch |
| `A + B → C` | Multiple | Many parents |
| Combination of patterns | Hybrid | Mixed |

### Ultimate Recognition Rule

```text
A → B
    ↓
Single

A → B → C
    ↓
Multilevel

    A
   / \
  B   C
    ↓
Hierarchical

A   B
 \ /
  C
    ↓
Multiple

Mixed structures
    ↓
Hybrid
```

---

# 40. Pattern Recognition — A to Z

## Pattern 1 — One Parent, Many Children

> [!important]
> If multiple classes extend the same parent:
>
> ```text
> A
> ├── B
> ├── C
> └── D
> ```
>
> Think:
>
> **Hierarchical Inheritance**

---

## Pattern 2 — Common Functionality

> [!important]
> If several classes share common behavior:
>
> ```text
> Parent
> ├── commonMethod1()
> └── commonMethod2()
> ```
>
> and each child adds specialized behavior:
>
> **Think Hierarchical Inheritance.**

---

## Pattern 3 — Same Method, Different Behavior

> [!important]
> If:
>
> ```text
> Parent → sound()
> Dog → sound()
> Cat → sound()
> ```
>
> think:
>
> **Method Overriding + Hierarchical Inheritance**

---

## Pattern 4 — Parent Reference

> [!important]
> If you see:
>
> ```java
> Animal a = new Dog();
> ```
>
> check:
>
> 1. Parent reference
> 2. Child object
> 3. Overridden method
> 4. Runtime dispatch

---

## Pattern 5 — Constructor Question

> [!important]
> If the question asks constructor output:
>
> ```text
> Parent → Child
> ```
>
> think:
>
> **Parent constructor first.**

---

## Pattern 6 — Multiple Children

> [!important]
> If you see:
>
> ```text
> A
> ├── B
> ├── C
> └── D
> ```
>
> the arrows point downward from one common parent.
>
> **Hierarchical.**

---

## Pattern 7 — Multiple Parents

> [!important]
> If you see:
>
> ```text
> A   B
>  \ /
>   C
> ```
>
> do not call it hierarchical.
>
> This represents **Multiple Inheritance**.

---

## Pattern 8 — Chain

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
> think:
>
> **Multilevel**

---

## Pattern 9 — HAS-A

> [!important]
> If the statement says:
>
> ```text
> Car HAS-A Engine
> ```
>
> think:
>
> **Composition/Aggregation**
>
> not inheritance.

---

## Pattern 10 — IS-A

> [!important]
> If the statement says:
>
> ```text
> Dog IS-A Animal
> ```
>
> think:
>
> **Inheritance**

---

# 41. Interview Questions

## Beginner

### Q1. What is hierarchical inheritance?

**Answer:**

Hierarchical inheritance is an inheritance structure where multiple child classes inherit directly from the same parent class.

Example:

```text
       Animal
       /    \
      Dog   Cat
```

---

### Q2. What is the main characteristic?

**Answer:**

One parent class has multiple direct child classes.

---

### Q3. Which Java keyword is used?

**Answer:**

`extends`.

---

### Q4. Does Java support hierarchical inheritance?

**Answer:**

Yes. Java supports hierarchical inheritance.

---

### Q5. Give a real-world example.

**Answer:**

A common example is:

```text
Vehicle
 /    \
Car   Bike
```

Both `Car` and `Bike` inherit common behavior from `Vehicle`.

---

## Intermediate

### Q6. What is the difference between hierarchical and multilevel inheritance?

**Answer:**

Hierarchical:

```text
A
/ \
B C
```

Multilevel:

```text
A
|
B
|
C
```

Hierarchical has multiple children.

Multilevel has a chain.

---

### Q7. Can child classes override the same parent method differently?

**Answer:**

Yes.

For example:

```text
Animal → sound()

Dog → Bark
Cat → Meow
```

This demonstrates method overriding and can support runtime polymorphism.

---

### Q8. Can one child access another child’s methods?

**Answer:**

No, not merely because both have the same parent.

For example:

```text
Animal
 /   \
Dog  Cat
```

`Dog` does not automatically inherit methods defined only in `Cat`.

---

### Q9. Can a parent reference refer to different child objects?

**Answer:**

Yes.

Example:

    Animal a = new Dog();
    a = new Cat();

This is commonly used for runtime polymorphism.

---

### Q10. Why is hierarchical inheritance useful?

**Answer:**

It allows common functionality to be centralized in a parent while specialized behavior is implemented separately in different child classes.

---

## Advanced

### Q11. What is the relationship between hierarchical inheritance and polymorphism?

**Answer:**

A common parent type can be used as a reference for different child objects. If child classes override a parent method, runtime dispatch can select different implementations.

---

### Q12. What happens if two child classes override the same method?

**Answer:**

Each child can provide its own implementation.

Example:

```text
Animal.sound()

Dog.sound() → Bark
Cat.sound() → Meow
```

---

### Q13. Can hierarchical inheritance and multilevel inheritance exist in the same hierarchy?

**Answer:**

Yes.

Example:

```text
       Animal
       /    \
      Dog   Cat
      |
   Labrador
```

The hierarchy contains both branching and chaining.

---

### Q14. What is the biggest design concern with inheritance?

**Answer:**

Inheritance creates coupling between parent and child classes. An unnecessarily deep or rigid hierarchy can become difficult to maintain.

---

### Q15. When should composition be preferred?

**Answer:**

When the relationship is HAS-A rather than IS-A, or when flexible component-based behavior is more appropriate.

---

# 42. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Calling `A → B` Hierarchical

This is normally **single inheritance**, not hierarchical.

Hierarchical requires multiple child classes.

---

### Mistake 2 — Confusing Branch With Chain

```text
A
|
B
|
C
```

→ Multilevel.

```text
A
/ \
B C
```

→ Hierarchical.

---

### Mistake 3 — Confusing Hierarchical With Multiple

```text
A
/ \
B C
```

→ Hierarchical.

```text
A B
\ /
 C
```

→ Multiple.

---

### Mistake 4 — Thinking Sibling Classes Inherit From Each Other

Given:

```text
Animal
 /   \
Dog  Cat
```

`Dog` does not inherit from `Cat`.

Both inherit from `Animal`.

---

### Mistake 5 — Thinking Children Share Their Own Members

Given:

```text
Animal
 /   \
Dog  Cat
```

If `Dog` defines:

```text
bark()
```

`Cat` does not automatically get `bark()`.

---

### Mistake 6 — Assuming All Constructors Execute

If you create:

    new Dog();

and the hierarchy is:

```text
Animal
 /   \
Dog  Cat
```

only:

```text
Animal constructor
Dog constructor
```

execute.

The `Cat` constructor does not execute.

---

### Mistake 7 — Forgetting Runtime Dispatch

If:

    Animal a = new Cat();

and `Cat` overrides `sound()`:

```text
a.sound()
```

uses the `Cat` implementation.

---

### Mistake 8 — Using Inheritance Only for Code Reuse

Always ask:

```text
Is this genuinely IS-A?
```

If not, consider composition.

---

# 43. Placement Exam Strategy

When a multiple-choice question shows a class diagram, follow these steps.

## Step 1 — Count Parents

Ask:

```text
How many parent classes?
```

## Step 2 — Count Children

Ask:

```text
How many direct children?
```

## Step 3 — Look at the Shape

```text
Chain?
Branch?
Many parents?
```

## Step 4 — Classify

```text
A → B
→ Single

A → B → C
→ Multilevel

A → B
A → C
→ Hierarchical

A + B → C
→ Multiple
```

## Step 5 — Check for Mixed Patterns

If the diagram combines patterns:

```text
→ Hybrid
```

> [!tip]
> **Do not memorize names alone. Read the arrow structure.**

---

# 44. Fastest Exam Trick

> [!tip]
> Memorize this:

```text
1 Parent + 1 Child
        ↓
      Single

1 Parent + Many Children
        ↓
   Hierarchical

Chain of Levels
        ↓
    Multilevel

Many Parents + 1 Child
        ↓
     Multiple

Combination
        ↓
      Hybrid
```

This can solve most inheritance classification questions in seconds.

---

# 45. Formula Sheet

```text
Hierarchical Inheritance
= One Parent → Multiple Children

Basic Structure:

       Parent
      /      \
   Child    Child

Example:

      Animal
      /    \
     Dog   Cat

Java:

class Animal {
}

class Dog extends Animal {
}

class Cat extends Animal {
}

Key Rule:

1 Parent → Many Children
= Hierarchical

Chain:
A → B → C
= Multilevel

One-to-One:
A → B
= Single

Many-to-One:
A + B → C
= Multiple

Mixed:
Multiple patterns
= Hybrid

IS-A
= Inheritance

HAS-A
= Composition/Aggregation

Parent Reference:
Parent ref = new Child();

Overriding:
Same method
+
Different child implementation
=
Runtime Polymorphism

Constructor:
Parent constructor
↓
Child constructor
```

---

# 46. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Hierarchical inheritance means multiple child classes directly inherit from the same parent class.**

### Visual

```text
            Parent
           /      \
          ↓        ↓
       Child A   Child B
```

### Example

```text
          Vehicle
          /     \
        Car     Bike
```

### Remember

- One parent → multiple children.
- Uses `extends` for class inheritance.
- Parent contains common functionality.
- Children contain specialized functionality.
- Child classes do not inherit from each other.
- Constructors execute only along the selected object's parent chain.
- Child classes can override the same parent method differently.
- Parent references can refer to different child objects.
- This can enable runtime polymorphism.
- `IS-A` indicates inheritance.
- `HAS-A` usually indicates composition/aggregation.
- Hierarchical ≠ multilevel.
- Hierarchical ≠ multiple.
- Hierarchical can appear together with multilevel inheritance in a larger hierarchy.
- Avoid unnecessary inheritance depth.
- Use inheritance when the relationship is genuinely meaningful.

### Master Diagram

```text
                    Parent
                /     |     \
               ↓      ↓      ↓
            Child1  Child2  Child3
```

### Master Recognition

```text
One → Many
   ↓
Hierarchical
```

### Golden Memory Trick

**Hierarchical inheritance looks like a tree branch: one parent at the top and multiple children below it.**

### One-Line Recognition

**If multiple classes directly extend the same parent class, immediately think Hierarchical Inheritance.**