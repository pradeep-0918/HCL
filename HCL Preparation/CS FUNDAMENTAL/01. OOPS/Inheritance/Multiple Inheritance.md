---
type: concept
subject: aptitude
topic: "Multiple Inheritance"
parent: "Inheritance"
company: HCL
difficulty: hard
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - inheritance
  - multiple-inheritance
  - java
  - interfaces
  - object-oriented-programming
  - interview
wikilinks:
  - "[[OOP Basics]]"
  - "[[Inheritance]]"
  - "[[Single Inheritance]]"
  - "[[Multilevel Inheritance]]"
  - "[[Hierarchical Inheritance]]"
  - "[[Hybrid Inheritance]]"
  - "[[Polymorphism]]"
---

# Multiple Inheritance

> [!summary]
> **Multiple Inheritance** occurs when a single child class inherits from more than one parent class.
>
> The classic structure is:
>
> ```text
> Parent A       Parent B
>     \             /
>      \           /
>       \         /
>        Child C
> ```
>
> The key recognition rule is:
>
> **MULTIPLE PARENTS → ONE CHILD**

> [!important]
> **Java does NOT support multiple inheritance of classes.**
>
> Java can achieve multiple inheritance of type/behavior through **interfaces**.

---

# 1. Core Concept

Suppose we have:

```text
        Animal        Pet
           \          /
            \        /
             \      /
               Dog
```

Here `Dog` appears to inherit from two parents:

```text
Animal
Pet
```

This is the basic idea of multiple inheritance.

In a language that supports multiple class inheritance, the syntax might conceptually look like:

    class Dog extends Animal, Pet {
    }

But in Java, this is **not allowed**.

Java gives:

```text
class → extends → one class
class → implements → multiple interfaces
```

Therefore, Java avoids multiple inheritance of classes while still allowing a class to implement multiple interfaces.

---

# 2. Basic Meaning

The word **multiple** is the key.

```text
Multiple Parents
        ↓
    One Child
```

Compare:

```text
Single:
A → B

Multilevel:
A → B → C

Hierarchical:
    A
   / \
  B   C

Multiple:
A   B
 \ /
  C
```

The arrows tell you the inheritance type.

---

# 3. Main Formula

For exam recognition:

$$
\boxed{\text{Multiple Parents} \rightarrow \text{One Child}}
$$

or:

$$
\boxed{A + B \rightarrow C}
$$

Where:

```text
A = Parent 1
B = Parent 2
C = Child
```

### Fast Mental Formula

```text
MANY → ONE
```

means:

```text
Multiple Inheritance
```

> [!tip]
> **One parent → many children = Hierarchical**
>
> **Many parents → one child = Multiple**

This distinction is extremely important.

---

# 4. Why Is Multiple Inheritance Important?

Multiple inheritance can be useful when a class needs characteristics from multiple independent parent types.

For example, imagine a hypothetical system:

```text
Printer
Scanner
   \    /
    \  /
   MultiFunctionDevice
```

A multifunction device needs:

```text
Printer behavior
+
Scanner behavior
```

Conceptually:

```text
MultiFunctionDevice
      ↓
Can print
Can scan
```

However, instead of allowing Java classes to inherit from multiple classes, Java typically models such capabilities using interfaces.

---

# 5. Why Java Does Not Support Multiple Class Inheritance

This is one of the most important OOP interview questions.

Consider:

```text
          A
         / \
        B   C
         \ /
          D
```

Suppose:

```text
A → show()
```

`B` overrides:

```text
show() → "B"
```

`C` overrides:

```text
show() → "C"
```

Now `D` inherits from both `B` and `C`.

Question:

```text
D d = new D();

d.show();
```

Which method should execute?

```text
B.show()?
```

or:

```text
C.show()?
```

There is ambiguity.

This is called the:

$$
\boxed{\text{Diamond Problem}}
$$

---

# 6. Diamond Problem

The diagram:

```text
        A
       / \
      B   C
       \ /
        D
```

looks like a diamond.

Hence:

**Diamond Problem**

### Problem

`D` receives two possible paths to `A`:

```text
D → B → A
D → C → A
```

If `B` and `C` contain conflicting implementations, `D` may not know which implementation to use.

