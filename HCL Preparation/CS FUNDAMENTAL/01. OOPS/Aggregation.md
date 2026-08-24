---
type: concept
subject: aptitude
topic: "Aggregation"
parent: "OOPS"
company: HCL
difficulty: medium
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - java
  - aggregation
  - association
  - composition
  - has-a
  - object-relationship
  - uml
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Association]]"
  - "[[Composition]]"
  - "[[Inheritance]]"
  - "[[Coupling and Cohesion]]"
  - "[[SOLID Principles]]"
---

# Aggregation

> [!summary]
> **Aggregation is a weak whole-part relationship between two objects where the whole contains or groups the parts, but the parts can exist independently of the whole.**
>
> Core idea:
>
>     Aggregation
>     → HAS-A
>     → Whole-Part
>     → Weak Ownership
>     → Independent Lifecycle
>
> Example:
>
>     Department ◇──── Employee
>
> If the Department disappears, the Employee can still exist.
>
> The most important question is:
>
>     "Can the part exist independently of the whole?"
>
> If YES and the relationship is genuinely whole-part:
>
>     Aggregation

---

# 1. Core Concept

Aggregation is a specialized form of **Association**.

Association tells us:

    A is related to B

Aggregation tells us something more:

    A is a whole
    B is a part of A
    BUT
    B can exist independently

Example:

    Department
         ◇
         |
         |
      Employee

Here:

    Department = Whole
    Employee   = Part

But:

    Employee
       ↓
    can exist independently

Therefore:

    Department ◇── Employee

is a typical aggregation relationship.

---

# 2. Basic Meaning

Aggregation represents a **weak whole-part relationship**.

The whole contains, groups, manages, or organizes parts.

However, the whole does not completely control the lifecycle of those parts.

Examples:

    Department ◇── Employee

    Team ◇── Player

    Library ◇── Book

    Playlist ◇── Song

    University ◇── Professor

    Project ◇── Employee

The common property is:

    Whole
      ↓
    contains/groups
      ↓
    Part

while:

    Part
      ↓
    remains independently meaningful

---

# 3. Main Formula

There is no mathematical formula for aggregation.

Use this conceptual formula:

$$
\boxed{
Aggregation =
Association +
Weak\ Whole\text{-}Part\ Relationship
}
$$

The key condition is:

$$
\boxed{
Part\ Lifecycle\ is\ Independent
}
$$

Another useful mental model:

$$
\boxed{
Whole\ HAS\ Part
+
Part\ can\ survive\ Whole
=
Aggregation
}
$$

---

# 4. Core Characteristics

Aggregation has four major characteristics.

### 1. Whole-Part Relationship

There is a clear:

    Whole
       ↓
    Part

relationship.

### 2. Weak Ownership

The whole groups or contains the part but does not strongly own its lifecycle.

### 3. Independent Lifecycle

The part can continue to exist after the whole is removed.

### 4. Reusability

The part can often participate in another relationship.

Example:

    Player
       ↓
    Team A

Player leaves:

    Team A
       ↓
    Team B

The Player still exists.

---

# 5. UML Symbol

Aggregation is represented using a **hollow diamond**.

    Whole ◇──────── Part

Example:

    Department ◇──────── Employee

The diamond is placed near the **whole**.

Remember:

    ◇ = Aggregation

    ◆ = Composition

This is one of the most frequently tested OOP/UML concepts.

---

# 6. Diamond Memory Trick

> [!tip]
> **Remember the Diamonds**
>
>     ◇ = Aggregation
>     ◆ = Composition
>
> Hollow diamond:
>
>     Weak ownership
>
> Filled diamond:
>
>     Strong ownership

Memory:

    Hollow
       ↓
    Weak

    Filled
       ↓
    Strong

---

# 7. Aggregation vs Association

Association is a general relationship.

    A ───── B

Aggregation is a stronger whole-part relationship.

    A ◇──── B

| Feature | Association | Aggregation |
|---|---|---|
| General relationship | Yes | Yes |
| Whole-part | Not required | Yes |
| Weak ownership | Not required | Yes |
| Independent lifecycle | Usually | Yes |
| UML diamond | No | Hollow diamond |
| Example | Doctor-Patient | Department-Employee |

Memory:

    Association
    → "related"

    Aggregation
    → "whole has independent parts"

---

# 8. Aggregation vs Composition

This is the most important comparison.

| Feature | Aggregation | Composition |
|---|---|---|
| Relationship | Whole-Part | Whole-Part |
| Ownership | Weak | Strong |
| Part lifecycle | Independent | Dependent |
| Part can survive whole? | Yes | Generally no |
| UML symbol | ◇ | ◆ |
| Example | Team-Player | House-Room |
| Main idea | Grouping | Strong ownership |

Memory:

    Aggregation
    → Part survives

    Composition
    → Part depends on whole

---

# 9. Aggregation vs Inheritance

Inheritance represents:

    IS-A

Aggregation represents:

    HAS-A

Example:

    class Dog extends Animal

means:

    Dog IS-A Animal

But:

    Team ◇── Player

means:

    Team HAS Players

> [!important]
> **IS-A → Inheritance**
>
> **HAS-A + independent part → Aggregation candidate**

---

# 10. Aggregation vs Dependency

Dependency usually means:

    A temporarily uses B

Aggregation means:

    A is a whole containing/grouping B

Example:

    void print(Printer printer)

may represent:

    Dependency

