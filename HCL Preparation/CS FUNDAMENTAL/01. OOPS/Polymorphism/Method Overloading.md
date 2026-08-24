---
type: concept
subject: aptitude
topic: "Method Overloading"
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
  - method-overloading
  - compile-time-polymorphism
  - static-binding
  - java
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Polymorphism]]"
  - "[[Compile Time Polymorphism]]"
  - "[[Runtime Polymorphism]]"
  - "[[Method Overriding]]"
  - "[[Dynamic Method Dispatch]]"
---

# Method Overloading

> [!summary]
> **Method Overloading** means defining multiple methods with the **same method name** but **different parameter lists** within the same class or an applicable inherited context.
>
> It is the most common example of **Compile Time Polymorphism** in Java.
>
> Core pattern:
>
> ```text
> SAME METHOD NAME
> +
> DIFFERENT PARAMETERS
> =
> METHOD OVERLOADING
> ```
>
> Fast recognition:
>
> **Same name + different parameter list → Overloading → Compile Time**

---

# 1. Core Concept

Suppose a calculator needs to perform addition.

It may need:

```text
add(int, int)
add(int, int, int)
add(double, double)
```

Instead of creating unrelated names such as:

```text
addTwoNumbers()
addThreeNumbers()
addDoubleNumbers()
```

we use the same meaningful operation name:

```text
add()
```

with different parameter lists.

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

    System.out.println(c.add(10, 20));

    System.out.println(c.add(10, 20, 30));

    System.out.println(c.add(10.5, 20.5));

The compiler identifies which method matches each call.

Therefore:

$$
\boxed{\text{Method Overloading} \Rightarrow \text{Compile Time Polymorphism}}
$$

---

# 2. Basic Meaning

Method overloading means:

```text
Same method name
+
Different parameter list
```

The parameter list can differ in:

1. Number of parameters
2. Parameter data types
3. Parameter order

Therefore:

$$
\boxed{\text{Overloading} = \text{Same Name + Different Parameters}}
$$

---

# 3. Why Do We Need Method Overloading?

Imagine a mathematical library.

Without overloading:

    addTwoIntegers()
    addThreeIntegers()
    addTwoDoubles()
    addTwoFloats()

The API becomes harder to remember.

With overloading:

    add(int, int)
    add(int, int, int)
    add(double, double)
    add(float, float)

The caller only needs to remember:

```text
add()
```

The parameter list tells Java which version to use.

This improves:

- Readability
- API usability
- Consistency
- Developer productivity
- Compile-time checking

---

# 4. Main Rule

A method can be overloaded if at least one of these changes:

| Change | Can create overloading? |
|---|---|
| Number of parameters | Yes |
| Parameter type | Yes |
| Parameter order | Yes |
| Return type only | No |
| Parameter variable name | No |
| Access modifier only | No |
| `final` parameter modifier only | No |
| `throws` clause only | No |

### Master Rule

$$
\boxed{\text{Parameters Matter, Return Type Does Not}}
$$

for distinguishing Java method overloads.

---

# 5. Method Signature

A Java method signature consists of:

```text
Method Name
+
Parameter Types
```

Example:

    void calculate(int a, int b)

Signature:

```text
calculate(int, int)
```

Another:

    void calculate(double a, double b)

Signature:

```text
calculate(double, double)
```

These are different signatures.

Therefore they can coexist as overloaded methods.

---

# 6. What Is NOT Part of the Signature?

The following do not distinguish overloaded methods:

```text
Return type
Parameter variable names
Access modifiers
throws clause
```

Example:

    int calculate(int x)

    double calculate(int y)

These have the same signature:

```text
calculate(int)
```

Therefore they cannot be overloaded merely by changing return type or parameter name.

---

# 7. Pattern 1 — Different Number of Parameters

This is the easiest pattern.

    class Demo {

        void show(int a) {
            System.out.println("One parameter");
        }

        void show(int a, int b) {
            System.out.println("Two parameters");
        }
    }

Signatures:

```text
show(int)
show(int, int)
```

Parameter count differs.

Therefore:

$$
\boxed{\text{Overloading}}
$$

---

# 8. Pattern 2 — Different Parameter Types

Example:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(double x) {
            System.out.println("double");
        }
    }

Signatures:

```text
show(int)
show(double)
```

Parameter types differ.

Therefore:

$$
\boxed{\text{Overloading}}
$$

---

# 9. Pattern 3 — Different Parameter Order

Example:

    class Demo {

        void show(int x, String s) {
            System.out.println("int, String");
        }

        void show(String s, int x) {
            System.out.println("String, int");
        }
    }

Signatures:

```text
show(int, String)
show(String, int)
```

The order differs.

Therefore:

$$
\boxed{\text{Overloading}}
$$

> [!important]
> **Changing parameter order can create overloading when the parameter types are arranged differently.**

---

# 10. Pattern 4 — Different Reference Types

Example:

    class Notification {

        void send(String message) {
            System.out.println("String message");
        }

        void send(Object message) {
            System.out.println("Object message");
        }
    }

