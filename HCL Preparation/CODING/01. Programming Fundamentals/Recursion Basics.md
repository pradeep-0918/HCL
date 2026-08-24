---
type: concept
subject: coding
topic: "Recursion Basics"
parent: "Programming Fundamentals"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - recursion
  - java
  - programming
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Functions and Methods]]"
  - "[[Loops]]"
  - "[[Recursion]]"
---

# Recursion Basics

## 1. Core Concept

> [!summary]
> **Recursion** is a technique where a method calls itself to solve a smaller version of the same problem.

The basic idea is:

~~~text
Large Problem
    ↓
Smaller Problem
    ↓
Even Smaller Problem
    ↓
Base Case
    ↓
Return Back
~~~

Every recursive solution needs two important parts:

1. **Base Case** → tells the recursion when to stop.
2. **Recursive Case** → calls the same method with a smaller/simpler input.

Example:

~~~java
static void countDown(int n) {
    if (n == 0) {
        return;
    }

    System.out.println(n);
    countDown(n - 1);
}
~~~

Calling:

~~~java
countDown(3);
~~~

Produces:

~~~text
3
2
1
~~~

---

# 2. Basic Meaning

## What is Recursion?

Recursion occurs when a method directly or indirectly calls itself.

Direct recursion:

~~~java
static void fun(int n) {
    fun(n - 1);
}
~~~

The method `fun()` calls itself.

### General Structure

~~~java
static returnType method(parameters) {

    if (baseCase) {
        return result;
    }

    return method(smallerInput);
}
~~~

Think:

$$
\text{Recursion}=\text{Base Case}+\text{Recursive Case}
$$

---

# 3. Why Recursion?

Recursion is useful when a problem naturally contains smaller versions of itself.

Common examples:

- Factorial
- Fibonacci
- Sum of numbers
- Power
- Reverse a string
- Reverse a number
- Binary search
- Tree traversal
- Graph traversal
- Backtracking
- Divide and conquer
- Dynamic programming

> [!important]
> Recursion is especially powerful for **trees, graphs, backtracking, divide-and-conquer, and DP**.

---

# 4. Base Case

The **base case** is the stopping condition.

Example:

~~~java
static void print(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);
    print(n - 1);
}
~~~

Here:

~~~java
if (n == 0)
~~~

is the base case.

Without a base case, recursion may continue indefinitely.

> [!warning]
> Every recursive method must have a reachable stopping condition.

---

# 5. Recursive Case

The recursive case is the part where the method calls itself.

Example:

~~~java
static void print(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);

    print(n - 1);
}
~~~

Here:

~~~java
print(n - 1);
~~~

is the recursive case.

Notice that the problem becomes smaller:

$$
n\rightarrow n-1
$$

---

# 6. The Three Questions for Recursion

Whenever you see a recursive problem, ask:

### Question 1

**What is the smallest possible input?**

This helps identify the base case.

### Question 2

**How can I reduce the problem?**

This gives the recursive call.

### Question 3

**What should happen when the smallest case is reached?**

This gives the return value or stopping action.

> [!tip]
> Remember:
>
> **Base → Reduce → Call**

---

# 7. Basic Example — Countdown

## Example 1

### Question

Print numbers from `5` down to `1` using recursion.

### Pattern

Each call prints one number and decreases `n`.

### Code

~~~java
static void countdown(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);

    countdown(n - 1);
}
~~~

Call:

~~~java
countdown(5);
~~~

### Execution

~~~text
countdown(5)
→ print 5
→ countdown(4)

countdown(4)
→ print 4
→ countdown(3)

countdown(3)
→ print 3
→ countdown(2)

countdown(2)
→ print 2
→ countdown(1)

countdown(1)
→ print 1
→ countdown(0)

countdown(0)
→ stop
~~~

Output:

~~~text
5
4
3
2
1
~~~

### Answer

$$
\boxed{5,4,3,2,1}
$$

---

# 8. Recursive Call Stack

Every recursive call creates a new stack frame.

For:

~~~java
countdown(3);
~~~

The calls are:

~~~text
countdown(3)
    ↓
countdown(2)
    ↓
countdown(1)
    ↓
countdown(0)
~~~

Then the calls return.

This is managed using the **call stack**.

