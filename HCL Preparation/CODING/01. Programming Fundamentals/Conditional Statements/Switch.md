---
type: concept
subject: coding
topic: "Switch"
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
  - switch
  - java
  - programming
wikilinks:
  - "[[Conditional Statements]]"
  - "[[if]]"
  - "[[if else]]"
  - "[[Nested if]]"
  - "[[Loops]]"
---

# Switch

## 1. Core Concept

> [!summary]
> The `switch` statement is used when a program needs to choose **one action from multiple fixed choices** based on the value of an expression.

Basic structure:

~~~java
switch (expression) {

    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
}
~~~

Example:

~~~java
int day = 2;

switch (day) {

    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    default:
        System.out.println("Invalid Day");
}
~~~

Since:

$$
day=2
$$

the `case 2` block executes.

Output:

~~~text
Tuesday
~~~

---

# 2. Basic Meaning

A `switch` provides a clean way to compare one expression against several possible values.

Think:

~~~text
Expression
    ↓
 ┌──┴──┬──────┐
 ↓     ↓      ↓
case1 case2  case3
 ↓     ↓      ↓
Action Action Action
~~~

Example:

~~~java
int option = 3;

switch (option) {

    case 1:
        System.out.println("Add");
        break;

    case 2:
        System.out.println("Delete");
        break;

    case 3:
        System.out.println("Search");
        break;

    default:
        System.out.println("Invalid");
}
~~~

The value `3` matches `case 3`.

Therefore:

$$
\boxed{Search}
$$

---

# 3. Syntax

The standard form is:

~~~java
switch (expression) {

    case value1:
        statements;
        break;

    case value2:
        statements;
        break;

    default:
        statements;
}
~~~

Important components:

| Component | Meaning |
|---|---|
| `switch` | Starts the selection statement |
| `expression` | Value being tested |
| `case` | Possible matching value |
| `break` | Exits the switch |
| `default` | Executes when no case matches |
| `:` | Separates case value from its statements |

---

# 4. How switch Works

Suppose:

~~~java
int n = 3;
~~~

and:

~~~java
switch (n) {

    case 1:
        System.out.println("One");
        break;

    case 2:
        System.out.println("Two");
        break;

    case 3:
        System.out.println("Three");
        break;

    default:
        System.out.println("Other");
}
~~~

Java checks the switch expression:

$$
n=3
$$

Then searches for:

~~~text
case 3
~~~

It finds the match.

Therefore:

~~~text
Three
~~~

The `break` then exits the switch.

---

# 5. Basic Example — Day Number

## Example 1

### Question

Print the day corresponding to:

$$
day=3
$$

Use:

~~~text
1 → Monday
2 → Tuesday
3 → Wednesday
4 → Thursday
5 → Friday
~~~

### Pattern

One value with multiple fixed choices.

Use `switch`.

### Code

~~~java
int day = 3;

switch (day) {

    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    case 3:
        System.out.println("Wednesday");
        break;

    case 4:
        System.out.println("Thursday");
        break;

    case 5:
        System.out.println("Friday");
        break;

    default:
        System.out.println("Invalid Day");
}
~~~

Match:

$$
day=3
$$

Therefore:

### Answer

$$
\boxed{Wednesday}
$$

---

# 6. The break Statement

`break` stops execution of the current `switch`.

Example:

~~~java
int n = 2;

switch (n) {

    case 1:
        System.out.println("One");
        break;

    case 2:
        System.out.println("Two");
        break;

    case 3:
        System.out.println("Three");
        break;
}
~~~

Output:

~~~text
Two
~~~

The `break` prevents execution from continuing into `case 3`.

> [!important]
> In traditional switch syntax, `break` is commonly used to prevent unintended fall-through.

---

# 7. What Happens Without break?

Consider:

~~~java
int n = 2;

switch (n) {

    case 1:
        System.out.println("One");

    case 2:
        System.out.println("Two");

    case 3:
        System.out.println("Three");
}
~~~

`n` is `2`.

So Java starts at `case 2`.

It prints:

~~~text
Two
Three
~~~

Why?

Because there is no `break` after `case 2`.

This is called **fall-through**.

> [!warning]
> Forgetting `break` can cause multiple case blocks to execute unexpectedly.

---

# 8. Fall-Through

Fall-through means execution continues into the next case after a matching case when there is no terminating statement such as `break`.

Example:

~~~java
int n = 1;

switch (n) {

    case 1:
        System.out.println("A");

    case 2:
        System.out.println("B");

    case 3:
        System.out.println("C");
}
~~~

Output:

~~~text
A
B
C
~~~

Because execution starts at `case 1` and continues through later cases.

> [!important]
> Fall-through is not always a mistake. It can be intentionally used to group cases.

---

# 9. Intentional Fall-Through

Suppose:

~~~text
1 → Monday
2 → Tuesday
3 → Wednesday
4 → Thursday
5 → Friday