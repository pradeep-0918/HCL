---
type: concept
subject: aptitude
topic: "Access Modifiers"
parent: "OOPS"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - access-modifiers
  - java
  - encapsulation
  - visibility
  - interview
  - quantitative-aptitude
wikilinks:
  - "[[OOPS]]"
  - "[[Encapsulation]]"
  - "[[Inheritance]]"
  - "[[Association]]"
  - "[[Constructors]]"
  - "[[Polymorphism]]"
---

# Access Modifiers

> [!summary]
> **Access modifiers** control where a class, method, constructor, variable, or other member can be accessed from.
>
> In Java, the four access levels are:
>
>     public
>     protected
>     default / package-private
>     private
>
> The most important interview pattern is:
>
>     public
>     → Everywhere
>
>     protected
>     → Same package + subclasses
>
>     default
>     → Same package only
>
>     private
>     → Same class only
>
> Fast recognition:
>
> **If a question asks "Can this member be accessed here?", identify the access modifier first, then identify the location of the accessing code.**

# 1. Core Concept

Access modifiers are Java's visibility-control mechanism.

They answer one fundamental question:

> **Who is allowed to access this class or member?**

Consider:

    class BankAccount {

        private double balance;

        public double getBalance() {
            return balance;
        }
    }

Here:

    balance
       ↓
    private
       ↓
    Direct external access is restricted

But:

    getBalance()
       ↓
    public
       ↓
    External code can call it

This is a major part of **encapsulation**.

The basic idea is:

    Hide internal data
          ↓
    Expose controlled operations
          ↓
    Protect object state

# 2. Basic Meaning

Access modifiers define the accessibility or visibility of program elements.

The four Java access levels are:

| Modifier | Basic Meaning |
|---|---|
| `public` | Accessible from anywhere, subject to normal type/module visibility rules |
| `protected` | Accessible within the same package and through inheritance from other packages |
| No modifier | Package-private; accessible within the same package |
| `private` | Accessible only within the declaring top-level class |

The four levels can be ordered from **most accessible to least accessible**:

    public
      ↓
    protected
      ↓
    default
      ↓
    private

A useful memory trick:

> [!tip]
> **P-P-D-P**
>
>     Public
>     Protected
>     Default
>     Private
>
> Think:
>
>     Everyone
>     Package + Child
>     Package
>     Class

# 3. Main Comparison Table

| Access Modifier | Same Class | Same Package | Subclass in Different Package | Unrelated Class in Different Package |
|---|---:|---:|---:|---:|
| `public` | Yes | Yes | Yes | Yes |
| `protected` | Yes | Yes | Yes, through inheritance rules | No |
| default | Yes | Yes | No | No |
| `private` | Yes | No | No | No |

This table is one of the most important things to memorize.

# 4. The Four Access Levels

## 4.1 `public`

`public` provides the widest accessibility.

Example:

    public class Student {

        public int id;

        public void display() {
            System.out.println(id);
        }
    }

Other accessible classes can use:

    Student s = new Student();

    s.id = 101;

    s.display();

Think:

    public
       ↓
    Maximum visibility

> [!important]
> **`public` means the member is accessible wherever the containing type and other Java access rules permit access.**

# 5. `private`

`private` provides the most restrictive member-level access.

Example:

    class BankAccount {

        private double balance;

        private void calculateInterest() {
        }
    }

The `balance` field cannot be directly accessed from an unrelated external class.

Wrong:

    BankAccount account = new BankAccount();

    account.balance = 5000;

This produces a compilation error because `balance` is private.

Think:

    private
       ↓
    Declaring class only

# 6. Default / Package-Private

When no access modifier is written, Java uses **package-private** access.

Example:

    class Student {

        int id;

        void display() {
            System.out.println(id);
        }
    }

Here:

    int id

has no modifier.

Therefore it is:

    package-private

It can be accessed by classes in the same package.

It cannot be directly accessed from unrelated classes in another package.

> [!important]
> **"default access" does not mean "public".**
>
> No modifier means:
>
>     package-private

# 7. `protected`

`protected` has two major access paths:

    Same package
        +
    Subclasses in other packages

Example:

    class Parent {

        protected int value;
    }

Classes in the same package can access `value`.

A subclass in another package can also access it through inheritance, subject to Java's protected-access rules.

This is where many interview questions become tricky.

# 8. Master Access Table

Use this table for rapid revision:

| Modifier | Class | Package | Subclass Outside Package | World |
|---|---|---|---|---|
| `public` | Yes | Yes | Yes | Yes |
| `protected` | Yes | Yes | Yes* | No |
| default | Yes | Yes | No | No |
| `private` | Yes | No | No | No |

`*` For a subclass in another package, protected access has special rules and is generally through inheritance rather than arbitrary access through a parent-class reference.

# 9. Recognition Trick

When you see an access question, use this order:

    STEP 1
    Identify modifier.

         ↓

    STEP 2
    Identify location of member.

         ↓

    STEP 3
    Identify location of accessing code.

         ↓

    STEP 4
    Check whether inheritance exists.

         ↓

    STEP 5
    Check whether package relationship matters.

         ↓

    STEP 6
    Decide:
    Compile-time access allowed or denied?

This is much faster than trying to memorize random examples.

# 10. `public` — Detailed Understanding

Consider:

    package college;

    public class Student {

        public int id;
    }

Another package:

    package company;

    import college.Student;

    class Test {

        void show() {

            Student s = new Student();

            s.id = 101;
        }
    }

The member is:

    public

Therefore access is allowed, assuming the class itself is accessible.

# 11. `private` — Detailed Understanding

    class Student {

        private int id;

        void setId(int id) {

            this.id = id;
        }

        int getId() {

            return id;
        }
    }

Outside:

    Student s = new Student();

    s.setId(101);

This works if the method is accessible.

But:

    s.id = 101;

does not work.

Why?

    id
    ↓
    private
    ↓
    Only declaring class

# 12. Why `private` Is Important

Private members are commonly used to implement encapsulation.

Example:

    class BankAccount {

        private double balance;

        public void deposit(double amount) {

            if (amount > 0) {
                balance += amount;
            }
        }

        public double getBalance() {

            return balance;
        }
    }

External code cannot directly modify:

    balance

Instead it uses:

    deposit()

This allows the class to control its state.

# 13. Real-Time Example — Banking System

Imagine a bank application.

You should not allow:

    account.balance = -500000;

because the state may become invalid.

Instead:

    account.deposit(5000);

or:

    account.withdraw(1000);

The class controls the rules.

Pattern:

    private data
         +
    public methods
         ↓
    controlled access
         ↓
    encapsulation

# 14. Real-Time Example — Student Marks

Bad design:

    class Student {

        public int marks;
    }

External code can do:

    student.marks = -500;

Better:

    class Student {

        private int marks;

        public void setMarks(int marks) {

            if (marks >= 0 && marks <= 100) {
                this.marks = marks;
            }
        }

        public int getMarks() {
            return marks;
        }
    }

Now the class controls valid values.

# 15. Real-Time Example — Employee Salary

Instead of:

    public double salary;

use:

    private double salary;

Then:

    public void setSalary(double salary) {

        if (salary >= 0) {
            this.salary = salary;
        }
    }

This prevents invalid state.

# 16. Real-Time Example — Authentication

Consider:

    class User {

        private String password;

        public boolean authenticate(String input) {

            return password.equals(input);
        }
    }

The password is hidden from direct external access.

This demonstrates why `private` is important for sensitive internal state.

# 17. `protected` — Detailed Understanding

Consider:

    class Animal {

        protected String name;
    }

Same package:

    class Dog {

        void show(Animal a) {

            System.out.println(a.name);
        }
    }

This is allowed because both are in the same package.

But outside the package, a subclass can access the protected member through inheritance.

# 18. `protected` in Same Package

Suppose:

    package animals;

    class Animal {

        protected int age;
    }

Another class:

    package animals;

    class Dog {

        void show() {

            Animal a = new Animal();

            a.age = 5;
        }
    }

This is allowed.

Why?

Both classes belong to:

    animals

and protected members are accessible throughout the same package.

# 19. `protected` in Different Package

Suppose:

    package animals;

    public class Animal {

        protected int age;
    }

Then:

    package pets;

    import animals.Animal;

    public class Dog extends Animal {

        void show() {

            age = 5;
        }
    }

This is allowed because:

    Dog extends Animal

and `age` is protected.

# 20. Important Protected Trap

This is where many interview questions test deep understanding.

Suppose:

    package animals;

    public class Animal {

        protected int age;
    }

And:

    package pets;

    import animals.Animal;

    public class Dog extends Animal {

        void show() {

            Dog d = new Dog();

            d.age = 5;
        }
    }

This is allowed because the access occurs through the subclass context.

But arbitrary access through a `Parent` reference from a different package is not generally allowed.

The exact rule matters more than a simple "subclass can access protected".

# 21. Advanced Protected Example

