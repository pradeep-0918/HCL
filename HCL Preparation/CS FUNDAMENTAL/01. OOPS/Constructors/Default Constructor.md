---
type: concept
subject: aptitude
topic: "Default Constructor"
parent: "Constructors"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - constructors
  - default-constructor
  - java
  - object-creation
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Constructors]]"
  - "[[Parameterized Constructor]]"
  - "[[Constructor Overloading]]"
  - "[[this Keyword]]"
  - "[[Inheritance]]"
---

# Default Constructor

> [!summary]
> A **constructor** is a special member of a class that is executed when an object is created.
>
> A **default constructor** in Java is the no-argument constructor that the compiler automatically provides **only when the programmer does not declare any constructor**.
>
> Core idea:
>
>     No constructor written by programmer
>                 ↓
>     Compiler provides a no-argument constructor
>                 ↓
>     Object can be created using new
>
> Fast recognition:
>
> **No constructor declared + object creation → Compiler-provided default constructor**

# 1. Core Concept

Consider:

    class Student {

        int id;
        String name;
    }

No constructor is written.

Now:

    Student s = new Student();

This is valid.

Why?

Because Java automatically provides a constructor similar to:

    Student() {
        super();
    }

This compiler-provided constructor is commonly called the **default constructor**.

It allows the object to be created without explicitly writing a constructor.

# 2. Basic Meaning

A constructor is used to initialize an object during object creation.

Example:

    Student s = new Student();

The expression:

    new Student()

creates the object and invokes a constructor.

If no constructor is explicitly declared in `Student`, Java supplies a no-argument constructor automatically.

Conceptually:

    class Student {

        int id;
        String name;

        // Compiler provides this
        Student() {
            super();
        }
    }

# 3. Important Terminology

The word "default constructor" is often used loosely.

For interviews, distinguish these carefully:

| Term | Meaning |
|---|---|
| Default constructor | Compiler-provided no-argument constructor when no constructor is declared |
| No-argument constructor | Any constructor that takes zero arguments |
| User-defined constructor | Constructor explicitly written by programmer |

This distinction is extremely important.

> [!important]
> **Every default constructor is a no-argument constructor, but not every no-argument constructor is a compiler-provided default constructor.**

# 4. Main Rule

The most important Java rule is:

$$
\boxed{
\text{No Constructor Declared}
\Rightarrow
\text{Compiler Provides Default Constructor}
}
$$

But:

$$
\boxed{
\text{Any Constructor Declared}
\Rightarrow
\text{Compiler Does Not Provide Default Constructor}
}
$$

This is one of the most frequently tested constructor rules.

# 5. Basic Example

## Question

What happens here?

    class Student {

        int id;
        String name;
    }

    public class Main {

        public static void main(String[] args) {

            Student s = new Student();

            System.out.println(s.id);
            System.out.println(s.name);
        }
    }

## Step 1

No constructor is declared.

## Step 2

Java provides a compiler-generated no-argument constructor.

## Step 3

Object is created:

    new Student()

## Step 4

Instance fields receive Java's default values.

For:

    int id

default value:

    0

For:

    String name

default value:

    null

## Answer

    0
    null

# 6. Default Values of Instance Variables

When an object is created, instance variables receive default values if they are not explicitly initialized.

| Data Type | Default Value |
|---|---|
| `byte` | `0` |
| `short` | `0` |
| `int` | `0` |
| `long` | `0L` |
| `float` | `0.0f` |
| `double` | `0.0d` |
| `char` | `'\u0000'` |
| `boolean` | `false` |
| Reference types | `null` |

Example:

    class Demo {

        int a;
        double b;
        boolean c;
        char d;
        String e;
    }

After:

    Demo obj = new Demo();

Conceptually:

    a = 0
    b = 0.0
    c = false
    d = '\u0000'
    e = null

# 7. Default Constructor Does Not Mean "Initialize Everything to Zero"

This is an important conceptual distinction.

The constructor itself does not magically set every variable to zero.

Java initializes instance fields with default values as part of object initialization.

The compiler-provided constructor is responsible for constructor invocation and superclass constructor invocation.

Think:

    Object creation
         ↓
    Memory allocated
         ↓
    Instance fields get default values
         ↓
    Constructor chain executes
         ↓
    Object initialization completes

# 8. Compiler-Generated Default Constructor

Consider:

    class Employee {

        int id;
        String name;
    }

