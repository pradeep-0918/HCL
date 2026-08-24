---
type: concept
subject: aptitude
topic: "Compile Time Polymorphism"
parent: "Polymorphism"
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
  - method-overloading
  - static-binding
  - java
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Polymorphism]]"
  - "[[Method Overloading]]"
  - "[[Runtime Polymorphism]]"
  - "[[Method Overriding]]"
  - "[[Dynamic Method Dispatch]]"
---

# Compile Time Polymorphism

> [!summary]
> **Compile Time Polymorphism** is a form of polymorphism in which the compiler determines which method or operation should be selected during compilation.
>
> In Java, the primary example is **Method Overloading**.
>
> Core pattern:
>
> **Same method name + different parameter list = Method Overloading**
>
> **Method Overloading = Compile Time Polymorphism**

---

# 1. Core Concept

The word polymorphism comes from:

- `Poly` → Many
- `Morphism` → Forms

Therefore:

$$
\boxed{\text{Polymorphism} = \text{One concept represented in multiple forms}}
$$

In Java, polymorphism mainly appears in two important forms:

| Type | Main Mechanism | Binding |
|---|---|---|
| Compile Time Polymorphism | Method Overloading | Static / Early Binding |
| Runtime Polymorphism | Method Overriding | Dynamic / Late Binding |

The most important placement rule is:

$$
\boxed{\text{Overloading} \rightarrow \text{Compile Time}}
$$

$$
\boxed{\text{Overriding} \rightarrow \text{Runtime}}
$$

---

# 2. Basic Meaning

Suppose a calculator needs to add:

```text
2 integers
3 integers
2 doubles
```

Instead of creating completely different method names:

```text
addTwoIntegers()
addThreeIntegers()
addTwoDoubles()
```

we can use the same method name:

```text
add()
```

with different parameters.

Example:

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

Now:

    Calculator c = new Calculator();

    c.add(10, 20);
    c.add(10, 20, 30);
    c.add(10.5, 20.5);

The method name remains:

```text
add()
```

but the parameter lists are different:

```text
add(int, int)
add(int, int, int)
add(double, double)
```

The compiler can determine which overloaded method matches the call.

Therefore:

$$
\boxed{\text{Method Overloading} \Rightarrow \text{Compile Time Polymorphism}}
$$

---

# 3. Why Is It Called Compile Time Polymorphism?

Consider:

    class Calculator {

        void add(int a, int b) {
            System.out.println("int");
        }

        void add(double a, double b) {
            System.out.println("double");
        }
    }

Suppose we write:

    Calculator c = new Calculator();

    c.add(10, 20);

The compiler sees:

```text
10 → int
20 → int
```

Therefore the matching method is:

    add(int, int)

The selection of the overloaded method is based on the method call's argument information during compilation.

Conceptually:

```text
Method Call
    ↓
Examine arguments
    ↓
Find applicable overload
    ↓
Select method
    ↓
Compile
```

Hence:

$$
\boxed{\text{Compile Time} \rightarrow \text{Method Selection}}
$$

---

# 4. Static Polymorphism

Compile-time polymorphism is also commonly called:

- Static Polymorphism
- Early Binding
- Static Binding
- Compile-Time Binding

The central idea is:

```text
Compiler
   ↓
Method selection
```

rather than:

```text
Runtime object
   ↓
Dynamic method dispatch
```

Do not confuse:

```text
Static polymorphism
```

with:

```text
static keyword
```

They are not the same thing.

A method does not need to be declared `static` to participate in compile-time polymorphism.

---

# 5. Main Rule

For method overloading:

$$
\boxed{\text{Same Method Name} + \text{Different Parameter List}}
$$

The parameter list can differ by:

1. Number of parameters
2. Parameter types
3. Parameter order

Therefore:

$$
\boxed{
\text{Count} \;|\; \text{Type} \;|\; \text{Order}
}
$$

These are the three major recognition points.

---

# 6. Method Signature

A Java method signature consists of:

```text
Method name
+
Parameter types
```

Example:

    int add(int a, int b)

Signature:

```text
add(int, int)
```

Another method:

    double add(double a, double b)

Signature:

```text
add(double, double)
```

These signatures are different.

Therefore overloading is possible.

---

# 7. What Is NOT Part of the Method Signature?

The return type is not part of the Java method signature for overload distinction.

This is invalid:

    class Demo {

        int getValue() {
            return 10;
        }

        double getValue() {
            return 10.5;
        }
    }

Both have:

```text
getValue()
```

The only difference is:

```text
int
double
```

which is the return type.

Therefore:

$$
\boxed{\text{Return Type Alone Cannot Overload a Method}}
$$

