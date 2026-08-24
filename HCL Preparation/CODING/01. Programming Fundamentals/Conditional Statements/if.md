---
type: concept
subject: coding
topic: "if"
parent: "Conditional Statements"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - conditional-statements
  - if
  - java
  - programming
wikilinks:
  - "[[Conditional Statements]]"
  - "[[if else]]"
  - "[[Nested if]]"
  - "[[Switch]]"
---

# if

## 1. Core Concept

> [!summary]
> The `if` statement is used to execute a block of code **only when a condition is true**.

Basic structure:

~~~java
if (condition) {
    // code
}
~~~

Flow:

~~~text
Condition
   ↓
 true ──→ Execute block
   ↓
 false ─→ Skip block
~~~

Example:

~~~java
int age = 20;

if (age >= 18) {
    System.out.println("Eligible");
}
~~~

Since:

$$
20\geq18
$$

the condition is true.

Output:

~~~text
Eligible
~~~

---

# 2. Basic Meaning

An `if` statement allows a program to make a decision.

Think:

~~~text
IF condition is true
→ perform an action
~~~

Example:

~~~java
if (marks >= 40) {
    System.out.println("Pass");
}
~~~

The statement executes only when:

$$
marks\geq40
$$

If the condition is false, the block is skipped.

---

# 3. Syntax

The basic Java syntax is:

~~~java
if (condition) {
    statement1;
    statement2;
}
~~~

Example:

~~~java
int n = 10;

if (n > 0) {
    System.out.println("Positive");
}
~~~

Important parts:

| Part | Meaning |
|---|---|
| `if` | Conditional keyword |
| `(condition)` | Expression that evaluates to `true` or `false` |
| `{ }` | Block of statements |
| Statements | Code executed when condition is true |

> [!important]
> In Java, the condition inside `if` must evaluate to a `boolean` value.

---

# 4. Boolean Condition

A condition commonly uses relational operators.

Operators:

~~~text
>    Greater than
<    Less than
>=   Greater than or equal
<=   Less than or equal
==   Equal to
!=   Not equal to
~~~

Example:

~~~java
int x = 10;

if (x > 5) {
    System.out.println("Yes");
}
~~~

The expression:

$$
10>5
$$

is `true`.

Therefore the block executes.

---

# 5. Basic Examples

## Example 1 — Check Positive Number

### Question

Print `"Positive"` if a number is greater than zero.

### Pattern

Positive number:

$$
n>0
$$

### Code

~~~java
int n = 10;

if (n > 0) {
    System.out.println("Positive");
}
~~~

Since:

$$
10>0
$$

the condition is true.

### Answer

~~~text
Positive
~~~

---

## Example 2 — Check Even Number

### Question

Print `"Even"` if a number is even.

### Pattern

Even number:

$$
n\%2=0
$$

### Code

~~~java
int n = 24;

if (n % 2 == 0) {
    System.out.println("Even");
}
~~~

Calculation:

$$
24\%2=0
$$

Therefore:

~~~text
Even
~~~

### Answer

$$
\boxed{Even}
$$

---

## Example 3 — Check Passing Marks

### Question

Print `"Pass"` if marks are at least `40`.

### Pattern

At least `40` means:

$$
marks\geq40
$$

### Code

~~~java
int marks = 75;

if (marks >= 40) {
    System.out.println("Pass");
}
~~~

Since:

$$
75\geq40
$$

the condition is true.

### Answer

$$
\boxed{Pass}
$$

---

# 6. Multiple Statements Inside if

An `if` block can contain multiple statements.

Example:

~~~java
int n = 10;

if (n > 0) {
    System.out.println("Positive");
    System.out.println("Valid number");
}
~~~

Both statements execute because the condition is true.

Output:

~~~text
Positive
Valid number
~~~

> [!important]
> Use `{}` when the `if` block contains multiple statements.

---

# 7. if Without Braces

Java allows a single statement without braces.

Example:

~~~java
if (x > 0)
    System.out.println("Positive");
~~~

This is valid.

However, for placement coding and professional code, braces are generally recommended:

~~~java
if (x > 0) {
    System.out.println("Positive");
}
~~~

> [!warning]
> Indentation does not determine the block in Java. Braces determine the block.

---

# 8. Common Trap — Missing Braces

Consider:

~~~java
if (x > 0)
    System.out.println("Positive");
    System.out.println("Valid");
~~~

Only the first `println` belongs to the `if`.

The second statement executes regardless of the condition.

Correct:

~~~java
if (x > 0) {
    System.out.println("Positive");
    System.out.println("Valid");
}
~~~

> [!important]
> Without braces, only the immediately following statement belongs to the `if`.

---

# 9. Logical Conditions

Multiple conditions can be combined using logical operators.

### AND

~~~java
if (age >= 18 && age <= 60) {
    System.out.println("Eligible");
}
~~~

Both conditions must be true.

$$
age\geq18\land age\leq60
$$

---

### OR

~~~java
if (day == 6 || day == 7) {
    System.out.println("Weekend");
}
~~~

At least one condition must be true.

$$
day=6\lor day=7
$$

---

### NOT

~~~java
if (!isValid) {
    System.out.println("Invalid");
}
~~~

`!` reverses a boolean value.

---

# 10. Example — Range Checking

## Example 4

### Question

Check whether a number lies between `10` and `50`, inclusive.

### Pattern

Between means:

$$
10\leq n\leq50
$$

### Code

~~~java
int n = 35;

if (n >= 10 && n <= 50) {
    System.out.println("In range");
}
~~~

Check:

$$
35\geq10=true
$$

$$
35\leq50=true
$$

Therefore:

$$
true\land true=true
$$

### Answer

$$
\boxed{In\ range}
$$

---

# 11. Example — Multiple Conditions

## Example 5

### Question

Print `"Eligible"` if:

- Age is at least `18`
- Marks are at least `60`

### Pattern

Both conditions are required.

Use:

~~~text
&&
~~~

### Code

~~~java
int age = 20;
int marks = 75;

if (age >= 18 && marks >= 60) {
    System.out.println("Eligible");
}
~~~

Both conditions are true.

### Answer

$$
\boxed{Eligible}
$$

---

# 12. Nested Conditions

An `if` can contain another `if`.

Example:

~~~java
if (age >= 18) {

    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

Flow:

~~~text
age >= 18?
   ↓
  Yes
   ↓
hasId?
   ↓
  Yes
   ↓
Allowed
~~~

This is called **nested if**.

> [!important]
> Nested `if` is useful when the second condition should be checked only after the first condition succeeds.

---

# 13. Nested if vs Logical AND

These can sometimes produce the same result.

### Nested if

~~~java
if (age >= 18) {
    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

### Logical AND

~~~java
if (age >= 18 && hasId) {
    System.out.println("Allowed");
}
~~~

Both require:

$$
age\geq18
$$

and:

$$
hasId=true
$$

> [!tip]
> If conditions are simple and independent, `&&` can often make the logic shorter. Use nested `if` when the second decision naturally depends on the first.

---

# 14. Advanced Examples

## Example 6 — Largest of Two Numbers

### Question

Print the larger of two numbers.

Given:

$$
a=25,\quad b=40
$$

### Pattern

Compare:

$$
a>b
$$

### Code

~~~java
int a = 25;
int b = 40;

if (a > b) {
    System.out.println(a);
}

if (b > a) {
    System.out.println(b);
}
~~~

Since:

$$
40>25
$$

the output is:

~~~text
40
~~~

### Answer

$$
\boxed{40}
$$

> [!warning]
> For exactly one of two alternatives, `if-else` is usually cleaner than two independent `if` statements.

---

# 15. Example — Divisible by 5 and 3

## Example 7

### Question

Check whether a number is divisible by both `3` and `5`.

### Pattern

Divisible by `3`:

$$
n\%3=0
$$

Divisible by `5`:

$$
n\%5=0
$$

Both are required:

$$
(n\%3=0)\land(n\%5=0)
$$

### Code

~~~java
int n = 30;

if (n % 3 == 0 && n % 5 == 0) {
    System.out.println("Divisible by both");
}
~~~

Calculation:

$$
30\%3=0
$$

$$
30\%5=0
$$

### Answer

$$
\boxed{Divisible\ by\ both}
$$

---

# 16. Example — Positive and Even

## Example 8

### Question

Print `"Positive Even"` if a number is both positive and even.

### Pattern

Positive:

$$
n>0
$$

Even:

$$
n\%2=0
$$

### Code

~~~java
int n = 24;

if (n > 0 && n % 2 == 0) {
    System.out.println("Positive Even");
}
~~~

Both conditions are true.

### Answer

$$
\boxed{Positive\ Even}
$$

---

# 17. Example — Check Character

## Example 9

### Question

Check whether a character is an uppercase English letter.

### Pattern

Uppercase range:

$$
'A'\leq ch\leq'Z'
$$

### Code

~~~java
char ch = 'G';

if (ch >= 'A' && ch <= 'Z') {
    System.out.println("Uppercase");
}
~~~

Since:

~~~text
'G' lies between 'A' and 'Z'
~~~

### Answer

$$
\boxed{Uppercase}
$$

---

# 18. Example — Leap Year Condition

## Example 10

### Question

Check whether a year is a leap year.

A year is a leap year if:

- divisible by `400`, OR
- divisible by `4` but not by `100`

### Formula

$$
(year\%400=0)
$$

OR:

$$
(year\%4=0)\land(year\%100\neq0)
$$

### Code

~~~java
int year = 2024;

if (year % 400 == 0 ||
    (year % 4 == 0 && year % 100 != 0)) {

    System.out.println("Leap Year");
}
~~~

For `2024`:

$$
2024\%4=0
$$

and:

$$
2024\%100\neq0
$$

Therefore:

~~~text
Leap Year
~~~

### Answer

$$
\boxed{Leap\ Year}
$$

---

# 19. Shortcuts

> [!tip]
> **Shortcut: Positive**
>
> If the question says positive:
>
> $$n>0$$

> [!tip]
> **Shortcut: Negative**
>
> If the question says negative:
>
> $$n<0$$

> [!tip]
> **Shortcut: Non-negative**
>
> If the question says non-negative:
>
> $$n\geq0$$

> [!tip]
> **Shortcut: At least**
>
> "At least `x`":
>
> $$n\geq x$$

> [!tip]
> **Shortcut: At most**
>
> "At most `x`":
>
> $$n\leq x$$

> [!tip]
> **Shortcut: Between**
>
> "Between `a` and `b`, inclusive":
>
> $$a\leq n\leq b$$
>
> Java:
>
> ~~~java
> n >= a && n <= b
> ~~~

> [!tip]
> **Shortcut: Both**
>
> "Both conditions":
>
> ```text
> &&
> ```

> [!tip]
> **Shortcut: Either**
>
> "Either condition":
>
> ```text
> ||
> ```

---

# 20. Recognition Tricks

> [!important]
> If the question says **"if the number is..."**, immediately think `if`.

> [!important]
> If the question contains **"only when"**, think conditional execution.

> [!important]
> If the question says **"both conditions must be true"**, think `&&`.

> [!important]
> If the question says **"either condition can be true"**, think `||`.

> [!important]
> If the question says **"between A and B"**, think:
>
> $$A\leq x\leq B$$

> [!important]
> If the question says **"at least"**, think `>=`.

> [!important]
> If the question says **"at most"**, think `<=`.

> [!important]
> If the second condition should be checked only after the first condition succeeds, think **nested if**.

---

# 21. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Positive/Negative

~~~java
if (n > 0) {
}
~~~

---

### Pattern 2 — Even/Odd

~~~java
if (n % 2 == 0) {
}
~~~

---

### Pattern 3 — Range

~~~java
if (n >= low && n <= high) {
}
~~~

---

### Pattern 4 — Divisibility

~~~java
if (n % k == 0) {
}
~~~

---

### Pattern 5 — Multiple Requirements

~~~java
if (condition1 && condition2) {
}
~~~

---

### Pattern 6 — Alternative Conditions

~~~java
if (condition1 || condition2) {
}
~~~

---

### Pattern 7 — Character Range

~~~java
if (ch >= 'A' && ch <= 'Z') {
}
~~~

---

### Pattern 8 — Nested Decision

~~~java
if (condition1) {

    if (condition2) {
    }
}
~~~

---

# 22. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Using `=` Instead of `==`

Wrong:

~~~java
if (x = 10) {
}
~~~

Correct:

~~~java
if (x == 10) {
}
~~~

`=` is assignment.

`==` is comparison.

---

### Mistake 2 — Using `&&` When `||` Is Required

Question:

~~~text
Number is divisible by 3 or 5
~~~

Correct:

~~~java
if (n % 3 == 0 || n % 5 == 0) {
}
~~~

Using `&&` would incorrectly require both conditions.

---

### Mistake 3 — Incorrect Range Logic

Wrong:

~~~java
if (n >= 10 || n <= 50) {
}
~~~

This is true for almost every number.

Correct:

~~~java
if (n >= 10 && n <= 50) {
}
~~~

---

### Mistake 4 — Forgetting Braces

Wrong:

~~~java
if (x > 0)
    System.out.println("Positive");
    System.out.println("Valid");
~~~

Only the first statement belongs to the `if`.

---

### Mistake 5 — Confusing `!`

If:

~~~java
boolean valid = true;
~~~

Then:

~~~java
!valid
~~~

is:

$$
false
$$

---

### Mistake 6 — Incorrect Character Comparison

For uppercase English letters:

Correct:

~~~java
if (ch >= 'A' && ch <= 'Z') {
}
~~~

Do not compare unrelated character values without understanding their character codes.

---

# 23. Formula Sheet

### Positive

$$
n>0
$$

### Negative

$$
n<0
$$

### Zero

$$
n=0
$$

### Even

$$
n\%2=0
$$

### Odd

$$
n\%2\neq0
$$

### Divisible by K

$$
n\%k=0
$$

### Range

$$
a\leq n\leq b
$$

### AND

$$
A\land B
$$

Java:

~~~java
A && B
~~~

### OR

$$
A\lor B
$$

Java:

~~~java
A || B
~~~

### NOT

$$
\neg A
$$

Java:

~~~java
!A
~~~

### Uppercase English Letter

$$
'A'\leq ch\leq'Z'
$$

### Lowercase English Letter

$$
'a'\leq ch\leq'z'
$$

---

# 24. Quick Revision

> [!summary] One-Minute Revision

~~~text
if
→ Execute code only when condition is true.

Syntax
→ if (condition) { }

Condition
→ Must evaluate to boolean.

>
→ Greater than.

<
→ Less than.

>=
→ Greater than or equal.

<=
→ Less than or equal.

==
→ Equal comparison.

!=
→ Not equal.

&&
→ Both conditions must be true.

||
→ At least one condition must be true.

!
→ Reverses boolean value.

Positive
→ n > 0.

Negative
→ n < 0.

Even
→ n % 2 == 0.

Divisible by k
→ n % k == 0.

Range
→ low <= n && n <= high.

Nested if
→ if inside another if.

Use braces
→ For clear and safe multi-statement blocks.

Most common trap
→ = is assignment, == is comparison.
~~~

## Golden Memory Trick

**`if` means: "Only do this when this condition is true."**

## One-Line Recognition

**Whenever a problem asks you to perform an action only when a condition is satisfied, use an `if` statement.**
