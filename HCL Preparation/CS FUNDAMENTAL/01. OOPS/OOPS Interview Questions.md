---
type: concept
subject: aptitude
topic: "OOPS Interview Questions"
parent: "OOPS"
company: HCL
difficulty: hard
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - java
  - interview
  - oops-interview
  - object-oriented-programming
  - encapsulation
  - abstraction
  - inheritance
  - polymorphism
  - solid
  - placement
wikilinks:
  - "[[OOPS]]"
  - "[[Encapsulation]]"
  - "[[Abstraction]]"
  - "[[Inheritance]]"
  - "[[Polymorphism]]"
  - "[[Constructors]]"
  - "[[Access Modifiers]]"
  - "[[this Keyword]]"
  - "[[super Keyword]]"
  - "[[static Keyword]]"
  - "[[final Keyword]]"
  - "[[Association]]"
  - "[[Aggregation]]"
  - "[[Composition]]"
  - "[[Coupling and Cohesion]]"
  - "[[SOLID Principles]]"
---

# OOPS Interview Questions

> [!summary]
> **Object-Oriented Programming (OOP) is a programming paradigm that organizes software around objects containing state and behavior.**
>
> The four fundamental OOP concepts are:
>
> **Encapsulation → Abstraction → Inheritance → Polymorphism**
>
> For interviews, do not memorize only definitions. Learn to answer:
>
> **What → Why → Example → Real-world use → Difference → Code**

---

# 1. Core Concept

OOP is one of the most important topics in Java interviews.

Interviewers usually test OOP at several levels:

```text
Level 1
↓
Basic Definitions

Level 2
↓
Java Syntax

Level 3
↓
Conceptual Differences

Level 4
↓
Code Output / Prediction

Level 5
↓
Scenario-Based Questions

Level 6
↓
Design Questions

Level 7
↓
SOLID + Design Patterns
```

A strong OOP candidate should be able to explain concepts in:

```text
Simple English
+
Java Code
+
Real-World Example
+
Interview-Level Reasoning
```

---

# 2. Four Pillars of OOP

| Pillar | Main Idea | Easy Memory |
|---|---|---|
| Encapsulation | Bundle data and methods, control access | Protect |
| Abstraction | Hide implementation details | What |
| Inheritance | Reuse/derive behavior | Reuse |
| Polymorphism | One interface, multiple behaviors | Many Forms |

Memory:

```text
Encapsulation → Protect
Abstraction   → Hide
Inheritance   → Reuse
Polymorphism  → Many Forms
```

---

# 3. Class vs Object

## Question

What is a class?

### Interview Answer

> A class is a user-defined blueprint or template that defines the state and behavior of objects.

Example:

~~~java
class Student {

    String name;
    int age;

    void study() {
        System.out.println("Student is studying");
    }
}
~~~

---

## Question

What is an object?

### Interview Answer

> An object is a runtime instance of a class that has state, behavior, and identity.

Example:

~~~java
Student s1 = new Student();
~~~

Here:

```text
Student → Class
s1      → Object
new      → Creates object
```

---

# 4. Class vs Object

| Class | Object |
|---|---|
| Blueprint | Instance |
| Logical entity | Runtime entity |
| Does not represent one specific instance | Represents a specific instance |
| Defines state and behavior | Contains actual state |
| Example: Student | Example: s1 |

> [!tip]
> **Class = Blueprint**
>
> **Object = Actual Thing**

Real-world analogy:

```text
Class
→ House Blueprint

Object
→ Actual House
```

---

# 5. What Is Encapsulation?

### Interview Answer

> Encapsulation is the process of bundling data and methods into a single unit and restricting direct access to internal state using access control mechanisms.

Example:

~~~java
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
~~~

Here:

```text
balance
→ private

deposit()
→ controlled access

getBalance()
→ controlled read access
```

---

# 6. Why Encapsulation?

Encapsulation provides:

```text
Data Protection
Information Hiding
Controlled Access
Validation
Maintainability
Reduced Coupling
```

Without encapsulation:

~~~java
class BankAccount {

    public double balance;
}
~~~

Any class can do:

~~~java
account.balance = -100000;
~~~

This may violate business rules.

With encapsulation:

~~~java
private double balance;
~~~

the class controls how the value changes.

---

# 7. Encapsulation vs Data Hiding

These are related but not exactly identical.

### Encapsulation

```text
Bundle data + behavior
```

### Data Hiding

```text
Restrict visibility of internal details
```

Example:

~~~java
class User {

    private String password;

    public boolean verifyPassword(String input) {
        return password.equals(input);
    }
}
~~~

The password is hidden.

The user interacts through:

```text
verifyPassword()
```

---

# 8. What Is Abstraction?

### Interview Answer

> Abstraction means exposing the essential behavior of an object while hiding unnecessary implementation details.

Example:

~~~java
interface PaymentGateway {

    void pay(double amount);
}
~~~

Client knows:

```text
pay()
```

Client does not need to know:

```text
Network protocol
Encryption
API calls
Database updates
Transaction handling
```

---

# 9. Real-World Abstraction

When using an ATM:

```text
Insert Card
Enter PIN
Withdraw Money
```

You do not need to know:

```text
How bank servers communicate
How transaction validation works
How the database updates
How encryption works
```

You interact with a simple interface.

Therefore:

```text
ATM Interface
      ↓
Complex Internal Implementation
```

This is abstraction.

---

# 10. Abstraction vs Encapsulation

| Abstraction | Encapsulation |
|---|---|
| Hides unnecessary implementation details | Controls access to internal state |
| Focuses on what | Focuses on how access is controlled |
| Often achieved with interfaces/abstract classes | Often achieved with private fields and methods |
| Reduces conceptual complexity | Protects internal state |

Memory:

```text
Abstraction
→ WHAT

Encapsulation
→ CONTROL ACCESS
```

---

# 11. Abstract Class vs Interface

