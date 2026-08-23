---
type: concept
subject: coding
topic: "Variables and Data Types"
parent: "Programming Fundamentals"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - variables
  - data-types
  - programming
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Input and Output]]"
  - "[[Type Casting]]"
---

# Variables and Data Types

## 1. Core Concept

> [!summary]
> A **variable** is a named memory location used to store a value.
> A **data type** tells the programming language what kind of value can be stored and how that value should be handled.

### Basic Idea

Think of a variable as a labeled box.

~~~text
age → [21]
name → ["Pradeep"]
marks → [85.5]
isPassed → [true]
~~~

The variable name identifies the box, while the data type describes what can be stored inside it.

$$
\text{Variable} = \text{Name} + \text{Data Type} + \text{Value}
$$

### Example

~~~java
int age = 21;
~~~

Here:

- `int` → data type
- `age` → variable name
- `21` → value
- `=` → assignment operator

---

## 2. Basic Meaning

### What is a Variable?

A variable is a named storage location whose value can usually be changed during program execution.

Example:

~~~java
int age = 20;
age = 21;
~~~

Initially:

$$
age = 20
$$

After reassignment:

$$
age = 21
$$

### What is a Data Type?

A data type defines:

1. What kind of data can be stored.
2. How the data is represented.
3. What operations can be performed on it.
4. How much memory is generally required.

Example:

~~~java
int age = 21;
double salary = 45000.50;
char grade = 'A';
boolean passed = true;
~~~

---

## 3. Main Data Types

The examples in this note use **Java**.

### Primitive Data Types

Java has 8 primitive data types.

| Data Type | Typical Size | Example | Purpose |
|---|---:|---|---|
| `byte` | 8 bits | `byte x = 10;` | Small integers |
| `short` | 16 bits | `short x = 1000;` | Small/medium integers |
| `int` | 32 bits | `int x = 100000;` | General integers |
| `long` | 64 bits | `long x = 100000L;` | Large integers |
| `float` | 32 bits | `float x = 10.5f;` | Decimal values |
| `double` | 64 bits | `double x = 10.5;` | More precise decimals |
| `char` | 16 bits | `char c = 'A';` | Single character |
| `boolean` | JVM-dependent | `boolean b = true;` | `true` / `false` |

> [!important]
> For most coding problems, `int` is the default choice for normal integers and `long` is used when the range may exceed `int`.

---

## 4. Integer Data Types

Integer types store whole numbers.

~~~java
byte a = 10;
short b = 1000;
int c = 100000;
long d = 10000000000L;
~~~

### Range

For a signed integer type using $n$ bits:

$$
-2^{n-1} \leq x \leq 2^{n-1}-1
$$

### Common Java Ranges

| Type | Bits | Range |
|---|---:|---|
| `byte` | 8 | $-128$ to $127$ |
| `short` | 16 | $-32768$ to $32767$ |
| `int` | 32 | $-2^{31}$ to $2^{31}-1$ |
| `long` | 64 | $-2^{63}$ to $2^{63}-1$ |

For `int`:

$$
-2^{31} \leq x \leq 2^{31}-1
$$

Therefore:

$$
-2147483648 \leq x \leq 2147483647
$$

> [!tip]
> If a problem involves values larger than about $2.1$ billion, immediately consider using `long`.

---

## 5. Floating-Point Data Types

Floating-point types store decimal values.

### `float`

~~~java
float price = 99.5f;
~~~

The suffix `f` is required when assigning a decimal literal to a `float`.

### `double`

~~~java
double salary = 45000.75;
~~~

`double` provides greater precision than `float`.

> [!important]
> In most coding problems, prefer `double` for decimal calculations unless the problem specifically requires `float`.

---

## 6. Character Data Type

`char` stores a single character.

~~~java
char grade = 'A';
char symbol = '#';
char digit = '5';
~~~

Characters use **single quotes**.

Correct:

~~~java
char ch = 'A';
~~~

Incorrect:

~~~java
char ch = "A";
~~~