Suppose:

    package animals;

    public class Animal {

        protected int age;
    }

Then:

    package pets;

    import animals.Animal;

    public class Dog extends Animal {

        void test(Animal animal) {

            animal.age = 10;
        }
    }

This is not generally allowed merely because `Dog` is a subclass.

The protected access from another package must be through the subclass inheritance context, not arbitrary access through a superclass-typed reference.

A safer valid pattern is:

    void test(Dog dog) {

        dog.age = 10;
    }

This distinction is highly important for advanced Java interviews.

# 22. Default Access — Detailed Understanding

Example:

    class Student {

        int id;
    }

No modifier means:

    package-private

Same package:

    Student s = new Student();

    s.id = 101;

Allowed.

Different package:

    s.id = 101;

Not allowed.

Therefore:

    default
       ↓
    package boundary

# 23. `private` Across Packages

Private members ignore package relationships.

Example:

    class A {

        private int x;
    }

Whether another class is:

    Same package

or:

    Different package

does not matter.

Direct access is prohibited outside the declaring class.

# 24. Access Modifier Hierarchy

From widest to narrowest:

    public
       ↓
    protected
       ↓
    default
       ↓
    private

Memory:

> [!tip]
> **Public → Protected → Default → Private**
>
> Think:
>
>     World
>      ↓
>     Package + Inheritance
>      ↓
>     Package
>      ↓
>     Class

# 25. Important Difference: Class vs Member Access

Access modifiers behave differently for top-level classes and members.

A top-level class can generally be:

    public

or:

    package-private

A top-level class cannot be:

    private

or:

    protected

Example:

    public class Student {
    }

Valid.

Also:

    class Student {
    }

Valid.

But:

    private class Student {
    }

is invalid for a top-level class.

Similarly:

    protected class Student {
    }

is invalid for a top-level class.

# 26. Nested Classes

Nested classes are different.

A member or nested class can have access modifiers such as:

    public
    protected
    private
    package-private

Example:

    class Outer {

        private class Inner {
        }
    }

This is valid.

So remember:

    Top-level class
    → public or package-private

    Nested/member class
    → can use broader access modifiers

# 27. Public Class and File Name

If a top-level class is public:

    public class Student {
    }

the source file normally must be named:

    Student.java

This is a Java compilation rule related to public top-level types.

# 28. Multiple Top-Level Classes

A Java source file can contain multiple top-level classes if access rules permit.

For example:

    class A {
    }

    class B {
    }

Both can be package-private.

But you cannot have multiple public top-level classes in one source file under normal Java source-file rules.

# 29. Access Modifiers and Encapsulation

Access modifiers are one of the mechanisms used to achieve encapsulation.

Think:

    Encapsulation
         ↓
    Hide internal implementation
         ↓
    Restrict direct access
         ↓
    Expose controlled interface

Typical pattern:

    private fields
         +
    public methods
         ↓
    Controlled access

# 30. Access Modifiers and Abstraction

Do not confuse:

    Access Control

with:

    Abstraction

Access modifiers answer:

    "Who can access this?"

Abstraction answers:

    "What implementation details should be hidden from the user?"

They are related but not identical.

# 31. Access Modifiers and Inheritance

Inheritance affects `protected` access strongly.

Example:

    class Parent {

        protected int x;
    }

    class Child extends Parent {

        void show() {

            x = 10;
        }
    }

The child can access `x`.

But:

    private

members of the parent are not directly accessible in the child.

# 32. Private Members and Inheritance

Consider:

    class Parent {

        private int x = 10;
    }

    class Child extends Parent {

        void show() {

            System.out.println(x);
        }
    }

This fails.

Why?

    x
    ↓
    private
    ↓
    Parent only

The child cannot directly access it.

However, the parent object state still exists as part of the object. The child simply does not have direct access to the private member.

# 33. Protected vs Private in Inheritance

| Modifier | Child Same Package | Child Different Package |
|---|---:|---:|
| `private` | No direct access | No direct access |
| default | Yes | No |
| `protected` | Yes | Yes, through inheritance rules |
| `public` | Yes | Yes |

This is a very important comparison.

# 34. Protected vs Default

This is a common interview question.

| Feature | `protected` | default |
|---|---|---|
| Same package | Yes | Yes |
| Different-package subclass | Yes, through inheritance rules | No |
| Different-package unrelated class | No | No |
| Main purpose | Package + inheritance access | Package-only access |

Memory:

    protected
    = package + subclass access

    default
    = package only

# 35. Public vs Protected

