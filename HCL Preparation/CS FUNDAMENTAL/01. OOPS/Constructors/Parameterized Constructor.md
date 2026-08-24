---
type: concept
subject: aptitude
topic: "Parameterized Constructor"
parent: "Constructors"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - constructors
  - parameterized-constructor
  - object-initialization
  - java
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Constructors]]"
  - "[[Default Constructor]]"
  - "[[Constructor Overloading]]"
  - "[[this Keyword]]"
  - "[[Inheritance]]"
---

# Parameterized Constructor

> [!summary]
> A **parameterized constructor** is a constructor that accepts one or more parameters and uses them to initialize an object when it is created.
>
> Core pattern:
>
>     new Class(value1, value2)
>             ↓
>     Matching Constructor
>             ↓
>     Object Initialized
>
> Fast recognition:
>
> **Constructor + one or more parameters + object creation with arguments = Parameterized Constructor**

# 1. Core Concept

Suppose we have:

    class Student {

        int id;
        String name;
    }

Without a parameterized constructor, we may need:

    Student s = new Student();

    s.id = 101;
    s.name = "Arun";

This requires multiple statements.

A parameterized constructor allows us to initialize the object during creation:

    class Student {

        int id;
        String name;

        Student(int id, String name) {

            this.id = id;
            this.name = name;
        }
    }

Now:

    Student s = new Student(101, "Arun");

The object is created and initialized in one statement.

# 2. Basic Meaning

A parameterized constructor is simply a constructor with parameters.

Example:

    class Employee {

        int id;
        String name;
        double salary;

        Employee(int id, String name, double salary) {

            this.id = id;
            this.name = name;
            this.salary = salary;
        }
    }

Object creation:

    Employee e =
        new Employee(101, "Rahul", 50000);

The values:

    101
    "Rahul"
    50000

are passed to the constructor.

The constructor stores them inside the object.

# 3. Main Formula

There is no mathematical formula, but remember:

$$
\boxed{
\text{Parameterized Constructor}
=
\text{Constructor}
+
\text{One or More Parameters}
}
$$

Object creation:

$$
\boxed{
\text{new Class(arguments)}
\rightarrow
\text{Matching Constructor}
}
$$

Initialization pattern:

$$
\boxed{
\text{Parameter}
\rightarrow
\text{Instance Variable}
}
$$

Common Java pattern:

    this.field = parameter;

# 4. Basic Syntax

General syntax:

    class ClassName {

        ClassName(dataType parameter1,
                  dataType parameter2) {

            // initialization
        }
    }

Example:

    class Student {

        int id;
        String name;

        Student(int id, String name) {

            this.id = id;
            this.name = name;
        }
    }

Creation:

    Student s = new Student(101, "Arun");

# 5. Why Parameterized Constructors Are Needed

Without constructor:

    Student s = new Student();

    s.id = 101;
    s.name = "Arun";

With parameterized constructor:

    Student s = new Student(101, "Arun");

Benefits:

    Less code
    ↓
    Immediate initialization
    ↓
    Better readability
    ↓
    Easier object creation
    ↓
    Better control over object state

# 6. Basic Example

## Question

Create a `Student` object with an ID and name using a parameterized constructor.

## Solution

    class Student {

        int id;
        String name;

        Student(int id, String name) {

            this.id = id;
            this.name = name;
        }
    }

Create object:

    Student s = new Student(101, "Pradeep");

Values become:

    s.id   = 101
    s.name = "Pradeep"

## Answer

$$
\boxed{
id=101,\ name=\text{"Pradeep"}
}
$$

# 7. Understanding `this`

Consider:

    class Student {

        int id;

        Student(int id) {

            this.id = id;
        }
    }

There are two `id`s.

    this.id
       ↓
    Instance variable

    id
       ↓
    Constructor parameter

Therefore:

    this.id = id;

means:

    object.id = parameter id

This is one of the most important constructor patterns in Java.

# 8. Why `this` Is Commonly Used

Consider:

    class Student {

        int id;

        Student(int value) {

            id = value;
        }
    }

This works.

But when parameter and field have the same name:

    class Student {

        int id;

        Student(int id) {

            this.id = id;
        }
    }

`this` clearly distinguishes the object's field from the parameter.

Pattern:

    this.field = parameter;

This is widely used in Java code.

# 9. Real-Time Example — Student Management

Imagine a college application.

Every student needs:

    studentId
    name
    department
    year

A parameterized constructor can initialize all of them:

    class Student {

        int studentId;
        String name;
        String department;
        int year;

        Student(int studentId,
                String name,
                String department,
                int year) {

            this.studentId = studentId;
            this.name = name;
            this.department = department;
            this.year = year;
        }
    }

Create:

    Student s = new Student(
        101,
        "Arun",
        "CSE",
        4
    );