---

# 8. Pattern 1 — Different Number of Parameters

Example:

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        int add(int a, int b, int c) {
            return a + b + c;
        }
    }

Signatures:

```text
add(int, int)
add(int, int, int)
```

The parameter count differs.

Therefore:

$$
\boxed{\text{Method Overloading}}
$$

and:

$$
\boxed{\text{Compile Time Polymorphism}}
$$

---

# 9. Pattern 2 — Different Parameter Types

Example:

    class Printer {

        void print(int value) {
            System.out.println("Integer");
        }

        void print(String value) {
            System.out.println("String");
        }
    }

Signatures:

```text
print(int)
print(String)
```

The parameter type differs.

Therefore:

$$
\boxed{\text{Overloading}}
$$

---

# 10. Pattern 3 — Different Parameter Order

This is an important interview pattern.

Example:

    class Demo {

        void display(int a, String b) {
            System.out.println("int, String");
        }

        void display(String a, int b) {
            System.out.println("String, int");
        }
    }

The parameter count is the same:

```text
2
```

But the order differs:

```text
int, String
String, int
```

Therefore these methods can be overloaded.

---

# 11. Three Ways to Overload a Method

| Technique | Example |
|---|---|
| Different count | `show(int)` vs `show(int, int)` |
| Different type | `show(int)` vs `show(String)` |
| Different order | `show(int, String)` vs `show(String, int)` |

### Master Formula

$$
\boxed{\text{Overloading} = \text{Name Same + Parameter List Different}}
$$

---

# 12. Basic Example — Calculator

## Example 1

**Question**

Identify whether the following code demonstrates compile-time polymorphism.

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        int add(int a, int b, int c) {
            return a + b + c;
        }
    }

### Pattern Recognition

Same method name:

```text
add()
```

Different parameter lists:

```text
add(int, int)
add(int, int, int)
```

Therefore:

```text
Method Overloading
```

Hence:

$$
\boxed{\text{Compile Time Polymorphism}}
$$

---

# 13. Example — Different Parameter Types

## Example 2

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        double add(double a, double b) {
            return a + b;
        }
    }

Question:

What concept is demonstrated?

### Analysis

```text
Same name → add
Different types → int / double
```

Therefore:

$$
\boxed{\text{Method Overloading}}
$$

Answer:

$$
\boxed{\text{Compile Time Polymorphism}}
$$

---

# 14. Example — Parameter Order

## Example 3

    class Demo {

        void show(int a, String b) {
            System.out.println("A");
        }

        void show(String a, int b) {
            System.out.println("B");
        }
    }

Call:

    Demo d = new Demo();

    d.show("Hello", 10);

### Step 1 — Inspect arguments

```text
"Hello" → String
10 → int
```

### Step 2 — Find matching signature

```text
show(String, int)
```

### Step 3 — Select method

Output:

```text
B
```

---

# 15. Example — Exact Match

Consider:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(long x) {
            System.out.println("long");
        }
    }

Call:

    Demo d = new Demo();

    d.show(10);

### Argument Type

```text
10 → int
```

### Available Methods

```text
show(int)
show(long)
```

There is an exact match:

```text
show(int)
```

Therefore:

```text
Output:
int
```

> [!tip]
> **Exact match is generally preferred over a conversion.**

---

# 16. Example — Widening Conversion

Consider:

    class Demo {

        void show(long x) {
            System.out.println("long");
        }

        void show(double x) {
            System.out.println("double");
        }
    }

Call:

    Demo d = new Demo();

    d.show(10);

`10` is an `int`.

Possible widening conversions include:

```text
int → long
int → double
```

The `long` overload is selected.

Output:

```text
long
```

---

# 17. Primitive Widening

A useful primitive widening sequence is:

```text
byte
 ↓
short
 ↓
int
 ↓
long
 ↓
float
 ↓
double
```

Also:

```text
char
 ↓
int
 ↓
long
 ↓
float
 ↓
double
```

Examples:

```text
int → long
int → double
char → int
short → long
```

are widening conversions.

But:

```text
long → int
double → int
```

are narrowing conversions and are not automatically performed in ordinary method invocation.

---

# 18. Exact Match vs Widening

Example:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(long x) {
            System.out.println("long");
        }
    }

Call:

    show(10);

Possible:

```text
Exact:
int → int

Widening:
int → long
```

The compiler chooses the exact match.

Answer:

```text
int
```

### Recognition

> [!important]
> **Exact match beats widening.**

---

# 19. Overloading and `char`

Example:

    class Demo {

        void show(char c) {
            System.out.println("char");
        }

        void show(int x) {
            System.out.println("int");
        }
    }

