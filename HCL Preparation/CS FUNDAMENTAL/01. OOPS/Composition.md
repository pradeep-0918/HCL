---
type: concept
subject: aptitude
topic: "Composition"
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
  - composition
  - association
  - aggregation
  - has-a
  - uml
  - object-oriented-programming
  - java-interview
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Association]]"
  - "[[Aggregation]]"
  - "[[Coupling and Cohesion]]"
  - "[[SOLID Principles]]"
  - "[[Inheritance]]"
---

# Composition

> [!summary]
> **Composition is a strong whole-part relationship where the whole strongly owns the parts and the lifecycle of the part is dependent on the whole.**
>
> Core idea:
>
>     Composition
>     → HAS-A
>     → Strong Ownership
>     → Strong Whole-Part Relationship
>     → Dependent Lifecycle
>
> Classic example:
>
>     House ◆──── Room
>
> A Room is modeled as a component of a particular House.
>
> The most important question is:
>
>     "Does the part have a lifecycle strongly controlled by the whole?"
>
> If YES:
>
>     Composition candidate

---

# 1. Core Concept

Composition is one of the most important object relationships in OOP.

It represents a **strong whole-part relationship**.

The structure is:

    Whole
       ◆
       |
      Part

The whole strongly owns the part.

The part is generally considered to belong exclusively to that whole.

Example:

    House
      ◆
      |
     Room

The House contains Rooms.

In the domain model, the Room is strongly associated with the lifecycle of that House.

Therefore:

    House ◆── Room

represents Composition.

---

# 2. Basic Meaning

Composition means:

    HAS-A
    +
    Strong Ownership
    +
    Dependent Lifecycle

Example:

    Car ◆── Engine

If the Engine is modeled as an integral component belonging to a particular Car, the Car strongly owns that Engine.

Another example:

    Order ◆── OrderItem

An OrderItem exists as part of a particular Order.

If the Order is removed, its OrderItems are normally removed as well in that domain model.

Therefore:

    Order ◆── OrderItem

is a strong composition relationship.

---

# 3. Main Formula

There is no mathematical formula for Composition.

Use this conceptual formula:

$$
\boxed{
Composition =
Association +
Strong\ Whole\text{-}Part\ Relationship
}
$$

The most important condition is:

$$
\boxed{
Part\ Lifecycle\ is\ Dependent\ on\ Whole
}
$$

Another useful mental model:

$$
\boxed{
Whole\ OWNS\ Part
+
Part\ depends\ on\ Whole
=
Composition
}
$$

---

# 4. Core Characteristics

Composition has five major characteristics.

### 1. Whole-Part Relationship

There is a clear:

    Whole
       ↓
    Part

relationship.

### 2. Strong Ownership

The whole strongly owns the part.

### 3. Dependent Lifecycle

The part's lifecycle is strongly tied to the whole.

### 4. Strong Encapsulation

The whole often controls how its parts are created, accessed, and removed.

### 5. Exclusive Ownership

A composition normally represents a part belonging to one particular whole.

---

# 5. UML Symbol

Composition is represented using a **filled diamond**.

    Whole ◆──────── Part

Example:

    House ◆──────── Room

The filled diamond is placed near the:

    WHOLE

Remember:

    ◆ = Composition

    ◇ = Aggregation

This is one of the most important UML interview questions.

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
>
> Memory:
>
>     ◇ → Weak
>     ◆ → Strong

---

# 7. Composition vs Association

Association is a general relationship.

    A ───── B

Composition is a strong whole-part relationship.

    A ◆──── B

| Feature | Association | Composition |
|---|---|---|
| General relationship | Yes | Yes |
| Whole-part | Not required | Yes |
| Strong ownership | No requirement | Yes |
| Lifecycle dependency | No strong dependency | Strong dependency |
| UML diamond | No | Filled diamond |
| Example | Doctor-Patient | House-Room |

Memory:

    Association
    → related

    Composition
    → strongly owns part

---

# 8. Composition vs Aggregation

This is the most important comparison.

| Feature | Aggregation | Composition |
|---|---|---|
| Whole-part | Yes | Yes |
| Ownership | Weak | Strong |
| Part lifecycle | Independent | Dependent |
| Part survives whole? | Yes | Generally no |
| UML symbol | ◇ | ◆ |
| Typical example | Team-Player | House-Room |
| Main idea | Grouping | Strong ownership |
| Sharing | Often possible | Generally not |
| Whole controls lifecycle | Weak | Strong |

Memory:

    Aggregation
    → Part can live independently

    Composition
    → Part belongs strongly to Whole

---

# 9. Composition vs Inheritance

Inheritance:

    IS-A

Composition:

    HAS-A

Example:

    Dog
      ↓
    Animal

means:

    Dog IS-A Animal

But:

    Car
      ◆
      |
    Engine

means:

    Car HAS-A Engine

> [!important]
> **IS-A → Inheritance**
>
> **HAS-A + Strong Ownership → Composition**

---

# 10. Composition vs Dependency

Dependency usually means:

    A temporarily uses B

Composition means:

    A strongly owns B

Example:

    class ReportService {

        void print(Printer printer) {
            printer.print();
        }
    }

This can represent:

    Dependency

But:

    class Order {

        List<OrderItem> items;
    }

can represent:

    Composition

if OrderItems belong strongly to the Order lifecycle.

---

# 11. The Most Important Test

> [!important]
> **Lifecycle Test**
>
> Ask:
>
>     "If the whole is destroyed,
>      should the part still exist
>      as an independent part of that model?"
>
> If:
>
>     NO
>
> and the relationship is whole-part:
>
>     Composition candidate
>
> If:
>
>     YES
>
> and the relationship is weak whole-part:
>
>     Aggregation candidate

This is the most important conceptual test.

---

# 12. Death Test

Imagine:

    Whole dies

Then ask:

    What happens to Part?