Now the object immediately has meaningful data.

# 10. Real-Time Example — Employee

    class Employee {

        int id;
        String name;
        String department;
        double salary;

        Employee(int id,
                 String name,
                 String department,
                 double salary) {

            this.id = id;
            this.name = name;
            this.department = department;
            this.salary = salary;
        }
    }

Create:

    Employee e = new Employee(
        1001,
        "Rahul",
        "Engineering",
        75000
    );

The constructor establishes the initial employee state.

# 11. Real-Time Example — Product

An e-commerce application may have:

    Product ID
    Product Name
    Price
    Quantity

Constructor:

    class Product {

        int id;
        String name;
        double price;
        int quantity;

        Product(int id,
                String name,
                double price,
                int quantity) {

            this.id = id;
            this.name = name;
            this.price = price;
            this.quantity = quantity;
        }
    }

Create:

    Product p = new Product(
        501,
        "Laptop",
        65000,
        2
    );

# 12. Real-Time Example — Bank Account

A bank account may require:

    accountNumber
    holderName
    balance

Constructor:

    class BankAccount {

        String accountNumber;
        String holderName;
        double balance;

        BankAccount(String accountNumber,
                    String holderName,
                    double balance) {

            this.accountNumber = accountNumber;
            this.holderName = holderName;
            this.balance = balance;
        }
    }

Create:

    BankAccount account =
        new BankAccount(
            "ACC1001",
            "Arun",
            25000
        );

# 13. Real-Time Example — Car

    class Car {

        String brand;
        String model;
        int year;

        Car(String brand,
            String model,
            int year) {

            this.brand = brand;
            this.model = model;
            this.year = year;
        }
    }

Create:

    Car car =
        new Car("Toyota", "Camry", 2026);

The constructor creates a properly initialized car object.

# 14. Real-Time Example — User Account

    class User {

        String username;
        String email;
        String role;

        User(String username,
             String email,
             String role) {

            this.username = username;
            this.email = email;
            this.role = role;
        }
    }

Create:

    User user =
        new User(
            "arun123",
            "arun@example.com",
            "ADMIN"
        );

This pattern is common in backend applications.

# 15. Real-Time Example — API Request Object

Suppose an application receives:

    userId
    endpoint
    method

We can model the request:

    class Request {

        int userId;
        String endpoint;
        String method;

        Request(int userId,
                String endpoint,
                String method) {

            this.userId = userId;
            this.endpoint = endpoint;
            this.method = method;
        }
    }

Create:

    Request request =
        new Request(
            101,
            "/users",
            "GET"
        );

# 16. Parameterized Constructor and Object State

A constructor should ideally establish a meaningful initial state.

Example:

    class Rectangle {

        int length;
        int width;

        Rectangle(int length, int width) {

            this.length = length;
            this.width = width;
        }
    }

Create:

    Rectangle r = new Rectangle(10, 5);

Object state:

    length = 10
    width = 5

Then:

    int area = r.length * r.width;

Therefore:

    area = 50

# 17. Parameterized Constructor vs Field Assignment

Without constructor:

    Student s = new Student();

    s.id = 101;
    s.name = "Arun";
    s.department = "CSE";

With constructor:

    Student s =
        new Student(101, "Arun", "CSE");

The second approach communicates the required initial state more clearly.

# 18. Parameterized Constructor vs Default Constructor

| Feature | Default Constructor | Parameterized Constructor |
|---|---|---|
| Arguments | None | One or more |
| Initialization | Default field values | Supplied values |
| Example | `new Student()` | `new Student(101, "A")` |
| Compiler generated | If no constructor declared | No |
| Programmer written | Not necessarily | Yes |
| Main purpose | Basic object creation | Custom initialization |

# 19. Important Rule — Parameterized Constructor Is Not Automatically Generated

Java does not automatically create:

    Student(int id)

for you.

If you need it, you must declare it.

Example:

    class Student {

        int id;

        Student(int id) {
            this.id = id;
        }
    }

# 20. Important Rule — Parameterized Constructor Removes Automatic Default Constructor

This is one of the most important interview patterns.

Consider:

    class Student {

        Student(int id) {
            System.out.println(id);
        }
    }

Now:

    Student s = new Student();

Compilation error.

Why?

Because:

    Student(int)

exists.

But:

    Student()

does not exist.

The compiler does not generate the default constructor after a constructor has been declared.

# 21. How to Support Both Forms

If you need:

    new Student()

and:

    new Student(101)

define both constructors.

Example:

    class Student {

        int id;

        Student() {

            id = 0;
        }

        Student(int id) {

            this.id = id;
        }
    }

Now both are valid:

    Student s1 = new Student();

    Student s2 = new Student(101);

This is constructor overloading.

# 22. Constructor Overloading Preview

