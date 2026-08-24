---
type: concept
subject: aptitude
topic: "Polymorphism"
parent: "OOPS"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - polymorphism
  - compile-time-polymorphism
  - runtime-polymorphism
  - method-overloading
  - method-overriding
  - dynamic-method-dispatch
  - java
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Inheritance]]"
  - "[[Method Overloading]]"
  - "[[Method Overriding]]"
  - "[[Dynamic Method Dispatch]]"
  - "[[Abstraction]]"
---

# Polymorphism

> [!summary]
> **Polymorphism** means **"one name, many forms."**
>
> In OOP, the same method name, reference, or interface can represent different behavior depending on the situation.
>
> The two major forms in Java are:
>
> ```text
> Polymorphism
> ├── Compile-Time Polymorphism
> │   └── Method Overloading
> │
> └── Runtime Polymorphism
>     ├── Method Overriding
>     └── Dynamic Method Dispatch
> ```
>
> Core idea:
>
> **Same interface/name → different behavior**

---

# 1. Core Concept

The word **polymorphism** comes from:

```text
Poly  = Many
Morph = Forms
```

Therefore:

$$
\boxed{\text{Polymorphism} = \text{Many Forms}}
$$

In programming, polymorphism allows the same operation to behave differently depending on the context.

Consider:

```java
print()
```

The same conceptual operation may print:

```text
Text
Image
PDF
Invoice
Report
```

The operation is conceptually the same:

```text
print()
```

but the actual behavior can differ.

---

# 2. Simple Real-Life Intuition

Consider the word:

```text
"Pay"
```

A customer can pay using:

```text
UPI
Credit Card
Debit Card
Cash
Wallet
```

The action is:

```text
PAY
```

but the implementation differs.

```text
             Pay
          /   |   \
        UPI Card Wallet
```

This is the basic intuition behind polymorphism.

> [!important]
> **Polymorphism allows one common operation to represent different implementations.**

---

# 3. Basic Meaning

Suppose we have:

```java
animal.sound();
```

Different animals can produce different sounds.

```text
Animal
 /   \
Dog  Cat
 |    |
Bark Meow
```

The method name is:

```text
sound()
```

but the behavior changes.

```java
Dog → sound() → Bark
Cat → sound() → Meow
```

Therefore:

$$
\boxed{\text{Same Method} + \text{Different Behavior} = \text{Polymorphism}}
$$

---

# 4. Types of Polymorphism

Java mainly demonstrates polymorphism through two important mechanisms.

```text
                    Polymorphism
                         |
              +----------+----------+
              |                     |
              ↓                     ↓
        Compile-Time             Runtime
        Polymorphism             Polymorphism
              |                     |
              ↓                     ↓
      Method Overloading      Method Overriding
                                    |
                                    ↓
                         Dynamic Method Dispatch
```

---

# 5. Compile-Time Polymorphism

Compile-time polymorphism is commonly achieved through:

```text
Method Overloading
```

The compiler determines which overloaded method should be called based on the method signature and arguments.

Example:

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

Now:

```java
Calculator c = new Calculator();

c.add(10, 20);
c.add(10, 20, 30);
```

The method name is the same:

```text
add()
```

but the parameter lists differ.

```text
add(int, int)
add(int, int, int)
```

This is method overloading.

---

# 6. Runtime Polymorphism

Runtime polymorphism is commonly achieved through:

```text
Method Overriding
```

Example:

```java
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
```

Now:

```java
Animal a = new Dog();

a.sound();
```

Output:

```text
Bark
```

Why?

Because:

```text
Reference Type → Animal
Actual Object  → Dog
```

At runtime, Java selects:

```text
Dog.sound()
```

This is runtime polymorphism.

---

# 7. Main Difference

| Feature | Compile-Time | Runtime |
|---|---|---|
| Main mechanism | Overloading | Overriding |
| Decision | Compile time | Runtime |
| Inheritance required? | No | Generally yes |
| Same method name? | Yes | Yes |
| Parameters | Must differ | Usually same signature |
| Main concept | Which overloaded method? | Which overridden implementation? |
| Common term | Static/Early Binding | Dynamic/Late Binding |

> [!tip]
> **Overloading → Compiler decides**
>
> **Overriding → Runtime object decides**

---

# 8. Method Overloading

Method overloading means having multiple methods with the same name but different parameter lists in the same class or an inherited context.

Example:

```java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

Here:

```text
add(int, int)
add(double, double)
add(int, int, int)
```

are different method signatures.

---

# 9. What Can Change in Overloading?

To overload a method, the parameter list must differ.

You can change:

### Number of Parameters

```java
add(int, int)
add(int, int, int)
```

### Parameter Types

```java
add(int, int)
add(double, double)
```

### Parameter Order

```java
show(int, String)
show(String, int)
```

Example:

```java
void display(int x, String s) {
}

void display(String s, int x) {
}
```

These are overloaded methods.

---

# 10. What Does NOT Create Overloading?

Changing only the return type is not enough.

Invalid:

```java
int add(int a, int b) {
    return a + b;
}

double add(int a, int b) {
    return a + b;
}
```

The parameter list is identical.

The compiler cannot distinguish them using only the return type.

Therefore this is invalid.

> [!warning]
> **Return type alone cannot overload a method.**

---

# 11. Method Overloading Example

```java
class Printer {

    void print(int x) {
        System.out.println("Integer");
    }

    void print(double x) {
        System.out.println("Double");
    }

    void print(String x) {
        System.out.println("String");
    }
}
```

Now:

```java
Printer p = new Printer();

p.print(10);
p.print(10.5);
p.print("Hello");
```

Output:

```text
Integer
Double
String
```

The compiler selects the appropriate method based on the argument.

---

# 12. Real-Time Example — Login System

A system might support:

```text
login(username, password)

login(phoneNumber, otp)