Composition:

    Whole dies
       ↓
    Part's lifecycle ends
    with Whole

Aggregation:

    Whole dies
       ↓
    Part survives

Therefore:

    ◆
    → Composition

    ◇
    → Aggregation

---

# 13. Ownership Test

Ask:

> Who controls the part?

If:

    Whole strongly controls Part

then:

    Composition

Example:

    Order
      ◆
      |
    OrderItem

The Order manages the lifecycle of its OrderItems.

---

# 14. Creation Test

Ask:

> Who is responsible for creating the part?

If the whole creates and manages its parts internally, that is strong evidence for composition.

Example:

    class House {

        private Room room;

        House() {
            room = new Room();
        }
    }

The House creates the Room.

This supports composition semantics.

However:

> [!warning]
> Creation inside the whole is a useful clue, not the complete definition.
>
> The real concept is:
>
>     Strong Ownership
>     +
>     Dependent Lifecycle

---

# 15. Encapsulation Test

Composition often means the whole controls access to its parts.

Example:

    Order
      ◆
      |
    OrderItem

The Order may provide methods such as:

    addItem()
    removeItem()
    calculateTotal()

The caller does not necessarily manage OrderItems independently.

This supports strong encapsulation.

---

# 16. Exclusive Ownership Test

Ask:

> Can the same part independently belong to multiple wholes?

If the domain strongly says:

    one part
    → one whole

then composition becomes a strong candidate.

Example:

    OrderItem
       ↓
    Order

An OrderItem belongs to one particular Order.

This supports composition.

---

# 17. Real-Time Example: House and Room

Classic example:

    House
      ◆
      |
     Room

A House consists of Rooms.

The Room is modeled as a component of the House.

If the House is destroyed in the domain model:

    House
       ↓
    destroyed
       ↓
    Rooms
       ↓
    lifecycle ends with House

Therefore:

    House ◆── Room

is composition.

---

# 18. Real-Time Example: Order and OrderItem

This is one of the best real-world examples.

    Order
      ◆
      |
    OrderItem
      |
      ├── Product
      ├── quantity
      └── price

An OrderItem belongs to a particular Order.

If the Order is deleted, its OrderItems are normally deleted too.

Therefore:

    Order ◆── OrderItem

represents composition.

---

# 19. Real-Time Example: Order and OrderItem vs Product

This example is extremely important.

Consider:

    Order
      ◆
      |
    OrderItem
      |
      ◇
      |
    Product

Reasoning:

    Order
      ◆
    OrderItem

because OrderItem belongs to Order.

But:

    Product

exists independently.

The Product can appear in:

    Order A
    Order B
    Order C

Therefore:

    Order ◆── OrderItem

and:

    OrderItem ◇── Product

or Association, depending on the exact domain semantics.

This demonstrates that one system can contain multiple relationship types.

---

# 20. Real-Time Example: Car and Engine

Consider:

    Car
      ◆
      |
    Engine

If the Engine is modeled as a strongly owned component of a particular Car:

    Car ◆── Engine

The Car controls the Engine lifecycle.

This can represent composition.

However, in a real automobile system, engines may be replaced and exist as separately tracked entities.

Therefore:

> [!important]
> Real-world examples depend on the exact domain model.
>
> Do not blindly memorize "Car-Engine = Composition."
>
> Explain the lifecycle and ownership assumptions.

---

# 21. Real-Time Example: Computer and Motherboard

Possible model:

    Computer
       ◆
       |
    Motherboard

If the motherboard is treated as an integral component of the computer:

    Composition

The computer strongly owns its motherboard within that model.

But a replacement motherboard can exist independently in a repair inventory system.

Therefore, again:

    domain semantics
    →
    relationship type

---

# 22. Real-Time Example: Human and Heart

In a simplified conceptual model:

    Human
      ◆
      |
    Heart

The Heart is modeled as an integral component of the Human.

The lifecycle is strongly tied to the Human.

Therefore:

    Composition

This is a conceptual modeling example.

---

# 23. Real-Time Example: Document and Paragraph

Consider:

    Document
       ◆
       |
    Paragraph

A Paragraph is generally modeled as a part of a particular Document.

If the Document is deleted:

    Paragraphs
       ↓
    no longer exist
    as parts of that document

Therefore:

    Document ◆── Paragraph

is a strong composition example.

---

# 24. Real-Time Example: Document and Section

Consider:

    Document
       ◆
       |
    Section

Sections belong to a particular Document.

A Section is not normally treated as an independent document entity.

Therefore:

    Composition

---

# 25. Real-Time Example: University and Department

This example requires careful thinking.

Possible model:

    University
       ◆
       |
    Department

If Departments are considered integral parts of a particular University and their lifecycle is controlled by that University:

    Composition

But if Departments are modeled as independent organizational entities:

    Aggregation

Therefore:

> The correct relationship depends on the domain model.

This is a high-level interview insight.

---

# 26. Real-Time Example: Company and Department

Possible model:

    Company
       ◆
       |
    Department

If a Department exists only as part of that Company:

    Composition

If Departments are treated as independently managed entities:

    Aggregation

Again:

    lifecycle
    +
    ownership
    =
    relationship decision

---

# 27. Real-Time Example: Book and Chapter

Consider:

    Book
      ◆
      |
    Chapter

A Chapter is normally considered part of a specific Book.

If the Book is removed from the model:

    Chapter

has no independent role as a chapter of that Book.

Therefore:

    Book ◆── Chapter

is a good composition example.

---

# 28. Real-Time Example: Playlist and PlaylistItem

A realistic music system may use:

    Playlist
       ◆
       |
    PlaylistItem
       |
       ◇
       |
      Song

Why?

A PlaylistItem belongs strongly to the Playlist.

But:

    Song

exists independently.

Therefore:

    Playlist ◆── PlaylistItem

and:

    PlaylistItem ◇── Song

