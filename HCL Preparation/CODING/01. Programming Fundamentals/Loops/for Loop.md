---
type: concept
subject: coding
topic: "for Loop"
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
  - for-loop
  - iteration
  - java
  - programming
wikilinks:
  - "[[Loops]]"
  - "[[while Loop]]"
  - "[[do while Loop]]"
  - "[[Nested Loops]]"
  - "[[Conditional Statements]]"
---

# for Loop

## 1. Core Concept

> [!summary]
> A `for` loop is used to **repeat a block of code a known number of times** or while a condition remains true.
>
> The basic structure contains three parts:
>
> **Initialization → Condition → Update**

Basic syntax:

~~~java
for (initialization; condition; update) {
    // statements
}
~~~

Example:

~~~java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
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

The loop follows:

~~~text
Initialize i
    ↓
Check condition
    ↓
  true
    ↓
Execute body
    ↓
Update i
    ↓
Check condition again
    ↓
  false
    ↓
Exit loop
~~~

---

# 2. Basic Meaning

A loop allows us to execute the same block of code repeatedly without writing it multiple times.

Without a loop:

~~~java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);
~~~

With a loop:

~~~java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
~~~

Both produce:

~~~text
1
2
3
4
5
~~~

But the loop is shorter, cleaner, and easier to modify.

> [!important]
> Whenever a task says **repeat something multiple times**, think about using a loop.

---

# 3. Main Structure of a for Loop

The three sections are:

~~~java
for (initialization; condition; update) {
    // body
}
~~~

### 1. Initialization

Runs once at the beginning.

Example:

~~~java
int i = 1;
~~~

### 2. Condition

Checked before every iteration.

Example:

~~~java
i <= 5
~~~

### 3. Update

Runs after each iteration.

Example:

~~~java
i++
~~~

---

# 4. Execution Order

Consider:

~~~java
for (int i = 1; i <= 3; i++) {
    System.out.println(i);
}
~~~

Execution:

### Step 1

Initialize:

$$
i=1
$$

### Step 2

Check:

$$
1\leq3
$$

True.

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
2\leq3
$$

True.

### Step 6

Print:

~~~text
2
~~~

### Step 7

Update:

$$
i=3
$$

### Step 8

Check:

$$
3\leq3
$$

True.

### Step 9

Print:

~~~text
3
~~~

### Step 10

Update:

$$
i=4
$$

### Step 11

Check:

$$
4\leq3
$$

False.

Loop terminates.

### Answer

~~~text
1
2
3
~~~

---

# 5. Basic Example — Print Numbers

## Example 1

### Question

Print numbers from `1` to `10`.

### Pattern

Start:

$$
1
$$

End:

$$
10
$$

Increment:

$$
+1
$$

### Code

~~~java
for (int i = 1; i <= 10; i++) {
    System.out.println(i);
}
~~~

### Answer

~~~text
1
2
3
4
5
6
7
8
9
10
~~~

---

# 6. Basic Example — Print Even Numbers

## Example 2

### Question

Print even numbers from `2` to `10`.

### Pattern

Start at `2` and increase by `2`.

### Code

~~~java
for (int i = 2; i <= 10; i += 2) {
    System.out.println(i);
}
~~~

Sequence:

$$
2,4,6,8,10
$$

### Answer

~~~text
2
4
6
8
10
~~~

> [!tip]
> If every required number increases by a fixed amount, change the update expression instead of checking every number.

---

# 7. Basic Example — Print Odd Numbers

## Example 3

### Question

Print odd numbers from `1` to `10`.

### Pattern

Start at `1`, increment by `2`.

### Code