login(email, password)
```

Conceptually:

```java
void login(String username, String password) {
}

void login(long phone, int otp) {
}

void login(String email, String password, boolean rememberMe) {
}
```

Same conceptual operation:

```text
login()
```

Different parameter combinations.

This is overloading.

---

# 13. Real-Time Example — Payment

Consider:

```java
void pay(double amount) {
}

void pay(double amount, String cardNumber) {
}

void pay(double amount, String upiId, String pin) {
}
```

The operation is:

```text
pay()
```

but the input information differs.

This is compile-time polymorphism through method overloading.

---

# 14. Real-Time Example — Search

A search API may conceptually support:

```java
search(String keyword)

search(String keyword, int page)

search(String keyword, int page, int size)
```

Same operation:

```text
search()
```

Different parameters.

This is a common practical use of overloading.

---

# 15. Real-Time Example — Constructors

Constructors can also be overloaded.

```java
class Student {

    Student() {
    }

    Student(String name) {
    }

    Student(String name, int age) {
    }
}
```

This is:

```text
Constructor Overloading
```

It is another example of compile-time polymorphism.

---

# 16. Method Overriding

Method overriding occurs when a child class provides its own implementation of an inherited instance method with the same signature.

Example:

```java
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
```

Here:

```text
Animal.sound()
```

is overridden by:

```text
Dog.sound()
```

---

# 17. Why Override?

Overriding allows a child class to specialize inherited behavior.

Parent:

```text
Animal
→ sound()
```

Child:

```text
Dog
→ Bark
```

Another child:

```text
Cat
→ Meow
```

Therefore:

```text
Common contract
       ↓
Different implementations
```

This is one of the most important benefits of polymorphism.

---

# 18. Real-Time Example — Notification

Consider:

```text
Notification
      |
   send()
```

Different implementations:

```text
EmailNotification
      ↓
send() → Email

SMSNotification
      ↓
send() → SMS

PushNotification
      ↓
send() → Push
```

Java:

```java
class Notification {

    void send() {
        System.out.println("Sending notification");
    }
}

class EmailNotification extends Notification {

    @Override
    void send() {
        System.out.println("Sending Email");
    }
}

class SMSNotification extends Notification {

    @Override
    void send() {
        System.out.println("Sending SMS");
    }
}
```

Now:

```java
Notification n;

n = new EmailNotification();
n.send();

n = new SMSNotification();
n.send();
```

Output:

```text
Sending Email
Sending SMS
```

This is runtime polymorphism.

---

# 19. Real-Time Example — Payment Processing

Consider:

```text
             Payment
                |
              pay()
             /    \
            /      \
         UPI       Card
          |          |
        pay()       pay()
```

Java:

```java
class Payment {

    void pay() {
        System.out.println("Payment");
    }
}

class UPI extends Payment {

    @Override
    void pay() {
        System.out.println("UPI Payment");
    }
}

class Card extends Payment {

    @Override
    void pay() {
        System.out.println("Card Payment");
    }
}
```

Now:

```java
Payment p;

p = new UPI();
p.pay();

p = new Card();
p.pay();
```

Output:

```text
UPI Payment
Card Payment
```

The same reference type:

```text
Payment
```

can represent different actual objects.

---

# 20. Real-Time Example — Ride Booking

Consider a ride application:

```text
             Ride
              |
            book()
          /   |   \
         /    |    \
      Bike   Auto  Car
       |      |     |
     book() book() book()
```

The application can use:

```java
Ride ride;
```

Then:

```java
ride = new Bike();
ride.book();

ride = new Car();
ride.book();
```

The method call stays:

```text
ride.book()
```

but the actual behavior changes based on the object.

---

# 21. Real-Time Example — File Export

Consider:

```text
             Exporter
                |
              export()
           /     |      \
          /      |       \
        PDF     Excel    CSV
```

Each class can override:

```text
export()
```

The calling code can simply use:

```java
Exporter exporter;
```

without needing to know the exact implementation.

This is a major practical advantage of polymorphism.

---

# 22. Real-Time Example — Database Connection

Consider:

```text
             Database
                |
             connect()
           /    |     \
          /     |      \
       MySQL  Oracle  PostgreSQL
```

Application code can work against:

```text
Database
```

while each implementation provides its own connection logic.

This is a fundamental idea in scalable software architecture.

---

# 23. Real-Time Example — Shape

Consider:

```text
              Shape
            /   |   \
           /    |    \
       Circle Square Triangle
         |       |       |
       area()  area()  area()
```

Java:

```java
class Shape {

    double area() {
        return 0;
    }
}

class Circle extends Shape {

    @Override
    double area() {
        return 3.14 * 5 * 5;
    }
}

class Square extends Shape {

    @Override
    double area() {
        return 10 * 10;
    }
}
```

Then:

```java
Shape s = new Circle();

System.out.println(s.area());
```

The runtime object is `Circle`.

Therefore:

```text
Circle.area()
```

is selected.

---

# 24. Dynamic Method Dispatch

Dynamic Method Dispatch is the mechanism through which Java determines the overridden method implementation at runtime.

Example:

```java
Animal a = new Dog();

a.sound();
```

Break it into:

```text
Reference type
      ↓
Animal

Actual object
      ↓
Dog

Method
      ↓
sound()

Runtime selection
      ↓
Dog.sound()
```

Therefore:

$$
\boxed{\text{Dynamic Method Dispatch} = \text{Runtime Selection of Overridden Method}}
$$

---

# 25. The Most Important Rule

> [!important]
> For overridden **instance methods**, Java uses the **actual object type**, not merely the reference type, to select the implementation at runtime.

Example:

```java
Animal a = new Dog();
```

Think:

```text
Reference → Animal
Object    → Dog
```

Then:

```java
a.sound();
```

goes to:

```text
Dog.sound()
```

if `Dog` overrides it.

---

# 26. Parent Reference + Child Object

This is the heart of runtime polymorphism.

```java
Animal a = new Dog();
```

This is valid because:

```text
Dog IS-A Animal
```

The reference type controls what members are accessible through the reference.

The actual object controls overridden instance-method behavior at runtime.

This distinction is extremely important.

---

# 27. Accessible Methods vs Executed Methods

Consider:

```java
class Animal {