This is an excellent system-design pattern.

---

# 29. Real-Time Example: Shopping Cart and CartItem

Consider:

    ShoppingCart
         ◆
         |
      CartItem

A CartItem exists because it represents an item in a particular cart.

When the Cart is removed:

    CartItems

are normally removed as part of the cart.

Therefore:

    ShoppingCart ◆── CartItem

is a strong composition example.

---

# 30. Real-Time Example: Invoice and InvoiceLine

Consider:

    Invoice
      ◆
      |
    InvoiceLine

An InvoiceLine belongs to one particular Invoice.

If the Invoice disappears:

    InvoiceLine

normally disappears with it.

Therefore:

    Invoice ◆── InvoiceLine

Composition.

---

# 31. Real-Time Example: Exam and Question

Consider:

    Exam
      ◆
      |
    Question

If Questions are created specifically for that Exam and have no independent existence in the domain:

    Composition

Example:

    Exam
      ◆
      ├── Question 1
      ├── Question 2
      └── Question 3

If questions come from a reusable Question Bank, however:

    Exam
      ◇
      |
    Question

may be more appropriate.

This is an excellent interview trap.

---

# 32. Exam Question Bank Example

Suppose:

    Question Bank
         ◇
         |
       Question

Questions can be reused across:

    Exam A
    Exam B
    Exam C

Then:

    Question

has an independent lifecycle.

Therefore:

    Question Bank ◇── Question

But if:

    Exam
      ◆
      |
    ExamQuestion

and ExamQuestion exists only for that Exam:

    Composition

This demonstrates a sophisticated domain model.

---

# 33. Real-Time Example: UI and Components

Consider:

    Window
      ◆
      |
    Button

A Button may be created specifically as part of a particular UI Window.

The Window manages the Button.

Therefore:

    Window ◆── Button

can represent composition.

---

# 34. Real-Time Example: HTML DOM

Consider:

    Document
       ◆
       |
      Node
     /    \
 Element  Text

A DOM tree is naturally hierarchical.

Nodes belong to a particular document/tree.

Removing the document tree removes the corresponding nodes from that tree.

This provides a useful conceptual composition example.

---

# 35. Java Implementation

Java does not have a keyword:

    composition

Composition is implemented using:

    fields
    object references
    constructors
    private members
    collections
    methods

Example:

    class House {

        private Room room;

        House() {

            room = new Room();
        }
    }

Conceptually:

    House
      ◆
      |
    Room

---

# 36. Composition Through Internal Object Creation

Example:

    class Car {

        private final Engine engine;

        Car() {

            engine = new Engine();
        }
    }

The Car creates the Engine internally.

This is a strong signal of ownership.

Conceptually:

    Car ◆── Engine

Again, the exact lifecycle semantics matter.

---

# 37. Composition Through Multiple Parts

Example:

    class Computer {

        private final CPU cpu;
        private final RAM ram;
        private final Motherboard motherboard;

        Computer() {

            cpu = new CPU();
            ram = new RAM();
            motherboard =
                new Motherboard();
        }
    }

Conceptually:

    Computer
       ◆
       ├── CPU
       ├── RAM
       └── Motherboard

This represents a whole consisting of strongly owned components.

---

# 38. Composition Through Collection

Example:

    class Order {

        private final List<OrderItem>
            items =
            new ArrayList<>();

        public void addItem(
            Product product,
            int quantity
        ) {

            items.add(
                new OrderItem(
                    product,
                    quantity
                )
            );
        }
    }

Here:

    Order

creates:

    OrderItem

The Order controls the item lifecycle.

Therefore:

    Order ◆── OrderItem

is a strong composition model.

---

# 39. Composition and Encapsulation

A major benefit of composition is encapsulation.

Example:

    class Order {

        private final List<OrderItem>
            items;

        public void addItem(...) {
            ...
        }

        public void removeItem(...) {
            ...
        }
    }

The Order controls:

    creation
    modification
    removal
    access

of its OrderItems.

This makes the relationship explicit.

---

# 40. Composition and Constructor

Example:

    class House {

        private final Room room;

        House() {

            this.room =
                new Room();
        }
    }

The constructor establishes the internal part.

This makes ownership clear.

---

# 41. Composition and Factory Methods

The whole can create parts using methods.

Example:

    class Order {

        private final List<OrderItem>
            items = new ArrayList<>();

        public void addItem(
            Product product,
            int quantity
        ) {

            OrderItem item =
                new OrderItem(
                    product,
                    quantity
                );

            items.add(item);
        }
    }

The Order controls the lifecycle of OrderItem.

This strongly supports composition.

---

# 42. Composition and Private Constructors

A class may make its part difficult to create independently.

Example:

    class OrderItem {

        private OrderItem(
            Product product
        ) {
            ...
        }

        static OrderItem create(
            Product product
        ) {
            return new OrderItem(product);
        }
    }

The whole can control how parts are created.

This can reinforce strong ownership.

---

# 43. Composition and Access Control

Example:

    class Order {

        private final List<OrderItem>
            items;

        public List<OrderItem>
        getItems() {

            return List.copyOf(items);
        }
    }

The caller receives a read-only view.

The Order retains control over its internal collection.

This supports strong encapsulation.

---

# 44. Composition and Defensive Copying

Suppose:

    List<OrderItem> items

is passed from outside.

If the Order wants stronger ownership:

    new ArrayList<>(items)

can prevent external code from replacing the internal collection contents through the original list reference.

But remember:

> [!important]
> Defensive copying improves encapsulation.
>
> It does not, by itself, define Composition.
>
> Composition is determined by ownership and lifecycle semantics.

---

# 45. Composition and `final`

Example:

    private final Engine engine;

This means:

    engine reference
    cannot be reassigned

It does not automatically mean:

    Composition

But when combined with:

    internal creation
    +
    private ownership
    +
    dependent lifecycle

