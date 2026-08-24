---
type: concept
subject: aptitude
topic: "Coupling and Cohesion"
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
  - coupling
  - cohesion
  - low-coupling
  - high-cohesion
  - software-design
  - solid
  - clean-code
  - system-design
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Association]]"
  - "[[Aggregation]]"
  - "[[Composition]]"
  - "[[SOLID Principles]]"
  - "[[Abstraction]]"
  - "[[Encapsulation]]"
---

# Coupling and Cohesion

> [!summary]
> **Coupling measures how strongly different modules/classes depend on each other, while Cohesion measures how closely the responsibilities inside one module/class belong together.**
>
> Ideal OOP design:
>
> **Low Coupling + High Cohesion**
>
> Memory:
>
> **Coupling → BETWEEN**
>
> **Cohesion → WITHIN**

---

# 1. Core Concept

Coupling and Cohesion are two fundamental software-design concepts.

They help us answer two different questions.

## Coupling

Ask:

> "How much does Class A depend on Class B?"

Therefore:

**Coupling → dependency BETWEEN modules/classes**

Example:

```text
Class A
   |
   | depends heavily on
   ↓
Class B
```

This represents **high coupling**.

---

## Cohesion

Ask:

> "How closely related are the responsibilities inside one class?"

Example:

```text
StudentService

addStudent()
removeStudent()
updateStudent()
findStudent()
```

All methods are related to student management.

Therefore:

**High Cohesion**

---

# 2. Basic Meaning

## Coupling

Coupling is the degree of dependency between software modules.

Example:

```text
OrderService
      |
      ↓
StripePayment
```

If `OrderService` directly depends on a specific implementation such as `StripePayment`, changing the payment implementation may require changes in `OrderService`.

Therefore:

**High Coupling**

---

## Cohesion

Cohesion is the degree to which the responsibilities inside a module belong together.

Example:

```text
StudentService

addStudent()
removeStudent()
updateStudent()
findStudent()
```

All responsibilities are related.

Therefore:

**High Cohesion**

Bad example:

```text
StudentService

addStudent()
sendEmail()
resizeImage()
calculateTax()
generatePDF()
```

These responsibilities are unrelated.

Therefore:

**Low Cohesion**

---

# 3. Main Formula

There is no universal mathematical formula for Coupling and Cohesion.

Use these conceptual formulas:

$$
\boxed{
Coupling = Dependency\ Between\ Modules
}
$$

$$
\boxed{
Cohesion = Relatedness\ Within\ a\ Module
}
$$

Ideal design:

$$
\boxed{
Good\ Design = Low\ Coupling + High\ Cohesion
}
$$

Memory:

$$
\boxed{
Coupling \rightarrow BETWEEN
}
$$

$$
\boxed{
Cohesion \rightarrow WITHIN
}
$$

---

# 4. Important Properties

| Property | Coupling | Cohesion |
|---|---|---|
| Measures | Dependency | Relatedness |
| Scope | Between modules | Within module |
| Main question | How dependent are modules? | How related are responsibilities? |
| Preferred level | Low | High |
| Main benefit | Flexibility | Maintainability |
| Poor design | High coupling | Low cohesion |
| Memory | BETWEEN | WITHIN |

> [!important]
> **Coupling = BETWEEN**
>
> **Cohesion = WITHIN**

This is the most important rule in the entire topic.

---

# 5. Why Low Coupling Is Preferred

Suppose:

```text
OrderService
     |
     +── MySQLDatabase
     +── StripePayment
     +── GmailService
     +── PDFGenerator
```

`OrderService` directly depends on many concrete implementations.

If one implementation changes, `OrderService` may also need modification.

This creates:

**High Coupling**

A better design is:

```text
OrderService
     |
     +── OrderRepository
     +── PaymentGateway
     +── NotificationService
     +── ReportGenerator
```

These can be interfaces or abstractions.

Now implementation details can change independently.

This gives:

**Lower Coupling**

---

# 6. Why High Cohesion Is Preferred

Bad class:

```text
ApplicationManager

login()
calculateSalary()
sendEmail()
resizeImage()
generatePDF()
connectDatabase()
processPayment()
```

The class has too many unrelated responsibilities.

Therefore:

**Low Cohesion**

Better:

```text
AuthenticationService
PayrollService
EmailService
ImageService
ReportService
PaymentService
```

Each class has a focused purpose.

Therefore:

**Higher Cohesion**

---

# 7. Golden Design Rule

> [!important]
> **High Cohesion + Low Coupling = Good Software Design**

Why?

### High Cohesion

Means:

- Focused classes
- Clear responsibilities
- Easier maintenance
- Easier testing
- Better readability

### Low Coupling

Means:

- Fewer unnecessary dependencies
- Easier modification
- Better flexibility
- Easier replacement
- Reduced change impact

Together:

```text
High Cohesion
      +
Low Coupling
      ↓
Good Design
```

---

# 8. Real-Life Analogy

Imagine a restaurant.

## High Cohesion

The kitchen team handles:

- Food preparation
- Cooking
- Plating

These responsibilities belong together.

Therefore:

**High Cohesion**

## Low Coupling

The kitchen should not depend directly on one specific:

- Bank
- Delivery company
- Payment machine
- Supplier

Instead, it should communicate through defined contracts.

Therefore:

**Lower Coupling**

---

# 9. Another Real-Life Analogy

Think about a smartphone.

A smartphone contains:

```text
Camera
Battery
Display
Processor
Speaker
Storage
```

Each component has a focused responsibility.

Therefore:

**High Cohesion**

The components communicate through controlled interfaces.

Therefore:

**Controlled Coupling**

A good system consists of:

```text
Focused Components
        +
Controlled Dependencies
```

---

# 10. Recognition Tricks

> [!important]
> If the question says:
>
> "How dependent are two modules?"
>
> Think:
>
> **Coupling**

> [!important]
> If the question says:
>
> "How closely related are responsibilities inside a module?"
>
> Think:
>
> **Cohesion**

> [!important]
> If the question says:
>
> "What is the ideal software design?"
>
> Think:
>
> **Low Coupling + High Cohesion**

---

# 11. Fastest Memory Trick

> [!tip]
> **Coupling → Outside**
>
> **Cohesion → Inside**
>
> Another memory:
>
> **Coupling connects modules.**
>
> **Cohesion keeps responsibilities together.**

---

# 12. Types of Coupling

A commonly taught classification is:

1. Message Coupling
2. Data Coupling
3. Stamp Coupling
4. Control Coupling
5. External Coupling
6. Common Coupling
7. Content Coupling

Different textbooks may classify or order these slightly differently.

For interviews, remember the central principle:

```text
Less unnecessary dependency
        ↓
Lower Coupling
        ↓
Better Modularity
```

---

# 13. Message Coupling

Message coupling is generally considered very low coupling.

Modules communicate through:

- Messages
- Interfaces
- Public contracts

without depending on internal implementation.

Example:

