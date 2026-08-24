---
type: concept
subject: coding
topic: "Nested if"
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
  - nested-if
  - decision-making
  - java
  - programming
wikilinks:
  - "[[Conditional Statements]]"
  - "[[if]]"
  - "[[if else]]"
  - "[[Switch]]"
---

# Nested if

## 1. Core Concept

> [!summary]
> A **nested if** is an `if` statement placed inside another `if`, `else`, or `else-if` block.
>
> It is useful when one condition must be satisfied before another condition is checked.

Basic structure:

~~~java
if (condition1) {

    if (condition2) {
        // code
    }
}
~~~

Think:

~~~text
Check Condition 1
       ↓
     True?
       ↓
Check Condition 2
       ↓
     True?
       ↓
    Execute
~~~

Example:

~~~java
int age = 20;
boolean hasId = true;

if (age >= 18) {

    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

First:

$$
20\geq18
$$

Then:

$$
hasId=true
$$

Therefore:

~~~text
Allowed
~~~

---

# 2. Basic Meaning

A nested `if` represents a **decision inside another decision**.

Think of it as:

~~~text
IF condition A is true
    THEN check condition B
        IF condition B is true
            perform the action
~~~

Example:

~~~java
if (usernameCorrect) {

    if (passwordCorrect) {
        System.out.println("Login successful");
    }
}
~~~

The password is checked only after the username condition succeeds.

> [!important]
> The inner `if` is reached only when the outer condition allows execution to enter its block.

---

# 3. Syntax

### Basic Nested if

~~~java
if (condition1) {

    if (condition2) {
        statement;
    }
}
~~~

### Nested if-else

~~~java
if (condition1) {

    if (condition2) {
        statement1;
    } else {
        statement2;
    }

} else {
    statement3;
}
~~~

### Multiple Levels

~~~java
if (condition1) {

    if (condition2) {

        if (condition3) {
            statement;
        }
    }
}
~~~

> [!warning]
> Deeply nested conditions can become difficult to read. Use nesting only when the decision structure genuinely depends on previous conditions.

---

# 4. Why Nested if Is Used

Nested `if` is useful when:

1. The second condition should be checked only after the first condition succeeds.
2. One decision depends on another decision.
3. Different actions are required at different decision levels.
4. A problem naturally describes a hierarchy of conditions.

Example:

~~~text
Eligible for exam?
       ↓
     Yes
       ↓
Has valid ID?
       ↓
     Yes
       ↓
Allowed
~~~

---

# 5. Basic Example — Age and ID

## Example 1

### Question

A person can enter only if:

- Age is at least `18`.
- The person has a valid ID.

Given:

~~~text
age = 21
hasId = true
~~~

### Pattern

First check age.

Then check ID.

### Code

~~~java
int age = 21;
boolean hasId = true;

if (age >= 18) {

    if (hasId) {
        System.out.println("Entry Allowed");
    }
}
~~~

### Step-by-Step

First:

$$
21\geq18=true
$$

Enter the outer `if`.

Then:

$$
hasId=true
$$

Enter the inner `if`.

### Answer

$$
\boxed{Entry\ Allowed}
$$

---

# 6. Example — Outer Condition False

## Example 2

### Question

Using the previous logic, determine the output when:

~~~text
age = 16
hasId = true
~~~

### Code

~~~java
int age = 16;
boolean hasId = true;

if (age >= 18) {

    if (hasId) {
        System.out.println("Entry Allowed");
    }
}
~~~

First:

$$
16\geq18=false
$$

The outer condition fails.

Therefore, the inner `if` is never checked.

### Answer

~~~text
No output
~~~

> [!important]
> This is one of the most important properties of nested `if`: if the outer condition is false, the inner condition is skipped completely.

---

# 7. Example — Inner Condition False

## Example 3

### Question

Given:

~~~text
age = 21
hasId = false
~~~

determine the output.

### Code

~~~java
int age = 21;
boolean hasId = false;

if (age >= 18) {

    if (hasId) {
        System.out.println("Entry Allowed");
    }
}
~~~

First:

$$
21\geq18=true
$$

The inner condition is checked.

Then:

$$
hasId=false
$$

The inner block does not execute.

### Answer

~~~text
No output
~~~

---

# 8. Nested if with else

An inner `if` can have its own `else`.

Example:

~~~java
int age = 20;
boolean hasId = false;

if (age >= 18) {

    if (hasId) {
        System.out.println("Entry Allowed");
    } else {
        System.out.println("ID Required");
    }
}
~~~

First:

$$
20\geq18=true
$$

Then:

$$
hasId=false
$$

Therefore the inner `else` executes.

### Answer

$$
\boxed{ID\ Required}
$$

---

# 9. Nested if-else at Both Levels

## Example 4

### Question

Classify a number as:

- Negative
- Zero
- Positive

Then, if positive, determine whether it is even or odd.

### Code

~~~java
int n = 12;

if (n < 0) {

    System.out.println("Negative");

} else {

    if (n == 0) {
        System.out.println("Zero");
    } else {

        if (n % 2 == 0) {
            System.out.println("Positive Even");
        } else {
            System.out.println("Positive Odd");
        }
    }
}
~~~

### Step-by-Step

First:

$$
12<0=false
$$

Go to `else`.

Next:

$$
12=0=false
$$

Go to the next `else`.

Now:

$$
12\%2=0
$$

Therefore:

~~~text
Positive Even
~~~

### Answer

$$
\boxed{Positive\ Even}
$$

---

# 10. Nested if vs else-if Ladder

These two structures can solve similar problems, but their logic is different.

### Nested if

~~~java
if (age >= 18) {

    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

The second condition depends on the first.

### else-if

~~~java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 75) {
    System.out.println("B");
}
~~~

The conditions represent alternative categories.

### Comparison

| Nested `if` | `else-if` |
|---|---|
| Decision inside another decision | Alternative conditions |
| Inner condition depends on outer path | Conditions are checked sequentially |
| Useful for hierarchical logic | Useful for classification |
| Can create multiple levels | Usually easier for many categories |

> [!important]
> Ask: **"Does the second condition depend on the first?"**
>
> If yes, nested `if` may be appropriate.

---

# 11. Nested if vs Logical AND

Sometimes nested `if` can be simplified using `&&`.

### Nested version

~~~java
if (age >= 18) {

    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

### `&&` version

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

### When to Prefer Nested if

Use nested logic when the second step needs a different action or additional processing.

Example:

~~~java
if (usernameCorrect) {

    if (passwordCorrect) {
        // login
    } else {
        // wrong password
    }

} else {
    // wrong username
}
~~~

This has different outcomes at different levels.

---

# 12. Example — Login Validation

## Example 5

### Question

A login should proceed only if:

1. Username is correct.
2. Password is correct.

If the username is incorrect, print `"Invalid Username"`.

If username is correct but password is wrong, print `"Invalid Password"`.

Otherwise print `"Login Successful"`.

### Code

~~~java
boolean usernameCorrect = true;
boolean passwordCorrect = false;

if (usernameCorrect) {

    if (passwordCorrect) {
        System.out.println("Login Successful");
    } else {
        System.out.println("Invalid Password");
    }

} else {
    System.out.println("Invalid Username");
}
~~~

### Step-by-Step

Username:

$$
true
$$

So enter the outer block.

Password:

$$
false
$$

Therefore:

### Answer

$$
\boxed{Invalid\ Password}
$$

---

# 13. Example — Student Eligibility

## Example 6

### Question

A student is eligible for an advanced course if:

- Marks are at least `60`.
- Attendance is at least `75%`.

If marks are below `60`, print `"Insufficient Marks"`.

If marks are sufficient but attendance is below `75%`, print `"Low Attendance"`.

Otherwise print `"Eligible"`.

### Code

~~~java
int marks = 70;
int attendance = 68;

if (marks >= 60) {

    if (attendance >= 75) {
        System.out.println("Eligible");
    } else {
        System.out.println("Low Attendance");
    }

} else {
    System.out.println("Insufficient Marks");
}
~~~

### Step-by-Step

Marks:

$$
70\geq60=true
$$

Attendance:

$$
68\geq75=false
$$

Therefore:

### Answer

$$
\boxed{Low\ Attendance}
$$

---

# 14. Example — Number Classification

## Example 7

### Question

Classify a number as:

- Positive Even
- Positive Odd
- Negative
- Zero

Given:

$$
n=-12
$$

### Code

~~~java
int n = -12;

if (n > 0) {

    if (n % 2 == 0) {
        System.out.println("Positive Even");
    } else {
        System.out.println("Positive Odd");
    }

} else {

    if (n == 0) {
        System.out.println("Zero");
    } else {
        System.out.println("Negative");
    }
}
~~~

### Step-by-Step

First:

$$
-12>0=false
$$

Go to outer `else`.

Then:

$$
-12=0=false
$$

Therefore:

~~~text
Negative
~~~

### Answer

$$
\boxed{Negative}
$$

---

# 15. Example — Largest of Three Numbers

## Example 8

### Question

Find the largest among:

$$
a=50,\quad b=30,\quad c=40
$$

### Pattern

Compare one number against the other two.

### Code

~~~java
int a = 50;
int b = 30;
int c = 40;

if (a >= b) {

    if (a >= c) {
        System.out.println(a);
    } else {
        System.out.println(c);
    }

} else {

    if (b >= c) {
        System.out.println(b);
    } else {
        System.out.println(c);
    }
}
~~~

### Step-by-Step

First:

$$
50\geq30=true
$$

Now compare `a` and `c`:

$$
50\geq40=true
$$

Therefore:

### Answer

$$
\boxed{50}
$$

---

# 16. Example — Smallest of Three Numbers

## Example 9

### Question

Find the smallest among:

$$
a=25,\quad b=10,\quad c=15
$$

### Code

~~~java
int a = 25;
int b = 10;
int c = 15;

if (a <= b) {

    if (a <= c) {
        System.out.println(a);
    } else {
        System.out.println(c);
    }

} else {

    if (b <= c) {
        System.out.println(b);
    } else {
        System.out.println(c);
    }
}
~~~

First:

$$
25\leq10=false
$$

Go to outer `else`.

Then:

$$
10\leq15=true
$$

Therefore:

### Answer

$$
\boxed{10}
$$

---

# 17. Example — Character Classification

## Example 10

### Question

Determine whether a character is:

- Uppercase
- Lowercase
- Digit
- Other

Given:

~~~text
ch = 'G'
~~~

### Code

~~~java
char ch = 'G';

if (ch >= 'A' && ch <= 'Z') {

    System.out.println("Uppercase");

} else {

    if (ch >= 'a' && ch <= 'z') {
        System.out.println("Lowercase");
    } else {

        if (ch >= '0' && ch <= '9') {
            System.out.println("Digit");
        } else {
            System.out.println("Other");
        }
    }
}
~~~

Check:

$$
'A'\leq'G'\leq'Z'
$$

Therefore:

### Answer

$$
\boxed{Uppercase}
$$

> [!tip]
> For many mutually exclusive categories, an `else-if` ladder is usually more readable than deeply nested `if` statements.

---

# 18. Example — Leap Year with Nested Logic

## Example 11

### Question

Determine whether:

$$
year=2000
$$

is a leap year using nested conditions.

### Logic

A leap year is:

- divisible by `400`, OR
- divisible by `4` but not by `100`.

### Nested Code

~~~java
int year = 2000;

if (year % 4 == 0) {

    if (year % 100 == 0) {

        if (year % 400 == 0) {
            System.out.println("Leap Year");
        } else {
            System.out.println("Not Leap Year");
        }

    } else {
        System.out.println("Leap Year");
    }

} else {
    System.out.println("Not Leap Year");
}
~~~

### Step-by-Step

First:

$$
2000\%4=0
$$

Then:

$$
2000\%100=0
$$

Then:

$$
2000\%400=0
$$

Therefore:

### Answer

$$
\boxed{Leap\ Year}
$$

---

# 19. Example — Nested if with Range

## Example 12

### Question

A number is considered valid if:

$$
0\leq n\leq100
$$

If valid, determine whether it is at least `50`.

Given:

$$
n=75
$$

### Code

~~~java
int n = 75;

if (n >= 0 && n <= 100) {

    if (n >= 50) {
        System.out.println("Valid and High");
    } else {
        System.out.println("Valid and Low");
    }

} else {
    System.out.println("Invalid");
}
~~~

### Step-by-Step

Check validity:

$$
75\geq0
$$

and:

$$
75\leq100
$$

So the number is valid.

Then:

$$
75\geq50
$$

Therefore:

### Answer

$$
\boxed{Valid\ and\ High}
$$

---

# 20. Nested if with Input

A common coding pattern is:

1. Read input.
2. Validate input.
3. Perform another operation only if valid.

Example:

~~~java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        if (n >= 0) {

            if (n % 2 == 0) {
                System.out.println("Non-negative Even");
            } else {
                System.out.println("Non-negative Odd");
            }

        } else {
            System.out.println("Negative");
        }
    }
}
~~~