Call:

    show('A');

Important:

```text
'A' → char
```

Therefore:

```text
show(char)
```

is an exact match.

Output:

```text
char
```

---

# 20. `char` vs `String`

This is a classic MCQ trap.

```text
'A' → char
"A" → String
```

Example:

    void show(char c) {
        System.out.println("char");
    }

    void show(String s) {
        System.out.println("String");
    }

Call:

    show('A');

Output:

```text
char
```

Call:

    show("A");

Output:

```text
String
```

> [!tip]
> **Single quotes → char**
>
> **Double quotes → String**

---

# 21. Overloading and `null`

`null` is an important advanced pattern.

Consider:

    class Demo {

        void show(String s) {
            System.out.println("String");
        }

        void show(Object o) {
            System.out.println("Object");
        }
    }

Call:

    Demo d = new Demo();

    d.show(null);

`null` can be passed to reference types.

Both methods are applicable:

```text
show(String)
show(Object)
```

But:

```text
String extends Object
```

Therefore `String` is more specific.

Output:

```text
String
```

---

# 22. `null` Ambiguity

Consider:

    class Demo {

        void show(String s) {
            System.out.println("String");
        }

        void show(Integer i) {
            System.out.println("Integer");
        }
    }

Call:

    Demo d = new Demo();

    d.show(null);

Both are valid reference types:

```text
String
Integer
```

But neither is more specific than the other.

Therefore the compiler cannot choose.

Result:

$$
\boxed{\text{Compile-Time Ambiguity}}
$$

> [!warning]
> When `null` is passed to overloaded methods, check whether one parameter type is more specific than the other.
>
> If the reference types are unrelated, the call may be ambiguous.

---

# 23. Overloading With Wrapper Classes

Java has wrapper classes:

| Primitive | Wrapper |
|---|---|
| `byte` | `Byte` |
| `short` | `Short` |
| `int` | `Integer` |
| `long` | `Long` |
| `float` | `Float` |
| `double` | `Double` |
| `char` | `Character` |
| `boolean` | `Boolean` |

Example:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(Integer x) {
            System.out.println("Integer");
        }
    }

Call:

    show(10);

`10` is already an `int`.

Therefore:

```text
show(int)
```

is an exact match.

Output:

```text
int
```

---

# 24. Boxing

Boxing means converting:

```text
Primitive → Wrapper Object
```

Example:

    Integer x = 10;

Conceptually:

```text
int → Integer
```

Java performs this conversion automatically when required.

---

# 25. Unboxing

Unboxing means:

```text
Wrapper Object → Primitive
```

Example:

    Integer x = 10;

    int y = x;

Conceptually:

```text
Integer → int
```

Both boxing and unboxing can affect overload resolution.

---

# 26. Widening vs Boxing

Consider:

    class Demo {

        void show(long x) {
            System.out.println("long");
        }

        void show(Integer x) {
            System.out.println("Integer");
        }
    }

Call:

    show(10);

Possible paths:

```text
int → long
```

or:

```text
int → Integer
```

The primitive widening method is considered before boxing in overload resolution.

Therefore:

```text
long
```

is selected.

> [!important]
> For common interview questions:
>
> **Widening primitive conversion is preferred over boxing when choosing between these applicable overload phases.**

---

# 27. Varargs

Varargs allows a method to accept a variable number of arguments.

Syntax:

    void show(int... values)

Examples:

    show();

    show(10);

    show(10, 20);

    show(10, 20, 30);

Conceptually, the parameter behaves like an array:

```text
int[]
```

---

# 28. Fixed Parameter vs Varargs

Consider:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(int... x) {
            System.out.println("varargs");
        }
    }

Call:

    show(10);

Possible methods:

```text
show(int)
show(int...)
```

The fixed-arity exact method is preferred.

Output:

```text
int
```

> [!tip]
> **Exact fixed-arity match beats varargs.**

---

# 29. Varargs Ambiguity

Consider:

    class Demo {

        void show(int... x) {
            System.out.println("int");
        }

        void show(boolean... x) {
            System.out.println("boolean");
        }
    }

Call:

    show();

Both methods can accept zero arguments.

Therefore the compiler cannot choose.

Result:

$$
\boxed{\text{Ambiguous Method Call}}
$$

---

# 30. Array and Varargs Trap

Consider:

    class Demo {

        void show(int[] x) {
            System.out.println("array");
        }

        void show(int... x) {
            System.out.println("varargs");
        }
    }

This is not valid as two distinct overloads.

Why?

Because:

```text
int...
```

is represented as:

```text
int[]
```

Therefore both declarations have the same parameter type.

> [!warning]
> **`int[]` and `int...` cannot be used as separate overloads.**

