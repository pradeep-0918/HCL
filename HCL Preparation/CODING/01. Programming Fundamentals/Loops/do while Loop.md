---
type: concept
subject: coding
topic: "do while Loop"
parent: "Loops"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - loops
  - do-while-loop
  - iteration
  - java
  - programming
wikilinks:
  - "[[Loops]]"
  - "[[for Loop]]"
  - "[[while Loop]]"
  - "[[Nested Loops]]"
  - "[[Conditional Statements]]"
---

# do while Loop

## 1. Core Concept

> [!summary]
> A `do while` loop executes the loop body **at least once**, and then continues repeating as long as the condition is true.
>
> The key difference from `while` is:
>
> **`while` → condition first, body second**
>
> **`do while` → body first, condition second**

Basic syntax:

~~~java
do {
    // statements
} while (condition);
~~~

Example:

~~~java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
~~~

Output:

~~~text
1
2
3
4
5
~~~

Execution flow:

~~~text
Start
  ↓
Execute body
  ↓
Check condition
  ↓
 true?
 ┌──┴──┐
Yes   No
 ↓     ↓
Body   Exit
 ↓
Check again
~~~

> [!important]
> The body of a `do while` loop executes **at least once**, even if the condition is initially false.

---

# 2. Basic Meaning

Think of `do while` as:

~~~text
DO this work first
THEN ask:
"Should I repeat?"
~~~

Example:

~~~java
int i = 10;

do {
    System.out.println(i);
    i++;
} while (i < 5);
~~~

The condition is:

$$
10<5
$$

which is false.

But the body already executed once.

Output:

~~~text
10
~~~

### Key Rule

$$
\boxed{\text{do while executes at least once}}
$$

---

# 3. Syntax

The standard Java syntax is:

~~~java
do {
    // loop body
} while (condition);
~~~

> [!warning]
> The semicolon after the `while` condition is required.

Correct:

~~~java
do {
    // body
} while (condition);
~~~

Incorrect:

~~~java
do {
    // body
} while (condition)
~~~

---

# 4. Execution Order

Consider:

~~~java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 3);
~~~

### Step 1

Initialize:

$$
i=1
$$

### Step 2

Execute body.

Print:

~~~text
1
~~~

### Step 3

Update:

$$
i=2
$$

### Step 4

Check:

$$
2\leq3=true
$$

Repeat.

### Step 5

Print:

~~~text
2
~~~

Update:

$$
i=3
$$

### Step 6

Check:

$$
3\leq3=true
$$

Repeat.

### Step 7

Print:

~~~text
3
~~~

Update:

$$
i=4
$$

### Step 8

Check:

$$
4\leq3=false
$$

Exit.

### Answer

~~~text
1
2
3
~~~

---

# 5. Most Important Difference from while

Consider the same condition:

$$
i<5
$$

### while

~~~java
int i = 10;

while (i < 5) {
    System.out.println(i);
}
~~~

Condition is initially false.

Output:

~~~text
No output
~~~

### do while

~~~java
int i = 10;

do {
    System.out.println(i);
} while (i < 5);
~~~

Body executes before the condition is checked.

Output:

~~~text
10
~~~

Therefore:

| Loop | Minimum Executions |
|---|---:|
| `while` | 0 |
| `do while` | 1 |
| `for` | 0 |
| `do while` | At least 1 |

> [!important]
> This is one of the most frequently tested differences between `while` and `do while`.

---

# 6. Basic Example — Print 1 to 5

## Example 1

### Question

Print numbers from `1` to `5`.

### Pattern

Start at `1`.

Continue while:

$$
i\leq5
$$

### Code

~~~java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
~~~

### Answer

~~~text
1
2
3
4
5
~~~

---

# 7. Example — Condition Initially False

## Example 2

### Question

What is the output?

~~~java
int i = 10;

do {
    System.out.println(i);
    i++;
} while (i < 5);
~~~

### Step 1

Body executes immediately.

Print:

~~~text
10
~~~

### Step 2

Update:

$$
i=11
$$

### Step 3

Check:

$$
11<5=false
$$

Loop stops.

### Answer

$$
\boxed{10}
$$

> [!tip]
> In output questions, check the loop type first. If it is `do while`, execute the body once before evaluating the condition.

---

# 8. Example — Sum of Numbers

## Example 3

### Question

Find:

$$
1+2+3+4+5
$$

