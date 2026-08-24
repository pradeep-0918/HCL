---
type: concept
subject: coding
topic: "if else"
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
  - if-else
  - java
  - programming
wikilinks:
  - "[[Conditional Statements]]"
  - "[[if]]"
  - "[[Nested if]]"
  - "[[Switch]]"
---

# if else

## 1. Core Concept

> [!summary]
> The `if-else` statement is used when there are **two possible paths**.
>
> If the condition is `true`, the `if` block executes.
>
> If the condition is `false`, the `else` block executes.

Basic structure:

~~~java
if (condition) {
    // true case
} else {
    // false case
}
~~~

Flow:

~~~text
             Condition
              /     \
           true     false
            ↓         ↓
        if block   else block
            \         /
             Continue
~~~

Example:

~~~java
int n = 10;

if (n > 0) {
    System.out.println("Positive");
} else {
    System.out.println("Not Positive");
}
~~~

Since:

$$
10>0
$$

the `if` block executes.

Output:

~~~text
Positive
~~~

---

# 2. Basic Meaning

An `if-else` statement provides an alternative path.

Think:

~~~text
IF condition is true
→ Do A

ELSE
→ Do B
~~~

Example:

~~~java
int age = 16;

if (age >= 18) {
    System.out.println("Eligible");
} else {
    System.out.println("Not Eligible");
}
~~~

Since:

$$
16<18
$$

the `else` block executes.

Output:

~~~text
Not Eligible
~~~

> [!important]
> Exactly one of the two blocks executes.

---

# 3. Syntax

The basic Java syntax is:

~~~java
if (condition) {
    // statements
} else {
    // statements
}
~~~

Important parts:

| Part | Meaning |
|---|---|
| `if` | Checks the condition |
| `condition` | Must evaluate to `true` or `false` |
| `if` block | Executes when condition is true |
| `else` block | Executes when condition is false |

---

# 4. Basic Examples

## Example 1 — Positive or Negative

### Question

Determine whether a number is positive or not.

Given:

$$
n=-5
$$

### Pattern

Positive:

$$
n>0
$$

Otherwise:

~~~text
Not Positive
~~~

### Code

~~~java
int n = -5;

if (n > 0) {
    System.out.println("Positive");
} else {
    System.out.println("Not Positive");
}
~~~

Since:

$$
-5>0=false
$$

the `else` block executes.

### Answer

$$
\boxed{Not\ Positive}
$$

---

# 5. Example — Even or Odd

## Example 2

### Question

Check whether a number is even or odd.

Given:

$$
n=27
$$

### Pattern

Even:

$$
n\%2=0
$$

Otherwise → odd.

### Code

~~~java
int n = 27;

if (n % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
~~~

Calculation:

$$
27\%2=1
$$

Therefore the condition is false.

### Answer

$$
\boxed{Odd}
$$

> [!important]
> This is one of the most common `if-else` patterns in basic coding questions.

---

# 6. Example — Pass or Fail

## Example 3

### Question

A student passes if marks are at least `40`.

Given:

$$
marks=35
$$

### Pattern

Pass:

$$
marks\geq40
$$

### Code

~~~java
int marks = 35;

if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
~~~

Since:

$$
35\geq40=false
$$

### Answer

$$
\boxed{Fail}
$$

---

# 7. Example — Greater of Two Numbers

## Example 4

### Question

Find the larger of:

$$
a=25,\quad b=40
$$

### Pattern

Compare:

$$
a>b
$$

If true → `a`.

Otherwise → `b`.

### Code

~~~java
int a = 25;
int b = 40;

if (a > b) {
    System.out.println(a);
} else {
    System.out.println(b);
}
~~~

Since:

$$
25>40=false
$$

the `else` block executes.

### Answer

$$
\boxed{40}
$$

> [!tip]
> For exactly two alternatives, `if-else` is usually cleaner than two independent `if` statements.

---

# 8. if vs if-else

## `if`

Use when you want an action only when a condition is true.

~~~java
if (age >= 18) {
    System.out.println("Adult");
}
~~~

If false, nothing happens.

## `if-else`

Use when there are two mutually exclusive outcomes.

~~~java
if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
~~~

### Comparison

| Feature | `if` | `if-else` |
|---|---|---|
| True case | Yes | Yes |
| False case | Nothing | `else` executes |
| Alternatives | One possible action | Two possible paths |
| Example | Check condition | Pass/Fail |

---

# 9. Nested if-else

An `if` or `else` block can contain another conditional statement.

Example:

~~~java
int n = 10;

if (n >= 0) {

    if (n == 0) {
        System.out.println("Zero");
    } else {
        System.out.println("Positive");
    }

} else {
    System.out.println("Negative");
}
~~~

Flow:

~~~text
n >= 0?
├── No  → Negative
└── Yes
     ↓
   n == 0?
   ├── Yes → Zero
   └── No  → Positive
~~~

### Answer

For:

$$
n=10
$$

the output is:

$$
\boxed{Positive}
$$

---

# 10. else-if Ladder

When there are more than two possibilities, use `else if`.

Example:

~~~java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 75) {
    System.out.println("B");
} else if (marks >= 60) {
    System.out.println("C");
} else if (marks >= 40) {
    System.out.println("D");
} else {
    System.out.println("F");
}
~~~

