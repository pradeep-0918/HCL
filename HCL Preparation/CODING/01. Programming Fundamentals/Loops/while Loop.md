---
type: concept
subject: coding
topic: "while Loop"
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
  - while-loop
  - iteration
  - java
  - programming
wikilinks:
  - "[[Loops]]"
  - "[[for Loop]]"
  - "[[do while Loop]]"
  - "[[Nested Loops]]"
  - "[[Conditional Statements]]"
---

# while Loop

## 1. Core Concept

> [!summary]
> A `while` loop repeatedly executes a block of code **as long as a condition remains true**.
>
> It is especially useful when the number of iterations is **not known in advance**.

Basic syntax:

~~~java
while (condition) {
    // statements
}
~~~

Example:

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
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
Initialize
    ↓
Check condition
    ↓
 true?
 ┌──┴──┐
Yes   No
 ↓     ↓
Body   Exit
 ↓
Update
 ↓
Check again
~~~

> [!important]
> A `while` loop checks its condition **before** executing the loop body.

---

# 2. Basic Meaning

Think of `while` as:

~~~text
WHILE this condition is true
→ keep doing this work
~~~

Example:

~~~java
int count = 1;

while (count <= 5) {
    System.out.println(count);
    count++;
}
~~~

The loop continues while:

$$
count\leq5
$$

Once:

$$
count>5
$$

the loop stops.

---

# 3. Syntax

The standard structure is:

~~~java
while (condition) {
    // loop body
}
~~~

Unlike a `for` loop, the initialization and update are usually written separately.

Example:

~~~java
int i = 1;

while (i <= 10) {
    System.out.println(i);
    i++;
}
~~~

Equivalent `for` loop:

~~~java
for (int i = 1; i <= 10; i++) {
    System.out.println(i);
}
~~~

---

# 4. Execution Order

Consider:

~~~java
int i = 1;

while (i <= 3) {
    System.out.println(i);
    i++;
}
~~~

### Step 1

Initialize:

$$
i=1
$$

### Step 2

Check:

$$
1\leq3=true
$$

### Step 3

Print:

~~~text
1
~~~

### Step 4

Update:

$$
i=2
$$

### Step 5

Check:

$$
2\leq3=true
$$

Print:

~~~text
2
~~~

### Step 6

Update:

$$
i=3
$$

### Step 7

Check:

$$
3\leq3=true
$$

Print:

~~~text
3
~~~

### Step 8

Update:

$$
i=4
$$

### Step 9

Check:

$$
4\leq3=false
$$

Loop exits.

### Answer

~~~text
1
2
3
~~~

---

# 5. Important Property — May Execute Zero Times

Because the condition is checked before the body, a `while` loop can execute **zero times**.

Example:

~~~java
int i = 10;

while (i < 5) {
    System.out.println(i);
    i++;
}
~~~

Condition:

$$
10<5=false
$$

The body is never executed.

### Answer

~~~text
No output
~~~

> [!important]
> `while` is a **zero-or-more times** loop.

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

Increase by `1`.

### Code

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
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

# 7. Example — Print N to 1

## Example 2

### Question

Print numbers from `5` down to `1`.

### Pattern

Start at `5`.

Decrease by `1`.

### Code

~~~java
int i = 5;

while (i >= 1) {
    System.out.println(i);
    i--;
}
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

# 8. Example — Print Even Numbers

## Example 3

### Question

Print even numbers from `2` to `10`.

### Pattern

Start at `2`.

Increase by `2`.

### Code

~~~java
int i = 2;

while (i <= 10) {
    System.out.println(i);
    i += 2;
}
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

# 9. Example — Print Odd Numbers

## Example 4

### Question

Print odd numbers from `1` to `10`.

### Code

~~~java
int i = 1;

while (i <= 10) {
    System.out.println(i);
    i += 2;
}
~~~

### Answer

~~~text
1
3
5
7
9
~~~

---

# 10. Example — Sum of Numbers

## Example 5

### Question

Find:

$$
1+2+3+4+5
$$

### Pattern

Use a running sum.

### Code

~~~java
int i = 1;
int sum = 0;

while (i <= 5) {
    sum += i;
    i++;
}

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

# 11. Example — Multiplication Table

## Example 6

### Question

Print the table of `7`.

### Code

~~~java
int n = 7;
int i = 1;

while (i <= 10) {
    System.out.println(n + " x " + i + " = " + (n * i));
    i++;
}
~~~

Output:

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

# 12. Example — Count Digits

## Example 7

### Question

Count the digits in:

$$
n=58342
$$