This creates ambiguity.

> [!important]
> **The diamond problem is a major reason Java does not allow multiple inheritance of classes.**

---

# 7. Java's Solution

Java separates:

### Class Inheritance

```text
class B extends A
```

A class can have:

```text
ONE direct superclass
```

### Interface Implementation

A class can implement multiple interfaces:

    class SmartDevice implements Camera, GPS, MusicPlayer {
    }

Conceptually:

```text
Camera      GPS      MusicPlayer
   \         |          /
    \        |         /
       SmartDevice
```

This allows a class to acquire multiple capabilities without inheriting from multiple concrete classes.

---

# 8. `extends` vs `implements`

This is one of the most important interview tables.

| Relationship | Keyword | Number |
|---|---|---:|
| Class → Class | `extends` | One direct superclass |
| Class → Interface | `implements` | Multiple interfaces possible |
| Interface → Interface | `extends` | Multiple interfaces possible |

Examples:

### Class Extending Class

    class Dog extends Animal {
    }

### Class Implementing Multiple Interfaces

    class Smartphone implements Camera, GPS, MusicPlayer {
    }

### Interface Extending Multiple Interfaces

    interface SmartDevice extends Camera, GPS {
    }

> [!important]
> **`extends` does not mean "multiple classes are allowed."**
>
> A Java class can extend only one class.

---

# 9. Real-Time Example — Smartphone

Think about a smartphone.

A smartphone can:

```text
Make calls
Take photos
Use GPS
Play music
Access internet
```

You could conceptually think:

```text
Phone
Camera
GPS
MusicPlayer
      \
       \
     Smartphone
```

In Java, interfaces are ideal for representing these capabilities.

    interface Camera {

        void takePhoto();
    }

    interface GPS {

        void getLocation();
    }

    interface MusicPlayer {

        void playMusic();
    }

    class Smartphone implements Camera, GPS, MusicPlayer {

        public void takePhoto() {
            System.out.println("Taking photo");
        }

        public void getLocation() {
            System.out.println("Getting location");
        }

        public void playMusic() {
            System.out.println("Playing music");
        }
    }

Now:

    Smartphone phone = new Smartphone();

    phone.takePhoto();
    phone.getLocation();
    phone.playMusic();

The smartphone implements multiple capabilities.

---

# 10. Real-Time Example — MultiFunction Printer

Consider:

```text
Printer
Scanner
   \   /
    \ /
MultiFunctionPrinter
```

A device may need:

```text
print()
scan()
```

Interfaces:

    interface Printer {

        void print();
    }

    interface Scanner {

        void scan();
    }

    class MultiFunctionPrinter implements Printer, Scanner {

        public void print() {
            System.out.println("Printing");
        }

        public void scan() {
            System.out.println("Scanning");
        }
    }

This is a very common real-world way to understand multiple interfaces.

---

# 11. Real-Time Example — Payment System

Suppose a payment application requires multiple capabilities:

```text
PaymentProcessor
Refundable
Auditable
```

A class could implement:

    class OnlinePayment
        implements PaymentProcessor, Refundable, Auditable {
    }

The class combines multiple contracts.

This is often preferable to creating multiple parent classes.

---

# 12. Real-Time Example — Employee Roles

Imagine an employee who is both:

```text
Developer
TeamLead
```

Instead of multiple parent classes, interfaces can represent capabilities.

    interface Developer {

        void writeCode();
    }

    interface TeamLead {

        void manageTeam();
    }

    class SeniorDeveloper implements Developer, TeamLead {

        public void writeCode() {
            System.out.println("Writing code");
        }

        public void manageTeam() {
            System.out.println("Managing team");
        }
    }

The class has multiple capabilities.

---

# 13. Real-Time Example — E-Commerce

A system may have:

```text
Payable
Shippable
Trackable
```

A product order may implement multiple interfaces:

    class Order implements Payable, Shippable, Trackable {
    }

The class can provide:

```text
pay()
ship()
track()
```

This demonstrates how interfaces can model multiple capabilities.

---

# 14. Real-Time Example — Gaming Character

A game character may have multiple abilities:

```text
Flyable
Attackable
Movable
```

A class:

    class SuperHero implements Flyable, Attackable, Movable {
    }