| Abstract Class | Interface |
|---|---|
| Can have instance variables | Can define constants and interface members |
| Can have constructors | No constructors |
| Can contain concrete methods | Can contain default/static methods in modern Java |
| Can contain abstract methods | Abstract methods define contracts |
| Extended using `extends` | Implemented using `implements` |
| A class can extend one class | A class can implement multiple interfaces |

Example:

~~~java
abstract class Animal {

    abstract void sound();

    void eat() {
        System.out.println("Eating");
    }
}
~~~

Interface:

~~~java
interface Flyable {

    void fly();
}
~~~

---

# 12. Interview Trap: Can We Create an Object of an Abstract Class?

No.

You cannot directly instantiate an abstract class.

This is invalid:

~~~java
Animal a = new Animal();
~~~

But you can create a reference:

~~~java
Animal a = new Dog();
~~~

if `Dog` is a concrete subclass.

Memory:

```text
Abstract class
→ Cannot instantiate directly

Reference
→ Allowed
```

---

# 13. What Is Inheritance?

### Interview Answer

> Inheritance is an OOP mechanism in which a class derives properties and behavior from another class.

Example:

~~~java
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
~~~

Now:

```text
Dog
↓
inherits
↓
Animal
```

Dog can use:

```text
eat()
bark()
```

---

# 14. Why Use Inheritance?

Inheritance can provide:

```text
Code Reuse
Specialization
Polymorphism
Hierarchical Classification
```

But inheritance should represent a valid:

```text
IS-A
```

relationship.

Example:

```text
Dog IS-A Animal
Car IS-A Vehicle
Manager IS-A Employee
```

---

# 15. Types of Inheritance

Common forms:

```text
Single
Multilevel
Hierarchical
Multiple
Hybrid
```

Java classes support:

```text
Single
Multilevel
Hierarchical
```

Java does not support multiple inheritance of classes.

However, Java supports multiple inheritance of type through interfaces.

---

# 16. Single Inheritance

```text
Animal
   ↑
   |
  Dog
```

Example:

~~~java
class Animal {
}

class Dog extends Animal {
}
~~~

One parent:

```text
Animal
```

One child:

```text
Dog
```

---

# 17. Multilevel Inheritance

```text
Animal
   ↑
 Mammal
   ↑
  Dog
```

Example:

~~~java
class Animal {
}

class Mammal extends Animal {
}

class Dog extends Mammal {
}
~~~

Dog indirectly inherits from Animal.

---

# 18. Hierarchical Inheritance

```text
       Animal
       /    \
      /      \
    Dog      Cat
```

Example:

~~~java
class Animal {
}

class Dog extends Animal {
}

class Cat extends Animal {
}
~~~

One parent:

```text
Animal
```

Multiple children:

```text
Dog
Cat
```

---

# 19. Multiple Inheritance in Java

Java does not allow:

~~~java
class C extends A, B {
}
~~~

because it can create ambiguity.

Instead Java supports:

~~~java
interface A {
    void methodA();
}
~~~

~~~java
interface B {
    void methodB();
}
~~~

~~~java
class C implements A, B {

    public void methodA() {
    }

    public void methodB() {
    }
}
~~~

Thus:

```text
Multiple inheritance through interfaces
→ Supported
```

---

# 20. Diamond Problem

Suppose:

```text
      A
     / \
    B   C
     \ /
      D
```

If B and C both inherit or provide different implementations of the same method, D may face ambiguity.

Java avoids this problem for classes by not allowing multiple class inheritance.

With interface default methods, Java requires the ambiguity to be resolved explicitly when necessary.

---

# 21. What Is Polymorphism?

### Interview Answer

> Polymorphism means one interface or reference can represent multiple forms of behavior.

Two major forms in Java:

```text
Compile-Time Polymorphism
→ Method Overloading

Runtime Polymorphism
→ Method Overriding
```

Memory:

```text
Overloading
→ Compile Time

Overriding
→ Runtime
```

---

# 22. Method Overloading

Same method name:

```text
Different parameter list
```

Example:

~~~java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }

    double add(double a, double b) {
        return a + b;
    }
}
~~~

The method name remains:

```text
add()
```

but parameter lists differ.

---

# 23. What Can Change During Overloading?

You can change:

```text
Number of parameters
Parameter types
Parameter order
```

Example:

~~~java
void test(int x) {
}
~~~

~~~java
void test(int x, int y) {
}
~~~

~~~java
void test(double x) {
}
~~~

~~~java
void test(int x, double y) {
}
~~~

---

# 24. Can Return Type Alone Overload a Method?

No.

Invalid:

~~~java
int calculate() {
    return 10;
}
~~~

~~~java
double calculate() {
    return 10.5;
}
~~~

The parameter list is identical.

Changing only return type is not method overloading.

> [!warning]
> **Return type alone cannot distinguish overloaded methods.**

---

# 25. Method Overriding

When a subclass provides its own implementation of an inherited instance method, it is method overriding.

Example:

~~~java
class Animal {

    void sound() {
        System.out.println("Animal sound");
    }
}
~~~

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Bark");
    }
}
~~~

Now:

~~~java
Animal a = new Dog();

a.sound();
~~~

Output:

```text
Bark
```

This is runtime polymorphism.

---

# 26. Overloading vs Overriding

| Overloading | Overriding |
|---|---|
| Usually same class | Requires inheritance/subtyping |
| Same method name | Same method signature |
| Parameters differ | Parameters must match |
| Compile-time method selection | Runtime method dispatch |
| Return type alone cannot overload | Covariant return types can be used |
| Static methods can be overloaded | Static methods are hidden, not overridden |

Memory:

```text
Different Parameters
→ Overloading

Same Signature + Child
→ Overriding
```

---

# 27. Dynamic Method Dispatch

Example:

~~~java
class Animal {

    void sound() {
        System.out.println("Animal");
    }
}
~~~

~~~java
class Dog extends Animal {

    @Override
    void sound() {
        System.out.println("Dog");
    }
}
~~~

Then:

~~~java
Animal a = new Dog();

a.sound();
~~~

Reference type:

```text
Animal
```

Actual object type:

```text
Dog
```

Method selected at runtime:

```text
Dog.sound()
```

This is:

```text
Dynamic Method Dispatch
```

---

# 28. Important Polymorphism Trick

> [!important]
> In runtime polymorphism:
>
> **Reference type controls what members are accessible.**
>
> **Actual object type controls which overridden instance method executes.**

Example:

~~~java
class Parent {

    void show() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    @Override
    void show() {
        System.out.println("Child");
    }

    void childOnly() {
        System.out.println("Child only");
    }
}
~~~

Then:

~~~java
Parent p = new Child();

p.show();
~~~

Output:

```text
Child
```

But:

~~~java
p.childOnly();
~~~

does not compile because `childOnly()` is not visible through the `Parent` reference.

---

# 29. Constructors

A constructor is a special member used to initialize an object.

Characteristics:

```text
Same name as class
No return type
Called during object creation
Can be overloaded
Not inherited
```

Example:

~~~java
class Student {

    String name;

    Student() {
        name = "Unknown";
    }
}
~~~

---

# 30. Default Constructor

If you define no constructor, Java may provide a compiler-generated no-argument constructor.

Example:

~~~java
class Student {
}
~~~

Conceptually:

~~~java
Student() {
}
~~~

But be careful:

> [!warning]
> If you define any constructor yourself, Java does not automatically add the no-argument constructor.

Example:

~~~java
class Student {

    Student(String name) {
    }
}
~~~

This does not automatically provide:

~~~java
Student()
~~~

---

# 31. Parameterized Constructor

A constructor that accepts arguments.

~~~java
class Student {

    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
~~~

Usage:

~~~java
Student s =
    new Student("Pradeep", 21);
~~~

---

# 32. Constructor Overloading

Multiple constructors with different parameter lists.

~~~java
class Student {

    Student() {
    }

    Student(String name) {
    }

    Student(String name, int age) {
    }
}
~~~

This is:

```text
Constructor Overloading
```

---

# 33. Can Constructors Be Overridden?

No.

Constructors are not inherited.

Therefore:

```text
Constructor
→ Can be overloaded
→ Cannot be overridden
```

This is a very common interview question.

---

# 34. Can Constructor Be Inherited?

No.

A subclass does not inherit the constructors of its parent.

However, a subclass constructor can invoke a parent constructor using:

~~~java
super();
~~~

---

# 35. this Keyword

`this` refers to the current object.

Common uses:

```text
Resolve variable shadowing
Call current class constructor
Pass current object
Return current object
Access current object members
```

Example:

~~~java
class Student {

    String name;

    Student(String name) {
        this.name = name;
    }
}
~~~

Here:

```text
this.name
→ instance variable

name
→ parameter
```

---

# 36. this() Constructor Chaining

You can call another constructor in the same class using:

~~~java
this();
~~~

Example:

~~~java
class Student {

    Student() {
        this("Unknown");
    }

    Student(String name) {
        System.out.println(name);
    }
}
~~~

Important:

> [!warning]
> `this()` must be the first statement in a constructor.

---

# 37. super Keyword

`super` refers to the immediate parent class portion of the current object.

Common uses:

```text
Access parent variable
Call parent method
Call parent constructor
```

Example:

~~~java
class Parent {

    int x = 10;
}
~~~

~~~java
class Child extends Parent {

    int x = 20;

    void show() {
        System.out.println(super.x);
    }
}
~~~

Output:

```text
10
```

---

# 38. super() Constructor Call

Example:

~~~java
class Parent {

    Parent() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    Child() {
        super();
        System.out.println("Child");
    }
}
~~~

Output:

```text
Parent
Child
```

If not explicitly written, Java inserts an implicit `super()` when applicable.

---

# 39. this vs super

| `this` | `super` |
|---|---|
| Current object/class | Immediate parent |
| Current class member | Parent member |
| `this()` calls current class constructor | `super()` calls parent constructor |
| Used for current object | Used for parent part |

Memory:

```text
this
→ Me

super
→ Parent
```

---

# 40. static Keyword

`static` means the member belongs to the class rather than each individual object.

Example:

~~~java
class Student {

    static String college =
        "SRM";
}
~~~

All objects share the same static field.

Usage:

~~~java
Student.college
~~~

---

# 41. Static Variable vs Instance Variable

~~~java
class Student {

    static String college = "SRM";

    String name;
}
~~~

Here:

```text
college
→ Shared

name
→ Object-specific
```

Memory:

```text
static
→ One per class

instance
→ One per object
```

---

# 42. Can Static Methods Be Overridden?

No.

Static methods are associated with the class.

If a subclass defines a static method with the same signature, it is:

```text
Method Hiding
```

not runtime overriding.

Example:

~~~java
class Parent {

    static void show() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    static void show() {
        System.out.println("Child");
    }
}
~~~

The method selected depends on the reference/class context, not runtime object dispatch in the same way as instance overriding.

---

# 43. final Keyword

`final` can be applied to:

```text
Variable
Method
Class
```

## final variable

Cannot be reassigned after initialization.

~~~java
final int x = 10;
~~~

---

## final method

Cannot be overridden.

~~~java
class Parent {