| Feature | `public` | `protected` |
|---|---|---|
| Same class | Yes | Yes |
| Same package | Yes | Yes |
| Different package subclass | Yes | Yes, through inheritance rules |
| Different package unrelated class | Yes | No |

Memory:

    public
    → unrestricted by access modifier

    protected
    → restricted outside package unless inheritance context applies

# 36. Private vs Default

| Feature | `private` | default |
|---|---|---|
| Same class | Yes | Yes |
| Same package other class | No | Yes |
| Different package | No | No |

Memory:

    private
    → class boundary

    default
    → package boundary

# 37. Access Modifiers and Constructors

Constructors can also have access modifiers.

Example:

    public class Student {

        private Student() {
        }
    }

This is valid.

A private constructor prevents normal object creation from outside the class.

Example:

    Student s = new Student();

This fails outside the class because the constructor is private.

# 38. Real-Time Example — Singleton Pattern

A private constructor is commonly used in Singleton-style designs.

Example:

    class Singleton {

        private static Singleton instance;

        private Singleton() {
        }

        public static Singleton getInstance() {

            if (instance == null) {
                instance = new Singleton();
            }

            return instance;
        }
    }

The private constructor prevents external code from directly doing:

    new Singleton();

This is an important real-world use of private constructors.

# 39. Private Constructor and Utility Classes

A utility-style class may prevent object creation.

Example:

    final class MathUtils {

        private MathUtils() {
        }

        public static int square(int x) {

            return x * x;
        }
    }

Usage:

    int result = MathUtils.square(5);

No object is required.

The private constructor communicates:

    This class is not intended to be instantiated.

# 40. Access Modifiers and Methods

Methods can use all four access levels:

    public void a() {
    }

    protected void b() {
    }

    void c() {
    }

    private void d() {
    }

Their visibility follows the same basic hierarchy.

# 41. Access Modifiers and Fields

Fields can also use all four:

    public int a;

    protected int b;

    int c;

    private int d;

The same accessibility principles apply.

# 42. Access Modifiers and Static Members

Static fields and methods can also use access modifiers.

Example:

    class Counter {

        private static int count;

        public static int getCount() {

            return count;
        }
    }

Here:

    count
    → private static

    getCount()
    → public static

This is common in real applications.

# 43. Access Modifiers and Final Members

`final` and access modifiers solve different problems.

Example:

    private final int id;

Here:

    private
    → controls who can access it

    final
    → controls reassignment

Therefore:

    Access Modifier
    = Visibility

    final
    = Reassignment restriction

Do not confuse them.

# 44. Access Modifiers vs `static`

Similarly:

    private static int count;

means:

    private
    → visibility

    static
    → belongs to class rather than each object

Different keywords solve different problems.

# 45. Access Modifiers vs `final`

Example:

    public final int id;

means:

    public
    → accessible according to public access rules

    final
    → cannot be reassigned after initialization

One controls access.

The other controls reassignment.

# 46. Access Modifier and Method Overriding

A child class can override an inherited method, but it cannot reduce the method's visibility.

Example:

    class Parent {

        public void show() {
        }
    }

A child cannot do:

    class Child extends Parent {

        private void show() {
        }
    }

This attempts to reduce:

    public
    ↓
    private

which is not allowed.

# 47. Visibility Rule During Overriding

The overriding method must provide at least the same accessibility as the inherited method.

Example:

    Parent:

    protected void show()

Child can use:

    protected void show()

or:

    public void show()

But not:

    private void show()

Similarly:

    public
    → can remain public only

# 48. Why Cannot Visibility Be Reduced?

Suppose:

    Parent p = new Child();

If the parent promises:

    public void show()

the code using `Parent` expects `show()` to be accessible.

If `Child` reduced it to private, the subclass would violate the parent contract.

This connects access modifiers with the **Liskov Substitution Principle**.

# 49. Access Modifiers and Interface Methods

Interface methods are generally public as part of the interface contract.

Example:

    interface Payment {

        void pay();
    }

A class implementing it:

    class CreditCardPayment
        implements Payment {

        public void pay() {
        }
    }

The implementation cannot reduce the method to:

    protected

or:

    private

because it must satisfy the interface contract.

# 50. Common Interview Question

### Question

Can we reduce the visibility of an overridden method?

### Answer

No.

For example:

    public

cannot become:

    protected

or:

    private

in the overriding method.

Visibility can stay the same or become broader where Java permits it.

# 51. Access Modifiers and Packages

A package is a major boundary for:

    default
    protected

access.