```java
interface PaymentGateway {

    void pay(double amount);
}

class OrderService {

    private final PaymentGateway gateway;

    OrderService(PaymentGateway gateway) {
        this.gateway = gateway;
    }

    void placeOrder(double amount) {
        gateway.pay(amount);
    }
}
```

`OrderService` knows about:

```text
PaymentGateway
```

but does not need to know whether the implementation is:

```text
Stripe
Razorpay
PayPal
UPI
```

This reduces concrete implementation coupling.

---

# 14. Data Coupling

Data coupling occurs when one module passes only the required data to another module.

Example:

```java
class TaxCalculator {

    double calculateTax(double income) {
        return income * 0.10;
    }
}

class PayrollService {

    private final TaxCalculator calculator;

    PayrollService(TaxCalculator calculator) {
        this.calculator = calculator;
    }

    double calculateTax(double income) {
        return calculator.calculateTax(income);
    }
}
```

Only the required value is passed:

```text
income
```

The receiving method does not receive unnecessary data.

Therefore:

**Data Coupling**

---

# 15. Stamp Coupling

Stamp coupling occurs when a complete data structure is passed even though the receiving module uses only a portion of it.

Example:

```java
class Employee {

    String name;
    String department;
    double salary;
    String address;
    String phone;
}
```

Suppose:

```java
void printName(Employee employee) {
    System.out.println(employee.name);
}
```

The method only needs:

```text
name
```

but receives:

```text
Entire Employee object
```

This creates dependency on the structure of `Employee`.

A more focused method could be:

```java
void printName(String name) {
    System.out.println(name);
}
```

However:

> [!important]
> Passing an object is not automatically bad.
>
> Object-oriented applications naturally pass domain objects.
>
> The concern is unnecessary dependency on the object's internal structure.

---

# 16. Control Coupling

Control coupling occurs when one module passes information that controls the internal behavior of another module.

Example:

```java
void process(int mode) {

    if (mode == 1) {
        processA();
    }
    else if (mode == 2) {
        processB();
    }
}
```

The caller controls the internal behavior using:

```text
mode
```

This creates:

**Control Coupling**

---

# 17. Control Coupling Example

Bad design:

```java
void generateReport(String type) {

    if (type.equals("PDF")) {
        generatePDF();
    }
    else if (type.equals("EXCEL")) {
        generateExcel();
    }
}
```

The caller needs to know the internal options:

```text
PDF
EXCEL
```

A better design can use polymorphism.

```java
interface ReportGenerator {

    void generate();
}
```

Then:

```java
class PdfReportGenerator
        implements ReportGenerator {

    public void generate() {
        // PDF logic
    }
}
```

and:

```java
class ExcelReportGenerator
        implements ReportGenerator {

    public void generate() {
        // Excel logic
    }
}
```

Now the client depends on:

```text
ReportGenerator
```

rather than controlling internal behavior with flags.

---

# 18. External Coupling

External coupling occurs when modules depend on externally imposed:

- Protocols
- Formats
- Devices
- APIs
- Operating systems
- Databases
- External services

Examples:

```text
HTTP
JSON
SQL
REST API
Payment API
Operating System API
```

External coupling cannot always be eliminated.

The goal is to isolate it.

Useful techniques:

```text
Interfaces
Adapters
Wrappers
Gateways
Facade
```

---

# 19. Adapter Pattern and Coupling

Suppose:

```text
Application
     |
     ↓
ExternalPaymentAPI
```

The application is directly coupled to the external API.

Better:

```text
Application
     |
     ↓
PaymentGateway
     |
     ↓
PaymentAdapter
     |
     ↓
ExternalPaymentAPI
```

Now external API details are isolated.

This is an important system-design technique.

---

# 20. Common Coupling

Common coupling occurs when multiple modules share common global data.

Example:

```java
class GlobalData {

    static int count;
}
```

Class A:

```java
class A {

    void update() {
        GlobalData.count++;
    }
}
```

Class B:

```java
class B {

    void reset() {
        GlobalData.count = 0;
    }
}
```

Now:

```text
A
 \
  → GlobalData ← B
```

Both modules depend on shared mutable state.

This creates:

**Common Coupling**

---

# 21. Why Global State Is Dangerous

Shared mutable global state can cause:

- Unexpected side effects
- Difficult debugging
- Hidden dependencies
- Race conditions
- Testing problems
- Order-dependent behavior

Therefore:

> [!warning]
> Avoid unnecessary shared mutable global state.

Prefer:

```text
Encapsulation
Dependency Injection
Immutable Objects
Explicit Dependencies
```

---

# 22. Content Coupling

Content coupling is very strong coupling.

It occurs when one module directly accesses or modifies the internal implementation details of another module.

Conceptually:

```text
Module A
    |
    ↓
directly accesses
    |
    ↓
internals of Module B
```

Example:

```java
class B {

    int value;
}

class A {

    void change(B b) {
        b.value = 100;
    }
}
```

Class A depends directly on the internal representation of B.

Better:

```java
class B {

    private int value;

    void setValue(int value) {
        this.value = value;
    }
}
```

Now B controls its own state.

This supports:

```text
Encapsulation
Information Hiding
Lower Coupling
```

---

# 23. Coupling Hierarchy Memory

A commonly taught order from lower/better to higher/worse is:

```text
Message
   ↓
Data
   ↓
Stamp
   ↓
Control
   ↓
External
   ↓
Common
   ↓
Content
```

Memory:

> [!tip]
> **M D S C E C C**
>
> Message
> Data
> Stamp
> Control
> External
> Common
> Content

Important:

> Different textbooks may use slightly different classifications or ordering. Focus first on the principle that unnecessary dependency should be minimized.

---

# 24. Types of Cohesion

A commonly taught classification from weaker/lower cohesion to stronger/higher cohesion is:

1. Coincidental Cohesion
2. Logical Cohesion
3. Temporal Cohesion
4. Procedural Cohesion
5. Communicational Cohesion
6. Sequential Cohesion
7. Functional Cohesion

The most important interview rule:

```text
Coincidental
→ Weakest

Functional
→ Strongest
```

---

# 25. Coincidental Cohesion

Coincidental cohesion occurs when unrelated responsibilities are placed together.

Example:

```java
class Utility {

    void calculateSalary() {
        // salary
    }

    void resizeImage() {
        // image
    }

    void sendEmail() {
        // email
    }

    void connectDatabase() {
        // database
    }
}
```

These responsibilities are unrelated.

Therefore:

**Low Cohesion**

This is a common code smell.

---

# 26. Logical Cohesion

Logical cohesion occurs when operations are grouped because they belong to the same broad category, even though only one operation may be selected at a time.

Example:

```java
class InputHandler {

    void handle(String type) {

        if (type.equals("KEYBOARD")) {
            // keyboard input
        }
        else if (type.equals("MOUSE")) {
            // mouse input
        }
    }
}
```

Both are related to:

```text
Input
```

but perform different operations.

Therefore:

**Logical Cohesion**

---

# 27. Temporal Cohesion

Temporal cohesion occurs when operations are grouped because they happen at the same time.

Example:

```java
void startup() {

    loadConfiguration();
    connectDatabase();
    initializeCache();
    initializeLogging();
}
```

All operations happen during:

```text
Application Startup
```

Therefore:

**Temporal Cohesion**

Recognition:

> [!important]
> If the clue is **"same time"**, think **Temporal Cohesion**.

---

# 28. Procedural Cohesion

Procedural cohesion occurs when elements are grouped because they follow a particular execution sequence or procedure.

Example:

```java
void processOrder() {

    validateOrder();
    calculateTotal();
    saveOrder();
    sendNotification();
}
```

The operations are connected through the sequence:

```text
Validate
   ↓
Calculate
   ↓
Save
   ↓
Notify
```

Therefore:

**Procedural Cohesion**

Recognition:

> [!important]
> If the clue is **"same procedure/order"**, think **Procedural Cohesion**.

---

# 29. Communicational Cohesion

Communicational cohesion occurs when operations work on the same data.

Example:

```java
void processStudent(Student student) {

    validate(student);
    update(student);
    save(student);
}
```

All operations use:

```text
Same Student object
```

Therefore:

**Communicational Cohesion**

Recognition:

> [!important]
> If the clue is **"same data"**, think **Communicational Cohesion**.

---

# 30. Sequential Cohesion

Sequential cohesion occurs when the output of one operation becomes the input of another.

Pattern:

```text
Read
 ↓
Parse
 ↓
Transform
 ↓
Store
```

Example:

```java
Data read() {
    return readFile();
}

ParsedData parse(Data data) {
    return parser.parse(data);
}

Result transform(ParsedData data) {
    return transformer.transform(data);
}
```

The output flows into the next operation.

Therefore:

**Sequential Cohesion**

Recognition:

> [!important]
> If the clue is **"output of one becomes input of another"**, think **Sequential Cohesion**.

---

# 31. Functional Cohesion

Functional cohesion is generally considered the strongest form of cohesion.

A module performs:

```text
One well-defined task
```

Example:

```java
class TaxCalculator {

    double calculateTax(double income) {
        return income * 0.10;
    }
}
```

The class has one clear purpose:

```text
Calculate Tax
```

Therefore:

**Functional Cohesion**

Recognition:

> [!important]
> If the clue is **"one clear task"**, think **Functional Cohesion**.

---

# 32. Cohesion Hierarchy Memory

Common order:

```text
Coincidental
      ↓
Logical
      ↓
Temporal
      ↓
Procedural
      ↓
Communicational
      ↓
Sequential
      ↓
Functional
```

Memory:

> [!tip]
> **C L T P C S F**
>
> Coincidental
> Logical
> Temporal
> Procedural
> Communicational
> Sequential
> Functional

Remember:

```text
Coincidental
→ Weakest

Functional
→ Strongest
```

---

# 33. Coupling vs Cohesion Example

Consider:

```java
class OrderManager {

    void createOrder() {
        // order logic
    }

    void cancelOrder() {
        // order logic
    }

    void sendEmail() {
        // email logic
    }

    void generatePDF() {
        // PDF logic
    }

    void calculateTax() {
        // tax logic
    }
}
```

There are two major problems.

### Problem 1

The class contains unrelated responsibilities.

Therefore:

```text
Low Cohesion
```

### Problem 2

The class may depend on many unrelated external systems.

Therefore:

```text
High Coupling
```

This is poor design.

---

# 34. Refactoring the Example

Instead:

```java
class OrderService {

    void createOrder() {
        // order logic
    }

    void cancelOrder() {
        // order logic
    }
}
```

Then:

```java
class EmailService {

    void sendEmail() {
        // email logic
    }
}
```

Then:

```java
class PdfService {

    void generatePDF() {
        // PDF logic
    }
}
```

Then:

```java
class TaxCalculator {

    double calculateTax(double amount) {
        return amount * 0.10;
    }
}
```

Now each class has a focused responsibility.

Therefore:

```text
Higher Cohesion
```

---

# 35. High Cohesion Example

```java
class StudentService {

    void addStudent(Student student) {
        // add
    }

    void updateStudent(Student student) {
        // update
    }

    void deleteStudent(int id) {
        // delete
    }

    Student findStudent(int id) {
        // find
        return null;
    }
}
```

All methods deal with:

```text
Student Management
```

Therefore:

**High Cohesion**

---

# 36. Low Cohesion Example

```java
class StudentService {

    void addStudent() {
        // student
    }

    void calculateElectricityBill() {
        // electricity
    }

    void resizeImage() {
        // image
    }

    void sendSMS() {
        // SMS
    }
}
```

Responsibilities are unrelated.

Therefore:

**Low Cohesion**

---

# 37. High Coupling Example

```java
class OrderService {

    private MySQLDatabase database =
        new MySQLDatabase();

    private StripePayment payment =
        new StripePayment();

    private GmailService email =
        new GmailService();
}
```

`OrderService` is directly tied to:

```text
MySQL
Stripe
Gmail
```

Changing implementations may require changing `OrderService`.

Therefore:

**High Coupling**

---

# 38. Lower Coupling With Interfaces

Better:

```java
interface PaymentGateway {

    void pay(double amount);
}
```

```java
interface EmailService {

    void send(String message);
}
```

```java
interface OrderRepository {

    void save(Order order);
}
```

Then:

```java
class OrderService {

    private final PaymentGateway payment;
    private final EmailService email;
    private final OrderRepository repository;

    OrderService(
        PaymentGateway payment,
        EmailService email,
        OrderRepository repository
    ) {
        this.payment = payment;
        this.email = email;
        this.repository = repository;
    }
}
```

Now `OrderService` depends on abstractions instead of concrete implementations.

This generally reduces concrete coupling.

---

# 39. Coupling and Abstraction

Abstraction can reduce coupling.

Without abstraction:

```text
OrderService
     |
     ↓
StripePayment
```

With abstraction:

```text
OrderService
     |
     ↓
PaymentGateway
    /      \
Stripe     UPI
```

Now `OrderService` does not need to know which concrete payment implementation is used.

This is a major OOP design principle.

---

# 40. Coupling and Polymorphism

Polymorphism can help reduce concrete coupling.

Example:

```java
interface Notification {

    void send(String message);
}
```

Implementation:

```java
class EmailNotification
        implements Notification {

    public void send(String message) {
        // email
    }
}
```

Another implementation:

```java
class SMSNotification
        implements Notification {

    public void send(String message) {
        // SMS
    }
}
```

Client:

```java
class NotificationService {

    private final Notification notification;

    NotificationService(
        Notification notification
    ) {
        this.notification = notification;
    }
}
```

The client depends on:

```text
Notification
```

rather than:

```text
EmailNotification
```

This reduces concrete implementation coupling.

---

# 41. Coupling and Dependency Injection

Without Dependency Injection:

```java
class OrderService {

    private PaymentService payment =
        new PaymentService();
}
```

The class creates its dependency.

With Dependency Injection:

```java
class OrderService {

    private final PaymentService payment;

    OrderService(PaymentService payment) {
        this.payment = payment;
    }
}
```