---

# 31. Overloading Static Methods

Static methods can be overloaded.

Example:

    class Demo {

        static void show(int x) {
            System.out.println("int");
        }

        static void show(String s) {
            System.out.println("String");
        }
    }

This is valid.

The method selection is still based on the overloaded parameter list.

Therefore:

$$
\boxed{\text{Static Methods Can Be Overloaded}}
$$

---

# 32. Static Method Hiding

Static methods are not overridden in the same dynamic-dispatch sense as instance methods.

Example:

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

This is called:

```text
Method Hiding
```

not:

```text
Method Overriding
```

This distinction is frequently tested in interviews.

---

# 33. Overloading Does Not Require Inheritance

Consider:

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        double add(double a, double b) {
            return a + b;
        }
    }

There is no parent class.

There is no child class.

Still:

```text
Method Overloading
```

Therefore:

$$
\boxed{\text{Overloading Does Not Require Inheritance}}
$$

---

# 34. Overriding Requires Inheritance

Consider:

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

There is:

```text
Parent
↓
Child
```

and the child replaces the inherited implementation.

This is:

```text
Method Overriding
```

which is associated with runtime polymorphism.

---

# 35. Overloading vs Overriding

This is one of the highest-priority interview comparisons.

| Feature | Overloading | Overriding |
|---|---|---|
| Polymorphism | Compile time | Runtime |
| Main idea | Same name, different parameters | Same signature, new implementation |
| Inheritance required | No | Yes |
| Binding | Static | Dynamic |
| Parameters | Must differ | Normally same |
| Return type | Cannot distinguish overloads | Compatible return type required |
| Access level | No overriding relationship | Cannot reduce visibility |
| `static` | Can be overloaded | Static methods are hidden |
| Constructor | Can be overloaded | Cannot be overridden |
| Main purpose | Convenience / API flexibility | Specialized child behavior |

### Master Formula

$$
\boxed{\text{Overloading} = \text{Same Name + Different Parameters}}
$$

$$
\boxed{\text{Overriding} = \text{Same Signature + Different Implementation}}
$$

---

# 36. Compile Time vs Runtime

Visualize the difference:

```text
                  POLYMORPHISM
                       |
              +--------+--------+
              |                 |
         COMPILE TIME       RUNTIME
              |                 |
         OVERLOADING        OVERRIDING
              |                 |
       STATIC BINDING     DYNAMIC BINDING
              |                 |
          COMPILER            JVM
          decides            dispatches
```

This diagram should be memorized.

---

# 37. Real-Time Example — Calculator API

A calculator may support:

    add(int, int)

    add(int, int, int)

    add(double, double)

The user performs the same conceptual action:

```text
add
```

but with different input forms.

This is a natural use of overloading.

---

# 38. Real-Time Example — Logging System

Imagine a logging API:

    log(String message)

    log(String message, int level)

    log(String message, Exception exception)

The operation is conceptually the same:

```text
log
```

but different information can be supplied.

This makes the API easier to use.

---

# 39. Real-Time Example — Search System

A search service could provide:

    search(String keyword)

    search(String keyword, int page)

    search(String keyword, int page, int pageSize)

Same operation:

```text
search()
```

Different parameter combinations.

This is method overloading.

---

# 40. Real-Time Example — Notification Service

A notification API could provide:

    send(String message)

    send(String message, String recipient)

    send(String message, String recipient, boolean urgent)

Again:

```text
Same operation
Different input forms
```

This is compile-time polymorphism.

---

# 41. Real-Time Example — File Utility

A file utility could provide:

    open(String path)

    open(String path, String mode)

    open(String path, String mode, boolean createIfMissing)

The caller can use the same conceptual method name.

This improves readability.

---

# 42. Real-Time Example — Database Utility

A database helper might provide:

    query(String sql)

    query(String sql, Object parameter)

    query(String sql, Object[] parameters)

The operation is still:

```text
query()
```

but the supported input forms differ.

---

# 43. Real-Time Example — Drawing API

A graphics library could provide:

    draw(int x, int y)

    draw(int x, int y, int radius)

    draw(int x1, int y1, int x2, int y2)

Same conceptual operation:

```text
draw()
```

Different parameter lists.

---

# 44. Why Use Method Overloading?

Without overloading:

```text
addTwoNumbers()
addThreeNumbers()
addDoubleNumbers()
```

With overloading:

```text
add()
add()
add()
```

The method name communicates the operation.

The parameters communicate the variation.

Therefore:

$$
\boxed{\text{Overloading Improves API Readability}}
$$

---

# 45. Advantages

## 1. Readability

Related operations share one meaningful name.

