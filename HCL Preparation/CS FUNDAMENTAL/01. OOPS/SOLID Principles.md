---
type: concept
subject: aptitude
topic: "SOLID Principles"
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
  - solid
  - srp
  - ocp
  - lsp
  - isp
  - dip
  - software-design
  - clean-code
  - design-principles
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Coupling and Cohesion]]"
  - "[[Abstraction]]"
  - "[[Encapsulation]]"
  - "[[Polymorphism]]"
  - "[[Inheritance]]"
  - "[[Composition]]"
  - "[[Dependency Injection]]"
  - "[[Design Patterns]]"
---

# SOLID Principles

> [!summary]
> **SOLID is a set of five object-oriented design principles that help create software that is easier to understand, maintain, test, extend, and modify.**
>
> The five principles are:
>
> **S** → Single Responsibility Principle  
> **O** → Open/Closed Principle  
> **L** → Liskov Substitution Principle  
> **I** → Interface Segregation Principle  
> **D** → Dependency Inversion Principle
>
> Core goal:
>
> **High Cohesion + Low Coupling + Maintainable Design**

---

# 1. Core Concept

SOLID is not a programming language feature.

It is a collection of **software design principles**.

These principles help answer questions such as:

- Where should a responsibility belong?
- How should classes depend on each other?
- How can we add new functionality safely?
- How can subclasses remain compatible with parent types?
- How can interfaces remain focused?
- How can high-level business logic avoid depending directly on low-level implementations?

The five principles are:

| Letter | Principle | Main Idea |
|---|---|---|
| S | Single Responsibility Principle | One primary responsibility |
| O | Open/Closed Principle | Open for extension, closed for modification |
| L | Liskov Substitution Principle | Subtypes must be safely substitutable |
| I | Interface Segregation Principle | Depend only on interfaces you need |
| D | Dependency Inversion Principle | Depend on abstractions, not concrete implementations |

---

# 2. The Big Picture

Think of SOLID as a software-design checklist.

```text
                 SOLID
                   |
       +-----------+-----------+
       |           |           |
       ↓           ↓           ↓
    Focused     Extensible   Replaceable
    Classes      Design        Types
       |
       +---------------------------+
                                   |
                             Maintainable
                               Software
```

A good SOLID design generally tries to achieve:

```text
High Cohesion
+
Low Coupling
+
Clear Responsibilities
+
Stable Abstractions
+
Safe Extension
```

---

# 3. Basic Meaning

SOLID consists of five principles.

## S — Single Responsibility Principle

A class should have:

```text
One primary responsibility
```

and therefore ideally:

```text
One primary reason to change
```

---

## O — Open/Closed Principle

A software component should be:

```text
Open for extension
Closed for modification
```

Meaning:

> New behavior should preferably be added by extending the design rather than repeatedly changing stable existing code.

---

## L — Liskov Substitution Principle

Objects of a subtype should be usable wherever objects of the parent type are expected without breaking the expected behavior or contract.

Simple memory:

```text
Child should safely behave like Parent
```

---

## I — Interface Segregation Principle

Clients should not be forced to depend on methods they do not need.

Simple memory:

```text
Small focused interfaces
>
Huge interfaces
```

---

## D — Dependency Inversion Principle

High-level modules should not depend directly on low-level implementation details.

Both should depend on abstractions.

Simple memory:

```text
High Level
    ↓
Abstraction
    ↑
Low Level
```

---

# 4. Main Formula

SOLID has no mathematical formula.

Use these conceptual rules:

$$
\boxed{S = One\ Responsibility}
$$

$$
\boxed{O = Extend\ Without\ Constantly\ Modifying\ Stable\ Code}
$$

$$
\boxed{L = Subtypes\ Must\ Preserve\ Expected\ Contracts}
$$

$$
\boxed{I = Small,\ Focused\ Interfaces}
$$

$$
\boxed{D = Depend\ on\ Abstractions}
$$

Overall:

$$
\boxed{SOLID \rightarrow Maintainable\ Object-Oriented\ Design}
$$

---

# 5. Most Important Memory Trick

> [!tip]
> **S → Single Job**
>
> **O → Open to Extension**
>
> **L → Legitimate Substitute**
>
> **I → Interface is Small**
>
> **D → Depend on Abstraction**

Ultra-short memory:

```text
S → One Job
O → Extend
L → Substitute
I → Split Interfaces
D → Abstraction
```

---

# 6. SOLID and Coupling/Cohesion

SOLID is strongly connected with:

```text
High Cohesion
+
Low Coupling
```

### SRP

Encourages:

```text
High Cohesion
```

### OCP

Reduces unnecessary modification of stable code.

### LSP

Makes inheritance and polymorphism safer.

### ISP

Reduces unnecessary interface dependencies.

### DIP

Reduces dependency on concrete implementations.

Therefore:

```text
SOLID
  ↓
Better Design
  ↓
High Cohesion
+
Low Coupling
```

---

# 7. S — Single Responsibility Principle

## Definition

> [!summary]
> **A class should have one primary responsibility and one primary reason to change.**

This does NOT necessarily mean:

```text
One method per class
```

It means:

```text
One cohesive responsibility
```

---

# 8. What Is a Responsibility?

A responsibility is a meaningful job performed by a class.

Example:

```text
Invoice
```

may be responsible for:

```text
Calculating invoice totals
Managing invoice items
```

But this class should not necessarily also be responsible for:

```text
Sending emails
Printing PDFs
Saving to database
Sending SMS
```

Those are separate concerns.

---

# 9. Bad SRP Example