Now the dependency is supplied from outside.

Benefits:

- Easier testing
- Easier replacement
- Lower concrete coupling
- Clearer dependencies
- Better flexibility

---

# 42. Coupling and Encapsulation

Encapsulation hides internal implementation.

Example:

```java
class BankAccount {

    private double balance;

    public void deposit(double amount) {

        if (amount > 0) {
            balance += amount;
        }
    }
}
```

Other classes cannot directly manipulate:

```text
balance
```

Instead:

```text
External Class
      ↓
public method
      ↓
internal state
```

This reduces coupling to internal representation.

---

# 43. Coupling and Information Hiding

Information hiding means:

```text
Hide implementation details
```

Example:

```java
class PaymentService {

    public void pay(double amount) {

        validate(amount);
        processPayment(amount);
        recordTransaction(amount);
    }

    private void validate(double amount) {
        // internal
    }

    private void processPayment(double amount) {
        // internal
    }

    private void recordTransaction(double amount) {
        // internal
    }
}
```

Clients only need:

```text
pay()
```

They do not need to know:

```text
How validation works
How payment works
How transaction recording works
```

This reduces unnecessary coupling.

---

# 44. Coupling and Composition

Composition can help build systems from smaller components.

Example:

```text
Car
 |
 +-- Engine
 +-- BrakeSystem
 +-- Transmission
 +-- Navigation
```

Each component can have a focused responsibility.

Therefore:

```text
Composition
     ↓
Modularity
     ↓
Focused Components
```

With well-defined interfaces, dependencies can also be controlled.

---

# 45. Coupling and SOLID

SOLID principles strongly support:

```text
High Cohesion
+
Low Coupling
```

## Single Responsibility Principle

Encourages:

```text
Focused classes
```

Therefore:

```text
High Cohesion
```

## Open/Closed Principle

Encourages extension without unnecessary modification.

## Liskov Substitution Principle

Supports substitutable abstractions.

## Interface Segregation Principle

Prevents clients from depending on methods they do not need.

Therefore:

```text
Less unnecessary coupling
```

## Dependency Inversion Principle

Encourages:

```text
High-level modules
       ↓
Abstraction
       ↑
Low-level implementation
```

This reduces concrete implementation coupling.

---

# 46. Interface Segregation and Coupling

Bad interface:

```java
interface Worker {

    void work();

    void eat();

    void sleep();
}
```

A class may not need all these methods.

Better:

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

Clients depend only on the capabilities they need.

Therefore:

**Lower Unnecessary Coupling**

---

# 47. Cohesion and SRP

Single Responsibility Principle is strongly connected with cohesion.

Bad:

```java
class EmployeeManager {

    void calculateSalary() {
    }

    void generateReport() {
    }

    void sendEmail() {
    }

    void saveToDatabase() {
    }
}
```

Responsibilities include:

```text
Salary
Report
Email
Database
```

These are different reasons to change.

Therefore:

**Low Cohesion**

Better:

```text
PayrollService
ReportService
EmailService
EmployeeRepository
```

Each module has a focused responsibility.

Therefore:

**Higher Cohesion**

---

# 48. Cohesion and Utility Classes

A utility class is not automatically low cohesion.

Example:

```java
class MathUtils {

    static int max(int a, int b) {
        return Math.max(a, b);
    }

    static int min(int a, int b) {
        return Math.min(a, b);
    }

    static int gcd(int a, int b) {
        // logic
        return 0;
    }
}
```

All methods are related to:

```text
Mathematics
```

Therefore:

**Reasonable Cohesion**

But:

```text
MathUtils

max()
sendEmail()
resizeImage()
downloadFile()
```

would have poor cohesion.

---

# 49. Cohesion Through Domain Modeling

A class should represent a meaningful concept.

Good:

```text
Invoice
    |
    +-- calculateTotal()
    +-- addItem()
    +-- removeItem()
```

The operations are invoice-related.

Therefore:

**High Cohesion**

Bad:

```text
MiscUtility
    |
    +-- calculateSalary()
    +-- resizeImage()
    +-- sendEmail()
    +-- calculateTax()
```

The responsibilities are unrelated.

Therefore:

**Low Cohesion**

A useful test:

> "Can I explain what this class is responsible for in one sentence?"

If not, investigate whether the class has low cohesion.

---

# 50. God Class

A **God Class** is a class that knows or does too much.

Example:

```java
class ApplicationManager {

    void login() {
    }

    void calculateSalary() {
    }

    void sendEmail() {
    }

    void generatePDF() {
    }

    void processPayment() {
    }

    void resizeImage() {
    }

    void manageDatabase() {
    }
}
```

Problems:

```text
Low Cohesion
High Coupling
Difficult Testing
Difficult Maintenance
Large Change Impact
```

Refactor into:

```text
AuthenticationService
PayrollService
EmailService
PdfService
PaymentService
ImageService
Repository
```

---

# 51. Feature Envy

Feature Envy occurs when a method is more interested in another object's data than its own object's data.

Example:

```java
class Report {

    double calculate(Invoice invoice) {

        return invoice
            .getCustomer()
            .getAddress()
            .getCity()
            .length();
    }
}
```

The method knows about:

```text
Invoice
Customer
Address
City
```

This can increase coupling.

Possible improvement:

```java
invoice.getCustomerCityName();
```

or move the behavior closer to the data it needs.

This supports:

```text
Encapsulation
Information Hiding
Lower Coupling
```

---

# 52. Law of Demeter

The Law of Demeter is often summarized as:

> **Don't talk to strangers.**

Bad:

```java
order.getCustomer()
     .getAddress()
     .getCity()
     .getName();
```

`order` knows about:

```text
Customer
Address
City
Name
```

This creates a chain of knowledge.

Better design may expose a meaningful method:

```java
order.getCustomerCityName();
```

Now the internal structure is hidden.

The goal is:

```text
Less Knowledge
     ↓
Less Coupling
```

---

# 53. Coupling and Change Impact

Consider:

```text
Class A
   |
   ↓
Class B
   |
   ↓
Class C
   |
   ↓
Class D
```

A change in D may affect:

```text
C
B
A
```

This creates a large:

**Change Impact**

High coupling increases the chance of cascading changes.

Low coupling reduces unnecessary change propagation.

---

# 54. Cohesion and Change Responsibility

Suppose one class contains:

```text
Payment
Email
Reporting
```

A payment change and email change may require modification to the same class.

This indicates:

**Low Cohesion**

Better:

```text
PaymentService
EmailService
ReportingService
```

Now changes are more localized.

---

# 55. Coupling and Testing

High coupling can cause:

- Difficult mocking
- Large test setup
- Difficult isolation
- Fragile tests
- More external dependencies

High cohesion helps:

- Focused unit tests
- Smaller test cases
- Easier debugging
- Easier maintenance

Example:

```text
TaxCalculator
      |
      ↓
calculateTax()
```

This is easy to test.

But:

```text
GodClass
      |
      +-- Database
      +-- Payment
      +-- Email
      +-- File
      +-- Network
      +-- Tax
```

