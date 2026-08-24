---
type: concept
subject: coding
topic: "Operators and Expressions"
parent: "Programming Fundamentals"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - operators
  - expressions
  - java
  - programming
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Variables and Data Types]]"
  - "[[Operators]]"
  - "[[Type Casting]]"
---

# Operators and Expressions

## 1. Core Concept

> [!summary]
> An **expression** is a combination of values, variables, operators, and method calls that produces a value.
>
> An **operator** tells Java what operation to perform.

Example:

~~~java
int result = a + b * 2;
~~~

Here:

- `a` and `b` → operands
- `+` and `*` → operators
- `a + b * 2` → expression
- `result` → stores the evaluated value

Basic idea:

$$
\text{Expression} \rightarrow \text{Produces a value}
$$

Example:

$$
10+5\times2=20
$$

---

# 2. Basic Meaning

## What is an Expression?

An expression is something Java can evaluate to produce a value.

Examples:

~~~java
10 + 20
~~~

produces:

$$
30
$$

~~~java
x * 5
~~~

produces a value based on `x`.

~~~java
a > b
~~~

produces:

~~~text
true
or
false
~~~

~~~java
x % 2 == 0
~~~

produces a boolean result.

---

# 3. Expression Components

An expression may contain:

- Literals
- Variables
- Operators
- Method calls
- Parentheses

Example:

~~~java
int result = (a + 10) * square(b);
~~~

Components:

~~~text
a
10
b
+
*
()
square()
~~~

All together form an expression.

---

# 4. Types of Expressions

Common expressions include:

| Type | Example | Result |
|---|---|---|
| Arithmetic | `a + b` | Number |
| Relational | `a > b` | Boolean |
| Logical | `a > 0 && b > 0` | Boolean |
| Assignment | `x = 10` | Assigned value |
| Conditional | `x > 0 ? 1 : -1` | Selected value |
| String | `"Hi " + name` | String |

---

# 5. Arithmetic Expressions

Arithmetic expressions perform mathematical operations.

Operators:

~~~text
+  -  *  /  %
~~~

Example:

~~~java
int result = 10 + 5 * 2;
~~~

Multiplication has higher precedence.

$$
5\times2=10
$$

Then:

$$
10+10=20
$$

### Answer

$$
\boxed{20}
$$

---

# 6. Relational Expressions

Relational expressions compare values.

Operators:

~~~text
==  !=  >  <  >=  <=
~~~

Example:

~~~java
int a = 10;
int b = 20;

boolean result = a < b;
~~~

Since:

$$
10<20
$$

Therefore:

$$
result=true
$$

### Answer

$$
\boxed{true}
$$

---

# 7. Logical Expressions

Logical expressions combine boolean conditions.

Operators:

~~~text
&&
||
!
~~~

Example:

~~~java
int age = 25;

boolean eligible =
    age >= 18 && age <= 60;
~~~

Both conditions are true.

Therefore:

$$
eligible=true
$$

---

# 8. Assignment Expressions

Assignment stores a value in a variable.

Example:

~~~java
int x = 10;
~~~

The expression:

~~~text
x = 10
~~~

assigns `10` to `x`.

Compound assignments:

~~~text
+=
-=
*=
/=
%=
~~~

Example:

~~~java
int x = 10;

x += 5;
~~~

Equivalent to:

~~~java
x = x + 5;
~~~

Therefore:

$$
x=15
$$

---

# 9. Unary Expressions

Unary operators work on one operand.

Common operators:

~~~text
++
--
!
+
-
~~~

Example:

~~~java
int x = 5;

int y = -x;
~~~

Therefore:

$$
y=-5
$$

Boolean example:

~~~java
boolean result = !true;
~~~

Therefore:

$$
result=false
$$

---

# 10. Conditional Expression

The ternary operator creates a conditional expression.

Syntax:

~~~java
condition ? valueIfTrue : valueIfFalse
~~~

Example:

~~~java
int n = 10;