### Pattern

Repeatedly remove the last digit using:

$$
n=n/10
$$

until the number becomes zero.

### Code

~~~java
int n = 58342;
int count = 0;

while (n > 0) {
    count++;
    n /= 10;
}

System.out.println(count);
~~~

Trace:

~~~text
58342 → 5834
5834  → 583
583   → 58
58    → 5
5     → 0
~~~

Number of iterations:

$$
5
$$

### Answer

$$
\boxed{5}
$$

> [!important]
> This is a classic case where `while` is more natural than `for` because the number of iterations depends on the value being reduced.

---

# 13. Example — Reverse a Number

## Example 8

### Question

Reverse:

$$
12345
$$

### Pattern

Repeatedly:

1. Extract last digit.
2. Add it to the reversed number.
3. Remove the last digit.

Formulas:

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

while (n > 0) {

    int digit = n % 10;

    reverse = reverse * 10 + digit;

    n /= 10;
}

System.out.println(reverse);
~~~

Trace:

~~~text
n = 12345
digit = 5
reverse = 5

n = 1234
digit = 4
reverse = 54

n = 123
digit = 3
reverse = 543

n = 12
digit = 2
reverse = 5432

n = 1
digit = 1
reverse = 54321
~~~

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

### Pattern

Reverse the number and compare it with the original.

### Code

~~~java
int n = 121;
int original = n;
int reverse = 0;

while (n > 0) {

    int digit = n % 10;

    reverse = reverse * 10 + digit;

    n /= 10;
}

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

Therefore:

$$
original=reverse
$$

### Answer

$$
\boxed{Palindrome}
$$

---

# 15. Example — Sum of Digits

## Example 10

### Question

Find the sum of digits of:

$$
5832
$$

### Pattern

Extract digits repeatedly.

### Code

~~~java
int n = 5832;
int sum = 0;

while (n > 0) {

    int digit = n % 10;

    sum += digit;

    n /= 10;
}

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

---

# 16. Example — Digit Frequency

## Example 11

### Question

Count how many times digit `2` occurs in:

$$
122232
$$

### Pattern

Extract each digit and compare.

### Code

~~~java
int n = 122232;
int target = 2;
int count = 0;

while (n > 0) {

    int digit = n % 10;

    if (digit == target) {
        count++;
    }

    n /= 10;
}

System.out.println(count);
~~~

Digits:

~~~text
1 2 2 2 3 2
~~~

Number of `2`s:

$$
4
$$

### Answer

$$
\boxed{4}
$$

---

# 17. Example — GCD Using Euclidean Algorithm

## Example 12

### Question

Find:

$$
GCD(48,18)
$$

### Pattern

Use:

$$
a,b\rightarrow b,a\%b
$$

until:

$$
b=0
$$

### Code

~~~java
int a = 48;
int b = 18;

while (b != 0) {

    int temp = b;
    b = a % b;
    a = temp;
}

System.out.println(a);
~~~

Trace:

$$
48\%18=12
$$

Then:

$$
18\%12=6
$$

Then:

$$
12\%6=0
$$

Therefore:

$$
GCD=6
$$

### Answer

$$
\boxed{6}
$$

> [!important]
> The Euclidean algorithm is one of the most important practical uses of a `while` loop.

---

# 18. Example — Read Until Sentinel

## Example 13

### Question

Keep processing numbers until the user enters `-1`.

### Pattern

The number of inputs is unknown.

Use a sentinel value.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int n = sc.nextInt();

while (n != -1) {

    System.out.println("Processing: " + n);

    n = sc.nextInt();
}
~~~

The loop continues while:

$$
n\neq-1
$$

When:

$$
n=-1
$$

the loop stops.

> [!important]
> **Unknown number of iterations + stopping value** is a classic `while` loop pattern.

---

# 19. Example — Input Validation

## Example 14

### Question

Continue asking for a positive number until the user enters one.

### Code

~~~java
Scanner sc = new Scanner(System.in);

int n = sc.nextInt();

while (n <= 0) {

    System.out.println("Enter a positive number:");

    n = sc.nextInt();
}

System.out.println("Valid input");
~~~

The loop continues while:

$$
n\leq0
$$

It stops when:

$$
n>0
$$

### Pattern

~~~text
Invalid input
      ↓
Ask again
      ↓
Check
      ↓
Valid?
      ↓
Continue program
~~~

---

# 20. Example — Find First Divisible Number

## Example 15

### Question

Starting from `1`, find the first number divisible by both `7` and `11`.

### Pattern

Search until a condition becomes true.

### Code