> [!important]
> Recursion uses stack memory. Too many recursive calls can cause `StackOverflowError` in Java.

---

# 9. Recursion Flow

Consider:

~~~java
static void fun(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);
    fun(n - 1);
}
~~~

For:

~~~text
fun(3)
~~~

The execution goes:

~~~text
Going Down:
3
2
1
0

Returning:
1
2
3
~~~

However, because the `println()` occurs **before** the recursive call, the visible output is:

~~~text
3
2
1
~~~

This distinction is extremely important.

---

# 10. Before vs After Recursive Call

## Example 2

### Question

What is the output?

~~~java
static void fun(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);

    fun(n - 1);
}
~~~

For:

~~~java
fun(3);
~~~

Output:

~~~text
3
2
1
~~~

Because printing happens before the recursive call.

---

Now change the order:

~~~java
static void fun(int n) {

    if (n == 0) {
        return;
    }

    fun(n - 1);

    System.out.println(n);
}
~~~

Execution reaches the base case first and prints while returning.

Output:

~~~text
1
2
3
~~~

> [!important]
> **Before recursive call → forward order.**
>
> **After recursive call → reverse/unwinding order.**

---

# 11. Factorial Using Recursion

## Example 3

### Question

Find:

$$
5!
$$

### Formula

$$
n!=n\times(n-1)!
$$

Base case:

$$
0!=1
$$

### Code

~~~java
static int factorial(int n) {

    if (n == 0) {
        return 1;
    }

    return n * factorial(n - 1);
}
~~~

Call:

~~~java
factorial(5);
~~~

### Expansion

$$
5!=5\times4!
$$

$$
=5\times4\times3!
$$

$$
=5\times4\times3\times2!
$$

$$
=5\times4\times3\times2\times1!
$$

$$
=5\times4\times3\times2\times1
$$

$$
=120
$$

### Answer

$$
\boxed{120}
$$

---

# 12. Factorial Recursion Tree

For:

~~~text
factorial(4)
~~~

The calls are:

~~~text
factorial(4)
    ↓
factorial(3)
    ↓
factorial(2)
    ↓
factorial(1)
    ↓
factorial(0)
~~~

Then return:

~~~text
factorial(0) → 1
factorial(1) → 1 × 1 = 1
factorial(2) → 2 × 1 = 2
factorial(3) → 3 × 2 = 6
factorial(4) → 4 × 6 = 24
~~~

Therefore:

$$
\boxed{24}
$$

---

# 13. Sum of First N Numbers

## Example 4

### Question

Find the sum:

$$
1+2+3+4+5
$$

using recursion.

### Pattern

Reduce:

$$
sum(n)=n+sum(n-1)
$$

Base case:

$$
sum(0)=0
$$

### Code

~~~java
static int sum(int n) {

    if (n == 0) {
        return 0;
    }

    return n + sum(n - 1);
}
~~~

For:

$$
n=5
$$

Expansion:

$$
sum(5)=5+sum(4)
$$

$$
=5+4+sum(3)
$$

$$
=5+4+3+2+1+0
$$

$$
=15
$$

### Answer

$$
\boxed{15}
$$

---

# 14. Power Using Recursion

## Example 5

### Question

Calculate:

$$
2^5
$$

### Pattern

$$
a^n=a\times a^{n-1}
$$

Base case:

$$
a^0=1
$$

### Code

~~~java
static int power(int a, int n) {

    if (n == 0) {
        return 1;
    }

    return a * power(a, n - 1);
}
~~~

Expansion:

$$
2^5
=
2\times2^4
$$

$$
=2\times2\times2^3
$$

$$
=2\times2\times2\times2^2
$$

$$
=2\times2\times2\times2\times2
$$

$$
=32
$$

### Answer

$$
\boxed{32}
$$

---

# 15. Fibonacci Using Recursion

## Example 6

### Question

Find the 5th Fibonacci number.

Fibonacci sequence:

~~~text
0 1 1 2 3 5 8 ...
~~~

Using:

$$
F(n)=F(n-1)+F(n-2)
$$

Base cases:

$$
F(0)=0
$$

$$
F(1)=1
$$

### Code

~~~java
static int fibonacci(int n) {

    if (n == 0) {
        return 0;
    }

    if (n == 1) {
        return 1;
    }

    return fibonacci(n - 1)
         + fibonacci(n - 2);
}
~~~