String result =
    n % 2 == 0 ? "Even" : "Odd";
~~~

Since:

$$
10\%2=0
$$

Therefore:

$$
result=\text{"Even"}
$$

### Answer

$$
\boxed{Even}
$$

---

# 11. Operator Precedence

When multiple operators appear in an expression, Java follows precedence rules.

Important order:

| Priority | Operators | Meaning |
|---:|---|---|
| 1 | `()` | Parentheses |
| 2 | `++ --` | Increment/decrement |
| 3 | `+ - ! ~` | Unary |
| 4 | `* / %` | Multiplication/division/remainder |
| 5 | `+ -` | Addition/subtraction |
| 6 | `< > <= >=` | Relational |
| 7 | `== !=` | Equality |
| 8 | `&` | Bitwise AND |
| 9 | `^` | Bitwise XOR |
| 10 | `|` | Bitwise OR |
| 11 | `&&` | Logical AND |
| 12 | `||` | Logical OR |
| 13 | `?:` | Ternary |
| 14 | `= += -= *= /= %=` | Assignment |

> [!important]
> You do not need to memorize every Java precedence rule initially. Master parentheses, arithmetic, relational, logical, ternary, and assignment precedence first.

---

# 12. Parentheses

Parentheses have very high precedence and can explicitly control evaluation order.

Example:

~~~java
int result = (10 + 5) * 2;
~~~

First:

$$
10+5=15
$$

Then:

$$
15\times2=30
$$

### Answer

$$
\boxed{30}
$$

Without parentheses:

~~~java
int result = 10 + 5 * 2;
~~~

First:

$$
5\times2=10
$$

Then:

$$
10+10=20
$$

### Answer

$$
\boxed{20}
$$

---

# 13. Left-to-Right Evaluation

Operators with the same precedence are generally evaluated according to associativity.

For common arithmetic operators such as:

~~~text
+
-
*
/
%
~~~

evaluation is generally left-to-right.

Example:

~~~java
int result = 20 / 5 * 2;
~~~

First:

$$
20/5=4
$$

Then:

$$
4\times2=8
$$

### Answer

$$
\boxed{8}
$$

Not:

$$
20/(5\times2)=2
$$

---

# 14. Basic Examples

## Example 1 — Arithmetic Expression

### Question

Evaluate:

$$
10+5\times2
$$

### Pattern

Multiplication before addition.

### Calculation

$$
5\times2=10
$$

$$
10+10=20
$$

### Answer

$$
\boxed{20}
$$

---

## Example 2 — Parentheses

### Question

Evaluate:

$$
(10+5)\times2
$$

### Calculation

$$
10+5=15
$$

$$
15\times2=30
$$

### Answer

$$
\boxed{30}
$$

---

## Example 3 — Modulus Expression

### Question

Evaluate:

$$
27\%5
$$

### Calculation

$$
27=5\times5+2
$$

Therefore:

$$
27\%5=2
$$

### Answer

$$
\boxed{2}
$$

---

# 15. Mixed Expression

## Example 4

### Question

Evaluate:

~~~java
int result = 10 + 20 / 5 * 2;
~~~

### Pattern

`/` and `*` have higher precedence than `+`.

They have equal precedence, so evaluate left to right.

First:

$$
20/5=4
$$

Then:

$$
4\times2=8
$$

Finally:

$$
10+8=18
$$

### Answer

$$
\boxed{18}
$$

---

# 16. Relational + Logical Expression

## Example 5

### Question

Evaluate:

~~~java
int x = 15;

boolean result =
    x > 10 && x < 20;
~~~

### Calculation

First condition:

$$
15>10=true
$$

Second:

$$
15<20=true
$$

Therefore:

$$
true\land true=true
$$

### Answer

$$
\boxed{true}
$$

---

# 17. Complex Boolean Expression

## Example 6

### Question

Evaluate:

~~~java
int x = 5;
int y = 10;