### Code

~~~java
int i = 1;
int sum = 0;

do {
    sum += i;
    i++;
} while (i <= 5);

System.out.println(sum);
~~~

Calculation:

$$
1+2+3+4+5=15
$$

### Answer

$$
\boxed{15}
$$

---

# 9. Example — Print Even Numbers

## Example 4

### Question

Print even numbers from `2` to `10`.

### Code

~~~java
int i = 2;

do {
    System.out.println(i);
    i += 2;
} while (i <= 10);
~~~

### Answer

~~~text
2
4
6
8
10
~~~

---

# 10. Example — Print Numbers in Reverse

## Example 5

### Question

Print numbers from `5` down to `1`.

### Code

~~~java
int i = 5;

do {
    System.out.println(i);
    i--;
} while (i >= 1);
~~~

### Answer

~~~text
5
4
3
2
1
~~~

---

# 11. Example — Multiplication Table

## Example 6

### Question

Print the multiplication table of `7`.

### Code

~~~java
int n = 7;
int i = 1;

do {
    System.out.println(n + " x " + i + " = " + (n * i));
    i++;
} while (i <= 10);
~~~

### Answer

~~~text
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
7 x 6 = 42
7 x 7 = 49
7 x 8 = 56
7 x 9 = 63
7 x 10 = 70
~~~

---

# 12. Example — Sum of Digits

## Example 7

### Question

Find the sum of digits of:

$$
5832
$$

### Pattern

Extract digits repeatedly.

### Formula

$$
digit=n\%10
$$

$$
n=\left\lfloor\frac{n}{10}\right\rfloor
$$

### Code

~~~java
int n = 5832;
int sum = 0;

do {

    int digit = n % 10;

    sum += digit;

    n /= 10;

} while (n > 0);

System.out.println(sum);
~~~

Calculation:

$$
5+8+3+2=18
$$

### Answer

$$
\boxed{18}
$$

> [!important]
> `do while` is particularly interesting for digit problems when you want to guarantee processing at least one digit.

---

# 13. Example — Reverse a Number

## Example 8

### Question

Reverse:

$$
12345
$$

### Pattern

Extract the last digit and construct the reverse.

### Formula

$$
digit=n\%10
$$

$$
reverse=reverse\times10+digit
$$

$$
n=n/10
$$

### Code

~~~java
int n = 12345;
int reverse = 0;

do {

    int digit = n % 10;

    reverse = reverse * 10 + digit;

    n /= 10;

} while (n > 0);

System.out.println(reverse);
~~~

Calculation:

$$
12345\rightarrow54321
$$

### Answer

$$
\boxed{54321}
$$

---

# 14. Example — Palindrome Number

## Example 9

### Question

Check whether:

$$
121
$$

is a palindrome.

### Code

~~~java
int n = 121;
int original = n;
int reverse = 0;

do {

    int digit = n % 10;

    reverse = reverse * 10 + digit;

    n /= 10;

} while (n > 0);

if (original == reverse) {
    System.out.println("Palindrome");
} else {
    System.out.println("Not Palindrome");
}
~~~

Reverse:

$$
121
$$

Comparison:

$$
121=121
$$

### Answer

$$
\boxed{Palindrome}
$$

---

# 15. Example — Menu Driven Program

One of the most important real-world uses of `do while` is a menu that must be displayed **at least once**.

## Example 10

### Question

Display a menu repeatedly until the user chooses `0`.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int choice;

do {

    System.out.println("1. Add");
    System.out.println("2. Delete");
    System.out.println("3. Search");
    System.out.println("0. Exit");

    choice = sc.nextInt();

    switch (choice) {

        case 1:
            System.out.println("Add selected");
            break;

        case 2:
            System.out.println("Delete selected");
            break;

        case 3:
            System.out.println("Search selected");
            break;

        case 0:
            System.out.println("Exiting");
            break;

        default:
            System.out.println("Invalid choice");
    }

} while (choice != 0);
~~~

Pattern:

~~~text
Show menu
   ↓
Read choice
   ↓
Perform action
   ↓
Choice == 0?
   ↓
No → Show menu again
Yes → Exit
~~~

> [!important]
> A menu-driven program is a classic `do while` pattern because the menu must be displayed at least once.

---

# 16. Example — Input Validation

## Example 11

### Question

Ask the user to enter a positive number. Keep asking until the input is valid.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int n;