Example:

    class Student {

        Student() {
        }

        Student(int id) {
        }

        Student(int id, String name) {
        }
    }

Available forms:

    Student()
    Student(int)
    Student(int, String)

Java chooses the matching constructor based on the arguments.

This is compile-time constructor selection.

# 23. Constructor Matching

Suppose:

    class Student {

        Student(int id) {
        }

        Student(String name) {
        }
    }

Then:

    new Student(101)

matches:

    Student(int)

And:

    new Student("Arun")

matches:

    Student(String)

But:

    new Student(10.5)

does not directly match either constructor in the same way.

The compiler searches for a compatible constructor.

# 24. Exact Matching

Suppose:

    class Test {

        Test(int x) {
            System.out.println("int");
        }

        Test(String x) {
            System.out.println("String");
        }
    }

Then:

    new Test(10);

prints:

    int

And:

    new Test("10");

prints:

    String

The argument types guide constructor selection.

# 25. Type Conversion During Constructor Selection

Java can consider widening conversions.

Example:

    class Test {

        Test(long x) {
            System.out.println("long");
        }
    }

Now:

    Test t = new Test(10);

The literal:

    10

is an `int`.

It can widen:

    int → long

Therefore the constructor can be selected.

# 26. Constructor Selection Priority

For overloaded constructors, Java generally prefers the most specific applicable match.

A useful mental order is:

    Exact match
        ↓
    Widening primitive
        ↓
    Reference widening
        ↓
    Other applicable conversions

For interview questions, always first look for an exact match.

# 27. Ambiguous Constructor Calls

Consider:

    class Test {

        Test(Integer x) {
            System.out.println("Integer");
        }

        Test(String x) {
            System.out.println("String");
        }
    }

Calling:

    new Test(null);

can be ambiguous because `null` can be assigned to both reference types.

Therefore compilation can fail due to ambiguity.

> [!warning]
> **`null` is compatible with reference types, so overloaded constructors accepting unrelated reference types can become ambiguous.**

# 28. Primitive vs Wrapper Trap

Consider:

    class Test {

        Test(int x) {
            System.out.println("int");
        }

        Test(Integer x) {
            System.out.println("Integer");
        }
    }

Now:

    new Test(10);

The exact primitive match:

    int

is preferred.

Output:

    int

This is a common overload-resolution question.

# 29. `this` Constructor Chaining

A constructor can call another constructor in the same class using:

    this(...)

Example:

    class Student {

        int id;
        String name;

        Student() {

            this(0, "Unknown");
        }

        Student(int id, String name) {

            this.id = id;
            this.name = name;
        }
    }

Now:

    Student s = new Student();

Execution:

    Student()
       ↓
    this(0, "Unknown")
       ↓
    Student(int, String)

This avoids duplicate initialization code.

# 30. Important Rule — `this()` Must Be First

If using:

    this(...)

it must be the first statement in the constructor.

Valid:

    Student() {

        this(0, "Unknown");

        System.out.println("Created");
    }

Invalid:

    Student() {

        System.out.println("Created");

        this(0, "Unknown");
    }

> [!important]
> **`this(...)` must be the first statement of a constructor.**

# 31. `this()` vs `this`

Do not confuse:

    this

and:

    this()

### `this`

Refers to the current object.

Example:

    this.id = id;

### `this()`

Calls another constructor in the same class.

Example:

    this(101);

Memory:

    this.field
    → current object's field

    this(...)
    → another constructor in same class

# 32. Constructor Chaining with `this()`

Example:

    class Employee {

        int id;
        String name;
        double salary;

        Employee() {

            this(0, "Unknown", 0.0);
        }

        Employee(int id, String name, double salary) {

            this.id = id;
            this.name = name;
            this.salary = salary;
        }
    }

Now:

    Employee e = new Employee();

The no-argument constructor delegates to the parameterized constructor.

This reduces duplication.

# 33. Real-Time Example — Default Values with Constructor Chaining

    class User {

        String name;
        String role;

        User() {

            this("Guest", "USER");
        }

        User(String name, String role) {

            this.name = name;
            this.role = role;
        }
    }

Now:

    User u = new User();

produces:

    name = "Guest"
    role = "USER"

This is a clean design pattern.

# 34. Validation Inside Parameterized Constructor

Constructors can validate input.

Example:

    class BankAccount {

        double balance;

        BankAccount(double balance) {

            if (balance < 0) {
                throw new IllegalArgumentException(
                    "Balance cannot be negative"
                );
            }

            this.balance = balance;
        }
    }

Now:

    BankAccount account =
        new BankAccount(10000);

is valid.

But:

    new BankAccount(-500);

throws an exception.

This helps prevent invalid object states.