    void eat() {
    }

    void sound() {
    }
}

class Dog extends Animal {

    @Override
    void sound() {
    }

    void bark() {
    }
}
```

Now:

```java
Animal a = new Dog();
```

Can we write:

```java
a.eat();
```

Yes.

Can we write:

```java
a.sound();
```

Yes.

Can we write:

```java
a.bark();
```

No, not directly through an `Animal` reference because `bark()` is not declared in `Animal`.

This creates a crucial rule:

> [!important]
> **Reference type determines what members can be accessed.**
>
> **Actual object determines which overridden instance method implementation runs.**

---

# 28. High-Level Mental Model

Think of:

```java
Animal a = new Dog();
```

as:

```text
                Reference
                   |
                   ↓
                Animal
                   |
             "What can I access?"

                   +

                 Object
                   |
                   ↓
                  Dog
                   |
             "Which override runs?"
```

Therefore:

```text
Reference Type → Access
Object Type    → Runtime Override
```

This is one of the most important Java interview rules.

---

# 29. Compile-Time vs Runtime — Deep Difference

Consider overloading:

```java
class Printer {

    void print(int x) {
        System.out.println("int");
    }

    void print(double x) {
        System.out.println("double");
    }
}
```

Call:

```java
Printer p = new Printer();

p.print(10);
```

The compiler sees:

```text
10 → int
```

and chooses:

```text
print(int)
```

This happens during compilation.

Now overriding:

```java
Animal a = new Dog();

a.sound();
```

The compiler verifies that `sound()` is available through `Animal`.

But the overridden implementation is selected based on the runtime object.

```text
Actual object = Dog
```

Therefore:

```text
Dog.sound()
```

---

# 30. Binding

Binding means associating a method call with a method implementation.

There are two important concepts:

### Static / Early Binding

Association happens at compile time.

Commonly associated with:

```text
Overloading
static methods
private methods
final methods
```

### Dynamic / Late Binding

Association of an overridden instance method happens at runtime.

Commonly associated with:

```text
Method overriding
```

> [!tip]
> **Overloading → Early Binding**
>
> **Overriding → Late Binding**

---

# 31. Static Method Trap

Static methods are not overridden in the same polymorphic way as instance methods.

They are hidden.

Example:

```java
class Parent {

    static void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    static void show() {
        System.out.println("Child");
    }
}
```

Now:

```java
Parent p = new Child();

p.show();
```

Output:

```text
Parent
```

Why?

Static method resolution is based on the reference/class context, not runtime dynamic dispatch like overridden instance methods.

> [!warning]
> **Do not apply runtime polymorphism rules blindly to static methods.**

---

# 32. Private Method Trap

Private methods are not overridden because they are not inherited as accessible methods by subclasses.

Example:

```java
class Parent {

    private void show() {
        System.out.println("Parent");
    }
}
```

A child may declare:

```java
void show() {
    System.out.println("Child");
}
```

This is not method overriding of the parent's private method.

They are separate methods.

---

# 33. Final Method Trap

A `final` instance method cannot be overridden.

Example:

```java
class Parent {

    final void show() {
        System.out.println("Parent");
    }
}
```

This is invalid:

```java
class Child extends Parent {

    @Override
    void show() {
        System.out.println("Child");
    }
}
```

because the parent method is `final`.

> [!important]
> `final` instance method → cannot be overridden.

---

# 34. Method Overloading vs Overriding

This table should be memorized.

| Feature | Overloading | Overriding |
|---|---|---|
| Class relationship | Same class commonly | Parent-child |
| Method name | Same | Same |
| Parameters | Must differ | Same signature |
| Return type | May differ if parameters differ | Same or covariant return |
| Binding | Compile time | Runtime |
| Inheritance | Not required | Required |
| Purpose | Different ways to call same operation | Specialized child behavior |
| Example | `add(int,int)` / `add(int,int,int)` | `Animal.sound()` / `Dog.sound()` |

---

# 35. Overloading Recognition

> [!important]
> If you see:
>
> ```text
> Same method name
> +
> Different parameters
> ```
>
> think:
>
> **Method Overloading**

Example:

```text
add(int, int)
add(double, double)
add(int, int, int)
```

---

# 36. Overriding Recognition

> [!important]
> If you see:
>
> ```text
> Parent method
> +
> Child same signature
> ```
>
> think:
>
> **Method Overriding**

Example:

```text
Animal.sound()
Dog.sound()
```

---

# 37. Dynamic Dispatch Recognition

> [!important]
> If you see:
>
> ```java
> Parent ref = new Child();
> ref.method();
> ```
>
> and `Child` overrides `method()`,
>
> think:
>
> **Dynamic Method Dispatch**
>
> and expect:
>
> **Child's overridden implementation**

---

# 38. Important Rule — Static Type vs Dynamic Type

Two types may be involved.

Example:

```java
Animal a = new Dog();
```

### Static Type

```text
Animal
```

Also called:

```text
Compile-time type
Reference type
```

### Dynamic Type

```text
Dog
```

Also called:

```text
Runtime type
Actual object type
```

Therefore:

$$
\boxed{\text{Static Type} = \text{Reference Type}}
$$

$$
\boxed{\text{Dynamic Type} = \text{Actual Object Type}}
$$

---

# 39. Advanced Example — Access and Dispatch

Consider:

```java
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

    void bark() {
        System.out.println("Bark");
    }
}
```

Now:

```java
Animal a = new Dog();
```

### Question 1

Can we call:

```java
a.sound();
```

Yes.

### Question 2

Which implementation?

```text
Dog.sound()
```

### Question 3

Can we call:

```java
a.bark();
```

No.

Why?

```text
bark() is not declared in Animal.
```

Therefore:

```text
Access → Reference Type
Override selection → Actual Object
```

---

# 40. Downcasting

If you know the actual object is a `Dog`, you can cast:

```java
Animal a = new Dog();