The character has multiple capabilities without inheriting from multiple concrete classes.

---

# 15. Multiple Inheritance of Type vs Class

This is a higher-level interview concept.

Java does not support:

```text
Multiple inheritance of classes
```

But Java does allow a class to implement multiple interfaces.

Therefore, a class can have multiple **types**.

Example:

    interface A {
    }

    interface B {
    }

    class C implements A, B {
    }

Then:

```text
C is an A
C is a B
```

Conceptually:

$$
\boxed{C \text{ has multiple interface types}}
$$

This is sometimes described as multiple inheritance of type.

---

# 16. Interface-Based Multiple Inheritance

Consider:

    interface A {

        void showA();
    }

    interface B {

        void showB();
    }

    class C implements A, B {

        public void showA() {
            System.out.println("A");
        }

        public void showB() {
            System.out.println("B");
        }
    }

Now:

    C obj = new C();

    obj.showA();
    obj.showB();

Output:

```text
A
B
```

`C` satisfies both interfaces.

---

# 17. Default Methods and the Diamond Problem

Modern Java interfaces can contain `default` methods.

Example:

    interface A {

        default void show() {
            System.out.println("A");
        }
    }

    interface B {

        default void show() {
            System.out.println("B");
        }
    }

Now:

    class C implements A, B {
    }

This creates a conflict because both interfaces provide a default implementation of `show()`.

Java does not silently choose one.

The class must resolve the conflict.

Example:

    class C implements A, B {

        @Override
        public void show() {

            A.super.show();

            System.out.println("C");
        }
    }

This is an advanced interview topic.

> [!important]
> Java avoids class-level multiple inheritance, but interface default methods can still create conflicts that the implementing class must resolve.

---

# 18. Why Interfaces Are Safer

Suppose:

```text
A
B
```

both provide the same abstract method:

```text
show()
```

A class implementing both can provide one implementation:

    class C implements A, B {

        public void show() {
            System.out.println("C");
        }
    }

The class decides how to implement the contract.

This avoids inheriting two competing concrete class implementations.

---

# 19. Basic Examples

## Example 1 — Identify Multiple Inheritance

**Question**

Which diagram represents multiple inheritance?

```text
A.

A
|
B


B.

A
/ \
B  C


C.

A   B
 \ /
  C


D.

A
|
B
|
C
```

### Analysis

```text
A → Single
B → Hierarchical
C → Multiple
D → Multilevel
```

### Answer

$$
\boxed{\text{C}}
$$

---

# 20. Example 2 — Identify the Parents

**Question**

Consider:

```text
A     B
 \   /
   C
```

Which classes are the parents?

### Analysis

Both arrows point toward `C`.

Therefore:

```text
A → Parent
B → Parent
C → Child
```

### Answer

$$
\boxed{A \text{ and } B}
$$

---

# 21. Example 3 — Identify the Child

**Question**

```text
A     B
 \   /
   C
```

Which class has multiple parents?

### Answer

```text
C
```

Therefore:

$$
\boxed{C}
$$

---

# 22. Example 4 — Java Validity

**Question**

Is this valid Java?

    class A {
    }

    class B {
    }

    class C extends A, B {
    }

### Analysis

Java does not allow a class to extend multiple classes.

### Answer

$$
\boxed{\text{Invalid}}
$$

---

# 23. Example 5 — Multiple Interfaces

**Question**

Is this valid Java?

    interface A {
    }

    interface B {
    }

    class C implements A, B {
    }

### Analysis

A Java class can implement multiple interfaces.

### Answer

$$
\boxed{\text{Valid}}
$$

---

# 24. Medium Example — Interface Implementation

## Example 6

Consider:

    interface Printable {

        void print();
    }

    interface Scannable {

        void scan();
    }

    class Machine implements Printable, Scannable {

        public void print() {
            System.out.println("Print");
        }

        public void scan() {
            System.out.println("Scan");
        }
    }

What does `Machine` represent?

### Analysis

```text
Printable
     \
      Machine
     /
Scannable
```

The class implements multiple interfaces.

### Answer

It demonstrates:

$$
\boxed{\text{Multiple Interface Implementation}}
$$

---

# 25. Medium Example — Parent Type References