# 35. Real-Time Example — Age Validation

    class Person {

        String name;
        int age;

        Person(String name, int age) {

            if (age < 0) {
                throw new IllegalArgumentException(
                    "Age cannot be negative"
                );
            }

            this.name = name;
            this.age = age;
        }
    }

This ensures:

    age >= 0

at object creation.

# 36. Real-Time Example — Product Price Validation

    class Product {

        String name;
        double price;

        Product(String name, double price) {

            if (price < 0) {
                throw new IllegalArgumentException(
                    "Price cannot be negative"
                );
            }

            this.name = name;
            this.price = price;
        }
    }

This protects the object's initial state.

# 37. Real-Time Example — Employee ID Validation

    class Employee {

        int id;
        String name;

        Employee(int id, String name) {

            if (id <= 0) {
                throw new IllegalArgumentException(
                    "Invalid employee ID"
                );
            }

            this.id = id;
            this.name = name;
        }
    }

This is much safer than creating an object with an invalid ID and checking it later.

# 38. Parameterized Constructor and Encapsulation

Consider:

    class BankAccount {

        private double balance;

        BankAccount(double balance) {

            if (balance < 0) {
                throw new IllegalArgumentException();
            }

            this.balance = balance;
        }
    }

The constructor controls how the object begins its life.

This works together with encapsulation:

    private state
         +
    controlled initialization
         ↓
    safer object

# 39. Parameterized Constructor and Immutability

Constructors are especially important for immutable objects.

Example:

    final class Student {

        private final int id;
        private final String name;

        Student(int id, String name) {

            this.id = id;
            this.name = name;
        }
    }

Once initialized:

    id
    name

cannot be reassigned.

The constructor becomes the main place where the object's final state is established.

# 40. Real-Time Example — Immutable Configuration

    final class ServerConfig {

        private final String host;
        private final int port;

        ServerConfig(String host, int port) {

            this.host = host;
            this.port = port;
        }
    }

Create:

    ServerConfig config =
        new ServerConfig("localhost", 8080);

The configuration is established at construction time.

# 41. Parameterized Constructor and Dependency Injection

In professional applications, constructors are often used to provide dependencies.

Example:

    class UserService {

        private UserRepository repository;

        UserService(UserRepository repository) {

            this.repository = repository;
        }
    }

Create:

    UserRepository repository =
        new UserRepository();

    UserService service =
        new UserService(repository);

The dependency is explicitly supplied to the object.

This is called constructor-based dependency injection.

# 42. Why Constructor Injection Is Powerful

Instead of:

    UserService service =
        new UserService();

and later:

    service.setRepository(repository);

we can require the dependency during creation:

    new UserService(repository)

This communicates:

    UserService
       ↓
    requires Repository
       ↓
    Constructor enforces dependency

This is an important real-world design pattern.

# 43. Parameterized Constructor and Object Validity

A useful design principle is:

> An object should preferably be valid immediately after construction.

Example:

    class Rectangle {

        private final int length;
        private final int width;

        Rectangle(int length, int width) {

            if (length <= 0 || width <= 0) {
                throw new IllegalArgumentException(
                    "Dimensions must be positive"
                );
            }

            this.length = length;
            this.width = width;
        }
    }

Now every successfully created rectangle satisfies:

    length > 0
    width > 0

This is much stronger than allowing invalid objects.

# 44. Advanced Example — Constructor Chaining

Consider:

    class Employee {

        int id;
        String name;
        double salary;

        Employee() {

            this(0, "Unknown", 0);
        }

        Employee(int id) {

            this(id, "Unknown", 0);
        }

        Employee(int id, String name, double salary) {

            this.id = id;
            this.name = name;
            this.salary = salary;
        }
    }

Now:

    Employee e1 = new Employee();

    Employee e2 = new Employee(101);

    Employee e3 =
        new Employee(101, "Arun", 50000);

Execution paths:

    e1
    ↓
    Employee()
    ↓
    Employee(int, String, double)

    e2
    ↓
    Employee(int)
    ↓
    Employee(int, String, double)

    e3
    ↓
    Employee(int, String, double)

This is constructor overloading combined with constructor chaining.

# 45. Advanced Example — Parent + Parameterized Constructor

Consider:

    class Person {

        String name;

        Person(String name) {

            this.name = name;
        }
    }

    class Student extends Person {

        int id;

        Student(int id, String name) {

            super(name);
            this.id = id;
        }
    }

Create:

    Student s =
        new Student(101, "Arun");

Execution:

    Student constructor
          ↓
    super(name)
          ↓
    Person constructor
          ↓
    this.id = id

Object becomes:

    id = 101
    name = "Arun"

# 46. `super(...)` in Parameterized Constructors

A child constructor can invoke a parent constructor using:

    super(arguments);

Example:

    class Animal {

        String name;

        Animal(String name) {

            this.name = name;
        }
    }

    class Dog extends Animal {

        String breed;

        Dog(String name, String breed) {

            super(name);
            this.breed = breed;
        }
    }