do {

    System.out.println("Enter a positive number:");
    n = sc.nextInt();

} while (n <= 0);

System.out.println("Valid number: " + n);
~~~

The body executes at least once because the user must be asked for input.

Condition:

$$
n\leq0
$$

means:

~~~text
Invalid → ask again
~~~

When:

$$
n>0
$$

the loop stops.

> [!tip]
> If the program must perform an action once and then decide whether to repeat, `do while` is a strong candidate.

---

# 17. Example — Password Validation

## Example 12

### Question

Keep asking for a password until the correct password is entered.

### Code

~~~java
Scanner sc = new Scanner(System.in);

String password;

do {

    System.out.println("Enter password:");
    password = sc.nextLine();

} while (!password.equals("java123"));

System.out.println("Access Granted");
~~~

The password is requested at least once.

The loop continues while:

$$
password\neq"java123"
$$

### Answer

The loop stops when:

~~~text
java123
~~~

is entered.

> [!important]
> For Java strings, use `.equals()` for content comparison.

---

# 18. Example — Continue Until Exit

## Example 13

### Question

Read numbers until the user enters `0`.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int n;

do {

    n = sc.nextInt();

    if (n != 0) {
        System.out.println("You entered: " + n);
    }

} while (n != 0);
~~~

The input is read at least once.

The loop terminates when:

$$
n=0
$$

This is called a **sentinel-controlled loop**.

---

# 19. Sentinel-Controlled do while

A sentinel is a special value used to stop repetition.

Common examples:

~~~text
-1 → Stop
0  → Exit
"exit" → Stop
"quit" → Stop
~~~

General pattern:

~~~java
do {

    // process input

} while (input != sentinel);
~~~

> [!important]
> When the question says **"continue until the user enters X"**, immediately consider a sentinel-controlled `do while` loop.

---

# 20. do while with break

`break` immediately exits the loop.

Example:

~~~java
int i = 1;

do {

    if (i == 4) {
        break;
    }

    System.out.println(i);
    i++;

} while (i <= 10);
~~~

When:

$$
i=4
$$

`break` terminates the loop.

Output:

~~~text
1
2
3
~~~

> [!important]
> `break` overrides the normal loop condition and exits immediately.

---

# 21. do while with continue

`continue` skips the remaining statements of the current iteration and proceeds to the loop condition.

Example:

~~~java
int i = 0;

do {

    i++;

    if (i == 3) {
        continue;
    }

    System.out.println(i);

} while (i < 5);
~~~

Output:

~~~text
1
2
4
5
~~~

> [!warning]
> With `do while`, `continue` still leads to the condition check. Make sure the loop variable is updated correctly before reaching `continue`.

---

# 22. Infinite do while Loop

Example:

~~~java
do {
    System.out.println("Running");
} while (true);
~~~

Since:

$$
true=true
$$

the condition never becomes false.

Therefore the loop is infinite.

To terminate it:

~~~java
do {

    if (condition) {
        break;
    }

} while (true);
~~~

> [!warning]
> Use infinite loops intentionally. An accidental infinite loop can cause a program to hang or produce Time Limit Exceeded.

---

# 23. while vs do while

This is the most important comparison.

### while

~~~java
while (condition) {
    // body
}
~~~

Execution:

~~~text
Check
 ↓
Body
 ↓
Check
~~~

### do while

~~~java
do {
    // body
} while (condition);
~~~

Execution:

~~~text
Body
 ↓
Check
 ↓
Body
 ↓
Check
~~~

---

# 24. Comparison Table

| Property | `while` | `do while` |
|---|---|---|
| Condition checked | Before body | After body |
| Minimum executions | 0 | 1 |
| Guaranteed first execution | No | Yes |
| Menu programs | Possible | Natural |
| Input validation | Possible | Natural |
| Sentinel input | Possible | Natural |
| Condition-first logic | Better | Less natural |
| Action-first logic | Less natural | Better |

> [!important]
> The single biggest difference:
>
> $$\boxed{while=0\text{ or more},\quad do\ while=1\text{ or more}}$$

---

# 25. for vs while vs do while

| Requirement | Best Natural Choice |
|---|---|
| Repeat exactly N times | `for` |
| Traverse an array | `for` |
| Known start/end/step | `for` |
| Unknown number of iterations | `while` |
| Continue until condition changes | `while` |
| Process digits until number becomes 0 | `while` |
| Menu must appear once | `do while` |
| Input must be requested once | `do while` |
| Validation must happen at least once | `do while` |
| Sentinel input with mandatory first input | `do while` |