The parameter types differ:

```text
String
Object
```

Therefore these methods are overloaded.

---

# 11. Pattern 5 — Primitive vs Wrapper

Example:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(Integer x) {
            System.out.println("Integer");
        }
    }

The parameter types are:

```text
int
Integer
```

These are different types.

Therefore overloading is valid.

---

# 12. Pattern 6 — Array Parameter

Example:

    class Demo {

        void process(int x) {
            System.out.println("Single integer");
        }

        void process(int[] x) {
            System.out.println("Integer array");
        }
    }

Parameter types:

```text
int
int[]
```

These are different.

Therefore overloading is valid.

---

# 13. What Does NOT Create Overloading?

## Return Type Only

Invalid:

    class Demo {

        int getValue() {
            return 10;
        }

        double getValue() {
            return 10.5;
        }
    }

Why?

Both have:

```text
getValue()
```

The return types differ, but return type is not enough to distinguish methods.

Therefore:

$$
\boxed{\text{Compile-Time Error}}
$$

---

# 14. Parameter Name Only

Invalid:

    class Demo {

        void show(int x) {
        }

        void show(int y) {
        }
    }

Both signatures are:

```text
show(int)
```

Parameter names:

```text
x
y
```

do not matter.

Therefore this is not overloading.

---

# 15. Access Modifier Only

Invalid:

    class Demo {

        public void show(int x) {
        }

        private void show(int x) {
        }
    }

The parameter lists are identical.

Changing:

```text
public
```

to:

```text
private
```

does not create an overload.

---

# 16. `final` Parameter Trap

Invalid:

    class Demo {

        void show(int x) {
        }

        void show(final int x) {
        }
    }

For method signature purposes:

```text
int
```

is still:

```text
int
```

The `final` modifier on the parameter does not create another overload.

---

# 17. `throws` Clause Trap

Invalid:

    class Demo {

        void show() throws Exception {
        }

        void show() throws IOException {
        }
    }

The parameter lists are both:

```text
show()
```

Changing the `throws` clause does not create overloading.

---

# 18. Basic Example — Identify the Overload

## Example 1

Which pair represents valid method overloading?

### A

    int show(int x)

    double show(int x)

### B

    void show(int x)

    void show(String x)

### C

    void show(int x)

    void show(int y)

### D

    void show(int x)

    private void show(int x)

### Analysis

Option B has:

```text
show(int)
show(String)
```

Different parameter types.

### Answer

$$
\boxed{\text{B}}
$$

---

# 19. Example — Different Parameter Count

## Example 2

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        int add(int a, int b, int c) {
            return a + b + c;
        }
    }

Call:

    Calculator c = new Calculator();

    int result = c.add(10, 20, 30);

### Step 1

Count arguments:

```text
3
```

### Step 2

Find matching overload:

```text
add(int, int, int)
```

### Step 3

Calculate:

$$
10+20+30=60
$$

### Answer

$$
\boxed{60}
$$

---

# 20. Example — Different Types

## Example 3

    class Printer {

        void print(int x) {
            System.out.println("Integer");
        }

        void print(String x) {
            System.out.println("String");
        }
    }

Call:

    Printer p = new Printer();

    p.print("Hello");

Argument type:

```text
String
```

Matching method:

```text
print(String)
```

Output:

```text
String
```

---

# 21. Example — Different Order

## Example 4

    class Demo {

        void display(int x, String s) {
            System.out.println("A");
        }

        void display(String s, int x) {
            System.out.println("B");
        }
    }

Call:

    Demo d = new Demo();

    d.display("Java", 10);

Argument types:

```text
String
int
```

Matching signature:

```text
display(String, int)
```

Output:

```text
B
```

---

# 22. Example — Exact Match

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

Literal:

```text
10 → int
```

Available:

```text
show(int)
show(long)
```

Exact match:

```text
show(int)
```

Output:

```text
int
```

> [!tip]
> **Exact match is preferred over a conversion.**

---

# 23. Example — Widening

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

    d.show(10);

`10` is an `int`.

Possible conversions:

```text
int → long
int → double
```

The closer widening conversion is `int → long`.

Output:

```text
long
```

---

# 24. Primitive Widening Table

| From | Can widen to |
|---|---|
| `byte` | `short`, `int`, `long`, `float`, `double` |
| `short` | `int`, `long`, `float`, `double` |
| `char` | `int`, `long`, `float`, `double` |
| `int` | `long`, `float`, `double` |
| `long` | `float`, `double` |
| `float` | `double` |
| `double` | None |

Important:

```text
boolean
```

does not participate in numeric widening.

---

# 25. Example — `char`

    class Demo {

        void show(char x) {
            System.out.println("char");
        }

        void show(int x) {
            System.out.println("int");
        }
    }

Call:

    d.show('A');

`'A'` is:

```text
char
```

There is an exact match:

```text
show(char)
```

Therefore output:

```text
char
```

---

# 26. Character Literal Trap

Remember:

```text
'A' → char
"A" → String
```

Example:

    show('A');

calls:

```text
show(char)
```