Think:

    Same Package
        ↓
    default works
    protected works

Different Package
        ↓
    default fails
    protected may work through inheritance
    public works
    private fails

# 52. Package Recognition Trick

When a question mentions:

    package A
    package B

immediately think:

    default
    protected

These are the modifiers most affected by package boundaries.

# 53. Four-Question Method

For every access-modifier question, ask:

    Q1. What is the modifier?

    Q2. Is the accessing code in the same class?

    Q3. Is it in the same package?

    Q4. If different package,
        is there inheritance?

This solves most interview questions.

# 54. Decision Tree

    What modifier?
          |
    +-----+-----+----------+
    |     |     |          |
  public protected default private
    |     |     |          |
    ↓     ↓     ↓          ↓
  Everywhere Package   Same      Same
           + subclass  package   class
             rules

# 55. Fast Exam Shortcut

> [!tip]
> If the question gives no package information:
>
> Assume the classes are in the same package unless the problem explicitly establishes different packages.
>
> Then:
>
>     public     → Yes
>     protected  → Yes
>     default    → Yes
>     private    → Only same class
>
> This is a useful shortcut for basic questions.

# 56. Fast Interview Shortcut

> [!tip]
> If two packages are explicitly mentioned:
>
> immediately eliminate:
>
>     default
>
> for cross-package access.
>
> Then inspect:
>
>     protected
>
> for inheritance.
>
> `public` remains accessible if the type itself is accessible.
>
> `private` remains inaccessible outside the declaring class.

# 57. Basic Example — All Four

    class Example {

        public int a;
        protected int b;
        int c;
        private int d;
    }

Inside the same class:

    a → Yes
    b → Yes
    c → Yes
    d → Yes

Same package, different class:

    a → Yes
    b → Yes
    c → Yes
    d → No

Different package, unrelated class:

    a → Yes
    b → No
    c → No
    d → No

Different package, subclass:

    a → Yes
    b → Yes, through protected inheritance rules
    c → No
    d → No

# 58. Example — Same Package

Suppose:

    package p1;

    class A {

        public int a = 1;
        protected int b = 2;
        int c = 3;
        private int d = 4;
    }

And:

    package p1;

    class B {

        void test() {

            A obj = new A();

            System.out.println(obj.a);
            System.out.println(obj.b);
            System.out.println(obj.c);
            // obj.d;  // Error
        }
    }

Output:

    1
    2
    3

`d` is private.

# 59. Example — Different Package

Suppose:

    package p1;

    public class A {

        public int a = 1;
        protected int b = 2;
        int c = 3;
        private int d = 4;
    }

Then:

    package p2;

    import p1.A;

    class B {

        void test() {

            A obj = new A();

            System.out.println(obj.a);

            // obj.b;  // Error
            // obj.c;  // Error
            // obj.d;  // Error
        }
    }

Only the public member is directly accessible from this unrelated class.

# 60. Example — Different Package Subclass

    package p2;

    import p1.A;

    class B extends A {

        void test() {

            System.out.println(a);
            System.out.println(b);

            // System.out.println(c); // Error
            // System.out.println(d); // Error
        }
    }

Here:

    public a
    → accessible

    protected b
    → accessible through inheritance

    default c
    → inaccessible

    private d
    → inaccessible

# 61. Advanced Protected Trap

Consider:

    package p1;

    public class Parent {

        protected int x = 10;
    }

Then:

    package p2;

    import p1.Parent;

    public class Child extends Parent {

        void test() {

            Child c = new Child();

            c.x = 20;
        }
    }

This is valid under the protected inheritance access rules.

But:

    void test(Parent p) {

        p.x = 20;
    }

is not generally allowed from the different package simply because `Child` extends `Parent`.

The reference expression matters.

# 62. Why Protected Is Tricky

The simplified rule:

    protected = subclass access

is useful but incomplete.

The precise idea is:

    Same package
       OR
    Subclass context across package boundary

When outside the package, access must respect the protected inheritance rules.

This is why advanced Java interviews often use:

    Parent reference
    vs
    Child reference

to test understanding.

# 63. Private Access and Nested Classes

A nested class can access private members of its enclosing class.

Example:

    class Outer {

        private int x = 10;

        class Inner {

            void show() {

                System.out.println(x);
            }
        }
    }

This is valid.

Both classes participate in the same enclosing type context.

# 64. Private Constructor Example

    class Database {

        private Database() {
        }
    }

Outside:

    Database db = new Database();

Compilation error.

The constructor is private.

This can be useful when the class controls object creation through a static factory method.