Consider:

    interface A {

        void show();
    }

    interface B {

        void show();
    }

    class C implements A, B {

        public void show() {
            System.out.println("C");
        }
    }

Now:

    A obj = new C();

    obj.show();

Output:

```text
C
```

Why?

The actual object is `C`, and `C` provides the implementation.

---

# 26. Advanced Example — Default Method Conflict

Consider:

    interface A {

        default void show() {
            System.out.println("A");
        }
    }

    interface B {

        default void show() {
            System.out.println("B");
        }
    }

    class C implements A, B {

        @Override
        public void show() {
            System.out.println("C");
        }
    }

Now:

    C obj = new C();

    obj.show();

Output:

```text
C
```

The class resolves the conflict by providing its own implementation.

---

# 27. Advanced Example — Calling a Specific Interface Default

Consider:

    interface A {

        default void show() {
            System.out.println("A");
        }
    }

    interface B {

        default void show() {
            System.out.println("B");
        }
    }

    class C implements A, B {

        @Override
        public void show() {

            A.super.show();

            System.out.println("C");
        }
    }

Output:

```text
A
C
```

Here:

```text
A.super.show()
```

explicitly calls the default method from interface `A`.

---

# 28. Multiple Inheritance vs Multiple Interface Implementation

These terms should not be used carelessly.

### Strict Java Class Inheritance

```text
class C extends A
```

Only one direct superclass.

### Multiple Interface Implementation

```text
class C implements A, B
```

Multiple interfaces.

A technically accurate interview answer is:

> **Java does not support multiple inheritance of classes, but it supports implementing multiple interfaces.**

This is better than simply saying:

> "Java supports multiple inheritance."

because that answer is incomplete.

---

# 29. Multiple Inheritance vs Hierarchical Inheritance

This is the most important comparison.

### Hierarchical

```text
      A
     / \
    B   C
```

Direction:

```text
ONE → MANY
```

### Multiple

```text
    A   B
     \ /
      C
```

Direction:

```text
MANY → ONE
```

### Golden Shortcut

$$
\boxed{1 \rightarrow N = \text{Hierarchical}}
$$

$$
\boxed{N \rightarrow 1 = \text{Multiple}}
$$

---

# 30. Multiple vs Multilevel

### Multiple

```text
A   B
 \ /
  C
```

Multiple parents.

### Multilevel

```text
A
↓
B
↓
C
```

Multiple levels.

> [!tip]
> **Multiple asks "How many parents?"**
>
> **Multilevel asks "How many levels?"**

This is an excellent exam trick.

---

# 31. Multiple vs Hybrid

### Multiple

The structure specifically contains multiple parents for one child.

```text
A   B
 \ /
  C
```

### Hybrid

More than one inheritance pattern is combined.

Example:

```text
       A
      / \
     B   C
     |
     D
```

This contains:

```text
Hierarchical
+
Multilevel
```

So it is a mixed/hybrid structure.

---

# 32. Multiple Inheritance and the Diamond Problem

Let's understand the diamond problem deeply.

Consider:

```text
          A
        /   \
       B     C
        \   /
          D
```

Suppose `A` has:

    void show() {
        System.out.println("A");
    }

Suppose `B` and `C` both inherit `show()`.

If `D` inherits from both:

```text
D → B → A
D → C → A
```

Java would have to determine how the inherited state and implementation should be resolved.

If `B` and `C` override the method differently:

```text
B → show() = "B"
C → show() = "C"
```

then:

```text
D.show()
```

has an ambiguity.

Which one?

```text
B?
C?
```

This is the core diamond problem.

---

# 33. Why the Diamond Problem Is Dangerous

The problem is not simply the existence of two parents.

The bigger issue is:

```text
Ambiguous inherited state
+
Ambiguous inherited behavior
+
Complex method resolution
```

Possible conflicts include:

- Which method?
- Which field?
- Which constructor?
- Which parent implementation?
- Which initialization order?

Avoiding class-level multiple inheritance simplifies these issues.

---

# 34. Java's Object Model

Every Java class ultimately derives from:

```text
Object
```

Conceptually:

```text
Object
  ↓
Animal
  ↓
Dog
```

or:

```text
Object
  ↓
Vehicle
 /    \
Car   Bike
```