is much harder to test.

---

# 56. Coupling and Microservices

Microservices should avoid unnecessary coupling.

Bad:

```text
Service A
    |
    ↓
Database of Service B
```

Service A directly depends on:

```text
B's table names
B's columns
B's database schema
```

This creates high coupling.

Better:

```text
Service A
    |
    ↓
API / Event
    |
    ↓
Service B
    |
    ↓
Database B
```

Now Service B controls its own data.

---

# 57. Cohesion in Microservices

Good service boundaries usually try to group related business responsibilities.

Example:

```text
User Service
Order Service
Payment Service
Notification Service
```

Each service has a focused purpose.

Therefore:

**Higher Service Cohesion**

Bad:

```text
EverythingService
```

containing:

```text
Users
Orders
Payments
Reports
Notifications
Inventory
Analytics
```

This is a large low-cohesion boundary.

---

# 58. Database Coupling

Bad architecture:

```text
Application A
      |
      ↓
Database Table B
```

Application A directly depends on:

```text
Table names
Column names
Schema
```

If B changes its schema:

```text
Application A
      ↓
may break
```

Better:

```text
Application A
      |
      ↓
API
      |
      ↓
Service B
      |
      ↓
Database B
```

The database becomes an internal implementation detail of Service B.

---

# 59. Temporal Coupling

Temporal coupling occurs when one component must execute before another.

Example:

```text
initialize()
     ↓
loadConfig()
     ↓
connectDatabase()
     ↓
startApplication()
```

If:

```text
startApplication()
```

runs before:

```text
connectDatabase()
```

the system may fail.

This creates ordering dependency.

Ways to reduce unnecessary temporal coupling include:

```text
Constructors
Object Lifecycle Management
Dependency Injection
Encapsulation
State Validation
```

---

# 60. Coupling Through Static State

Bad:

```java
class Config {

    static String environment;
}
```

Many classes directly access:

```text
Config.environment
```

This creates a hidden shared dependency.

Possible improvement:

```java
class Service {

    private final Config config;

    Service(Config config) {
        this.config = config;
    }
}
```

Now the dependency is explicit.

---

# 61. Coupling Through Concrete Classes

High coupling:

```java
class OrderService {

    private StripePayment payment =
        new StripePayment();
}
```

Lower coupling:

```java
class OrderService {

    private final PaymentGateway payment;

    OrderService(PaymentGateway payment) {
        this.payment = payment;
    }
}
```

The second design depends on:

```text
PaymentGateway
```

rather than:

```text
StripePayment
```

---

# 62. Coupling Through Inheritance

Inheritance can create strong coupling between:

```text
Superclass
     +
Subclass
```

Example:

```java
class Child extends Parent {
}
```

The child depends on the parent's:

- Contract
- Behavior
- Protected members
- Assumptions
- Method semantics

Deep inheritance hierarchies can become difficult to maintain.

This is one reason for the principle:

> **Favor Composition Over Inheritance**

---

# 63. Composition as an Alternative

Instead of:

```text
Animal
   ↑
 Dog
   ↑
SpecialDog
   ↑
VerySpecialDog
```

we can compose behavior:

```text
Dog
 |
 +-- MovementBehavior
 +-- SoundBehavior
 +-- FeedingBehavior
```

Behavior can be assembled from components.

Benefits:

```text
Flexibility
Testability
Maintainability
Reuse
```

---

# 64. Coupling Through Public Fields

Bad:

```java
class User {

    public String name;
}
```

Other classes directly depend on:

```text
User.name
```

If representation changes:

```text
name
```

to:

```text
firstName
lastName
```

many clients may break.

Better:

```java
class User {

    private String name;

    public String getName() {
        return name;
    }
}
```

Now representation can change internally.

---

# 65. Refactoring Pattern

Before:

```text
OrderManager
 |
 +-- order logic
 +-- payment logic
 +-- email logic
 +-- PDF logic
 +-- tax logic
```

Problems:

```text
Low Cohesion
High Coupling
```

After:

```text
OrderService
PaymentService
NotificationService
ReportService
TaxCalculator
```

Each component has a focused responsibility.

---

# 66. A-to-Z Design Thinking

When designing a class, ask:

### A — Abstraction

What should clients know?

### B — Boundaries

Where should responsibility stop?

### C — Coupling

What other modules must this class depend on?

### D — Dependency

Can dependencies be injected?

### E — Encapsulation

What implementation details should remain hidden?

### F — Focus

Does the class have one clear purpose?

### G — Grouping

Which responsibilities naturally belong together?

### H — High Cohesion

Are related responsibilities together?

### I — Interfaces

Can clients depend on abstractions?

### J — Just Enough Dependency

Can unnecessary dependencies be removed?

### K — Keep Responsibilities Focused

Avoid God Classes.

### L — Low Coupling

Minimize unnecessary dependencies.

### M — Modularity

Can the component change independently?

### N — Naming

Can the class purpose be explained in one sentence?

### O — Ownership

Who owns the object lifecycle?

### P — Polymorphism

Can varying behavior be abstracted?

### Q — Quality

Is the design easy to test?

### R — Responsibility

Does every responsibility belong here?

### S — SRP

Does the class have one primary reason to change?

### T — Testing

Can the class be tested independently?

### U — Unnecessary Dependencies

Remove them.

### V — Visibility

Keep implementation details private.

### W — Why

Always ask why the dependency exists.

### X — eXchangeability

Can implementations be replaced?

### Y — Yield

Does the design reduce change impact?

### Z — Zero Unnecessary Coupling

Aim for minimal unnecessary dependency.

---

# 67. Pattern Recognition

> [!important]
> **Pattern 1 — Dependency Between Classes**
>
> If the question says:
>
> "Dependency between modules/classes"
>
> Think:
>
> **Coupling**

> [!important]
> **Pattern 2 — Relatedness Within a Class**
>
> If the question says:
>
> "Responsibilities inside a module"
>
> Think:
>
> **Cohesion**

> [!important]
> **Pattern 3 — Best Design**
>
> If the question asks for ideal software design:
>
> Think:
>
> **Low Coupling + High Cohesion**

> [!important]
> **Pattern 4 — Many Unrelated Responsibilities**
>
> Think:
>
> **Low Cohesion**

> [!important]
> **Pattern 5 — One Focused Responsibility**
>
> Think:
>
> **High Cohesion**

> [!important]
> **Pattern 6 — Many Concrete Dependencies**
>
> Think:
>
> **High Coupling**

> [!important]
> **Pattern 7 — Global Shared Mutable Data**
>
> Think:
>
> **Common Coupling**

> [!important]
> **Pattern 8 — Direct Access to Internal Representation**
>
> Think:
>
> **Content Coupling**

> [!important]
> **Pattern 9 — Behavior Controlled by a Flag**
>
> Think:
>
> **Control Coupling**

> [!important]
> **Pattern 10 — Same Time**
>
> Think:
>
> **Temporal Cohesion**

> [!important]
> **Pattern 11 — Same Data**
>
> Think:
>
> **Communicational Cohesion**