You did not write:

    Employee() {
    }

But Java allows:

    Employee e = new Employee();

Conceptually, Java supplies:

    Employee() {
        super();
    }

The exact generated bytecode is more detailed, but this is the correct conceptual model for interviews.

# 9. What Happens If You Declare a Constructor?

This is a major trap.

Consider:

    class Student {

        Student(int id) {
            System.out.println(id);
        }
    }

Now try:

    Student s = new Student();

This produces a compilation error.

Why?

Because you declared:

    Student(int id)

Therefore Java does not automatically add:

    Student()

So:

    new Student()

has no matching constructor.

> [!warning]
> **The moment you declare any constructor, Java stops providing the automatic default constructor.**

# 10. Most Important Interview Pattern

Remember this:

    No constructor written
            ↓
    Default constructor generated

But:

    Constructor written
            ↓
    No automatic default constructor

Example:

    class A {
    }

Valid:

    A a = new A();

But:

    class B {

        B(int x) {
        }
    }

Invalid:

    B b = new B();

because `B()` does not exist.

# 11. Basic Example — No Constructor

    class Car {

        String brand;
        int price;
    }

    public class Main {

        public static void main(String[] args) {

            Car car = new Car();

            System.out.println(car.brand);
            System.out.println(car.price);
        }
    }

Output:

    null
    0

Reason:

    No constructor declared
            ↓
    Compiler provides no-argument constructor
            ↓
    Instance variables have default values

# 12. Basic Example — Explicit No-Argument Constructor

Consider:

    class Car {

        String brand;
        int price;

        Car() {
            brand = "Toyota";
            price = 1000000;
        }
    }

Now:

    Car car = new Car();

Output:

    Toyota
    1000000

Important:

This is a **user-defined no-argument constructor**.

It is not the compiler-generated default constructor.

# 13. Default Constructor vs User-Defined No-Argument Constructor

| Feature | Compiler Default Constructor | User-Defined No-Argument Constructor |
|---|---|---|
| Written by programmer | No | Yes |
| Arguments | None | None |
| Automatically supplied | Yes, under condition | No |
| Custom initialization | No custom body | Yes |
| Calls `super()` | Yes conceptually | If not explicitly specified, constructor invokes superclass constructor |
| Exists after another constructor is declared | No automatic generation | Only if explicitly written |

Example of compiler-provided:

    class A {
    }

Example of user-defined:

    class B {

        B() {
            System.out.println("Hello");
        }
    }

# 14. Important Trap — "Default Constructor" vs "No-Arg Constructor"

Consider:

    class Student {

        Student() {
            System.out.println("Student created");
        }
    }

Does Java provide a default constructor?

No.

Why?

Because a constructor has already been explicitly declared.

But does the class have a no-argument constructor?

Yes.

Therefore:

    No-arg constructor = Yes

    Compiler-generated default constructor = No

This distinction is frequently useful in interviews.

# 15. Constructor Invocation

When you write:

    Student s = new Student();

the constructor is invoked during object creation.

General flow:

    new Student()
          ↓
    Memory allocated
          ↓
    Fields receive default values
          ↓
    Constructor executes
          ↓
    Object reference returned

# 16. Constructor and `new`

The keyword:

    new

does more than simply create a reference.

Example:

    Student s = new Student();

Here:

    Student s

declares a reference variable.

And:

    new Student()

creates an object and invokes the constructor.

Therefore:

    Reference
       ↓
    Student s

    Object Creation
       ↓
    new Student()

# 17. Default Constructor and `super()`