~~~java
for (int i = 1; i <= 10; i += 2) {
    System.out.println(i);
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

# 8. Counting Iterations

## Example 4

### Question

How many times does this loop execute?

~~~java
for (int i = 1; i <= 20; i++) {
    System.out.println(i);
}
~~~

The values are:

$$
1,2,3,\ldots,20
$$

Number of iterations:

$$
20
$$

### Answer

$$
\boxed{20}
$$

---

# 9. Important Iteration Formula

When a loop runs from `start` to `end`, inclusive, with step `1`:

$$
\text{Iterations}=end-start+1
$$

Example:

~~~java
for (int i = 5; i <= 15; i++) {
}
~~~

Therefore:

$$
15-5+1=11
$$

### Answer

$$
\boxed{11}
$$

> [!tip]
> This formula is extremely useful for quickly solving loop-tracing and output questions.

---

# 10. Iterations with Step

Suppose:

~~~java
for (int i = 2; i <= 20; i += 3) {
}
~~~

Values:

$$
2,5,8,11,14,17,20
$$

There are:

$$
7
$$

iterations.

General idea:

$$
\text{Iterations}
=
\left\lfloor
\frac{end-start}{step}
\right\rfloor+1
$$

when the loop starts at `start`, increases by a positive `step`, and the final value satisfying the condition is included.

---

# 11. Example — Sum of Numbers

## Example 5

### Question

Find the sum of numbers from `1` to `10`.

### Pattern

Repeated addition.

### Code

~~~java
int sum = 0;

for (int i = 1; i <= 10; i++) {
    sum += i;
}

System.out.println(sum);
~~~

Calculation:

$$
1+2+3+\cdots+10
$$

Using the arithmetic series formula:

$$
\frac{n(n+1)}{2}
$$

For:

$$
n=10
$$

we get:

$$
\frac{10(11)}{2}=55
$$

### Answer

$$
\boxed{55}
$$

---

# 12. Example — Sum of Even Numbers

## Example 6

### Question

Find the sum of even numbers from `2` to `20`.

### Pattern

Start at `2`, increment by `2`.

### Code

~~~java
int sum = 0;

for (int i = 2; i <= 20; i += 2) {
    sum += i;
}

System.out.println(sum);
~~~

Calculation:

$$
2+4+6+\cdots+20
$$

There are:

$$
10
$$

even numbers.

Using:

$$
\text{Sum}=\frac{n(first+last)}{2}
$$

we get:

$$
\frac{10(2+20)}{2}
$$

$$
=110
$$

### Answer

$$
\boxed{110}
$$

---

# 13. Example — Multiplication Table

## Example 7

### Question

Print the multiplication table of `7` from `1` to `10`.

### Pattern

Repeated multiplication.

### Code

~~~java
int n = 7;

for (int i = 1; i <= 10; i++) {
    System.out.println(n + " x " + i + " = " + (n * i));
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

### Answer

$$
\boxed{7\times1\text{ through }7\times10}
$$

---

# 14. Example — Factorial

## Example 8

### Question

Find:

$$
5!
$$

### Formula

$$
n!=n(n-1)(n-2)\cdots1
$$

### Code

~~~java
int n = 5;
long fact = 1;

for (int i = 1; i <= n; i++) {
    fact *= i;
}

System.out.println(fact);
~~~

Calculation:

$$
5!=1\times2\times3\times4\times5
$$

$$
=120
$$

### Answer

$$
\boxed{120}
$$

> [!warning]
> Factorials grow very quickly. For larger values, `int` may overflow. Use an appropriate numeric type or `BigInteger` when necessary.

---

# 15. Example — Count Digits

## Example 9

### Question

Count the number of digits in:

$$
n=58342
$$

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

This particular problem is naturally solved with a `while` loop because the number of iterations depends on the changing digits.

However, if the problem gives a known range of positions or digits, a `for` loop may be appropriate.

> [!important]
> Do not force every repetition problem into a `for` loop. Choose the loop structure based on the problem.

---

# 16. Example — Reverse Loop

## Example 10

### Question

Print numbers from `10` down to `1`.

### Pattern

Start high and decrease.

### Code

~~~java
for (int i = 10; i >= 1; i--) {
    System.out.println(i);
}
~~~

### Answer

~~~text
10
9
8
7
6
5
4
3
2
1
~~~

> [!tip]
> Increasing loop:
>
> ~~~java
> i++
> ~~~
>
> Decreasing loop:
>
> ~~~java
> i--
> ~~~

---

# 17. Example — Sum from N to 1

## Example 11

### Question

Find:

$$
5+4+3+2+1
$$

### Code

~~~java
int n = 5;
int sum = 0;

for (int i = n; i >= 1; i--) {
    sum += i;
}

System.out.println(sum);
~~~

Calculation:

$$
5+4+3+2+1=15
$$

### Answer

$$
\boxed{15}
$$

---

# 18. Example — Count Multiples

## Example 12

### Question

Count numbers between `1` and `100` that are divisible by `5`.

### Pattern

Multiples of `5`:

$$
5,10,15,\ldots,100
$$

### Efficient loop

~~~java
int count = 0;

for (int i = 5; i <= 100; i += 5) {
    count++;
}

System.out.println(count);
~~~

Number of multiples:

$$
\frac{100}{5}=20
$$

### Answer

$$
\boxed{20}
$$

> [!tip]
> Instead of checking every number with `%`, directly iterate through multiples when appropriate.

---

# 19. Example — Search an Array

## Example 13

### Question

Check whether `25` exists in an array.

~~~text
10 15 20 25 30
~~~

### Pattern

Array traversal + comparison.

### Code

~~~java
int[] arr = {10, 15, 20, 25, 30};
int target = 25;

boolean found = false;

for (int i = 0; i < arr.length; i++) {

    if (arr[i] == target) {
        found = true;
        break;
    }
}

System.out.println(found);
~~~

When:

$$
arr[i]=25
$$

the target is found.

### Answer

$$
\boxed{true}
$$

> [!important]
> `break` is useful here because there is no need to continue searching after finding the target.

---

# 20. Example — Find Maximum in Array

## Example 14

### Question

Find the largest element:

~~~text
8 3 15 6 10
~~~

### Pattern

Maintain a running maximum.

### Code

~~~java
int[] arr = {8, 3, 15, 6, 10};

int max = arr[0];

for (int i = 1; i < arr.length; i++) {

    if (arr[i] > max) {
        max = arr[i];
    }
}

System.out.println(max);
~~~

Trace:

~~~text
max = 8
15 > 8  → max = 15
6 > 15  → false
10 > 15 → false
~~~

### Answer

$$
\boxed{15}
$$

---

# 21. Example — Count Even Numbers in Array

## Example 15

### Question

Count even numbers in:

~~~text
2 7 4 9 10 11
~~~

### Pattern

Traverse array and test:

$$
arr[i]\%2=0
$$

### Code

~~~java
int[] arr = {2, 7, 4, 9, 10, 11};

int count = 0;

for (int i = 0; i < arr.length; i++) {

    if (arr[i] % 2 == 0) {
        count++;
    }
}

System.out.println(count);
~~~

Even numbers:

~~~text
2, 4, 10
~~~

Therefore:

$$
count=3
$$

### Answer

$$
\boxed{3}
$$

---

# 22. for Loop with Multiple Variables

A `for` loop can contain multiple initialization or update expressions.

Example:

~~~java
for (int i = 1, j = 10; i <= 5; i++, j--) {
    System.out.println(i + " " + j);
}
~~~

Output:

~~~text
1 10
2 9
3 8
4 7
5 6
~~~

This is useful when two values must change together.

> [!warning]
> Multiple variables can make code harder to read. Use them only when they make the logic clearer.

---

# 23. Infinite for Loop

A `for` loop can omit its three components.

Example:

~~~java
for (;;) {
    System.out.println("Running");
}
~~~

This creates an infinite loop.

Equivalent concept:

~~~java
while (true) {
    System.out.println("Running");
}
~~~

To terminate an intentional infinite loop, a condition or `break` is usually required.

Example:

~~~java
for (;;) {

    if (condition) {
        break;
    }
}
~~~

> [!warning]
> An accidental infinite loop can cause a program to hang or produce a Time Limit Exceeded error.

---

# 24. for Loop Without Initialization

Initialization can happen before the loop.

~~~java
int i = 1;

for (; i <= 5; i++) {
    System.out.println(i);
}
~~~

This is valid Java.

However, the standard form is usually clearer:

~~~java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
~~~

---

# 25. for Loop Without Update

The update can be written inside the loop.

~~~java
for (int i = 1; i <= 5;) {

    System.out.println(i);

    i++;
}
~~~

This is valid but generally less readable than:

~~~java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
~~~

---

# 26. break in for Loop

`break` immediately terminates the loop.

Example:

~~~java
for (int i = 1; i <= 10; i++) {

    if (i == 6) {
        break;
    }

    System.out.println(i);
}
~~~

Execution stops when:

$$
i=6
$$

Output:

~~~text
1
2
3
4
5
~~~

> [!important]
> `break` means:
>
> **"Stop the loop completely."**

---

# 27. continue in for Loop

`continue` skips the current iteration and moves to the next iteration.

Example:

~~~java
for (int i = 1; i <= 5; i++) {

    if (i == 3) {
        continue;
    }

    System.out.println(i);
}
~~~

When:

$$
i=3
$$

the print statement is skipped.

Output:

~~~text
1
2
4
5
~~~

> [!important]
> `break` → exit loop.
>
> `continue` → skip current iteration.

---

# 28. Example — Skip Multiples of 3

## Example 16

### Question

Print numbers from `1` to `10`, excluding multiples of `3`.

### Code

~~~java
for (int i = 1; i <= 10; i++) {

    if (i % 3 == 0) {
        continue;
    }

    System.out.println(i);
}
~~~

Skipped:

$$
3,6,9
$$

### Answer

~~~text
1
2
4
5
7
8
10
~~~

---

# 29. Nested for Loops

A `for` loop can contain another `for` loop.

Example:

~~~java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 3; j++) {
        System.out.println(i + " " + j);
    }
}
~~~