But:

    class Department {
        List<Employee> employees;
    }

can represent:

    Aggregation

if Employee is a genuine independent part of Department.

---

# 11. The Most Important Test

> [!important]
> **Lifecycle Test**
>
> Ask:
>
>     "If the whole is destroyed,
>      can the part still exist?"
>
> If:
>
>     YES
>
> and it is a whole-part relationship:
>
>     Aggregation
>
> If:
>
>     NO
>
> and the lifecycle is strongly dependent:
>
>     Composition candidate

This is one of the fastest ways to solve interview questions.

---

# 12. Death Test

A very useful shortcut is the **Death Test**.

Imagine:

    Whole dies

Then ask:

    Does Part survive?

Example:

    Team dies
       ↓
    Player survives
       ↓
    Aggregation

Another example:

    Department closes
       ↓
    Employee survives
       ↓
    Aggregation

But:

    House destroyed
       ↓
    Room does not independently
    continue as part of that House
       ↓
    Composition candidate

---

# 13. Move Test

Another powerful test:

> **Can the part move from one whole to another?**

Example:

    Player
       ↓
    Team A

Player leaves:

    Player
       ↓
    Team B

The Player survives.

Therefore:

    Aggregation

Common examples:

    Player → Team

    Employee → Department

    Book → Library

    Song → Playlist

---

# 14. Independent Creation Test

Ask:

> Can the part exist before being added to the whole?

Example:

~~~java
Employee e = new Employee();

Department d = new Department();

d.addEmployee(e);
~~~

Here:

    Employee

was created independently.

Then:

    Department

received it.

This supports aggregation semantics.

However:

> [!warning]
> Object creation alone does not prove aggregation.
>
> The real definition depends on:
>
>     Whole-Part relationship
>     +
>     Independent lifecycle

---

# 15. Shared-Part Test

Another useful clue:

> Can the same part participate in multiple wholes?

Example:

    Song
     ↑
     |
    Playlist A

    Song
     ↑
     |
    Playlist B

The same Song can appear in multiple playlists.

Deleting one playlist does not destroy the Song.

Therefore:

    Aggregation

is a strong conceptual model.

---

# 16. Real-Time Example: Department and Employee

Consider:

    Department
         ◇
         |
      Employee

A Department contains Employees.

But an Employee can:

    leave the department
    move to another department
    continue working elsewhere

Therefore:

    Employee
    has independent lifecycle

So:

    Department ◇── Employee

represents aggregation.

---

# 17. Real-Time Example: Team and Player

Consider:

    Team
      ◇
      |
    Player

A player can move between teams.

Example:

    Player
       ↓
    Team A

Later:

    Player
       ↓
    Team B

The Player still exists.

Therefore:

    Aggregation

---

# 18. Real-Time Example: Company and Employee

Consider:

    Company
       ◇
       |
    Employee

An Employee can leave the company.

The employee does not automatically cease to exist.

Therefore, if the model treats Company as a whole grouping Employees:

    Aggregation

However, if the requirement only says:

    Company works with Employee

then simple Association may be more precise.

> [!important]
> The exact relationship depends on the intended domain semantics.

---

# 19. Real-Time Example: Library and Book

Consider:

    Library
       ◇
       |
      Book

A Book can:

    exist outside the library
    move to another library
    be purchased
    be stored privately

Therefore:

    Book
    has independent lifecycle

Hence:

    Library ◇── Book

can represent aggregation.

---

# 20. Real-Time Example: Playlist and Song

Consider:

    Playlist
       ◇
       |
      Song

A Song can exist independently.

The same Song can appear in:

    Workout Playlist
    Study Playlist
    Favorites Playlist

Deleting one playlist does not delete the Song.

Therefore:

    Aggregation

---

# 21. Real-Time Example: University and Professor

Consider:

    University
        ◇
        |
    Professor

A Professor can:

    change universities
    work independently
    retire
    join another organization

Therefore:

    Professor
    has independent lifecycle

So:

    University ◇── Professor

can be modeled as aggregation.

---

# 22. Real-Time Example: Project and Employee

Consider:

    Project
       ◇
       |
    Employee

An Employee can work on:

    Project A

and later:

    Project B

The employee survives after Project A ends.

Therefore:

    Aggregation

is a possible whole-part model.

---

# 23. Real-Time Example: School and Teacher

Consider:

    School
       ◇
       |
    Teacher

A Teacher can move from:

    School A

to:

    School B

The Teacher continues to exist.

Therefore:

    Aggregation

is a reasonable model when the school is modeled as a grouping of teachers.

---

# 24. Real-Time Example: Course and Student

Consider:

    Course
       ◇
       |
    Student

A Student can exist without a particular Course.

A Student may enroll in:

    Course A
    Course B
    Course C

Therefore:

    Student lifecycle
    is independent.

Aggregation may be used when the relationship is modeled as whole-part grouping.

However, in many designs this may simply be modeled as Association.

The requirements determine the correct abstraction.

---

# 25. Real-Time Example: Project and Developer

Consider:

    Project
       ◇
       |
    Developer

A developer can move between projects.

    Developer
        ↓
    Project A

Later:

    Developer
        ↓
    Project B

The developer still exists.

Therefore:

    Aggregation

can be a suitable whole-part interpretation.

---

# 26. Real-Time Example: Cart and Product

Consider:

    ShoppingCart
         ◇
         |
       Product

A Product exists independently from a cart.