it strongly supports a composition-style design.

---

# 46. Composition and Garbage Collection

Do not confuse:

    Composition

with:

    Garbage Collection

Composition is:

    design relationship

Garbage Collection is:

    memory management

When a whole becomes unreachable, its exclusively referenced parts may also become unreachable.

But this is a consequence of object references and reachability, not a special Java "composition mechanism."

> [!warning]
> Java garbage collection does not understand UML diamonds.

---

# 47. Composition and `null`

Suppose:

    order.items = null;

This is an implementation detail.

It does not define the UML relationship.

The relationship is determined by:

    ownership
    lifecycle
    whole-part semantics

---

# 48. Composition and Interfaces

Composition does not require concrete classes.

Example:

    interface Engine {
        void start();
    }

    class Car {

        private final Engine engine;

        Car(Engine engine) {
            this.engine = engine;
        }
    }

This may look like strong ownership in some designs, but the external injection of Engine means the lifecycle semantics need careful consideration.

Therefore:

> [!important]
> Dependency injection does not automatically mean Aggregation.
>
> The relationship still depends on domain ownership and lifecycle.

---

# 49. Composition and Dependency Injection

This is an advanced interview topic.

Many developers assume:

    Constructor injection
    → Aggregation

Not necessarily.

Example:

    class Order {

        private final OrderRepository repository;

        Order(OrderRepository repository) {
            this.repository = repository;
        }
    }

This is usually a dependency relationship, not composition.

Why?

Because:

    OrderRepository

is not a part of the Order.

It is a service the Order uses.

Therefore:

    Whole-Part
    ≠
    Dependency

This distinction is very important.

---

# 50. Composition vs Dependency Injection

Compare:

    Order
      ◆
      |
    OrderItem

OrderItem:

    → part of Order

versus:

    Order
      |
      ↓
    OrderRepository

Repository:

    → service used by Order

Therefore:

    OrderItem
    → Composition candidate

    OrderRepository
    → Dependency

This is an important system-design distinction.

---

# 51. Composition and Loose Coupling

Composition itself represents strong ownership.

That does not mean the entire system must be tightly coupled.

Example:

    Order
      ◆
      |
    OrderItem
      |
      ↓
    Product

Order strongly owns OrderItems.

But OrderItem can depend on:

    Product interface

This can preserve abstraction while maintaining strong lifecycle ownership.

---

# 52. Composition and Polymorphism

Composition can work with polymorphism.

Example:

    interface PaymentMethod {
        void pay();
    }

    class CreditCardPayment
        implements PaymentMethod {
        ...
    }

    class UPIPayment
        implements PaymentMethod {
        ...
    }

A Payment object may contain a PaymentMethod.

However, whether this is composition depends on whether PaymentMethod is a true part of Payment or merely a dependency.

This is why semantic analysis matters.

---

# 53. Composition and SOLID

Composition is heavily connected to good object-oriented design.

The principle:

> **Favor composition over inheritance**

is a major software design idea.

It means:

    Instead of creating deep inheritance hierarchies,
    combine objects through composition.

Example:

Instead of:

    SmartPhone
       ↑
    AdvancedPhone
       ↑
    SuperSmartPhone

we can use:

    SmartPhone
       |
       ◆
       ├── Camera
       ├── Storage
       ├── Processor
       └── NetworkModule

This makes behavior modular.

---

# 54. Favor Composition Over Inheritance

This is a famous interview statement.

Inheritance creates:

    strong type coupling
    rigid hierarchy
    difficult changes

Composition allows:

    interchangeable components
    flexible behavior
    easier testing
    better modularity

Example:

    Car
      ◆
      ├── Engine
      ├── BrakeSystem
      ├── Transmission
      └── Navigation

Instead of building a huge inheritance hierarchy, functionality can be composed from components.

---

# 55. Composition in Strategy Pattern

A classic example is the Strategy Pattern.

    PaymentService
         ◆
         |
    PaymentStrategy
       /       \
    Card       UPI

The service can be composed with a strategy object.

Then behavior can change without changing the entire class hierarchy.

This demonstrates:

    Composition
    +
    Polymorphism
    +
    Strategy Pattern

---

# 56. Composition in Dependency Injection

Example:

    class OrderService {

        private final PaymentService
            paymentService;

        OrderService(
            PaymentService paymentService
        ) {
            this.paymentService =
                paymentService;
        }
    }

Conceptually, this is often described as:

    has-a dependency

But whether it is UML composition depends on whether PaymentService is truly a part of OrderService or simply a collaborating service.

Usually:

    OrderService
       ↓
    PaymentService

is better understood as a dependency.

This is an important high-level distinction.

---

# 57. Composition vs "Has-A"

A common interview question:

> Is every HAS-A relationship Composition?

Answer:

    NO.

HAS-A is a broad concept.

Possible relationships:

    Association
    Aggregation
    Composition

The exact relationship depends on:

    ownership
    lifecycle
    whole-part semantics

---

# 58. Composition Decision Tree

Use this during interviews:

    Are A and B related?
            |
           YES
            ↓
       Is B a part of A?
         /        \
       NO          YES
       |            |
       ↓            ↓
 Association    Is B's lifecycle
                strongly tied to A?
                    /      \
                  YES       NO
                   |         |
                   ↓         ↓
              Composition  Aggregation
                               or
                          Association
~~~

---

# 59. Fast Recognition Algorithm

When solving a relationship question:

### Step 1

Identify:

    Whole
    Part

### Step 2

Ask:

    Is it IS-A?

If yes:

    Inheritance

### Step 3

Ask:

    Is it whole-part?

If no:

    Association

### Step 4

Ask:

    Is ownership strong?

If yes:

    Continue

### Step 5

Ask:

    Is the part lifecycle dependent?

If yes:

    Composition

If no:

    Aggregation

---