For every value of `i`, the inner loop runs completely.

Execution:

~~~text
i = 1 → j = 1,2,3
i = 2 → j = 1,2,3
i = 3 → j = 1,2,3
~~~

Total executions:

$$
3\times3=9
$$

> [!important]
> Nested loops are extremely important for pattern printing, matrix problems, pair problems, and many coding interview questions.

---

# 30. Example — Rectangle Pattern

## Example 17

### Question

Print:

~~~text
* * * *
* * * *
* * * *
~~~

### Pattern

3 rows × 4 columns.

### Code

~~~java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 4; j++) {
        System.out.print("* ");
    }

    System.out.println();
}
~~~

### Answer

~~~text
* * * *
* * * *
* * * *
~~~

Number of stars:

$$
3\times4=12
$$

### Answer

$$
\boxed{12\ stars}
$$

---

# 31. Example — Triangle Pattern

## Example 18

### Question

Print:

~~~text
*
* *
* * *
* * * *
~~~

### Pattern

Row number = number of stars.

### Code

~~~java
for (int i = 1; i <= 4; i++) {

    for (int j = 1; j <= i; j++) {
        System.out.print("* ");
    }

    System.out.println();
}
~~~

Observe:

~~~text
row 1 → 1 star
row 2 → 2 stars
row 3 → 3 stars
row 4 → 4 stars
~~~