A product can appear in many carts.

Therefore:

    Product lifecycle
    ≠
    Cart lifecycle

This supports an aggregation-style relationship.

However, real e-commerce systems often introduce:

    CartItem

A more realistic model may be:

    ShoppingCart
         ◆
         |
      CartItem
         |
         ◇
         |
      Product

Here:

    Cart
    ◆
    CartItem

can represent Composition because CartItem belongs strongly to the Cart.

While:

    CartItem
    ◇
    Product

can represent a weaker relationship because Product exists independently.

This is an important real-world modeling pattern.

---

# 27. Java Has No Aggregation Keyword

Java does not contain a keyword such as:

    aggregation

Aggregation is a:

    OOP concept
    UML concept
    design relationship

It is implemented using ordinary Java mechanisms.

Common mechanisms:

    object references
    fields
    collections
    constructors
    setters
    interfaces

---

# 28. Aggregation Through a Field

Example:

~~~java
class Department {

    private Employee employee;
}
~~~

The Department stores a reference to Employee.

If Employee is:

    independent

and Department is:

    whole

then this can represent aggregation.

---

# 29. Aggregation Through a Collection

This is extremely common.

~~~java
class Team {

    private List<Player> players;

    Team(List<Player> players) {
        this.players = players;
    }
}
~~~

Relationship:

    Team
      ◇
      |
      ├── Player
      ├── Player
      └── Player

This represents:

    One Team
       ↓
    Many Players

If Players have independent lifecycles:

    Aggregation

---

# 30. Aggregation Through Constructor

Example:

~~~java
class Department {

    private final List<Employee> employees;

    Department(List<Employee> employees) {
        this.employees = employees;
    }
}
~~~

Usage:

~~~java
Employee e1 = new Employee();
Employee e2 = new Employee();

List<Employee> employees =
    List.of(e1, e2);

Department d =
    new Department(employees);
~~~

The Employees already exist before Department receives them.

This supports independent lifecycle.

---

# 31. Aggregation Through Setter

Example:

~~~java
class Team {

    private List<Player> players;

    public void setPlayers(
        List<Player> players
    ) {
        this.players = players;
    }
}
~~~

The Team receives existing Player objects.

Again, this can support aggregation semantics.

---

# 32. Aggregation Through Add Method

Example:

~~~java
class Team {

    private final List<Player> players =
        new ArrayList<>();

    public void addPlayer(Player player) {
        players.add(player);
    }
}
~~~

Usage:

~~~java
Player p = new Player();

Team team = new Team();

team.addPlayer(p);
~~~

The Player exists independently.

The Team simply groups the Player.

---

# 33. Important Java Insight

> [!important]
> The presence of a field does **not** automatically prove aggregation.
>
> This:
>
> ~~~java
> class A {
>     B b;
> }
> ~~~
>
> only proves:
>
>     A has a reference to B
>
> To identify Aggregation, ask:
>
>     Is B a part of A?
>     Can B exist independently?
>     Is A acting as a whole?

---

# 34. Aggregation Is Semantic

This is an important advanced interview concept.

Given:

~~~java
class Company {

    List<Employee> employees;
}
~~~

The code alone does not tell us whether the relationship is:

    Association
    Aggregation
    Composition

We need the domain requirements.

If the requirement says:

    Company groups Employees.
    Employees can exist independently.

Then:

    Aggregation

If it only says:

    Company interacts with Employees.

Then:

    Association

Therefore:

> **Aggregation is determined by semantics, not simply syntax.**

---

# 35. Aggregation and `final`

Example:

~~~java
class Department {

    private final List<Employee> employees;
}
~~~

`final` means:

    employees reference
    cannot be reassigned

It does NOT automatically mean:

    Aggregation

It also does NOT mean:

    List is immutable

This is an important Java interview trap.

---

# 36. `final` Reference vs Immutable Object

Example:

~~~java
private final List<Employee> employees;
~~~

This means:

    employees = anotherList;

is not allowed after initialization.

But:

~~~java
employees.add(employee);
~~~

may still be allowed.

Therefore:

    final reference
    ≠
    immutable object

---

# 37. Defensive Copying

For better encapsulation:

~~~java
class Department {

    private final List<Employee> employees;

    Department(List<Employee> employees) {

        this.employees =
            new ArrayList<>(employees);
    }

    public List<Employee> getEmployees() {

        return List.copyOf(employees);
    }
}
~~~

Benefits:

    protects internal collection
    reduces accidental modification
    improves encapsulation
    makes object boundaries clearer

---

# 38. Aggregation and Encapsulation

Aggregation answers:

    "How are objects related?"

Encapsulation answers:

    "How is access to object state controlled?"

Example:

~~~java
class Department {

    private final List<Employee> employees;
}
~~~

Here:

    private
    → Encapsulation

    List<Employee>
    → Object relationship

    Whole-Part + independent lifecycle
    → Aggregation

These are different concepts working together.

---

# 39. Aggregation and Dependency Injection

Aggregation can be combined with Dependency Injection.

Example:

~~~java
class Team {

    private final List<Player> players;

    Team(List<Player> players) {
        this.players = players;
    }
}
~~~

The Team receives Players from outside.

Benefits:

    explicit dependencies
    easier testing
    less object creation responsibility
    better separation of concerns
    flexible design

---

# 40. Aggregation With Interfaces

Example:

~~~java
interface Employee {
    void work();
}

class Department {

    private final List<Employee> employees;