    final void show() {
    }
}
~~~

A child cannot override `show()`.

---

## final class

Cannot be extended.

~~~java
final class SecurityManager {
}
~~~

This is invalid:

~~~java
class Child extends SecurityManager {
}
~~~

---

# 44. final Memory Trick

```text
final variable
→ Cannot reassign

final method
→ Cannot override

final class
→ Cannot extend
```

---

# 45. Access Modifiers

Java has four access levels:

```text
private
default
protected
public
```

| Modifier | Same Class | Same Package | Subclass Other Package | Other Package |
|---|---:|---:|---:|---:|
| private | Yes | No | No | No |
| default | Yes | Yes | No* | No |
| protected | Yes | Yes | Yes** | No |
| public | Yes | Yes | Yes | Yes |

`*` A subclass in another package cannot access a package-private member merely by inheritance.

`**` A protected member in another package is accessible to a subclass through an appropriate inherited/subclass context, not as arbitrary access through any parent instance.

---

# 46. Access Modifier Memory

> [!tip]
> Think:

```text
private
→ Same class

default
→ Same package

protected
→ Package + subclass access

public
→ Everywhere subject to normal Java access rules
```

---

# 47. Association

Association represents a general relationship between objects.

Example:

```text
Teacher
   |
   | teaches
   ↓
Student
```

A teacher can exist without a particular student.

A student can exist without a particular teacher.

Therefore:

```text
Association
```

---

# 48. Aggregation

Aggregation represents a weak whole-part relationship.

Example:

```text
Department
     ◇
     |
     ↓
  Teacher
```

The teacher can exist independently of the department.

Therefore:

```text
Aggregation
→ Weak Ownership
→ Independent Lifecycle
```

---

# 49. Composition

Composition represents a strong whole-part relationship.

Example:

```text
House
  ◆
  |
  ↓
Room
```

Conceptually, the room is treated as part of the house's lifecycle in the composition model.

Therefore:

```text
Composition
→ Strong Ownership
→ Dependent Lifecycle
```

---

# 50. Aggregation vs Composition

| Aggregation | Composition |
|---|---|
| Weak ownership | Strong ownership |
| Part can exist independently | Part lifecycle is strongly tied to whole |
| Hollow diamond in UML | Filled diamond in UML |
| Example: Department–Teacher | Example: House–Room |

Memory:

```text
Aggregation
→ Weak

Composition
→ Strong
```

---

# 51. Coupling and Cohesion

### Coupling

Dependency:

```text
BETWEEN modules
```

### Cohesion

Relatedness:

```text
WITHIN module
```

Ideal:

```text
Low Coupling
+
High Cohesion
```

---

# 52. SOLID Interview Memory

```text
S → Single Responsibility
O → Open/Closed
L → Liskov Substitution
I → Interface Segregation
D → Dependency Inversion
```

Fast recognition:

```text
Too many jobs
→ S

New feature modifies old code repeatedly
→ O

Child breaks parent contract
→ L

Unused interface methods
→ I

Concrete dependency
→ D
```

---

# 53. Overloading vs Overriding: Master Table

| Feature | Overloading | Overriding |
|---|---|---|
| Polymorphism | Compile time | Runtime |
| Method name | Same | Same |
| Parameters | Must differ | Must match |
| Inheritance | Not required | Required |
| Return type | Cannot differ only by return type | Same or covariant |
| Access | Normal overload rules | Cannot reduce visibility |
| Static | Can overload | Hidden, not overridden |
| final method | Can overload another signature | Cannot override |
| private method | Can overload | Cannot override |

---

# 54. Can We Override a Private Method?

No.

Private methods are not accessible to subclasses and are not inherited in the normal overriding sense.

Example:

~~~java
class Parent {

    private void show() {
    }
}
~~~

~~~java
class Child extends Parent {

    private void show() {
    }
}
~~~

This is not method overriding.

The child method is a separate method.

---

# 55. Can We Override a Final Method?

No.

`final` explicitly prevents overriding.

---

# 56. Can We Override a Static Method?

No.

Static methods are hidden, not overridden.

---

# 57. Can We Override a Constructor?

No.

Constructors are not inherited.

---

# 58. Can We Overload a Static Method?

Yes.

Example:

~~~java
class Calculator {

    static int add(int a, int b) {
        return a + b;
    }

    static int add(int a, int b, int c) {
        return a + b + c;
    }
}
~~~

This is valid overloading.

---

# 59. Can We Overload a Constructor?

Yes.

Example:

~~~java
class Student {

    Student() {
    }

    Student(String name) {
    }

    Student(String name, int age) {
    }
}
~~~

---

# 60. Can We Have Multiple Constructors?

Yes.

Constructors can be overloaded using different parameter lists.

---

# 61. Can an Abstract Class Have a Constructor?

Yes.

Even though an abstract class cannot be instantiated directly, its constructor can run as part of constructing a concrete subclass.

Example:

~~~java
abstract class Animal {

    Animal() {
        System.out.println("Animal constructor");
    }
}
~~~

~~~java
class Dog extends Animal {

    Dog() {
        System.out.println("Dog constructor");
    }
}
~~~

Creating:

~~~java
Dog d = new Dog();
~~~

produces:

```text
Animal constructor
Dog constructor
```

---

# 62. Can an Interface Have a Constructor?

No.

An interface is not instantiated directly.

Therefore:

```text
Abstract class
→ Can have constructor

Interface
→ Cannot have constructor
```

---

# 63. Can an Abstract Class Have Concrete Methods?

Yes.

Example:

~~~java
abstract class Animal {

    abstract void sound();

    void eat() {
        System.out.println("Eating");
    }
}
~~~

It can contain:

```text
Abstract methods
Concrete methods
Fields
Constructors
```

---

# 64. Can an Interface Have Method Implementations?

Modern Java interfaces can contain:

```text
default methods
static methods
private methods
```

They can also declare abstract methods.

Example:

~~~java
interface Vehicle {

    void drive();

    default void start() {
        System.out.println("Starting");
    }

    static void info() {
        System.out.println("Vehicle");
    }
}
~~~

---

# 65. Object Class

In Java, classes ultimately derive from:

```text
java.lang.Object
```

Important methods include:

```text
toString()
equals()
hashCode()
getClass()
clone()
wait()
notify()
notifyAll()
```

Not every method is appropriate to override directly, but several are extremely important in interviews.

---

# 66. equals() vs ==

This is one of the most common Java interview questions.

### `==`

For object references, `==` checks whether two references point to the same object.

### `equals()`

`equals()` is intended to compare logical equality according to the class's implementation.

Example:

~~~java
String a = new String("Java");
String b = new String("Java");
~~~

Then:

~~~java
a == b
~~~

is typically:

```text
false
```

because they are different objects.

But:

~~~java
a.equals(b)
~~~

is:

```text
true
```

because String defines logical equality based on content.

> [!tip]
> **`==` → Reference identity**
>
> **`equals()` → Logical equality**

---

# 67. equals() and hashCode()

Important rule:

> If two objects are equal according to `equals()`, they must have the same `hashCode()`.

Example:

~~~java
class Student {