### Answer

~~~text
*
* *
* * *
* * * *
~~~

> [!important]
> In many pattern problems, the inner loop limit depends on the outer loop variable.

---

# 32. Example — Multiplication Table Grid

## Example 19

### Question

Print multiplication values from `1 × 1` to `3 × 3`.

### Code

~~~java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 3; j++) {
        System.out.print((i * j) + " ");
    }

    System.out.println();
}
~~~

Output:

~~~text
1 2 3
2 4 6
3 6 9
~~~

Each pair `(i, j)` is processed.

Total operations:

$$
3\times3=9
$$

---

# 33. Time Complexity of for Loops

Consider:

~~~java
for (int i = 0; i < n; i++) {
    System.out.println(i);
}
~~~

The loop runs approximately `n` times.

Therefore:

$$
\boxed{O(n)}
$$

### Constant Work Inside Loop

~~~java
for (int i = 0; i < n; i++) {
    x++;
}
~~~

Time:

$$
O(n)
$$

---

# 34. Two Separate for Loops

Consider:

~~~java
for (int i = 0; i < n; i++) {
}

for (int j = 0; j < n; j++) {
}
~~~

The total work is:

$$
n+n=2n
$$

Ignore constants:

$$
\boxed{O(n)}
$$

> [!important]
> Sequential loops are generally **added**, not multiplied.