```java
class Employee {

    void calculateSalary() {
        // salary logic
    }

    void saveToDatabase() {
        // database logic
    }

    void generateReport() {
        // report logic
    }

    void sendEmail() {
        // email logic
    }
}
```

Responsibilities:

```text
Salary
Database
Reporting
Email
```

There are multiple reasons for change.

Therefore:

```text
Low Cohesion
Possible SRP Violation
```

---

# 10. Better SRP Design

```java
class SalaryCalculator {

    double calculateSalary(Employee employee) {
        return 0;
    }
}
```

```java
class EmployeeRepository {

    void save(Employee employee) {
        // database logic
    }
}
```

```java
class EmployeeReport {

    void generate(Employee employee) {
        // report logic
    }
}
```

```java
class EmailService {

    void send(String message) {
        // email logic
    }
}
```

Now responsibilities are separated.

```text
SalaryCalculator
→ Salary

EmployeeRepository
→ Persistence

EmployeeReport
→ Reporting

EmailService
→ Email
```

---

# 11. SRP Recognition Trick

> [!important]
> If the question says:
>
> "The class has multiple unrelated responsibilities."
>
> Think:
>
> **SRP violation**

Another clue:

> "The class changes for many unrelated reasons."

Think:

```text
Single Responsibility Principle
```

---

# 12. SRP Shortcut

> [!tip]
> Ask:
>
> **"How many reasons can this class change?"**
>
> If the answer is:
>
> ```text
> Many unrelated reasons
> ```
>
> suspect an SRP violation.

---

# 13. SRP Real-Time Example — E-Commerce

Bad:

```text
OrderService
├── calculateTotal()
├── saveOrder()
├── sendEmail()
├── generateInvoicePDF()
├── processPayment()
└── sendSMS()
```

Better:

```text
OrderService
PaymentService
OrderRepository
InvoiceService
EmailService
SmsService
```

Each component has a focused responsibility.

---

# 14. SRP Real-Time Example — College Management

Bad:

```text
CollegeManager

registerStudent()
calculateFees()
sendEmail()
generateHallTicket()
saveToDatabase()
manageLibrary()
```

Better:

```text
StudentService
FeeService
EmailService
HallTicketService
StudentRepository
LibraryService
```

---

# 15. SRP Interview Question

### Question

Does SRP mean a class should contain only one method?

### Answer

No.

SRP means a class should have one cohesive responsibility or one primary reason to change.

Example:

```java
class Order {

    void addItem() {
    }

    void removeItem() {
    }

    double calculateTotal() {
        return 0;
    }
}
```

These methods belong to the same responsibility:

```text
Order management
```

Therefore the class can still follow SRP.

---

# 16. O — Open/Closed Principle

## Definition

> [!summary]
> **Software entities should be open for extension but closed for modification.**

Software entities include:

- Classes
- Modules
- Functions
- Components

The idea is:

```text
Existing stable behavior
        ↓
Do not repeatedly modify it
        ↓
Extend behavior instead
```

---

# 17. What Does "Open for Extension" Mean?

It means we should be able to add new behavior.

Example:

```text
Payment
├── CreditCard
├── UPI
├── PayPal
└── NewPaymentMethod
```

We should be able to add:

```text
NewPaymentMethod
```

without rewriting the core payment-processing logic unnecessarily.

---

# 18. What Does "Closed for Modification" Mean?

It does NOT mean:

```text
Code can never be changed.
```

It means:

> Stable, tested code should not need constant modification whenever a new variation is introduced.

This is an important interview distinction.

---

# 19. Bad OCP Example

```java
class PaymentService {

    void pay(String type) {

        if (type.equals("CARD")) {
            // card payment
        }
        else if (type.equals("UPI")) {
            // UPI payment
        }
        else if (type.equals("PAYPAL")) {
            // PayPal payment
        }
    }
}
```

Suppose we add:

```text
Crypto
```

We modify the existing class:

```java
else if (type.equals("CRYPTO")) {
    // crypto payment
}
```

Every new payment type requires modification.

This can become difficult to maintain.

---

# 20. Better OCP Design

Use an abstraction.

```java
interface Payment {

    void pay(double amount);
}
```

Implementation:

```java
class CardPayment implements Payment {

    public void pay(double amount) {
        // card payment
    }
}
```

Another:

```java
class UpiPayment implements Payment {

    public void pay(double amount) {
        // UPI payment
    }
}
```

Another:

```java
class PaypalPayment implements Payment {

    public void pay(double amount) {
        // PayPal payment
    }
}
```

Now adding:

```java
class CryptoPayment implements Payment {

    public void pay(double amount) {
        // crypto payment
    }
}
```

does not require changing the `Payment` interface or the existing payment implementations.

This demonstrates the OCP idea.

---

# 21. OCP Recognition Trick

> [!important]
> If every new feature requires:
>
> ```text
> Editing a large if-else/switch block
> ```
>
> think:
>
> **Possible OCP problem**

If you see:

```text
if type == A
if type == B
if type == C
if type == D
```

and new types keep being added:

```text
Strategy
Polymorphism
Factory
Plugin architecture
```

may be useful depending on the design.

---

# 22. OCP Shortcut

> [!tip]
> **New variation?**
>
> Ask:
>
> "Can I add a new implementation instead of changing stable logic?"
>
> If yes:
>
> **OCP-friendly design**

---

# 23. OCP Real-Time Example — Notifications

Bad:

```java
class NotificationService {

    void send(String type, String message) {

        if (type.equals("EMAIL")) {
            // email
        }

        if (type.equals("SMS")) {
            // SMS
        }

        if (type.equals("PUSH")) {
            // push
        }
    }
}
```