~~~java
int n = 1;

while (!(n % 7 == 0 && n % 11 == 0)) {
    n++;
}

System.out.println(n);
~~~

A number divisible by both `7` and `11` is:

$$
LCM(7,11)=77
$$

Therefore:

### Answer

$$
\boxed{77}
$$

---

# 21. Example — Power of Two

## Example 16

### Question

Determine whether `64` is a power of `2`.

### Pattern

Repeatedly divide by `2`.

### Code

~~~java
int n = 64;

while (n > 1 && n % 2 == 0) {
    n /= 2;
}

if (n == 1) {
    System.out.println("Power of Two");
} else {
    System.out.println("Not Power of Two");
}
~~~

Trace:

~~~text
64 → 32 → 16 → 8 → 4 → 2 → 1
~~~

Therefore:

### Answer

$$
\boxed{Power\ of\ Two}
$$

---

# 22. while Loop with break

`break` immediately terminates the loop.

Example:

~~~java
int i = 1;

while (i <= 10) {

    if (i == 6) {
        break;
    }

    System.out.println(i);

    i++;
}
~~~

When:

$$
i=6
$$

the loop exits.

Output:

~~~text
1
2
3
4
5
~~~

> [!important]
> `break` means **terminate the entire loop immediately**.

---

# 23. while Loop with continue

`continue` skips the current iteration.

Example:

~~~java
int i = 0;

while (i < 5) {

    i++;

    if (i == 3) {
        continue;
    }

    System.out.println(i);
}
~~~

Output:

~~~text
1
2
4
5
~~~

When `i == 3`, the current iteration is skipped.

> [!important]
> Be careful with `continue` in a `while` loop. The update must still happen, otherwise the loop may become infinite.

---

# 24. Infinite while Loop

A `while` loop becomes infinite when its condition never becomes false.

Example:

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
}
~~~

The value of `i` never changes.

Therefore:

$$
i=1
$$

forever.

The condition:

$$
1\leq5
$$

always remains true.

> [!warning]
> Always check how the loop variable or state changes inside a `while` loop.

---

# 25. Example — Correct vs Infinite Loop

### Infinite

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
}
~~~

### Correct

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
~~~

The update:

~~~java
i++;
~~~

moves the loop toward termination.

---

# 26. while vs for

Both can perform repeated execution.

### for

Best when the iteration structure is known.

~~~java
for (int i = 1; i <= 10; i++) {
}
~~~

### while

Best when termination depends on a condition or changing state.

~~~java
while (n != -1) {
}
~~~

### Comparison

| Feature | `for` | `while` |
|---|---|---|
| Known iteration count | Excellent | Possible |
| Unknown iteration count | Possible | Excellent |
| Initialization | Usually inside header | Usually before loop |
| Update | Usually in header | Usually inside body |
| Input until sentinel | Possible | Natural |
| Digit processing | Possible | Natural |
| Search until condition | Possible | Natural |
| Infinite loop | `for(;;)` | `while(true)` |

---

# 27. Recognition Tricks

> [!important]
> If the number of iterations is **known**, think:
>
> `for` loop.

> [!important]
> If the number of iterations is **unknown**, think:
>
> `while` loop.

> [!important]
> If the problem says **"until"**, think `while`.
>
> Examples:
>
> ```text
> until user enters -1
> until number becomes 0
> until password is correct
> until target is found
> ```

> [!important]
> If a value is repeatedly reduced:
>
> ```text
> n → n / 10
> ```
>
> think `while`.

> [!important]
> If digits must be processed one by one, think:
>
> ```text
> while (n > 0)
> ```

> [!important]
> If the loop stops when a special value appears, think **sentinel-controlled while loop**.

> [!important]
> If input must be valid before continuing, think:
>
> ```text
> while (input is invalid)
>     read again
> ```

---

# 28. Shortcuts

> [!tip]
> **Shortcut: Unknown Repetitions**
>
> If you cannot determine the exact number of iterations before execution:
>
> $$\boxed{while}$$

> [!tip]
> **Shortcut: "Until"**
>
> Question contains:
>
> ```text
> until
> ```
>
> immediately consider:
>
> ```java
> while (...)
> ```

> [!tip]
> **Shortcut: Digit Problems**
>
> For:
>
> ```text
> count digits
> sum digits
> reverse number
> palindrome
> digit frequency
> ```
>
> remember:
>
> ~~~java
> while (n > 0) {
>     int digit = n % 10;
>     n /= 10;
> }
> ~~~