    int id;

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }

        if (!(obj instanceof Student)) {
            return false;
        }

        Student other = (Student) obj;

        return id == other.id;
    }

    @Override
    public int hashCode() {
        return Integer.hashCode(id);
    }
}
~~~

This matters especially for:

```text
HashMap
HashSet
Hashtable
```

---

# 68. What Is Immutability?

An immutable object cannot have its observable state changed after creation.

Example:

```text
String
```

is a famous Java immutable class.

Typical techniques for designing immutable objects include:

```text
final class
private final fields
No setters
Initialize through constructor
Defensive copies for mutable fields
```

---

# 69. Why Is Immutability Useful?

Benefits:

```text
Thread Safety
Predictability
Safe Sharing
Easier Reasoning
Reduced Side Effects
```

Example:

~~~java
final class Student {

    private final String name;

    Student(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}
~~~

No setter is provided.

---

# 70. Is final Object Immutable?

No.

Example:

~~~java
final List<String> list =
    new ArrayList<>();
~~~

The reference cannot point to another list:

~~~java
list = new ArrayList<>();
~~~

But the contents can still change:

~~~java
list.add("Java");
~~~

Therefore:

```text
final reference
≠
immutable object
```

This is a very common interview trap.

---

# 71. Shallow Copy vs Deep Copy

### Shallow Copy

Copies the object structure but may share references to nested mutable objects.

### Deep Copy

Creates independent copies of nested mutable objects as well.

Memory:

```text
Shallow
→ Outer copied
→ Inner references may be shared

Deep
→ Outer copied
→ Inner objects copied
```

---

# 72. Composition vs Inheritance Interview Question

### Question

When should you prefer composition over inheritance?

### Answer

> Prefer composition when you need flexible behavior, want to avoid rigid inheritance hierarchies, or when the relationship is better modeled as "has-a" rather than "is-a."

Example:

```text
Car HAS-A Engine
```

rather than:

```text
Car IS-A Engine
```

---

# 73. IS-A vs HAS-A

## IS-A

Usually inheritance/subtyping.

```text
Dog IS-A Animal
```

## HAS-A

Usually composition/aggregation/association.

```text
Car HAS-A Engine
```

Memory:

```text
IS-A
→ Inheritance

HAS-A
→ Composition/Aggregation
```

---

# 74. Runtime Polymorphism Interview Question

Given:

~~~java
class Parent {

    void show() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    @Override
    void show() {
        System.out.println("Child");
    }
}
~~~

~~~java
Parent p = new Child();

p.show();
~~~

### Answer

```text
Child
```

Reason:

```text
Reference type = Parent
Actual object = Child

Overridden instance method
→ Resolved at runtime
```

---

# 75. Constructor Execution Order

Consider:

~~~java
class Parent {

    Parent() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    Child() {
        System.out.println("Child");
    }
}
~~~

~~~java
Child c = new Child();
~~~

Output:

```text
Parent
Child
```

Why?

```text
Child constructor
     ↓
implicit super()
     ↓
Parent constructor
     ↓
Child constructor body
```

Memory:

> [!tip]
> **Parent constructor runs before Child constructor body.**

---

# 76. Initialization Order Interview Trap

For a normal object construction involving inheritance, think broadly:

```text
Superclass initialization
        ↓
Superclass constructor
        ↓
Subclass initialization
        ↓
Subclass constructor
```

Static initialization occurs separately when classes are initialized.

For exact output questions, carefully trace:

```text
Static fields/blocks
Instance fields/blocks
Constructors
```

in the language-defined initialization order.

---

# 77. Access Modifier Interview Trap

Can a subclass reduce visibility while overriding?

No.

Example:

Parent:

~~~java
class Parent {

    protected void show() {
    }
}
~~~

Child cannot do:

~~~java
class Child extends Parent {

    @Override
    private void show() {
    }
}
~~~

This would reduce visibility.

The overriding method must provide compatible access.

---

# 78. Covariant Return Type

A subclass overriding method may return a subtype of the original return type.

Example:

~~~java
class Animal {
}
~~~

~~~java
class Dog extends Animal {
}
~~~

~~~java
class Parent {

    Animal create() {
        return new Animal();
    }
}
~~~

~~~java
class Child extends Parent {

    @Override
    Dog create() {
        return new Dog();
    }
}
~~~

This is called:

```text
Covariant Return Type
```

---

# 79. Overloading Resolution Trick

Consider:

~~~java
void show(int x) {
    System.out.println("int");
}

void show(double x) {
    System.out.println("double");
}
~~~

Call:

~~~java
show(10);
~~~

Output:

```text
int
```

because the exact matching overload is preferred.

General idea:

```text
Exact match
→ Prefer exact match

Then applicable widening conversions
→ Consider wider types
```

For difficult overload questions, carefully check:

```text
Exact match
Primitive widening
Reference widening
Boxing/unboxing
Varargs
```

---

# 80. Autoboxing Interview Trap

Suppose:

~~~java
void show(int x) {
    System.out.println("int");
}
~~~

~~~java
void show(Integer x) {
    System.out.println("Integer");
}
~~~

Then:

~~~java
show(10);
~~~

typically chooses:

```text
int
```

because an exact primitive match is preferred over boxing.

---

# 81. Varargs Interview Trap

Example:

~~~java
void show(int x) {
    System.out.println("int");
}

void show(int... x) {
    System.out.println("varargs");
}
~~~

Call:

~~~java
show(10);
~~~

Output:

```text
int
```

because the fixed-arity method is preferred over varargs when applicable.

---

# 82. Null and Overloading

Consider:

~~~java
void show(String s) {
    System.out.println("String");
}

void show(Integer i) {
    System.out.println("Integer");
}
~~~

Then:

~~~java
show(null);
~~~

This is ambiguous because `null` can match both reference types and neither is more specific than the other.

Therefore the code does not compile.

> [!warning]
> `null` + unrelated reference overloads can create ambiguity.

---

# 83. Static vs Instance Method Output Trap

Consider:

~~~java
class Parent {