Better:

```java
interface Notification {

    void send(String message);
}
```

Implementations:

```text
EmailNotification
SmsNotification
PushNotification
WhatsAppNotification
```

New notification types can be added as new implementations.

---

# 24. L — Liskov Substitution Principle

## Definition

> [!summary]
> **If B is a subtype of A, objects of B should be usable wherever objects of A are expected without breaking the expected behavior or contract.**

Simple memory:

```text
Child should safely behave like Parent
```

---

# 25. LSP Basic Example

Suppose:

```java
class Bird {

    void eat() {
    }
}
```

and:

```java
class Sparrow extends Bird {

    void fly() {
    }
}
```

A Sparrow can still behave as a Bird for operations defined by `Bird`.

Therefore:

```text
Sparrow
is-a
Bird
```

This is a reasonable substitution relationship.

---

# 26. Famous LSP Example — Rectangle and Square

Suppose:

```java
class Rectangle {

    protected int width;
    protected int height;

    void setWidth(int width) {
        this.width = width;
    }

    void setHeight(int height) {
        this.height = height;
    }

    int area() {
        return width * height;
    }
}
```

Now:

```java
class Square extends Rectangle {

    @Override
    void setWidth(int width) {
        this.width = width;
        this.height = width;
    }

    @Override
    void setHeight(int height) {
        this.width = height;
        this.height = height;
    }
}
```

At first glance:

```text
Square is-a Rectangle
```

mathematically.

But behaviorally, the substitution can break assumptions.

Example:

```java
Rectangle r = new Square();

r.setWidth(5);
r.setHeight(10);

System.out.println(r.area());
```

A caller expecting independent width and height may expect:

```text
50
```

But Square enforces:

```text
10 × 10 = 100
```

The subtype changes the expected behavior.

This is a classic LSP discussion.

---

# 27. Important LSP Insight

LSP is NOT simply:

```text
Child extends Parent
```

Inheritance alone does not guarantee LSP.

The real question is:

> **Can the subtype preserve the behavioral expectations of the parent contract?**

---

# 28. LSP Contract Thinking

Think about three things:

```text
Preconditions
Postconditions
Invariants
```

A subtype should not unexpectedly violate the parent's behavioral contract.

Simplified interview memory:

```text
Parent Promise
      ↓
Child must honor it
```

---

# 29. LSP Recognition Trick

> [!important]
> If the question says:
>
> "Subclass cannot be used where superclass is expected."
>
> Think:
>
> **Liskov Substitution Principle violation**

Another clue:

```text
Child changes expected parent behavior
```

Think:

```text
LSP
```

---

# 30. LSP Bad Example — Payment

Suppose:

```java
class Payment {

    void pay(double amount) {
        // payment
    }
}
```

Then:

```java
class FreePayment extends Payment {

    @Override
    void pay(double amount) {
        throw new UnsupportedOperationException();
    }
}
```

If code expects every `Payment` to support:

```text
pay()
```

but the subtype throws an exception instead, the subtype may violate the expected contract.

This suggests poor abstraction.

---

# 31. LSP Better Design

Instead of forcing unrelated types into one hierarchy:

```java
interface Payable {

    void pay(double amount);
}
```

Only payment-capable classes implement it.

Or design a more appropriate abstraction.

The principle:

```text
Do not force a subtype to support behavior
that contradicts the parent contract.
```

---

# 32. LSP Real-Time Example — File Storage

Suppose:

```text
Storage
├── LocalStorage
├── CloudStorage
└── ReadOnlyStorage
```

If `Storage` promises:

```text
read()
write()
delete()
```

but `ReadOnlyStorage` cannot safely perform:

```text
write()
delete()
```

then the abstraction may be poorly designed.

Possible solution:

```text
ReadableStorage
WritableStorage
DeletableStorage
```

This also connects LSP with ISP.

---

# 33. LSP Shortcut

> [!tip]
> Ask:
>
> **"Can I replace Parent with Child without surprising the client?"**
>
> If yes:
>
> LSP is likely satisfied.
>
> If no:
>
> suspect an LSP violation.

---

# 34. I — Interface Segregation Principle

## Definition

> [!summary]
> **Clients should not be forced to depend on methods they do not use.**

Simple memory:

```text
Don't create one huge interface.
Create focused interfaces.
```

---

# 35. Bad ISP Example

```java
interface Worker {

    void work();

    void eat();

    void sleep();
}
```

Suppose a robot implements it:

```java
class Robot implements Worker {

    public void work() {
    }

    public void eat() {
        throw new UnsupportedOperationException();
    }

    public void sleep() {
        throw new UnsupportedOperationException();
    }
}
```

The robot does not need:

```text
eat()
sleep()
```

The interface is too large.

This violates ISP.

---

# 36. Better ISP Design

Split the interface:

```java
interface Workable {

    void work();
}
```

```java
interface Eatable {

    void eat();
}
```

```java
interface Sleepable {

    void sleep();
}
```

Human:

```java
class Human
        implements Workable, Eatable, Sleepable {

    public void work() {
    }

    public void eat() {
    }

    public void sleep() {
    }
}
```

Robot:

```java
class Robot
        implements Workable {

    public void work() {
    }
}
```

Now each client depends only on what it needs.

---

# 37. ISP Recognition Trick

> [!important]
> If you see:
>
> ```text
> Huge Interface
> ```
>
> and classes implement methods they do not need:
>
> Think:
>
> **ISP violation**

Especially watch for:

```java
throw new UnsupportedOperationException();
```

inside unused interface methods.

This is a strong practical clue.

---

# 38. ISP Shortcut