# 60. Five-Second Composition Test

> [!important]
> Ask these three questions:
>
>     1. Is it Whole-Part?
>     2. Does the Whole strongly own the Part?
>     3. Does the Part's lifecycle depend on the Whole?
>
> If:
>
>     YES
>     YES
>     YES
>
> think:
>
>     Composition

---

# 61. Five-Second OOP Relationship Test

> [!tip]
> Memorize this:

    IS-A
    → Inheritance

    Related
    → Association

    Whole-Part + Independent
    → Aggregation

    Whole-Part + Dependent
    → Composition

    Temporary Use
    → Dependency

This single pattern can solve many interview questions.

---

# 62. Pattern Recognition

> [!important]
> **Pattern 1 — Strong Whole-Part**
>
> If the question says:
>
>     strong whole-part relationship
>
> think:
>
>     Composition

> [!important]
> **Pattern 2 — Strong Ownership**
>
> If the whole:
>
>     creates
>     controls
>     manages
>     destroys
>
> the part:
>
>     Composition candidate

> [!important]
> **Pattern 3 — Dependent Lifecycle**
>
> If:
>
>     Part lifecycle
>     depends on Whole
>
> think:
>
>     Composition

> [!important]
> **Pattern 4 — Filled Diamond**
>
> If you see:
>
>     ◆
>
> think:
>
>     Composition

> [!important]
> **Pattern 5 — Exclusive Part**
>
> If the part belongs strongly to one whole:
>
>     Composition candidate

> [!important]
> **Pattern 6 — Whole Creates Part**
>
> If the whole creates and manages the part internally:
>
>     Composition candidate

> [!important]
> **Pattern 7 — Part Cannot Meaningfully Exist Alone**
>
> think:
>
>     Composition

---

# 63. Shortcuts

> [!tip]
> **Shortcut 1: Filled Diamond**
>
>     ◆
>     → Composition

> [!tip]
> **Shortcut 2: Strong Ownership**
>
> Whole strongly owns Part:
>
>     Composition

> [!tip]
> **Shortcut 3: Death Test**
>
> Whole dies:
>
>     Part lifecycle ends
>
> → Composition candidate

> [!tip]
> **Shortcut 4: Exclusive Ownership**
>
> Part belongs strongly to one Whole:
>
>     Composition candidate

> [!tip]
> **Shortcut 5: Internal Creation**
>
> Whole creates Part and controls it:
>
>     Composition candidate

> [!tip]
> **Shortcut 6: Dependent Lifecycle**
>
> Part cannot meaningfully exist independently:
>
>     Composition

> [!tip]
> **Shortcut 7: Hollow Diamond**
>
>     ◇
>     → Aggregation
>
> Do not confuse it with:
>
>     ◆
>     → Composition

> [!tip]
> **Shortcut 8: IS-A**
>
>     IS-A
>     → Inheritance

> [!tip]
> **Shortcut 9: General Relationship**
>
>     Related
>     → Association

> [!tip]
> **Shortcut 10: Temporary Usage**
>
>     Uses temporarily
>     → Dependency

---

# 64. Common Exam Patterns

> [!important] Must Master

1. Definition of Composition
2. Strong whole-part relationship
3. Strong ownership
4. Dependent lifecycle
5. Filled diamond notation
6. Composition vs Association
7. Composition vs Aggregation
8. Composition vs Inheritance
9. Composition vs Dependency
10. Composition in Java
11. Composition using fields
12. Composition using constructors
13. Composition using collections
14. Composition using private members
15. Composition and encapsulation
16. Composition and `final`
17. Composition and object creation
18. Composition and garbage collection
19. Composition and polymorphism
20. Composition and interfaces
21. Composition and dependency injection
22. Composition and SOLID
23. Favor Composition over Inheritance
24. Strategy Pattern
25. Lifecycle-based questions
26. Ownership-based questions
27. UML diagram questions
28. Multiplicity questions
29. Scenario-based questions
30. System-design relationship questions
31. Order-OrderItem
32. Cart-CartItem
33. Invoice-InvoiceLine
34. Book-Chapter
35. Document-Paragraph
36. Exam-Question
37. Playlist-PlaylistItem
38. House-Room
39. Company-Department
40. University-Department

---

# 65. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Every HAS-A Is Composition

Wrong:

    A has B
    → Composition

Correct:

    HAS-A
    → broad category

Possible relationships:

    Association
    Aggregation
    Composition

---

### Mistake 2 — Confusing Aggregation and Composition

Wrong:

    Both are whole-part
    → same

Correct:

    Aggregation
    → weak ownership
    → independent lifecycle

    Composition
    → strong ownership
    → dependent lifecycle

---

### Mistake 3 — Thinking Creation Inside Always Means Composition

Internal creation is strong evidence.

But the real concept is:

    ownership
    +
    lifecycle

Do not rely on creation alone.

---

### Mistake 4 — Thinking `final` Means Composition

Wrong:

    final
    → Composition

Correct:

    final
    → reference cannot be reassigned

It does not define the UML relationship.

---

### Mistake 5 — Thinking Composition Is a Java Keyword

Wrong.

Java has no:

    composition

keyword.

---

### Mistake 6 — Thinking Composition Controls Garbage Collection

Wrong.

Java GC uses:

    reachability

Composition is:

    design semantics

---

### Mistake 7 — Thinking Filled Diamond Means Inheritance

Wrong.

    ◆
    → Composition

Inheritance uses a different UML notation.

---

### Mistake 8 — Thinking Composition Means the Part Can Never Be Replaced

Not necessarily.

A component can sometimes be replaced while the whole continues to exist.

The important question is:

    Who owns the lifecycle?

---

### Mistake 9 — Confusing Dependency With Composition

Example:

    OrderService
        ↓
    PaymentService

may simply mean:

    dependency

The PaymentService may not be a physical/logical part of OrderService.

---