> [!tip]
> These are guidelines, not strict restrictions. The same problem can often be solved with different loop types.

---

# 26. Recognition Tricks

> [!important]
> If the question says **"execute at least once"**, think:
>
> $$\boxed{do\ while}$$

> [!important]
> If the program must **show a menu before checking the exit condition**, think:
>
> $$\boxed{do\ while}$$

> [!important]
> If the program must **ask for input at least once**, think:
>
> $$\boxed{do\ while}$$

> [!important]
> If the question says:
>
> ```text
> Ask until valid
> ```
>
> think:
>
> ```java
> do {
>     read input;
> } while (invalid);
> ```

> [!important]
> If the question says:
>
> ```text
> Continue until user enters 0
> ```
>
> think:
>
> ```java
> do {
>     ...
> } while (value != 0);
> ```

> [!important]
> If the condition may be false initially but the body still needs to execute, use:
>
> $$\boxed{do\ while}$$

---

# 27. Shortcuts

> [!tip]
> **Shortcut: At Least Once**
>
> Remember:
>
> ```text
> Must execute once?
>        ↓
>    do while
> ```

> [!tip]
> **Shortcut: Menu**
>
> ```text
> Display menu
> → Read choice
> → Process choice
> → Repeat until Exit
> ```
>
> Think:
>
> $$\boxed{do\ while}$$

> [!tip]
> **Shortcut: Validation**
>
> ```text
> Ask
> ↓
> Validate
> ↓
> Invalid → Ask again
> ```
>
> Think:
>
> $$\boxed{do\ while}$$

> [!tip]
> **Shortcut: Sentinel**
>
> If the first input must always be read:
>
> ~~~java
> do {
>     // read/process
> } while (value != sentinel);
> ~~~

> [!tip]
> **Shortcut: Output Questions**
>
> When tracing a `do while`, never check the condition first.
>
> Always:
>
> ```text
> Execute body
> → Update
> → Check condition
> ```

---

# 28. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Menu Driven Program

~~~java
do {
    displayMenu();
    readChoice();
    processChoice();
} while (choice != 0);
~~~

### Pattern 2 — Input Validation

~~~java
do {
    input = readInput();
} while (invalid(input));
~~~

### Pattern 3 — Sentinel

~~~java
do {
    input = readInput();
    process(input);
} while (input != sentinel);
~~~

### Pattern 4 — Number Processing

~~~java
do {
    digit = n % 10;
    n /= 10;
} while (n > 0);
~~~

### Pattern 5 — Reverse Number

~~~java
do {
    digit = n % 10;
    reverse = reverse * 10 + digit;
    n /= 10;
} while (n > 0);
~~~

### Pattern 6 — Password Retry

~~~java
do {
    password = readPassword();
} while (!isCorrect(password));
~~~

### Pattern 7 — Exit Choice

~~~java
do {
    // perform operation
} while (choice != EXIT);
~~~

---

# 29. Advanced Example — Menu + switch

## Example 14

### Question

Create a simple calculator menu that continues until the user chooses `0`.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int choice;

do {

    System.out.println("1. Add");
    System.out.println("2. Subtract");
    System.out.println("3. Multiply");
    System.out.println("4. Divide");
    System.out.println("0. Exit");

    choice = sc.nextInt();

    switch (choice) {

        case 1:
            System.out.println("Addition selected");
            break;

        case 2:
            System.out.println("Subtraction selected");
            break;

        case 3:
            System.out.println("Multiplication selected");
            break;

        case 4:
            System.out.println("Division selected");
            break;

        case 0:
            System.out.println("Goodbye");
            break;

        default:
            System.out.println("Invalid choice");
    }

} while (choice != 0);
~~~

This combines:

~~~text
do while
+
switch
~~~

The `do while` controls repetition.

The `switch` selects the operation.

---

# 30. Advanced Example — Keep Reading Until Negative

## Example 15

### Question

Read positive numbers and calculate their sum. Stop when a negative number is entered.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int n;
int sum = 0;

do {

    n = sc.nextInt();

    if (n >= 0) {
        sum += n;
    }

} while (n >= 0);

System.out.println(sum);
~~~