Even when you don't explicitly write:

    extends Object

Java classes ultimately have `Object` as their root superclass, except interfaces, which have different inheritance semantics.

This is useful for interviews involving:

```text
toString()
equals()
hashCode()
getClass()
```

---

# 35. Important Java Rule

A Java class can:

```text
extend ONE class
```

and:

```text
implement MANY interfaces
```

Example:

    class Smartphone extends Device
        implements Camera, GPS, MusicPlayer {
    }

This is completely valid.

Visual:

```text
             Device
                |
                ↓
          Smartphone
          /    |    \
         /     |     \
     Camera   GPS   MusicPlayer
```

This design combines:

```text
Class inheritance
+
Multiple interface implementation
```

---

# 36. Hybrid Structure in Java

A class can participate in a structure like:

```text
          Device
             |
             ↓
        Smartphone
          /    \
         /      \
     Camera      GPS
```

Where:

```text
Device → Smartphone
```

is class inheritance.

And:

```text
Smartphone implements Camera, GPS
```

is multiple interface implementation.

This is often a more practical Java design than multiple class inheritance.

---

# 37. Real-Time System Design Example

Consider a smart home device.

```text
                 Device
                    |
                    ↓
               SmartDevice
                /       \
               /         \
          Camera        Speaker
```

Or capabilities:

```text
Camera
AudioPlayer
InternetConnected
```

A class might implement:

    class SmartSecurityCamera
        extends SmartDevice
        implements Camera, AudioPlayer, NetworkDevice {
    }

This gives:

```text
One class parent
+
Multiple interfaces
```

This is a powerful pattern in Java.

---

# 38. Interface Segregation Connection

Multiple interfaces work particularly well when each interface represents one focused capability.

Instead of:

```text
HugeParentClass
```

we can have:

```text
Printable
Scannable
Faxable
```

Then:

    class Printer implements Printable {
    }

    class MultiFunctionPrinter
        implements Printable, Scannable, Faxable {
    }

This keeps responsibilities separate.

This idea connects strongly with the **Interface Segregation Principle** from SOLID.

---

# 39. When Multiple Capabilities Are Better Than Multiple Classes

Suppose a device can:

```text
Print
Scan
Copy
```

Instead of creating:

```text
PrinterScannerCopier
```

with multiple class inheritance, use interfaces:

    interface Printable {
        void print();
    }

    interface Scannable {
        void scan();
    }

    interface Copyable {
        void copy();
    }

Then:

    class MultiFunctionMachine
        implements Printable, Scannable, Copyable {
    }

This is flexible and modular.

---

# 40. Recognition Tricks — A to Z

## Pattern 1 — Many Parents

> [!important]
> If one class receives arrows from multiple parent classes:
>
> ```text
> A   B
>  \ /
>   C
> ```
>
> Think:
>
> **Multiple Inheritance**

---

## Pattern 2 — `extends A, B`

> [!important]
> If you see:
>
> ```java
> class C extends A, B
> ```
>
> immediately think:
>
> **Invalid Java**

---

## Pattern 3 — `implements A, B`

> [!important]
> If you see:
>
> ```java
> class C implements A, B
> ```
>
> think:
>
> **Valid multiple interface implementation**

---

## Pattern 4 — Diamond

> [!important]
> If the diagram looks like:
>
> ```text
>     A
>    / \
>   B   C
>    \ /
>     D
> ```
>
> think:
>
> **Diamond Problem**

---

## Pattern 5 — Same Default Method

> [!important]
> If two interfaces contain the same `default` method:
>
> ```text
> A.default show()
> B.default show()
> ```
>
> and one class implements both:
>
> the class must resolve the conflict.

---

## Pattern 6 — One Class + Many Interfaces

> [!important]
> If you see:
>
> ```java
> class C extends A implements B, D
> ```
>
> think:
>
> **One superclass + multiple interfaces**

---

## Pattern 7 — `A.super.method()`

> [!important]
> If you see:
>
> ```java
> A.super.show();
> ```
>
> inside a class implementing `A`:
>
> think:
>
> **Call interface A's default implementation.**

---

## Pattern 8 — Many → One

> [!important]
> Memorize:
>
> ```text
> Many Parents
>       ↓
> One Child
>       ↓
> Multiple
> ```