### Mistake 10 — Assuming Every Real-World Example Has One Fixed Answer

For example:

    Car-Engine

can be modeled differently depending on:

    replacement
    ownership
    inventory
    lifecycle
    domain requirements

Always explain your assumption.

---

### Mistake 11 — Confusing Multiplicity With Relationship Type

    1:N

means:

    One-to-Many

It does not mean:

    Composition

---

### Mistake 12 — Assuming Composition Requires Private Fields

Private fields are useful for encapsulation.

But:

    private
    ≠
    composition

The lifecycle semantics are the important part.

---

# 66. Advanced Interview Questions

## Q1. What is Composition in OOP?

Strong answer:

> Composition is a strong whole-part relationship where the whole strongly owns its parts and the lifecycle of the parts is dependent on the whole. In UML, composition is represented by a filled diamond.

---

## Q2. What is the UML symbol for Composition?

Answer:

    Filled diamond

Symbol:

    ◆

The diamond is placed near the whole.

---

## Q3. What is the difference between Composition and Aggregation?

Answer:

> Composition represents strong ownership and dependent lifecycle, while aggregation represents weak ownership and independent lifecycle.

---

## Q4. Is Composition a Java keyword?

Answer:

> No. Composition is an OOP/UML design concept implemented using normal Java constructs such as object references, fields, constructors, collections, and methods.

---

## Q5. What is the key property of Composition?

Answer:

    Strong ownership
    +
    Dependent lifecycle

---

## Q6. What happens to the part when the whole is destroyed?

In a composition model:

    Part lifecycle ends
    with the Whole.

---

## Q7. Can the same part belong to multiple wholes?

Generally, composition represents strong ownership of the part by one whole.

If the same independent object is shared across multiple wholes, aggregation or association may be more appropriate.

---

## Q8. Can Composition be one-to-many?

Yes.

Example:

    Order ◆── OrderItem

One Order:

    → Many OrderItems

---

## Q9. Can Composition be one-to-one?

Yes.

Example:

    House ◆── Room

if the model represents one specific Room as a strongly owned component.

---

## Q10. Can Composition be many-to-many?

A true composition normally does not represent shared ownership of the same part by multiple wholes.

If multiple wholes share the same independently existing object, aggregation or association is usually more appropriate.

---

## Q11. Does Java provide a Composition keyword?

No.

It is a design concept.

---

## Q12. Does `new` automatically indicate Composition?

No.

It is evidence of creation responsibility, but not sufficient by itself.

---

## Q13. What is the Death Test?

Ask:

> If the whole disappears, does the part's lifecycle end with it?

If yes:

    Composition candidate

---

## Q14. What is the Ownership Test?

Ask:

> Does the whole strongly control creation, management, and lifecycle of the part?

If yes:

    Composition candidate

---

## Q15. What is the difference between Composition and Inheritance?

Inheritance:

    IS-A

Composition:

    HAS-A

---

## Q16. Why is Composition often preferred over Inheritance?

Composition provides:

    flexibility
    modularity
    replaceable components
    easier testing
    reduced hierarchy coupling

This supports the design principle:

    Favor Composition Over Inheritance

---

## Q17. Can Composition use interfaces?

Yes.

A whole can own a component through an interface while hiding implementation details.

---

## Q18. Can Composition use Dependency Injection?

Yes, but dependency injection alone does not prove Composition.

You still need:

    whole-part semantics
    +
    ownership
    +
    lifecycle relationship

---

## Q19. Does Composition mean the whole creates the part?

Often, but not always.

Creation responsibility is a clue.

Lifecycle ownership is the stronger definition.

---

## Q20. What is the strongest difference between Aggregation and Composition?

The strongest difference is:

    Lifecycle dependency

Aggregation:

    Part independent

Composition:

    Part dependent

---

# 67. Scenario-Based Questions

## Example 1 — Order and OrderItem

### Question

An Order contains OrderItems. An OrderItem exists only as part of that Order.

### Recognition

    Whole:
    Order

    Part:
    OrderItem

    Ownership:
    Strong

    Lifecycle:
    Dependent

### Answer

    Composition

    Order ◆── OrderItem

---

## Example 2 — Shopping Cart and CartItem

### Question

A CartItem represents an item in one specific shopping cart and is removed when the cart is removed.

### Recognition

    Whole-Part
    +
    Strong Ownership
    +
    Dependent Lifecycle

### Answer

    Composition

---

## Example 3 — Book and Chapter

### Question

A Chapter belongs to one specific Book and is modeled as a component of that Book.

### Answer

    Composition

    Book ◆── Chapter

---

## Example 4 — Document and Paragraph

### Question

Paragraphs are created as components of a document and do not have independent existence in the model.

### Answer

    Composition

---

## Example 5 — Playlist and Song

### Question

Songs exist independently and can belong to multiple playlists.

### Recognition

    Independent Song

### Answer

    Aggregation or Association

Not Composition.

---

## Example 6 — Exam and Question

### Question

An Exam creates its own questions and those questions have no independent existence outside the Exam.

### Recognition

    Strong ownership
    +
    Dependent lifecycle

### Answer

    Composition

---

## Example 7 — Question Bank and Question

### Question

A Question Bank stores reusable questions that can appear in multiple exams.

### Recognition

    Question exists independently
    +
    reusable

### Answer

    Aggregation or Association

Not Composition.

---

## Example 8 — House and Room

### Question

Rooms are modeled as components of a particular House.

### Answer

    Composition

---

## Example 9 — Doctor and Patient

### Question

A Doctor treats Patients, but both entities exist independently.

### Recognition

    No whole-part lifecycle ownership

### Answer

    Association

---

## Example 10 — Order and Product

### Question

An Order references Products, but Products exist independently and can appear in many Orders.

### Recognition

    Product lifecycle independent

### Answer

    Association or Aggregation

Not Composition.