Suppose input is:

~~~text
10
20
30
-1
~~~

Calculation:

$$
10+20+30=60
$$

The `-1` acts as the sentinel.

### Answer

$$
\boxed{60}
$$

---

# 31. Advanced Example — At Least One Attempt

Suppose a system requires at least one attempt.

~~~java
int attempts = 0;

do {

    attempts++;

    System.out.println("Attempt " + attempts);

} while (attempts < 3);
~~~

Output:

~~~text
Attempt 1
Attempt 2
Attempt 3
~~~

This illustrates the important idea:

~~~text
Do first
↓
Check later
~~~

---

# 32. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting the Semicolon

Wrong:

~~~java
do {
    System.out.println("Hello");
} while (condition)
~~~

Correct:

~~~java
do {
    System.out.println("Hello");
} while (condition);
~~~

The semicolon is required.

---

### Mistake 2 — Thinking do while Checks First

Wrong mental model:

~~~text
Check → Execute
~~~

Correct:

~~~text
Execute → Check
~~~

---

### Mistake 3 — Assuming Zero Executions Are Possible

A `do while` always executes the body at least once.

Example:

~~~java
int x = 10;

do {
    System.out.println(x);
} while (x < 5);
~~~

Output:

~~~text
10
~~~

---

### Mistake 4 — Forgetting to Update the Condition Variable

Wrong:

~~~java
int i = 1;

do {
    System.out.println(i);
} while (i <= 5);
~~~

`i` never changes.

This creates an infinite loop.

Correct:

~~~java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
~~~

---

### Mistake 5 — Wrong Condition Direction

Wrong:

~~~java
int i = 5;

do {
    System.out.println(i);
    i++;
} while (i >= 1);
~~~

`i` increases while the condition checks whether it is at least `1`.

The condition may never become false.

Correct:

~~~java
int i = 5;

do {
    System.out.println(i);
    i--;
} while (i >= 1);
~~~

---

### Mistake 6 — Incorrect continue Usage

Dangerous:

~~~java
int i = 1;

do {

    if (i == 3) {
        continue;
    }

    i++;

} while (i <= 5);
~~~

When `i == 3`, `continue` occurs before `i++`, so `i` remains `3`.

This can create an infinite loop.

---

### Mistake 7 — Losing the Original Number

For palindrome or reverse problems, do not destroy the original value if you need it later.

Use:

~~~java
int original = n;
~~~

Then process `n`.

---

### Mistake 8 — Using do while When Zero Execution Is Required

If the operation should happen only when a condition is initially true, a normal `while` may be more appropriate.

Example:

~~~java
while (balance > 0) {
    process();
}
~~~

This correctly allows zero executions when:

$$
balance\leq0
$$

---

# 33. Time Complexity

The complexity of a `do while` loop depends on how many times the body executes.

### Linear

~~~java
int i = 1;

do {
    i++;
} while (i <= n);
~~~

Time:

$$
\boxed{O(n)}
$$

### Logarithmic

~~~java
int n = 100;

do {
    n /= 2;
} while (n > 1);
~~~

Time:

$$
\boxed{O(\log n)}
$$

### Nested

~~~java
int i = 0;

do {

    int j = 0;

    do {
        j++;
    } while (j < n);

    i++;

} while (i < n);
~~~

Total:

$$
n\times n
$$

Therefore:

$$
\boxed{O(n^2)}
$$

---

# 34. Space Complexity

A basic `do while` loop normally requires constant auxiliary space.

Example:

~~~java
int i = 0;

do {
    i++;
} while (i < n);
~~~

Extra memory:

$$
\boxed{O(1)}
$$

> [!important]
> The loop may execute many times without requiring additional memory.

---

# 35. Output-Tracing Strategy

For placement coding questions, use this method.

### Step 1

Identify the loop type.

If:

~~~java
do {
}
while (...);
~~~

remember:

**body executes first.**

### Step 2

Write the initial variable values.

### Step 3

Execute the body.

### Step 4

Apply all updates.

### Step 5

Evaluate the condition.

### Step 6

Repeat until false.

Example:

~~~java
int x = 3;

do {
    System.out.println(x);
    x += 2;
} while (x < 8);
~~~

Trace:

| Iteration | Printed | New `x` | Condition |
|---|---:|---:|---|
| 1 | 3 | 5 | `5 < 8` → true |
| 2 | 5 | 7 | `7 < 8` → true |
| 3 | 7 | 9 | `9 < 8` → false |