    Department(List<Employee> employees) {
        this.employees = employees;
    }
}
~~~

Possible implementations:

    Developer
    Tester
    Designer
    Manager

Department depends on the abstraction:

    Employee

rather than one concrete class.

This supports flexible design.

---

# 41. Aggregation and Polymorphism

Example:

~~~java
interface Player {
    void play();
}

class FootballPlayer
    implements Player {

    public void play() {
        System.out.println("Football");
    }
}

class Team {

    private List<Player> players;
}
~~~

Now:

    Team
      ◇
      |
    Player
    /    \
Football  Cricket

The Team can work with different implementations.

This combines:

    Aggregation
    +
    Interface
    +
    Polymorphism

---

# 42. Aggregation and Loose Coupling

Good aggregation design can support loose coupling.

Instead of:

~~~java
class ReportService {

    private PDFExporter exporter =
        new PDFExporter();
}
~~~

Prefer:

~~~java
interface Exporter {
    void export();
}

class ReportService {

    private final Exporter exporter;

    ReportService(Exporter exporter) {
        this.exporter = exporter;
    }
}
~~~

Now:

    ReportService
         ↓
      Exporter
       ↑    ↑
      PDF  Excel

This is easier to extend and test.

---

# 43. Aggregation and SOLID

Aggregation itself is not a SOLID principle.

However, good aggregation design can support:

    Single Responsibility Principle
    Dependency Inversion Principle
    Open/Closed Principle

Example:

    NotificationManager
          ◇
          |
    NotificationChannel
       /      |      \
    Email    SMS    Push

The manager can work with multiple channel implementations.

---

# 44. Aggregation and Object Lifecycle

This is the most important technical distinction.

Aggregation:

~~~text
Whole
  |
  ◇
  |
Part

Whole destroyed
       ↓
Part can survive
~~~

Composition:

~~~text
Whole
  |
  ◆
  |
Part

Whole destroyed
       ↓
Part lifecycle is strongly tied
to Whole
~~~

---

# 45. Aggregation and Object Creation

A common shortcut is:

    Aggregation
    → Part created outside

    Composition
    → Part created inside

This can help with intuition.

But do not use it as the formal definition.

The correct principle is:

    Aggregation
    → Independent lifecycle

    Composition
    → Strong lifecycle dependency

Object creation location is only a clue.

---

# 46. Aggregation and Garbage Collection

Do not confuse UML aggregation with Java memory management.

Aggregation:

    design relationship

Garbage Collection:

    memory management

Java garbage collection is based on:

    object reachability

not:

    UML diamond type

Therefore:

> [!warning]
> Aggregation does not directly control Java garbage collection.

---

# 47. Aggregation and `null`

Suppose:

~~~java
department.setEmployee(null);
~~~

The relationship from that Department may be removed.

But the Employee object can still exist if another reference points to it.

This is consistent with the idea of:

    independent lifecycle

---

# 48. Aggregation and Multiple References

Example:

~~~java
Employee e = new Employee();

department1.addEmployee(e);
department2.addEmployee(e);
~~~

The same Employee can be referenced by multiple objects.

The Employee still exists independently.

This demonstrates an important aggregation-style idea:

    Part
      ↓
    independent
      ↓
    can participate in other relationships

---

# 49. Aggregation and Shared Objects

Example:

    Song
     ↑
     |
Playlist A

and:

    Song
     ↑
     |
Playlist B

The same Song object can conceptually belong to multiple playlists.

If Playlist A is deleted:

    Song survives.

If Playlist B is deleted:

    Song survives.

This is a strong aggregation example.

---

# 50. Aggregation and Exclusive Membership

Important:

> Aggregation does not require that a part belong to multiple wholes.

Example:

    Employee
       ↓
    Department

An employee may belong to only one department at a time.

Still:

    Employee
    can exist after leaving department.

Therefore:

    Aggregation

can still be valid.

The key condition is:

    independent lifecycle

not:

    multiple ownership

---

# 51. Aggregation and Multiplicity

Aggregation and multiplicity answer different questions.

Aggregation asks:

    What type of relationship?

Multiplicity asks:

    How many objects?

Example:

    Department ◇──── Employee

can have:

    1 : N

Meaning:

    One Department
    → Many Employees

Therefore:

    Aggregation
    = relationship type

    1:N
    = multiplicity

---

# 52. Common Multiplicities

| Notation | Meaning |
|---|---|
| `1` | Exactly one |
| `0..1` | Zero or one |
| `*` | Many |
| `1..*` | One or more |
| `0..*` | Zero or more |

Examples:

    Department 1 ◇──── 0..* Employee

means:

    One Department
    can have zero or many Employees.

---

# 53. One-to-One Aggregation

Possible example:

    Organization
         ◇
         |
    Headquarters

The exact model depends on domain requirements.

Multiplicity:

    1 : 1

Remember:

    1:1
    → quantity

not:

    relationship strength

---

# 54. One-to-Many Aggregation

Very common pattern:

    Department
       ◇
       |
       ├── Employee
       ├── Employee
       └── Employee

Multiplicity:

    1 : N

Examples:

    Department → Employees

    Team → Players

    Library → Books

    Playlist → Songs

---

# 55. Many-to-Many Aggregation

Possible pattern:

    Project
       ↔
    Employee

One Employee:

    → many Projects

One Project:

    → many Employees

If whole-part semantics are appropriate:

    Aggregation

