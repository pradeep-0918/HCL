---
type: concept
subject: coding
topic: "Type Casting"
parent: "Programming Fundamentals"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - type-casting
  - type-conversion
  - java
  - programming
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Variables and Data Types]]"
  - "[[Operators]]"
  - "[[Functions and Methods]]"
---

# Type Casting

## 1. Core Concept

> [!summary]
> **Type casting** means converting a value from one data type to another data type.

Example:

~~~java
int x = 10;
double y = (double) x;
~~~

Here:

$$
int \rightarrow double
$$

The value `10` is converted from `int` to `double`.

### Basic Idea

~~~text
Original Type
     ↓
Conversion
     ↓
New Type
~~~

Example:

~~~text
int → double
double → int
char → int
long → int
~~~

---

# 2. Basic Meaning

Programming problems often require different data types to work together.

Example:

~~~java
int a = 5;
double b = 2.5;

double result = a + b;
~~~

Java converts `a` to a compatible type during the operation.

Type conversion can be:

1. **Widening conversion**
2. **Narrowing conversion**
3. **Implicit conversion**
4. **Explicit conversion**

---

# 3. Widening Type Casting

Widening means converting a smaller-range type into a larger-range compatible type.

Example:

~~~java
int x = 100;
long y = x;
~~~

Here:

$$
int \rightarrow long
$$

No explicit cast is normally required.

### Common Widening Path

~~~text
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
~~~

> [!important]
> Widening generally does not require explicit casting because the destination type can represent the source type's values within the relevant numeric model.

---

# 4. Implicit Type Conversion

When Java automatically converts one compatible type into another, it is called implicit conversion.

Example:

~~~java
int x = 10;
double y = x;
~~~

Java automatically converts:

$$
10 \rightarrow 10.0
$$

Therefore:

~~~text
x = 10
y = 10.0
~~~

No explicit cast is required.

---

# 5. Narrowing Type Casting

Narrowing means converting a type with a wider range into a type with a smaller range.

Example:

~~~java
double x = 10.75;
int y = (int) x;
~~~

Here:

$$
double \rightarrow int
$$

The fractional part is removed.

Therefore:

$$
10.75 \rightarrow 10
$$

### Important

Narrowing usually requires explicit casting.

Syntax:

~~~java
targetType variable = (targetType) value;
~~~

Example:

~~~java
int x = (int) 10.75;
~~~

---

# 6. Explicit Type Casting

Explicit casting means telling Java exactly which type you want.

Syntax:

~~~java
(targetType) value
~~~

Example:

~~~java
double x = 25.8;

int y = (int) x;
~~~

Result:

$$
y=25
$$

> [!warning]
> Casting a floating-point value to an integer does **not** round it. The fractional part is discarded.

---

# 7. Basic Examples

## Example 1 — Int to Double

### Question

Convert `10` from `int` to `double`.

### Pattern

Smaller numeric type → larger compatible type.

### Code

~~~java
int x = 10;
double y = x;
~~~

Therefore:

$$
y=10.0
$$

### Answer

$$
\boxed{10.0}
$$

---

## Example 2 — Double to Int

### Question

Convert `15.75` to an integer.

### Pattern

`double` → `int` requires explicit casting.

### Code

~~~java
double x = 15.75;
int y = (int) x;
~~~

Fractional part:

$$
0.75
$$

is discarded.

Therefore:

$$
y=15
$$

### Answer

$$
\boxed{15}
$$

---

## Example 3 — Long to Int

### Question

Convert a `long` value to `int`.

~~~java
long x = 100;
int y = (int) x;
~~~

Since the value fits inside `int`:

$$
y=100
$$

### Answer

$$
\boxed{100}
$$

> [!warning]
> If the `long` value is outside the `int` range, narrowing conversion can produce an unexpected result.

---

# 8. Character and Integer Conversion

In Java, `char` is a numeric type representing a UTF-16 code unit.

A `char` can be converted to an integer.

Example:

~~~java
char ch = 'A';
int x = ch;
~~~

The integer value corresponds to the Unicode code unit for `A`.

For common English characters:

$$
'A'=65
$$

Therefore:

$$
x=65
$$

### Reverse Conversion

~~~java
int x = 65;
char ch = (char) x;
~~~

Result:

~~~text
A
~~~

> [!important]
> Character-to-integer conversion is useful in character and string problems.

---

# 9. Example — Character to Integer

## Example 4

### Question

Find the integer value of:

~~~text
'A'
~~~

### Code

~~~java
char ch = 'A';
int value = ch;
~~~

Therefore:

$$
'A'=65
$$

### Answer

$$
\boxed{65}
$$

---

# 10. Example — Digit Character to Integer

## Example 5

### Question

Convert character `'7'` into integer `7`.

### Pattern

Digit character:

~~~text
'0' → 0
'1' → 1
...
'9' → 9
~~~

A common formula is:

$$
digit=ch-'0'
$$

### Code

~~~java
char ch = '7';

int digit = ch - '0';
~~~

Since:

$$
'7'-'0'=7
$$

### Answer

$$
\boxed{7}
$$

> [!important]
> This pattern is extremely common in string and digit problems.

---

# 11. Integer to Digit Character

The reverse conversion can be done using:

$$
ch=(char)('0'+digit)
$$

Example:

~~~java
int digit = 5;

char ch = (char) ('0' + digit);
~~~

Result:

~~~text
'5'
~~~

### Answer

$$
\boxed{'5'}
$$

> [!tip]
> Remember:
>
> Character digit → integer:
>
> $$ch-'0'$$
>
> Integer digit → character:
>
> $$'0'+digit$$

---

# 12. Integer Division and Casting

This is one of the most important placement traps.

Consider:

~~~java
int a = 5;
int b = 2;

double result = a / b;
~~~

You may expect:

$$
2.5
$$

But Java first performs integer division:

$$
5/2=2
$$

Then stores `2` as:

$$
2.0
$$

Therefore:

$$
result=2.0
$$

---

# 13. Correct Decimal Division

To obtain:

$$
2.5
$$

cast one operand before division.

~~~java
int a = 5;
int b = 2;

double result = (double) a / b;
~~~

Now:

$$
5.0/2=2.5
$$

### Answer

$$
\boxed{2.5}
$$

> [!important]
> **Cast before the operation**, not after it.

---

# 14. Wrong vs Correct Casting

### Wrong

~~~java
double result = (double) (5 / 2);
~~~

First:

$$
5/2=2
$$

Then:

$$
(double)2=2.0
$$

Result:

$$
\boxed{2.0}
$$

### Correct

~~~java
double result = (double) 5 / 2;
~~~

Now:

$$
5.0/2=2.5
$$

Result:

$$
\boxed{2.5}
$$

> [!important]
> This is a very common coding interview and placement mistake.

---

# 15. Type Promotion in Expressions

Java may automatically promote smaller numeric types during arithmetic.

Example:

~~~java
byte a = 10;
byte b = 20;

int result = a + b;
~~~

The arithmetic result is promoted to `int`.

Therefore:

$$
result=30
$$

This is why:

~~~java
byte c = a + b;
~~~

does not compile without an explicit cast.

You would need:

~~~java
byte c = (byte) (a + b);
~~~

if the result is known to fit.

> [!important]
> Arithmetic involving `byte`, `short`, and `char` commonly promotes the operands to `int`.

---

# 16. Example — Byte Promotion

## Example 6

### Question

What is the type of:

~~~java
byte a = 10;
byte b = 20;

var result = a + b;
~~~

### Pattern

`byte` arithmetic is promoted to `int`.

Therefore:

~~~text
result → int
value → 30
~~~

### Answer

$$
\boxed{int,\ 30}
$$

---

# 17. Overflow During Narrowing

Narrowing can lose information.

Example:

~~~java
int x = 130;
byte y = (byte) x;
~~~

A Java `byte` has range:

$$
-128\leq x\leq127
$$

The value `130` is outside this range.

The result is:

$$
130\rightarrow-126
$$

### Answer

$$
\boxed{-126}
$$

> [!warning]
> Explicit casting does not guarantee that the original value will be preserved.

---

# 18. Example — Narrowing Overflow

## Example 7

### Question

Find the value of:

~~~java
int x = 128;
byte y = (byte) x;
~~~

### Pattern

`int` → `byte` is narrowing.

`byte` range:

$$
-128\text{ to }127
$$

The value `128` cannot be represented directly.