while:

    show("A");

calls:

```text
show(String)
```

> [!tip]
> **Single quotes → char**
>
> **Double quotes → String**

---

# 27. Example — `null` and Specificity

Consider:

    class Demo {

        void show(Object obj) {
            System.out.println("Object");
        }

        void show(String str) {
            System.out.println("String");
        }
    }

Call:

    d.show(null);

Both can accept `null`:

```text
Object
String
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

# 28. Example — `null` Ambiguity

Consider:

    class Demo {

        void show(String str) {
            System.out.println("String");
        }

        void show(Integer num) {
            System.out.println("Integer");
        }
    }

Call:

    d.show(null);

Both are applicable:

```text
String
Integer
```

But:

```text
String
```

and:

```text
Integer
```

are unrelated types.

Neither overload is more specific.

Therefore:

$$
\boxed{\text{Compile-Time Ambiguity}}
$$

---

# 29. Boxing

Boxing converts:

```text
primitive → wrapper
```

Examples:

```text
int → Integer
double → Double
char → Character
boolean → Boolean
```

Example:

    Integer x = 10;

The primitive `10` is automatically boxed into an `Integer`.

---

# 30. Unboxing

Unboxing converts:

```text
wrapper → primitive
```

Example:

    Integer x = 10;

    int y = x;

Conceptually:

```text
Integer → int
```

---

# 31. Widening vs Boxing

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

    d.show(10);

Possible:

```text
int → long
```

or:

```text
int → Integer
```

For common overload-resolution questions, primitive widening is considered before boxing.

Therefore:

```text
long
```

is selected.

> [!important]
> **Do not automatically assume boxing is preferred just because a wrapper overload exists.**

---

# 32. Varargs

Varargs allows a variable number of arguments.

Syntax:

    void sum(int... values)

Calls can be:

    sum();

    sum(10);

    sum(10, 20);

    sum(10, 20, 30);

For declaration purposes:

```text
int...
```

corresponds to:

```text
int[]
```

---

# 33. Fixed Parameter vs Varargs

Consider:

    class Demo {

        void show(int x) {
            System.out.println("fixed");
        }

        void show(int... x) {
            System.out.println("varargs");
        }
    }

Call:

    d.show(10);

There is an exact fixed-arity method:

```text
show(int)
```

Therefore it is selected instead of the varargs overload.

Output:

```text
fixed
```

---

# 34. Array vs Varargs

This is a common interview trap.

Do not write both:

    void show(int[] x)

and:

    void show(int... x)

as separate overloads.

Why?

Because:

```text
int...
```

is represented as:

```text
int[]
```

Therefore the declarations conflict.

---

# 35. Method Overloading and Static Methods

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

Both methods have the same name:

```text
show()
```

but different parameters.

Therefore:

```text
Static Method Overloading
```

is valid.

---

# 36. Static Method Hiding vs Overloading

Consider:

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

This is:

```text
Method Hiding
```

not overriding.

However:

    class Demo {

        static void show(int x) {
        }

        static void show(String s) {
        }
    }

is:

```text
Method Overloading
```

---

# 37. Method Overloading Does Not Require Inheritance

Example:

    class Calculator {

        int add(int a, int b) {
            return a + b;
        }

        double add(double a, double b) {
            return a + b;
        }
    }

No inheritance exists.

Still:

```text
Method Overloading
```

Therefore:

$$
\boxed{\text{Overloading does not require inheritance}}
$$

---

# 38. Method Overloading With Inheritance

Overloading can also occur across an inheritance hierarchy.

Example:

    class Parent {

        void show(int x) {
            System.out.println("Parent int");
        }
    }

    class Child extends Parent {

        void show(String x) {
            System.out.println("Child String");
        }
    }

Now the child has access to:

```text
show(int)
```

from the parent and declares:

```text
show(String)
```

in the child.

These represent different parameter lists.

This can participate in overload resolution for a `Child` reference.

> [!important]
> **Overloading is based on different parameter lists, not simply on whether methods are written in the same source class.**

---

# 39. Overloading vs Overriding

This is one of the most important interview comparisons.

| Feature | Method Overloading | Method Overriding |
|---|---|---|
| Main concept | Same name, different parameters | Same signature, new child implementation |
| Polymorphism | Compile time | Runtime |
| Binding | Static | Dynamic |
| Inheritance | Not required | Required |
| Parameter list | Must differ | Normally same |
| Return type alone | Cannot overload | Compatible return type may be allowed |
| Constructor | Can be overloaded | Cannot be overridden |
| Static method | Can be overloaded | Hidden, not overridden |
| Purpose | Convenience / API flexibility | Specialized behavior |

### Master Memory

```text
OVERLOAD
→ Parameters Change
→ Compiler

OVERRIDE
→ Implementation Changes
→ Runtime
```

---

# 40. Overloading vs Overriding Visual

```text
                 POLYMORPHISM
                      |
             +--------+--------+
             |                 |
         OVERLOADING       OVERRIDING
             |                 |
        Compile Time        Runtime
             |                 |
        Static Binding    Dynamic Binding
             |                 |
      Different Params    Same Signature