Dog d = (Dog) a;

d.bark();
```

Now the reference is:

```text
Dog
```

so `bark()` is accessible.

> [!warning]
> Downcasting is only safe when the actual object is compatible with the target type.

This can otherwise cause:

```text
ClassCastException
```

---

# 41. Upcasting

Upcasting is assigning a child object to a parent reference.

```java
Dog dog = new Dog();

Animal animal = dog;
```

This is generally safe because:

```text
Dog IS-A Animal
```

It is commonly used for polymorphism.

```text
Dog object
   ↓
Animal reference
```

---

# 42. Upcasting vs Downcasting

| Type | Direction | Example |
|---|---|---|
| Upcasting | Child → Parent | `Animal a = new Dog();` |
| Downcasting | Parent reference → Child reference | `Dog d = (Dog) a;` |

### Shortcut

> [!tip]
> **Up = toward parent**
>
> **Down = toward child**

---

# 43. Real-Time Polymorphic Collection

One of the biggest practical uses of polymorphism is storing different child objects under a common parent type.

Example:

```java
List<Animal> animals = new ArrayList<>();

animals.add(new Dog());
animals.add(new Cat());
animals.add(new Cow());
```

Then:

```java
for (Animal animal : animals) {
    animal.sound();
}
```

Output might be:

```text
Bark
Meow
Moo
```

The loop does not need separate code for every animal.

This is powerful.

---

# 44. Why Polymorphism Reduces `if-else`

Without polymorphism, code may become:

```java
if (type.equals("DOG")) {
    dogSound();
}
else if (type.equals("CAT")) {
    catSound();
}
else if (type.equals("COW")) {
    cowSound();
}
```

With polymorphism:

```java
animal.sound();
```

Each object knows how to perform its own behavior.

This improves extensibility.

---

# 45. Open/Closed Principle Connection

Polymorphism works strongly with the Open/Closed Principle.

The idea:

```text
Open for extension
Closed for modification
```

Suppose:

```text
Shape
 /   \
Circle Square
```

Later we add:

```text
Triangle
```

If the code depends on:

```text
Shape
```

rather than hardcoded types, we can add a new implementation without rewriting every consumer.

This is one reason polymorphism is central to object-oriented design.

---

# 46. Interface-Based Polymorphism

Polymorphism does not require a parent class.

Interfaces are extremely important.

Example:

```java
interface Payment {

    void pay();
}
```

Implementations:

```java
class UPI implements Payment {

    public void pay() {
        System.out.println("UPI");
    }
}

class Card implements Payment {

    public void pay() {
        System.out.println("Card");
    }
}
```

Now:

```java
Payment p;

p = new UPI();
p.pay();

p = new Card();
p.pay();
```

Output:

```text
UPI
Card
```

This is runtime polymorphism through an interface.

---

# 47. Real-Time Example — Dependency Injection

Suppose:

```java
interface PaymentService {

    void pay();
}
```

Implementations:

```text
UPIPaymentService
CardPaymentService
WalletPaymentService
```

A class can depend on the interface:

```java
class OrderService {

    private PaymentService paymentService;

    OrderService(PaymentService paymentService) {
        this.paymentService = paymentService;
    }

    void checkout() {
        paymentService.pay();
    }
}
```

Now:

```java
new OrderService(new UPIPaymentService());
```

or:

```java
new OrderService(new CardPaymentService());
```

The `OrderService` does not need to know the concrete implementation.

This is a major real-world use of polymorphism.

---

# 48. Strategy Pattern Connection

Polymorphism is the foundation of the Strategy Design Pattern.

Example:

```text
             PaymentStrategy
              /      |      \
             /       |       \
          UPI       Card    Wallet
```

Each strategy implements:

```text
pay()
```

The client works with:

```text
PaymentStrategy
```

rather than hardcoding one payment mechanism.

This allows behavior to be changed dynamically.

---

# 49. Basic Examples

## Example 1 — Identify Polymorphism

**Question**

```java
void add(int a, int b) {
}

void add(int a, int b, int c) {
}
```

What concept is this?

### Pattern

```text
Same method name
+
Different parameters
```

### Answer

$$
\boxed{\text{Method Overloading}}
$$

Therefore:

$$
\boxed{\text{Compile-Time Polymorphism}}
$$

---

# 50. Example 2 — Identify Overriding

**Question**

```java
class Animal {

    void sound() {
    }
}

class Dog extends Animal {

    @Override
    void sound() {
    }
}
```

What concept is this?

### Pattern

```text
Parent
↓
Child
↓
Same method signature
```

### Answer

$$
\boxed{\text{Method Overriding}}
$$

Therefore:

$$
\boxed{\text{Runtime Polymorphism}}
$$

---

# 51. Example 3 — Dynamic Dispatch

**Question**

```java
Animal a = new Dog();

a.sound();
```

`Dog` overrides `sound()`.

Which method executes?

### Analysis

```text
Reference → Animal
Object → Dog
```

Runtime object:

```text
Dog
```

Therefore:

```text
Dog.sound()
```

### Answer

$$
\boxed{\text{Dog.sound()}}
$$

---

# 52. Example 4 — Overloading

**Question**

```java
class Test {

    void show(int x) {
        System.out.println("int");
    }

    void show(double x) {
        System.out.println("double");
    }
}
```

Now:

```java
Test t = new Test();