boolean result =
    x < y && y > 5 || x == 0;
~~~

### Pattern

`&&` has higher precedence than `||`.

First:

$$
x<y
$$

$$
5<10=true
$$

Second:

$$
y>5
$$

$$
10>5=true
$$

Therefore:

$$
true\land true=true
$$

Then:

$$
true\lor false=true
$$

### Answer

$$
\boxed{true}
$$

---

# 18. Short-Circuit Evaluation

Java evaluates `&&` and `||` using short-circuit behavior.

## AND

If the first condition is false, the remaining condition may not be evaluated.

Example:

~~~java
int x = 0;

boolean result =
    x != 0 && 10 / x > 2;
~~~

First:

$$
x\neq0
$$

is false.

Therefore Java does not evaluate:

$$
10/x
$$

This avoids division by zero.

---

## OR

If the first condition is true, the remaining condition may not be evaluated.

Example:

~~~java
int x = 10;

boolean result =
    x == 10 || x / 0 > 2;
~~~

First condition is true.

Therefore the second condition is skipped.

> [!important]
> `&&` and `||` are short-circuit logical operators.

---

# 19. Increment Expressions

Consider:

~~~java
int x = 5;

int y = x++;
~~~

Post-increment:

1. Use `x`.
2. Increment `x`.

Therefore:

$$
y=5
$$

$$
x=6
$$

### Answer

$$
\boxed{x=6,\ y=5}
$$

---

# 20. Pre-Increment Expression

Consider:

~~~java
int x = 5;

int y = ++x;
~~~

Pre-increment:

1. Increment `x`.
2. Use the new value.

Therefore:

$$
x=6
$$

$$
y=6
$$

### Answer

$$
\boxed{x=6,\ y=6}
$$

---

# 21. Advanced Expression Example

## Example 7

### Question

Find the final values.

~~~java
int x = 5;

int result =
    x++ + ++x;
~~~

### Step-by-Step

Initially:

$$
x=5
$$

First:

~~~text
x++
~~~

Uses `5`, then:

$$
x=6
$$

Second:

~~~text
++x
~~~

First increments:

$$
x=7
$$

Then uses `7`.

Therefore:

$$
result=5+7=12
$$

Final:

$$
x=7
$$

### Answer

$$
\boxed{x=7,\ result=12}
$$

---

# 22. Type Conversion in Expressions

Different data types can appear in the same expression.

Example:

~~~java
int a = 10;
double b = 2.5;

double result = a + b;
~~~

Java promotes `a` to a compatible floating-point type for the operation.

Therefore:

$$
10+2.5=12.5
$$

### Answer

$$
\boxed{12.5}
$$

---

# 23. Integer Division Expression

## Example 8

### Question

Find the value of:

~~~java
int result = 5 / 2;
~~~

Both operands are integers.

Therefore integer division occurs:

$$
5/2=2
$$

### Answer

$$
\boxed{2}
$$

To obtain a decimal:

~~~java
double result = (double) 5 / 2;
~~~

Therefore:

$$
result=2.5
$$

---

# 24. String Concatenation Expressions

The `+` operator can also concatenate strings.

Example:

~~~java
String name = "Pradeep";

String result = "Hello " + name;
~~~

Result:

~~~text
Hello Pradeep
~~~

### Important Trap

~~~java
System.out.println("Result = " + 10 + 20);
~~~

Output:

~~~text
Result = 1020
~~~

Why?

Evaluation occurs from left to right:

~~~text
"Result = " + 10
→ "Result = 10"

"Result = 10" + 20
→ "Result = 1020"
~~~

Correct:

~~~java
System.out.println("Result = " + (10 + 20));
~~~

Output:

~~~text
Result = 30
~~~

> [!important]
> Parentheses force arithmetic to happen before string concatenation.

---

# 25. Assignment Expression Trap

Consider:

~~~java
int x = 10;

int y = (x = 20);
~~~

The assignment expression:

~~~text
x = 20
~~~