    static void show() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    static void show() {
        System.out.println("Child");
    }
}
~~~

~~~java
Parent p = new Child();

p.show();
~~~

Output:

```text
Parent
```

Why?

```text
Static method
→ Class/reference-based resolution
→ Not runtime overriding
```

---

# 84. Instance Method vs Static Method

| Instance Method | Static Method |
|---|---|
| Belongs to object behavior | Belongs to class |
| Runtime overriding possible | Static hiding |
| Can access instance members directly | Cannot directly access instance members |
| Uses object context | Uses class context |

---

# 85. `this` vs `super` Interview Question

### `this`

```text
Current object
Current class constructor
Current class members
```

### `super`

```text
Parent portion
Parent constructor
Parent members
```

Memory:

```text
this → Me
super → Parent
```

---

# 86. `final` vs `finally` vs `finalize`

Very common Java interview question.

## final

Keyword used for:

```text
Variable
Method
Class
```

## finally

Block associated with exception handling.

~~~java
try {
    // code
}
finally {
    // cleanup logic
}
~~~

## finalize

A legacy method associated with garbage-collection-related finalization. It has been deprecated and should not be relied upon for resource management.

Memory:

```text
final
→ Restriction

finally
→ Cleanup block

finalize
→ Legacy/deprecated mechanism
```

---

# 87. Abstract Class vs Concrete Class

| Abstract Class | Concrete Class |
|---|---|
| Cannot instantiate directly | Can instantiate |
| May contain abstract methods | Cannot have abstract methods unless itself abstract |
| Can contain concrete methods | Contains implemented behavior |
| Can have constructors | Can have constructors |
| Used as incomplete/base abstraction | Used for actual objects |

---

# 88. Interface vs Class

| Interface | Class |
|---|---|
| Defines a contract/type | Defines state and behavior |
| No constructors | Constructors allowed |
| Multiple interfaces can be implemented | Class extends only one class |
| Supports abstraction | Can be concrete or abstract |
| Can have default/static/private methods | Can have normal methods |

---

# 89. Association vs Aggregation vs Composition

```text
Association
→ General relationship

Aggregation
→ Weak whole-part relationship

Composition
→ Strong whole-part relationship
```

Memory:

```text
Association
     ↓
Aggregation
     ↓
Composition

Relationship becomes increasingly ownership-oriented.
```

---

# 90. Coupling vs Cohesion

### Coupling

```text
Between modules
```

### Cohesion

```text
Within module
```

Ideal:

```text
Low Coupling
+
High Cohesion
```

---

# 91. SOLID vs OOP Pillars

OOP pillars describe major object-oriented mechanisms:

```text
Encapsulation
Abstraction
Inheritance
Polymorphism
```

SOLID provides design principles for using OOP mechanisms effectively.

Therefore:

```text
OOP
 ↓
Programming Model

SOLID
 ↓
Design Guidance
```

---

# 92. Real-Time Interview Scenario

### Question

You are designing a payment application supporting:

```text
Credit Card
UPI
PayPal
Net Banking
```

How would you design it?

### Strong Answer

Use an abstraction:

~~~java
interface PaymentGateway {

    void pay(double amount);
}
~~~

Then create implementations:

```text
CardPayment
UpiPayment
PaypalPayment
NetBankingPayment
```

Inject the abstraction into the high-level service:

~~~java
class CheckoutService {

    private final PaymentGateway gateway;

    CheckoutService(PaymentGateway gateway) {
        this.gateway = gateway;
    }
}
~~~

Benefits:

```text
DIP
OCP
Polymorphism
Low Coupling
High Cohesion
Testability
```

---

# 93. Real-Time Interview Scenario

### Question

A class has:

```text
1000 lines
15 methods
Database code
Email code
Payment code
Logging code
Report generation
```

What would you do?

### Strong Answer

First identify responsibilities.

Then split the class into cohesive components:

```text
PaymentService
EmailService
ReportService
Repository
LoggingService
```

Apply:

```text
SRP
High Cohesion
Low Coupling
DIP where appropriate
```

Avoid blindly splitting classes without meaningful boundaries.

---

# 94. Real-Time Interview Scenario

### Question

Your manager asks you to add a new notification channel every month.

Current code:

~~~java
if (type.equals("EMAIL")) {
}
else if (type.equals("SMS")) {
}
else if (type.equals("PUSH")) {
}
~~~

What would you change?

### Strong Answer

Use a notification abstraction:

~~~java
interface Notification {