Create:

    Dog dog =
        new Dog("Bruno", "Labrador");

The parent portion is initialized by:

    super(name)

The child portion is initialized by:

    this.breed = breed

# 47. `super()` vs `this()`

| Keyword | Purpose |
|---|---|
| `this` | Current object |
| `this(...)` | Calls another constructor in same class |
| `super` | Parent-class reference |
| `super(...)` | Calls parent constructor |

Memory:

    this(...)
    → Same class

    super(...)
    → Parent class

# 48. Important Rule — `this()` and `super()` Cannot Both Be First

A constructor cannot directly start with both:

    this(...)

and:

    super(...)

because both must be the first statement.

Example:

    class Student {

        Student() {

            this(101);
            super();
        }
    }

Invalid.

Why?

A constructor can delegate to:

    another constructor in same class

or:

    superclass constructor

but not both directly.

# 49. Constructor Initialization Order

Suppose:

    class Parent {

        int x = 10;

        Parent(int value) {

            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        int y = 20;

        Child(int value) {

            super(value);
            System.out.println("Child");
        }
    }

When:

    Child c = new Child(5);

the general flow is:

    Object memory allocation
          ↓
    Fields receive initial/default values
          ↓
    Parent initialization
          ↓
    Parent constructor
          ↓
    Child field initialization
          ↓
    Child constructor body

Understanding this becomes important in advanced constructor output questions.

# 50. Constructor vs Setter

Suppose:

    Student s = new Student();

    s.setId(101);
    s.setName("Arun");

Alternative:

    Student s =
        new Student(101, "Arun");

Constructor initialization is often preferable when values are required for a valid object.

A setter is useful when a property is allowed to change after construction.

Think:

    Required at creation
    → Constructor

    Changeable after creation
    → Setter

This is a design guideline, not an absolute rule.

# 51. Parameterized Constructor and Encapsulation

A constructor can initialize private fields:

    class Account {

        private String accountNumber;
        private double balance;

        Account(String accountNumber,
                double balance) {

            this.accountNumber = accountNumber;
            this.balance = balance;
        }
    }

External code cannot directly modify the private fields.

The constructor controls initial state.

# 52. Advanced Example — Defensive Validation

    class User {

        private final String username;

        User(String username) {

            if (username == null ||
                username.isBlank()) {

                throw new IllegalArgumentException(
                    "Username is required"
                );
            }

            this.username = username;
        }
    }

This creates a strong invariant:

    username
    ≠ null
    AND
    username is not blank

after successful construction.

# 53. Constructor and `final` Variables

A blank final instance variable can be initialized in a constructor.

Example:

    class Student {

        private final int id;

        Student(int id) {

            this.id = id;
        }
    }

This is valid.

After initialization:

    id

cannot be reassigned.

This is an important real-world use of parameterized constructors.

# 54. Constructor and Static Variables

Static fields belong to the class, not individual objects.

A parameterized constructor can technically modify static state, but this should be done deliberately.

Example:

    class Student {

        static int count;

        Student() {

            count++;
        }
    }

Each object creation increments:

    Student.count

But static state is shared by all objects.

# 55. Parameterized Constructor with Arrays

A constructor can receive arrays.

Example:

    class Student {

        int[] marks;

        Student(int[] marks) {

            this.marks = marks;
        }
    }

Create:

    int[] marks = {90, 85, 95};

    Student s =
        new Student(marks);

The constructor receives the array reference.

# 56. Parameterized Constructor with Objects

Constructors can accept objects as parameters.

Example:

    class Address {

        String city;

        Address(String city) {
            this.city = city;
        }
    }

    class Student {

        String name;
        Address address;

        Student(String name, Address address) {

            this.name = name;
            this.address = address;
        }
    }

Create:

    Address address =
        new Address("Trichy");

    Student student =
        new Student("Arun", address);

This is common in object-oriented design.

# 57. Constructor Parameter vs Field Reference

Consider:

    class Employee {

        String name;

        Employee(String name) {

            this.name = name;
        }
    }

Inside the constructor:

    name

refers to the nearest parameter.

Therefore:

    this.name

is needed to explicitly refer to the instance variable.

Memory:

    this.name = name;

means:

    object field = constructor parameter

# 58. What Happens If `this` Is Removed?

Consider:

    class Student {

        int id;

        Student(int id) {

            id = id;
        }
    }

This compiles, but both sides refer to the parameter.

The instance field remains unchanged.

Therefore:

    this.id = id;

is required when both names are the same.

This is a very common bug.

# 59. Output Question — Missing `this`

    class Student {

        int id;

        Student(int id) {

            id = id;
        }
    }

    Student s = new Student(101);

    System.out.println(s.id);

Output:

    0

Why?

    id = id

assigns the parameter to itself.

Correct:

    this.id = id;

Then output:

    101

# 60. Output Question — Correct `this`

    class Student {

        int id;

        Student(int id) {

            this.id = id;
        }
    }

    Student s = new Student(101);

    System.out.println(s.id);

Output:

    101

# 61. Advanced Output — Constructor Chaining

Consider:

    class Test {

        int x;

        Test() {

            this(100);
        }

        Test(int x) {

            this.x = x;
        }
    }

    Test t = new Test();

    System.out.println(t.x);

Execution:

    Test()
      ↓
    this(100)
      ↓
    Test(int)
      ↓
    this.x = 100

Answer:

    100

# 62. Advanced Output — Parent Constructor

    class Parent {

        Parent(int x) {

            System.out.println("Parent " + x);
        }
    }

    class Child extends Parent {

        Child() {

            super(10);
            System.out.println("Child");
        }
    }

    Child c = new Child();

Output:

    Parent 10
    Child

# 63. Advanced Output — Constructor Order

    class A {

        A() {
            System.out.println("A");
        }
    }

    class B extends A {

        B(int x) {
            System.out.println("B");
        }
    }

    B b = new B(10);

Output:

    A
    B

Why?

The child constructor implicitly begins with:

    super()

because `A()` exists.

# 64. Advanced Output — Parameterized Parent

    class A {

        A(int x) {
            System.out.println("A");
        }
    }

    class B extends A {

        B() {
            super(10);
            System.out.println("B");
        }
    }

    B b = new B();

Output:

    A
    B

# 65. Advanced Output — `this()` and `super()`

    class A {

        A(int x) {
            System.out.println("A");
        }
    }

    class B extends A {

        B() {
            this(10);
        }

        B(int x) {
            super(x);
            System.out.println("B");
        }
    }

    B b = new B();

Output:

    A
    B

Execution:

    B()
      ↓
    this(10)
      ↓
    B(int)
      ↓
    super(10)
      ↓
    A(int)

# 66. Pattern Recognition

> [!important]
> **Pattern 1 — Constructor Has Parameters**
>
> If you see:
>
>     Student(int id)
>
> think:
>
> **Parameterized Constructor**

> [!important]
> **Pattern 2 — Object Created With Arguments**
>
> If you see:
>
>     new Student(101)
>
> search for:
>
>     Student(int)

> [!important]
> **Pattern 3 — `this.field = parameter`**
>
> If you see:
>
>     this.id = id;
>
> think:
>
> **Constructor parameter is initializing the instance field.**

> [!important]
> **Pattern 4 — Parameterized Constructor Exists**
>
> If a class contains:
>
>     Student(int id)
>
> do not assume:
>
>     Student()
>
> exists.

> [!important]
> **Pattern 5 — `this(...)`**
>
> If you see:
>
>     this(10);
>
> think:
>
> **Constructor chaining within the same class.**

> [!important]
> **Pattern 6 — `super(...)`**
>
> If you see:
>
>     super(10);
>
> think:
>
> **Calling parent constructor.**

> [!important]
> **Pattern 7 — Validation**
>
> If constructor checks:
>
>     if (value < 0)
>
> think:
>
> **Object invariant / valid initial state.**

> [!important]
> **Pattern 8 — `final` Field**
>
> If you see:
>
>     private final int id;
>
> and:
>
>     this.id = id;
>
> inside the constructor:
>
> think:
>
> **Constructor initialization of a blank final field.**

# 67. Shortcuts

> [!tip]
> **Shortcut 1 — P-C-I**
>
>     P = Parameters
>     C = Constructor
>     I = Initialization
>
> Parameterized Constructor:
>
> **Parameters → Constructor → Initialization**

> [!tip]
> **Shortcut 2 — `this.field = parameter`**
>
> Memorize:
>
>     this.x = x;
>
> as:
>
>     object's x = incoming x

> [!tip]
> **Shortcut 3 — `new Class(args)`**
>
> For:
>
>     new Student(101, "A")
>
> immediately search for:
>
>     Student(int, String)

> [!tip]
> **Shortcut 4 — Any Constructor Removes Automatic Default**
>
>     Student(int x)
>
> means:
>
>     Student()
>
> is NOT automatically available.

> [!tip]
> **Shortcut 5 — `this()`**
>
>     this(...)
>     → same class constructor

> [!tip]
> **Shortcut 6 — `super()`**
>
>     super(...)
>     → parent constructor

> [!tip]
> **Shortcut 7 — Required vs Optional**
>
> Required at object creation:
>
>     Constructor
>
> Optional/changeable later:
>
>     Setter

> [!tip]
> **Shortcut 8 — Constructor Output**
>
> When solving output questions:
>
>     new
>      ↓
>     matching constructor
>      ↓
>     super / this chain
>      ↓
>     constructor body
>
> Follow the chain in this order.

# 68. Common Exam Patterns

> [!important] Must Master

1. Basic parameterized constructor
2. `this.field = parameter`
3. Constructor vs method
4. Default vs parameterized constructor
5. Parameterized constructor suppressing automatic default constructor
6. Constructor overloading
7. Constructor chaining with `this()`
8. Parent constructor chaining with `super()`
9. Constructor argument matching
10. Primitive widening during overload resolution
11. Wrapper vs primitive constructor selection
12. `null` ambiguity
13. Validation inside constructors
14. Final field initialization
15. Constructor-based dependency injection
16. Encapsulation through constructors
17. Immutable objects
18. Constructor execution order
19. Inheritance and parameterized constructors
20. Output prediction
21. Missing `this`
22. `this()` vs `this`
23. `super()` vs `super`
24. Constructor invocation
25. Object state initialization

# 69. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting `this`

Wrong:

    Student(int id) {
        id = id;
    }

Correct:

    Student(int id) {
        this.id = id;
    }

---

### Mistake 2 — Assuming Default Constructor Still Exists

Wrong:

    class Student {

        Student(int id) {
        }
    }

    Student s = new Student();

This fails because `Student()` was not declared.

---

### Mistake 3 — Calling `this()` After Another Statement

Wrong:

    Student() {

        System.out.println("Hello");

        this(10);
    }

Correct:

    Student() {

        this(10);

        System.out.println("Hello");
    }

---

### Mistake 4 — Using Both `this()` and `super()` Directly

A constructor cannot directly begin with both.

---

### Mistake 5 — Confusing `this` and `this()`

    this
    → current object

    this()
    → another constructor

---

### Mistake 6 — Confusing `super` and `super()`

    super
    → parent object reference

    super()
    → parent constructor

---

### Mistake 7 — Treating Constructor Like a Method

Wrong:

    void Student(int id) {
    }

This is a method.

Correct constructor:

    Student(int id) {
    }

---

### Mistake 8 — Ignoring Parent Constructor

If a child constructor does not explicitly call `super(...)`, Java attempts an implicit no-argument superclass constructor.

If it does not exist, compilation fails.

---

### Mistake 9 — Assuming Constructor Validation Is Optional

If a constructor represents required state, validation can prevent invalid objects from being created.

---

### Mistake 10 — Forgetting Reference Parameters

When a constructor receives an object:

    Student(Address address)

the constructor receives a reference to the object.

# 70. Interview Questions

## Beginner

### Q1. What is a parameterized constructor?

**Answer:**

A parameterized constructor is a constructor that accepts one or more parameters and uses them to initialize an object.

### Q2. Why are parameterized constructors used?

**Answer:**

They allow object state to be initialized during object creation using supplied values.

### Q3. Give an example.

**Answer:**

    class Student {

        int id;

        Student(int id) {
            this.id = id;
        }
    }

Creation:

    Student s = new Student(101);

### Q4. Does Java automatically create parameterized constructors?

**Answer:**

No. Parameterized constructors must be explicitly declared.

### Q5. What happens to the default constructor when a parameterized constructor is declared?

**Answer:**

The compiler does not automatically provide the default constructor.

# 71. Intermediate Interview Questions

### Q6. Why is `this.id = id` used?

**Answer:**

The left side `this.id` refers to the instance variable, while the right side `id` refers to the constructor parameter.

### Q7. What happens if we write `id = id`?

**Answer:**

The parameter is assigned to itself, so the instance field remains unchanged.

### Q8. Can parameterized constructors be overloaded?

**Answer:**

Yes. A class can have multiple constructors with different parameter lists.

### Q9. Can a constructor call another constructor?

**Answer:**

Yes, using `this(...)`.

### Q10. Where must `this(...)` appear?

**Answer:**

It must be the first statement of the constructor.

# 72. Advanced Interview Questions

### Q11. Can a constructor call a parent constructor?

**Answer:**

Yes, using `super(...)`.

### Q12. Can a constructor call both `this(...)` and `super(...)` directly?

**Answer:**

No. Both require first-statement position, so a constructor can directly invoke either another constructor in the same class or a superclass constructor.

### Q13. Can a parameterized constructor initialize final fields?

**Answer:**

Yes. Blank final instance fields can be assigned in a constructor.

### Q14. Why are constructors useful for immutable classes?

**Answer:**

They can initialize all required final fields once, creating a complete state that cannot later be reassigned.

### Q15. What is constructor-based dependency injection?

**Answer:**

It is a design approach where required dependencies are passed through the constructor instead of being created internally or assigned later.

# 73. High-Level Interview Question

### Question

Why is constructor initialization generally better than creating an empty object and setting all fields later?

### Strong Answer

Constructor initialization can establish the required state immediately, reduce the possibility of partially initialized objects, make dependencies explicit, support validation, and improve readability. It is especially useful when certain values are required for an object to be valid.

# 74. High-Level Interview Question

### Question

Explain the difference between constructor overloading and method overloading.

### Strong Answer

Constructor overloading means defining multiple constructors in the same class with different parameter lists. Method overloading means defining multiple methods with the same name but different parameter lists. Both are resolved at compile time, but constructors are specifically responsible for object initialization.

# 75. High-Level Interview Question

### Question

Why is `this` important in parameterized constructors?

### Strong Answer

`this` provides an explicit reference to the current object. It is especially useful when constructor parameters have the same names as instance variables, allowing code such as `this.id = id` to clearly distinguish the object's field from the incoming parameter.

# 76. Output Prediction Framework

When solving parameterized-constructor questions:

    STEP 1
    Find all constructors.

         ↓

    STEP 2
    Write down each signature.

         ↓

    STEP 3
    Look at new Class(arguments).

         ↓

    STEP 4
    Find the matching constructor.

         ↓

    STEP 5
    Check for this(...).

         ↓

    STEP 6
    Check for super(...).

         ↓

    STEP 7
    Follow constructor execution order.

         ↓

    STEP 8
    Track field assignments.

         ↓

    STEP 9
    Predict final object state/output.

# 77. Master Decision Tree

    Is a constructor present?
            |
       +----+----+
       |         |
      No        Yes
       |         |
       ↓         ↓
    Default    List all
    constructor constructors
    generated
                 |
                 ↓
          Does new Class(args)
          match one?
                 |
          +------+------+
          |             |
         Yes            No
          |             |
          ↓             ↓
      Execute       Compilation
      constructor      error
                      

For parameterized construction:

    new Class(value)
          ↓
    Find matching constructor
          ↓
    Assign parameters
          ↓
    Execute constructor body
          ↓
    Object initialized

# 78. Master Recognition Table

| Code Pattern | Meaning |
|---|---|
| `Student(int id)` | Parameterized constructor |
| `new Student(101)` | Calls `Student(int)` |
| `this.id = id` | Field initialized from parameter |
| `this(...)` | Calls another constructor in same class |
| `super(...)` | Calls parent constructor |
| Any constructor declared | No automatic default constructor |
| `Student()` explicitly written | User-defined no-arg constructor |
| `final int id` initialized in constructor | Valid blank-final initialization |
| Constructor validation | Protects object state |
| Constructor accepting dependency | Constructor injection |
| Multiple constructor signatures | Constructor overloading |
| `void Student(...)` | Method, not constructor |

# 79. Formula Sheet

```text
PARAMETERIZED CONSTRUCTOR

Parameterized Constructor
=
Constructor + One or More Parameters

Example:

Student(int id, String name)

Object Creation:

new Student(101, "Arun")
→ Student(int, String)

Common Initialization:

this.field = parameter

Example:

this.id = id

this
→ Current Object

this(...)
→ Another Constructor in Same Class

super
→ Parent Reference

super(...)
→ Parent Constructor

Any Explicit Constructor
→ No Automatic Default Constructor

Constructor Overloading
→ Multiple Constructors
→ Different Parameter Lists

Constructor Validation
→ Prevent Invalid Object State

Blank final field
→ Can Be Initialized in Constructor

Constructor Injection
→ Dependency Passed Through Constructor

Required State
→ Prefer Constructor Initialization

Changeable State
→ Setter may be appropriate
```

# 80. Quick Revision

> [!summary] One-Minute Revision

### Definition

**A parameterized constructor is a constructor that accepts arguments and uses them to initialize an object during creation.**

### Core Pattern

    class Student {

        int id;

        Student(int id) {
            this.id = id;
        }
    }

    Student s = new Student(101);

### Most Important Rule

    Parameterized constructor declared
          ↓
    Automatic default constructor does NOT exist

### `this`

    this.id = id;

means:

    object.id = incoming id

### Constructor Chaining

    this(...)
    → same class constructor

    super(...)
    → parent constructor

### Important Rule

    this(...)
    → must be first statement

    super(...)
    → must be first statement

### Constructor Benefits

    Immediate initialization
    Validation
    Encapsulation
    Object validity
    Dependency injection
    Immutable object support
    Cleaner object creation

### Common Trap

    class A {

        A(int x) {
        }
    }

    A a = new A();

Result:

    Compilation Error

because:

    A()
    does not exist.

### Golden Memory Trick

**Parameterized constructor = pass the required data at `new` time and initialize the object's state immediately.**

### One-Line Recognition

**Whenever you see `ClassName(arguments)` in a constructor and `new ClassName(arguments)` during object creation, think Parameterized Constructor.**