For:

$$
F(5)
$$

$$
F(5)=5
$$

### Answer

$$
\boxed{5}
$$

> [!warning]
> Simple recursive Fibonacci is inefficient because it repeatedly solves the same subproblems. This is a major reason **Dynamic Programming** is used.

---

# 16. Recursive Fibonacci Tree

For:

$$
F(4)
$$

The recursive structure is:

~~~text
             F(4)
           /      \
        F(3)      F(2)
       /   \      /   \
    F(2)  F(1) F(1)  F(0)
    /  \
  F(1) F(0)
~~~

Notice that `F(2)` and other values are calculated repeatedly.

This causes exponential growth in the number of calls.

Time complexity:

$$
O(2^n)
$$

> [!important]
> Recursion does not automatically mean efficient. Always analyze the number of recursive calls.

---

# 17. Recursive String Reversal

## Example 7

### Question

Reverse the string:

~~~text
"hello"
~~~

### Pattern

Take the first character and recursively reverse the remaining string.

Conceptually:

~~~text
hello
→ h + reverse("ello")

ello
→ e + reverse("llo")

llo
→ l + reverse("lo")

lo
→ l + reverse("o")

o
→ o
~~~

One possible implementation:

~~~java
static String reverse(String s) {

    if (s.length() <= 1) {
        return s;
    }

    return reverse(s.substring(1))
         + s.charAt(0);
}
~~~

Result:

~~~text
olleh
~~~

### Answer

$$
\boxed{olleh}
$$

---

# 18. Recursion vs Iteration

Recursion and loops can often solve the same problem.

Example: factorial.

### Recursive

~~~java
static int factorial(int n) {

    if (n == 0) {
        return 1;
    }

    return n * factorial(n - 1);
}
~~~

### Iterative

~~~java
static int factorial(int n) {

    int result = 1;

    for (int i = 1; i <= n; i++) {
        result *= i;
    }

    return result;
}
~~~

Both calculate:

$$
n!
$$

### Comparison

| Feature | Recursion | Loop |
|---|---|---|
| Repetition | Method calls | Iteration |
| Memory | Uses call stack | Usually less |
| Code | Often shorter for recursive structures | Often simpler for linear tasks |
| Best for | Trees, backtracking, divide-and-conquer | Simple repeated calculations |
| Risk | Stack overflow | Usually no recursion stack |

> [!important]
> Use recursion when it naturally matches the problem structure, not simply because it is possible.

---

# 19. Direct vs Indirect Recursion

## Direct Recursion

A method directly calls itself.

~~~java
static void fun() {
    fun();
}
~~~

## Indirect Recursion

One method calls another method, which eventually calls the first method.

~~~java
static void A() {
    B();
}

static void B() {
    A();
}
~~~

Flow:

~~~text
A()
 ↓
B()
 ↓
A()
 ↓
B()
 ↓
...
~~~

> [!important]
> Both forms are recursion, but direct recursion is the most common beginner pattern.

---

# 20. Tail Recursion

A recursive call is **tail-recursive** when it is the final operation performed by the method.

Example:

~~~java
static void countdown(int n) {

    if (n == 0) {
        return;
    }

    System.out.println(n);
    countdown(n - 1);
}
~~~

The recursive call is the final operation.

Non-tail example:

~~~java
static int factorial(int n) {

    if (n == 0) {
        return 1;
    }

    return n * factorial(n - 1);
}
~~~

After the recursive call returns, multiplication still has to happen.

> [!important]
> Java does not generally perform tail-call optimization, so tail recursion can still consume stack space.

---

# 21. Recursion and Call Stack

Consider:

~~~java
static int sum(int n) {

    if (n == 0) {
        return 0;
    }

    return n + sum(n - 1);
}
~~~

Calling:

~~~text
sum(3)
~~~

creates:

~~~text
sum(3)
sum(2)
sum(1)
sum(0)
~~~

Then returns:

~~~text
sum(0) → 0
sum(1) → 1
sum(2) → 3
sum(3) → 6
~~~

Each active method call occupies stack memory.

Therefore, if recursion depth is $n$:

$$
\text{Auxiliary Stack Space}=O(n)
$$

for a single recursive chain.

---