## 2. Convenience

The caller does not need to remember multiple method names.

## 3. Reusability

The same conceptual operation supports different input forms.

## 4. Compile-Time Checking

Invalid calls can be detected by the compiler.

## 5. Cleaner APIs

Methods representing the same operation remain grouped together.

---

# 46. Disadvantages

Too many overloads can create confusion.

For example:

    process()

    process(int)

    process(long)

    process(double)

    process(Integer)

    process(String)

    process(Object)

    process(int...)

Now method selection may become difficult to predict.

Potential problems:

- Ambiguous calls
- Unexpected conversions
- Boxing confusion
- `null` ambiguity
- Poor readability
- Maintenance difficulty

> [!warning]
> **Use overloading when the methods represent the same conceptual operation.**

Do not create overloads merely because Java allows them.

---

# 47. Recognition Tricks

> [!important]
> **If the method name is the same but parameters change, think OVERLOADING.**

Example:

    calculate(int)

    calculate(double)

Answer:

```text
Overloading
→ Compile Time Polymorphism
```

---

> [!important]
> **If only the return type changes, think INVALID.**

Example:

    int get()

    double get()

Answer:

```text
Cannot overload using return type alone.
```

---

> [!important]
> **If parent and child have the same method signature, think OVERRIDING.**

Example:

    Parent → show()

    Child → show()

Answer:

```text
Overriding
→ Runtime Polymorphism
```

---

> [!important]
> **If there is no inheritance but methods have the same name with different parameters, it can still be compile-time polymorphism.**

---

# 48. Shortcuts

> [!tip]
> **Shortcut 1 — O = Overloading = Offline/Compile Decision**
>
> For interview memory:
>
> ```text
> Overloading → Compile Time
> Overriding → Runtime
> ```

> [!tip]
> **Shortcut 2 — CTO**
>
> Remember:
>
> ```text
> C = Count
> T = Type
> O = Order
> ```
>
> To overload, change:
>
> ```text
> Count
> Type
> Order
> ```
>
> of parameters.

> [!tip]
> **Shortcut 3 — Return Type Trap**
>
> If the question says:
>
> ```text
> Same name
> Same parameters
> Different return type
> ```
>
> immediately think:
>
> ```text
> INVALID
> ```

> [!tip]
> **Shortcut 4 — Exact Match**
>
> If an exact overload exists:
>
> ```text
> Exact match
> ```
>
> is generally preferred over conversion.

> [!tip]
> **Shortcut 5 — Quotes**
>
> ```text
> 'A' → char
> "A" → String
> ```

> [!tip]
> **Shortcut 6 — null**
>
> If:
>
> ```text
> show(String)
> show(Integer)
> ```
>
> then:
>
> ```text
> show(null)
> ```
>
> is ambiguous because neither type is more specific than the other.

> [!tip]
> **Shortcut 7 — Varargs**
>
> Fixed exact parameter generally beats varargs.
>
> ```text
> show(int)
> ```
>
> beats:
>
> ```text
> show(int...)
> ```

> [!tip]
> **Shortcut 8 — Static**
>
> ```text
> static methods → can be overloaded
> static methods → hidden, not overridden
> ```

---

# 49. Overload Resolution — Interview Priority

When an interviewer gives multiple overloaded methods, use this mental process:

```text
STEP 1
Look for exact match.

        ↓

STEP 2
If no exact match,
check applicable primitive widening.

        ↓

STEP 3
Consider boxing/unboxing where applicable.

        ↓

STEP 4
Consider reference-type widening / specificity.

        ↓

STEP 5
Consider varargs.

        ↓

STEP 6
If two equally good candidates remain:
AMBIGUOUS
```

This is an exam-oriented simplification. Java's actual overload resolution rules are more detailed, especially around generic methods, poly expressions, lambdas, and method references.

---

# 50. Pattern — Exact Match

Given:

    show(int)

    show(long)

Call:

    show(10);

Recognition:

```text
10 → int
```

Therefore:

```text
show(int)
```

---

# 51. Pattern — Widening

Given:

    show(long)

    show(double)

Call:

    show(10);

Recognition:

```text
int → long
int → double
```

Prefer the closer widening conversion:

```text
long
```

---

# 52. Pattern — Boxing

Given:

    show(Integer)

Call:

    show(10);

Recognition:

```text
10 → int
```

then:

```text
int → Integer
```

This is boxing.

---

# 53. Pattern — `null` + Parent Type

Given:

    show(Object)

    show(String)

Call:

    show(null);

Recognition:

```text
null → Object
null → String
```

`String` is more specific.

Answer:

```text
String
```

---

# 54. Pattern — `null` + Unrelated Types