updates `x` and also produces the assigned value.

Therefore:

$$
x=20
$$

$$
y=20
$$

### Answer

$$
\boxed{x=20,\ y=20}
$$

> [!important]
> Assignment can itself participate in an expression in Java.

---

# 26. Chained Assignment

Example:

~~~java
int a, b, c;

a = b = c = 10;
~~~

Assignment is evaluated right-to-left.

First:

$$
c=10
$$

Then:

$$
b=10
$$

Then:

$$
a=10
$$

Final:

~~~text
a = 10
b = 10
c = 10
~~~

### Answer

$$
\boxed{a=b=c=10}
$$

---

# 27. Conditional Expression

## Example 9

### Question

Find the maximum of two numbers using an expression.

Given:

$$
a=10,\quad b=20
$$

### Pattern

Two choices → ternary.

~~~java
int max = a > b ? a : b;
~~~

Since:

$$
10>20=false
$$

The second value is selected:

$$
max=20
$$

### Answer

$$
\boxed{20}
$$

---

# 28. Nested Expressions

Expressions can contain other expressions.

Example:

~~~java
int result =
    (a + b) * (c - d);
~~~

This contains:

~~~text
(a + b)
(c - d)
multiplication
assignment
~~~

Solve from the inside outward:

$$
a+b
$$

then:

$$
c-d
$$

then multiply.

> [!tip]
> When an expression looks complicated, break it into smaller sub-expressions.

---

# 29. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Operator Precedence

If multiple operators appear:

~~~text
Check precedence first.
~~~

Priority to remember:

$$
()
\rightarrow
*,/,\%
\rightarrow
+,-
\rightarrow
comparison
\rightarrow
&&
\rightarrow
||
\rightarrow
?:
\rightarrow
assignment
$$

---

### Pattern 2 — Parentheses

If parentheses exist:

~~~text
Solve them first.
~~~

---

### Pattern 3 — Integer Division

If both operands are integers:

~~~text
int / int
→ integer result
~~~

---

### Pattern 4 — Modulus

If the question asks for:

~~~text
remainder
even/odd
last digit
cycle
~~~

Think:

~~~text
%
~~~

---

### Pattern 5 — Boolean Conditions

If the expression contains:

~~~text
both
all
and
~~~

Think:

~~~text
&&
~~~

If it contains:

~~~text
either
any
or
~~~

Think:

~~~text
||
~~~

---

### Pattern 6 — Increment

If you see:

~~~text
++x
x++
~~~

Track whether the value changes before or after it is used.

---

### Pattern 7 — String + Number

If a string appears with `+`:

~~~text
String concatenation
~~~

Check whether arithmetic needs parentheses.

---

### Pattern 8 — Assignment Inside Expression

If you see:

~~~java
x = y = 10;
~~~

Think:

~~~text
Right-to-left assignment.
~~~

---

# 30. Recognition Tricks

> [!important]
> If an expression has parentheses, solve the innermost parentheses first.

> [!important]
> If `*`, `/`, and `%` appear with `+` or `-`, perform multiplication/division/remainder first.

> [!important]
> If `&&` and `||` appear together, evaluate `&&` before `||`.

> [!important]
> If `++x` appears, change first.

> [!important]
> If `x++` appears, use first.

> [!important]
> If two integers are divided, check for integer division.

> [!important]
> If a string appears before `+`, check for string concatenation.

> [!important]
> If the expression is difficult to evaluate mentally, add parentheses or break it into smaller steps.

---

# 31. Shortcuts

> [!tip]
> **Shortcut: PEMDAS-style mental order**
>
> ```text
> Parentheses
> ↓
> Unary
> ↓
> *, /, %
> ↓
> +, -
> ↓
> Comparisons
> ↓
> &&
> ↓
> ||
> ↓
> Ternary
> ↓
> Assignment
> ```

> [!tip]
> **Shortcut: Boolean**
>
> `&&` → all must be true.
>
> `||` → at least one must be true.
>
> `!` → opposite.