```

Memorize this diagram.

---

# 41. Real-Time Example — Calculator

A calculator is the classic example.

Possible methods:

    add(int, int)

    add(long, long)

    add(double, double)

    add(int, int, int)

All represent:

```text
ADD
```

but support different input forms.

This is a clean use of overloading.

---

# 42. Real-Time Example — Banking

A banking system might have:

    deposit(double amount)

    deposit(double amount, String chequeNumber)

    deposit(double amount, String chequeNumber, String bankName)

The conceptual operation is always:

```text
deposit
```

but additional information can be supplied when required.

---

# 43. Real-Time Example — E-Commerce

An e-commerce system could have:

    search(String keyword)

    search(String keyword, int page)

    search(String keyword, int page, int pageSize)

The operation remains:

```text
search
```

Different parameters provide additional search controls.

---

# 44. Real-Time Example — Notification

A notification service might provide:

    send(String message)

    send(String message, String user)

    send(String message, String user, boolean urgent)

Same conceptual operation:

```text
send
```

Different parameter lists.

---

# 45. Real-Time Example — Logging

A logger might support:

    log(String message)

    log(String message, int level)

    log(String message, Exception exception)

This makes the API convenient because the caller can provide only the information available.

---

# 46. Real-Time Example — Drawing

A graphics library could have:

    draw(int x, int y)

    draw(int x, int y, int radius)

    draw(int x1, int y1, int x2, int y2)

The method name describes the common operation.

The parameters describe the variation.

---

# 47. Real-Time Example — File Operations

A file utility might provide:

    open(String path)

    open(String path, String mode)

    open(String path, String mode, boolean create)

Again:

```text
Same operation
Different input forms
```

---

# 48. Real-Time Example — Database API

A database helper could provide:

    query(String sql)

    query(String sql, Object parameter)

    query(String sql, Object[] parameters)

This lets the API support:

```text
Simple query
Parameterized query
Multiple parameters
```

under one conceptual method name.

---

# 49. Why Overloading Is Useful in Real Software

Without overloading:

```text
sendMessage()
sendMessageToUser()
sendMessageToUserWithPriority()
```

With overloading:

    send(String message)

    send(String message, String user)

    send(String message, String user, boolean priority)

The method names remain consistent.

This is particularly useful for APIs and libraries.

---

# 50. Advantages

## 1. Readability

Related operations use one meaningful method name.

## 2. Consistency

The API feels predictable.

## 3. Convenience

Developers can supply only the parameters they need.

## 4. Compile-Time Safety

Invalid argument combinations can be caught early.

## 5. Reusability

The same conceptual operation handles multiple input types.

## 6. Better API Design

Methods representing one operation remain logically grouped.

---

# 51. Disadvantages

Overloading can become problematic when there are too many variations.

Example:

    process(int x)

    process(long x)

    process(float x)

    process(double x)

    process(Integer x)

    process(Object x)

    process(String x)

    process(int... x)

This can create:

- Confusing overload resolution
- Ambiguous calls
- Unexpected type conversions
- `null` ambiguity
- Boxing/unboxing surprises
- Maintenance complexity

> [!warning]
> **Do not create many overloads just because overloading is possible.**

The overloads should represent logically related operations.

---

# 52. Recognition Tricks

> [!important]
> **Pattern 1 — Same Name + Different Count**
>
> ```text
> add(int, int)
> add(int, int, int)
> ```
>
> Think:
>
> **Overloading**

---

> [!important]
> **Pattern 2 — Same Name + Different Type**
>
> ```text
> print(int)
> print(String)
> ```
>
> Think:
>
> **Overloading**

---

> [!important]
> **Pattern 3 — Same Name + Different Order**
>
> ```text
> show(int, String)
> show(String, int)
> ```
>
> Think:
>
> **Overloading**

---

> [!important]
> **Pattern 4 — Only Return Type Changes**
>
> ```text
> int get()
> double get()
> ```
>
> Think:
>
> **Invalid**

---

> [!important]
> **Pattern 5 — Parent + Child + Same Signature**
>
> ```text
> Parent → show()
> Child  → show()
> ```
>
> Think:
>
> **Overriding**

---

> [!important]
> **Pattern 6 — No Inheritance + Different Parameters**
>
> Still:
>
> **Overloading**

---

> [!important]
> **Pattern 7 — `null` + Parent/Child Reference Types**
>
> ```text
> show(Object)
> show(String)
> show(null)
> ```
>
> Think:
>
> **String is more specific**

---

> [!important]
> **Pattern 8 — `null` + Unrelated Types**
>
> ```text
> show(String)
> show(Integer)
> show(null)
> ```
>
> Think:
>
> **Ambiguous**

---

> [!important]
> **Pattern 9 — Fixed Method + Varargs**
>
> ```text
> show(int)
> show(int...)
> ```
>
> Call:
>
> ```text
> show(10)
> ```
>
> Think:
>
> **Fixed exact match**

---

# 53. Shortcuts

> [!tip]
> **Shortcut 1 — CTO**
>
> Remember:
>
> ```text
> C = Count
> T = Type
> O = Order
> ```
>
> If Count, Type, or Order of parameters changes:
>
> **Overloading**

---

> [!tip]
> **Shortcut 2 — Parameters First**
>
> When comparing two methods, ignore the return type initially.
>
> Check:
>
> ```text
> Method name
> ↓
> Parameter count
> ↓
> Parameter types
> ↓
> Parameter order
> ```
>
> Only then consider return type for compatibility.

---

> [!tip]
> **Shortcut 3 — OR**
>
> ```text
> Overloading → Parameters Change
> Overriding → Parameters Usually Same
> ```
>
> This is one of the fastest interview distinctions.

---

> [!tip]
> **Shortcut 4 — Exact Match**
>
> If:
>
> ```text
> show(int)
> show(long)
> ```
>
> and:
>
> ```text
> show(10)
> ```
>
> choose:
>
> ```text
> show(int)
> ```

---

> [!tip]
> **Shortcut 5 — Quotes**
>
> ```text
> 'A' → char
> "A" → String
> ```

---

> [!tip]
> **Shortcut 6 — null**
>
> ```text
> String + Object + null
> → String
>
> String + Integer + null
> → Ambiguous
> ```

---

> [!tip]
> **Shortcut 7 — Varargs**
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
>
> for a normal single `int` argument because the fixed-arity overload is a better match.

---

# 54. Overload Resolution Strategy

When an interviewer gives multiple overloads, follow this process.

## Step 1 — Identify the argument types

Example:

    show(10);

Think:

```text
10 → int
```

## Step 2 — Search for exact match

```text
show(int)
```

If found, it is generally preferred.

## Step 3 — Check widening

Example:

```text
int → long
```

## Step 4 — Consider boxing/unboxing

Example:

```text
int → Integer
```

## Step 5 — Check reference-type specificity

Especially for:

```text
null
```

## Step 6 — Consider varargs

Varargs is generally considered later than fixed-arity alternatives.

## Step 7 — Check ambiguity

If two candidates are equally good and neither is more specific:

```text
Compile-time error
```

---

# 55. Example — Multiple Overloads

Consider:

    class Demo {

        void show(int x) {
            System.out.println("int");
        }

        void show(long x) {
            System.out.println("long");
        }

        void show(Integer x) {
            System.out.println("Integer");
        }

        void show(Object x) {
            System.out.println("Object");
        }
    }

Call:

    d.show(10);

### Step 1

```text
10 → int
```

### Step 2

Exact match exists:

```text
show(int)
```

### Step 3

Stop.

Output:

```text
int
```

The presence of `long`, `Integer`, and `Object` does not matter because the exact overload is available.

---

# 56. Example — No Exact Match

Consider:

    class Demo {

        void show(long x) {
            System.out.println("long");
        }

        void show(double x) {
            System.out.println("double");
        }

        void show(Integer x) {
            System.out.println("Integer");
        }
    }

Call:

    d.show(10);

Possible:

```text
int → long
int → double
int → Integer
```

For this common overload-resolution case, primitive widening is considered before boxing.

Among the widening candidates:

```text
int → long
```

is preferred over:

```text
int → double
```

Output:

```text
long
```

---

# 57. Advanced Example — `null`

Consider:

    class Demo {

        void print(Object x) {
            System.out.println("Object");
        }

        void print(String x) {
            System.out.println("String");
        }
    }

Call:

    d.print(null);

Possible:

```text
Object
String
```

Specificity:

```text
String → Object
```

Therefore:

```text
String
```

is more specific.

Output:

```text
String
```

---

# 58. Advanced Example — Ambiguous `null`

Consider:

    class Demo {

        void print(String x) {
            System.out.println("String");
        }

        void print(Integer x) {
            System.out.println("Integer");
        }
    }

Call:

    d.print(null);

Both are applicable.

But:

```text
String
```

is not a subtype of:

```text
Integer
```

and:

```text
Integer
```

is not a subtype of:

```text
String
```

Therefore:

```text
No most-specific method
```

Result:

$$
\boxed{\text{Compile-Time Error}}
$$

---

# 59. Advanced Example — Varargs

Consider:

    class Demo {

        void print(int x) {
            System.out.println("fixed");
        }

        void print(int... x) {
            System.out.println("varargs");
        }
    }

Call:

    d.print(10);

There is a direct fixed-arity match:

```text
print(int)
```

Therefore:

```text
fixed
```

is printed.

---

# 60. Advanced Example — Parameter Order

Consider:

    class Demo {

        void process(String name, int age) {
            System.out.println("Person");
        }

        void process(int age, String name) {
            System.out.println("Reversed");
        }
    }

Call:

    d.process(21, "Pradeep");

Argument types:

```text
int
String
```

Matching signature:

```text
process(int, String)
```

Output:

```text
Reversed
```

The parameter order matters.

---

# 61. Advanced Example — Return Type Trap

Consider:

    class Demo {

        int calculate(int x) {
            return x * 2;
        }

        double calculate(int x) {
            return x * 2.0;
        }
    }

Question:

Will this compile?

### Analysis

Both signatures are:

```text
calculate(int)
```

Return type differs:

```text
int
double
```

Return type alone cannot overload.

### Answer

$$
\boxed{\text{No — Compile-Time Error}}
$$

---

# 62. Advanced Example — Parameter Name Trap

Consider:

    class Demo {

        void calculate(int x) {
        }

        void calculate(int y) {
        }
    }

Both signatures:

```text
calculate(int)
```

Parameter names are irrelevant.

Therefore:

$$
\boxed{\text{Compile-Time Error}}
$$

---

# 63. Advanced Example — `final` Parameter Trap

Consider:

    class Demo {

        void calculate(int x) {
        }

        void calculate(final int x) {
        }
    }

The method signatures are still:

```text
calculate(int)
```

Therefore:

$$
\boxed{\text{Compile-Time Error}}
$$

---

# 64. Constructor Overloading

Constructors can also be overloaded.

Example:

    class Student {

        Student() {
            System.out.println("Default");
        }

        Student(String name) {
            System.out.println(name);
        }

        Student(String name, int age) {
            System.out.println(name + " " + age);
        }
    }

Now:

    new Student();

selects:

```text
Student()
```

while:

    new Student("Pradeep");

selects:

```text
Student(String)
```

and:

    new Student("Pradeep", 21);

selects:

```text
Student(String, int)
```

This topic will be covered deeply in the Constructors section.

---

# 65. Method Overloading in APIs

A good API often uses overloading when operations are conceptually identical.

For example:

```text
print()
print(String)
print(Object)
```

The caller recognizes:

```text
print
```

as the operation.

The parameter list determines the required variation.

This principle is used throughout Java libraries.

---

# 66. Important Interview Detail — Overloading and Inherited Methods

Suppose:

    class Parent {

        void show(int x) {
            System.out.println("Parent");
        }
    }

    class Child extends Parent {

        void show(String s) {
            System.out.println("Child");
        }
    }

For a `Child` object:

    Child c = new Child();

    c.show(10);

The inherited method:

```text
show(int)
```

is available.

The child method:

```text
show(String)
```

is also available.

The argument is:

```text
10 → int
```

Therefore:

```text
Parent.show(int)
```

is selected.

This shows that overload resolution can consider inherited methods.

---

# 67. Important Interview Detail — Overloading vs Reference Type

Consider:

    class Parent {

        void show(int x) {
            System.out.println("Parent int");
        }
    }

    class Child extends Parent {

        void show(String x) {
            System.out.println("Child String");
        }
    }

Now:

    Parent p = new Child();

    p.show(10);

The compile-time type of `p` is:

```text
Parent
```

So the compiler considers the methods available through the `Parent` type.

It finds:

```text
show(int)
```

Therefore:

```text
Parent int
```

This illustrates an important concept:

> [!important]
> **Overload resolution is primarily based on the compile-time type and argument types.**

Runtime dispatch is a separate concept associated with overriding.

---

# 68. Interview Trap — Overloading and Runtime Object

This distinction is critical.

```text
Overloading
↓
Compile-time method selection
↓
Reference/argument information matters
```

Whereas:

```text
Overriding
↓
Runtime dispatch
↓
Actual object type matters
```

This distinction is frequently used in advanced Java output questions.

---

# 69. Common Exam Patterns

> [!important] Must Master

### Pattern 1
Same method name with different parameter count.

### Pattern 2
Same method name with different parameter types.

### Pattern 3
Same method name with different parameter order.

### Pattern 4
Return type alone.

### Pattern 5
Parameter names only.

### Pattern 6
Access modifier only.

### Pattern 7
`final` parameter only.

### Pattern 8
`throws` clause only.

### Pattern 9
Primitive widening.

### Pattern 10
Exact match.

### Pattern 11
Boxing and unboxing.

### Pattern 12
`null` and reference specificity.

### Pattern 13
Ambiguous `null`.

### Pattern 14
Varargs.

### Pattern 15
Array vs varargs.

### Pattern 16
Static method overloading.

### Pattern 17
Static method hiding.

### Pattern 18
Constructor overloading.

### Pattern 19
Inherited overloads.

### Pattern 20
Compile-time reference type vs runtime object.

---

# 70. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Return Type Creates Overloading

Wrong:

```text
int get()
double get()
```

Correct:

```text
Return type alone cannot overload.
```

---

### Mistake 2 — Parameter Names Create Overloading

Wrong:

```text
show(int x)
show(int y)
```

Correct:

```text
Same signature.
```

---

### Mistake 3 — Access Modifier Creates Overloading

Wrong:

```text
public show(int)
private show(int)
```

Correct:

```text
Same parameter signature.
```

---

### Mistake 4 — `final` Creates Overloading

Wrong:

```text
show(int)
show(final int)
```

Correct:

```text
Same signature.
```

---

### Mistake 5 — `throws` Creates Overloading

Wrong:

```text
show() throws A
show() throws B
```

Correct:

```text
Throws clause does not distinguish overloads.
```

---

### Mistake 6 — Overloading Requires Inheritance

False.

A single class can contain multiple overloaded methods.

---

### Mistake 7 — Overloading and Overriding Are the Same

They are not.

```text
Overloading → Different parameters
Overriding → Same signature, child implementation
```

---

### Mistake 8 — Ignoring Exact Match

If:

```text
show(int)
show(long)
```

and:

```text
show(10)
```

then `show(int)` is preferred.

---

### Mistake 9 — Ignoring `null`

`null` can match multiple reference overloads.

Check specificity.

---

### Mistake 10 — Treating `int...` and `int[]` as Different

They represent the same parameter type for declaration purposes.

---

# 71. Interview Questions

## Beginner Level

### Q1. What is method overloading?

**Answer:**

Method overloading is defining multiple methods with the same name but different parameter lists.

---

### Q2. What type of polymorphism does method overloading represent?

**Answer:**

Compile-time polymorphism.

---

### Q3. Is method overloading compile-time or runtime?

**Answer:**

Compile-time.

---

### Q4. Does method overloading require inheritance?

**Answer:**

No.

---

### Q5. How can methods be overloaded?

**Answer:**

By changing:

```text
Parameter count
Parameter types
Parameter order
```

---

### Q6. Can return type alone overload a method?

**Answer:**

No.

---

### Q7. Can constructors be overloaded?

**Answer:**

Yes.

---

### Q8. Can static methods be overloaded?

**Answer:**

Yes.

---

# 72. Intermediate Interview Questions

### Q9. What is the difference between overloading and overriding?

**Answer:**

Overloading uses the same method name with different parameter lists and is associated with compile-time polymorphism.

Overriding uses the same method signature in a parent-child relationship and is associated with runtime polymorphism.

---

### Q10. Is the return type part of the method signature?

**Answer:**

No.

---

### Q11. Are parameter names part of the method signature?

**Answer:**

No.

---

### Q12. Can methods be overloaded by changing access modifiers?

**Answer:**

No.

---

### Q13. Can methods be overloaded by changing only the `throws` clause?

**Answer:**

No.

---

### Q14. Can static methods be overridden?

**Answer:**

No. They are hidden rather than overridden.

---

### Q15. Can a child class add an overload of a parent method?

**Answer:**

Yes.

A child can declare a method with the same name but a different parameter list.

---

# 73. Advanced Interview Questions

### Q16. Which overload is selected first?

**Answer:**

Java's overload-resolution process prefers the most specific applicable method according to its formal rules. For common interview problems, think:

```text
Exact match
↓
Primitive widening
↓
Other applicable conversions such as boxing
↓
Varargs
```

---

### Q17. What happens with `show(null)` when overloads are `show(String)` and `show(Object)`?

**Answer:**

`show(String)` is selected because `String` is more specific than `Object`.

---

### Q18. What happens with `show(null)` when overloads are `show(String)` and `show(Integer)`?

**Answer:**

The call is ambiguous because neither type is more specific than the other.

---

### Q19. Can `int[]` and `int...` be overloaded separately?

**Answer:**

No. `int...` corresponds to `int[]` for the method declaration.

---

### Q20. Can methods be overloaded using generic parameter differences?

**Answer:**

It depends on whether the resulting erased signatures are distinct. Java generics use type erasure, so seemingly different generic declarations can have the same erased signature and cause a name clash.

---

# 74. Advanced Generic Overloading Trap

Consider:

    void process(List<String> list)

    void process(List<Integer> list)

This does not work as two independent overloads because Java's type erasure removes the generic type argument.

After erasure, both effectively become:

```text
process(List)
```

Therefore they have the same erased signature.

Result:

```text
Name clash / compile-time error
```

> [!important]
> This is an advanced interview topic:
>
> **Generics can look different at source level but become the same after type erasure.**

---

# 75. Advanced Interview Trap — Generic Arrays

Be careful with:

    void process(List<String> list)

and:

    void process(ArrayList<String> list)

These parameter types are different:

```text
List
ArrayList
```

and may form valid overloads because their erased parameter types remain different.

However, overload resolution and inheritance relationships still determine which method is selected.

---

# 76. Advanced Interview Trap — Varargs and Overload

Consider:

    void test(int x)

    void test(int... x)

Call:

    test(10);

The fixed-arity method is preferred.

Therefore:

```text
test(int)
```

is selected.

But:

    test();

can only match:

```text
test(int...)
```

Therefore varargs is selected.

---

# 77. Advanced Interview Trap — Reference Widening

Consider:

    class Parent {
    }

    class Child extends Parent {
    }

    void show(Parent p) {
        System.out.println("Parent");
    }

    void show(Object o) {
        System.out.println("Object");
    }

Call:

    Child c = new Child();

    show(c);

Both are applicable:

```text
Child → Parent
Child → Object
```

`Parent` is more specific than `Object`.

Therefore:

```text
Parent
```

is selected.

---

# 78. High-Level Problem-Solving Framework

When solving an overload question, never guess.

Use:

```text
INPUT
  ↓