For:

$$
marks=82
$$

Check:

$$
82\geq90=false
$$

Then:

$$
82\geq75=true
$$

Therefore:

~~~text
B
~~~

### Answer

$$
\boxed{B}
$$

> [!important]
> In an `if-else-if` ladder, once one condition becomes true, its block executes and the remaining `else if` conditions are skipped.

---

# 11. Order of Conditions

The order of conditions matters.

Example:

~~~java
int marks = 95;

if (marks >= 40) {
    System.out.println("Pass");
} else if (marks >= 90) {
    System.out.println("A");
}
~~~

The first condition is already true:

$$
95\geq40
$$

So the output is:

~~~text
Pass
~~~

The `90` condition is never reached.

Correct ordering:

~~~java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
~~~

> [!warning]
> In an `else-if` ladder, put **more specific or stricter conditions before broader conditions** when they overlap.

---

# 12. Example — Grade Calculation

## Example 5

### Question

Assign grades:

| Marks | Grade |
|---:|---|
| 90–100 | A |
| 75–89 | B |
| 60–74 | C |
| 40–59 | D |
| Below 40 | F |

Given:

$$
marks=76
$$

### Pattern

Multiple ranges → `else-if` ladder.

### Code

~~~java
int marks = 76;

if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 75) {
    System.out.println("B");
} else if (marks >= 60) {
    System.out.println("C");
} else if (marks >= 40) {
    System.out.println("D");
} else {
    System.out.println("F");
}
~~~

Check:

$$
76\geq90=false
$$

$$
76\geq75=true
$$

Therefore:

### Answer

$$
\boxed{B}
$$

---

# 13. Multiple Conditions with if-else

`if-else` can contain logical operators.

Example:

~~~java
int age = 25;
boolean hasId = true;

if (age >= 18 && hasId) {
    System.out.println("Allowed");
} else {
    System.out.println("Not Allowed");
}
~~~

Both conditions are true:

$$
25\geq18
$$

and:

$$
hasId=true
$$

Therefore:

### Answer

$$
\boxed{Allowed}
$$

---

# 14. OR Condition

## Example 6

### Question

A person gets a discount if they are a student or a senior citizen.

### Pattern

Either condition can be true.

Use:

$$
||
$$

### Code

~~~java
boolean student = false;
boolean senior = true;

if (student || senior) {
    System.out.println("Discount");
} else {
    System.out.println("No Discount");
}
~~~

Since:

$$
false\lor true=true
$$

### Answer

$$
\boxed{Discount}
$$

---

# 15. Example — Absolute Value

## Example 7

### Question

Find the absolute value of:

$$
n=-15
$$

### Pattern

If negative, change its sign.

### Code

~~~java
int n = -15;

if (n < 0) {
    n = -n;
}

System.out.println(n);
~~~

Here only an `if` is necessary because nothing special is required for positive values.

Output:

~~~text
15
~~~

### Answer

$$
\boxed{15}
$$

> [!important]
> Not every problem needs `else`. Use `else` only when the false case requires a different action.

---

# 16. Example — Maximum of Three Numbers

## Example 8

### Question

Find the largest among:

$$
10,\ 25,\ 18
$$

### Pattern

Multiple comparisons.

### Code

~~~java
int a = 10;
int b = 25;
int c = 18;

if (a >= b && a >= c) {
    System.out.println(a);
} else if (b >= a && b >= c) {
    System.out.println(b);
} else {
    System.out.println(c);
}
~~~

Check:

~~~text
a = 10
b = 25
c = 18
~~~

`a` is not largest.

`b` is greater than both:

$$
25\geq10
$$

$$
25\geq18
$$

Therefore:

### Answer

$$
\boxed{25}
$$

---

# 17. Ternary Operator vs if-else

For simple assignments, the ternary operator can replace an `if-else`.

### if-else

~~~java
int max;

if (a > b) {
    max = a;
} else {
    max = b;
}
~~~

### Ternary

~~~java
int max = a > b ? a : b;
~~~

Both perform the same basic decision.

> [!tip]
> Use ternary for short, simple value selection. Use `if-else` when the logic is longer or contains multiple statements.

---

# 18. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Even/Odd