> [!tip]
> **Big Interface → Split It**
>
> **Unused Methods → ISP Problem**

---

# 39. ISP Real-Time Example — Printer

Bad:

```java
interface Printer {

    void print();

    void scan();

    void fax();

    void copy();
}
```

A basic printer may only support:

```text
print()
```

Better:

```java
interface Printable {
    void print();
}
```

```java
interface Scannable {
    void scan();
}
```

```java
interface Faxable {
    void fax();
}
```

```java
interface Copyable {
    void copy();
}
```

Now devices implement only the capabilities they support.

---

# 40. ISP Real-Time Example — Payment

Bad:

```java
interface PaymentSystem {

    void pay();
    void refund();
    void recurringPayment();
    void internationalPayment();
    void cryptoPayment();
}
```

Not every implementation may support every feature.

Better:

```text
Payable
Refundable
RecurringPayable
InternationalPayable
CryptoPayable
```

Interfaces are focused around capabilities.

---

# 41. D — Dependency Inversion Principle

## Definition

> [!summary]
> **High-level modules should not depend directly on low-level modules. Both should depend on abstractions.**

Also:

> **Abstractions should not depend on details. Details should depend on abstractions.**

This is one of the most important SOLID principles for interviews.

---

# 42. High-Level vs Low-Level

### High-Level Module

Contains:

```text
Business logic
```

Example:

```text
OrderService
```

### Low-Level Module

Contains implementation details.

Examples:

```text
MySQLRepository
StripePayment
SMTPEmailService
FileLogger
```

Bad:

```text
OrderService
      ↓
StripePayment
```

The high-level business logic directly depends on a concrete detail.

---

# 43. DIP Better Architecture

```text
             OrderService
             High Level
                  |
                  ↓
          PaymentGateway
             Abstraction
                  ↑
                  |
           StripePayment
            Low Level
```

Both depend on:

```text
PaymentGateway
```

This is Dependency Inversion.

---

# 44. DIP Example

Bad:

```java
class OrderService {

    private StripePayment payment =
        new StripePayment();

    void placeOrder(double amount) {
        payment.pay(amount);
    }
}
```

Problem:

```text
OrderService
     ↓
StripePayment
```

If we replace Stripe with another payment system, the high-level class must change.

---

# 45. DIP Better Example

```java
interface PaymentGateway {

    void pay(double amount);
}
```

```java
class StripePayment
        implements PaymentGateway {

    public void pay(double amount) {
        // Stripe logic
    }
}
```

```java
class OrderService {

    private final PaymentGateway payment;

    OrderService(PaymentGateway payment) {
        this.payment = payment;
    }

    void placeOrder(double amount) {
        payment.pay(amount);
    }
}
```

Now:

```text
OrderService
      ↓
PaymentGateway
      ↑
StripePayment
```

The high-level module depends on the abstraction.

---

# 46. DIP vs Dependency Injection

These two are often confused.

## Dependency Inversion Principle

A:

```text
Design Principle
```

It tells us:

```text
Depend on abstractions.
```

## Dependency Injection

A:

```text
Technique
```

used to provide dependencies from outside.

Example:

```java
OrderService(PaymentGateway payment)
```

The constructor receives the dependency.

Therefore:

```text
DIP
→ Principle

DI
→ Technique
```

Dependency Injection can be used to implement a DIP-friendly design.

---

# 47. DIP Recognition Trick

> [!important]
> If the question says:
>
> "High-level module directly depends on a concrete low-level class."
>
> Think:
>
> **Dependency Inversion Principle violation**

If you see:

```java
new ConcreteClass()
```

inside important business logic, investigate whether the dependency should be abstracted.

---

# 48. DIP Shortcut

> [!tip]
> Remember:
>
> ```text
> High Level
>      ↓
> Abstraction
>      ↑
> Low Level
> ```
>
> Not:
>
> ```text
> High Level
>      ↓
> Concrete Detail
> ```

---

# 49. DIP Real-Time Example — Database

Bad:

```java
class UserService {

    private MySQLDatabase database =
        new MySQLDatabase();
}
```

The business logic depends directly on:

```text
MySQL
```

Better:

```java
interface UserRepository {

    void save(User user);
}
```

Implementation:

```java
class MySQLUserRepository
        implements UserRepository {

    public void save(User user) {
        // MySQL
    }
}
```

Service:

```java
class UserService {

    private final UserRepository repository;

    UserService(UserRepository repository) {
        this.repository = repository;
    }
}
```

Now:

```text
UserService
      ↓
UserRepository
      ↑
MySQLUserRepository
```

---

# 50. DIP Real-Time Example — Logging

Bad:

```java
class OrderService {

    private FileLogger logger =
        new FileLogger();
}
```

Better:

```java
interface Logger {

    void log(String message);
}
```

Implementations:

```text
FileLogger
ConsoleLogger
DatabaseLogger
CloudLogger
```

The business logic depends on:

```text
Logger
```

not:

```text
FileLogger
```

---

# 51. DIP Real-Time Example — Notification

```text
NotificationService
          |
          ↓
     Notifier
      /   |   \
     /    |    \
 Email    SMS   Push
```

New notification implementation can be added without changing the high-level service.

This supports:

```text
DIP
OCP
Low Coupling
Polymorphism
```

Several SOLID principles often work together.

---

# 52. SOLID Principles Work Together

The principles are not isolated.

Example:

```text
DIP
 ↓
Depend on Interface
 ↓
OCP
 ↓
Add New Implementations
 ↓
Polymorphism
 ↓
Lower Concrete Coupling
```

Another:

```text
SRP
 ↓
Focused Class
 ↓
High Cohesion
```