# 65. Static Factory Method

Example:

    class User {

        private String name;

        private User(String name) {

            this.name = name;
        }

        public static User create(String name) {

            return new User(name);
        }
    }

External code uses:

    User u = User.create("Arun");

instead of:

    new User("Arun");

This demonstrates controlled object creation.

# 66. Access Modifiers and API Design

Imagine a library:

    class PaymentService {

        private PaymentProcessor processor;

        public void pay(double amount) {
            processor.process(amount);
        }
    }

The user sees:

    pay()

but does not need to directly manipulate:

    processor

This creates a cleaner public API.

Think:

    Public API
        ↓
    Small controlled surface

    Private implementation
        ↓
    Hidden internal complexity

# 67. Real-Time Software Architecture Example

A web application might contain:

    Controller
       ↓
    Service
       ↓
    Repository
       ↓
    Database

Access modifiers can help enforce boundaries.

For example:

    public controller methods
    private helper methods
    private fields
    package-private implementation classes
    protected members only when inheritance is intentionally designed

The goal is not to make everything private blindly.

The goal is:

    expose only what clients need

# 68. Encapsulation Pattern

A common Java class structure:

    public class Employee {

        private int id;
        private String name;
        private double salary;

        public Employee(
            int id,
            String name,
            double salary
        ) {
            this.id = id;
            this.name = name;
            this.salary = salary;
        }

        public int getId() {
            return id;
        }

        public String getName() {
            return name;
        }

        public double getSalary() {
            return salary;
        }
    }

External users interact through the public interface.

Internal state remains private.

# 69. Access Modifiers and Information Hiding

Information hiding means preventing unnecessary implementation details from becoming part of the external interface.

Example:

    private void calculateTax() {
    }

The caller does not need to know how tax is calculated.

They may simply call:

    public double getFinalAmount() {
    }

This reduces dependency on internal implementation.

# 70. Access Modifiers and Coupling

More publicly exposed members can increase the number of ways other classes depend on your implementation.

Think:

    More exposed implementation
        ↓
    More possible dependencies
        ↓
    Higher coupling risk

Controlled visibility can reduce unnecessary coupling.

This is one reason professional Java design often favors:

    private fields
    +
    small public APIs

# 71. Access Modifiers and Maintainability

Suppose a field is public:

    public double salary;

Many classes may directly depend on it.

Later, you want to change:

    salary

to:

    BigDecimal salary

Many clients may break.

If it is private:

    private BigDecimal salary;

and accessed through a controlled method, the internal representation can potentially change without affecting clients.

This is an important design benefit.

# 72. Access Modifiers and SOLID

Access modifiers support several object-oriented design principles.

Especially:

    Encapsulation
    Information Hiding
    Low Coupling
    Single Responsibility
    Liskov Substitution

They are not SOLID principles themselves, but they help implement good designs.

# 73. Access Modifier vs Encapsulation

> [!important]
> **Access modifier is a language mechanism.**
>
> **Encapsulation is an OOP design concept.**

Example:

    private int balance;

uses an access modifier.

The design decision:

    "Users should not directly manipulate balance."

is encapsulation.

# 74. Access Modifier vs Abstraction

> [!important]
> **Access modifiers control visibility.**
>
> **Abstraction hides unnecessary implementation complexity.**

Example:

    private calculateInterest()

uses access control.

Providing:

    public calculateFinalBalance()

while hiding the calculation details demonstrates abstraction.

# 75. Access Modifier vs Data Hiding

Data hiding is the practice of restricting direct access to internal data.

Common implementation:

    private fields

Therefore:

    private
       ↓
    supports data hiding

But:

    private alone
       ≠
    complete encapsulation

Good encapsulation also involves controlled operations and appropriate class design.

# 76. Advanced Interview Question — Can a Top-Level Class Be Private?

### Answer

No.

A top-level class can generally be:

    public

or:

    package-private

It cannot be declared:

    private

or:

    protected

Nested classes have different rules and can use these modifiers.

# 77. Advanced Interview Question — Can a Constructor Be Private?

### Answer

Yes.

A private constructor prevents direct construction from outside the declaring class.

Common uses include:

    Singleton-style designs
    Utility classes
    Static factory methods
    Controlled object creation

# 78. Advanced Interview Question — Can a Method Be Protected?

### Answer

Yes.

Example:

    protected void calculate() {
    }

It is accessible within the same package and to subclasses outside the package subject to protected-access rules.

# 79. Advanced Interview Question — What Is Package-Private?

### Answer

