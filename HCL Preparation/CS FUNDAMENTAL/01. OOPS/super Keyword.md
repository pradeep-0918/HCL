---
type: concept
subject: aptitude
topic: "super Keyword"
parent: "OOPS"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - java
  - super-keyword
  - inheritance
  - constructors
  - method-overriding
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Inheritance]]"
  - "[[Constructors]]"
  - "[[Method Overriding]]"
  - "[[this Keyword]]"
  - "[[Polymorphism]]"
  - "[[Encapsulation]]"
---

# super Keyword

> [!summary]
> The `super` keyword in Java is used inside a subclass to refer to the **immediate parent class**.
>
> The three core uses are:
>
>     super.variable
>     → Access parent class variable
>
>     super.method()
>     → Call parent class method
>
>     super(...)
>     → Call parent class constructor
>
> Core memory:
>
>     this
>     → Current class/object
>
>     super
>     → Immediate parent class

# 1. Core Concept

Inheritance allows one class to acquire properties and behavior from another class.

Example:

    class Animal {

        String name = "Animal";

        void sound() {

            System.out.println("Animal sound");
        }
    }

    class Dog extends Animal {

        String name = "Dog";

        void show() {

            System.out.println(name);
        }
    }

Here:

    Dog
      ↓
    extends
      ↓
    Animal

The `Dog` class inherits from `Animal`.

Inside `Dog`, the keyword:

    super

can be used to access the immediate parent-class members.

Therefore:

    super.name

means:

    Parent class's name

and:

    super.sound()

means:

    Parent class's sound() method

# 2. Basic Meaning

`super` is a special reference used by a subclass to access the immediate superclass.

Think:

    Child
      ↑
    Parent

Inside Child:

    this
    → current Child object

    super
    → parent-class part/reference

The most important distinction is:

| Keyword | Main Meaning |
|---|---|
| `this` | Current object/current class context |
| `super` | Immediate parent-class context |

# 3. Main Forms of `super`

Java mainly provides three important forms:

    super.variable

    super.method()

    super(...)

Each has a different purpose.

| Syntax | Purpose |
|---|---|
| `super.x` | Access parent variable |
| `super.show()` | Call parent method |
| `super()` | Call parent constructor |

# 4. Main Formula

There is no mathematical formula, but remember:

$$
\boxed{
super.x = \text{Parent class's } x
}
$$

$$
\boxed{
super.method() = \text{Parent class's method}
}
$$

$$
\boxed{
super(...) = \text{Parent class constructor}
}
$$

# 5. First Major Use — Parent Variable

Consider:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void show() {

            System.out.println(x);
            System.out.println(this.x);
            System.out.println(super.x);
        }
    }

Output:

    20
    20
    10

Why?

    x
    → Child's x

    this.x
    → Current object's Child x

    super.x
    → Parent's x

# 6. Variable Shadowing in Inheritance

This is one of the most important interview patterns.

Example:

    class Parent {

        int value = 100;
    }

    class Child extends Parent {

        int value = 200;

        void display() {

            System.out.println(value);
            System.out.println(super.value);
        }
    }

Output:

    200
    100

Recognition:

> [!important]
> If parent and child have fields with the same name:
>
>     value
>     → Child field
>
>     this.value
>     → Child field
>
>     super.value
>     → Parent field

# 7. Real-Time Example — Vehicle and Car

    class Vehicle {

        String brand = "Toyota";
    }

    class Car extends Vehicle {

        String brand = "BMW";

        void showBrand() {

            System.out.println(this.brand);
            System.out.println(super.brand);
        }
    }

Create:

    Car car = new Car();

    car.showBrand();

Output:

    BMW
    Toyota

Interpretation:

    this.brand
    → Car's brand

    super.brand
    → Vehicle's brand

# 8. Real-Time Example — Employee

    class Employee {

        String role = "Employee";
    }

    class Manager extends Employee {

        String role = "Manager";

        void displayRole() {

            System.out.println(
                this.role
            );

            System.out.println(
                super.role
            );
        }
    }

Output:

    Manager
    Employee

This is useful when parent and child maintain fields with related names.

# 9. Second Major Use — Calling Parent Method

Suppose:

    class Parent {

        void show() {

            System.out.println(
                "Parent show"
            );
        }
    }

    class Child extends Parent {

        void show() {

            System.out.println(
                "Child show"
            );
        }
    }

The child overrides the parent method.

Normally:

    show();

inside `Child` refers to the child's implementation.

To explicitly call the parent version:

    super.show();

# 10. Method Overriding + `super`

Example:

    class Animal {

        void sound() {

            System.out.println(
                "Animal makes sound"
            );
        }
    }

    class Dog extends Animal {

        @Override
        void sound() {

            System.out.println(
                "Dog barks"
            );
        }

        void test() {

            sound();
            super.sound();
        }
    }

Calling:

    new Dog().test();

Output:

    Dog barks
    Animal makes sound

Why?

    sound()
    → Child's overridden method

    super.sound()
    → Parent's method

# 11. Real-Time Example — Payment System

Consider:

    class Payment {

        void process() {

            System.out.println(
                "Generic payment processing"
            );
        }
    }

    class CreditCardPayment
        extends Payment {

        @Override
        void process() {

            super.process();

            System.out.println(
                "Credit card validation"
            );
        }
    }

Here the child extends the parent behavior.

Execution:

    super.process()
    ↓
    Generic processing

    Child code
    ↓
    Credit-card-specific processing

This pattern is useful when a subclass wants to **reuse parent behavior and then add its own behavior**.

# 12. Real-Time Example — Logging

    class Service {

        void execute() {

            System.out.println(
                "Base service execution"
            );
        }
    }

    class UserService extends Service {

        @Override
        void execute() {

            super.execute();

            System.out.println(
                "User service execution"
            );
        }
    }

The child does not completely replace the parent behavior.

Instead:

    Parent behavior
        +
    Child behavior

# 13. Third Major Use — Calling Parent Constructor

The third major use is:

    super(...)

This invokes a constructor of the immediate parent class.

Example:

    class Parent {

        Parent() {

            System.out.println(
                "Parent constructor"
            );
        }
    }

    class Child extends Parent {

        Child() {

            super();

            System.out.println(
                "Child constructor"
            );
        }
    }

Create:

    new Child();

Output:

    Parent constructor
    Child constructor

# 14. Constructor Execution Order

When creating a child object:

    new Child();

the parent constructor executes before the child constructor body.

Conceptually:

    Child object creation
          ↓
    Parent initialization
          ↓
    Parent constructor
          ↓
    Child initialization
          ↓
    Child constructor

This is a critical inheritance concept.

# 15. Why Does Parent Constructor Execute First?

A child object contains inherited state from the parent.

Therefore Java initializes the superclass portion before completing subclass initialization.

Think:

    Parent
       ↓
    Child

Initialization:

    Parent first
       ↓
    Child second

# 16. `super()` Must Be First Statement

Example:

    class Child extends Parent {

        Child() {

            super();

            System.out.println(
                "Child"
            );
        }
    }

This is valid.

But:

    Child() {

        System.out.println(
            "Child"
        );

        super();
    }

is invalid.

> [!important]
> **A constructor invocation using `super(...)` must be the first statement in the constructor.**

# 17. `super()` vs `super(...)`

These are related.

    super();

calls the no-argument parent constructor.

    super(100);

calls a parent constructor that accepts one argument.

Example:

    class Parent {

        Parent(int x) {

            System.out.println(x);
        }
    }

    class Child extends Parent {

        Child() {

            super(100);
        }
    }

Output:

    100

# 18. Constructor Chaining

Consider:

    class Parent {

        Parent() {

            System.out.println("P");
        }
    }

    class Child extends Parent {

        Child() {

            super();

            System.out.println("C");
        }
    }

Execution:

    new Child();

    ↓

    super()

    ↓

    Parent()

    ↓

    P

    ↓

    Child constructor

    ↓

    C

Output:

    P
    C

# 19. `super()` Is Implicit

If you do not explicitly write a constructor invocation, Java may insert:

    super();

as the first statement of a constructor, provided the parent has an accessible no-argument constructor.

Example:

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

Conceptually Java treats it like:

    Child() {

        super();

        System.out.println("Child");
    }

Output:

    Parent
    Child

# 20. Important Trap — Parent Has No Default Constructor

Consider:

    class Parent {

        Parent(int x) {
        }
    }

    class Child extends Parent {

        Child() {
        }
    }

This fails to compile.

Why?

The child constructor implicitly tries:

    super();

But `Parent` does not have a no-argument constructor.

Therefore you must explicitly call:

    super(10);

Correct:

    class Child extends Parent {

        Child() {

            super(10);
        }
    }

# 21. Recognition Trick — Constructor Error

> [!important]
> If:
>
>     Parent has only parameterized constructor
>
> and:
>
>     Child constructor does not explicitly call super(...)
>
> think:
>
> **Compilation error**
>
> because Java tries to call:
>
>     super()
>
> automatically.

This is one of the most common Java interview traps.

# 22. `super` and Parameterized Parent Constructor

Example:

    class Person {

        String name;

        Person(String name) {

            this.name = name;
        }
    }

    class Student extends Person {

        int rollNo;

        Student(
            String name,
            int rollNo
        ) {

            super(name);

            this.rollNo = rollNo;
        }
    }

Create:

    Student s =
        new Student(
            "Arun",
            101
        );

Execution:

    super(name)
    ↓
    Person(name)
    ↓
    this.name = name

Then:

    this.rollNo = rollNo

# 23. Real-Time Example — User and Admin

    class User {

        String username;

        User(String username) {

            this.username = username;
        }
    }

    class Admin extends User {

        String role;

        Admin(
            String username,
            String role
        ) {

            super(username);

            this.role = role;
        }
    }

Create:

    Admin admin =
        new Admin(
            "pradeep",
            "ADMIN"
        );

The parent initializes:

    username

The child initializes:

    role

This demonstrates constructor delegation.

# 24. `this()` vs `super()`

This is one of the highest-priority interview comparisons.

| Syntax | Meaning |
|---|---|
| `this()` | Call another constructor in same class |
| `super()` | Call parent constructor |
| `this(...)` | Same-class constructor with arguments |
| `super(...)` | Parent constructor with arguments |

Memory:

    this(...)
    → Same class

    super(...)
    → Parent class

# 25. Constructor First-Statement Rule

A constructor can begin with either:

    this(...)

or:

    super(...)

but not both.

Example:

    Child() {

        this(10);
    }

valid.

But:

    Child() {

        super();
        this(10);
    }

invalid.

Also:

    Child() {

        this(10);
        super();
    }

invalid.

Why?

A constructor cannot directly invoke two constructors.

# 26. Constructor Chaining Graph

Consider:

    class Child extends Parent {

        Child() {

            this(10);
        }

        Child(int x) {

            super(x);
        }
    }

Execution:

    Child()
       ↓
    this(10)
       ↓
    Child(int)
       ↓
    super(x)
       ↓
    Parent(int)

The chain is:

    Child()
      ↓
    Child(int)
      ↓
    Parent(int)

# 27. Important Rule — Constructor Cycle

Java does not allow constructor invocation cycles.

For example:

    Child() {

        this(10);
    }

    Child(int x) {

        this();
    }

This creates:

    Child()
      ↓
    Child(int)
      ↓
    Child()
      ↓
    ...

This is invalid.

> [!warning]
> Constructor chaining must eventually reach a superclass constructor. It cannot form a cycle.

# 28. `super` Always Refers to Immediate Parent

Suppose:

    class A {
    }

    class B extends A {
    }

    class C extends B {
    }

Inside `C`:

    super

refers to:

    B

not directly to:

    A

Therefore:

    C
    ↓
    super
    ↓
    B

This is an important inheritance rule.

# 29. Three-Level Inheritance

Example:

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

Output:

    30
    20

Why not 10?

Because:

    super

means immediate parent:

    C → B

It does not directly mean:

    C → A

# 30. Accessing Grandparent Members

Java does not provide syntax such as:

    super.super.x

This is invalid.

You cannot directly use repeated `super` to skip the immediate parent.

If a grandparent member is inherited and not hidden, normal inherited access may reach it, but there is no direct:

    super.super

syntax.

# 31. `super.super` Interview Trap

Question:

Can we write:

    super.super.show();

Answer:

No.

Java does not support chained `super.super` access.

Memory:

    super
    → immediate parent only

# 32. `super` and Parent Fields

Fields are not dynamically overridden like methods.

If parent and child both define:

    int x;

then:

    this.x

and:

    super.x

can refer to different fields.

Example:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void show() {

            System.out.println(
                super.x
            );
        }
    }