Another:

```text
ISP
 ↓
Small Interfaces
 ↓
Less Unnecessary Dependency
 ↓
Lower Coupling
```

Another:

```text
LSP
 ↓
Safe Substitution
 ↓
Reliable Polymorphism
```

---

# 53. SOLID Complete Example — Payment System

Suppose we need:

```text
Credit Card
UPI
PayPal
```

## Step 1 — Abstraction

```java
interface PaymentGateway {

    void pay(double amount);
}
```

## Step 2 — Implementations

```java
class CardPayment
        implements PaymentGateway {

    public void pay(double amount) {
        // card payment
    }
}
```

```java
class UpiPayment
        implements PaymentGateway {

    public void pay(double amount) {
        // UPI payment
    }
}
```

```java
class PaypalPayment
        implements PaymentGateway {

    public void pay(double amount) {
        // PayPal payment
    }
}
```

## Step 3 — High-Level Service

```java
class OrderService {

    private final PaymentGateway payment;

    OrderService(PaymentGateway payment) {
        this.payment = payment;
    }

    void checkout(double amount) {
        payment.pay(amount);
    }
}
```

Now:

```text
OrderService
      ↓
PaymentGateway
      ↑
 +----+----+----+
 |    |    |    |
Card UPI PayPal ...
```

Benefits:

```text
DIP
OCP
Polymorphism
Low Coupling
High Cohesion
```

---

# 54. SOLID Complete Example — Notification System

Bad:

```java
class NotificationService {

    void send(String type, String message) {

        if (type.equals("EMAIL")) {
            // email
        }

        else if (type.equals("SMS")) {
            // SMS
        }

        else if (type.equals("PUSH")) {
            // push
        }
    }
}
```

Problems:

```text
OCP concern
High branching
Growing modification cost
Concrete behavior mixed together
```

Better:

```java
interface Notification {

    void send(String message);
}
```

Implement:

```text
EmailNotification
SmsNotification
PushNotification
```

Service:

```java
class NotificationService {

    private final Notification notification;

    NotificationService(Notification notification) {
        this.notification = notification;
    }

    void send(String message) {
        notification.send(message);
    }
}
```

Now:

```text
DIP
+
OCP
+
Polymorphism
+
Low Coupling
```

---

# 55. SOLID Complete Example — Employee System

Bad:

```java
class EmployeeManager {

    void calculateSalary() {
    }

    void saveEmployee() {
    }

    void generateReport() {
    }

    void sendEmail() {
    }

    void exportExcel() {
    }
}
```

Problems:

```text
SRP violation
Low Cohesion
Potential High Coupling
```

Refactor:

```text
SalaryService
EmployeeRepository
ReportService
EmailService
ExcelExporter
```

Now each component has a focused role.

---

# 56. SOLID Complete Example — Shape System

Suppose:

```java
interface Shape {

    double area();
}
```

Implementations:

```java
class Circle implements Shape {

    public double area() {
        return 0;
    }
}
```

```java
class Rectangle implements Shape {

    public double area() {
        return 0;
    }
}
```

Now:

```java
class AreaCalculator {

    double calculate(Shape shape) {
        return shape.area();
    }
}
```

Adding:

```text
Triangle
Pentagon
Hexagon
```

can be done through new implementations.

This demonstrates:

```text
OCP
DIP
Polymorphism
```

provided the abstraction remains appropriate.

---

# 57. SOLID and Design Patterns

SOLID principles often lead naturally to design patterns.

Examples:

| Principle | Common Supporting Patterns |
|---|---|
| SRP | Facade, Command, Observer |
| OCP | Strategy, Decorator, Factory |
| LSP | Strategy, Template Method |
| ISP | Adapter, Role-based interfaces |
| DIP | Dependency Injection, Factory, Strategy |

These are not strict one-to-one relationships.

A pattern does not automatically make code SOLID.

The design intent matters.

---

# 58. SOLID and Clean Code

SOLID encourages:

```text
Small focused classes
Meaningful abstractions
Explicit dependencies
Replaceable implementations
Controlled responsibilities
```

This generally improves:

```text
Readability
Maintainability
Testability
Extensibility
```

---

# 59. SOLID and Unit Testing

### SRP

Focused class:

```text
Easy to test
```

### DIP

Dependencies can be replaced with:

```text
Mocks
Stubs
Fakes
```

### ISP

Tests depend on smaller contracts.

### LSP

Different implementations can be substituted.

### OCP

New implementations can be tested independently.

Therefore SOLID often improves testability.

---

# 60. SOLID and Mocking

Suppose:

```java
class OrderService {

    private final PaymentGateway gateway;

    OrderService(PaymentGateway gateway) {
        this.gateway = gateway;
    }
}
```

During testing:

```text
Real Payment Gateway
        ↓
     replaced by
        ↓
Mock Payment Gateway
```

This is easier because the dependency is expressed through an abstraction.

This is a major practical benefit of DIP.

---

# 61. SOLID and Microservices

SOLID principles apply at multiple scales.

Class level:

```text
Class
```

Module level:

```text
Package
```

Service level:

```text
Microservice
```

Example:

```text
PaymentService
```

should not become:

```text
Payment + Authentication + Analytics + Email + Inventory
```

A focused service boundary improves cohesion.

---

# 62. SOLID and APIs

Good API design often uses:

```text
Stable contracts
Small interfaces
Clear responsibilities
Hidden implementation details
```

This connects directly with:

```text
OCP
ISP
DIP
Encapsulation
Abstraction
```

---

# 63. SOLID and Database Architecture

A service should ideally not force unrelated components to know its internal database implementation.