> [!tip]
> **Shortcut: Sentinel**
>
> If a problem says:
>
> ```text
> continue until X
> ```
>
> use:
>
> ~~~java
> while (value != X) {
> }
> ~~~

> [!tip]
> **Shortcut: Repeated Division**
>
> If:
>
> $$n\rightarrow\frac{n}{2}$$
>
> or:
>
> $$n\rightarrow\frac{n}{10}$$
>
> happens repeatedly, a `while` loop is often natural.

---

# 29. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Count Digits

~~~java
while (n > 0) {
    count++;
    n /= 10;
}
~~~

### Pattern 2 — Sum Digits

~~~java
while (n > 0) {
    sum += n % 10;
    n /= 10;
}
~~~

### Pattern 3 — Reverse Number

~~~java
while (n > 0) {
    int digit = n % 10;
    reverse = reverse * 10 + digit;
    n /= 10;
}
~~~

### Pattern 4 — Palindrome

~~~text
Original
   ↓
Reverse
   ↓
Compare
~~~

### Pattern 5 — GCD

~~~java
while (b != 0) {
    int temp = b;
    b = a % b;
    a = temp;
}
~~~

### Pattern 6 — Sentinel Input

~~~java
while (value != sentinel) {
    // process
}
~~~

### Pattern 7 — Input Validation

~~~java
while (inputIsInvalid) {
    // read again
}
~~~

### Pattern 8 — Search Until Found

~~~java
while (!found) {
    // continue searching
}
~~~

### Pattern 9 — Repeated Reduction

~~~java
while (n > 1) {
    n /= 2;
}
~~~

### Pattern 10 — Menu Until Exit

~~~java
while (choice != 0) {
    // process choice
}
~~~

---

# 30. Time Complexity

## Linear while Loop

~~~java
int i = 0;

while (i < n) {
    i++;
}
~~~

Number of iterations:

$$
n
$$

Time:

$$
\boxed{O(n)}
$$

---

## Logarithmic while Loop

~~~java
int n = 100;

while (n > 1) {
    n /= 2;
}
~~~

Each iteration halves the value.

Therefore:

$$
\boxed{O(\log n)}
$$

---

## Nested while Loops

~~~java
int i = 0;

while (i < n) {

    int j = 0;

    while (j < n) {
        j++;
    }

    i++;
}
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

# 31. Space Complexity

A basic `while` loop usually uses constant extra memory.

Example:

~~~java
int i = 0;

while (i < n) {
    i++;
}
~~~

Extra variables are constant.

Therefore:

$$
\boxed{O(1)}
$$

> [!important]
> Loop count affects **time complexity**, not necessarily space complexity.

---

# 32. Advanced Pattern — Two-Pointer while Loop

A common DSA pattern uses two pointers.

Example:

~~~java
int left = 0;
int right = arr.length - 1;

while (left < right) {

    if (arr[left] + arr[right] == target) {
        break;
    }

    if (arr[left] + arr[right] < target) {
        left++;
    } else {
        right--;
    }
}
~~~

This pattern appears in:

- Two Sum on sorted arrays
- Pair search
- Palindrome checking
- Partitioning
- Sliding-window style algorithms

Typical complexity:

$$
\boxed{O(n)}
$$

when each pointer moves only forward or backward through the array.

---

# 33. Advanced Pattern — Two Pointer Palindrome

## Example 17

### Question

Check whether a string is a palindrome.

### Code

~~~java
String s = "madam";

int left = 0;
int right = s.length() - 1;

boolean palindrome = true;

while (left < right) {

    if (s.charAt(left) != s.charAt(right)) {
        palindrome = false;
        break;
    }

    left++;
    right--;
}

System.out.println(palindrome);
~~~

Comparisons:

~~~text
m == m
a == a
d == d
~~~

Therefore:

### Answer

$$
\boxed{true}
$$

---

# 34. Advanced Pattern — Read Until EOF

In some coding environments, input may continue until there is no more input.

The exact Java implementation depends on the input source.

For a `Scanner`, a conceptual pattern is:

~~~java
while (sc.hasNextInt()) {
    int n = sc.nextInt();
    // process n
}
~~~

This is useful when the number of input values is not specified.

> [!important]
> Always follow the input format provided by the coding platform. Do not assume EOF-based input unless the problem statement supports it.

---

# 35. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting the Update

Wrong:

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
}
~~~

The condition never becomes false.

Correct:

~~~java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
~~~

---

### Mistake 2 — Updating in the Wrong Direction

Wrong:

~~~java
int i = 5;

while (i >= 1) {
    System.out.println(i);
    i++;
}
~~~

`i` increases:

$$
5,6,7,8,\ldots
$$

so:

$$
i\geq1
$$

remains true.

Correct:

~~~java
i--;
~~~

---

### Mistake 3 — Off-by-One Error

Consider:

~~~java
int i = 1;

while (i < 5) {
    System.out.println(i);
    i++;
}
~~~

Output:

~~~text
1
2
3
4
~~~

It does not print `5`.

To include `5`:

~~~java
while (i <= 5) {
}
~~~

---

### Mistake 4 — Updating Before Processing

Compare:

~~~java
while (i <= 5) {
    System.out.println(i);
    i++;
}
~~~

with:

~~~java
while (i <= 5) {
    i++;
    System.out.println(i);
}
~~~

The second version starts printing from `2`.

Always trace the order carefully.

---

### Mistake 5 — Incorrect continue

Dangerous:

~~~java
int i = 1;

while (i <= 5) {

    if (i == 3) {
        continue;
    }

    i++;
}
~~~

When `i == 3`, `continue` happens before `i++`.

Therefore `i` remains `3` forever.

Correct:

~~~java
int i = 1;

while (i <= 5) {

    i++;

    if (i == 3) {
        continue;
    }

    System.out.println(i);
}
~~~

or structure the update so it always occurs before continuing.

---

### Mistake 6 — Modifying the Wrong Variable

Wrong:

~~~java
int i = 1;
int j = 10;

while (i <= 5) {
    System.out.println(i);
    j++;
}
~~~

`i` never changes.

The loop condition depends on `i`, so the loop may become infinite.

---

### Mistake 7 — Changing the Original Number Too Early

For palindrome or reverse problems, preserve the original value.

Correct:

~~~java
int original = n;
~~~

Then modify `n`.

---

### Mistake 8 — Assuming while Always Runs Once

It may run zero times.

Example:

~~~java
int n = 10;

while (n < 5) {
    System.out.println(n);
}
~~~

The condition is initially false.

---

# 36. for vs while Recognition Table

| Question Pattern | Best First Thought |
|---|---|
| Print 1 to 100 | `for` |
| Print table 1 to 10 | `for` |
| Traverse array | `for` |
| Repeat exactly N times | `for` |
| Read until `-1` | `while` |
| Count digits | `while` |
| Reverse number | `while` |
| Sum digits | `while` |
| GCD Euclidean algorithm | `while` |
| Validate input until valid | `while` |
| Search until target found | `while` |
| Two-pointer traversal | `while` |

> [!tip]
> This is not a strict rule. Both loops can often solve the same problem. Choose the structure that makes the stopping logic easiest to understand.

---

# 37. Formula Sheet

### Basic while

~~~java
while (condition) {
    // body
}
~~~

### Increasing

~~~java
int i = start;

while (i <= end) {
    // body
    i++;
}
~~~

### Decreasing

~~~java
int i = start;

while (i >= end) {
    // body
    i--;
}
~~~

### Even Numbers

~~~java
int i = 2;

while (i <= n) {
    // body
    i += 2;
}
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

### GCD

$$
(a,b)\rightarrow(b,a\%b)
$$

until:

$$
b=0
$$

### Linear Loop

$$
O(n)
$$

### Halving Loop

$$
O(\log n)
$$

### Nested Loop

$$
O(n^2)
$$

---

# 38. Quick Revision

> [!summary] One-Minute Revision

~~~text
while loop
→ Repeat while condition is true.

Syntax
→ while (condition) { }

Execution
→ Check condition → Execute → Update → Repeat.

Condition checked
→ Before every iteration.

Zero iterations
→ Possible if condition is initially false.

Known iterations
→ for is usually natural.

Unknown iterations
→ while is usually natural.

"Until"
→ Think while.

Sentinel
→ Continue until a special value appears.

Digit problems
→ while (n > 0)

Extract digit
→ n % 10

Remove digit
→ n /= 10

Reverse number
→ reverse = reverse * 10 + digit

GCD
→ while (b != 0)

break
→ Exit entire loop.

continue
→ Skip current iteration.

Infinite loop
→ Condition never becomes false.

Main danger
→ Forgetting to update the variable controlling the condition.

One loop
→ O(n)

Repeated halving/division
→ O(log n)

Nested loops
→ Often O(n²).

Two pointers
→ while (left < right) is a common pattern.
~~~

## Golden Memory Trick

**`while` means: "Keep doing this while the condition is true; stop when it becomes false."**

## One-Line Recognition

**When the number of repetitions is not fixed and the loop should continue until a condition changes, think `while` loop.**