But in many real systems this is simply modeled as Association with an intermediate entity.

---

# 56. Association Class

Sometimes the relationship itself has important information.

Example:

    Student
       ↔
    Course

But the relationship has:

    enrollmentDate
    grade
    status

Create:

    Enrollment

Now:

    Student
       |
       |
    Enrollment
       |
       |
    Course

The relationship becomes an object.

This is called an **Association Class** in UML.

---

# 57. Real-Time Example: Employee and Project

Suppose:

    Employee
       ↔
    Project

But we need:

    role
    startDate
    allocationPercentage

Create:

    Assignment

Then:

    Employee
       |
    Assignment
       |
    Project

This is much more expressive than storing only direct references.

---

# 58. Aggregation and Database Thinking

Aggregation is useful for understanding object relationships that later appear in databases.

Examples:

    Department
       ↓
    Employee

can correspond conceptually to:

    Department 1 : N Employee

Another:

    Student
       ↔
    Course

can correspond to:

    Student N : N Course

with a join table.

OOP relationship thinking helps with:

    DBMS
    SQL
    ORM
    JPA
    Hibernate
    System Design

---

# 59. Aggregation in JPA/Hibernate

In Java enterprise applications, object relationships may be represented using:

    @OneToOne
    @OneToMany
    @ManyToOne
    @ManyToMany

Example:

~~~java
class Employee {

    @ManyToOne
    private Department department;
}
~~~

This describes a persistence relationship.

However:

> [!warning]
> JPA annotation alone does not automatically determine UML aggregation semantics.

Database mapping and UML lifecycle semantics are related but not identical.

---

# 60. Aggregation Decision Tree

Use this during interviews:

~~~text
Are A and B related?
        |
       YES
        |
        v
Is B a part of A?
     /       \
   NO         YES
   |           |
   v           v
Association   Can B exist
              independently?
                 /    \
               YES     NO
                |       |
                v       v
          Aggregation  Composition
~~~

Memory:

    Related only
    → Association

    Whole-Part + Independent
    → Aggregation

    Whole-Part + Dependent
    → Composition

    IS-A
    → Inheritance

---

# 61. Fast Recognition Algorithm

When you see an OOP relationship question:

### Step 1

Identify the two objects.

Example:

    Department
    Employee

### Step 2

Ask:

    Is one a type of another?

If yes:

    Inheritance

### Step 3

If not, ask:

    Are they simply related?

If yes:

    Association

### Step 4

Ask:

    Is it a whole-part relationship?

If no:

    Association

### Step 5

Ask:

    Can the part exist independently?

If yes:

    Aggregation

If no:

    Composition candidate

---

# 62. Pattern Recognition

> [!important]
> **Pattern 1 — Weak Whole-Part**
>
> If the question says:
>
>     weak whole-part relationship
>
> think:
>
>     Aggregation

> [!important]
> **Pattern 2 — Independent Part**
>
> If:
>
>     Part survives Whole
>
> think:
>
>     Aggregation

> [!important]
> **Pattern 3 — Part Can Move**
>
> If:
>
>     Part moves from A to B
>
> think:
>
>     Aggregation

> [!important]
> **Pattern 4 — Hollow Diamond**
>
> If you see:
>
>     ◇
>
> think:
>
>     Aggregation

> [!important]
> **Pattern 5 — Filled Diamond**
>
> If you see:
>
>     ◆
>
> think:
>
>     Composition

> [!important]
> **Pattern 6 — IS-A**
>
> If you see:
>
>     IS-A
>
> think:
>
>     Inheritance

> [!important]
> **Pattern 7 — General Relationship**
>
> If the objects are simply:
>
>     related
>     interact
>     communicate
>     know
>
> think:
>
>     Association

---

# 63. Shortcuts

> [!tip]
> **Shortcut 1: Hollow Diamond**
>
>     ◇
>     → Aggregation

> [!tip]
> **Shortcut 2: Death Test**
>
> Whole dies:
>
>     Part survives
>
> → Aggregation

> [!tip]
> **Shortcut 3: Move Test**
>
> Part can move:
>
>     Whole A
>       ↓
>     Part
>       ↓
>     Whole B
>
> → Aggregation

> [!tip]
> **Shortcut 4: Independent Lifecycle**
>
> If:
>
>     Part has its own lifecycle
>
> → Aggregation candidate

> [!tip]
> **Shortcut 5: Weak Ownership**
>
> If:
>
>     Whole groups Part
>     but does not strongly own lifecycle
>
> → Aggregation

> [!tip]
> **Shortcut 6: Strong Ownership**
>
> If:
>
>     Whole strongly controls Part lifecycle
>
> → Composition

> [!tip]
> **Shortcut 7: IS-A**
>
>     IS-A
>     → Inheritance

> [!tip]
> **Shortcut 8: General Relationship**
>
>     Related
>     → Association

> [!tip]
> **Shortcut 9: Quantity**
>
>     1:N
>     → One-to-Many
>
> Do not confuse multiplicity with aggregation.

> [!tip]
> **Shortcut 10: Java Field Trap**
>
> Seeing:
>
>     B b;
>
> does not automatically mean:
>
>     Aggregation
>
> Ask:
>
>     Is B a genuine part of A?
>     Can B exist independently?

---

# 64. Common Exam Patterns

> [!important] Must Master