### Pattern

~~~text
Input
 ↓
Check sign
 ↓
If non-negative
 ↓
Check parity
~~~

This structure appears frequently in beginner coding problems.

---

# 21. Short-Circuit Behavior

Nested `if` can naturally avoid evaluating unnecessary conditions.

Example:

~~~java
if (arr != null) {

    if (arr.length > 0) {
        System.out.println(arr[0]);
    }
}
~~~

The array length is checked only after confirming that `arr` is not `null`.

Conceptually:

~~~text
arr exists?
    ↓
   Yes
    ↓
arr has elements?
    ↓
   Yes
    ↓
access arr[0]
~~~

> [!important]
> This pattern is useful when the second operation is safe only after the first condition has been established.

---

# 22. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Two-Level Validation

~~~java
if (condition1) {

    if (condition2) {
        // valid
    }
}
~~~

Use when the second condition is meaningful only after the first succeeds.

---

### Pattern 2 — Login Validation

~~~text
Username
   ↓
Password
   ↓
Success
~~~

---

### Pattern 3 — Eligibility Validation

~~~text
Basic eligibility
      ↓
Additional requirement
      ↓
Eligible
~~~

---

### Pattern 4 — Number Classification

~~~text
Positive?
 ├─ Yes → Even/Odd
 └─ No  → Zero/Negative