---

# 35. Nested Loop Complexity

Consider:

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < n; j++) {
    }
}
~~~

The outer loop runs:

$$
n
$$

times.

For each outer iteration, the inner loop runs:

$$
n
$$

times.

Total:

$$
n\times n=n^2
$$

Therefore:

$$
\boxed{O(n^2)}
$$

---

# 36. Different Nested Loop Bounds

Consider:

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < i; j++) {
    }
}
~~~

Inner iterations:

~~~text
i = 0 → 0
i = 1 → 1
i = 2 → 2
...
i = n-1 → n-1
~~~

Total:

$$
0+1+2+\cdots+(n-1)
$$

$$
=\frac{n(n-1)}{2}
$$

Therefore:

$$
\boxed{O(n^2)}
$$

> [!important]
> Even when the inner loop does not run `n` times every time, the total can still be quadratic.

---

# 37. Logarithmic for Loop

Consider:

~~~java
for (int i = 1; i <= n; i *= 2) {
    System.out.println(i);
}
~~~

Values:

$$
1,2,4,8,16,\ldots
$$

The number of iterations is approximately:

$$
\log_2 n
$$

Therefore:

$$
\boxed{O(\log n)}
$$

> [!tip]
> If the loop variable is repeatedly multiplied or divided by a constant, think **logarithmic complexity**.

---

# 38. Example — Powers of Two

## Example 20

### Question

How many iterations?

~~~java
for (int i = 1; i <= 100; i *= 2) {
    System.out.println(i);
}
~~~

Values:

~~~text
1
2
4
8
16
32
64
~~~

Next:

$$
128>100
$$

So the loop stops.

There are:

$$
7
$$

iterations.

### Answer

$$
\boxed{7}
$$

---

# 39. Pattern Recognition

> [!important]
> If the question says **"from 1 to N"**, think:
>
> ~~~java
> for (int i = 1; i <= n; i++)
> ~~~

> [!important]
> If the question says **"from N to 1"**, think:
>
> ~~~java
> for (int i = n; i >= 1; i--)
> ~~~

> [!important]
> If the question says **"even numbers"**, think:
>
> ~~~java
> for (int i = 2; i <= n; i += 2)
> ~~~

> [!important]
> If the question says **"odd numbers"**, think:
>
> ~~~java
> for (int i = 1; i <= n; i += 2)
> ~~~

> [!important]
> If the question says **"repeat N times"**, think:
>
> ~~~java
> for (int i = 0; i < n; i++)
> ~~~

> [!important]
> If the question says **"every multiple of K"**, think:
>
> ~~~java
> for (int i = k; i <= n; i += k)
> ~~~

> [!important]
> If the question involves **rows and columns**, think:
>
> **Nested `for` loops.**

> [!important]
> If the loop variable doubles:
>
> ~~~java
> i *= 2
> ~~~
>
> think:
>
> $$O(\log n)$$

---

# 40. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Print 1 to N

~~~java
for (int i = 1; i <= n; i++) {
    System.out.println(i);
}
~~~

### Pattern 2 — Print N to 1

~~~java
for (int i = n; i >= 1; i--) {
    System.out.println(i);
}
~~~

### Pattern 3 — Sum 1 to N