    void send(String message);
}
~~~

Create implementations:

```text
EmailNotification
SmsNotification
PushNotification
```

Then new channels can be added through new implementations.

Relevant principles:

```text
OCP
DIP
Polymorphism
```

---

# 95. Real-Time Interview Scenario

### Question

A `Bird` parent class has:

~~~java
void fly()
~~~

but `Penguin` extends Bird and cannot fly.

What is the problem?

### Answer

Potential:

```text
LSP violation
```

The abstraction incorrectly assumes that every Bird supports flying.

Better model capabilities:

```text
Bird
   |
   +-- FlyingBird
   |
   +-- NonFlyingBird
```

or:

~~~java
interface Flyable {
    void fly();
}
~~~

Only flying birds implement it.

This can improve both:

```text
LSP
ISP
```

---

# 96. Real-Time Interview Scenario

### Question

A `Robot` must implement:

```text
work()
eat()
sleep()
```

but only needs `work()`.

### Answer

Potential:

```text
ISP violation
```

Split the interface into focused capabilities.

---

# 97. Most Important OOP "Why" Questions

These questions often distinguish memorization from understanding.

## Why use encapsulation?

```text
Protect state
Control access
Validate changes
Reduce coupling
```

## Why use abstraction?

```text
Hide complexity
Expose essential behavior
Reduce conceptual complexity
```

## Why use inheritance?

```text
Reuse/specialization
Polymorphic relationships
```

But use it only when the subtype relationship is valid.

## Why use polymorphism?

```text
Flexible behavior
Replaceable implementations
Reduced conditional logic
Extensibility
```

## Why use interfaces?

```text
Contracts
Abstraction
Multiple interface implementation
Loose coupling
```

---

# 98. OOP Interview Rapid-Fire

## Q1. Four pillars?

```text
Encapsulation
Abstraction
Inheritance
Polymorphism
```

## Q2. Class?

```text
Blueprint
```

## Q3. Object?

```text
Runtime instance
```

## Q4. Constructor return type?

```text
None
```

## Q5. Can constructor be overloaded?

```text
Yes
```

## Q6. Can constructor be overridden?

```text
No
```

## Q7. Can static method be overridden?

```text
No
```

## Q8. Can final method be overridden?

```text
No
```

## Q9. Can private method be overridden?

```text
No
```

## Q10. Can abstract class have constructor?

```text
Yes
```

## Q11. Can interface have constructor?

```text
No
```

## Q12. Can abstract class have concrete methods?

```text
Yes
```

## Q13. Multiple class inheritance in Java?

```text
No
```

## Q14. Multiple interface implementation?

```text
Yes
```

## Q15. Compile-time polymorphism?

```text
Method Overloading
```

## Q16. Runtime polymorphism?

```text
Method Overriding
```

## Q17. `==` for object references?

```text
Reference identity
```

## Q18. `equals()`?

```text
Logical equality according to implementation
```

## Q19. Best coupling?

```text
Low
```

## Q20. Best cohesion?

```text
High
```

---

# 99. Tricky Interview Questions

## Question 1

Can a class have multiple constructors?

**Yes.**

---

## Question 2

Can a constructor be private?

**Yes.**

This is useful in patterns such as:

```text
Singleton
Factory-style creation
Controlled instantiation
```

---

## Question 3

Can an abstract class be final?

No.

Reason:

```text
abstract
→ Intended to be extended

final
→ Cannot be extended
```

These requirements conflict.

---

## Question 4

Can a method be both abstract and final?

No.

Reason:

```text
abstract
→ Must be implemented by subclass

final
→ Cannot be overridden
```

---

## Question 5

Can an abstract method be static?

No.

An abstract method requires overriding by a subclass, while static methods are not overridden polymorphically.

---

## Question 6

Can an interface extend another interface?

Yes.

~~~java
interface A {
}

interface B extends A {
}
~~~

---

## Question 7

Can an interface extend multiple interfaces?

Yes.

~~~java
interface A {
}

interface B {
}

interface C extends A, B {
}
~~~

---

## Question 8

Can a class implement multiple interfaces?

Yes.

~~~java
class C implements A, B {
}
~~~

---

## Question 9

Can an interface extend a class?

No.

An interface extends interfaces.

A class extends a class and implements interfaces.

---

# 100. Output-Based Interview Pattern

When solving OOP output questions, use this order:

```text
Step 1
Identify reference type.

Step 2
Identify actual object type.

Step 3
Check static vs instance.

Step 4
Check overload vs override.

Step 5
Check access modifiers.

Step 6
Check constructor order.

Step 7
Check this/super.

Step 8
Check initialization blocks.

Step 9
Check final/private/static restrictions.
```

This prevents most mistakes.

---

# 101. Master OOP Code Analysis Trick

When you see:

~~~java
Parent p = new Child();
~~~

immediately write:

```text
Reference Type → Parent
Object Type    → Child
```

Then ask:

```text
Is method overridden?
```

If yes:

```text
Child implementation
```

For fields and static members, do not blindly apply the same rule as instance method overriding.

---

# 102. Interview Code Pattern

~~~java
class Parent {

    int x = 10;

    void show() {
        System.out.println("Parent");
    }
}
~~~

~~~java
class Child extends Parent {

    int x = 20;