---

# 41. Shortcuts

> [!tip]
> **Shortcut 1 — Arrow Direction**
>
> Count where arrows come FROM.
>
> ```text
> A   B
>  \ /
>   C
> ```
>
> Two parents → Multiple.

> [!tip]
> **Shortcut 2 — `extends`**
>
> In Java:
>
> ```text
> class → extends → ONE class
> ```
>
> Never assume multiple classes can appear after `extends`.

> [!tip]
> **Shortcut 3 — `implements`**
>
> ```text
> class → implements → MANY interfaces
> ```
>
> This is the standard Java solution for multiple capabilities.

> [!tip]
> **Shortcut 4 — Diamond**
>
> Whenever you see:
>
> ```text
>   A
>  / \
> B   C
>  \ /
>   D
> ```
>
> immediately recall:
>
> **Diamond Problem**

> [!tip]
> **Shortcut 5 — Multiple vs Multilevel**
>
> Ask:
>
> ```text
> Multiple parents?
> → Multiple
>
> Multiple levels?
> → Multilevel
> ```

> [!tip]
> **Shortcut 6 — Multiple vs Hierarchical**
>
> ```text
> One parent → many children
> = Hierarchical
>
> Many parents → one child
> = Multiple
> ```

---

# 42. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Identify multiple inheritance from a diagram.

### Pattern 2
Differentiate multiple and hierarchical inheritance.

### Pattern 3
Differentiate multiple and multilevel inheritance.

### Pattern 4
Identify the diamond problem.

### Pattern 5
Determine whether Java code using multiple `extends` is valid.

### Pattern 6
Identify multiple interface implementation.

### Pattern 7
Understand `extends` vs `implements`.

### Pattern 8
Understand default-method conflicts.

### Pattern 9
Understand interface-based multiple inheritance.

### Pattern 10
Trace parent-reference behavior.

### Pattern 11
Understand why Java avoids multiple class inheritance.

### Pattern 12
Recognize hybrid Java designs.

### Pattern 13
Understand common-interface contracts.

### Pattern 14
Understand runtime polymorphism with multiple interfaces.

### Pattern 15
Identify IS-A vs capability-based relationships.

---

# 43. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Saying Java Supports Multiple Class Inheritance

Incorrect:

```text
Java supports multiple class inheritance.
```

Correct:

```text
Java does not support multiple inheritance of classes.
Java supports implementing multiple interfaces.
```

---

### Mistake 2 — Confusing Multiple With Hierarchical

```text
A   B
 \ /
  C
```

→ Multiple.

```text
A
/ \
B C
```

→ Hierarchical.

---

### Mistake 3 — Thinking `implements` Means Class Inheritance

`implements` means a class implements an interface contract.

It is not the same as:

```text
class extends class
```

---

### Mistake 4 — Ignoring Default Method Conflicts

If two interfaces provide conflicting default methods, the implementing class may need to resolve the conflict.

---

### Mistake 5 — Thinking Interfaces Cannot Have Implementations

Modern Java interfaces can contain default and static methods, so interface conflicts can occur.

---

### Mistake 6 — Saying Multiple Interfaces Cause the Diamond Problem Exactly Like Multiple Classes

The classic diamond problem is associated with multiple inheritance of classes.

Java's interface rules provide explicit conflict-resolution mechanisms.

---

### Mistake 7 — Using `extends` With Multiple Classes

Invalid:

    class C extends A, B {
    }

Valid:

    class C implements A, B {
    }

when `A` and `B` are interfaces.

---

### Mistake 8 — Confusing Capability With IS-A

Interfaces can model capabilities:

```text
Flyable
Printable
Serializable
Comparable
```

They do not necessarily represent a concrete parent class in the same sense as class inheritance.

---

# 44. Interview Questions

## Beginner

### Q1. What is multiple inheritance?

**Answer:**

Multiple inheritance is a model in which one child class inherits from multiple parent classes.

Conceptually:

```text
A   B
 \ /
  C
```

---

### Q2. Does Java support multiple inheritance?

**Answer:**

Java does not support multiple inheritance of classes.

However, a class can implement multiple interfaces.

---

### Q3. Why doesn't Java support multiple class inheritance?