~~~java
int sum = 0;

for (int i = 1; i <= n; i++) {
    sum += i;
}
~~~

### Pattern 4 — Even Numbers

~~~java
for (int i = 2; i <= n; i += 2) {
}
~~~

### Pattern 5 — Odd Numbers

~~~java
for (int i = 1; i <= n; i += 2) {
}
~~~

### Pattern 6 — Multiples

~~~java
for (int i = k; i <= n; i += k) {
}
~~~

### Pattern 7 — Factorial

~~~java
long fact = 1;

for (int i = 1; i <= n; i++) {
    fact *= i;
}
~~~

### Pattern 8 — Array Traversal

~~~java
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
~~~

### Pattern 9 — Maximum in Array

~~~java
int max = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
        max = arr[i];
    }
}
~~~

### Pattern 10 — Pattern Printing

~~~java
for (int i = 1; i <= rows; i++) {

    for (int j = 1; j <= columns; j++) {
        // print
    }

    System.out.println();
}
~~~

---

# 41. Shortcuts

> [!tip]
> **Shortcut: 1 to N**
>
> Instead of thinking about every iteration:
>
> $$1,2,3,\ldots,N$$
>
> immediately recognize:
>
> ~~~java
> for (int i = 1; i <= n; i++)
> ~~~

> [!tip]
> **Shortcut: N to 1**
>
> ~~~java
> for (int i = n; i >= 1; i--)
> ~~~

> [!tip]
> **Shortcut: Even Numbers**
>
> Start at `2` and step by `2`.
>
> ~~~java
> for (int i = 2; i <= n; i += 2)
> ~~~

> [!tip]
> **Shortcut: Odd Numbers**
>
> Start at `1` and step by `2`.
>
> ~~~java
> for (int i = 1; i <= n; i += 2)
> ~~~

> [!tip]
> **Shortcut: Count Multiples**
>
> Number of positive multiples of `k` up to `n`:
>
> $$\left\lfloor\frac{n}{k}\right\rfloor$$
>
> Example:
>
> Multiples of `5` up to `100`:
>
> $$\left\lfloor\frac{100}{5}\right\rfloor=20$$

> [!tip]
> **Shortcut: Sum 1 to N**
>
> $$\frac{n(n+1)}{2}$$
>
> This can replace a loop when only the sum is required.

> [!tip]
> **Shortcut: Arithmetic Series**
>
> $$S=\frac{n(first+last)}{2}$$
>
> Use when terms form an arithmetic progression.

---

# 42. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Off-by-One Error

Wrong:

~~~java
for (int i = 1; i < 10; i++) {
}
~~~

This runs:

$$
1\text{ through }9
$$

not `1` through `10`.

Correct for `1` through `10`:

~~~java
for (int i = 1; i <= 10; i++) {
}
~~~

---

### Mistake 2 — Wrong Update

Example:

~~~java
for (int i = 1; i <= 10; ) {
    System.out.println(i);
}
~~~

There is no update.

The loop can become infinite.

Correct:

~~~java
for (int i = 1; i <= 10; i++) {
}
~~~

---

### Mistake 3 — Wrong Direction

Wrong:

~~~java
for (int i = 10; i >= 1; i++) {
}
~~~

`i` keeps increasing, so the condition never becomes false.

Correct:

~~~java
for (int i = 10; i >= 1; i--) {
}
~~~

---

### Mistake 4 — Semicolon After for

Avoid:

~~~java
for (int i = 0; i < n; i++);
{
    System.out.println(i);
}
~~~

The semicolon creates an empty loop body.

Correct:

~~~java
for (int i = 0; i < n; i++) {
    System.out.println(i);
}
~~~

---

### Mistake 5 — Incorrect Array Boundary

Wrong:

~~~java
for (int i = 0; i <= arr.length; i++) {
    System.out.println(arr[i]);
}
~~~

The last valid index is:

$$
arr.length-1
$$

Correct:

~~~java
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
~~~