~~~

---

### Pattern 5 — Hierarchical Range Checking

~~~text
Valid range?
 ├─ No → Invalid
 └─ Yes
      ↓
   High/Low
~~~

---

### Pattern 6 — Maximum/Minimum

Compare the first candidate.

Then compare the winner against the remaining candidate.

---

### Pattern 7 — Character Classification

~~~text
Uppercase?
 ↓
Lowercase?
 ↓
Digit?
 ↓
Other
~~~

---

### Pattern 8 — Dependent Decisions

If the second decision cannot logically happen until the first succeeds, nested `if` is a natural pattern.

---

# 23. Recognition Tricks

> [!important]
> If the question says **"first check A, then check B"**, think nested `if`.

> [!important]
> If condition B makes sense only when condition A is true, think:
>
> ~~~text
> if A
>     if B
> ~~~

> [!important]
> If there are two independent conditions that simply must both be true, `&&` may be simpler.

> [!important]
> If each condition represents a separate category, think `else-if`.

> [!important]
> If a condition protects a later operation, think nested `if`.
>
> Example:
>
> ~~~text
> valid array?
>     ↓
> non-empty?
>     ↓
> access element
> ~~~

> [!important]
> If the question has a hierarchy of decisions, think:
>
> ```text
> Outer decision
>      ↓
> Inner decision
>      ↓
> Final action
> ```