t.show(10);
```

Which method executes?

### Analysis

```text
10 → int
```

Therefore:

```text
show(int)
```

### Answer

```text
int
```

---

# 53. Medium Example — Three Overloads

Consider:

```java
class Printer {

    void print(int x) {
        System.out.println("int");
    }

    void print(double x) {
        System.out.println("double");
    }

    void print(String x) {
        System.out.println("String");
    }
}
```

Now:

```java
Printer p = new Printer();

p.print(10);
p.print(10.5);
p.print("Java");
```

Output:

```text
int
double
String
```

The compiler resolves each call using the argument types.

---

# 54. Medium Example — Overriding

Consider:

```java
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
```

Now:

```java
Dog d = new Dog();

d.sound();
```

Output:

```text
Dog
```

The child implementation overrides the inherited implementation.

---

# 55. Advanced Example — Parent Reference

Consider:

```java
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

Animal a = new Dog();

a.sound();
```

### Step 1

Reference:

```text
Animal
```

### Step 2

Actual object:

```text
Dog
```

### Step 3

`Dog` overrides `sound()`.

### Step 4

Runtime dispatch selects:

```text
Dog.sound()
```

### Answer

```text
Dog
```

---

# 56. Advanced Example — Parent Reference and Child Method

Consider:

```java
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

    void bark() {
        System.out.println("Bark");
    }
}
```

Now:

```java
Animal a = new Dog();

a.sound();
```

Output:

```text
Dog
```

But:

```java
a.bark();
```

does not compile.

Why?

Because:

```text
bark()
```

is not declared in `Animal`.

---

# 57. Advanced Example — Static Method

Consider:

```java
class Parent {

    static void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    static void show() {
        System.out.println("Child");
    }
}

Parent p = new Child();

p.show();
```

### Important

`show()` is static.

Static methods are hidden rather than dynamically overridden.

The reference/class context determines the method.

### Answer

```text
Parent
```

---

# 58. Advanced Example — Final Method

Consider:

```java
class Parent {

    final void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    // Cannot override show()
}
```

A child cannot provide an override for a final method.

Therefore:

```text
final → no overriding
```

---

# 59. Advanced Example — Private Method

Consider:

```java
class Parent {

    private void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    void show() {
        System.out.println("Child");
    }
}
```

The `Child.show()` method is not an override of `Parent.show()`.

Why?

Because the parent method is private.

This is another interview trap.

---

# 60. Covariant Return Type

Overriding allows a child method to return a subtype of the parent's return type.

Example:

```java
class Animal {
}

class Dog extends Animal {
}

class Parent {

    Animal getAnimal() {
        return new Animal();
    }
}

class Child extends Parent {

    @Override
    Dog getAnimal() {
        return new Dog();
    }
}
```

Here:

```text
Parent → Animal
Child  → Dog
```

Since:

```text
Dog IS-A Animal
```

the return type is covariant.

This is an advanced overriding rule.

---

# 61. Access Modifier Rule in Overriding

A child cannot reduce the visibility of an overridden method.

Suppose:

```java
class Parent {

    public void show() {
    }
}
```

The child cannot write:

```java
protected void show() {
}
```

or:

```java
private void show() {
}
```

because that would reduce visibility.

The child may maintain or increase accessibility according to Java's rules.

> [!important]
> **Overriding cannot make an inherited method less accessible.**

---

# 62. Exception Rule in Overriding

A child overriding method cannot introduce broader checked exceptions than allowed by the parent method's declaration.

This is an advanced interview topic.

The core memory:

```text
Overriding
→ Cannot widen checked exceptions arbitrarily.
```

Unchecked exceptions have different rules.

---

# 63. `super` and Runtime Polymorphism

Suppose:

```java
class Animal {

    void sound() {
        System.out.println("Animal");
    }
}

class Dog extends Animal {

    @Override
    void sound() {

        super.sound();

        System.out.println("Dog");
    }
}
```

Now:

```java
Animal a = new Dog();

a.sound();
```

Output:

```text
Animal
Dog
```

Why?

The dynamic dispatch initially selects:

```text
Dog.sound()
```

Inside `Dog.sound()`:

```text
super.sound()
```

explicitly invokes the parent implementation.

---

# 64. Polymorphism and Abstraction

Polymorphism and abstraction are closely related.

Abstraction says:

```text
What should be done?
```

Polymorphism says:

```text
Which implementation should perform it?
```

Example:

```text
Payment
  ↓
pay()
```

The abstraction defines:

```text
pay()
```

Different implementations:

```text
UPI
Card
Wallet
```

provide the actual behavior.

---

# 65. Polymorphism and Encapsulation

Encapsulation hides internal implementation.

Polymorphism allows clients to use a common interface.

Together:

```text
Client
  ↓
Common Interface
  ↓