> [!important]
> **Pattern 12 — Output Becomes Input**
>
> Think:
>
> **Sequential Cohesion**

> [!important]
> **Pattern 13 — One Clear Function**
>
> Think:
>
> **Functional Cohesion**

---

# 68. Shortcuts

> [!tip]
> **Shortcut 1**
>
> Coupling = **BETWEEN**

> [!tip]
> **Shortcut 2**
>
> Cohesion = **WITHIN**

> [!tip]
> **Shortcut 3**
>
> Good Design:
>
> **LOW COUPLING + HIGH COHESION**

> [!tip]
> **Shortcut 4**
>
> Many unrelated jobs:
>
> **LOW COHESION**

> [!tip]
> **Shortcut 5**
>
> One focused responsibility:
>
> **HIGH COHESION**

> [!tip]
> **Shortcut 6**
>
> Many concrete dependencies:
>
> **HIGH COUPLING**

> [!tip]
> **Shortcut 7**
>
> Interface + Dependency Injection:
>
> **Often reduces concrete coupling**

> [!tip]
> **Shortcut 8**
>
> Global shared state:
>
> **COMMON COUPLING**

> [!tip]
> **Shortcut 9**
>
> Direct internal access:
>
> **CONTENT COUPLING**

> [!tip]
> **Shortcut 10**
>
> Behavior controlled by flag:
>
> **CONTROL COUPLING**

> [!tip]
> **Shortcut 11**
>
> Same time:
>
> **TEMPORAL COHESION**

> [!tip]
> **Shortcut 12**
>
> Same data:
>
> **COMMUNICATIONAL COHESION**

> [!tip]
> **Shortcut 13**
>
> Output → Input:
>
> **SEQUENTIAL COHESION**

> [!tip]
> **Shortcut 14**
>
> Same procedure:
>
> **PROCEDURAL COHESION**

> [!tip]
> **Shortcut 15**
>
> One clear task:
>
> **FUNCTIONAL COHESION**

---

# 69. Common Exam Patterns

> [!important] Must Master

1. Definition of Coupling
2. Definition of Cohesion
3. Coupling vs Cohesion
4. Low Coupling
5. High Coupling
6. Low Cohesion
7. High Cohesion
8. Best software design
9. Message Coupling
10. Data Coupling
11. Stamp Coupling
12. Control Coupling
13. External Coupling
14. Common Coupling
15. Content Coupling
16. Coincidental Cohesion
17. Logical Cohesion
18. Temporal Cohesion
19. Procedural Cohesion
20. Communicational Cohesion
21. Sequential Cohesion
22. Functional Cohesion
23. Coupling and Encapsulation
24. Coupling and Abstraction
25. Coupling and Polymorphism
26. Coupling and Dependency Injection
27. Coupling and SOLID
28. Coupling and Interface Segregation
29. Coupling and Dependency Inversion
30. Coupling and Composition
31. Coupling and Inheritance
32. Coupling and Law of Demeter
33. Coupling and Global State
34. Coupling and Database Design
35. Coupling in Microservices
36. Cohesion and SRP
37. Cohesion and God Class
38. Cohesion and Refactoring
39. Cohesion and Clean Architecture
40. Scenario-Based Design Questions
41. Code-Quality Questions
42. Design-Pattern Questions
43. System-Design Questions
44. Interview Comparison Questions

---

# 70. Common Mistakes

> [!warning] Avoid These

## Mistake 1 — Reversing Coupling and Cohesion

Wrong:

```text
Coupling = Within Class
```

Correct:

```text
Coupling = BETWEEN

Cohesion = WITHIN
```

---

## Mistake 2 — Thinking High Coupling Is Good

Wrong:

```text
High Coupling
→ Strong Integration
→ Better
```

Correct:

```text
High Coupling
→ Strong Dependency
→ Harder Maintenance
```

---

## Mistake 3 — Thinking Low Cohesion Is Good

Wrong:

```text
Low Cohesion
→ Flexible
```

Correct:

```text
High Cohesion
→ Focused Responsibilities
```

---

## Mistake 4 — Trying to Eliminate All Coupling

Impossible.

Software modules must communicate.

The goal is:

```text
Minimize unnecessary coupling
```

not:

```text
Eliminate every dependency
```

---

## Mistake 5 — Thinking Interfaces Remove All Coupling

Interfaces can reduce dependency on concrete implementations.

But:

```text
Interface Dependency
```

still exists.

The goal is:

```text
Stable
Explicit
Controlled
Meaningful
Dependencies
```

---

## Mistake 6 — Assuming More Classes Automatically Means Better Cohesion

Splitting classes blindly can create:

- Excessive complexity
- Too much indirection
- Difficult navigation

The goal is:

```text
Meaningful Responsibilities
```

not:

```text
Maximum Number of Classes
```

---

## Mistake 7 — Confusing Cohesion With Encapsulation

They are related but different.

```text
Encapsulation
→ Hides implementation/state

Cohesion
→ Measures relatedness of responsibilities
```

---

## Mistake 8 — Confusing Coupling With Association

Association:

```text
Object relationship
```

Coupling:

```text
Degree of dependency
```

They are related but not identical concepts.

---

## Mistake 9 — Assuming Dependency Injection Automatically Means Low Coupling

Dependency Injection can reduce concrete coupling.

But poor abstractions can still create strong coupling.

---

## Mistake 10 — Thinking Inheritance Always Means Good Reuse

Inheritance can create strong coupling between:

```text
Superclass
+
Subclass
```

Composition is often preferred when behavior needs flexibility.

---

## Mistake 11 — Ignoring Global Variables

Global mutable state can create:

```text
Common Coupling
```

and hidden dependencies.

---

## Mistake 12 — Ignoring Class Responsibility

If a class has:

```text
Many unrelated responsibilities
```

the likely problem is:

```text
Low Cohesion
```

---

## Mistake 13 — Memorizing Cohesion Types Without Understanding

Do not only memorize:

```text
C L T P C S F
```

Understand the clues:

```text
Coincidental
→ Unrelated

Logical
→ Same broad category

Temporal
→ Same time

Procedural
→ Same procedure

Communicational
→ Same data

Sequential
→ Output becomes input

Functional
→ One focused task
```

---

# 71. Advanced Interview Questions

## Q1. What is Coupling?

**Answer:**

> Coupling is the degree of dependency between software modules or classes. Good design generally aims to minimize unnecessary coupling so that changes in one module do not strongly affect others.

---

## Q2. What is Cohesion?

**Answer:**

> Cohesion is the degree to which the responsibilities and elements inside a module are related to one another. Good design generally aims for high cohesion.

---

## Q3. What is the ideal combination?

**Answer:**

```text
Low Coupling
+
High Cohesion
```

---

## Q4. What is the difference between Coupling and Cohesion?

**Answer:**

> Coupling measures dependency between modules, whereas cohesion measures how closely related the responsibilities within a module are.

---

## Q5. Which is better: High or Low Coupling?

**Answer:**

```text
Low Coupling
```