Instead:

```text
Business Logic
      ↓
Repository Interface
      ↑
Database Implementation
```

This supports:

```text
DIP
Low Coupling
Testability
```

---

# 64. SOLID and Composition Over Inheritance

A common design guideline is:

> Prefer composition over inheritance when composition provides more flexibility.

Inheritance creates a strong relationship:

```text
Child
  ↓
Parent
```

Composition:

```text
Class
  |
  +-- Component A
  +-- Component B
```

Composition can make behavior easier to replace.

This can support:

```text
OCP
DIP
Low Coupling
```

---

# 65. Interview Pattern Recognition Table

| Question Clue | Think |
|---|---|
| One reason to change | SRP |
| Multiple unrelated responsibilities | SRP violation |
| Add feature without modifying stable code | OCP |
| Huge if-else for types | Possible OCP problem |
| Subclass breaks parent expectations | LSP |
| Child cannot safely replace parent | LSP |
| Huge interface | ISP |
| Unused interface methods | ISP |
| High-level depends on concrete class | DIP |
| Depend on abstraction | DIP |
| Constructor receives dependency | Dependency Injection |
| Focused class | High Cohesion |
| Many dependencies | High Coupling |

---

# 66. Five-Second Recognition Method

When an interview question gives you code, ask these five questions.

```text
1. Does this class do too many unrelated things?
       ↓
      SRP

2. Do I need to modify existing logic for every new type?
       ↓
      OCP

3. Can a child safely replace its parent?
       ↓
      LSP

4. Does a class implement methods it doesn't need?
       ↓
      ISP

5. Does business logic directly create concrete dependencies?
       ↓
      DIP
```

This is one of the fastest ways to identify SOLID questions.

---

# 67. Advanced Shortcut

> [!tip]
> Use the **S-O-L-I-D Question Method**:
>
> **S → "Too many jobs?"**
>
> **O → "Need to modify for every new type?"**
>
> **L → "Can child replace parent?"**
>
> **I → "Forced to implement unused methods?"**
>
> **D → "Depends directly on concrete detail?"**

---

# 68. Common Mistakes

> [!warning] Avoid These

## Mistake 1 — SRP Means One Method

Wrong:

```text
One class = One method
```

Correct:

```text
One cohesive responsibility
```

---

## Mistake 2 — OCP Means Never Modify Code

Wrong:

```text
Existing code can never change.
```

Correct:

```text
Stable behavior should not require constant modification
for every new variation.
```

---

## Mistake 3 — LSP Means Every Child Must Be Identical

Wrong:

```text
Child must behave exactly like Parent.
```

Correct:

```text
Child must honor the behavioral contract expected from Parent.
```

---

## Mistake 4 — ISP Means Every Interface Must Have One Method

Wrong:

```text
Every interface must contain exactly one method.
```

Correct:

```text
Interfaces should be focused and clients should not depend
on methods they do not need.
```

---

## Mistake 5 — DIP Means Dependency Injection

Not exactly.

```text
DIP
→ Principle

DI
→ Technique
```

---

## Mistake 6 — Interface Automatically Means SOLID

Using an interface does not automatically make a design good.

You must ask:

```text
Is the abstraction meaningful?
Is it stable?
Is it focused?
Does it reduce unnecessary dependency?
```

---

## Mistake 7 — More Classes Always Means Better Design

Not necessarily.

Too many classes can create:

```text
Overengineering
Excessive indirection
Complexity
```

Use meaningful boundaries.

---

## Mistake 8 — OCP Means Never Using If Statements

Not every `if` violates OCP.

The problem occurs when a design repeatedly requires modification for every new variation.

---

## Mistake 9 — LSP Is Only About Inheritance Syntax

No.

LSP is primarily about:

```text
Behavioral substitutability
```

---

## Mistake 10 — SOLID Is a Strict Coding Law

SOLID principles are design guidelines.

Real systems require balancing:

```text
Simplicity
Performance
Maintainability
Flexibility
Business Requirements
```

---

# 69. Advanced Interview Questions

## Q1. What is SOLID?

**Answer:**

> SOLID is a set of five object-oriented design principles: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion. They help create maintainable, extensible, testable, and loosely coupled software.

---

## Q2. Which SOLID principle is related to high cohesion?

**Answer:**

> SRP strongly supports high cohesion because it encourages classes to contain closely related responsibilities.

---

## Q3. Which principle is most directly related to abstractions?

**Answer:**

> Dependency Inversion Principle strongly emphasizes depending on abstractions rather than concrete implementations.

---

## Q4. Which principle helps avoid large interfaces?

**Answer:**

```text
Interface Segregation Principle
```

---

## Q5. Which principle deals with safe inheritance?

**Answer:**

```text
Liskov Substitution Principle
```

---

## Q6. Which principle supports adding new behavior without repeatedly changing existing code?

**Answer:**

```text
Open/Closed Principle
```

---

## Q7. What is the relationship between SRP and cohesion?

**Answer:**

> SRP encourages related responsibilities to remain together, which generally increases cohesion.

---

## Q8. What is the relationship between DIP and Dependency Injection?

**Answer:**

> DIP is a design principle, while Dependency Injection is a technique for supplying dependencies from outside. DI can be used to implement a DIP-friendly design.

---

## Q9. Why is LSP important?

**Answer:**

> LSP ensures that polymorphism remains safe by requiring subtypes to preserve the behavioral expectations of their parent abstractions.

---

## Q10. Why is ISP useful?

**Answer:**

> ISP prevents clients from being forced to depend on methods they do not use, reducing unnecessary coupling.

---