`"A"` is a string, while `'A'` is a character.

---

## 7. Boolean Data Type

A boolean stores one of two logical values:

~~~java
boolean isPassed = true;
boolean isLoggedIn = false;
~~~

Possible values:

~~~text
true
false
~~~

Example:

~~~java
int age = 21;
boolean adult = age >= 18;
~~~

Result:

$$
adult = true
$$

---

## 8. Reference Data Types

Java also has reference types.

Common examples:

~~~text
String
Array
Class
Object
Interface
~~~

Example:

~~~java
String name = "Pradeep";
~~~

Here `String` is not a primitive data type.

| Primitive | Reference |
|---|---|
| `int` | `String` |
| `double` | Array |
| `char` | Object |
| `boolean` | Class |

> [!important]
> `String` is frequently confused with a primitive data type. In Java, `String` is a class/reference type.

---

## 9. Variable Declaration and Initialization

### Declaration

Creating a variable without assigning a value:

~~~java
int age;
~~~

### Initialization

Assigning a value:

~~~java
age = 21;
~~~

### Declaration + Initialization

Both can be done together:

~~~java
int age = 21;
~~~

### Pattern

| Operation | Syntax |
|---|---|
| Declaration | `dataType variableName;` |
| Initialization | `variableName = value;` |
| Both | `dataType variableName = value;` |

---

## 10. Basic Examples

### Example 1 — Integer Variable

**Question**

Create a variable to store the age `21`.

**Pattern**

Whole number → `int`

**Calculation**

~~~java
int age = 21;
~~~

Therefore:

$$
age = 21
$$

**Answer**

$$
\boxed{age = 21}
$$

---

### Example 2 — Multiple Variables

**Question**

Store a student's age, marks, and grade.

**Pattern**

- Age → integer
- Marks → decimal
- Grade → character

**Calculation**

~~~java
int age = 21;
double marks = 87.5;
char grade = 'A';
~~~

Therefore:

~~~text
age   → 21
marks → 87.5
grade → A
~~~

**Answer**

$$
\boxed{\text{age}=21,\ \text{marks}=87.5,\ \text{grade}=A}
$$

---

### Example 3 — Boolean Expression

**Question**

A student passes if marks are at least `40`. Determine whether a student with `65` marks passes.

**Pattern**

Condition → Boolean.

**Calculation**

~~~java
int marks = 65;
boolean passed = marks >= 40;
~~~

Since:

$$
65 \geq 40
$$

Therefore:

$$
passed = true
$$

**Answer**

$$
\boxed{true}
$$

---

## 11. Advanced Examples

### Example 4 — Integer Overflow

**Question**

What happens here?

~~~java
int x = 2147483647;
x = x + 1;
~~~

**Pattern**

Maximum `int` value + `1`.

Maximum `int` value:

$$
2^{31}-1=2147483647
$$

Adding `1` causes integer overflow.

The result becomes:

$$
-2147483648
$$

**Answer**

$$
\boxed{-2147483648}
$$

> [!warning]
> Always check the range of the data before selecting a numeric type.

---

### Example 5 — Large Number

**Question**

Store:

$$
10,000,000,000
$$

Can it safely be stored in an `int`?

**Pattern**

Check the value against the `int` range.

Maximum `int`:

$$
2147483647
$$

But:

$$
10,000,000,000 > 2,147,483,647
$$

Therefore `int` is insufficient.

Use:

~~~java
long n = 10000000000L;
~~~

**Answer**

$$
\boxed{\text{Use long}}
$$

---

### Example 6 — Character vs String

**Question**

Which correctly stores the letter `A`?

Option 1:

~~~java
char a = 'A';
~~~

Option 2:

~~~java
char a = "A";
~~~

**Pattern**

Single character → `char` → single quotes.

Therefore:

~~~java
char a = 'A';
~~~

**Answer**

$$
\boxed{\texttt{char a = 'A';}}
$$

---

## 12. Type Selection

Use this quick decision table:

| Requirement | Recommended Type |
|---|---|
| Small integer | `byte` / `short` |
| Normal integer | `int` |
| Very large integer | `long` |
| Decimal value | `double` |
| Single character | `char` |
| True/false | `boolean` |
| Text | `String` |

> [!tip]
> Coding-problem default:
>
> Integer → `int`  
> Large integer → `long`  
> Decimal → `double`  
> Character → `char`  
> Text → `String`  
> Condition → `boolean`

---

## 13. Variable Naming Rules

Java variable names can contain:

- Letters
- Digits
- `_`
- `$`

But a variable name:

- Cannot start with a digit.
- Cannot contain spaces.
- Cannot be a Java keyword.
- Is case-sensitive.

### Valid

~~~java
int age;
int studentAge;
int student_age;
int age2;
~~~

### Invalid

~~~java
int 2age;
int student age;
int class;
~~~

---

## 14. Case Sensitivity

Java is case-sensitive.

These are different variables:

~~~java
int age = 20;
int Age = 30;
int AGE = 40;
~~~

Therefore:

$$
age \neq Age \neq AGE
$$

> [!warning]
> `count`, `Count`, and `COUNT` are three different identifiers.

---

## 15. Constants

A variable whose value should not change can be declared using `final`.

~~~java
final double PI = 3.14159;
~~~

Attempting to change it:

~~~java
PI = 3.14;
~~~

causes a compilation error.

### Pattern

$$
\texttt{final} \rightarrow \text{cannot be reassigned}
$$

---

## 16. Scope of Variables

Scope determines where a variable can be accessed.

Example:

~~~java
public static void main(String[] args) {
    int x = 10;

    if (x > 5) {
        int y = 20;
        System.out.println(y);
    }
}
~~~

`x` is accessible throughout the method.

`y` exists only inside the `if` block.

~~~text
main scope
│
├── x
│
└── if scope
    └── y
~~~

> [!important]
> A variable declared inside a block generally cannot be accessed outside that block.

---

## 17. Default Values in Java

Instance and class variables receive default values.

| Type | Default Value |
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

> [!warning]
> Local variables do **not** automatically receive default values. They must be initialized before use.

Example:

~~~java
public static void main(String[] args) {
    int x;
    System.out.println(x);
}
~~~

This produces a compilation error because `x` has not been initialized.

---

## 18. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Choose the Correct Data Type

Question gives a value and asks which type should store it.

Think:

~~~text
Normal integer → int
Large integer → long
Decimal → double
Character → char
True/False → boolean
Text → String
~~~

---

### Pattern 2 — Detect Overflow

Look for:

~~~text
maximum value + something
minimum value - something
large multiplication
large addition
~~~

Think:

$$
\text{Check data-type range}
$$

---

### Pattern 3 — Character vs String

Look for:

~~~text
'A' → char
"A" → String
~~~

---

### Pattern 4 — Variable Scope

Look for:

~~~text
variable declared inside a block
~~~

Think:

$$
\text{Can this variable be accessed outside the block?}
$$

---

### Pattern 5 — Constant Variable

Look for:

~~~java
final
~~~

Think:

$$
\text{Cannot be reassigned}
$$

---

### Pattern 6 — Type Selection Using Constraints

Look at the constraints before choosing the type.

Example:

~~~text
1 ≤ n ≤ 10^9
~~~

`int` is generally sufficient.

Example:

~~~text
1 ≤ n ≤ 10^18
~~~

Use:

~~~java
long
~~~

> [!important]
> In coding problems, constraints often tell you which data type is safe.

---

## 19. Recognition Tricks

> [!important]
> If the question says **whole number**, think `int`.

> [!important]
> If the number can exceed **2,147,483,647**, think `long`.

> [!important]
> If the question involves **decimal values**, think `double`.

> [!important]
> If exactly **one character** is required, think `char`.

> [!important]
> If the answer is **yes/no** or **true/false**, think `boolean`.

> [!important]
> If the input is **text**, think `String`.

> [!important]
> If you see `final`, think **constant / cannot reassign**.