Identify argument types
  ↓
List all candidate methods
  ↓
Check exact match
  ↓
Check widening
  ↓
Check reference specificity
  ↓
Check boxing/unboxing
  ↓
Check varargs
  ↓
Choose most specific
  ↓
If no unique best method:
AMBIGUOUS
```

This approach is much more reliable than memorizing isolated examples.

---

# 79. One-Minute Interview Explanation

If an interviewer asks:

**"Explain method overloading."**

Use this answer:

> Method overloading is a compile-time polymorphism mechanism in Java where multiple methods have the same name but different parameter lists. The difference can be in the number, type, or order of parameters. Return type alone cannot create an overload. The compiler determines the appropriate method based on the compile-time argument information. For example, `add(int,int)` and `add(double,double)` are overloaded methods.

---

# 80. Placement MCQ Strategy

When you see a question containing several methods:

### First

Ignore implementation details.

### Second

Write only:

```text
methodName(parameter types)
```

### Third

Compare signatures.

Example:

```text
add(int,int)
add(int,int,int)
add(double,double)
```

Immediately recognize:

```text
Overloading
```

### Fourth

If a call is given:

```text
add(10,20)
```

identify:

```text
int,int
```

Then find the best matching overload.

---

# 81. Ultimate Recognition Table

| Code Pattern | Result |
|---|---|
| `show(int)` + `show(int,int)` | Overloading |
| `show(int)` + `show(String)` | Overloading |
| `show(int,String)` + `show(String,int)` | Overloading |
| `show(int)` + `show(int)` | Duplicate |
| `int show()` + `double show()` | Invalid |
| `show(int x)` + `show(int y)` | Duplicate |
| `public show(int)` + `private show(int)` | Duplicate |
| `show(int)` + `show(final int)` | Duplicate |
| `show() throws A` + `show() throws B` | Duplicate |
| `show(int)` + `show(Integer)` | Valid overloads |
| `show(int)` + `show(long)` | Valid overloads |
| `show(int)` + `show(int...)` | Valid overloads |
| `show(int[])` + `show(int...)` | Conflict |
| `show(String)` + `show(Object)` + `null` | `String` |
| `show(String)` + `show(Integer)` + `null` | Ambiguous |
| Overloaded constructor | Valid |
| Overloaded static method | Valid |
| Static same-signature child method | Hiding |
| Parent-child same instance signature | Overriding |

---

# 82. Formula Sheet

```text
METHOD OVERLOADING