Different Implementations
```

The client does not need to know implementation details.

This is a fundamental OOP design advantage.

---

# 66. Polymorphism and Inheritance

Inheritance is not identical to polymorphism.

Inheritance:

```text
Child IS-A Parent
```

Polymorphism:

```text
Same interface
→ Different behavior
```

Inheritance can enable runtime polymorphism, but polymorphism can also be achieved through interfaces.

Example:

```java
Payment p = new UPI();
```

The important relationship is:

```text
UPI implements Payment
```

not necessarily class inheritance.

---

# 67. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Identify compile-time polymorphism.

### Pattern 2
Identify runtime polymorphism.

### Pattern 3
Identify method overloading.

### Pattern 4
Identify method overriding.

### Pattern 5
Trace overloaded method calls.

### Pattern 6
Trace overridden method calls.

### Pattern 7
Understand parent reference + child object.

### Pattern 8
Understand dynamic method dispatch.

### Pattern 9
Understand static method hiding.

### Pattern 10
Understand private methods are not overridden.

### Pattern 11
Understand final methods cannot be overridden.

### Pattern 12
Understand upcasting.

### Pattern 13
Understand downcasting.

### Pattern 14
Understand interface-based polymorphism.

### Pattern 15
Understand covariant return types.

### Pattern 16
Understand overriding access restrictions.

### Pattern 17
Understand constructor overloading.

### Pattern 18
Understand polymorphic collections.

### Pattern 19
Understand dependency injection.

### Pattern 20
Understand Strategy Pattern.

---

# 68. Recognition Tricks — A to Z

## Pattern 1 — Same Name + Different Parameters

> [!important]
> If:
>
> ```text
> add(int,int)
> add(int,int,int)
> ```
>
> think:
>
> **Overloading**
>
> → Compile-Time Polymorphism

---

## Pattern 2 — Same Signature + Parent/Child

> [!important]
> If:
>
> ```text
> Parent.sound()
> Child.sound()
> ```
>
> with the same signature:
>
> think:
>
> **Overriding**
>
> → Runtime Polymorphism

---

## Pattern 3 — Parent Reference + Child Object

> [!important]
> If:
>
> ```java
> Parent p = new Child();
> ```
>
> and `Child` overrides the method:
>
> think:
>
> **Dynamic Method Dispatch**

---

## Pattern 4 — Static Method

> [!important]
> If the method is:
>
> ```java
> static
> ```
>
> do not apply normal runtime overriding rules.

---

## Pattern 5 — Final Method

> [!important]
> If the method is:
>
> ```java
> final
> ```
>
> it cannot be overridden.

---

## Pattern 6 — Private Method

> [!important]
> If the parent method is:
>
> ```java
> private
> ```
>
> the child declaration with the same signature is not overriding that private method.

---

## Pattern 7 — Interface Reference

> [!important]
> If:
>
> ```java
> Payment p = new UPI();
> ```
>
> and `UPI` implements `Payment`:
>
> think:
>
> **Interface-based runtime polymorphism**

---

## Pattern 8 — List of Parent Types

> [!important]
> If you see:
>
> ```java
> List<Animal>
> ```
>
> containing:
>
> ```text
> Dog
> Cat
> Cow
> ```
>
> think:
>
> **Polymorphic collection**

---

## Pattern 9 — `super.method()`

> [!important]
> If you see:
>
> ```java
> super.show();
> ```
>
> inside an override:
>
> think:
>
> **Explicit parent implementation call**

---

## Pattern 10 — Same Operation, Different Objects

> [!important]
> If the code uses:
>
> ```text
> payment.pay()
> ```
>
> for:
>
> ```text
> UPI
> Card
> Wallet
> ```
>
> think:
>
> **Polymorphism**

---

# 69. Shortcuts

> [!tip]
> **Shortcut 1 — OL vs OR**
>
> ```text
> OL = OverLoading
> → Different Parameters
> → Compile Time
>
> OR = OverRiding
> → Same Signature
> → Runtime
> ```

> [!tip]
> **Shortcut 2 — Compiler vs Object**
>
> ```text
> Overloading
> → Compiler decides
>
> Overriding
> → Actual object decides
> ```

> [!tip]
> **Shortcut 3 — Parent Ref Test**
>
> Whenever you see:
>
> ```java
> Parent p = new Child();
> ```
>
> ask:
>
> **Did Child override the method?**
>
> If yes:
>
> ```text
> Child implementation
> ```

> [!tip]
> **Shortcut 4 — Static/Final/Private Trap**
>
> Remember:
>
> ```text
> static  → hidden
> final   → cannot override
> private → not overridden
> ```
>
> Do not blindly call all three runtime polymorphism cases.

> [!tip]
> **Shortcut 5 — Access vs Execution**
>
> ```text
> Reference type
> → What can I call?
>
> Object type
> → Which overridden method runs?
> ```

> [!tip]
> **Shortcut 6 — Up vs Down**
>
> ```text
> Child → Parent = Upcasting
>
> Parent reference → Child reference
> = Downcasting
> ```

---

# 70. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Overloading Requires Inheritance

It does not.

Overloading can happen within the same class.

---

### Mistake 2 — Thinking Return Type Alone Creates Overloading

It does not.

The parameter list must differ.

---

### Mistake 3 — Confusing Overloading and Overriding

```text
Different parameters
→ Overloading

Same signature in child
→ Overriding
```

---

### Mistake 4 — Looking Only at Reference Type

Given:

```java
Animal a = new Dog();
```

Do not conclude that:

```text
Animal.sound()
```

must execute.

If `Dog` overrides `sound()`, runtime dispatch selects:

```text
Dog.sound()
```

---

### Mistake 5 — Assuming Child-Specific Methods Are Accessible

Given:

```java
Animal a = new Dog();
```

You cannot directly call:

```java
a.bark();
```

if `bark()` exists only in `Dog`.

---

### Mistake 6 — Applying Runtime Dispatch to Static Methods

Static methods are hidden, not dynamically overridden like instance methods.

---

### Mistake 7 — Calling Private Methods Overridden

Private methods are not overridden.

---

### Mistake 8 — Trying to Override Final Methods

A final method cannot be overridden.

---

### Mistake 9 — Unsafe Downcasting

This can fail:

```java
Animal a = new Cat();

Dog d = (Dog) a;
```

because the actual object is a `Cat`.

This can cause:

```text
ClassCastException
```

---

### Mistake 10 — Thinking Polymorphism Means Only Overriding

Polymorphism is a broader OOP concept.

In Java, important forms include:

```text
Overloading
Overriding
Interface-based polymorphism
```

---

# 71. Interview Questions

## Beginner

### Q1. What is polymorphism?

**Answer:**

Polymorphism means one interface or operation can have multiple forms of behavior.

---

### Q2. What are the two major types of polymorphism commonly discussed in Java?

**Answer:**

```text
Compile-Time Polymorphism
→ Method Overloading