Output:

    10

# 33. Fields vs Methods

This distinction is extremely important.

Fields:

    hidden

Methods:

    overridden

Example:

    class Parent {

        int x = 10;

        void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {

        int x = 20;

        @Override
        void show() {

            System.out.println(
                "Child"
            );
        }
    }

Field behavior and method behavior are different.

# 34. `super` and Method Overriding

When a child overrides a method:

    super.method()

lets the child explicitly invoke the parent implementation.

Example:

    class Parent {

        void display() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {

        @Override
        void display() {

            System.out.println(
                "Child"
            );
        }

        void test() {

            super.display();
        }
    }

Output:

    Parent

# 35. Why Use `super.method()`?

There are several reasons:

    Reuse parent behavior
    Add child-specific behavior
    Avoid duplicating code
    Extend rather than completely replace behavior

Typical pattern:

    @Override
    void process() {

        super.process();

        // Additional child logic
    }

This is common in real applications.

# 36. Real-Time Example — Employee Processing

    class Employee {

        void calculateSalary() {

            System.out.println(
                "Base salary calculation"
            );
        }
    }

    class Manager extends Employee {

        @Override
        void calculateSalary() {

            super.calculateSalary();

            System.out.println(
                "Manager bonus calculation"
            );
        }
    }

The manager reuses the parent calculation and adds its own behavior.

# 37. Real-Time Example — Logging

    class Logger {

        void log() {

            System.out.println(
                "Base logging"
            );
        }
    }

    class FileLogger extends Logger {

        @Override
        void log() {

            super.log();

            System.out.println(
                "File logging"
            );
        }
    }

Execution:

    Base logging
    File logging

This demonstrates extension of behavior.

# 38. Real-Time Example — Framework Lifecycle

In framework-based code, a subclass may override a lifecycle method while still invoking the parent implementation.

Conceptually:

    @Override
    void initialize() {

        super.initialize();

        initializeChildComponents();
    }

The child extends the parent's initialization sequence.

# 39. `super` and Access Modifiers

The parent member must be accessible to the child.

For example:

    private

members cannot be directly accessed using:

    super.x

Example:

    class Parent {

        private int x = 10;
    }

    class Child extends Parent {

        void show() {

            // System.out.println(super.x);
        }
    }

This is invalid.

# 40. `super` and Protected Members

Protected members are commonly accessed from subclasses.

Example:

    class Parent {

        protected int x = 10;
    }

    class Child extends Parent {

        void show() {

            System.out.println(
                super.x
            );
        }
    }

This is valid.

# 41. `super` and Public Members

Public parent members can also be accessed.

Example:

    class Parent {

        public int x = 10;
    }

    class Child extends Parent {

        void show() {

            System.out.println(
                super.x
            );
        }
    }

Valid.

# 42. `super` and Default Members

Default/package-private members are accessible from a subclass when the subclass is in the same package.

Example:

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        void show() {

            System.out.println(
                super.x
            );
        }
    }

If both belong to the same package, access is valid.

# 43. `super` and Private Members

Private parent members are not directly accessible from the child.

Wrong:

    super.privateField

Private members belong to the declaring class's access boundary.

Use an accessible parent method if the parent provides one.

# 44. `super` and Private Methods

Example:

    class Parent {

        private void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {

        void test() {

            // super.show();
        }
    }

This is not valid because the private method is not directly accessible in the child.

Also, a private method is not overridden.

# 45. `super` and Final Methods

A final method cannot be overridden.

Example:

    class Parent {

        final void show() {
        }
    }

    class Child extends Parent {

        // Cannot override show()
    }

However, an inherited accessible final method can still be invoked normally.

The important point is:

    final
    → prevents overriding

not:

    prevents calling

# 46. `super` and Static Methods

Static methods are associated with classes rather than objects.

A subclass can access inherited static methods, but static methods are hidden rather than overridden.

Do not apply runtime polymorphism rules to static methods.

This is a common interview distinction.

# 47. `super` and Static Context

The `super` keyword is tied to a subclass instance context.

Therefore it cannot be used directly in a static method.

Example:

    class Child extends Parent {

        static void show() {

            // super.show();
        }
    }

This is invalid.

Why?

There is no current child instance in the static method.

# 48. `super` and Instance Context

Example:

    class Child extends Parent {

        void show() {

            super.show();
        }
    }

This is valid because `show()` is an instance method and there is a current object.

# 49. `super` and Constructor Initialization

Parent constructor:

    class Parent {

        Parent() {

            System.out.println(
                "Parent"
            );
        }
    }

Child constructor:

    class Child extends Parent {

        Child() {

            super();

            System.out.println(
                "Child"
            );
        }
    }

Execution order:

    Parent
    ↓
    Child

# 50. Real-Time Example — Person → Student

    class Person {

        String name;

        Person(String name) {

            this.name = name;
        }
    }

    class Student extends Person {

        int rollNo;

        Student(
            String name,
            int rollNo
        ) {

            super(name);

            this.rollNo = rollNo;
        }
    }

This separates responsibilities:

    Parent
    → common person state

    Child
    → student-specific state

# 51. Real-Time Example — Account → SavingsAccount

    class Account {

        protected double balance;

        Account(double balance) {

            this.balance = balance;
        }
    }

    class SavingsAccount
        extends Account {

        private double interestRate;

        SavingsAccount(
            double balance,
            double interestRate
        ) {

            super(balance);

            this.interestRate = interestRate;
        }
    }

The parent constructor initializes:

    balance

The child initializes:

    interestRate

# 52. Real-Time Example — Vehicle → Car

    class Vehicle {

        protected String brand;

        Vehicle(String brand) {

            this.brand = brand;
        }

        void start() {

            System.out.println(
                "Vehicle starts"
            );
        }
    }

    class Car extends Vehicle {

        Car(String brand) {

            super(brand);
        }

        @Override
        void start() {

            super.start();

            System.out.println(
                "Car starts"
            );
        }
    }

Here all three major uses can appear:

    super(brand)
    → parent constructor

    super.start()
    → parent method

    inherited brand
    → parent state

# 53. `super` in Constructor + Method Example

    class Parent {

        String name;

        Parent(String name) {

            this.name = name;
        }

        void show() {

            System.out.println(
                "Parent: " + name
            );
        }
    }

    class Child extends Parent {

        Child(String name) {

            super(name);
        }

        @Override
        void show() {

            super.show();

            System.out.println(
                "Child"
            );
        }
    }

Create:

    Child c =
        new Child("Arun");

    c.show();

Output:

    Parent: Arun
    Child

# 54. `this` vs `super` — Master Comparison

| Feature | `this` | `super` |
|---|---|---|
| Refers to | Current object | Immediate parent context |
| Field access | `this.x` | `super.x` |
| Method access | `this.show()` | `super.show()` |
| Constructor call | `this(...)` | `super(...)` |
| Constructor target | Same class | Parent class |
| Main use | Current object | Parent members |
| Static method | Not allowed | Not allowed |
| Used in inheritance | Yes | Yes |
| Can access parent private members | No | No |
| Constructor invocation first | `this(...)` | `super(...)` |

Memory:

    this
    ↓
    CURRENT

    super
    ↓
    PARENT

# 55. `this()` vs `super()`

| Feature | `this(...)` | `super(...)` |
|---|---|---|
| Target | Same class | Parent class |
| Purpose | Constructor chaining | Parent initialization |
| Must be first | Yes | Yes |
| Both in same constructor | No | No |
| Can be used in ordinary method | No | No |

# 56. Constructor Execution Pattern

Consider:

    class A {

        A() {

            System.out.println("A");
        }
    }

    class B extends A {

        B() {

            super();

            System.out.println("B");
        }
    }

    class C extends B {

        C() {

            super();

            System.out.println("C");
        }
    }

Create:

    new C();

Execution:

    C()
      ↓
    B()
      ↓
    A()
      ↓
    A
      ↓
    B
      ↓
    C

Output:

    A
    B
    C

Recognition:

> [!tip]
> For constructor output questions:
>
> **Go upward first, then come back downward.**
>
>     Child creation
>        ↓
>     Parent constructor
>        ↓
>     Grandparent constructor
>        ↓
>     Return downward
>        ↓
>     Child constructor

# 57. Constructor Output Shortcut

When you see:

    new Child();

immediately trace:

    Child constructor
        ↓
    super()
        ↓
    Parent constructor
        ↓
    super()
        ↓
    Grandparent constructor

The deepest constructor prints first.

Then execution returns upward toward the child.

# 58. Output Question 1 — Basic `super.x`

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void show() {

            System.out.println(
                super.x
            );
        }
    }

    new Child().show();

Output:

    10

# 59. Output Question 2 — `this` vs `super`

    class Parent {

        int x = 10;
    }

    class Child extends Parent {

        int x = 20;

        void show() {

            System.out.println(this.x);
            System.out.println(super.x);
        }
    }

    new Child().show();

Output:

    20
    10

# 60. Output Question 3 — Overriding

    class Parent {

        void show() {

            System.out.println("P");
        }
    }

    class Child extends Parent {

        @Override
        void show() {

            System.out.println("C");
        }

        void test() {

            show();
            super.show();
        }
    }

    new Child().test();

Output:

    C
    P

# 61. Output Question 4 — Constructor Order

    class Parent {

        Parent() {

            System.out.println("P");
        }
    }

    class Child extends Parent {

        Child() {

            super();

            System.out.println("C");
        }
    }

    new Child();

Output:

    P
    C

# 62. Output Question 5 — Parameterized Constructor

    class Parent {

        Parent(int x) {

            System.out.println(x);
        }
    }

    class Child extends Parent {

        Child() {

            super(100);
        }
    }

    new Child();

Output:

    100

# 63. Output Question 6 — `this()` + `super()`

    class Parent {

        Parent(int x) {

            System.out.println(
                "Parent " + x
            );
        }
    }

    class Child extends Parent {

        Child() {

            this(10);

            System.out.println(
                "Child no arg"
            );
        }

        Child(int x) {

            super(x);

            System.out.println(
                "Child int"
            );
        }
    }

    new Child();

Execution:

    Child()
       ↓
    this(10)
       ↓
    Child(int)
       ↓
    super(10)
       ↓
    Parent(10)

Output:

    Parent 10
    Child int
    Child no arg

# 64. Output Question 7 — Three-Level Constructor Chain

    class A {

        A() {

            System.out.println("A");
        }
    }

    class B extends A {

        B() {

            super();

            System.out.println("B");
        }
    }

    class C extends B {

        C() {

            super();

            System.out.println("C");
        }
    }

    new C();

Output:

    A
    B
    C

# 65. Output Question 8 — Parent Method Reuse

    class Parent {

        void show() {

            System.out.println("P");
        }
    }

    class Child extends Parent {

        @Override
        void show() {

            super.show();

            System.out.println("C");
        }
    }

    new Child().show();

Output:

    P
    C

# 66. Output Question 9 — Parent Field

    class Parent {

        String name = "Parent";
    }

    class Child extends Parent {

        String name = "Child";

        void show() {

            System.out.println(name);
            System.out.println(super.name);
        }
    }

    new Child().show();

Output:

    Child
    Parent

# 67. Output Question 10 — Parent Constructor + Child Field

    class Parent {

        Parent() {

            show();
        }

        void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {

        @Override
        void show() {

            System.out.println(
                "Child"
            );
        }
    }

    new Child();

Output:

    Child

The parent constructor calls an overridable method, and dynamic dispatch can invoke the child's override.

This is why calling overridable methods from constructors can be dangerous.

# 68. Important Constructor Trap

Suppose:

    class Parent {

        Parent() {

            show();
        }

        void show() {
        }
    }

    class Child extends Parent {

        int x = 100;

        @Override
        void show() {

            System.out.println(x);
        }
    }

    new Child();

The child field initialization has not completed when the parent constructor executes.

Therefore:

    x

may still contain its default value:

    0

This is a classic advanced interview question.

# 69. Recognition Trick — Parent Constructor Calls Method

> [!warning]
> If you see:
>
>     Parent constructor
>     +
>     overridden method
>
> immediately check initialization order.
>
> Parent constructor executes before child instance-field initialization.
>
> Therefore child fields may still have default values.

# 70. `super` and Dynamic Method Dispatch

Consider:

    class Parent {

        void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {

        @Override
        void show() {

            System.out.println(
                "Child"
            );
        }

        void test() {

            super.show();
        }
    }

`super.show()` explicitly invokes the parent implementation.

This bypasses normal dynamic dispatch for that specific invocation.

# 71. `this.show()` vs `super.show()`

Inside Child:

    this.show();

means:

    Current object's method

While:

    super.show();

means:

    Parent implementation

If the child overrides `show()`:

    this.show()
    → Child.show()

    super.show()
    → Parent.show()

This is a very high-value interview distinction.

# 72. `super` Does Not Create a New Object

This is a common misconception.

When you write:

    super.show();

Java does not create a separate parent object.

It accesses the parent-class implementation associated with the current inherited object.

Think:

    One Child Object
         ↓
    Parent state + Child state

`super` provides parent-level access to that object.

# 73. Deep Concept — One Object, Multiple Class Views

Suppose:

    Child c = new Child();

There is one object.

Conceptually:

    [ Parent part ]
    [ Child part  ]
           ↑
        one object

Inside Child:

    this
    → current object

    super
    → parent-class context

So `super` does not mean "another object".

# 74. Real-Time Analogy

Imagine:

    Employee
       ↓
    Manager

A manager is also an employee.

The manager object contains employee-related state plus manager-specific state.

`super` lets the manager access employee-level behavior.

    this
    → Manager view/current object

    super
    → Employee-level implementation

# 75. `super` and Template-Like Behavior

A parent class may provide a general algorithm:

    class Report {

        void generate() {

            validate();
            format();
            save();
        }
    }

A subclass can override one part or extend behavior.

The use of:

    super.generate();

can allow the subclass to reuse parent behavior before adding specialized behavior.

This is useful when designing extensible class hierarchies.

# 76. `super` and Protected Design

A parent class may intentionally expose certain members to subclasses using:

    protected

Example:

    class Framework {

        protected void initialize() {
        }
    }

    class Application
        extends Framework {

        @Override
        protected void initialize() {

            super.initialize();

            // App-specific initialization
        }
    }

This demonstrates controlled inheritance-based extensibility.

# 77. `super` and Constructor Injection

Example:

    class Repository {

        protected String connection;

        Repository(String connection) {

            this.connection = connection;
        }
    }

    class UserRepository
        extends Repository {

        UserRepository(String connection) {

            super(connection);
        }
    }

The subclass delegates common initialization to the parent.

# 78. Advanced Interview Question — Does `super()` Always Appear in Bytecode?

Conceptually, every constructor must establish the superclass constructor chain.

If you omit an explicit constructor invocation, Java inserts an implicit `super()` when applicable at source level.

At bytecode level, constructor invocation is represented through constructor invocation instructions.

For placement interviews, remember the source-level rule:

    Missing explicit super(...)
    +
    Accessible no-arg parent constructor
    =
    Implicit super()

# 79. Advanced Interview Question — What If Parent Constructor Is Private?

Suppose:

    class Parent {

        private Parent() {
        }
    }

    class Child extends Parent {
    }

The child cannot call the private parent constructor.

Therefore the inheritance setup fails because the superclass constructor is inaccessible.

# 80. Advanced Interview Question — Can `super()` Call a Private Parent Constructor?

No.

Private constructors are accessible only within the declaring class.

A subclass cannot directly invoke them.

# 81. Advanced Interview Question — Can `super` Access Parent Private Fields?

No.

Example:

    class Parent {

        private int x;
    }

    class Child extends Parent {

        void show() {

            // System.out.println(super.x);
        }
    }

This fails.

Use an accessible method provided by the parent if one exists.

# 82. Advanced Interview Question — Can `super` Access Parent Protected Members?

Yes, provided normal Java protected-access rules are satisfied.

This is one of the common purposes of `super`.

# 83. Advanced Interview Question — Can `super` Be Used in a Static Method?

No.

A static method has no current object instance.

# 84. Advanced Interview Question — Can `super` Be Used Outside a Subclass?

No.

`super` is specifically associated with superclass access from a subclass context.

# 85. Advanced Interview Question — Can We Use `super` in an Unrelated Class?

No.

Example:

    class A {
    }

    class B {

        void show() {

            // super.show();
        }
    }

This is invalid because `B` is not using `super` as a subclass context.

# 86. Advanced Interview Question — Can `super` Refer to Grandparent?

Not directly.

Inside:

    class C extends B

`super` refers to:

    B

not:

    A

when:

    B extends A

There is no:

    super.super

syntax.

# 87. Advanced Interview Question — Why Is `super` Useful?

Strong answer:

`super` allows a subclass to explicitly access inherited parent behavior, resolve field-name conflicts, invoke parent implementations of overridden methods, and delegate construction to the parent constructor.

# 88. Advanced Interview Question — Why Use `super(...)`?

Strong answer:

A subclass uses `super(...)` to initialize the superclass portion of the object and pass required constructor arguments to the parent class.

# 89. Advanced Interview Question — Why Use `super.method()`?

Strong answer:

When a subclass overrides a method, `super.method()` allows it to invoke the immediate parent's implementation and optionally extend that behavior with additional child-specific logic.

# 90. Advanced Interview Question — What Happens If Parent Has No No-Arg Constructor?

If the child does not explicitly call an accessible parent constructor, Java attempts to insert `super()`.

If no accessible no-argument parent constructor exists, compilation fails.

# 91. Advanced Interview Question — What Is Constructor Chaining?

Constructor chaining is the process of one constructor invoking another constructor.

Two forms:

    this(...)
    → same class

    super(...)
    → parent class

# 92. Advanced Interview Question — Which Executes First?

For a child object:

    Parent constructor
    executes before
    Child constructor body

Across multiple levels:

    Grandparent
       ↓
    Parent
       ↓
    Child

# 93. Advanced Interview Question — Can `this()` and `super()` Be Used Together?

Not directly in the same constructor because both must be the first statement.

A constructor can use:

    this(...)

which eventually calls:

    super(...)

through another constructor.

# 94. Advanced Interview Question — Can `super()` Be Called From a Normal Method?

No.

`super(...)` is constructor invocation syntax and can only be used from a constructor.

However:

    super.method()

can be used from an appropriate instance context.

# 95. Advanced Interview Question — Can `super.method()` Be Used in Constructor?

Yes, if the parent method is accessible.

Example:

    Child() {

        super.show();
    }

But remember that calling overridable methods during construction requires careful design.

# 96. Common Exam Patterns

> [!important] Must Master

1. `super` keyword definition
2. `super.variable`
3. `super.method()`
4. `super()`
5. `super(...)`
6. Parent field access
7. Parent method access
8. Parent constructor access
9. Variable hiding
10. Method overriding
11. `this` vs `super`
12. `this()` vs `super()`
13. Constructor chaining
14. Implicit `super()`
15. Parameterized parent constructor
16. Parent without default constructor
17. Three-level inheritance
18. Immediate parent rule
19. `super.super` trap
20. Private parent members
21. Protected parent members
22. Public parent members
23. Static method restrictions
24. Final method restrictions
25. Dynamic method dispatch
26. Parent constructor execution order
27. Constructor output questions
28. Parent constructor calling overridden method
29. Initialization-order traps
30. Real-world behavior extension

# 97. Shortcuts

> [!tip]
> **Shortcut 1 — Three Forms**
>
> Memorize:
>
>     super.x
>     → Parent variable
>
>     super.method()
>     → Parent method
>
>     super(...)
>     → Parent constructor

> [!tip]
> **Shortcut 2 — Current vs Parent**
>
>     this
>     → Current
>
>     super
>     → Parent

> [!tip]
> **Shortcut 3 — Constructor**
>
> If you see:
>
>     super(...)
>
> immediately jump to the parent constructor.

> [!tip]
> **Shortcut 4 — Constructor Output**
>
> For:
>
>     new Child()
>
> trace upward first:
>
>     Child
>       ↓
>     Parent
>       ↓
>     Grandparent
>
> Then read output while returning downward.

> [!tip]
> **Shortcut 5 — Parent Has Only Parameterized Constructor**
>
> If Child does not write:
>
>     super(value)
>
> expect:
>
>     Compilation Error
>
> because implicit `super()` cannot be resolved.

> [!tip]
> **Shortcut 6 — Overridden Method**
>
>     method()
>     → Child implementation
>
>     super.method()
>     → Parent implementation

> [!tip]
> **Shortcut 7 — Same Field Name**
>
>     this.x
>     → Child/current field
>
>     super.x
>     → Parent field

> [!tip]
> **Shortcut 8 — Immediate Parent**
>
>     super
>     → only immediate parent
>
> Never:
>
>     super.super

> [!tip]
> **Shortcut 9 — Private Parent Member**
>
> If parent member is private:
>
>     super.member
>     → Not directly accessible

> [!tip]
> **Shortcut 10 — Static Context**
>
> If you see:
>
>     static
>     +
>     super
>
> think:
>
>     Compilation Error

# 98. Recognition Tricks

> [!important]
> **If you see `super.x`, think "parent field."**

> [!important]
> **If you see `super.show()`, think "parent implementation of show."**

> [!important]
> **If you see `super(...)`, think "parent constructor."**

> [!important]
> **If parent and child have the same field name, use `super.field` to identify the parent field.**

> [!important]
> **If a child overrides a method and calls `super.method()`, the child is reusing/extending the parent behavior.**

> [!important]
> **If a child constructor has no explicit constructor call, check whether the parent has an accessible no-argument constructor.**

> [!important]
> **If you see `super.super`, mark it invalid.**

> [!important]
> **If `super` appears inside a static method, mark it invalid.**

# 99. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking `super` Creates a Parent Object

Wrong:

    super
    =
    new Parent()

Correct:

    super
    → parent-class context of the current inherited object

---

### Mistake 2 — Thinking `super` Means Grandparent

Wrong:

    super
    → any ancestor

Correct:

    super
    → immediate parent only

---

### Mistake 3 — Using `super.super`

This syntax does not exist in Java.

---

### Mistake 4 — Forgetting `super()` Is Implicit

If a child constructor does not explicitly call:

    this(...)

or:

    super(...)

Java attempts to insert:

    super();

provided an accessible no-arg parent constructor exists.

---

### Mistake 5 — Assuming Every Parent Has `super()`

Not true.

If the parent only has:

    Parent(int x)

then:

    super()

does not exist.

---

### Mistake 6 — Calling Private Parent Members with `super`

Private members are not directly accessible from the child.

---

### Mistake 7 — Confusing Field Hiding With Method Overriding

Fields are hidden.

Methods can be overridden.

Therefore:

    super.x

and:

    super.show()

follow different conceptual rules.

---

### Mistake 8 — Thinking `super.method()` Uses Dynamic Dispatch

`super.method()` explicitly selects the parent implementation.

---

### Mistake 9 — Putting `super()` After Another Statement

Constructor invocation must be first.

---

### Mistake 10 — Using `super()` Inside a Normal Method

`super(...)` is for constructor invocation.

---

### Mistake 11 — Using `super` in Static Context

A static method has no current object instance.

---

### Mistake 12 — Forgetting Constructor Order

Always remember:

    Parent constructor
       ↓
    Child constructor

# 100. Master Decision Tree

When you see `super`:

    What form?

        |
        +----------------+
        |                |
     super.x         super.method()
        |                |
    Parent field     Parent method
        |
        |
     super(...)
        |
    Parent constructor

Then ask:

    Is the parent member accessible?

        |
        +---- No → Compilation Error
        |
       Yes
        ↓
    Continue execution

# 101. Constructor Problem-Solving Framework

For:

    new Child()

use:

    Step 1
    Find Child constructor.

    Step 2
    Check for this(...).

    Step 3
    If absent, check super(...).

    Step 4
    If absent, assume super().

    Step 5
    Verify parent constructor exists.

    Step 6
    Execute parent constructor first.

    Step 7
    Return to child constructor.

    Step 8
    Continue child statements.

# 102. Output Problem Framework

When solving output questions involving `super`:

    Step 1
    Identify inheritance hierarchy.

    Step 2
    Mark fields with same names.

    Step 3
    Mark overridden methods.

    Step 4
    Separate:
        this.method()
        super.method()

    Step 5
    Trace constructor chain.

    Step 6
    Check initialization order.

    Step 7
    Execute statements in actual order.

This prevents most mistakes.

# 103. High-Level Real-World Pattern — Extend Parent Behavior

A strong use of `super` is:

    @Override
    void process() {

        super.process();

        additionalProcessing();
    }

Think:

    Parent behavior
         +
    Child behavior
         =
    Extended behavior

This is often better than copying the parent's code.

# 104. High-Level Real-World Pattern — Reuse Parent Constructor

Use:

    super(commonData);

when the parent is responsible for initializing common state.

Think:

    Common state
       ↓
    Parent

    Specialized state
       ↓
    Child

This follows a clean separation of responsibility.

# 105. High-Level Real-World Pattern — Parent API Extension

Example:

    class Notification {

        void send() {

            System.out.println(
                "Sending notification"
            );
        }
    }

    class EmailNotification
        extends Notification {

        @Override
        void send() {

            super.send();

            System.out.println(
                "Sending email-specific data"
            );
        }
    }

The subclass extends an existing abstraction.

# 106. High-Level Interview Answer

### Explain `super` in Java.

A strong interview answer:

> "`super` is a keyword used inside a subclass to access members of its immediate superclass. It can be used to access a parent field using `super.field`, invoke an overridden parent method using `super.method()`, and invoke a parent constructor using `super(...)`. A constructor invocation using `super(...)` must be the first statement of the constructor."

# 107. High-Level Interview Answer

### Difference between `this` and `super`

A strong answer:

> "`this` refers to the current object and is commonly used to access current-class members or invoke another constructor in the same class. `super` refers to the immediate superclass context and is used to access parent members or invoke the parent constructor."

# 108. High-Level Interview Answer

### Why is `super()` automatically inserted?

A child object must initialize its superclass portion before its own construction completes. Therefore Java inserts an implicit `super()` when no explicit constructor invocation is written and an accessible no-argument parent constructor exists.

# 109. High-Level Interview Answer

### Why use `super.method()`?

It allows a subclass to invoke the parent implementation of an overridden method. This is useful when the child wants to reuse the parent's behavior and then add specialized behavior.

# 110. High-Level Interview Answer

### Why can `super()` fail to compile?

If the parent class does not have an accessible no-argument constructor and the child does not explicitly invoke another accessible parent constructor, the compiler cannot establish the superclass constructor chain.

# 111. Formula Sheet

```text
SUPER KEYWORD

super
→ Immediate parent-class context

super.x
→ Parent class field x

super.method()
→ Parent class method implementation

super(...)
→ Parent class constructor

super()
→ Parent no-argument constructor

super(value)
→ Parent parameterized constructor

this
→ Current object

super
→ Immediate parent context

this(...)
→ Same-class constructor

super(...)
→ Parent constructor

Constructor Rule:

super(...)
→ Must be first statement

this(...)
→ Must be first statement

Cannot use both directly in one constructor.

If no explicit constructor invocation:

Java attempts:
super()

provided an accessible no-arg parent constructor exists.

Inheritance:

C extends B
B extends A

Inside C:

super
→ B

Not A.

No:
super.super

Fields:

this.x
→ Current/child field

super.x
→ Parent field

Methods:

this.show()
→ Current implementation

super.show()
→ Parent implementation

Private Parent Member:

super.privateMember
→ Not directly accessible

Static Context:

super
→ Cannot be used directly

Parent constructor order:

Grandparent
    ↓
Parent
    ↓
Child

Overridden method:

super.method()
→ Explicit parent implementation

Constructor chaining:

this(...)
→ Same class

super(...)
→ Parent class