---

### Mistake 6 — Starting Array Index at 1

Java arrays are zero-indexed.

For:

~~~java
int[] arr = {10, 20, 30};
~~~

valid indices are:

~~~text
0 → 10
1 → 20
2 → 30
~~~

Correct traversal:

~~~java
for (int i = 0; i < arr.length; i++) {
}
~~~

---

### Mistake 7 — Confusing break and continue

`break`:

~~~text
Stop entire loop
~~~

`continue`:

~~~text
Skip current iteration
~~~

---

### Mistake 8 — Wrong Complexity for Nested Loops

Two sequential loops:

~~~java
for (...) {
}

for (...) {
}
~~~

Usually:

$$
O(n)
$$

Two nested loops:

~~~java
for (...) {

    for (...) {
    }
}
~~~

Usually:

$$
O(n^2)
$$

---

# 43. Time Complexity Cheat Sheet

| Loop Pattern | Complexity |
|---|---:|
| One loop to `n` | $O(n)$ |
| Two sequential loops | $O(n)$ |
| Two nested loops to `n` | $O(n^2)$ |
| Three nested loops | $O(n^3)$ |
| `i *= 2` | $O(\log n)$ |
| `i /= 2` | $O(\log n)$ |
| Loop over array | $O(n)$ |
| Loop inside loop over array | $O(n^2)$ |

> [!important]
> Always analyze how many times the loop body executes rather than judging complexity only from the number of `for` keywords.

---

# 44. Formula Sheet

### Standard for Loop

~~~java
for (initialization; condition; update) {
    // body
}
~~~

### Increasing

~~~java
for (int i = start; i <= end; i++) {
}
~~~

### Decreasing

~~~java
for (int i = start; i >= end; i--) {
}
~~~

### Step

~~~java
for (int i = start; i <= end; i += step) {
}
~~~

### Iterations

For inclusive range with step `1`:

$$
end-start+1
$$

### General Positive-Step Count

$$
\left\lfloor\frac{end-start}{step}\right\rfloor+1
$$

when the end condition includes the final reachable value.

### Sum of 1 to N

$$
\frac{n(n+1)}{2}
$$

### Arithmetic Series

$$
S=\frac{n(first+last)}{2}
$$

### Sum of First N Odd Numbers

$$
1+3+5+\cdots+(2n-1)=n^2
$$

### Sum of First N Even Numbers

$$
2+4+6+\cdots+2n=n(n+1)
$$

### Multiples of K up to N

$$
\left\lfloor\frac{n}{k}\right\rfloor
$$

### Nested N × N Loop

$$
O(n^2)
$$

### Doubling Loop

$$
O(\log n)
$$

---

# 45. Quick Revision

> [!summary] One-Minute Revision

~~~text
for loop
→ Repeat code using initialization, condition, and update.

Basic form
→ for (init; condition; update)

Execution
→ Initialize → Check → Execute → Update → Repeat.

1 to N
→ i = 1; i <= N; i++

N to 1
→ i = N; i >= 1; i--

Even
→ i = 2; i += 2

Odd
→ i = 1; i += 2

Multiples of K
→ i = K; i += K

Array traversal
→ i = 0; i < arr.length; i++

break
→ Exit loop completely.

continue
→ Skip current iteration.

Nested for
→ Useful for rows, columns, matrices, and patterns.

One normal loop
→ O(n)

Nested n × n loop
→ O(n²)

Doubling/halving variable
→ O(log n)

Sequential loops
→ Usually add, then simplify.

1 to N sum
→ n(n + 1) / 2

Array last index
→ arr.length - 1

Common trap
→ <= vs < causes off-by-one errors.

Infinite loop
→ Usually caused by a condition that never becomes false
   or a missing/incorrect update.
~~~

## Golden Memory Trick

**A `for` loop means: Start here → keep going while this is true → change the value → repeat.**

## One-Line Recognition

**When you know the starting point, stopping condition, and how the value changes, think `for` loop.**