The resulting byte value is:

$$
-128
$$

### Answer

$$
\boxed{-128}
$$

---

# 19. Type Casting in Expressions

Consider:

~~~java
int a = 10;
double b = 3.0;

double result = a / b;
~~~

Java promotes `a` to `double`.

Therefore:

$$
10/3.0=3.333...
$$

Result:

$$
\boxed{3.333...}
$$

### Pattern

If one operand is `double`, the arithmetic operation can be performed in floating-point arithmetic.

---

# 20. Mixed Data Types

Example:

~~~java
int a = 10;
long b = 20;
double c = 2.5;

double result = a + b + c;
~~~

The values are promoted as necessary so the expression can be evaluated in a compatible type.

Conceptually:

~~~text
int
 ↓
long
 ↓
double
~~~

Therefore:

$$
10+20+2.5=32.5
$$

### Answer

$$
\boxed{32.5}
$$

---

# 21. String Conversion

Type casting and parsing are different concepts.

For example:

~~~java
String s = "123";
int n = Integer.parseInt(s);
~~~

This is **parsing**, not primitive numeric casting.

The string:

~~~text
"123"
~~~

becomes:

$$
123
$$

### Common Parsing Methods

| Conversion | Method |
|---|---|
| `String` → `int` | `Integer.parseInt()` |
| `String` → `long` | `Long.parseLong()` |
| `String` → `double` | `Double.parseDouble()` |
| `String` → `float` | `Float.parseFloat()` |

---

# 22. Parsing vs Casting

### Casting

Changes between compatible types.

~~~java
double x = 10.5;
int y = (int) x;
~~~

### Parsing

Converts text representing a value into a numeric type.

~~~java
String s = "10";
int x = Integer.parseInt(s);
~~~

| Operation | Example |
|---|---|
| Casting | `int → double` |
| Casting | `double → int` |
| Parsing | `String → int` |
| Parsing | `String → double` |

> [!important]
> Do not say `(int) "123"` in Java. A `String` must be parsed.

---

# 23. Example — String to Integer

## Example 8

### Question

Convert `"250"` into an integer.

### Pattern

String containing a number → parsing.

### Code

~~~java
String s = "250";

int n = Integer.parseInt(s);
~~~

Therefore:

$$
n=250
$$

### Answer

$$
\boxed{250}
$$

---

# 24. Example — Integer to String

## Example 9

### Question

Convert integer `100` into a string.

### Code

~~~java
int n = 100;

String s = String.valueOf(n);
~~~

Result:

~~~text
"100"
~~~

Another common method:

~~~java
String s = Integer.toString(n);
~~~

### Answer

$$
\boxed{"100"}
$$

---

# 25. Boolean Conversion

Java does not allow arbitrary numeric-to-boolean casting.

This is invalid:

~~~java
int x = 1;
boolean b = (boolean) x;
~~~

Java requires an explicit logical condition.

Correct:

~~~java
boolean b = x != 0;
~~~

For:

$$
x=1
$$

we get:

$$
b=true
$$

> [!important]
> Java does not treat `1` as `true` and `0` as `false` through casting.

---

# 26. Advanced Example — Average

## Example 10

### Question

Find the average of:

$$
10,\ 20,\ 30
$$

and make sure the result is decimal.

### Wrong

~~~java
int a = 10;
int b = 20;
int c = 30;

double avg = (a + b + c) / 3;
~~~

The division is integer division.

### Correct

~~~java
double avg = (double) (a + b + c) / 3;
~~~

Calculation:

$$
\frac{10+20+30}{3}
$$

$$
=\frac{60}{3}
$$

$$
=20.0
$$

### Answer

$$
\boxed{20.0}
$$

---

# 27. Advanced Example — Percentage

## Example 11

### Question

A student scores `45` out of `80`. Find the percentage.

### Formula

$$
Percentage=\frac{marks}{total}\times100
$$

### Wrong Approach

~~~java
double percentage =
    (45 / 80) * 100;
~~~

Because:

$$
45/80=0
$$

under integer division.

Therefore:

$$
0\times100=0
$$

### Correct Approach

~~~java
double percentage =
    (double) 45 / 80 * 100;
~~~

Calculation:

$$
\frac{45}{80}\times100
$$