---

# 24. Shortcuts

> [!tip]
> **Shortcut: Dependent Conditions**
>
> Ask:
>
> **"Can I check the second condition without checking the first?"**
>
> If no, nested `if` may be appropriate.

> [!tip]
> **Shortcut: Two Independent Conditions**
>
> If both conditions simply need to be true:
>
> ~~~java
> if (condition1 && condition2) {
> }
> ~~~
>
> may be cleaner than nested `if`.

> [!tip]
> **Shortcut: Multiple Categories**
>
> For:
>
> ```text
> A
> B
> C
> D
> ```
>
> prefer an `else-if` ladder when the categories are mutually exclusive.

> [!tip]
> **Shortcut: Protection Pattern**
>
> Use:
>
> ~~~text
> Validate
> ↓
> Process
> ~~~
>
> Example:
>
> ~~~java
> if (n >= 0) {
>     if (n > 0) {
>         // process
>     }
> }
> ~~~

---

# 25. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing Nested if with else-if

Nested:

~~~java
if (condition1) {

    if (condition2) {
    }
}
~~~

This means condition 2 is checked inside condition 1.

Else-if:

~~~java
if (condition1) {
} else if (condition2) {
}
~~~

This means condition 2 is an alternative path.

---

### Mistake 2 — Forgetting the Outer Condition