---

# 68. Advanced Scenario: Order System

Consider:

    Customer
       |
       ↓
     Order
       ◆
       |
    OrderItem
       |
       ◇
       |
    Product

Interpretation:

    Customer
    → associated with Order

    Order
    → strongly owns OrderItem

    OrderItem
    → references Product

    Product
    → independent entity

This is a realistic object model.

---

# 69. Advanced Scenario: Learning Platform

Consider:

    Course
       ◆
       |
    Lesson
       ◆
       |
    Quiz
       ◆
       |
    Question

Possible lifecycle:

    Course
      ↓
    Lessons
      ↓
    Quizzes
      ↓
    Questions

If each level is created specifically as part of its parent and has no independent lifecycle:

    Composition

This produces a hierarchical object model.

---

# 70. Advanced Scenario: Company System

Consider:

    Company
       ◆
       |
    Department
       ◆
       |
    Team
       ◆
       |
    Employee

This could represent strong ownership if the domain defines:

    Company owns Department
    Department owns Team
    Team owns Employee

However, real enterprise systems usually treat:

    Employee

as an independent entity.

Therefore, a more realistic model may use:

    Association
    or
    Aggregation

for some of these relationships.

The lesson:

> Never blindly classify a relationship without understanding the lifecycle.

---

# 71. Advanced Scenario: Social Media

Consider:

    User
       |
       ↓
    Post
       ◆
       |
    Comment

A Comment usually belongs to a particular Post.

If the model says:

    Post deleted
       ↓
    Comments deleted

then:

    Post ◆── Comment

is Composition.

But:

    User
       |
       ↓
    Post

may be Association or Aggregation depending on the domain model.

---

# 72. Advanced Scenario: Banking

Consider:

    BankAccount
       ◆
       |
    Transaction

A Transaction belongs to a particular account in the model.

If deleting the Account removes its Transactions:

    Composition

But if Transactions are preserved independently for audit/history:

    Association/Aggregation may be more appropriate.

This is an important system-design consideration.

---

# 73. Advanced Scenario: Logging System

Consider:

    Application
        |
        ↓
      Logger

This is usually not Composition.

Why?

Logger is a service.

It is not necessarily a physical/logical part of Application.

Better interpretation:

    Dependency

This helps distinguish:

    "uses"

from:

    "owns"

---

# 74. Advanced Scenario: Report Generator

Consider:

    Report
      ◆
      |
    ReportSection

A ReportSection belongs to one Report.

Deleting the Report removes its sections.

Therefore:

    Composition

But:

    Report
       ↓
    PDFGenerator

is usually:

    Dependency

because PDFGenerator is a service.

---

# 75. Advanced Scenario: Game Development

Consider:

    Game
      ◆
      |
    GameLevel
      ◆
      |
    Enemy

If enemies exist only inside a particular level and disappear when that level is destroyed:

    Composition

Example:

    Game
      ◆
    Level
      ◆
    Enemy

This creates a hierarchy of owned components.

---

# 76. Composition in System Design

Composition is extremely useful for building modular systems.

Instead of:

    GiantClass
       |
       ├── Everything
       ├── Everything
       ├── Everything
       └── Everything

use:

    MainObject
       ◆
       ├── Component A
       ├── Component B
       ├── Component C
       └── Component D

Benefits:

    modularity
    separation of responsibilities
    maintainability
    testability
    extensibility

---

# 77. Composition and "Favor Composition Over Inheritance"

This principle is extremely important for interviews.

Suppose we need different payment behaviors.

Inheritance approach:

    Payment
       ↑
    CardPayment
       ↑
    SpecialCardPayment
       ↑
    PremiumCardPayment

This can become rigid.

Composition approach:

    PaymentService
         ◆
         |
    PaymentStrategy
       /       \
    Card       UPI

Now behavior can be replaced.

Benefits:

    less rigid hierarchy
    better reuse
    easier testing
    runtime flexibility

---

# 78. Composition and Runtime Flexibility

Inheritance often determines behavior structurally.

Composition can allow components to change at runtime.

Example:

    PaymentService
         |
         ↓
    PaymentStrategy

Initially:

    CardPayment

Later:

    UPIPayment

The service can switch strategies.

This is one reason composition is powerful.

---

# 79. Composition and Testing

Composition makes unit testing easier when components are replaceable.

Example:

    OrderService
         ↓
    PaymentService

A test can supply:

    MockPaymentService

instead of the real implementation.

This is primarily dependency injection and loose coupling, but composition-style object assembly can support this architecture.

---

# 80. Composition and Maintainability

If a class contains smaller specialized components:

    Car
      ◆
      ├── Engine
      ├── BrakeSystem
      └── Transmission

each component can have a focused responsibility.

This improves:

    readability
    testing
    maintenance
    extensibility

---

# 81. Composition and Single Responsibility

Instead of one class doing everything:

    Order
       |
       ├── payment logic
       ├── email logic
       ├── inventory logic
       ├── tax logic
       └── shipping logic

use specialized components:

    Order
       |
       ├── PaymentService
       ├── TaxCalculator
       ├── InventoryService
       └── ShippingService

However, note:

    "contains a service"
    does not automatically mean UML Composition.

These may be dependencies.

The design principle is broader than the strict UML relationship.

---

# 82. Advanced Interview Trap

> [!warning]
> Interviewers may deliberately give:
>
>     A contains B
>
> and ask:
>
>     "Is this Composition?"
>
> Do not immediately say yes.
>
> Ask:
>
>     Is B a true part of A?
>     Who owns B?
>     Can B exist independently?
>     What happens when A is destroyed?
>     Can B be shared?
>
> These questions determine the answer.

---

# 83. Composition Recognition Table