1. Definition of Aggregation
2. Aggregation as specialized Association
3. Weak whole-part relationship
4. Independent lifecycle
5. Weak ownership
6. Hollow diamond
7. Aggregation vs Association
8. Aggregation vs Composition
9. Aggregation vs Inheritance
10. Aggregation vs Dependency
11. Aggregation in Java
12. Aggregation through fields
13. Aggregation through collections
14. Aggregation through constructors
15. Aggregation through setters
16. Aggregation through interfaces
17. Aggregation and polymorphism
18. Aggregation and dependency injection
19. Aggregation and encapsulation
20. Aggregation and `final`
21. Aggregation and garbage collection
22. Aggregation and multiplicity
23. One-to-one aggregation
24. One-to-many aggregation
25. Many-to-many relationship
26. UML aggregation
27. UML navigability
28. UML multiplicity
29. Death Test
30. Move Test
31. Independent Creation Test
32. Shared-Part Test
33. Lifecycle questions
34. Real-world modeling
35. Association Class
36. Aggregation with interfaces
37. Aggregation and loose coupling
38. Aggregation and SOLID
39. Aggregation and ORM
40. Scenario-based interview questions

---

# 65. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Every HAS-A Is Aggregation

Wrong:

    Car has Driver
    → Aggregation

Not necessarily.

HAS-A is broad.

It can mean:

    Association
    Aggregation
    Composition

depending on semantics.

---

### Mistake 2 — Aggregation Means Shared Objects

Not necessarily.

Shared objects are only one common example.

The actual definition is:

    Whole-Part
    +
    Independent Lifecycle

---

### Mistake 3 — Aggregation and Composition Are Same

Wrong:

    Both are HAS-A
    → same relationship

Correct:

    Aggregation
    → weak ownership

    Composition
    → strong ownership

---

### Mistake 4 — Java Has an Aggregation Keyword

Wrong.

Java has no:

    aggregation

keyword.

It is a design relationship.

---

### Mistake 5 — Created Outside Means Automatically Aggregation

Wrong.

Creation location is only a clue.

The real test is:

    independent lifecycle

---

### Mistake 6 — Aggregation Controls Garbage Collection

Wrong.

Java GC uses:

    reachability

not:

    UML relationship type

---

### Mistake 7 — 1:N Means Aggregation

Wrong.

`1:N` describes:

    multiplicity

Aggregation describes:

    whole-part relationship

---

### Mistake 8 — Bidirectional Means Aggregation

Wrong.

Bidirectional means:

    both sides can navigate/know each other

It does not determine:

    Association
    Aggregation
    Composition

---

### Mistake 9 — Arrow Means Ownership

Wrong.

In UML:

    Arrow
    → navigability

    Diamond
    → whole-part semantics

---

### Mistake 10 — `final` Means Aggregation

Wrong.

`final` only restricts reassignment of a reference.

It does not define the UML relationship.

---

### Mistake 11 — Aggregation Always Means One-to-Many

Wrong.

Aggregation can have different multiplicities.

Examples:

    1:1
    1:N
    N:N

---

### Mistake 12 — Ignore Domain Requirements

Two systems can model the same real-world objects differently.

Always ask:

    What does the requirement say?
    Who owns the lifecycle?
    Can the part survive?
    Is this actually a whole-part relationship?

---

# 66. Advanced Interview Questions

## Q1. What is Aggregation?

Strong answer:

> Aggregation is a specialized form of association representing a weak whole-part relationship. The whole contains or groups the parts, but the parts can exist independently of the whole.

---

## Q2. What is the UML symbol for Aggregation?

Answer:

    Hollow diamond

Symbol:

    ◇

The diamond is placed near the whole.

---

## Q3. What is the difference between Aggregation and Composition?

Answer:

> Aggregation represents weak ownership where the part has an independent lifecycle. Composition represents strong ownership where the part's lifecycle is strongly tied to the whole.

---

## Q4. Is Aggregation a Java keyword?

Answer:

> No. Aggregation is an OOP/UML design concept implemented using normal Java constructs such as references, fields, collections, constructors, and methods.

---

## Q5. Is Aggregation a type of Association?

Answer:

> Yes. Aggregation can be viewed as a specialized whole-part form of association.

---

## Q6. What is the key property of Aggregation?

Answer:

    Independent lifecycle of the part.

---

## Q7. What happens if the whole is destroyed?

In aggregation:

    Part can survive.

---

## Q8. Can the part move to another whole?

Often yes.

Example:

    Player
       ↓
    Team A

then:

    Player
       ↓
    Team B

---

## Q9. Does Aggregation require multiple ownership?

No.

A part can still have only one whole at a time and remain independently alive.

---

## Q10. Can Aggregation be one-to-many?

Yes.

Example:

    Department
       ◇
       |
    Employees

---

## Q11. Can Aggregation be many-to-many?

Yes, depending on the domain model.

---

## Q12. Can Java code alone prove Aggregation?

No.

The semantic meaning of the relationship must be considered.

---

## Q13. Does Aggregation control garbage collection?

No.

Garbage collection is based on reachability.

---

## Q14. Does `final` imply Aggregation?

No.

`final` controls reassignment of a reference.

---

## Q15. Is "created outside" the definition of Aggregation?

No.

The stronger definition is:

    Weak whole-part
    +
    Independent lifecycle

---

## Q16. What is the Death Test?

Ask:

> If the whole disappears, can the part still exist meaningfully?

If yes:

    Aggregation candidate

---

## Q17. What is the Move Test?

Ask:

> Can the part move from one whole to another?

If yes:

    Aggregation is often a strong candidate.

---

## Q18. What is the difference between Aggregation and Association?

Association:

    General relationship

Aggregation:

    Whole-part relationship
    +
    independent part

---

## Q19. What is the difference between Aggregation and Inheritance?

Inheritance:

    IS-A

Aggregation:

    HAS-A
    +
    independent part

---

## Q20. What is the difference between Aggregation and Dependency?

Dependency:

    temporary usage

Aggregation:

    structural whole-part relationship

---

# 67. Scenario-Based Questions

## Example 1 — Department and Employee

### Question

A department contains employees. Employees can be transferred to other departments and continue to exist.

### Recognition

    Whole:
    Department

    Part:
    Employee

    Independent lifecycle:
    YES

### Answer

    Aggregation

    Department ◇── Employee

---

## Example 2 — Team and Player

### Question

A player can leave Team A and join Team B.

### Recognition

    Player survives
    Team changes

### Answer

    Aggregation

---

## Example 3 — Playlist and Song

### Question

A song can exist independently and can belong to multiple playlists.

### Recognition

    Independent Song
    +
    grouped by Playlist

### Answer

    Aggregation

---

## Example 4 — House and Room

### Question

A room is modeled as a part whose lifecycle strongly depends on the house.

### Recognition

    Whole-Part
    +
    Strong Lifecycle

### Answer

    Composition

---

## Example 5 — Doctor and Patient

### Question

A doctor treats patients. Both exist independently.

### Recognition

    Related
    +
    Not whole-part

### Answer

    Association

---

## Example 6 — Student and Course

### Question

Students can enroll in multiple courses and courses can have many students. Both exist independently.

### Recognition

    N:N
    +
    Independent Lifecycle

### Answer

    Many-to-Many Association

---

## Example 7 — Order and OrderItem

### Question

An OrderItem has no meaningful independent lifecycle outside its Order.

### Recognition

    Whole-Part
    +
    Strong Lifecycle

### Answer

    Composition

    Order ◆── OrderItem

---

## Example 8 — Employee and Project

### Question

Employees can work on different projects and continue existing after projects end.

### Recognition

    Employee survives
    Project changes

### Answer

    Aggregation candidate

---

# 68. High-Level Design Insight

A strong OOP designer does not start by memorizing:

    Association
    Aggregation
    Composition

Instead, think:

    Identify objects
          ↓
    Identify responsibilities
          ↓
    Identify relationships
          ↓
    Ask ownership questions
          ↓
    Ask lifecycle questions
          ↓
    Determine multiplicity
          ↓
    Determine navigability
          ↓
    Choose relationship type

This produces much better designs.

---

# 69. Relationship Decision Framework

Use this framework in interviews:

~~~text
                OOP Relationship
                       |
                       v
                Is it IS-A?
                 /       \
               YES        NO
                |          |
          Inheritance      v
                     Are A and B related?
                           |
                          YES
                           |
                           v
                    Is it whole-part?
                      /          \
                    NO            YES
                    |              |
                    v              v
              Association      Can Part
                               exist independently?
                                /       \
                              YES       NO
                               |         |
                               v         v
                         Aggregation  Composition
~~~

---

# 70. Aggregation Master Comparison

| Concept | Meaning | Lifecycle | UML |
|---|---|---|---|
| Association | General relationship | Independent | Line |
| Aggregation | Weak whole-part | Independent | ◇ |
| Composition | Strong whole-part | Dependent | ◆ |
| Inheritance | IS-A | Type hierarchy | Generalization arrow |
| Dependency | Temporary usage | Independent | Dashed arrow |

---

# 71. Real-Time Architecture Example

Consider a notification system.

    NotificationManager
             ◇
             |
             |
      NotificationChannel
          /       |       \
         /        |        \
      Email      SMS       Push

The manager works with multiple channels.

Possible implementations:

    EmailChannel
    SMSChannel
    PushChannel

The channels can exist independently.

This design supports:

    Aggregation
    Polymorphism
    Loose Coupling
    Dependency Injection
    Open/Closed Principle

---

# 72. Real-Time E-Commerce Example

Consider:

    ShoppingCart
         ◆
         |
      CartItem
         |
         ◇
         |
      Product

Reasoning:

    CartItem
    belongs strongly to Cart

Therefore:

    Composition

But:

    Product
    exists independently

Therefore:

    Aggregation/Association

This demonstrates an important design principle:

> **A single system can contain multiple relationship types simultaneously.**

---

# 73. Real-Time Project Management Example

Consider:

    Project
       ◇
       |
    Developer
       |
       ◇
    Project

A Developer can participate in multiple Projects.

Developer lifecycle:

    independent

Therefore:

    Aggregation-style relationship

If the relationship itself has:

    role
    startDate
    allocation

introduce:

    Assignment

Then:

    Developer
       |
    Assignment
       |
    Project

This is a richer domain model.

---

# 74. Real-Time Music Application

Consider:

    Playlist
       ◇
       |
      Song

A Song may belong to:

    Favorites
    Workout
    Coding
    Relaxation

Deleting a Playlist:

    does not delete Song

Therefore:

    Aggregation

This is an excellent real-world example to remember.

---

# 75. Real-Time Education Application

Consider:

    Course
       ◇
       |
    Student

A Student can:

    enroll
    drop
    change course
    take multiple courses

Student lifecycle:

    independent