## Q11. Can one class violate multiple SOLID principles?

Yes.

Example:

```java
class OrderManager {

    void processPayment() {
    }

    void sendEmail() {
    }

    void saveToDatabase() {
    }

    void generatePDF() {
    }
}
```

Possible issues:

```text
SRP violation
Low Cohesion
Potential DIP violation
Potential OCP problems
```

SOLID principles often overlap.

---

# 70. Advanced Scenario-Based Questions

## Scenario 1

```java
class ReportService {

    void generatePDF() {
    }

    void sendEmail() {
    }

    void saveDatabase() {
    }
}
```

### Question

Which principle is most obviously violated?

### Recognition

Multiple unrelated responsibilities.

### Answer

```text
SRP
```

---

## Scenario 2

```java
class PaymentService {

    void pay(String type) {

        if (type.equals("CARD")) {
        }
        else if (type.equals("UPI")) {
        }
        else if (type.equals("PAYPAL")) {
        }
    }
}
```

### Question

Adding every payment method requires modifying the class. Which principle is relevant?

### Answer

```text
OCP
```

Possible improvement:

```text
Payment Interface
+
Polymorphic Implementations
```

---

## Scenario 3

```java
class Bird {

    void fly() {
    }
}

class Penguin extends Bird {

    @Override
    void fly() {
        throw new UnsupportedOperationException();
    }
}
```

### Question

What principle is potentially violated?

### Answer

```text
LSP
```

The abstraction incorrectly assumes all birds can fly.

Better:

```text
Bird
 |
 +-- FlyingBird
 |
 +-- NonFlyingBird
```

or use capability-based interfaces.

---

## Scenario 4

```java
interface Machine {

    void print();
    void scan();
    void fax();
}
```

A basic printer only supports:

```text
print()
```

### Answer

```text
ISP
```

Split the interface into focused capabilities.

---

## Scenario 5

```java
class OrderService {

    private MySQLDatabase database =
        new MySQLDatabase();
}
```

### Question

What principle is relevant?

### Answer

```text
DIP
```

Use:

```text
Repository abstraction
+
Dependency Injection
```

---

# 71. Advanced Design Exercise

Suppose we have:

```java
class ECommerceSystem {

    void createOrder() {
    }

    void processPayment() {
    }

    void sendEmail() {
    }

    void generateInvoice() {
    }

    void saveToDatabase() {
    }
}
```

Analyze it.

### Step 1 — SRP

Multiple responsibilities:

```text
Order
Payment
Email
Invoice
Persistence
```

Therefore:

```text
SRP problem
```

### Step 2 — Cohesion

Responsibilities are unrelated.

Therefore:

```text
Low Cohesion
```

### Step 3 — Coupling

If the class directly creates:

```text
StripePayment
MySQLDatabase
GmailService
```

then:

```text
High Coupling
```

### Step 4 — Refactor

Create:

```text
OrderService
PaymentService
NotificationService
InvoiceService
OrderRepository
```

### Step 5 — Abstraction

Use:

```text
PaymentGateway
Notification
OrderRepository
```

### Step 6 — Dependency Injection

Inject dependencies:

```java
OrderService(
    PaymentGateway payment,
    Notification notification,
    OrderRepository repository
)
```

Result:

```text
SRP
+
DIP
+
High Cohesion
+
Lower Coupling
```

---

# 72. SOLID Cheat Sheet

```text
S
Single Responsibility Principle

Question:
"How many reasons can this class change?"

Answer:
One primary responsibility.


O
Open/Closed Principle

Question:
"Can I add behavior without repeatedly changing stable code?"

Answer:
Extend rather than constantly modify.


L
Liskov Substitution Principle

Question:
"Can Child safely replace Parent?"

Answer:
Yes, without breaking expected behavior.


I
Interface Segregation Principle

Question:
"Is the client forced to depend on unused methods?"

Answer:
If yes, split the interface.


D
Dependency Inversion Principle

Question:
"Does high-level business logic depend directly on concrete details?"

Answer:
Use abstractions.
```

---

# 73. SOLID vs OOP Concepts

| Concept | Main Purpose |
|---|---|
| Encapsulation | Hide internal state/details |
| Abstraction | Expose essential behavior |
| Inheritance | Reuse/derive behavior and contracts |
| Polymorphism | Use different implementations through common abstractions |
| SOLID | Guide maintainable object-oriented design |

SOLID builds on OOP concepts.

---

# 74. SOLID vs Coupling and Cohesion

| Concept | Meaning |
|---|---|
| Coupling | Dependency between modules |
| Cohesion | Relatedness within a module |
| SOLID | Design principles that help improve structure |

Important relationship:

```text
SOLID
  ↓
High Cohesion
+
Low Coupling
```

---

# 75. Interview Comparison Table

| Principle | Main Problem | Main Solution |
|---|---|---|
| SRP | Too many responsibilities | Split responsibilities |
| OCP | Constant modification for new behavior | Extend through abstractions/polymorphism |
| LSP | Broken subtype behavior | Design valid substitutable abstractions |
| ISP | Huge interfaces | Split into focused interfaces |
| DIP | High-level depends on concrete detail | Depend on abstractions |

---

# 76. Master Recognition Tree

```text
                 SOLID QUESTION
                       |
       +---------------+---------------+
       |               |               |
       ↓               ↓               ↓
   Class issue     Extension issue   Inheritance
       |               |               |
       ↓               ↓               ↓
      SRP             OCP             LSP
       |
       |
       +-----------------------+
                               |
                         Interface issue
                               |
                               ↓
                              ISP

                         Dependency issue
                               |
                               ↓
                              DIP
```