Suppose:

    class Parent {

        Parent() {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {
    }

No constructor is declared in `Child`.

Java conceptually provides:

    Child() {
        super();
    }

Therefore:

    Child child = new Child();

Output:

    Parent

The child constructor automatically invokes the parent's no-argument constructor.

# 18. Constructor Chain

Consider:

    class Parent {

        Parent() {
            System.out.println("Parent Constructor");
        }
    }

    class Child extends Parent {
    }

Now:

    Child child = new Child();

Execution:

    Child()
       ↓
    super()
       ↓
    Parent()

Output:

    Parent Constructor

# 19. Important Rule — Parent Must Have a Matching Constructor

Consider:

    class Parent {

        Parent(int x) {
            System.out.println(x);
        }
    }

    class Child extends Parent {
    }

Now:

    Child child = new Child();

This causes a compilation error.

Why?

The compiler-generated `Child()` conceptually tries:

    super();

But `Parent` does not have:

    Parent()

It only has:

    Parent(int)

Therefore the constructor chain fails.

> [!important]
> **A compiler-generated child constructor implicitly calls the parent no-argument constructor. If the parent has no accessible no-argument constructor, the child must explicitly call a suitable parent constructor.**

# 20. Fixing the Parent Constructor Problem

Parent:

    class Parent {

        Parent(int x) {
            System.out.println(x);
        }
    }

Child:

    class Child extends Parent {

        Child() {
            super(10);
        }
    }

Now:

    Child child = new Child();

Output:

    10

Execution:

    Child()
       ↓
    super(10)
       ↓
    Parent(10)

# 21. Real-Time Example — Student

Consider a student object.

    class Student {

        int id;
        String name;
        String department;
    }

If no constructor is declared:

    Student student = new Student();

the object is created with default values:

    id = 0
    name = null
    department = null

This is useful when values will be assigned later.

Example:

    student.id = 101;
    student.name = "Pradeep";
    student.department = "CSE";

# 22. Real-Time Example — Employee

    class Employee {

        int id;
        String name;
        double salary;
    }

Without a constructor:

    Employee employee = new Employee();

Initially:

    id = 0
    name = null
    salary = 0.0

Then values can be assigned:

    employee.id = 1001;
    employee.name = "Arun";
    employee.salary = 50000;

This approach works, but constructors can make object initialization cleaner.

# 23. Real-Time Example — Product

    class Product {

        int id;
        String name;
        double price;
    }

Creation:

    Product product = new Product();

Default state:

    id = 0
    name = null
    price = 0.0

A constructor can later be used to guarantee meaningful initialization.

# 24. Why Constructors Are Useful

Constructors help ensure that an object starts in a valid state.

Without constructor initialization:

    Student student = new Student();

might result in:

    id = 0
    name = null

With a parameterized constructor:

    Student student = new Student(101, "Arun");

the object can immediately have meaningful values.

Therefore:

    Constructor
       ↓
    Object Initialization
       ↓
    Valid Initial State

# 25. Default Constructor vs Parameterized Constructor

| Feature | Default Constructor | Parameterized Constructor |
|---|---|---|
| Arguments | None | One or more |
| Main purpose | Basic object creation | Initialize using supplied values |
| Example | `new Student()` | `new Student(101, "A")` |
| Compiler generated | If no constructor declared | No |
| Custom values | Usually no | Yes |

# 26. Constructor Types in Java

At a high level, constructors can be discussed as:

    1. Compiler-Provided Default Constructor
    2. User-Defined No-Argument Constructor
    3. Parameterized Constructor
    4. Constructor Overloading

Current topic:

    Default Constructor

The next constructor topics build on this foundation.

# 27. Default Constructor and Inheritance

Consider:

    class Animal {
    }

    class Dog extends Animal {
    }

Neither class declares a constructor.

Conceptually:

    Animal() {
        super();
    }

    Dog() {
        super();
    }

When:

    Dog dog = new Dog();

the constructor chain begins with the parent.

Conceptually:

    Dog()
      ↓
    Animal()
      ↓
    Object()

This demonstrates constructor chaining.

# 28. Object Class Connection

Every Java class ultimately derives from:

    Object

Therefore constructor chaining can eventually reach:

    Object()

Example:

    class Animal {
    }

    class Dog extends Animal {
    }

Conceptually:

    Dog()
      ↓
    Animal()
      ↓
    Object()

This is a useful interview-level understanding.

# 29. Constructor Execution Order

For inheritance:

    Child object creation
          ↓
    Parent constructor
          ↓
    Child constructor

More precisely:

    Child constructor starts
          ↓
    implicit/explicit super constructor
          ↓
    Parent constructor completes
          ↓
    Child constructor body executes

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

    Child child = new Child();

Output:

    Parent
    Child

# 30. Default Constructor and Instance Variables

Consider:

    class Demo {

        int a;
        boolean b;
        String c;
    }

No constructor is declared.

After:

    Demo d = new Demo();

Values are:

    a = 0
    b = false
    c = null

Important:

These are Java's default values for instance fields.

# 31. Local Variables Are Different

This is a major Java interview trap.

Instance variable:

    class Demo {

        int x;
    }

This receives:

    0

But local variable:

    void test() {

        int x;

        System.out.println(x);
    }

does not receive an automatic default value.

This causes a compile-time error because the local variable may not have been initialized.

> [!warning]
> **Instance variables get default values. Local variables do not automatically get default values.**

# 32. Static Variables Are Different

Static fields also receive default values.

Example:

    class Demo {

        static int count;
        static String name;
    }

Before explicit assignment:

    count = 0
    name = null

This happens independently of the default constructor concept.

> [!important]
> **Do not confuse Java's default field initialization with the compiler-generated default constructor. They are related to object initialization but are conceptually different mechanisms.**

# 33. Basic Output Question

Consider:

    class Test {

        int x;
        boolean flag;
        String name;
    }

    public class Main {

        public static void main(String[] args) {

            Test t = new Test();

            System.out.println(t.x);
            System.out.println(t.flag);
            System.out.println(t.name);
        }
    }

Output:

    0
    false
    null

Reason:

    No constructor declared
          ↓
    Compiler provides default constructor
          ↓
    Instance fields have default values

# 34. Output Question — Explicit Constructor

Consider:

    class Test {

        int x;

        Test(int value) {
            x = value;
        }
    }

Now:

    Test t = new Test();

What happens?

Compilation error.

Why?

Only:

    Test(int)

exists.

There is no:

    Test()

The compiler does not create the default constructor because a constructor was already declared.

# 35. Output Question — Explicit No-Arg Constructor

Consider:

    class Test {

        int x;

        Test() {
            x = 50;
        }
    }

Now:

    Test t = new Test();

    System.out.println(t.x);

Output:

    50

This is a user-defined no-argument constructor.

It is not the compiler-generated default constructor.

# 36. Output Question — Constructor + Default Values

Consider:

    class Test {

        int x;

        Test() {
        }
    }

Now:

    Test t = new Test();

    System.out.println(t.x);

Output:

    0

The constructor exists, but it does not assign `x`.

Therefore `x` keeps its default value:

    0

# 37. Important Interview Trap

Question:

> If I write a no-argument constructor, is it called a default constructor?

Best precise answer:

> A no-argument constructor written by the programmer is a **user-defined no-argument constructor**. In Java terminology, the **default constructor** specifically refers to the constructor automatically supplied by the compiler when no constructor is declared.

This is a strong interview answer.

# 38. Default Constructor and Constructor Overloading

Suppose:

    class Student {

        Student() {
        }

        Student(int id) {
        }
    }

Now there are two constructors:

    Student()
    Student(int)

This is constructor overloading.

The compiler does not need to generate a default constructor because constructors have already been explicitly declared.

The no-argument constructor exists because the programmer wrote it.

# 39. Recognition Trick — Constructor Declaration

When reading code, first search for:

    ClassName(

Example:

    Student()
    Student(int)
    Student(String)

If you find no constructor:

    → Compiler-generated default constructor exists.

If you find at least one constructor:

    → No compiler-generated default constructor.

This is one of the fastest ways to solve constructor questions.

# 40. Recognition Trick — Object Creation

When you see:

    new ClassName()

ask:

    "Does ClassName have a zero-argument constructor?"

If no constructor is declared:

    Yes, compiler provides one.

If any constructor is declared:

    Check whether an explicit zero-argument constructor exists.

# 41. Recognition Trick — Constructor Matching

For:

    new Student()

search for:

    Student()

For:

    new Student(10)

search for:

    Student(int)

For:

    new Student("A")

search for:

    Student(String)

The constructor arguments must match an available constructor.

# 42. Recognition Trick — Constructor Exists or Not?

Use this decision tree:

    Is any constructor declared?
             |
        +----+----+
        |         |
       No        Yes
        |         |
        ↓         ↓
    Compiler    No automatic
    provides    default constructor
    default
    constructor
                  |
                  ↓
             Check declared
             constructors

# 43. Shortcuts

> [!tip]
> **Shortcut 1 — Zero Constructor Rule**
>
>     No constructor written
>     → Default constructor generated
>
> This is the most important rule.

> [!tip]
> **Shortcut 2 — One Constructor Rule**
>
>     Any constructor written
>     → No automatic default constructor
>
> Even if the constructor is parameterized.

> [!tip]
> **Shortcut 3 — `new Class()` Rule**
>
> For:
>
>     new Class()
>
> look for:
>
>     Class()
>
> If no constructor is written anywhere:
>
>     Compiler provides it.
>
> If another constructor is written:
>
>     Class() must be explicitly declared.

> [!tip]
> **Shortcut 4 — Default vs No-Arg**
>
>     Compiler-generated no-arg
>     = Default constructor
>
>     Programmer-written no-arg
>     = User-defined no-arg constructor
>
> Never confuse the two in interviews.

> [!tip]
> **Shortcut 5 — Field Values**
>
> For object fields:
>
>     int     → 0
>     double  → 0.0
>     boolean → false
>     char    → '\u0000'
>     object  → null

> [!tip]
> **Shortcut 6 — Constructor Chain**
>
> Child creation:
>
>     Child()
>       ↓
>     Parent()
>       ↓
>     Object()
>
> if suitable no-argument constructors are available.

# 44. Common Exam Patterns

> [!important] Must Master

1. No constructor declared
2. Compiler-generated default constructor
3. User-defined no-argument constructor
4. Default constructor vs no-argument constructor
5. Parameterized constructor suppressing default constructor
6. `new Class()` constructor matching
7. Constructor chaining
8. `super()` in constructors
9. Parent constructor availability
10. Default values of instance variables
11. Instance variable vs local variable
12. Static variable initialization
13. Constructor overloading
14. Parent-child constructor execution order
15. `Object()` constructor chain
16. Compile-time errors caused by missing constructors
17. Output prediction
18. Constructor invocation
19. Inheritance and constructors
20. Constructor terminology questions

# 45. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Every No-Arg Constructor Is a Default Constructor

Not precisely.

A programmer-written no-argument constructor is not the compiler-generated default constructor.

---

### Mistake 2 — Thinking Java Always Provides `Class()`

Wrong.

Java provides it automatically only when no constructor has been declared.

---

### Mistake 3 — Forgetting Parameterized Constructors Suppress the Default Constructor

Example:

    class A {

        A(int x) {
        }
    }

This does not provide:

    A()

Therefore:

    new A()

is invalid.

---

### Mistake 4 — Confusing Instance Fields and Local Variables

Instance field:

    int x;

gets:

    0

Local variable:

    int x;

must be initialized before use.

---

### Mistake 5 — Thinking Constructor Has a Return Type

This is not a constructor:

    void Student() {
    }

It is a method named `Student`.

A constructor has no return type.

---

### Mistake 6 — Thinking Constructor Is Inherited

Constructors are not inherited.

A child has its own constructors.

---

### Mistake 7 — Forgetting Parent Constructor Invocation

A child constructor implicitly invokes a suitable superclass constructor if one is not explicitly specified.

---

### Mistake 8 — Ignoring Parent Constructor Availability

If the parent has only:

    Parent(int x)

then an automatically generated child constructor cannot simply call:

    super()

because `Parent()` does not exist.

# 46. Constructor vs Method

| Feature | Constructor | Method |
|---|---|---|
| Purpose | Initialize object | Perform behavior |
| Name | Same as class | Any valid method name |
| Return type | None | Required unless `void` |
| Called automatically during `new` | Yes | No |
| Inherited | No | Can be inherited |
| Overridden | No | Yes, subject to rules |
| Can be overloaded | Yes | Yes |
| Invocation | During object creation | Explicit method call |

# 47. Default Constructor vs Method

Consider:

    class Student {

        Student() {
            System.out.println("Constructor");
        }

        void Student() {
            System.out.println("Method");
        }
    }

These are different.

    Student()

is a constructor.

    void Student()

is a method.

The presence of `void` makes it a method.

# 48. Real-Time Design Perspective

In real applications, constructors are often used to establish object state.

For example:

    class User {

        String username;
        String role;
    }

A meaningful object should have:

    username
    role

A parameterized constructor can enforce this:

    User(String username, String role)

The default constructor is useful when:

    object creation occurs first
    and initialization occurs later

But in many well-designed classes, constructors are used to ensure required values are provided immediately.

# 49. Example — Configuration Object

A configuration class may initially be created without parameters:

    class Configuration {

        String host;
        int port;
    }

    Configuration config = new Configuration();

Later:

    config.host = "localhost";
    config.port = 8080;

This is possible because the compiler-generated default constructor allows:

    new Configuration()

# 50. Example — Student Record

    class Student {

        int id;
        String name;
        String department;
    }

    Student student = new Student();

Later:

    student.id = 101;
    student.name = "Arun";
    student.department = "CSE";

This demonstrates simple object creation using a compiler-provided default constructor.

# 51. Example — Product Object

    class Product {

        int id;
        String name;
        double price;
    }

Creation:

    Product product = new Product();

Initial state:

    id = 0
    name = null
    price = 0.0

A parameterized constructor would be better when all values are required at creation time.

# 52. Advanced Interview Question — Why Does Java Provide a Default Constructor?

### Answer

The compiler provides a default constructor when no constructor is explicitly declared so that objects can still be instantiated using the no-argument form.

Example:

    class Student {
    }

allows:

    Student s = new Student();

Without this automatic constructor, the class would have no constructor available for object creation.

# 53. Advanced Interview Question — Does Every Class Have a Default Constructor?

### Answer

No.

A class receives a compiler-generated default constructor only when no constructor is explicitly declared.

Example:

    class A {
    }

has one.

But:

    class B {

        B(int x) {
        }
    }

does not automatically have:

    B()

# 54. Advanced Interview Question — Is the Default Constructor Visible?

The compiler-generated constructor has an access level corresponding to the class's accessibility in the relevant Java language rules.

For a commonly used public class:

    public class Student {
    }

the generated no-argument constructor is accessible accordingly.

For interview purposes, remember that constructor accessibility matters when another class attempts to instantiate the class.

# 55. Advanced Interview Question — What Does the Default Constructor Do?

Conceptually, a compiler-generated default constructor:

    1. Takes no arguments.
    2. Invokes the superclass no-argument constructor.
    3. Does not contain custom initialization logic written by the programmer.

Example:

    class Child {
    }

Conceptually:

    Child() {
        super();
    }

This is a useful mental model.

# 56. Advanced Interview Question — Why Does This Code Fail?

    class Parent {

        Parent(int x) {
        }
    }

    class Child extends Parent {
    }

### Reason

The compiler-generated `Child()` would need to invoke:

    super()

But:

    Parent()

does not exist.

Only:

    Parent(int)

exists.

Therefore compilation fails.

# 57. Advanced Interview Question — How Can We Fix It?

Option 1:

Add a parent no-argument constructor:

    class Parent {

        Parent() {
        }

        Parent(int x) {
        }
    }

Option 2:

Explicitly call the existing constructor:

    class Child extends Parent {

        Child() {
            super(10);
        }
    }

# 58. Output Prediction Framework

When solving constructor questions, follow:

    STEP 1
    Find the class.

         ↓

    STEP 2
    Search for constructors.

         ↓

    STEP 3
    Ask:
    Is any constructor explicitly declared?

         ↓

    NO
    ↓
    Compiler provides default constructor.

         ↓

    YES
    ↓
    No automatic default constructor.

         ↓

    STEP 4
    Match new Class(arguments)
    with available constructor.

         ↓

    STEP 5
    If inheritance exists,
    check parent constructor.

         ↓

    STEP 6
    Check implicit or explicit super().

         ↓

    STEP 7
    Check field initialization.

# 59. Interview Output Example

Consider:

    class A {

        int x;
    }

    public class Main {

        public static void main(String[] args) {

            A obj = new A();

            System.out.println(obj.x);
        }
    }

### Analysis

No constructor declared.

Therefore:

    Default constructor generated.

Instance variable:

    int x

gets:

    0

### Answer

    0

# 60. Interview Output Example — Parameterized Constructor

Consider:

    class A {

        int x;

        A(int value) {
            x = value;
        }
    }

    public class Main {

        public static void main(String[] args) {

            A obj = new A();
        }
    }

### Analysis

Declared constructor:

    A(int)

Automatic default constructor:

    Does not exist.

Required constructor:

    A()

Not found.

### Answer

    Compilation Error

# 61. Interview Output Example — Explicit No-Arg Constructor

Consider:

    class A {

        int x;

        A() {
            x = 100;
        }
    }

    A obj = new A();

    System.out.println(obj.x);

Output:

    100

Reason:

    Programmer-defined no-argument constructor
             ↓
    x = 100

# 62. Interview Output Example — Empty Constructor

Consider:

    class A {

        int x;

        A() {
        }
    }

    A obj = new A();

    System.out.println(obj.x);

Output:

    0

Why?

The constructor does not assign `x`.

Java's default initialization for the instance field remains:

    0

# 63. Interview Output Example — Constructor Chain

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

    Child obj = new Child();

Output:

    Parent
    Child

Reason:

    Child()
       ↓
    super()
       ↓
    Parent()
       ↓
    Child body

# 64. Interview Output Example — Three-Level Chain

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

    C obj = new C();

Output:

    A
    B
    C

Constructor execution moves from the topmost superclass toward the actual class.

# 65. Master Recognition Table

| Code Pattern | Result |
|---|---|
| `class A { }` | Compiler-generated default constructor |
| `class A { A() { } }` | User-defined no-arg constructor |
| `class A { A(int x) { } }` | No automatic `A()` |
| `new A()` with no constructor declared | Valid |
| `new A()` with only `A(int)` | Compilation error |
| `new A(10)` with `A(int)` | Valid |
| Child has no constructor | Compiler may generate one |
| Parent has no-arg constructor | Child can implicitly call `super()` |
| Parent has only parameterized constructor | Child needs explicit matching `super(...)` |
| Instance field `int x` | Default value `0` |
| Instance field `String s` | Default value `null` |
| Local variable `int x` | Must be initialized before use |
| Constructor with return type | It is a method, not constructor |
| Constructor inherited | No |
| Constructor overridden | No |
| Constructor overloaded | Yes |

# 66. Common Interview Traps

> [!warning] High-Priority Traps

### Trap 1

"No constructor is written."

Think:

    Compiler-generated default constructor

---

### Trap 2

"One parameterized constructor is written."

Think:

    No automatic default constructor

---

### Trap 3

"Programmer writes `ClassName()`."

Think:

    User-defined no-argument constructor

Not compiler-generated default constructor.

---

### Trap 4

"Instance variable is not initialized."

Think:

    Java gives default field value

---

### Trap 5

"Local variable is not initialized."

Think:

    Compilation error when used before definite assignment

---

### Trap 6

"Parent has only parameterized constructor."

Think:

    Child cannot implicitly call super()

---

### Trap 7

"Constructor has `void`."

Think:

    It is a method, not a constructor.

---

### Trap 8

"Constructor is inherited."

Think:

    False.

Constructors are not inherited.

---

### Trap 9

"Default constructor is overloaded."

Think carefully.

A compiler-generated default constructor exists only when no constructor is explicitly declared.

# 67. Formula Sheet

```text
DEFAULT CONSTRUCTOR

No Constructor Declared
→ Compiler Provides Default Constructor

Any Constructor Declared
→ Compiler Does Not Provide Automatic Default Constructor

Default Constructor
→ No Arguments

User-Defined No-Arg Constructor
→ Programmer Writes It

Default Constructor ≠ Every No-Arg Constructor

new Class()
→ Requires Class()

new Class(value)
→ Requires Matching Constructor

Instance Variable Defaults:

byte    → 0
short   → 0
int     → 0
long    → 0L
float   → 0.0f
double  → 0.0d
char    → '\u0000'
boolean → false
Object  → null

Constructor:
→ No Return Type
→ Same Name As Class
→ Not Inherited
→ Not Overridden
→ Can Be Overloaded

Constructor Chain:

Child()
  ↓
super()
  ↓
Parent()
  ↓
Object()

If Parent has only Parent(int):
Child must explicitly call:
super(value)
```

# 68. Quick Revision

> [!summary] One-Minute Revision

### Definition

**A default constructor is the compiler-provided no-argument constructor generated when a class declares no constructor.**

### Most Important Rule

    No constructor declared
         ↓
    Default constructor generated

    Any constructor declared
         ↓
    No automatic default constructor

### Default vs No-Arg

    Compiler-written no-arg
    → Default constructor

    Programmer-written no-arg
    → User-defined no-arg constructor

### Object Creation

    new Class()

requires:

    Class()

If no constructor is declared:

    Java provides it automatically.

If another constructor is declared:

    Class() must be explicitly provided if needed.

### Constructor Chain

    Child()
      ↓
    Parent()
      ↓
    Object()

when suitable no-argument constructors exist.

### Field Defaults

    int     → 0
    double  → 0.0
    boolean → false
    char    → '\u0000'
    Object  → null

### Important Difference

    Instance variable
    → Gets default value

    Local variable
    → Must be initialized before use

### Golden Memory Trick

**No constructor written = Java gives you a no-argument constructor; once you write any constructor, Java stops giving you one automatically.**

### One-Line Recognition

**When you see a class with no constructor declaration and `new Class()`, immediately think Compiler-Generated Default Constructor.**