Therefore:

    Aggregation may be appropriate when the model treats Course as a whole grouping Students.

But if the system simply models:

    Student enrolls in Course

then:

    Association

may be more precise.

Always inspect the semantics.

---

# 76. Real-Time Banking Example

Consider:

    Bank
       ◇
       |
    Customer

A Customer can:

    change banks
    have multiple relationships
    exist independently

Therefore:

    Aggregation may be used if Bank is explicitly modeled as a whole grouping Customers.

If the model only says:

    Bank serves Customer

then:

    Association

may be sufficient.

This demonstrates why terminology alone is not enough.

---

# 77. Real-Time Social Media Example

Consider:

    Playlist
       ◇
       |
      Song

or:

    User
       ↔
    User

For:

    User follows User

the relationship is usually Association.

For:

    Playlist contains Songs

aggregation is more appropriate when the playlist is modeled as a whole grouping independent songs.

---

# 78. Aggregation and Pattern Recognition in Interviews

When the interviewer gives a scenario, immediately extract:

    WHOLE
    PART
    LIFECYCLE
    OWNERSHIP
    MULTIPLICITY

Example:

    "A team contains players,
     and players can move to
     another team."

Extract:

    Whole:
    Team

    Part:
    Player

    Lifecycle:
    Independent

    Ownership:
    Weak

    Relationship:
    Aggregation

    Multiplicity:
    1:N

---

# 79. Five-Second Aggregation Test

> [!important]
> During a fast interview, ask only these three questions:
>
>     1. Is it Whole-Part?
>     2. Can the Part survive independently?
>     3. Is ownership weak?
>
> If:
>
>     YES
>     YES
>     YES
>
> think:
>
>     Aggregation

---

# 80. Five-Second Relationship Test

> [!tip]
> Memorize:
>
>     IS-A
>     → Inheritance
>
>     Related
>     → Association
>
>     Whole-Part + Independent
>     → Aggregation
>
>     Whole-Part + Dependent
>     → Composition
>
>     Temporary Use
>     → Dependency

---

# 81. Formula Sheet

## Aggregation

~~~text
Aggregation
= Association
+ Weak Whole-Part Relationship

Core:

Whole ◇── Part

◇
= Hollow Diamond
= Aggregation

◆
= Filled Diamond
= Composition


Main condition:

Whole-Part
+
Independent Part Lifecycle
=
Aggregation


Death Test:

Whole destroyed
+
Part survives
=
Aggregation candidate


Move Test:

Part moves from Whole A
to Whole B
=
Aggregation candidate


Association:

A ─── B
=
General relationship


Aggregation:

A ◇── B
=
Weak whole-part


Composition:

A ◆── B
=
Strong whole-part


Inheritance:

A IS-A B
=
Inheritance


Dependency:

A temporarily uses B
=
Dependency candidate


Multiplicity:

1:1
=
One-to-One

1:N
=
One-to-Many

N:1
=
Many-to-One

N:N
=
Many-to-Many


UML multiplicity:

1
=
Exactly one

0..1
=
Zero or one

*
=
Many

1..*
=
One or more

0..*
=
Zero or more


Common examples:

Department ◇── Employee

Team ◇── Player

Library ◇── Book

Playlist ◇── Song

University ◇── Professor

Project ◇── Employee


Java:

class Department {

    private List<Employee> employees;
}


Important:

Java has no aggregation keyword.

A Java reference alone does not prove aggregation.

Domain semantics determine the relationship.


Final reference:

private final List<Employee> employees;

means:

Reference cannot be reassigned.

It does NOT automatically mean:

Aggregation

It does NOT automatically mean:

Immutable collection.


Core memory:

◇ = Aggregation
◆ = Composition

Aggregation = WEAK OWNERSHIP
Composition = STRONG OWNERSHIP


Decision:

Related?
→ Association

Whole-Part?
→ Continue

Part Independent?
→ Aggregation

Part Dependent?
→ Composition

IS-A?
→ Inheritance

Temporary Use?
→ Dependency
~~~

---

# 82. Quick Revision

> [!summary] One-Minute Revision

### Definition

Aggregation is a **weak whole-part relationship** where the part can exist independently of the whole.

### Core Symbol

    ◇

Hollow diamond:

    Aggregation

### Core Pattern

    Whole
       ◇
       |
      Part

### Most Important Property

    Part lifecycle
    is independent.

### Death Test

    Whole dies
       ↓
    Part survives
       ↓
    Aggregation

### Move Test

    Part moves from
    Whole A → Whole B
       ↓
    Aggregation candidate

### Examples

    Department ◇── Employee

    Team ◇── Player

    Library ◇── Book

    Playlist ◇── Song

    University ◇── Professor

### Association

    General relationship

### Aggregation

    Weak whole-part

### Composition

    Strong whole-part

### Inheritance

    IS-A

### Dependency

    Temporary usage

### Java

Java has no:

    aggregation

keyword.

It is represented through:

    references
    fields
    collections
    constructors
    setters
    interfaces

### Most Important Warning

Do not decide aggregation merely because you see:

    A has B

Instead ask:

    Is B actually a part of A?
    Can B exist independently?
    Can B survive if A disappears?
    Can B move to another whole?

### Golden Memory Trick

**Aggregation = "Whole has Parts, but Parts can live on their own."**

### One-Line Recognition

**If you see a weak whole-part relationship where the part has an independent lifecycle, think Aggregation.**