If no access modifier is specified for a class member, the member has package-private accessibility.

Example:

    class Student {

        int id;
    }

`id` can be accessed by classes in the same package but not by unrelated classes in other packages.

# 80. Advanced Interview Question — Which Modifier Is Most Restrictive?

### Answer

`private`.

It restricts direct access to the declaring class.

# 81. Advanced Interview Question — Which Modifier Is Least Restrictive?

### Answer

`public`.

It provides the broadest access allowed by Java's type and module rules.

# 82. Advanced Interview Question — Is Protected More Accessible Than Default?

### Answer

Yes, because protected additionally allows access from subclasses in different packages, subject to protected-access rules.

Both are accessible throughout the same package.

# 83. Advanced Interview Question — Can Private Methods Be Overridden?

### Answer

No.

A private method is not inherited by subclasses, so it cannot be overridden.

A subclass may declare another method with the same name and signature, but it is not overriding the private method.

# 84. Advanced Interview Question — Can Static Methods Be Overridden?

Static methods are not overridden in the runtime-polymorphism sense.

They are hidden when a subclass declares a compatible static method.

Access modifiers still affect whether the declaration is legal.

# 85. Advanced Interview Question — Can an Overriding Method Reduce Access?

No.

Example:

    Parent:

    public void show()

Child cannot declare:

    private void show()

The overriding method cannot be less accessible than the inherited method.

# 86. Advanced Interview Question — Can an Overriding Method Increase Access?

Yes.

Example:

    Parent:

    protected void show()

Child may declare:

    public void show()

because `public` is broader.

# 87. Advanced Interview Question — Why Are Fields Usually Private?

Private fields:

    reduce direct coupling
    protect object state
    support validation
    enable information hiding
    allow internal representation changes

Example:

    private double balance;

instead of:

    public double balance;

# 88. Advanced Interview Question — Why Not Make Everything Public?

Because public members become part of the class's accessible interface.

Once many clients depend on them:

    changing implementation
       ↓
    may break clients

Controlled visibility creates a smaller and more stable API.

# 89. Interview Pattern — Find Compilation Error

Consider:

    class A {

        private int x = 10;
    }

    class B {

        void test() {

            A a = new A();

            System.out.println(a.x);
        }
    }

Question:

Will this compile?

No.

Reason:

    x
    ↓
    private
    ↓
    only A can directly access it

# 90. Interview Pattern — Protected

    class A {

        protected int x = 10;
    }

    class B extends A {

        void test() {

            System.out.println(x);
        }
    }

Same package or suitable subclass context:

    Allowed

# 91. Interview Pattern — Default

    class A {

        int x = 10;
    }

    class B {

        void test() {

            A a = new A();

            System.out.println(a.x);
        }
    }

If both classes are in the same package:

    Allowed

If they are in different packages:

    Not allowed

# 92. Interview Pattern — Public

    class A {

        public int x = 10;
    }

Another accessible class can access:

    a.x

subject to the class itself being accessible.

# 93. Quick Output / Compilation Framework

When solving access questions:

    1. Locate the declaration.
    2. Identify the modifier.
    3. Locate the accessing statement.
    4. Check same class.
    5. Check same package.
    6. Check inheritance.
    7. Check reference type for protected access.
    8. Decide whether compilation succeeds.

# 94. Common Exam Patterns

> [!important] Must Master

1. Four Java access modifiers
2. Public access
3. Protected access
4. Default/package-private access
5. Private access
6. Same class access
7. Same package access
8. Different package access
9. Subclass in another package
10. Protected-reference trap
11. Top-level class modifiers
12. Nested class modifiers
13. Private constructors
14. Utility class design
15. Singleton-style private constructor
16. Access modifiers and inheritance
17. Access modifiers and encapsulation
18. Access modifiers and method overriding
19. Visibility reduction during overriding
20. Visibility increase during overriding
21. Private methods and overriding
22. Interface method visibility
23. Public API design
24. Package-private implementation
25. Compilation-error prediction

# 95. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Default Means Public

Wrong:

    no modifier
    =
    public

Correct:

    no modifier
    =
    package-private

---

### Mistake 2 — Thinking Protected Means Everywhere

Wrong:

    protected
    =
    public

Correct:

    protected
    =
    same package
    +
    cross-package subclass access under inheritance rules

---

### Mistake 3 — Thinking Private Means Object Cannot Exist

Private members do not prevent object creation.

Only a private constructor restricts direct constructor access.

---

### Mistake 4 — Thinking Private Fields Are Inherited Normally