Given:

    show(String)

    show(Integer)

Call:

    show(null);

Recognition:

```text
String
Integer
```

Neither is more specific.

Answer:

```text
Compile-time ambiguity
```

---

# 55. Pattern — Varargs

Given:

    show(int)

    show(int...)

Call:

    show(10);

Recognition:

```text
Exact fixed arity exists
```

Answer:

```text
show(int)
```

---

# 56. Pattern — Constructor Overloading

Given:

    Student()

    Student(String)

    Student(String, int)

Creating:

    new Student();

selects:

```text
Student()
```

Creating:

    new Student("Pradeep");

selects:

```text
Student(String)
```

Creating:

    new Student("Pradeep", 21);

selects:

```text
Student(String, int)
```

This is constructor overloading.

---

# 57. Pattern — Static Overloading

Given:

    static show(int)

    static show(String)

Both methods can coexist.

Therefore:

```text
Static methods can be overloaded.
```

---

# 58. Pattern — Static Hiding

Given:

    class Parent {
        static void show() {
        }
    }

    class Child extends Parent {
        static void show() {
        }
    }

This is:

```text
Method Hiding
```

not runtime overriding.

---

# 59. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Identify compile-time polymorphism.

### Pattern 2
Identify method overloading.

### Pattern 3
Different number of parameters.

### Pattern 4
Different parameter types.

### Pattern 5
Different parameter order.

### Pattern 6
Return-type-only overloading trap.

### Pattern 7
Method signature questions.

### Pattern 8
Exact-match overload resolution.

### Pattern 9
Primitive widening.

### Pattern 10
Boxing and unboxing.

### Pattern 11
`null` overload ambiguity.

### Pattern 12
Reference-type specificity.

### Pattern 13
Varargs resolution.

### Pattern 14
Array vs varargs.

### Pattern 15
Static method overloading.

### Pattern 16
Static method hiding.

### Pattern 17
Constructor overloading.

### Pattern 18
Overloading without inheritance.

### Pattern 19
Overloading vs overriding.

### Pattern 20
Compile-time vs runtime binding.

---

# 60. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Return Type Creates Overloading

Wrong:

    int get()

    double get()

Correct:

```text
Return type alone cannot overload a method.
```

---

### Mistake 2 — Confusing Overloading and Overriding

Wrong:

```text
Same name = overriding
```

Correct:

```text
Same name + different parameters
→ Overloading

Same signature + parent-child relationship
→ Overriding
```

---

### Mistake 3 — Thinking Inheritance Is Required for Overloading

It is not.

A single class can contain multiple overloaded methods.

---

### Mistake 4 — Thinking `static` Means Compile-Time Polymorphism

Static polymorphism and the `static` keyword are different concepts.

Static methods can participate in overloading, but compile-time polymorphism is not defined by the `static` keyword.

---

### Mistake 5 — Ignoring Parameter Order

These can be different:

    show(int, String)

    show(String, int)

---

### Mistake 6 — Treating `'A'` as String

Wrong:

```text
'A' → String
```

Correct:

```text
'A' → char
```

---

### Mistake 7 — Treating `"A"` as char

Wrong:

```text
"A" → char
```

Correct:

```text
"A" → String
```

---

### Mistake 8 — Ignoring `null` Ambiguity

This can fail:

    show(String)

    show(Integer)

    show(null);

because the compiler cannot determine the more specific unrelated reference type.

---

### Mistake 9 — Forgetting Varargs

`int...` behaves as an array-like parameter:

```text
int[]
```

for declaration purposes.

---

### Mistake 10 — Assuming More Parameters Always Means Overloading

Parameter lists must actually differ.

For example:

    show(int, String)

    show(int, String)

is simply a duplicate declaration, not overloading.

---

# 61. Interview Questions

## Beginner Level

### Q1. What is compile-time polymorphism?

**Answer:**

Compile-time polymorphism is polymorphism where the compiler determines the appropriate overloaded method during compilation. In Java, method overloading is the main example.

---

### Q2. What is another name for compile-time polymorphism?

**Answer:**

It is commonly called:

```text
Static Polymorphism
Early Binding
Static Binding
```

---

### Q3. What is method overloading?

**Answer:**

Method overloading means defining multiple methods with the same name but different parameter lists.

---

### Q4. What are the ways to overload a method?

**Answer:**

A method can be overloaded by changing:

```text
Number of parameters
Parameter types
Parameter order
```

---

### Q5. Can return type alone overload a method?

**Answer:**

No.

---

### Q6. Does method overloading require inheritance?

**Answer:**

No.

---

# 62. Intermediate Interview Questions

### Q7. What is the difference between overloading and overriding?