If:

~~~java
if (age >= 18) {

    if (hasId) {
        System.out.println("Allowed");
    }
}
~~~

and:

$$
age<18
$$

the inner condition is never checked.

---

### Mistake 3 — Wrong else Association

Consider:

~~~java
if (a > 0)
    if (b > 0)
        System.out.println("A");
    else
        System.out.println("B");
~~~

The `else` belongs to the nearest unmatched `if`.

Use braces to avoid confusion.

---

### Mistake 4 — Unnecessary Deep Nesting

Avoid structures like:

~~~java
if (a) {
    if (b) {
        if (c) {
            if (d) {
                // code
            }
        }
    }
}
~~~

when the logic can be expressed clearly using:

~~~java
if (a && b && c && d) {
    // code
}
~~~

---

### Mistake 5 — Incorrect Range Conditions

Wrong:

~~~java
if (n >= 10) {
    if (n <= 50) {
        // valid
    }
}
~~~

This is logically valid for an inclusive range, but when there are more complex outcomes, make sure each branch clearly handles what happens when the range fails.

---

### Mistake 6 — Using Nested if for Simple Classification

If the problem is simply:

~~~text
90+ → A
75+ → B
60+ → C
40+ → D
else → F
~~~

an `else-if` ladder is generally clearer.

---

### Mistake 7 — Forgetting Braces

Always use braces for nested conditions.

Good:

~~~java
if (condition1) {

    if (condition2) {
        statement;
    }
}
~~~

This makes the hierarchy obvious.

---

# 26. Formula Sheet

### Nested if

~~~java
if (condition1) {

    if (condition2) {
        statement;
    }
}
~~~

### Nested if-else

~~~java
if (condition1) {

    if (condition2) {
        statement1;
    } else {
        statement2;
    }

} else {
    statement3;
}
~~~

### Both Conditions

$$
A\land B
$$

Java:

~~~java
A && B
~~~

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

### Range

$$
a\leq n\leq b
$$

Java:

~~~java
n >= a && n <= b
~~~

### Uppercase

$$
'A'\leq ch\leq'Z'
$$

### Lowercase

$$
'a'\leq ch\leq'z'
$$

### Digit

$$
'0'\leq ch\leq'9'
$$

---

# 27. Quick Revision

> [!summary] One-Minute Revision

~~~text
Nested if
→ if inside another if/else block.

Main idea
→ Decision inside a decision.

Outer condition
→ Must succeed before inner condition is checked.

Basic structure
→ if (A) { if (B) { } }

Dependent conditions
→ Strong use case for nested if.

Independent conditions
→ && may be simpler.

Multiple categories
→ else-if is usually clearer.

Outer false
→ Inner if is skipped.

Outer true + inner true
→ Inner block executes.

Outer true + inner false
→ Inner else executes if present.

Two-level validation
→ Common nested-if pattern.

Login
→ Username → Password → Result.

Eligibility
→ Basic requirement → Additional requirement.

Classification
→ First category → More specific category.

Protection
→ Validate before performing an operation.

Use braces
→ Prevent ambiguity.

Avoid deep nesting
→ Prefer clearer conditions when possible.

Most important question:
→ Does the second decision depend on the first?
~~~

## Golden Memory Trick

**Nested `if` means: "First pass this decision, then make the next decision."**

## One-Line Recognition

**When one condition must be satisfied before another condition is meaningfully checked, think Nested `if`.**