> [!tip]
> **Shortcut: Pre/Post**
>
> Pre:
>
> ```text
> Change → Use
> ```
>
> Post:
>
> ```text
> Use → Change
> ```

> [!tip]
> **Shortcut: Decimal Result**
>
> If you need decimal division:
>
> ~~~java
> (double) a / b
> ~~~

> [!tip]
> **Shortcut: String Concatenation**
>
> Use parentheses when arithmetic should happen first:
>
> ~~~java
> "Sum = " + (a + b)
> ~~~

---

# 32. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Evaluating Strictly Left to Right

Wrong:

~~~text
10 + 5 × 2
→ 15 × 2
→ 30
~~~

Correct:

$$
5\times2=10
$$

$$
10+10=20
$$

---

### Mistake 2 — Ignoring Parentheses

~~~java
(10 + 5) * 2
~~~

is different from:

~~~java
10 + 5 * 2
~~~

Results:

$$
30\neq20
$$

---

### Mistake 3 — Forgetting Integer Division

~~~java
5 / 2
~~~

produces:

$$
2
$$

not:

$$
2.5
$$

---

### Mistake 4 — Confusing `&&` and `||`

Remember:

~~~text
&& → all
|| → either/at least one
~~~

---

### Mistake 5 — Confusing `++x` and `x++`

~~~text
++x → change first
x++ → use first
~~~

---

### Mistake 6 — Forgetting String Concatenation

~~~java
System.out.println("Sum = " + 10 + 20);
~~~

produces:

~~~text
Sum = 1020
~~~

Correct:

~~~java
System.out.println("Sum = " + (10 + 20));
~~~

produces:

~~~text
Sum = 30
~~~

---

### Mistake 7 — Casting After Division

Wrong:

~~~java
(double) (5 / 2)
~~~

Result:

$$
2.0
$$

Correct:

~~~java
(double) 5 / 2
~~~

Result:

$$
2.5
$$

---

# 33. Formula Sheet

### Arithmetic

$$
a+b
$$

$$
a-b
$$

$$
a\times b
$$

$$
a/b
$$

$$
a\%b
$$

### Even

$$
n\%2=0
$$

### Odd

$$
n\%2\neq0
$$

### Range

$$
low\leq x\leq high
$$

### Logical AND

$$
A\land B
$$

Java:

~~~java
A && B
~~~

### Logical OR

$$
A\lor B
$$

Java:

~~~java
A || B
~~~

### Logical NOT

$$
\neg A
$$

Java:

~~~java
!A
~~~

### Ternary

~~~java
condition ? trueValue : falseValue
~~~

### Decimal Division

~~~java
(double) a / b
~~~

### Pre-Increment

~~~java
++x
~~~

### Post-Increment

~~~java
x++
~~~

---

# 34. Quick Revision

> [!summary] One-Minute Revision

~~~text
Expression
→ Produces a value.

Operator
→ Performs an operation.

Arithmetic
→ + - * / %

Relational
→ == != > < >= <=

Logical
→ && || !

Assignment
→ = += -= *= /= %=

Unary
→ ++ -- ! + -

Ternary
→ condition ? A : B

Parentheses
→ Highest practical priority.

*, /, %
→ Before + and -.

Comparison
→ Produces boolean.

&&
→ Evaluated before ||.

int / int
→ Integer division.

(double) a / b
→ Decimal division.

++x
→ Change first, use later.

x++
→ Use first, change later.

String + value
→ String concatenation.

String + (a + b)
→ Arithmetic first.

Assignment
→ Generally right-to-left.

When confused
→ Add parentheses and solve step-by-step.
~~~

## Golden Memory Trick

**An expression produces a value; evaluate it by following parentheses, precedence, associativity, data types, and operator behavior.**

## One-Line Recognition

**When a coding question asks for the result of a complex expression, identify the operators first, apply precedence and type rules, then evaluate step-by-step.**