~~~java
if (n % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
~~~

---

### Pattern 2 — Positive/Negative

~~~java
if (n >= 0) {
    System.out.println("Non-negative");
} else {
    System.out.println("Negative");
}
~~~

---

### Pattern 3 — Pass/Fail

~~~java
if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
~~~

---

### Pattern 4 — Greater of Two

~~~java
if (a > b) {
    System.out.println(a);
} else {
    System.out.println(b);
}
~~~

---

### Pattern 5 — Divisible/Not Divisible

~~~java
if (n % k == 0) {
    System.out.println("Divisible");
} else {
    System.out.println("Not Divisible");
}
~~~

---

### Pattern 6 — Valid/Invalid

~~~java
if (condition) {
    System.out.println("Valid");
} else {
    System.out.println("Invalid");
}
~~~

---

### Pattern 7 — Grade Classification

Use an:

~~~text
else-if ladder
~~~

---

### Pattern 8 — Multiple Requirements

Use:

~~~java
if (condition1 && condition2) {
    ...
} else {
    ...
}
~~~

---

# 19. Recognition Tricks

> [!important]
> If the question has **exactly two outcomes**, think `if-else`.

Examples:

~~~text
Even / Odd
Pass / Fail
Positive / Negative
Valid / Invalid
Eligible / Not Eligible
Yes / No
Greater / Smaller
~~~

> [!important]
> If the question has **more than two categories**, think `else-if ladder`.

> [!important]
> If the false case requires no action, use only `if`.

> [!important]
> If both conditions must be true, think `&&`.

> [!important]
> If either condition can be true, think `||`.

> [!important]
> If the conditions overlap, order the stricter conditions first.

---

# 20. Shortcuts

> [!tip]
> **Shortcut: Two Outcomes**
>
> ```text
> Two possible results
> → if-else
> ```
>
> Example:
>
> ```text
> Pass / Fail
> Even / Odd
> Yes / No
> ```

> [!tip]
> **Shortcut: Multiple Outcomes**
>
> ```text
> 3 or more categories
> → else-if ladder
> ```

> [!tip]
> **Shortcut: At Least**
>
> "At least 50":
>
> $$n\geq50$$
>
> Use:
>
> ~~~java
> n >= 50
> ~~~

> [!tip]
> **Shortcut: At Most**
>
> "At most 50":
>
> $$n\leq50$$
>
> Use:
>
> ~~~java
> n <= 50
> ~~~

> [!tip]
> **Shortcut: Two-Choice Maximum**
>
> For two values:
>
> ~~~java
> a > b ? a : b
> ~~~
>
> or use `if-else`.

---

# 21. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Using `if` Instead of `if-else`

If the problem requires exactly one of two outputs:

~~~text
Even / Odd
~~~

use:

~~~java
if (n % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
~~~

Do not unnecessarily use two independent conditions.

---

### Mistake 2 — Wrong Condition Order

Wrong:

~~~java
if (marks >= 40) {
    System.out.println("Pass");
} else if (marks >= 90) {
    System.out.println("A");
}
~~~

The `A` case can never be reached for marks `90+`.

Correct:

~~~java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 40) {
    System.out.println("Pass");
}
~~~

---

### Mistake 3 — Incorrect Range

Wrong:

~~~java
if (n >= 10 || n <= 50) {
}
~~~

Correct:

~~~java
if (n >= 10 && n <= 50) {
}
~~~

---

### Mistake 4 — Using `=` Instead of `==`

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

---

### Mistake 5 — Forgetting That `else` Belongs to the Nearest Unmatched `if`

Consider:

~~~java
if (a > 0)
    if (b > 0)
        System.out.println("A");
    else
        System.out.println("B");
~~~

The `else` belongs to the inner `if`.

Using braces makes the intention clear:

~~~java
if (a > 0) {
    if (b > 0) {
        System.out.println("A");
    } else {
        System.out.println("B");
    }
}
~~~

> [!important]
> This is called the **dangling else** situation.

---

### Mistake 6 — Overusing Nested if

Instead of:

~~~java
if (age >= 18) {
    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

a simple logical condition may be clearer:

~~~java
if (age >= 18 && hasId) {
    System.out.println("Allowed");
}
~~~

Choose the structure that makes the logic easiest to understand.

---

# 22. Formula Sheet

### Basic if-else

~~~java
if (condition) {
    // true
} else {
    // false
}
~~~

### Even

$$
n\%2=0
$$

### Odd

$$
n\%2\neq0
$$

### Positive

$$
n>0
$$

### Negative

$$
n<0
$$

### Non-negative

$$
n\geq0
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

~~~java
condition1 && condition2
~~~

### OR

~~~java
condition1 || condition2
~~~

### Ternary Equivalent

~~~java
condition ? value1 : value2
~~~

---

# 23. Quick Revision

> [!summary] One-Minute Revision

~~~text
if-else
→ Two possible paths.

if
→ Executes when condition is true.

else
→ Executes when condition is false.

Exactly one
→ if block OR else block executes.

Two outcomes
→ Use if-else.

Three or more outcomes
→ Use else-if ladder.

Both conditions
→ &&

Either condition
→ ||

Even
→ n % 2 == 0

Odd
→ n % 2 != 0

Divisible by k
→ n % k == 0

At least x
→ >= x

At most x
→ <= x

Range
→ low <= n && n <= high

Overlapping conditions
→ Put stricter conditions first.

Simple value selection
→ Ternary can replace if-else.

Use braces
→ Avoid ambiguity and dangling-else mistakes.
~~~

## Golden Memory Trick

**`if` handles the true path, `else` handles the false path — together they create a two-way decision.**

## One-Line Recognition

**When a problem has exactly two possible outcomes based on one condition, think `if-else`.**