| Question clue | Think |
|---|---|
| Strong whole-part | Composition |
| Strong ownership | Composition |
| Dependent lifecycle | Composition |
| Filled diamond | Composition |
| Part belongs to one whole | Composition candidate |
| Whole controls part | Composition candidate |
| Whole creates/manages part | Composition candidate |
| Part survives independently | Aggregation |
| Weak ownership | Aggregation |
| Hollow diamond | Aggregation |
| General relationship | Association |
| IS-A | Inheritance |
| Temporary usage | Dependency |

---

# 84. Common Interview Traps

> [!warning]
> **Trap 1**
>
>     "HAS-A = Composition"
>
> False.
>
> HAS-A is broader.

> [!warning]
> **Trap 2**
>
>     "new = Composition"
>
> False.
>
> Creation is only a clue.

> [!warning]
> **Trap 3**
>
>     "final = Composition"
>
> False.
>
> `final` controls reassignment.

> [!warning]
> **Trap 4**
>
>     "1:N = Composition"
>
> False.
>
> `1:N` is multiplicity.

> [!warning]
> **Trap 5**
>
>     "Java supports composition with a special keyword"
>
> False.
>
> There is no composition keyword.

> [!warning]
> **Trap 6**
>
>     "Composition controls Garbage Collection"
>
> False.
>
> Java GC uses reachability.

> [!warning]
> **Trap 7**
>
>     "Constructor injection always means Aggregation"
>
> False.
>
> Injection does not determine UML semantics.

---

# 85. Interview Answer Template

When asked:

> "Why is this Composition?"

Use this structure:

    1. Identify the Whole.
    2. Identify the Part.
    3. Explain strong ownership.
    4. Explain lifecycle dependency.
    5. Mention the UML symbol if relevant.

Example:

> "Order is the whole and OrderItem is the part. Order strongly owns its OrderItems, and the OrderItems do not have an independent lifecycle in this model. Therefore, this is a Composition relationship, represented by a filled diamond."

This is a strong interview-quality answer.

---

# 86. Interview Answer Template: Aggregation vs Composition

Use:

    Aggregation:
    weak ownership
    independent lifecycle
    hollow diamond

    Composition:
    strong ownership
    dependent lifecycle
    filled diamond

One-line answer:

> "The key distinction is lifecycle dependency: aggregation allows the part to exist independently, while composition strongly ties the part's lifecycle to the whole."

---

# 87. Formula Sheet

~~~text
COMPOSITION

Composition
= Association
+ Strong Whole-Part Relationship


Core:

Whole ◆── Part


◆
= Filled Diamond
= Composition


◇
= Hollow Diamond
= Aggregation


Main condition:

Whole-Part
+
Strong Ownership
+
Dependent Part Lifecycle
=
Composition


Death Test:

Whole destroyed
+
Part lifecycle ends with Whole
=
Composition candidate


Ownership Test:

Whole strongly controls Part
=
Composition candidate


Creation Test:

Whole creates and manages Part
=
Strong evidence for Composition

But:

Creation alone
≠
formal definition


Exclusive Ownership:

Part strongly belongs to one Whole
=
Composition candidate


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
Dependency


Common examples:

House ◆── Room

Order ◆── OrderItem

ShoppingCart ◆── CartItem

Invoice ◆── InvoiceLine

Book ◆── Chapter

Document ◆── Paragraph

Exam ◆── ExamQuestion

Playlist ◆── PlaylistItem


Important comparison:

Aggregation
→ Weak ownership
→ Independent lifecycle
→ ◇

Composition
→ Strong ownership
→ Dependent lifecycle
→ ◆


Multiplicity:

1:1
→ One-to-One

1:N
→ One-to-Many

N:1
→ Many-to-One

N:N
→ Many-to-Many


Important:

Multiplicity
≠
Composition

`final`
≠
Composition

`new`
≠
Composition

HAS-A
≠
Always Composition

Java
has no Composition keyword.


Master decision:

Related?
→ Association

Whole-Part?
→ Continue

Part Independent?
→ Aggregation

Part Strongly Owned and Dependent?
→ Composition

IS-A?
→ Inheritance

Temporary Use?
→ Dependency
~~~

---

# 88. Quick Revision

> [!summary] One-Minute Revision

### Definition

Composition is a **strong whole-part relationship** where the whole strongly owns the part and the part's lifecycle is dependent on the whole.

### Core Symbol

    ◆

Filled diamond:

    Composition

### Core Pattern

    Whole
       ◆
       |
      Part

### Most Important Property

    Strong ownership
    +
    Dependent lifecycle

### Death Test

    Whole dies
       ↓
    Part lifecycle ends
    with Whole
       ↓
    Composition

### Aggregation Comparison

    Whole ◇── Part

    Part survives
       ↓
    Aggregation

### Composition

    Whole ◆── Part

    Part lifecycle depends
    on Whole
       ↓
    Composition

### Examples

    House ◆── Room

    Order ◆── OrderItem

    Cart ◆── CartItem

    Invoice ◆── InvoiceLine

    Book ◆── Chapter

    Document ◆── Paragraph

    Exam ◆── ExamQuestion

### Association

    General relationship

### Aggregation

    Weak whole-part
    Independent lifecycle
    ◇

### Composition

    Strong whole-part
    Dependent lifecycle
    ◆

### Inheritance

    IS-A

### Dependency

    Temporary usage

### Java

Java has no:

    composition

keyword.

Composition is implemented using:

    fields
    object references
    constructors
    collections
    methods
    encapsulation

### Most Important Interview Rule

Do not decide Composition merely because:

    A has B

Ask:

    Is B a true part of A?
    Does A strongly own B?
    Can B exist independently?
    What happens when A is destroyed?
    Can B belong to another whole?

### Golden Memory Trick

**Composition = "The Whole strongly owns the Part, so the Part's lifecycle depends on the Whole."**

### One-Line Recognition

**If the question describes a strong whole-part relationship with dependent lifecycle, think Composition and remember the filled diamond `◆`.**