# 22. Example — Count Digits Recursively

## Example 8

### Question

Count the number of digits in:

$$
12345
$$

### Pattern

Remove one digit using integer division by `10`.

$$
n\rightarrow n/10
$$

Base case:

$$
n=0
$$

### Code

~~~java
static int countDigits(int n) {

    if (n == 0) {
        return 0;
    }

    return 1 + countDigits(n / 10);
}
~~~

For:

$$
12345
$$

The sequence is:

~~~text
12345
1234
123
12
1
0
~~~

Therefore:

$$
5
$$

### Answer

$$
\boxed{5}
$$

> [!warning]
> This simple implementation needs special handling if `n = 0`, because zero itself has one digit.

---

# 23. Example — Sum of Digits

## Example 9

### Question

Find the sum of digits of:

$$
1234
$$

### Pattern

Last digit:

$$
n\%10
$$

Remaining number:

$$
n/10
$$

Recursive formula:

$$
sumDigits(n)=n\%10+sumDigits(n/10)
$$

Base case:

$$
n=0
$$

### Code

~~~java
static int sumDigits(int n) {

    if (n == 0) {
        return 0;
    }

    return n % 10 + sumDigits(n / 10);
}
~~~

Calculation:

$$
1234\rightarrow4+sumDigits(123)
$$

$$
=4+3+2+1
$$

$$
=10
$$

### Answer

$$
\boxed{10}
$$

---

# 24. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Factorial

If the question contains:

~~~text
n!
product from 1 to n
~~~

Think:

$$
factorial(n)=n\times factorial(n-1)
$$

Base:

$$
factorial(0)=1
$$

---

### Pattern 2 — Sum from 1 to N

If the question says:

~~~text
sum of first n numbers
~~~

Think:

$$
sum(n)=n+sum(n-1)
$$

Base:

$$
sum(0)=0
$$

---

### Pattern 3 — Power

If the question says:

~~~text
calculate a^n
~~~

Think:

$$
power(a,n)=a\times power(a,n-1)
$$

Base:

$$
power(a,0)=1
$$

---

### Pattern 4 — Digit Problems

If the problem involves:

~~~text
digits
reverse
digit sum
digit count
~~~

Think:

~~~text
n % 10 → last digit
n / 10 → remove last digit
~~~

---

### Pattern 5 — Fibonacci

If the problem follows:

~~~text
previous two values determine the next
~~~

Think:

$$
F(n)=F(n-1)+F(n-2)
$$

---

### Pattern 6 — Tree Problems

If each node has smaller child/subtree problems:

~~~text
Think → recursion
~~~

Typical examples:

- Tree traversal
- Tree height
- Tree diameter
- Tree path problems

---

### Pattern 7 — Backtracking

If the problem requires:

~~~text
choose
explore
undo
choose again
~~~

Think:

$$
\text{Recursion + Backtracking}
$$

---

# 25. Recognition Tricks

> [!important]
> If the problem can be expressed as the **same problem with smaller input**, think recursion.

> [!important]
> If you can write:

$$
f(n)=\text{something involving }f(n-1)
$$

think recursive solution.

> [!important]
> If the problem naturally divides into two or more smaller versions, recursion may be useful.

> [!important]
> If you see a tree structure, immediately consider recursion.

> [!important]
> If the problem says **choose → explore → undo**, think recursion/backtracking.

> [!important]
> If digits are repeatedly removed, think:

$$
n\%10,\quad n/10
$$

> [!important]
> If a recursive method has no reachable base case, expect infinite recursion or stack overflow.

---

# 26. Shortcuts

> [!tip]
> **Shortcut: Recursion Formula**
>
> Ask:
>
> ```text
> What is the smallest case?
> How do I reduce the input?
> What should I return?
> ```

> [!tip]
> **Shortcut: Digit Recursion**
>
> Last digit:
>
> $$n\%10$$
>
> Remove last digit:
>
> $$n/10$$

> [!tip]
> **Shortcut: Factorial**
>
> $$n!=n\times(n-1)!$$
>
> Base:
>
> $$0!=1$$

> [!tip]
> **Shortcut: Fibonacci**
>
> $$F(n)=F(n-1)+F(n-2)$$
>
> Base:
>
> $$F(0)=0,\quad F(1)=1$$