Runtime Polymorphism
→ Method Overriding
```

---

### Q3. What is method overloading?

**Answer:**

Defining multiple methods with the same name but different parameter lists.

---

### Q4. What is method overriding?

**Answer:**

A child class provides its own implementation of an inherited instance method with the same signature.

---

### Q5. What is dynamic method dispatch?

**Answer:**

It is the runtime mechanism that selects the overridden instance method implementation based on the actual object.

---

# 72. Intermediate Interview Questions

### Q6. Is return type enough for method overloading?

**Answer:**

No.

The parameter list must differ.

---

### Q7. Is inheritance required for overloading?

**Answer:**

No.

Overloading can occur within a single class.

---

### Q8. Is inheritance required for overriding?

**Answer:**

An overriding relationship requires inheritance or an interface implementation relationship.

---

### Q9. Can static methods be overridden?

**Answer:**

No. Static methods are hidden rather than overridden dynamically.

---

### Q10. Can private methods be overridden?

**Answer:**

No. Private methods are not inherited in a way that permits overriding.

---

### Q11. Can final methods be overridden?

**Answer:**

No.

---

### Q12. What determines accessible members in `Parent p = new Child()`?

**Answer:**

The reference type, `Parent`, determines what members are accessible through `p`.

---

### Q13. What determines the implementation of an overridden instance method?

**Answer:**

The actual runtime object.

---

# 73. Advanced Interview Questions

### Q14. Explain:

```java
Animal a = new Dog();
```

**Answer:**

The reference type is `Animal`, while the actual object is `Dog`.

The reference type determines accessible members, while overridden instance-method behavior is selected based on the runtime object.

---

### Q15. What is upcasting?

**Answer:**

Assigning a child object to a parent reference.

```java
Animal a = new Dog();
```

---

### Q16. What is downcasting?

**Answer:**

Converting a compatible parent reference back to a child reference.

```java
Dog d = (Dog) a;
```

It is only safe when the actual object is compatible.

---

### Q17. Why is polymorphism useful?

**Answer:**

It reduces coupling, enables flexible implementations, simplifies client code, and allows new implementations to be introduced with minimal changes to existing consumers.

---

### Q18. How does polymorphism support extensibility?

**Answer:**

Code can depend on a parent class or interface rather than concrete implementations.

New implementations can then be added without changing the code that uses the common abstraction.

---

### Q19. What is covariant return type?

**Answer:**

When an overriding method returns a subtype of the return type declared by the parent method.

---

### Q20. What is the difference between early and late binding?

**Answer:**

Early binding associates a call at compile time, commonly seen with overloading and non-polymorphic method categories.

Late binding resolves an overridden instance method at runtime based on the actual object.

---

# 74. Interview Trap Questions

## Trap 1

**Question:**

Can a method be overloaded by changing only return type?

**Answer:**

No.

---

## Trap 2

**Question:**

Can static methods be overridden?

**Answer:**

No. They are hidden.

---

## Trap 3

**Question:**

Can a final method be overridden?

**Answer:**

No.

---

## Trap 4

**Question:**

Can a private method be overridden?

**Answer:**

No.

---

## Trap 5

**Question:**

Does `Parent p = new Child();` mean the object is a Parent?

**Answer:**

The actual object is a `Child`; the reference type is `Parent`.

---

## Trap 6

**Question:**

Can `p.childOnlyMethod()` be called through a parent reference?

**Answer:**

Not directly if the method is not declared in the parent reference type.

---

## Trap 7

**Question:**

Does overloading require inheritance?

**Answer:**

No.

---

## Trap 8

**Question:**

Does overriding happen at compile time?

**Answer:**

The selection of an overridden instance method is dynamic and occurs at runtime.

---

# 75. Output-Based Questions

## Question 1

```java
class Parent {

    void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    @Override
    void show() {
        System.out.println("Child");
    }
}

public class Main {

    public static void main(String[] args) {

        Parent p = new Child();

        p.show();
    }
}
```

### Answer

```text
Child
```

### Why?

```text
Reference → Parent
Object → Child
Child overrides show()
```

Therefore:

```text
Child.show()
```

---

# 76. Output-Based Question 2

```java
class Test {

    void show(int x) {
        System.out.println("int");
    }

    void show(double x) {
        System.out.println("double");
    }

    public static void main(String[] args) {

        Test t = new Test();

        t.show(10);
    }
}
```

### Answer

```text
int
```

### Why?

The argument is an `int`, so the compiler selects:

```text
show(int)
```

---

# 77. Output-Based Question 3

```java
class Parent {

    static void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    static void show() {
        System.out.println("Child");
    }
}

public class Main {

    public static void main(String[] args) {

        Parent p = new Child();

        p.show();
    }
}
```

### Answer

```text
Parent
```

### Why?

Static methods are hidden, not dynamically dispatched based on the runtime object.

---

# 78. Output-Based Question 4

```java
class Parent {

    final void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

}
```

What happens?

### Answer

The code is valid because `Child` does not attempt to override `show()`.

If `Child` attempted:

```java
@Override
void show() {
}
```

it would cause a compilation error.

---

# 79. Output-Based Question 5

```java
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

    void bark() {
        System.out.println("Bark");
    }
}

public class Main {

    public static void main(String[] args) {

        Animal a = new Dog();

        a.sound();
    }
}
```

Output:

```text
Dog
```

But:

```java
a.bark();
```

does not compile.

This is a classic interview question.

---

# 80. Real-World Architecture Pattern

A scalable application often looks like:

```text
                    Interface
                       |
          +------------+------------+
          |            |            |
          ↓            ↓            ↓
      Service A    Service B    Service C