Same method name
+
Different parameter list
=
Method Overloading

Overloading
=
Compile-Time Polymorphism

Different parameters can mean:

1. Different number
2. Different types
3. Different order

Method Signature
=
Method Name + Parameter Types

Return Type:
NOT part of overload signature

Cannot overload using only:
- Return type
- Parameter names
- Access modifiers
- final parameter modifier
- throws clause

Overloading:
Does NOT require inheritance

Overriding:
Requires inheritance

Exact match:
Preferred over conversion

Primitive widening:
byte → short → int → long → float → double

char → int → long → float → double

Boxing:
int → Integer

Unboxing:
Integer → int

Varargs:
int... → int[]

Static methods:
Can be overloaded
Are hidden, not overridden

Constructors:
Can be overloaded
Cannot be overridden

null:
Matches reference types

String + Object + null:
String is more specific

String + Integer + null:
Ambiguous

Generic overloads:
Type erasure can cause signature clashes
```

---

# 83. Quick Revision

> [!summary] One-Minute Revision

### Definition

**Method overloading means multiple methods have the same name but different parameter lists.**

### Three Main Ways

```text
1. Different parameter count

2. Different parameter type

3. Different parameter order
```

### Example

    add(int, int)

    add(int, int, int)

    add(double, double)

All are overloads.

### Does Return Type Matter?

```text
No.
```

This is invalid:

    int get()

    double get()

### Compile-Time Relationship

```text
Overloading
     ↓
Compile Time
     ↓
Static / Early Binding
```

### Runtime Relationship

```text
Overriding
     ↓
Runtime
     ↓
Dynamic Binding
```

### Fast Interview Formula

```text
OVERLOAD
= SAME NAME
+ DIFFERENT PARAMETERS

OVERRIDE
= SAME SIGNATURE
+ CHILD IMPLEMENTATION
```

### Parameter Recognition

```text
COUNT
TYPE
ORDER
```

If one changes:

```text
Overloading
```

### Important Traps

```text
Return type only
→ Invalid

Parameter name only
→ Invalid

Access modifier only
→ Invalid

final parameter only
→ Invalid

throws clause only
→ Invalid

int[] vs int...
→ Same declaration type

null + unrelated reference overloads
→ Ambiguous
```

### Golden Memory Trick

**Overloading means the same operation gets different parameter forms, and the compiler chooses the appropriate form.**

### One-Line Recognition

**When you see the same method name with a different parameter count, type, or order, immediately think Method Overloading and Compile Time Polymorphism.**