**Answer:**

One major reason is avoiding ambiguity such as the diamond problem, where multiple parent classes could provide conflicting implementations.

---

### Q4. What keyword is used to implement multiple interfaces?

**Answer:**

`implements`.

Example:

    class C implements A, B {
    }

---

### Q5. How many classes can a Java class extend?

**Answer:**

One direct superclass.

---

## Intermediate

### Q6. How many interfaces can a Java class implement?

**Answer:**

A Java class can implement multiple interfaces, subject to practical language/compiler constraints.

---

### Q7. What is the diamond problem?

**Answer:**

The diamond problem occurs when a class could inherit the same ancestor through multiple paths, potentially causing ambiguity about which implementation or state should be used.

---

### Q8. What is the difference between `extends` and `implements`?

**Answer:**

`extends` is used for class inheritance, while `implements` is used when a class implements one or more interfaces.

---

### Q9. Can an interface extend multiple interfaces?

**Answer:**

Yes. Java interfaces can extend multiple interfaces.

Example:

    interface C extends A, B {
    }

---

### Q10. Can a class extend one class and implement multiple interfaces?

**Answer:**

Yes.

Example:

    class C extends A implements B, D {
    }

---

# 45. Advanced Interview Questions

### Q11. What happens if two interfaces have the same abstract method?

Suppose:

    interface A {
        void show();
    }

    interface B {
        void show();
    }

A class can implement both and provide one implementation:

    class C implements A, B {

        public void show() {
            System.out.println("C");
        }
    }

This is valid because both interfaces require the same contract.

---

### Q12. What happens if two interfaces have conflicting default methods?

Example:

    interface A {

        default void show() {
            System.out.println("A");
        }
    }

    interface B {

        default void show() {
            System.out.println("B");
        }
    }

Then:

    class C implements A, B {

        @Override
        public void show() {
            System.out.println("C");
        }
    }

The class resolves the conflict.

---

### Q13. Can an interface extend two interfaces?

Yes.

    interface A {
    }

    interface B {
    }

    interface C extends A, B {
    }

This is valid.

---

### Q14. Can a class extend two interfaces?

No.

Interfaces are implemented:

    class C implements A, B {
    }

---

### Q15. Can a class extend one class and implement two interfaces?

Yes.

    class C extends A implements B, D {
    }

This is one of the most useful Java inheritance patterns.

---

# 46. Advanced Output Question

Consider:

    interface A {

        default void show() {
            System.out.println("A");
        }
    }

    interface B {

        default void show() {
            System.out.println("B");
        }
    }

    class C implements A, B {

        public void show() {
            System.out.println("C");
        }
    }

    public class Main {

        public static void main(String[] args) {

            C obj = new C();

            obj.show();
        }
    }

What is the output?

### Step 1

`C` implements both `A` and `B`.

### Step 2

Both interfaces contain `show()`.

### Step 3

`C` provides its own implementation.

### Step 4

The class implementation wins.

### Answer

```text
C
```

---

# 47. Advanced Output Question — Interface Reference

Consider:

    interface A {

        default void show() {
            System.out.println("A");
        }
    }

    interface B {

        default void show() {
            System.out.println("B");
        }
    }

    class C implements A, B {

        @Override
        public void show() {
            System.out.println("C");
        }
    }

Now:

    A obj = new C();

    obj.show();

### Actual Object

```text
C
```

### Implementation

```text
C.show()
```

### Answer

```text
C
```

---

# 48. High-Level Design Insight

The biggest lesson from multiple inheritance is not merely:

> "Java doesn't support it."

The deeper idea is:

```text
Inheritance
     ↓
Relationship

Interface
     ↓
Capability / Contract
```

Example:

```text
Dog IS-A Animal
```

Inheritance.

But:

```text
Dog CAN-FLY
```

may be better represented by:

```text
Flyable
```

if flying is a capability rather than a parent class identity.

This distinction leads to better software design.

---

# 49. Composition Alternative

Suppose we want a class to have multiple capabilities.

Instead of:

```text
Multiple Parent Classes
```

we can use composition.

Example:

    class Engine {
    }

    class GPS {
    }

    class Car {

        Engine engine;
        GPS gps;
    }