---

# 77. Five-Second Interview Trick

When you read the code, look for the strongest clue.

```text
TOO MANY JOBS
→ S

NEW TYPE REQUIRES OLD CODE CHANGE
→ O

CHILD BREAKS PARENT EXPECTATION
→ L

UNUSED INTERFACE METHODS
→ I

CONCRETE DEPENDENCY IN BUSINESS LOGIC
→ D
```

---

# 78. One-Line Memory

> [!tip]
> **S = Single Job**
>
> **O = Open to Extend**
>
> **L = Legitimate Substitute**
>
> **I = Interfaces Split**
>
> **D = Depend on Abstraction**

---

# 79. Interview-Level Answer Template

If asked:

> "How do SOLID principles improve software design?"

Use:

> SOLID principles help organize object-oriented software around focused responsibilities, safe extension, valid substitution, small interfaces, and abstraction-based dependencies. Together they generally improve maintainability, testability, extensibility, and reduce unnecessary coupling.

---

# 80. Common Placement Questions

> [!important] Must Master

1. What does SOLID stand for?
2. Explain SRP.
3. What is the difference between SRP and cohesion?
4. What does Open/Closed mean?
5. How can OCP be implemented in Java?
6. What is LSP?
7. Give a real-world example of LSP violation.
8. Why is the Rectangle-Square example controversial?
9. What is ISP?
10. Why should interfaces be small?
11. What is DIP?
12. DIP vs DI.
13. Interface vs abstract class in relation to SOLID.
14. How does polymorphism support OCP?
15. How does abstraction support DIP?
16. How does SRP improve cohesion?
17. How does ISP reduce coupling?
18. What is a God Class?
19. How do you refactor a God Class?
20. Can a class violate multiple SOLID principles?
21. Does SOLID mean zero coupling?
22. Does SOLID always require interfaces?
23. Does SRP mean one method per class?
24. Does OCP mean code can never be modified?
25. Is inheritance always compatible with LSP?
26. What happens when an interface has too many methods?
27. Why is dependency injection useful?
28. How does SOLID help unit testing?
29. How does SOLID apply to microservices?
30. How does SOLID improve maintainability?

---

# 81. Golden Interview Examples

## Example A

```text
One class:
Login + Payment + Email + Database
```

Answer:

```text
SRP violation
+
Low Cohesion
```

---

## Example B

```text
Every new payment type requires editing if-else logic.
```

Answer:

```text
OCP concern
```

---

## Example C

```text
Child class throws UnsupportedOperationException
for a method promised by the parent abstraction.
```

Answer:

```text
LSP concern
```

---

## Example D

```text
Class implements 15 methods but uses only 3.
```

Answer:

```text
ISP concern
```

---

## Example E

```text
OrderService creates MySQLRepository directly.
```

Answer:

```text
DIP concern
```

---

# 82. Real-World Architecture Pattern

A practical SOLID-oriented architecture can look like:

```text
              Presentation Layer
                      |
                      ↓
              Application Layer
                      |
                      ↓
               Domain Abstraction
                      |
          +-----------+-----------+
          |                       |
          ↓                       ↓
     Repository              Payment Gateway
     Interface                  Interface
          ↑                       ↑
          |                       |
     MySQL Impl               Stripe Impl
```

The important idea is:

```text
Business Logic
      ↓
Stable Abstraction
      ↑
Implementation Detail
```

This keeps implementation details replaceable.

---

# 83. Final Master Notes

## S — Single Responsibility

```text
One primary responsibility
One primary reason to change
```

Main danger:

```text
God Class
```

---

## O — Open/Closed

```text
Open for Extension
Closed for Modification
```

Main danger:

```text
Constant modification of stable code
```

---

## L — Liskov Substitution

```text
Subtype must preserve expected behavior
```

Main danger:

```text
Broken inheritance contract
```

---

## I — Interface Segregation

```text
Clients should not depend on unused methods
```

Main danger:

```text
Fat Interface
```

---

## D — Dependency Inversion

```text
High-level code
      ↓
Abstraction
      ↑
Low-level implementation
```

Main danger:

```text
Direct concrete dependency
```

---

# 84. Quick Revision

> [!summary] One-Minute Revision

```text
SOLID
=
Five OOP Design Principles
```

### S

```text
Single Responsibility
→ One primary responsibility
→ One primary reason to change
```

### O

```text
Open/Closed
→ Open for extension
→ Closed for unnecessary modification
```

### L

```text
Liskov Substitution
→ Child should safely substitute Parent
→ Preserve behavioral contract
```

### I

```text
Interface Segregation
→ Do not force clients to depend on unused methods
→ Prefer focused interfaces
```

### D

```text
Dependency Inversion
→ High-level modules depend on abstractions
→ Low-level details implement abstractions
```

### Master Memory

```text
S → Single Job
O → Extend
L → Substitute
I → Split Interfaces
D → Abstraction
```

### Common Clues

```text
Too many responsibilities
→ SRP

New feature requires modifying old branching code
→ OCP

Child breaks parent expectations
→ LSP

Unused interface methods
→ ISP

Concrete dependency inside business logic
→ DIP
```

### Overall Goal

```text
SOLID
   ↓
High Cohesion
+
Low Coupling
+
Maintainability
+
Testability
+
Extensibility
```

---

# 85. Golden Memory Trick

**S = Single Job, O = Open to Extension, L = Legitimate Substitute, I = Interfaces Split, D = Depend on Abstraction.**

# 86. One-Line Recognition

**If the problem is about responsibility think S, extension think O, substitution think L, interfaces think I, and dependencies/abstraction think D.**