### Answer

~~~text
3
5
7
~~~

---

# 36. Placement Exam Pattern — Predict the Output

## Example 16

### Question

What is the output?

~~~java
int x = 5;

do {
    System.out.print(x + " ");
    x--;
} while (x > 2);
~~~

### Trace

Initial:

$$
x=5
$$

Print:

$$
5
$$

Update:

$$
x=4
$$

Print:

$$
4
$$

Update:

$$
x=3
$$

Print:

$$
3
$$

Update:

$$
x=2
$$

Check:

$$
2>2=false
$$

### Answer

~~~text
5 4 3
~~~

---

# 37. Placement Exam Pattern — False Condition

## Example 17

### Question

What is the output?

~~~java
int x = 10;

do {
    System.out.print(x);
} while (x < 5);
~~~

Initial condition:

$$
10<5=false
$$

But the body executes first.

### Answer

~~~text
10
~~~

> [!important]
> This is a classic trick question.

---

# 38. Placement Exam Pattern — Update Before Condition

## Example 18

### Question

What is the output?

~~~java
int x = 1;

do {
    x += 2;
    System.out.print(x + " ");
} while (x < 7);
~~~

Trace:

~~~text
x = 1
↓
x = 3 → print 3
↓
x = 5 → print 5
↓
x = 7 → print 7
↓
7 < 7 → false
~~~

### Answer

~~~text
3 5 7
~~~

> [!tip]
> In output questions, carefully check whether the update happens before or after the print statement.

---

# 39. Quick Decision Guide

Use this mental decision tree:

~~~text
Need repetition?
      ↓
     Yes
      ↓
Is the number of iterations clearly known?
      ↓
   Yes       No
    ↓         ↓
  for      Must body execute at least once?
              ↓
          Yes       No
           ↓         ↓
       do while    while
~~~

This is a practical way to select the loop quickly.

---

# 40. Formula Sheet

### Basic Syntax

~~~java
do {
    // body
} while (condition);
~~~

### Increasing

~~~java
int i = start;

do {
    // body
    i++;
} while (i <= end);
~~~

### Decreasing

~~~java
int i = start;

do {
    // body
    i--;
} while (i >= end);
~~~

### Digit Extraction

$$
digit=n\%10
$$

### Remove Last Digit

$$
n=\left\lfloor\frac{n}{10}\right\rfloor
$$

Java:

~~~java
n /= 10;
~~~

### Reverse Number

$$
reverse=reverse\times10+digit
$$

### Sentinel Pattern

~~~java
do {
    // process
} while (value != sentinel);
~~~

### Validation Pattern

~~~java
do {
    // read input
} while (invalid);
~~~

### Minimum Executions

$$
\boxed{1}
$$

### Linear Complexity

$$
O(n)
$$

### Logarithmic Complexity

$$
O(\log n)
$$

### Nested Loop

$$
O(n^2)
$$

---

# 41. Quick Revision

> [!summary] One-Minute Revision

~~~text
do while
→ Execute first, check later.

Syntax
→ do { } while (condition);

Important
→ Semicolon after while(condition).

Minimum executions
→ 1.

while
→ May execute 0 times.

do while
→ Always executes at least once.

Best use
→ Menu programs.
→ Input validation.
→ Sentinel-controlled input.
→ Password retry.
→ Any task that must happen once before checking.

Execution order
→ Body → Update → Condition → Repeat.

Menu pattern
→ Show → Read → Process → Check Exit.

Validation pattern
→ Read → Validate → Repeat if invalid.

Sentinel pattern
→ Process → Repeat until sentinel.

Digit pattern
→ digit = n % 10
→ n /= 10

Reverse pattern
→ reverse = reverse * 10 + digit

break
→ Exit loop immediately.

continue
→ Skip current iteration and proceed to condition.

Main danger
→ Infinite loop due to missing update.

Classic exam trick
→ Condition can be false initially, but body still executes once.

One loop
→ O(n)

Repeated halving
→ O(log n)

Nested loops
→ Often O(n²).
~~~

## Golden Memory Trick

**`do while` means: DO the work first, THEN ask whether you should continue.**

## One-Line Recognition

**If the problem requires the operation to happen at least once before checking the condition, use a `do while` loop.**