$$
=56.25
$$

### Answer

$$
\boxed{56.25\%}
$$

---

# 28. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Integer to Double

If you see:

~~~text
int → double
~~~

Think:

$$
\text{Widening / implicit conversion}
$$

Usually:

~~~java
double x = intValue;
~~~

---

### Pattern 2 — Double to Integer

If you see:

~~~text
double → int
~~~

Think:

~~~java
(int) value
~~~

Remember:

$$
10.99\rightarrow10
$$

The fractional part is discarded.

---

### Pattern 3 — Decimal Division

If the question expects a decimal result:

~~~text
Cast before division.
~~~

Use:

~~~java
(double) a / b
~~~

---

### Pattern 4 — Character Digit to Integer

If you see:

~~~text
'7'
~~~

and need:

~~~text
7
~~~

Think:

$$
ch-'0'
$$

---

### Pattern 5 — Integer Digit to Character

If you have:

~~~text
7
~~~

and need:

~~~text
'7'
~~~

Think:

$$
(char)('0'+digit)
$$

---

### Pattern 6 — String to Number

If input is:

~~~text
"123"
~~~

and you need integer `123`:

~~~java
Integer.parseInt(s)
~~~

Think:

$$
\text{String → parsing}
$$

---

### Pattern 7 — Large to Small Type

If you see:

~~~text
long → int
int → byte
~~~

Think:

$$
\text{Narrowing → explicit cast}
$$

Check for possible data loss.

---

### Pattern 8 — Byte/Short Arithmetic

If you see arithmetic involving:

~~~text
byte
short
char
~~~

Think:

$$
\text{Arithmetic promotion → int}
$$

---

# 29. Recognition Tricks

> [!important]
> If the destination type can safely represent the source value, think **widening conversion**.

> [!important]
> If you convert `double` to `int`, think **fractional part is discarded**.

> [!important]
> If decimal division is required, think **cast before division**.

> [!important]
> If you see `'7'`, think **character**, not integer.

> [!important]
> If you need integer `7` from `'7'`, think:

$$
'7'-'0'
$$

> [!important]
> If you need `'7'` from integer `7`, think:

$$
'0'+7
$$

> [!important]
> If a number is stored inside a `String`, think **parse**, not cast.

> [!important]
> If a smaller type is converted to a larger type, think **widening**.

> [!important]
> If a larger type is converted to a smaller type, think **narrowing**.

---

# 30. Shortcuts

> [!tip]
> **Shortcut: Widening**
>
> Think:
>
> ~~~text
> byte → short → int → long → float → double
> ~~~
>
> Smaller numeric type → larger numeric type.

> [!tip]
> **Shortcut: Decimal Division**
>
> Always remember:
>
> ~~~java
> (double) a / b
> ~~~
>
> not:
>
> ~~~java
> (double) (a / b)
> ~~~

> [!tip]
> **Shortcut: Character Digit**
>
> `'0'` to `'9'`:
>
> ~~~java
> int digit = ch - '0';
> ~~~
>
> Reverse:
>
> ~~~java
> char ch = (char) ('0' + digit);
> ~~~

> [!tip]
> **Shortcut: String Number**
>
> String → Number:
>
> ~~~java
> Integer.parseInt(s)
> ~~~
>
> Number → String:
>
> ~~~java
> String.valueOf(n)
> ~~~

---

# 31. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Casting After Integer Division

Wrong:

~~~java
double result = (double) (5 / 2);
~~~

Result:

$$
2.0
$$

Correct:

~~~java
double result = (double) 5 / 2;
~~~

Result:

$$
2.5
$$

---

### Mistake 2 — Thinking Casting Rounds Decimal Values

~~~java
int x = (int) 9.99;
~~~

Result:

$$
9
$$

Not:

$$
10
$$

---

### Mistake 3 — Ignoring Overflow

~~~java
int x = (int) 10000000000L;
~~~

The value is outside the `int` range.

The conversion can produce an unexpected result.

Always check the target type's range.

---

### Mistake 4 — Confusing Casting and Parsing

Wrong:

~~~java
int x = (int) "123";
~~~

Correct:

~~~java
int x = Integer.parseInt("123");
~~~

---

### Mistake 5 — Treating `'5'` as Integer `5`

~~~text
'5'