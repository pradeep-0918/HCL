---
type: concept
subject: coding
topic: "Operators"
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
  - java
  - programming
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Variables and Data Types]]"
  - "[[Conditional Statements]]"
  - "[[Operators and Expressions]]"
---

# Operators

## 1. Core Concept

> [!summary]
> An **operator** is a symbol that performs an operation on one or more values or variables.

Example:

~~~java
int a = 10;
int b = 5;

int sum = a + b;
~~~

Here:

- `a` and `b` → operands
- `+` → operator
- `a + b` → expression
- `sum` → result

Basic idea:

$$
\text{Operand} + \text{Operator} + \text{Operand}
$$

Example:

$$
10+5=15
$$

---

# 2. Basic Meaning

Operators are used to perform operations such as:

- Addition
- Subtraction
- Multiplication
- Division
- Remainder
- Comparison
- Logical checking
- Assignment
- Increment/decrement
- Bit manipulation

Java operators can be grouped into several categories.

| Category | Operators |
|---|---|
| Arithmetic | `+ - * / %` |
| Relational | `== != > < >= <=` |
| Logical | `&& || !` |
| Assignment | `= += -= *= /= %=` |
| Unary | `+ - ++ -- !` |
| Ternary | `condition ? x : y` |
| Bitwise | `& | ^ ~` |
| Shift | `<< >> >>>` |

---

# 3. Arithmetic Operators

Arithmetic operators perform mathematical calculations.