This means:

```text
Car HAS-A Engine
Car HAS-A GPS
```

Composition can avoid complex inheritance hierarchies.

---

# 50. Interview Rule — "Prefer Composition Over Inheritance"

This phrase often appears in software interviews.

It does **not** mean:

> Never use inheritance.

It means:

> When inheritance creates unnecessary coupling or the relationship is not a genuine IS-A relationship, composition may provide a more flexible design.

Example:

```text
Car HAS-A Engine
```

Composition is natural.

```text
Dog IS-A Animal
```

Inheritance is natural.

---

# 51. Placement Exam Strategy

When you see an inheritance diagram:

### Step 1 — Count Parents

```text
One?
Many?
```

### Step 2 — Count Children

```text
One?
Many?
```

### Step 3 — Look at Direction

```text
One → One
One → Many
Many → One
Chain
```

### Step 4 — Classify

```text
1 → 1
Single

1 → Many
Hierarchical

Many → 1
Multiple

Chain
Multilevel

Mixed
Hybrid
```

### Step 5 — For Java Code

Check:

```text
extends
implements
```

### Step 6 — For Interface Questions

Check:

```text
abstract method?
default method?
conflict?
class implementation?
```

---

# 52. Ultimate Recognition Table

| Structure | Meaning | Pattern |
|---|---|---|
| `A → B` | One parent, one child | Single |
| `A → B → C` | Chain | Multilevel |
| `A → B` and `A → C` | One parent, many children | Hierarchical |
| `A + B → C` | Many parents, one child | Multiple |
| Combination | Mixed patterns | Hybrid |

### Visual Memory

```text
SINGLE

A
↓
B


MULTILEVEL

A
↓
B
↓
C


HIERARCHICAL

    A
   / \
  B   C


MULTIPLE

A   B
 \ /
  C


HYBRID

    A
   / \
  B   C
  |
  D
```

---

# 53. Formula Sheet

```text
Multiple Inheritance
= Multiple Parents → One Child

Recognition:
A + B → C

Direction:
Many → One

Classic Diamond:

    A
   / \
  B   C
   \ /
    D

Diamond Problem:
Ambiguity caused by multiple inheritance paths.

Java:
Class extends → ONE class

Class implements → MULTIPLE interfaces

Interface extends → MULTIPLE interfaces possible

Valid:
class C extends A implements B, D {
}

Invalid:
class C extends A, B {
}

Same abstract method:
One implementation can satisfy both interfaces.

Conflicting default methods:
Implementing class must resolve the conflict.

IS-A:
Inheritance relationship

HAS-A:
Composition/Aggregation

Multiple Interfaces:
Multiple capabilities/contracts

Multiple Class Inheritance:
Not supported by Java
```

---

# 54. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Multiple inheritance means one child class inherits from multiple parent classes.**

### Visual

```text
Parent A     Parent B
    \           /
     \         /
       Child
```

### Java Rule

```text
class → extends → ONE class

class → implements → MANY interfaces
```

### Remember

- Multiple inheritance = many parents → one child.
- Java does not support multiple inheritance of classes.
- Java supports multiple interface implementation.
- `extends` is used for class inheritance.
- `implements` is used for interfaces.
- The diamond problem is a major issue with multiple class inheritance.
- Interfaces provide a safer way to model multiple capabilities.
- Two interfaces can declare the same abstract method.
- One class implementation can satisfy both contracts.
- Conflicting default methods must be resolved.
- A class can extend one class and implement multiple interfaces.
- An interface can extend multiple interfaces.
- `A.super.method()` can explicitly invoke an interface default implementation.
- Composition is an alternative to complex inheritance.
- `IS-A` → inheritance.
- `HAS-A` → composition/aggregation.
- Multiple ≠ Multilevel.
- Multiple ≠ Hierarchical.
- Always inspect arrow direction.

### Master Memory

```text
ONE → MANY
    = Hierarchical

MANY → ONE
    = Multiple

CHAIN
    = Multilevel
```

### Golden Memory Trick

**Multiple inheritance means MANY parents come together to form ONE child.**

### One-Line Recognition

**If one class would need more than one parent, think Multiple Inheritance; in Java, model this through multiple interfaces rather than multiple parent classes.**