Private members are not directly accessible through subclass code.

---

### Mistake 5 — Thinking Constructors Are Inherited

They are not.

---

### Mistake 6 — Reducing Visibility During Overriding

Wrong:

    public → protected

or:

    protected → private

This is not allowed for overriding methods.

---

### Mistake 7 — Ignoring Package Information

For:

    default
    protected

package boundaries matter.

---

### Mistake 8 — Oversimplifying Protected

"Subclass can always access protected member."

This is incomplete.

Cross-package protected access follows special inheritance/reference rules.

---

### Mistake 9 — Thinking `final` Controls Visibility

It does not.

    final
    → reassignment/inheritance-related restriction depending on context

    private
    → access control

---

### Mistake 10 — Making Everything Public

This increases the exposed API and can increase coupling.

# 96. Shortcuts

> [!tip]
> **Shortcut 1 — Visibility Ladder**
>
> Memorize:
>
>     public
>       ↓
>     protected
>       ↓
>     default
>       ↓
>     private
>
> From most accessible to least accessible.

> [!tip]
> **Shortcut 2 — PPD-P Memory**
>
>     Public   → Everywhere
>     Protected → Package + Subclass
>     Default  → Package
>     Private  → Class
>
> The word "package" is the key for protected/default.

> [!tip]
> **Shortcut 3 — Same Class**
>
> Inside the declaring class:
>
>     public     ✓
>     protected  ✓
>     default    ✓
>     private    ✓
>
> Everything works.

> [!tip]
> **Shortcut 4 — Same Package**
>
> Different class, same package:
>
>     public     ✓
>     protected  ✓
>     default    ✓
>     private    ✗

> [!tip]
> **Shortcut 5 — Different Package, Unrelated Class**
>
>     public     ✓
>     protected  ✗
>     default    ✗
>     private    ✗

> [!tip]
> **Shortcut 6 — Different Package, Subclass**
>
> Start with:
>
>     public     ✓
>     protected  ✓*
>     default    ✗
>     private    ✗
>
> Then remember:
>
> `protected` has special reference/inheritance rules.

> [!tip]
> **Shortcut 7 — Top-Level Class**
>
> Usually:
>
>     public
>     package-private
>
> Not:
>
>     private
>     protected

> [!tip]
> **Shortcut 8 — Overriding**
>
> Remember:
>
>     Child visibility
>     >=
>     Parent visibility
>
> Never reduce visibility.

> [!tip]
> **Shortcut 9 — Constructor**
>
> If the constructor is:
>
>     private
>
> think:
>
> **Controlled object creation.**

> [!tip]
> **Shortcut 10 — Encapsulation**
>
> If you see:
>
>     private field
>     +
>     public getter/setter
>
> think:
>
> **Encapsulation / controlled access.**

# 97. Recognition Patterns

> [!important]
> **If the question says "same class", all four access levels are accessible.**

> [!important]
> **If the question says "same package but different class", eliminate private.**

> [!important]
> **If the question says "different package, unrelated class", only public is directly accessible.**

> [!important]
> **If the question says "different package subclass", investigate protected.**

> [!important]
> **If the question says "no modifier", immediately think package-private.**

> [!important]
> **If the question says "private constructor", think restricted object creation.**

> [!important]
> **If the question says "overriding with weaker access", think compilation error.**

> [!important]
> **If the question says "top-level private class", think invalid.**

# 98. Formula Sheet

```text
ACCESS MODIFIERS

Most Accessible → Least Accessible

public
protected
default / package-private
private

Same Class:

public     → YES
protected  → YES
default    → YES
private    → YES

Same Package, Different Class:

public     → YES
protected  → YES
default    → YES
private    → NO

Different Package, Unrelated Class:

public     → YES
protected  → NO
default    → NO
private    → NO

Different Package, Subclass:

public     → YES
protected  → YES, subject to protected inheritance/reference rules
default    → NO
private    → NO

Top-Level Class:

public
package-private

Nested Class:

public
protected
package-private
private

No Modifier:

→ package-private

private:

→ declaring class only

protected:

→ same package
→ cross-package subclass access under protected rules

public:

→ broadest access

Overriding:

Child visibility
>=
Parent visibility

Cannot reduce:

public → protected/private
protected → private

Private Method:

→ Not inherited
→ Not overridden

Private Constructor:

→ Restricts direct object creation

Access Modifier:

→ Controls visibility

final:

→ Not an access modifier

static:

→ Not an access modifier

Encapsulation Pattern:

private fields
+
public controlled methods
=
controlled access