| Operator | Meaning | Example |
|---|---|---|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` |
| `%` | Remainder | `a % b` |

Example:

~~~java
int a = 10;
int b = 3;

System.out.println(a + b);
System.out.println(a - b);
System.out.println(a * b);
System.out.println(a / b);
System.out.println(a % b);
~~~

Output:

~~~text
13
7
30
3
1
~~~

Because:

$$
10+3=13
$$

$$
10-3=7
$$

$$
10\times3=30
$$

$$
10/3=3
$$

$$
10\%3=1
$$

> [!important]
> `%` gives the **remainder**, not the quotient.

---

# 4. Modulus Operator `%`

The modulus operator returns the remainder after division.

Examples:

$$
10\%3=1
$$

$$
20\%5=0
$$

$$
17\%4=1
$$

### Important Uses

The modulus operator is heavily used in coding problems.

#### Check Even

~~~java
if (n % 2 == 0) {
    System.out.println("Even");
}
~~~

#### Check Odd

~~~java
if (n % 2 != 0) {
    System.out.println("Odd");
}
~~~

#### Extract Last Digit

For a positive integer:

$$
n\%10
$$

gives the last digit.

Example:

$$
1234\%10=4
$$

> [!tip]
> Whenever you see **even/odd**, **last digit**, **cyclic pattern**, or **divisibility**, immediately consider `%`.

---

# 5. Relational Operators

Relational operators compare two values.

| Operator | Meaning |
|---|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

Example:

~~~java
int a = 10;
int b = 20;

System.out.println(a < b);
System.out.println(a > b);
System.out.println(a == b);
~~~

Output:

~~~text
true
false
false
~~~

Relational operators produce a boolean result.

$$
\text{Comparison} \rightarrow true/false
$$

---

# 6. Logical Operators

Logical operators combine or modify conditions.

| Operator | Meaning |
|---|---|
| `&&` | AND |
| `||` | OR |
| `!` | NOT |

## AND `&&`

Both conditions must be true.

$$
A\land B
$$

Example:

~~~java
int age = 25;

boolean result = age >= 18 && age <= 60;
~~~

Both conditions are true.

Therefore:

~~~text
result = true
~~~

### Truth Table

| A | B | `A && B` |
|---|---|---|
| true | true | true |
| true | false | false |
| false | true | false |
| false | false | false |

> [!important]
> `&&` means **all conditions must be true**.

---

# 7. OR `||`

At least one condition must be true.

Example:

~~~java
int day = 6;

boolean weekend =
    day == 6 || day == 7;
~~~

Since `day == 6` is true:

$$
weekend=true
$$

### Truth Table

| A | B | `A || B` |
|---|---|---|
| true | true | true |
| true | false | true |
| false | true | true |
| false | false | false |

> [!important]
> `||` means **at least one condition must be true**.

---

# 8. NOT `!`

`!` reverses a boolean value.

~~~java
boolean passed = true;

System.out.println(!passed);
~~~

Output:

~~~text
false
~~~

Therefore:

$$
!true=false
$$

$$
!false=true
$$

> [!tip]
> Think of `!` as **opposite of**.

---

# 9. Assignment Operators

Assignment operators store or update values.

| Operator | Meaning | Equivalent |
|---|---|---|
| `=` | Assign | `a = b` |
| `+=` | Add and assign | `a = a + b` |
| `-=` | Subtract and assign | `a = a - b` |
| `*=` | Multiply and assign | `a = a * b` |
| `/=` | Divide and assign | `a = a / b` |
| `%=` | Modulus and assign | `a = a % b` |

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

# 10. Basic Assignment Example

## Example 1 — Compound Assignment

### Question

Find the final value of `x`.

~~~java
int x = 10;

x += 5;
x *= 2;
~~~

### Pattern

Apply operations sequentially.

### Calculation

Initially:

$$
x=10
$$

After:

~~~java
x += 5;
~~~

$$
x=10+5=15
$$

After:

~~~java
x *= 2;
~~~

$$
x=15\times2=30
$$

### Answer

$$
\boxed{30}
$$

---

# 11. Unary Operators

Unary operators operate on one operand.

Common unary operators:

~~~text
+
-
++
--
!
~~~

Examples:

~~~java
int x = 5;

+x;
-x;
++x;
--x;
!true;
~~~

---

# 12. Increment Operator `++`

`++` increases a value by `1`.

~~~java
int x = 5;
x++;
~~~

Result:

$$
x=6
$$

Equivalent:

~~~java
x = x + 1;
~~~

There are two forms:

- Pre-increment: `++x`
- Post-increment: `x++`

---

# 13. Pre-Increment

Pre-increment first increases the value, then uses it.

Example:

~~~java
int x = 5;
int y = ++x;
~~~

Step 1:

$$
x=6
$$

Step 2:

$$
y=6
$$

Final:

~~~text
x = 6
y = 6
~~~

### Answer

$$
\boxed{x=6,\ y=6}
$$

> [!important]
> `++x` → **increment first, use later**.

---

# 14. Post-Increment

Post-increment first uses the current value, then increases it.

Example:

~~~java
int x = 5;
int y = x++;
~~~

Step 1:

$$
y=5
$$

Step 2:

$$
x=6
$$

Final:

~~~text
x = 6
y = 5
~~~

### Answer

$$
\boxed{x=6,\ y=5}
$$

> [!important]
> `x++` → **use first, increment later**.

---

# 15. Pre-Decrement

Pre-decrement decreases the value before using it.

~~~java
int x = 5;
int y = --x;
~~~

Therefore:

$$
x=4
$$

$$
y=4
$$

### Answer

$$
\boxed{x=4,\ y=4}
$$

---

# 16. Post-Decrement

Post-decrement uses the current value first and then decreases it.

~~~java
int x = 5;
int y = x--;
~~~

Therefore:

$$
y=5
$$

$$
x=4
$$

### Answer

$$
\boxed{x=4,\ y=5}
$$

---

# 17. Increment/Decrement Recognition Trick

> [!important]
> If you see `++x`:
>
> **Change first → use later**

> [!important]
> If you see `x++`:
>
> **Use first → change later**

> [!important]
> If you see `--x`:
>
> **Decrease first → use later**

> [!important]
> If you see `x--`:
>
> **Use first → decrease later**

---

# 18. Advanced Increment Example

## Example 2 — Pre and Post Increment

### Question

Find the output.

~~~java
int x = 5;

int result = x++ + ++x;
~~~

### Pattern

Track the value after every operation.

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

### Answer

$$
\boxed{12}
$$

Final:

$$
x=7
$$

---

# 19. Ternary Operator

The ternary operator is a short form of `if-else`.

Syntax:

~~~java
condition ? valueIfTrue : valueIfFalse;
~~~

Example:

~~~java
int age = 20;

String result =
    age >= 18 ? "Adult" : "Minor";
~~~

Since:

$$
20\geq18
$$

Result:

~~~text
Adult
~~~

### Equivalent `if-else`

~~~java
String result;

if (age >= 18) {
    result = "Adult";
} else {
    result = "Minor";
}
~~~

> [!tip]
> If a problem asks for a simple two-choice result, the ternary operator can make the code shorter.

---

# 20. Example — Even or Odd Using Ternary

## Example 3

### Question

Print whether `n` is even or odd.

### Pattern

Even → remainder `0`.

~~~java
int n = 17;

String result =
    n % 2 == 0 ? "Even" : "Odd";

System.out.println(result);
~~~

Calculation:

$$
17\%2=1
$$

Therefore:

$$
\boxed{Odd}
$$

---

# 21. Operator Precedence

When an expression contains multiple operators, Java follows precedence rules.

Important order:

| Priority | Operators |
|---:|---|
| 1 | `()` |
| 2 | `++`, `--`, unary |
| 3 | `*`, `/`, `%` |
| 4 | `+`, `-` |
| 5 | `<`, `>`, `<=`, `>=` |
| 6 | `==`, `!=` |
| 7 | `&&` |
| 8 | `||` |
| 9 | `?:` |
| 10 | Assignment operators |

Example:

~~~java
int result = 10 + 5 * 2;
~~~

Multiplication happens first:

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

# 22. Parentheses Override Precedence

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

> [!tip]
> When in doubt, use parentheses. They make the intended order explicit.

---

# 23. Example — Operator Precedence

## Example 4

### Question

Find the output.

~~~java
int x = 20 - 6 / 2;
~~~

### Pattern

Division has higher precedence than subtraction.

First:

$$
6/2=3
$$

Then:

$$
20-3=17
$$

### Answer

$$
\boxed{17}
$$

---

# 24. Example — Modulus Pattern

## Example 5

### Question

Find the last digit of `7834`.

### Pattern

Last digit → `% 10`.

### Calculation

$$
7834\%10=4
$$

### Answer

$$
\boxed{4}
$$

---

# 25. Example — Multiple Conditions

## Example 6

### Question

A person is eligible if age is between `18` and `60`, inclusive.

Given:

$$
age=25
$$

### Pattern

Range condition → use `&&`.

### Code

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

### Answer

$$
\boxed{true}
$$

---

# 26. Example — OR Condition

## Example 7

### Question

A number is accepted if it is either `10` or `20`.

Given:

$$
n=20
$$

### Pattern

Either condition → `||`.

### Code

~~~java
int n = 20;

boolean accepted =
    n == 10 || n == 20;
~~~

Since:

$$
n=20
$$

the second condition is true.

### Answer

$$
\boxed{true}
$$

---

# 27. Short-Circuit Evaluation

Java's logical operators `&&` and `||` use short-circuit evaluation.

## `&&`

If the first condition is false, Java may not evaluate the second condition.

Example:

~~~java
int x = 0;

boolean result =
    x != 0 && 10 / x > 2;
~~~

First condition:

$$
x\neq0
$$

is false.

Therefore Java does not need to evaluate:

$$
10/x
$$

This avoids division by zero.

---

## `||`

If the first condition is true, Java may not evaluate the second condition.

Example:

~~~java
int x = 10;

boolean result =
    x == 10 || x / 0 > 2;
~~~

The first condition is true, so the second condition is not evaluated.

> [!important]
> `&&` and `||` are **short-circuit logical operators**.

---

# 28. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Even/Odd

If the question says:

~~~text
Check whether a number is even or odd.
~~~

Think:

$$
n\%2
$$

Even:

$$
n\%2=0
$$

Odd:

$$
n\%2\neq0
$$

---

### Pattern 2 — Last Digit

If the question says:

~~~text
Find the last digit.
~~~

Think:

$$
n\%10
$$

---

### Pattern 3 — Multiple Conditions

If the question says:

~~~text
between A and B
~~~

Think:

$$
x\geq A\ \&\&\ x\leq B
$$

---

### Pattern 4 — Either/Or

If the question says:

~~~text
either condition A or condition B
~~~

Think:

$$
A\ ||\ B
$$

---

### Pattern 5 — Not Condition

If the question says:

~~~text
not equal
opposite
reverse condition
~~~

Think:

~~~text
!
!=
~~~

depending on whether the operation is boolean negation or comparison.

---

### Pattern 6 — Increase by One

If you see:

~~~text
increment
~~~

Think:

~~~text
++
~~~

---

### Pattern 7 — Decrease by One

If you see:

~~~text
decrement
~~~

Think:

~~~text
--
~~~

---

### Pattern 8 — Short Two-Choice Decision

If the question asks for:

~~~text
condition ? result A : result B
~~~

Think:

~~~text
ternary operator
~~~

---

# 29. Recognition Tricks

> [!important]
> If the question says **remainder**, think `%`.

> [!important]
> If the question says **even/odd**, think `% 2`.

> [!important]
> If the question says **last digit**, think `% 10`.

> [!important]
> If the question says **both conditions**, think `&&`.

> [!important]
> If the question says **either condition**, think `||`.

> [!important]
> If the question says **opposite of a boolean condition**, think `!`.

> [!important]
> If the question says **increase by 1**, think `++`.

> [!important]
> If the question says **decrease by 1**, think `--`.

> [!important]
> If you see `++x`, remember **change first**.

> [!important]
> If you see `x++`, remember **use first**.

> [!important]
> If you see a simple `if-else` assignment, consider `?:`.

---

# 30. Shortcuts

> [!tip]
> **Shortcut: `% 2`**
>
> Use `% 2` for even/odd questions.
>
> `n % 2 == 0` → even  
> `n % 2 != 0` → odd

> [!tip]
> **Shortcut: `% 10`**
>
> Use `% 10` to extract the last digit of a positive integer.

> [!tip]
> **Shortcut: Range**
>
> For an inclusive range:
>
> ~~~java
> x >= low && x <= high
> ~~~

> [!tip]
> **Shortcut: Pre vs Post**
>
> Pre → change first.
>
> Post → use first.

> [!tip]
> **Shortcut: PEMDAS-style priority**
>
> Parentheses → Multiplication/Division/Modulus → Addition/Subtraction → Comparison → Logical operations → Assignment.

---

# 31. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing `=` and `==`

Wrong comparison:

~~~java
if (x = 10)
~~~

Correct:

~~~java
if (x == 10)
~~~

Remember:

$$
= \rightarrow \text{assignment}
$$

$$
== \rightarrow \text{comparison}
$$

---

### Mistake 2 — Confusing `%` with Percentage

In Java:

~~~java
10 % 3
~~~

means remainder.

It does not mean percentage.

Result:

$$
1
$$

---

### Mistake 3 — Forgetting Integer Division

~~~java
int x = 5 / 2;
~~~

Result:

$$
2
$$

Not:

$$
2.5
$$

---

### Mistake 4 — Confusing `&&` and `||`

`&&`:

$$
\text{Both must be true}
$$

`||`:

$$
\text{At least one must be true}
$$

---

### Mistake 5 — Confusing Pre-Increment and Post-Increment

~~~java
++x
~~~

means:

$$
\text{Increment first}
$$

~~~java
x++
~~~

means:

$$
\text{Use first}
$$

---

### Mistake 6 — Ignoring Operator Precedence

Example:

~~~java
int x = 10 + 5 * 2;
~~~

Do not calculate from left to right.

Correct:

$$
5\times2=10
$$

$$
10+10=20
$$

---

### Mistake 7 — Forgetting Parentheses

Instead of relying on complicated precedence:

~~~java
int result = a + b * c;
~~~

Use parentheses when the intended calculation requires it:

~~~java
int result = (a + b) * c;
~~~

---

# 32. Formula Sheet

### Addition

$$
a+b
$$

### Subtraction

$$
a-b
$$

### Multiplication

$$
a\times b
$$

### Division

$$
a/b
$$

### Remainder

$$
a\%b
$$

### Even Number

$$
n\%2=0
$$

### Odd Number

$$
n\%2\neq0
$$

### Last Digit

$$
n\%10
$$

### Inclusive Range

$$
low\leq x\leq high
$$

Java:

~~~java
x >= low && x <= high
~~~

### Increment

$$
x++ \Rightarrow x=x+1
$$

### Decrement

$$
x-- \Rightarrow x=x-1
$$

### Ternary

~~~java
condition ? valueIfTrue : valueIfFalse
~~~

---

# 33. Quick Revision

> [!summary] One-Minute Revision

~~~text
Arithmetic
→ + - * / %

Relational
→ == != > < >= <=

Logical
→ && || !

Assignment
→ = += -= *= /= %=

Unary
→ ++ -- + - !

Ternary
→ condition ? A : B

% 
→ remainder

% 2
→ even / odd

% 10
→ last digit

&&
→ all conditions must be true

||
→ at least one condition must be true

!
→ reverses boolean value

++x
→ increment first, then use

x++
→ use first, then increment

--x
→ decrement first, then use

x--
→ use first, then decrement

Parentheses
→ highest priority

*
/
%
→ before + and -

=
→ assignment

==
→ comparison
~~~

## Golden Memory Trick

**Use `%` for remainder, `&&` for all, `||` for either, `!` for opposite, and remember pre changes before use while post changes after use.**

## One-Line Recognition

**When a coding question asks you to calculate, compare, combine conditions, update a value, or extract a pattern such as even/odd or last digit, identify the matching operator first.**