```

The application uses:

```text
Interface
```

rather than:

```text
Concrete Service
```

This is polymorphism.

For example:

```text
PaymentService
       |
       +── UPIService
       +── CardService
       +── WalletService
```

Client:

```java
PaymentService service;
```

The actual implementation can vary.

---

# 81. Why Companies Use Polymorphism

Polymorphism helps systems become:

### Flexible

Implementations can change.

### Extensible

New implementations can be added.

### Maintainable

Common code works through abstractions.

### Testable

Mock implementations can be supplied.

### Loosely Coupled

Consumers do not need to depend on concrete classes.

### Reusable

Common code can operate on a parent/interface type.

---

# 82. Polymorphism in Frameworks

Polymorphism is heavily used in software frameworks.

Examples include:

```text
Collections
Database APIs
Logging
Web frameworks
Dependency Injection
Payment systems
File systems
Plugin architectures
Serialization
Messaging systems
```

The common pattern is:

```text
Interface / Parent
        ↓
Multiple Implementations
        ↓
Client uses abstraction
```

---

# 83. One Powerful Mental Model

Think:

```text
          WHAT
           ↓
     Interface / Parent
           ↓
          HOW
           ↓
 Different Implementations
```

For example:

```text
WHAT:
pay()

HOW:
UPI
Card
Wallet
```

The caller only needs to know:

```text
pay()
```

This is the power of polymorphism.

---

# 84. The Four OOP Pillars Connection

Polymorphism is one of the four fundamental OOP concepts.

```text
             OOP
              |
    +---------+---------+
    |         |         |
Encapsulation Inheritance Polymorphism
              |
          Abstraction
```

A more conventional list is:

```text
1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction
```

### Encapsulation

Protect data and implementation.

### Inheritance

Create an IS-A relationship.

### Polymorphism

Allow common operations to have different implementations.

### Abstraction

Expose essential behavior while hiding unnecessary implementation details.

---

# 85. Polymorphism — Complete Pattern Map

```text
                         POLYMORPHISM
                              |
              +---------------+---------------+
              |                               |
              ↓                               ↓
       COMPILE-TIME                       RUNTIME
              |                               |
              ↓                               ↓
        OVERLOADING                      OVERRIDING
              |                               |
              ↓                               ↓
      Different Parameters            Same Signature
              |                               |
              ↓                               ↓
        Compiler Decides              Object Decides
                                              |
                                              ↓
                                    Dynamic Method Dispatch
```

Remember this diagram.

---

# 86. Master Recognition Algorithm

When you see a Java question involving methods:

```text
STEP 1
Is the method name same?

      No
       ↓
Probably not overloading/overriding.

      Yes
       ↓

STEP 2
Are parameters different?

      Yes
       ↓
Overloading

      No
       ↓

STEP 3
Is there a parent-child relationship?

      Yes
       ↓
Check overriding

      No
       ↓
Probably not overriding.

STEP 4
Is the method static?

      Yes
       ↓
Method hiding, not dynamic overriding.

STEP 5
Is it final?

      Yes
       ↓
Cannot override.

STEP 6
Is it private?

      Yes
       ↓
Not overridden.

STEP 7
Is there Parent ref = new Child()?

      Yes
       ↓
Check dynamic dispatch.
```

---

# 87. Formula Sheet

```text
POLYMORPHISM
= One Interface / Operation → Many Forms

Compile-Time Polymorphism
= Method Overloading

Runtime Polymorphism
= Method Overriding
+ Dynamic Method Dispatch

Overloading:
Same method name
+
Different parameter list

Valid overload differences:
- Number of parameters
- Parameter types
- Parameter order

Return type alone:
NOT enough for overloading

Overriding:
Parent method
+
Child same signature
=
Specialized implementation

Parent reference:
Parent p = new Child();

Reference Type:
Determines accessible members

Actual Object Type:
Determines overridden instance-method behavior

Upcasting:
Child → Parent

Example:
Animal a = new Dog();

Downcasting:
Parent reference → Child reference

Example:
Dog d = (Dog) a;

static:
Hidden, not dynamically overridden

private:
Not overridden

final:
Cannot be overridden

super.method():
Explicit parent implementation

Interface:
Can support runtime polymorphism

Covariant Return:
Child return type can be subtype of parent return type

OL:
OverLoading
→ Different Parameters
→ Compile Time

OR:
OverRiding
→ Same Signature
→ Runtime
```

---

# 88. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Polymorphism means one interface or operation can take many forms of behavior.**

### Two Main Types

```text
Compile-Time
→ Overloading

Runtime
→ Overriding
→ Dynamic Method Dispatch
```

### Overloading

```text
Same name
+
Different parameters
```

Example:

```text
add(int,int)
add(int,int,int)
```

Compiler decides.

### Overriding

```text
Parent
↓
Child
↓
Same method signature
```

Runtime object decides.

### Dynamic Dispatch

```java
Animal a = new Dog();

a.sound();
```

If `Dog` overrides `sound()`:

```text
Dog.sound()
```

runs.

### Most Important Rule

```text
Reference Type
→ What can I access?

Actual Object
→ Which overridden method runs?
```

### Special Cases

```text
static  → hidden
private → not overridden
final   → cannot override
```

### Casting

```text
Child → Parent
= Upcasting

Parent reference → Child
= Downcasting
```

### Real-World Pattern

```text
Payment
 /  |  \
UPI Card Wallet
```

All expose:

```text
pay()
```

but each implements it differently.

### Golden Recognition

```text
Different parameters
→ Overloading
→ Compile Time

Same signature + Child
→ Overriding
→ Runtime

Parent ref + Child object
→ Dynamic Method Dispatch
```

### Golden Memory Trick

**Polymorphism = ONE common operation, MANY possible behaviors.**

### One-Line Recognition

**If the same method/interface can behave differently depending on parameters or the actual object, think Polymorphism.**