---

## 20. Shortcuts

> [!tip]
> **Shortcut: I-L-D-C-B-S**
>
> **I**nt → normal integers  
> **L**ong → large integers  
> **D**ouble → decimals  
> **C**har → single character  
> **B**oolean → true/false  
> **S**tring → text

> [!tip]
> **Shortcut: Check constraints first.**
>
> Before selecting `int` or `long`, look at the maximum possible value.

> [!tip]
> **Shortcut: Remember numeric literal suffixes.**
>
> `L` → long  
> `f` → float

Examples:

~~~java
long x = 10000000000L;
float y = 10.5f;
~~~

---

## 21. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Using `int` for Very Large Values

Wrong:

~~~java
int x = 10000000000;
~~~

Correct:

~~~java
long x = 10000000000L;
~~~

Why?

The value exceeds the `int` range.

---

### Mistake 2 — Using Double Quotes for `char`

Wrong:

~~~java
char ch = "A";
~~~

Correct:

~~~java
char ch = 'A';
~~~

Remember:

$$
\texttt{'A'} \rightarrow char
$$

$$
\texttt{"A"} \rightarrow String
$$

---

### Mistake 3 — Forgetting `f` for Float

Wrong:

~~~java
float x = 10.5;
~~~

Correct:

~~~java
float x = 10.5f;
~~~

---

### Mistake 4 — Assuming Local Variables Have Default Values

Wrong assumption:

~~~java
int x;
System.out.println(x);
~~~

Local variables must be initialized before use.

---

### Mistake 5 — Ignoring Overflow

Example:

~~~java
int a = 100000;
int b = 100000;
int result = a * b;
~~~

Mathematical result:

$$
100000 \times 100000 = 10,000,000,000
$$

This exceeds the `int` range.

Safer approach:

~~~java
long result = (long) a * b;
~~~

> [!important]
> Cast before multiplication when necessary. Casting the final overflowed result is too late.

---

### Mistake 6 — Confusing Declaration and Initialization

Declaration:

~~~java
int age;
~~~

Initialization:

~~~java
age = 21;
~~~

Both together:

~~~java
int age = 21;
~~~

---

### Mistake 7 — Confusing `=` and `==`

Assignment:

~~~java
x = 10;
~~~

Comparison:

~~~java
x == 10;
~~~

Remember:

$$
= \rightarrow \text{assignment}
$$

$$
== \rightarrow \text{comparison}
$$

---

## 22. Formula Sheet

### Signed Integer Range

$$
-2^{n-1} \leq x \leq 2^{n-1}-1
$$

### Java `byte`

$$
-2^7 \leq x \leq 2^7-1
$$

### Java `short`

$$
-2^{15} \leq x \leq 2^{15}-1
$$

### Java `int`

$$
-2^{31} \leq x \leq 2^{31}-1
$$

### Java `long`

$$
-2^{63} \leq x \leq 2^{63}-1
$$

### Bit Conversion

$$
1\text{ byte}=8\text{ bits}
$$

$$
1\text{ KB}=1024\text{ bytes}
$$

$$
1\text{ MB}=1024\text{ KB}
$$

---

## 23. Quick Revision

> [!summary] One-Minute Revision

| Concept | Remember |
|---|---|
| Variable | Named storage location |
| Data Type | Defines kind of value |
| `int` | Normal integer |
| `long` | Large integer |
| `float` | Decimal, lower precision |
| `double` | Decimal, higher precision |
| `char` | Single character |
| `boolean` | `true` / `false` |
| `String` | Text/reference type |
| `final` | Cannot be reassigned |
| `int` range | $-2^{31}$ to $2^{31}-1$ |
| `long` range | $-2^{63}$ to $2^{63}-1$ |
| `'A'` | `char` |
| `"A"` | `String` |

### Golden Memory Trick

**Choose the data type based on the value's nature and range, not just its appearance.**

### One-Line Recognition

**When a coding problem gives you a value or constraint, first identify its type and range, then choose the smallest safe data type.**
:::