> [!tip]
> **Shortcut: Output Order**
>
> Print before recursive call → forward order.
>
> Print after recursive call → reverse/unwinding order.

---

# 27. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Missing Base Case

Wrong:

~~~java
static void fun(int n) {
    System.out.println(n);
    fun(n - 1);
}
~~~

There is no stopping condition.

This can eventually cause:

~~~text
StackOverflowError
~~~

---

### Mistake 2 — Base Case Is Never Reached

Example:

~~~java
static void fun(int n) {

    if (n == 0) {
        return;
    }

    fun(n + 1);
}
~~~

If `n` starts positive, it moves away from `0`.

Correct direction:

~~~java
fun(n - 1);
~~~

when the base case is `n == 0`.

---

### Mistake 3 — Forgetting to Return the Recursive Result

Wrong:

~~~java
static int sum(int n) {

    if (n == 0) {
        return 0;
    }

    sum(n - 1);
}
~~~

Correct:

~~~java
static int sum(int n) {

    if (n == 0) {
        return 0;
    }

    return n + sum(n - 1);
}
~~~

---

### Mistake 4 — Confusing Call Order and Return Order

For:

~~~java
fun(3)
~~~

the calls happen:

~~~text
3 → 2 → 1 → 0
~~~

But results may return:

~~~text
0 → 1 → 2 → 3
~~~

> [!important]
> Always separate the **calling phase** from the **returning phase**.

---

### Mistake 5 — Assuming Recursion Is Always Faster

Recursive Fibonacci:

$$
O(2^n)
$$

is much slower than an optimized iterative or DP solution.

Recursion is a technique, not automatically an optimization.

---

### Mistake 6 — Ignoring Stack Space

A recursive chain of depth $n$ generally uses:

$$
O(n)
$$

stack space.

Very deep recursion can cause stack overflow.

---

### Mistake 7 — Using Recursion When a Simple Loop Is Better

For a simple linear repetition, a loop is often more memory-efficient.

Example:

~~~java
for (int i = 1; i <= n; i++) {
    System.out.println(i);
}
~~~

may be preferable to recursive calls when recursion provides no real advantage.

---

# 28. Formula Sheet

### Basic Recursive Structure

~~~java
static returnType function(parameters) {

    if (baseCase) {
        return baseValue;
    }

    return recursiveFunction(smallerInput);
}
~~~

### Factorial

$$
n!=n\times(n-1)!
$$

$$
0!=1
$$

### Sum of First N Numbers

$$
sum(n)=n+sum(n-1)
$$

$$
sum(0)=0
$$

### Power

$$
a^n=a\times a^{n-1}
$$

$$
a^0=1
$$

### Fibonacci

$$
F(n)=F(n-1)+F(n-2)
$$

$$
F(0)=0,\quad F(1)=1
$$

### Sum of Digits

$$
sumDigits(n)=n\%10+sumDigits(n/10)
$$

### Digit Extraction

$$
\text{Last digit}=n\%10
$$

### Remove Last Digit

$$
n=n/10
$$

### Recursive Chain Space

$$
O(n)
$$

for a single recursion chain of depth $n$.

---

# 29. Quick Revision

> [!summary] One-Minute Revision

~~~text
Recursion
→ Method calls itself.

Two essential parts
→ Base case + Recursive case.

Base case
→ Stops recursion.

Recursive case
→ Reduces problem and calls itself.

Factorial
→ n! = n × (n-1)!

Sum
→ sum(n) = n + sum(n-1)

Power
→ a^n = a × a^(n-1)

Fibonacci
→ F(n) = F(n-1) + F(n-2)

Digit problems
→ n % 10 → last digit
→ n / 10 → remove last digit

Before recursive call
→ Forward output.

After recursive call
→ Reverse/unwinding output.

Recursion
→ Uses call stack.

Deep recursion
→ Can cause StackOverflowError.

Tree problems
→ Often naturally recursive.

Backtracking
→ Recursion + choose/explore/undo.

Always ask
→ Base case?
→ Smaller problem?
→ Return value?
~~~

## Golden Memory Trick

**Recursion means solve the same problem on a smaller input until the smallest case becomes directly solvable.**

## One-Line Recognition

**When a problem can be reduced to the same problem with a smaller input, look for a base case and consider recursion.**