    @Override
    void show() {
        System.out.println("Child");
    }
}
~~~

~~~java
Parent p = new Child();

System.out.println(p.x);
p.show();
~~~

Output:

```text
10
Child
```

Why?

```text
Field access
→ Reference type

Overridden instance method
→ Runtime object type
```

> [!important]
> **Fields are not polymorphically overridden like instance methods.**

---

# 103. Interview Preparation Strategy

For OOP interviews, study in this order:

```text
1. Class and Object
2. Encapsulation
3. Abstraction
4. Inheritance
5. Polymorphism
6. Overloading
7. Overriding
8. Constructors
9. this
10. super
11. static
12. final
13. Access Modifiers
14. Abstract Class
15. Interface
16. Association
17. Aggregation
18. Composition
19. Coupling
20. Cohesion
21. SOLID
22. equals/hashCode
23. Immutability
24. Composition vs Inheritance
25. Scenario-Based Design
26. Output-Based Questions
```

---

# 104. Interview Answer Framework

When asked an OOP question, answer using:

```text
1. Definition
2. Purpose
3. Simple Example
4. Real-World Example
5. Important Rule
6. Difference/Trap
```

Example:

### "What is polymorphism?"

Answer:

```text
Definition
→ One interface/reference can represent multiple forms.

Purpose
→ Flexible and extensible behavior.

Types
→ Overloading and overriding.

Example
→ Parent reference pointing to Child object.

Rule
→ Overridden instance method is selected at runtime.

Trap
→ Static methods are hidden, not overridden.
```

This gives a strong interview answer without unnecessary theory.

---

# 105. Most Important Differences

## Abstraction vs Encapsulation

```text
Abstraction
→ Hide complexity
→ WHAT

Encapsulation
→ Control access
→ Protect internal state
```

## Overloading vs Overriding

```text
Overloading
→ Different parameters
→ Compile time

Overriding
→ Same signature
→ Runtime
```

## Abstract Class vs Interface

```text
Abstract Class
→ Shared base implementation/state

Interface
→ Contract/capability
```

## Inheritance vs Composition

```text
Inheritance
→ IS-A

Composition
→ HAS-A
```

## `this` vs `super`

```text
this
→ Current object

super
→ Parent
```

## `==` vs `equals()`

```text
==
→ Reference identity for objects

equals()
→ Logical equality
```

## final vs static

```text
final
→ Restriction

static
→ Class-level member
```

---

# 106. Placement-Level OOP Checklist

Before an interview, make sure you can explain:

```text
[ ] Class
[ ] Object
[ ] Encapsulation
[ ] Abstraction
[ ] Inheritance
[ ] Polymorphism
[ ] Overloading
[ ] Overriding
[ ] Dynamic Method Dispatch
[ ] Constructor
[ ] Constructor Overloading
[ ] this
[ ] super
[ ] static
[ ] final
[ ] Access Modifiers
[ ] Abstract Class
[ ] Interface
[ ] Association
[ ] Aggregation
[ ] Composition
[ ] Coupling
[ ] Cohesion
[ ] SOLID
[ ] equals()
[ ] hashCode()
[ ] == vs equals()
[ ] Immutability
[ ] Composition vs Inheritance
[ ] IS-A vs HAS-A
[ ] Runtime Polymorphism
[ ] Multiple Inheritance
[ ] Diamond Problem
[ ] Output-Based Questions
[ ] Scenario-Based Design
```

---

# 107. Final Master Interview Map

```text
                         OOP
                          |
       +------------------+------------------+
       |                  |                  |
       ↓                  ↓                  ↓
   Encapsulation      Abstraction        Inheritance
       |                  |                  |
       ↓                  ↓                  ↓
   Data Control      Hide Complexity      Reuse
       |                  |                  |
       +------------------+------------------+
                          |
                          ↓
                    Polymorphism
                          |
                +---------+---------+
                |                   |
                ↓                   ↓
           Overloading         Overriding
           Compile Time        Runtime
                |                   |
                |                   ↓
                |            Dynamic Dispatch
                |
                +-------------------+
                                    |
                                    ↓
                             SOLID Principles
                                    |
             +----------+-----------+----------+
             |          |           |          |
             ↓          ↓           ↓          ↓
            SRP        OCP         LSP        ISP
             |          |           |          |
             +----------+-----------+----------+
                                    |
                                    ↓
                                   DIP
                                    |
                                    ↓
                          Low Coupling
                              +
                         High Cohesion
```

---

# 108. Golden Rules for OOP Interviews

> [!important] Must Remember

```text
1. Class = Blueprint
2. Object = Runtime Instance
3. Encapsulation = Bundle + Control Access
4. Abstraction = Hide Complexity
5. Inheritance = IS-A
6. Composition = HAS-A
7. Overloading = Compile Time
8. Overriding = Runtime
9. Constructor = Initialization
10. Constructor cannot be overridden
11. Static methods are hidden, not overridden
12. Private methods are not overridden
13. Final methods cannot be overridden
14. Abstract classes cannot be instantiated directly
15. Interfaces cannot have constructors
16. Java does not support multiple inheritance of classes
17. Java supports multiple interface implementation
18. == compares reference identity for objects
19. equals() compares logical equality according to implementation
20. Equal objects must have equal hash codes
21. Coupling = BETWEEN
22. Cohesion = WITHIN
23. Good design = Low Coupling + High Cohesion
24. SRP = One primary responsibility
25. OCP = Open for extension, closed for unnecessary modification
26. LSP = Safe substitution
27. ISP = Focused interfaces
28. DIP = Depend on abstractions
29. IS-A → Inheritance/Subtyping
30. HAS-A → Composition/Aggregation
```

---

# 109. Quick Revision

> [!summary] One-Minute Revision

## Four Pillars

```text
Encapsulation
→ Protect and control state

Abstraction
→ Hide unnecessary implementation

Inheritance
→ Reuse/derive behavior

Polymorphism
→ One interface, multiple behaviors
```

## Polymorphism

```text
Overloading
→ Compile Time

Overriding
→ Runtime
```

## Constructors

```text
Same class name
No return type
Can overload
Cannot override
Not inherited
```

## `this`

```text
Current object
```

## `super`

```text
Immediate parent
```

## `static`

```text
Class-level member
```

## `final`

```text
Variable → Cannot reassign
Method → Cannot override
Class → Cannot extend
```

## Relationships

```text
Association
→ General relationship

Aggregation
→ Weak ownership

Composition
→ Strong ownership
```

## Design

```text
Low Coupling
+
High Cohesion
```

## SOLID

```text
S → Single Responsibility
O → Open/Closed
L → Liskov Substitution
I → Interface Segregation
D → Dependency Inversion
```

## Most Important Interview Traps

```text
Return type alone
→ Cannot overload

Constructor
→ Cannot override

Static method
→ Cannot override

Private method
→ Cannot override

Final method
→ Cannot override

Abstract class
→ Cannot instantiate directly

Interface
→ No constructor

final reference
→ Does NOT make object immutable
```

## Runtime Polymorphism

For:

~~~java
Parent p = new Child();
~~~

remember:

```text
Reference Type → Accessible members

Actual Object → Overridden instance method behavior
```

---

# 110. Golden Memory Trick

**Protect with Encapsulation, hide with Abstraction, reuse with Inheritance, behave differently with Polymorphism, and design everything with Low Coupling + High Cohesion.**

# 111. One-Line Recognition

**When an OOP interview question appears, first identify whether it is testing object structure, data protection, abstraction, inheritance, polymorphism, Java-specific rules, or software design principles.**