because it reduces unnecessary dependencies.

---

## Q6. Which is better: High or Low Cohesion?

**Answer:**

```text
High Cohesion
```

because responsibilities remain focused.

---

## Q7. Why is High Cohesion preferred?

**Answer:**

> High cohesion creates focused modules that are easier to understand, test, maintain, and modify.

---

## Q8. Why is Low Coupling preferred?

**Answer:**

> Low coupling reduces dependency between modules, making the system easier to change, test, reuse, and extend.

---

## Q9. Can a system have Low Coupling and Low Cohesion?

Yes.

Example:

```text
Classes are independent
but each class contains unrelated responsibilities.
```

Therefore:

```text
Low Coupling
+
Low Cohesion
```

Still not ideal.

---

## Q10. Can a system have High Coupling and High Cohesion?

Yes.

A class may have a focused responsibility but depend heavily on many concrete modules.

Therefore:

```text
High Cohesion
+
High Coupling
```

The class is focused but difficult to change independently.

---

## Q11. What is the best design?

Generally:

```text
High Cohesion
+
Low Coupling
```

---

## Q12. What is Content Coupling?

**Answer:**

> Content coupling occurs when one module directly depends on or modifies the internal implementation details of another module.

It is generally considered very strong coupling.

---

## Q13. What is Common Coupling?

**Answer:**

> Common coupling occurs when multiple modules depend on shared global data.

---

## Q14. What is Control Coupling?

**Answer:**

> Control coupling occurs when one module passes information that determines the internal behavior or execution path of another module.

---

## Q15. What is Data Coupling?

**Answer:**

> Data coupling occurs when modules communicate by passing only the data required by the receiving module.

---

## Q16. What is Functional Cohesion?

**Answer:**

> Functional cohesion occurs when all elements of a module contribute to one well-defined function. It is generally considered the strongest form of cohesion.

---

## Q17. What is Coincidental Cohesion?

**Answer:**

> Coincidental cohesion occurs when unrelated responsibilities are grouped together without a meaningful relationship. It is generally considered the weakest form of cohesion.

---

## Q18. How does SRP improve cohesion?

**Answer:**

> SRP encourages a class to have one primary responsibility, which generally increases cohesion by keeping related behavior together.

---

## Q19. How does Dependency Inversion reduce coupling?

**Answer:**

> It encourages high-level modules to depend on abstractions instead of concrete low-level implementations, reducing concrete implementation coupling.

---

## Q20. How does Interface Segregation help?

**Answer:**

> It prevents clients from depending on methods they do not need, thereby reducing unnecessary coupling.

---

## Q21. Does Low Coupling mean No Dependencies?

**Answer:**

> No. Dependencies are necessary. The goal is to minimize unnecessary and unstable dependencies.

---

## Q22. How can you reduce coupling in Java?

Use:

```text
Interfaces
Dependency Injection
Encapsulation
Abstraction
Polymorphism
Composition
Adapter Pattern
Facade Pattern
Dependency Inversion
Avoiding unnecessary global state
```

---

## Q23. How can you increase cohesion?

Use:

```text
Focused classes
Single Responsibility
Meaningful domain boundaries
Related methods together
Extract unrelated responsibilities
```

---

## Q24. What is a God Class?

**Answer:**

> A God Class is a class that takes responsibility for too many unrelated parts of the system. It often indicates low cohesion and can also create high coupling.

---

## Q25. How does Composition help software design?

**Answer:**

> Composition allows behavior and responsibilities to be assembled from smaller components, often reducing rigid inheritance dependencies and improving modularity.

---

# 72. Advanced Scenario Questions

## Scenario 1 — One Class Does Everything

### Question

A class handles:

```text
Login
Payment
Email
Database
Reporting
```

What design problem exists?

### Recognition

```text
Many unrelated responsibilities
```

### Answer

```text
Low Cohesion
```

Likely:

```text
God Class
```

---

## Scenario 2 — One Class Depends on Many Concrete Classes

### Question

`OrderService` directly creates:

```text
StripePayment
MySQLRepository
GmailService
PdfGenerator
FileLogger
SmsService
```

What problem exists?

### Recognition

```text
Many concrete dependencies
```

### Answer

```text
High Coupling
```

---

## Scenario 3 — One Clear Responsibility

### Question

A class contains only:

```text
calculateTax()
```

What does this suggest?

### Answer

```text
High Cohesion
```

Potentially:

```text
Functional Cohesion
```

---

## Scenario 4 — Global State

### Question

Ten modules directly modify:

```text
GlobalConfig.count
```

What type of coupling is this?

### Answer

```text
Common Coupling
```

---

## Scenario 5 — Internal Access

### Question

Class A directly modifies internal implementation details of Class B.

What type of coupling does this resemble?

### Answer

```text
Content Coupling
```

---

## Scenario 6 — Mode Flag

### Question

A method receives:

```text
mode = 1
mode = 2
mode = 3
```

and changes its internal algorithm based on the mode.

What coupling?

### Answer

```text
Control Coupling
```

A Strategy Pattern may provide a cleaner design.

---

## Scenario 7 — Same Time

### Question

A module performs:

```text
Startup logging
Configuration loading
Cache initialization
Database connection
```

because all happen during application startup.

What cohesion?

### Answer

```text
Temporal Cohesion
```

---

## Scenario 8 — Same Data

### Question

Several operations all manipulate the same `Student` object.

What cohesion?

### Answer

```text
Communicational Cohesion
```

---

## Scenario 9 — Output to Input

### Question

One function reads data, another parses the result, and another transforms the parsed result.

What cohesion?

### Answer

```text
Sequential Cohesion
```

---

## Scenario 10 — One Clear Function

### Question

A class performs only:

```text
calculateInterest()
```

What cohesion?

### Answer

```text
Functional Cohesion
```

---

# 73. Design Improvement Pattern

> [!important]
> When you see:
>
> **LOW COHESION**
>
> Think:
>
> ```text
> Split Responsibilities
> Extract Classes
> Apply SRP
> ```
>
> When you see:
>
> **HIGH COUPLING**
>
> Think:
>
> ```text
> Introduce Abstraction
> Use Interfaces
> Dependency Injection
> Encapsulation
> Adapter
> Reduce Global State
> ```

---

# 74. Real-Time Project Example: E-Commerce

Suppose you build an e-commerce application.

Bad architecture:

```text
OrderManager
    |
    +-- Database
    +-- Payment
    +-- Email
    +-- Inventory
    +-- PDF
    +-- Logging
    +-- Analytics
```

Problems:

```text
High Coupling
Low Cohesion
```

Better:

```text
OrderService
PaymentService
InventoryService
NotificationService
ReportService
AnalyticsService
```

Each component has a focused responsibility.

Now:

```text
Higher Cohesion
+
Lower Coupling
```

---

# 75. Real-Time Banking Example

Bad:

```text
BankService
    |
    +-- Account
    +-- Loan
    +-- Payment
    +-- Email
    +-- Report
    +-- Image
```

This is likely a God Class.

Better:

```text
AccountService
LoanService
PaymentService
NotificationService
ReportService
```

Each service focuses on one domain responsibility.

---

# 76. Real-Time Food Delivery Example

Possible modules:

```text
CustomerService
RestaurantService
OrderService
PaymentService
DeliveryService
NotificationService
```

High cohesion:

```text
OrderService
→ Order-related responsibilities
```

Low coupling:

```text
OrderService
→ Depends on stable abstractions
→ Does not know concrete implementations
```

---

# 77. Real-Time Ride Booking Example

Possible components:

```text
RideService
DriverService
PaymentService
LocationService
NotificationService
```

Bad:

```text
RideService
→ Directly manipulates internal details
  of every other service
```

Better:

```text
RideService
     ↓
Stable Interfaces
     ↓
Specialized Services
```

This keeps dependencies controlled.

---

# 78. System Design Insight

In large systems, a useful goal is:

```text
Each module
    ↓
Owns a focused responsibility
```

while:

```text
Modules
    ↓
Communicate through stable contracts
```

Therefore:

```text
High Cohesion
+
Low Coupling
```

This principle applies from:

```text
Small Classes
     ↓
Packages
     ↓
Services
     ↓
Microservices
```

---

# 79. Advanced Interview Insight

### Question

"Is Low Coupling always better?"

### Strong Answer

> "The goal is not to eliminate all coupling. Some coupling is necessary for components to communicate. We want low unnecessary coupling and stable, well-defined dependencies."

This is better than saying:

```text
Coupling should be zero.
```

---

# 80. Advanced Interview Insight: Is High Cohesion Always Better?

Generally, high cohesion is desirable.

However, blindly splitting everything can create:

```text
Too many tiny classes
Excessive indirection
Difficult navigation
Unnecessary complexity
```

Therefore:

```text
High Cohesion
+
Sensible Boundaries
```

is the goal.

---

# 81. Advanced Interview Insight: Coupling Is Not Binary

Coupling is not simply:

```text
Coupled
or
Not Coupled
```

It can occur at different levels.

Examples:

```text
Concrete Implementation Coupling
Interface Coupling
Data Coupling
Control Coupling
Temporal Coupling
External Coupling
```

The goal is:

```text
Stable
Explicit
Minimal
Meaningful Dependencies
```

---

# 82. Advanced Interview Insight: Cohesion Is Not Number of Methods

A class with five methods can have:

```text
High Cohesion
```

A class with one method can still have a poor responsibility.

The number of methods is not the definition.

The real question is:

> "Are the responsibilities related?"

---

# 83. Advanced Interview Insight: Four Design Combinations

| Coupling | Cohesion | Design Quality |
|---|---|---|
| Low | High | Best target |
| Low | Low | Independent but unfocused |
| High | High | Focused but strongly dependent |
| High | Low | Poor design |

Ideal:

```text
Low Coupling
+
High Cohesion
```

---

# 84. Master Decision Tree

```text
              SOFTWARE DESIGN
                     |
          +----------+----------+
          |                     |
          ↓                     ↓
       WITHIN                BETWEEN
       MODULE                MODULES
          |                     |
          ↓                     ↓
      COHESION              COUPLING
          |                     |
     +----+----+           +----+----+
     |         |           |         |
     ↓         ↓           ↓         ↓
 Related?  Unrelated?   Weak?     Strong?
     |         |           |         |
     ↓         ↓           ↓         ↓
   HIGH       LOW        LOW       HIGH
 COHESION   COHESION   COUPLING   COUPLING
```

---

# 85. Formula Sheet

```text
COUPLING

Coupling
=
Degree of Dependency BETWEEN Modules


COHESION

Cohesion
=
Degree of Relatedness WITHIN a Module


IDEAL DESIGN

Low Coupling
+
High Cohesion
=
Good Software Design


MEMORY

Coupling
→ BETWEEN

Cohesion
→ WITHIN


COUPLING TYPES

Message
Data
Stamp
Control
External
Common
Content


COUPLING MEMORY

M D S C E C C


COHESION TYPES

Coincidental
Logical
Temporal
Procedural
Communicational
Sequential
Functional


COHESION MEMORY

C L T P C S F


COHESION QUALITY

Coincidental
→ Weakest

Functional
→ Strongest


COMMON COUPLING CLUES

Global Shared Data
→ Common Coupling

Direct Internal Modification
→ Content Coupling

Behavior Controlled by Flag
→ Control Coupling

Only Required Data Passed
→ Data Coupling

Large Structure Passed Unnecessarily
→ Stamp Coupling

External Protocol/System Dependency
→ External Coupling


COHESION CLUES

Unrelated Responsibilities
→ Coincidental

Same Broad Category
→ Logical

Same Time
→ Temporal

Same Procedure
→ Procedural

Same Data
→ Communicational

Output → Input
→ Sequential

One Clear Task
→ Functional


LOW COUPLING TECHNIQUES

Interfaces
Dependency Injection
Abstraction
Encapsulation
Polymorphism
Composition
Adapter Pattern
Facade Pattern
Dependency Inversion
Avoid Unnecessary Global State


HIGH COHESION TECHNIQUES

Single Responsibility
Focused Classes
Meaningful Boundaries
Related Methods Together
Extract Unrelated Responsibilities
Domain-Oriented Design
```

---

# 86. Quick Revision

> [!summary] One-Minute Revision

## Coupling

```text
Dependency BETWEEN Modules
```

## Cohesion

```text
Relatedness WITHIN a Module
```

## Ideal Design

```text
LOW COUPLING
+
HIGH COHESION
```

## Coupling Memory

```text
BETWEEN
```

## Cohesion Memory

```text
WITHIN
```

## Coupling Types

```text
Message
Data
Stamp
Control
External
Common
Content
```

## Cohesion Types

```text
Coincidental
Logical
Temporal
Procedural
Communicational
Sequential
Functional
```

## Fast Recognition

```text
"Between classes?"
→ Coupling

"Within class?"
→ Cohesion

"Global shared data?"
→ Common Coupling

"Direct internal access?"
→ Content Coupling

"Behavior controlled by flag?"
→ Control Coupling

"Same time?"
→ Temporal Cohesion

"Same data?"
→ Communicational Cohesion

"Output becomes input?"
→ Sequential Cohesion

"One clear task?"
→ Functional Cohesion
```

## Best Design

```text
High Cohesion
+
Low Coupling
```

## Important Design Techniques

```text
Abstraction
Encapsulation
Interfaces
Dependency Injection
Polymorphism
Composition
SOLID
Adapter Pattern
Dependency Inversion
```

## Interview Answer

> Good software design generally aims for high cohesion and low coupling. High cohesion keeps related responsibilities together, while low coupling minimizes unnecessary dependencies between modules.

---

# 87. Golden Memory Trick

**Coupling connects modules from the outside; Cohesion keeps related responsibilities together on the inside.**

# 88. One-Line Recognition

**If the question asks about dependency BETWEEN modules, think Coupling; if it asks about related responsibilities WITHIN a module, think Cohesion.**