**Answer:**

Overloading uses the same method name with different parameter lists and is associated with compile-time polymorphism.

Overriding occurs when a child class provides a new implementation for an inherited method with the same signature and is associated with runtime polymorphism.

---

### Q8. Is the return type part of the method signature in Java?

**Answer:**

No. The method signature consists of the method name and parameter types.

---

### Q9. Can static methods be overloaded?

**Answer:**

Yes.

---

### Q10. Can static methods be overridden?

**Answer:**

No. Static methods are hidden rather than overridden.

---

### Q11. Can constructors be overloaded?

**Answer:**

Yes.

---

### Q12. Can constructors be overridden?

**Answer:**

No. Constructors are not inherited and therefore cannot be overridden.

---

# 63. Advanced Interview Questions

### Q13. Which method is selected first: exact match or widening?

**Answer:**

An exact applicable match is generally preferred over a widening conversion.

---

### Q14. Which is preferred: widening or boxing?

**Answer:**

In Java overload resolution, primitive widening is considered before boxing in the relevant phases.

---

### Q15. What happens when `null` is passed to overloaded methods?

**Answer:**

If one reference type is more specific than another, the more specific overload can be selected.

If the applicable reference types are unrelated, the call may be ambiguous.

---

### Q16. Is `int[]` different from `int...` for overloading?

**Answer:**

No. A varargs parameter `int...` is represented as `int[]` for the method declaration, so they cannot be declared as two separate overloads.

---

### Q17. Can one method be overloaded using only different access modifiers?

No.

Example:

    public void show(int x)

    private void show(int x)

This is not valid overloading.

The parameter list is identical.

---

### Q18. Can methods be overloaded by changing only `final` on a parameter?

No.

For example:

    void show(int x)

and:

    void show(final int x)

have the same parameter type for signature purposes.

---

### Q19. Can methods be overloaded by changing parameter variable names?

No.

These are identical signatures:

    void show(int x)

    void show(int y)

The parameter name does not matter.

---

### Q20. Can methods be overloaded by changing only the `throws` clause?

No.

The `throws` clause does not distinguish overloaded methods.

---

# 64. High-Level Interview Trick

When an interviewer gives you two methods, do not immediately look at the return type.

Use this order:

```text
1. Method name
2. Parameter count
3. Parameter types
4. Parameter order
5. Return type
```

If:

```text
Name same
+
Parameters different
```

then:

```text
Overloading
```

If:

```text
Name same
+
Parameters same
+
Parent-child relationship
```

then investigate:

```text
Overriding
```

If only:

```text
Return type differs
```

then:

```text
Invalid overload
```

---

# 65. High-Level Problem-Solving Pattern

Suppose the interviewer gives:

    show(int)

    show(long)

    show(Integer)

    show(Object)

and asks:

    show(10);

Do not guess.

Follow:

```text
10
↓
int
↓
Is show(int) available?
↓
YES
↓
Exact match
↓
STOP
```

Answer:

```text
show(int)
```

---

# 66. High-Level `null` Problem

Suppose:

    show(Object)

    show(String)

and:

    show(null);

Follow:

```text
null
↓
Reference types possible
↓
Object
String
↓
String is more specific
↓
show(String)
```

Now change it to:

    show(String)

    show(Integer)

and:

    show(null);

Follow:

```text
null
↓
String
Integer
↓
Neither is more specific
↓
Ambiguous
```

This pattern solves many interview MCQs.

---

# 67. Real Interview Question — Explain in One Minute

**Question:**

Explain compile-time polymorphism in Java.

**Strong Answer:**

> Compile-time polymorphism is a form of polymorphism where the compiler determines which overloaded method should be invoked based on the method name and parameter list. In Java, method overloading is the main example. Multiple methods can have the same name as long as their parameter lists differ by number, type, or order. Return type alone cannot create overloading. It is also commonly called static or early binding.

---

# 68. Real Interview Question — Why Use Overloading?

**Answer:**

Method overloading allows related operations to use the same meaningful method name while supporting different input forms.

For example:

    add(int, int)

    add(double, double)

    add(int, int, int)

This improves readability, convenience, and API usability.

---

# 69. Real Interview Question — Why Is Return Type Not Enough?

Suppose:

    int calculate()

and:

    double calculate()

If Java allowed this, the compiler could face ambiguity:

    calculate();

Which return type should be selected?

The call does not contain information telling the compiler whether the caller wants:

```text
int
```

or:

```text
double
```

Therefore Java does not use return type alone to distinguish overloaded methods.

---

# 70. Compile-Time Polymorphism Decision Tree

Use this during MCQs:

```text
START
  |
  ↓
Same method name?
  |
  +-- NO → Not overloading
  |
  YES
  |
  ↓
Different parameter list?
  |
  +-- YES → Overloading
  |          ↓
  |      Compile-Time
  |      Polymorphism
  |
  +-- NO
       |
       ↓
Parent-child relationship?
       |
       +-- YES → Check overriding
       |
       +-- NO → Duplicate declaration
```

---

# 71. Ultimate Recognition Table

| Question Pattern | Think |
|---|---|
| Same name, different count | Overloading |
| Same name, different type | Overloading |
| Same name, different order | Overloading |
| Same name, same parameters, different return type | Invalid |
| Parent-child + same signature | Overriding |
| Overloading | Compile Time |
| Overriding | Runtime |
| Static method with different parameters | Overloading |
| Static method in child with same signature | Hiding |
| Constructor with different parameters | Constructor Overloading |
| `show(int)` vs `show(long)` with `10` | Exact `int` |
| `show(long)` vs `show(double)` with `10` | Usually `long` |
| `show(String)` vs `show(Object)` with `null` | `String` |
| `show(String)` vs `show(Integer)` with `null` | Ambiguous |
| `show(int)` vs `show(int...)` with `10` | `int` |
| `int[]` vs `int...` | Same declaration type |

---

# 72. Common Coding Traps

## Trap 1

    void test(int x)

    void test(int y)

Not overloading.

Reason:

```text
Parameter names do not matter.
```

---

## Trap 2

    void test(int x)

    void test(final int x)

Not overloading.

Reason:

```text
final parameter modifier does not change the signature.
```

---

## Trap 3

    int test()

    double test()

Not overloading.

Reason:

```text
Return type does not distinguish methods.
```

---

## Trap 4

    void test(int... x)

    void test(int[] x)

Not two overloads.

Reason:

```text
int... → int[]
```

---

## Trap 5

    void test(String x)

    void test(Object x)

    test(null);

This selects `String`, because `String` is more specific than `Object`.

---

## Trap 6

    void test(String x)

    void test(Integer x)

    test(null);

Ambiguous.

---

# 73. Formula Sheet

```text
COMPILE TIME POLYMORPHISM
= METHOD OVERLOADING

OVERLOADING
= SAME METHOD NAME
+ DIFFERENT PARAMETER LIST

Parameter differences:
1. Number
2. Type
3. Order

Return type alone:
NOT enough

Method signature:
Method name + parameter types

Compile Time:
Overloading

Runtime:
Overriding

Static binding:
Compile time

Dynamic binding:
Runtime

Exact match:
Preferred over conversion

Primitive widening:
byte → short → int → long → float → double

char → int → long → float → double

Boxing:
int → Integer
long → Long
double → Double
char → Character
boolean → Boolean

null:
Can match reference types

Unrelated reference overloads + null:
May be ambiguous

Varargs:
int... behaves as int[]

Static methods:
Can be overloaded
Cannot be overridden; they are hidden

Constructors:
Can be overloaded
Cannot be overridden
```

---

# 74. Quick Revision

> [!summary] One-Minute Revision

### What is Polymorphism?

```text
One concept
↓
Multiple forms
```

### Compile-Time Polymorphism

```text
Compile Time
      ↓
Method Overloading
      ↓
Static / Early Binding
```

### Method Overloading

```text
Same method name
+
Different parameter list
```

Change:

```text
Count
Type
Order
```

### Cannot overload using:

```text
Return type alone
Access modifier alone
Parameter names alone
final parameter modifier alone
throws clause alone
```

### Important Java Rules

```text
Overloading → Compile Time

Overriding → Runtime

Overloading does not require inheritance.

Overriding requires inheritance.

Static methods can be overloaded.

Static methods are hidden, not overridden.

Constructors can be overloaded.

Constructors cannot be overridden.
```

### Overload Resolution Memory

```text
Exact match
    ↓
Widening
    ↓
Boxing / applicable reference conversions
    ↓
Varargs
```

This is a practical interview-oriented simplification; Java's full overload-resolution specification contains additional rules.

### `null` Memory

```text
String + Object
+ null
→ String

String + Integer
+ null
→ Ambiguous
```

### Character Memory

```text
'A' → char

"A" → String
```

### Ultimate Difference

```text
OVERLOADING
Same name
Different parameters
Compile Time

OVERRIDING
Same signature
Parent → Child
Runtime
```

### Golden Memory Trick

**Overloading means ONE method name has MANY parameter forms, and the compiler chooses the appropriate form.**

### One-Line Recognition

**If the same method name appears with different parameter count, type, or order, immediately think Compile Time Polymorphism through Method Overloading.**