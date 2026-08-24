---
type: concept
subject: coding
topic: "Time and Space Complexity"
parent: "Programming Fundamentals"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - time-complexity
  - space-complexity
  - big-o
  - java
  - dsa
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Loops]]"
  - "[[Functions and Methods]]"
  - "[[Arrays]]"
  - "[[Searching]]"
---

# Time and Space Complexity

## 1. Core Concept

> [!summary]
> **Time Complexity** measures how the running time of an algorithm grows as the input size increases.
>
> **Space Complexity** measures how the memory usage of an algorithm grows as the input size increases.

The goal is not to calculate the exact number of seconds or bytes.

Instead, we study how the algorithm **scales**.

Example:

~~~text
Input size = n

Algorithm A
→ checks every element once
→ O(n)

Algorithm B
→ checks every pair
→ O(n²)
~~~

For large inputs:

$$
O(n) < O(n^2)
$$

So Algorithm A generally scales better.

---

# 2. Basic Meaning

## What is Input Size?

Input size is usually represented by:

$$
n
$$

Examples:

| Problem | Input Size |
|---|---|
| Array | Number of elements |
| String | Number of characters |
| Matrix | Rows × columns |
| Graph | Vertices and edges |
| Number | Number of bits/digits, depending on problem |

Example:

~~~java
int[] arr = new int[1000];
~~~

Here:

$$
n=1000
$$

---

# 3. Time Complexity

Time complexity describes how the number of operations grows with input size.

Example:

~~~java
for (int i = 0; i < n; i++) {
    System.out.println(arr[i]);
}
~~~

The loop runs approximately `n` times.

Therefore:

$$
\boxed{O(n)}
$$

---

# 4. Space Complexity

Space complexity describes how additional memory grows with input size.

Example:

~~~java
int sum = 0;

for (int i = 0; i < n; i++) {
    sum += arr[i];
}
~~~

Only a few variables are used regardless of `n`.

Therefore auxiliary space is:

$$
\boxed{O(1)}
$$

> [!important]
> In algorithm analysis, **auxiliary space** usually refers to extra memory used by the algorithm, excluding the input storage itself unless stated otherwise.

---

# 5. Big-O Notation

Big-O describes an asymptotic upper bound on growth and is commonly used to classify algorithm performance.

Common complexities:

| Complexity | Name | Typical Example |
|---|---|---|
| $O(1)$ | Constant | Array access |
| $O(\log n)$ | Logarithmic | Binary search |
| $O(n)$ | Linear | Linear search |
| $O(n\log n)$ | Linearithmic | Merge sort |
| $O(n^2)$ | Quadratic | Nested loops |
| $O(n^3)$ | Cubic | Triple nested loops |
| $O(2^n)$ | Exponential | Naive recursive Fibonacci |
| $O(n!)$ | Factorial | Brute-force permutations |

General growth:

$$
O(1)
<
O(\log n)
<
O(n)
<
O(n\log n)
<
O(n^2)
<
O(n^3)
<
O(2^n)
<
O(n!)
$$

> [!important]
> The smaller the growth rate, the better the scalability for large inputs, all else being equal.

---

# 6. Constant Time — $O(1)$

An operation is $O(1)$ when its running time does not depend on `n`.

Example:

~~~java
int x = arr[5];
~~~

Accessing a particular array index takes constant time.

Therefore:

$$
\boxed{O(1)}
$$

Another example:

~~~java
int sum = a + b;
~~~

Also:

$$
\boxed{O(1)}
$$

> [!important]
> `O(1)` does not necessarily mean exactly one machine operation. It means the number of operations is bounded independently of input size.

---

# 7. Linear Time — $O(n)$

An algorithm is linear when the work grows proportionally with input size.

Example:

~~~java
for (int i = 0; i < n; i++) {
    System.out.println(arr[i]);
}
~~~

The loop runs:

$$
n
$$

times.

Therefore:

$$
\boxed{O(n)}
$$

---

# 8. Example — Linear Search

## Example 1

### Question

Find the time complexity of:

~~~java
for (int i = 0; i < n; i++) {

    if (arr[i] == target) {
        return i;
    }
}

return -1;
~~~

### Pattern

One loop through the array.

### Worst Case

The target may be at the last position or absent.

Therefore approximately:

$$
n
$$

elements are checked.

### Answer

$$
\boxed{O(n)}
$$

> [!important]
> Linear search has:
>
> Best case:
>
> $$O(1)$$
>
> Worst case:
>
> $$O(n)$$

---

# 9. Logarithmic Time — $O(\log n)$

Logarithmic algorithms reduce the problem size by a constant factor during each step.

The classic example is binary search.

Example:

~~~text
n
↓
n/2
↓
n/4
↓
n/8
↓
...
↓
1
~~~

Number of steps:

$$
\log_2 n
$$

Therefore:

$$
\boxed{O(\log n)}
$$

---

# 10. Binary Search Complexity

## Example 2

### Question

What is the time complexity of binary search?

At every step:

$$
n\rightarrow\frac{n}{2}
$$

After `k` steps:

$$
\frac{n}{2^k}=1
$$

Therefore:

$$
2^k=n
$$

Taking logarithm:

$$
k=\log_2 n
$$

### Answer

$$
\boxed{O(\log n)}
$$

> [!important]
> Binary search requires a suitable ordered/searchable structure, such as a sorted array for the standard implementation.

---

# 11. Quadratic Time — $O(n^2)$

Quadratic complexity commonly appears with two nested loops.

Example:

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < n; j++) {
        System.out.println(i + " " + j);
    }
}
~~~

Outer loop:

$$
n
$$

Inner loop:

$$
n
$$

Total:

$$
n\times n=n^2
$$

Therefore:

$$
\boxed{O(n^2)}
$$

---

# 12. Example — Nested Loop

## Example 3

### Question

Find the time complexity.

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < n; j++) {

        System.out.println(arr[i] + arr[j]);
    }
}
~~~

### Pattern

Nested loops where both depend on `n`.

Therefore:

$$
n\times n=n^2
$$

### Answer

$$
\boxed{O(n^2)}
$$

---

# 13. Cubic Time — $O(n^3)$

Three nested loops often produce cubic complexity.

Example:

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < n; j++) {

        for (int k = 0; k < n; k++) {
            System.out.println(i + j + k);
        }
    }
}
~~~

Operations:

$$
n\times n\times n=n^3
$$

Therefore:

$$
\boxed{O(n^3)}
$$

---

# 14. Linearithmic Time — $O(n\log n)$

A common pattern is:

~~~text
n work
×
log n levels
~~~

This produces:

$$
O(n\log n)
$$

Common examples:

- Merge sort
- Heap sort
- Efficient comparison-based sorting algorithms

Merge sort:

~~~text
Divide
→ log n levels

Process all elements at each level
→ n work
~~~

Therefore:

$$
n\times\log n
$$

$$
\boxed{O(n\log n)}
$$

---

# 15. Sequential Loops

Consider:

~~~java
for (int i = 0; i < n; i++) {
    System.out.println(i);
}

for (int i = 0; i < n; i++) {
    System.out.println(i);
}
~~~

First loop:

$$
O(n)
$$

Second loop:

$$
O(n)
$$

Total:

$$
O(n)+O(n)=O(2n)
$$

Drop the constant:

$$
\boxed{O(n)}
$$

> [!important]
> Sequential loops are usually **added**, not multiplied.

---

# 16. Nested Loops

Consider:

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < n; j++) {
        // work
    }
}
~~~

The loops are nested.

Therefore:

$$
O(n)\times O(n)
$$

$$
\boxed{O(n^2)}
$$

> [!tip]
> **Sequential → add.**
>
> **Nested → multiply.**

---

# 17. Example — Different Loop Sizes

## Example 4

### Question

Find the complexity:

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 0; j < m; j++) {
        // work
    }
}
~~~

Outer loop:

$$
n
$$

Inner loop:

$$
m
$$

Total:

$$
n\times m
$$

### Answer

$$
\boxed{O(nm)}
$$

> [!important]
> Do not automatically replace different variables with $n^2$.

---

# 18. Loop With Doubling

Consider:

~~~java
for (int i = 1; i < n; i *= 2) {
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
...
~~~

The value doubles each iteration.

After `k` iterations:

$$
2^k\approx n
$$

Therefore:

$$
k=\log_2 n
$$

### Answer

$$
\boxed{O(\log n)}
$$

---

# 19. Loop With Halving

Consider:

~~~java
for (int i = n; i > 0; i /= 2) {
    System.out.println(i);
}
~~~

Values:

~~~text
n
n/2
n/4
n/8
...
1
~~~

Therefore:

$$
\boxed{O(\log n)}
$$

> [!important]
> If the loop variable repeatedly doubles or halves, immediately consider $O(\log n)$.

---

# 20. Example — Logarithmic Loop Inside Linear Loop

## Example 5

~~~java
for (int i = 0; i < n; i++) {

    for (int j = 1; j < n; j *= 2) {
        System.out.println(i + j);
    }
}
~~~

Outer:

$$
O(n)
$$

Inner:

$$
O(\log n)
$$

Nested:

$$
O(n\log n)
$$

### Answer

$$
\boxed{O(n\log n)}
$$

---

# 21. Dropping Constants

Consider:

~~~java
for (int i = 0; i < 3 * n; i++) {
    // work
}
~~~

Operations:

$$
3n
$$

Big-O:

$$
O(3n)
$$

Drop the constant:

$$
\boxed{O(n)}
$$

Similarly:

$$
O(100n)=O(n)
$$

> [!important]
> Big-O focuses on growth rate, so constant multipliers are ignored.

---

# 22. Dropping Lower-Order Terms

Consider:

$$
O(n^2+n+10)
$$

For very large `n`, the dominant term is:

$$
n^2
$$

Therefore:

$$
\boxed{O(n^2)}
$$

Example:

~~~text
n² + n + 10
       ↓
dominant term
       ↓
n²
~~~

---

# 23. Example — Polynomial Complexity

## Example 6

### Question

Simplify:

$$
O(5n^2+3n+100)
$$

### Step 1

Ignore constants:

$$
O(n^2+n+1)
$$

### Step 2

Keep the highest-order term:

$$
O(n^2)
$$

### Answer

$$
\boxed{O(n^2)}
$$

---

# 24. Best, Average, and Worst Case

An algorithm can have different complexity depending on the input.

### Best Case

Minimum work.

### Average Case

Expected work over typical inputs under a stated model.

### Worst Case

Maximum work.

Example: Linear search.

| Case | Complexity |
|---|---|
| Best | $O(1)$ |
| Average | $O(n)$ |
| Worst | $O(n)$ |

If the target is first:

$$
O(1)
$$

If the target is last or absent:

$$
O(n)
$$

> [!important]
> When an aptitude or interview question simply asks for "time complexity," check whether it expects worst-case complexity.

---

# 25. Space Complexity

Space complexity measures memory usage.

Consider:

~~~java
int x = 10;
int y = 20;
int sum = x + y;
~~~

Only a fixed number of variables are used.

Therefore:

$$
\boxed{O(1)}
$$

---

# 26. Linear Space — $O(n)$

Consider:

~~~java
int[] copy = new int[n];
~~~

The array requires memory proportional to `n`.

Therefore:

$$
\boxed{O(n)}
$$

Example:

~~~text
n = 10
→ 10 elements

n = 1000
→ 1000 elements
~~~

Memory grows with input size.

---

# 27. Two-Dimensional Space

Consider:

~~~java
int[][] matrix = new int[n][n];
~~~

Number of elements:

$$
n\times n=n^2
$$

Therefore:

$$
\boxed{O(n^2)}
$$

---

# 28. Recursion and Space Complexity

Consider:

~~~java
static void fun(int n) {

    if (n == 0) {
        return;
    }

    fun(n - 1);
}
~~~

There can be `n` active calls.

Therefore stack space:

$$
\boxed{O(n)}
$$

> [!important]
> Recursive calls consume stack memory even if no explicit array or collection is created.

---

# 29. Time and Space Together

## Example 7

~~~java
static int sum(int[] arr) {

    int sum = 0;

    for (int x : arr) {
        sum += x;
    }

    return sum;
}
~~~

### Time

Each element is visited once:

$$
O(n)
$$

### Extra Space

Only `sum` and loop variables are used:

$$
O(1)
$$

### Answer

$$
\boxed{Time=O(n),\ Space=O(1)}
$$

---

# 30. Example — Copying an Array

## Example 8

~~~java
static int[] copyArray(int[] arr) {

    int[] copy = new int[arr.length];

    for (int i = 0; i < arr.length; i++) {
        copy[i] = arr[i];
    }

    return copy;
}
~~~

### Time

The loop runs `n` times:

$$
O(n)
$$

### Extra Space

A new array of size `n` is created:

$$
O(n)
$$

### Answer

$$
\boxed{Time=O(n),\ Space=O(n)}
$$

---

# 31. Example — Nested Loop With Different Bounds

## Example 9

~~~java
for (int i = 0; i < n; i++) {

    for (int j = i; j < n; j++) {
        // work
    }
}
~~~

The inner loop does not always run `n` times.

Total iterations:

$$
n+(n-1)+(n-2)+...+1
$$

This equals:

$$
\frac{n(n+1)}{2}
$$

Therefore:

$$
\frac{n(n+1)}{2}
=
\frac{n^2+n}{2}
$$

Ignoring constants and lower-order terms:

$$
\boxed{O(n^2)}
$$

> [!important]
> Even when nested loops have changing bounds, calculate or estimate the total iterations before deciding the complexity.

---

# 32. Example — Triangular Loop

## Example 10

~~~java
for (int i = 1; i <= n; i++) {

    for (int j = 1; j <= i; j++) {
        // work
    }
}
~~~

Iterations:

$$
1+2+3+\cdots+n
$$

Formula:

$$
\frac{n(n+1)}{2}
$$

Therefore:

$$
\boxed{O(n^2)}
$$

---

# 33. Example — Logarithmic Recursion

Consider:

~~~java
static void fun(int n) {

    if (n <= 1) {
        return;
    }

    fun(n / 2);
}
~~~

Each call reduces `n` by half.

Sequence:

~~~text
n
n/2
n/4
n/8
...
1
~~~

Number of calls:

$$
O(\log n)
$$

### Time

$$
\boxed{O(\log n)}
$$

### Space

There are approximately $\log n$ active calls:

$$
\boxed{O(\log n)}
$$

---

# 34. Example — Exponential Recursion

Consider:

~~~java
static int fun(int n) {

    if (n <= 1) {
        return n;
    }

    return fun(n - 1) + fun(n - 2);
}
~~~

Each call branches into two recursive calls.

This produces an exponential recursion tree.

Approximate time complexity:

$$
\boxed{O(2^n)}
$$

Stack depth:

$$
\boxed{O(n)}
$$

> [!important]
> Time can be exponential while stack space remains linear.

---

# 35. Space Complexity: Input vs Auxiliary Space

Suppose:

~~~java
static int sum(int[] arr) {
    int sum = 0;

    for (int x : arr) {
        sum += x;
    }

    return sum;
}
~~~

Input array:

$$
O(n)
$$

Extra memory used:

$$
O(1)
$$

Therefore:

~~~text
Input space → O(n)
Auxiliary space → O(1)
~~~

> [!important]
> Always clarify whether the question asks for total space or auxiliary space.

---

# 36. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Single Loop

~~~java
for (...) {
}
~~~

Usually:

$$
O(n)
$$

---

### Pattern 2 — Two Nested Loops

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

### Pattern 3 — Three Nested Loops

Usually:

$$
O(n^3)
$$

---

### Pattern 4 — Sequential Loops

~~~text
O(n) + O(n)
→ O(n)
~~~

---

### Pattern 5 — Doubling/Halving

~~~text
i *= 2
i /= 2
~~~

Think:

$$
O(\log n)
$$

---

### Pattern 6 — Linear × Logarithmic

~~~text
Outer → O(n)
Inner → O(log n)
~~~

Think:

$$
O(n\log n)
$$

---

### Pattern 7 — Array Creation

~~~java
new int[n]
~~~

Think:

$$
O(n)\text{ space}
$$

---

### Pattern 8 — Matrix Creation

~~~java
new int[n][n]
~~~

Think:

$$
O(n^2)\text{ space}
$$

---

### Pattern 9 — Recursive Chain

~~~text
f(n)
→ f(n-1)
→ f(n-2)
→ ...
~~~

Usually:

$$
O(n)\text{ stack space}
$$

---

### Pattern 10 — Recursive Halving

~~~text
f(n)
→ f(n/2)
→ f(n/4)
→ ...
~~~

Think:

$$
O(\log n)
$$

---

# 37. Recognition Tricks

> [!important]
> **One loop from `0` to `n`**
>
> Think:
>
> $$O(n)$$

> [!important]
> **Two independent nested loops**
>
> Think:
>
> $$O(n^2)$$

> [!important]
> **Three independent nested loops**
>
> Think:
>
> $$O(n^3)$$

> [!important]
> **Loop variable doubles or halves**
>
> Think:
>
> $$O(\log n)$$

> [!important]
> **Every element + logarithmic processing**
>
> Think:
>
> $$O(n\log n)$$

> [!important]
> **Create an array of size `n`**
>
> Think:
>
> $$O(n)\text{ space}$$

> [!important]
> **Recursive call with `n - 1`**
>
> Think:
>
> $$O(n)\text{ depth}$$

> [!important]
> **Recursive call with `n / 2`**
>
> Think:
>
> $$O(\log n)\text{ depth}$$

> [!important]
> **Two recursive calls such as `f(n-1)` and `f(n-2)`**
>
> Think:
>
> Exponential time may occur.

---

# 38. Shortcuts

> [!tip]
> **Shortcut: Loop Counting**
>
> Ask:
>
> ```text
> How many times does the loop execute?
> ```
>
> That is usually the first step toward time complexity.

> [!tip]
> **Shortcut: Nested vs Sequential**
>
> ```text
> Sequential → Add
>
> Nested → Multiply
> ```

> [!tip]
> **Shortcut: Multiplicative Change**
>
> If:
>
> ```text
> i *= 2
> i /= 2
> n = n / 2
> ```
>
> think:
>
> $$O(\log n)$$

> [!tip]
> **Shortcut: Remove Constants**
>
> $$O(5n)\rightarrow O(n)$$
>
> $$O(10n^2)\rightarrow O(n^2)$$

> [!tip]
> **Shortcut: Keep Dominant Term**
>
> $$O(n^2+n+1)\rightarrow O(n^2)$$

> [!tip]
> **Shortcut: Recursion**
>
> Count:
>
> 1. Number of recursive calls per level.
> 2. Number of levels.
> 3. Work performed at each level.

---

# 39. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Counting Statements Instead of Growth

An algorithm performing `100` operations is still:

$$
O(1)
$$

if those operations do not depend on `n`.

---

### Mistake 2 — Keeping Constants

Wrong:

$$
O(3n)
$$

Standard simplified form:

$$
\boxed{O(n)}
$$

---

### Mistake 3 — Adding Nested Loops

For:

~~~java
for (...) {
    for (...) {
    }
}
~~~

Do not write:

$$
O(n+n)=O(n)
$$

Correct:

$$
O(n\times n)=O(n^2)
$$

---

### Mistake 4 — Multiplying Sequential Loops

For:

~~~java
for (...) {
}

for (...) {
}
~~~

Do not write:

$$
O(n^2)
$$

Correct:

$$
O(n+n)=O(n)
$$

---

### Mistake 5 — Assuming Every Nested Loop Is $O(n^2)$

Example:

~~~java
for (int i = 0; i < n; i++) {
    for (int j = 1; j < n; j *= 2) {
    }
}
~~~

Complexity:

$$
O(n\log n)
$$

not:

$$
O(n^2)
$$

---

### Mistake 6 — Ignoring Recursion Stack

Recursive code can use additional stack space even when no array is created.

---

### Mistake 7 — Confusing Time and Space

An algorithm can be:

$$
Time=O(n)
$$

and:

$$
Space=O(1)
$$

These are separate measurements.

---

### Mistake 8 — Assuming Faster for Small Inputs

Asymptotic complexity mainly describes growth for large inputs. Constant factors and implementation details can matter for small inputs.

---

# 40. Formula Sheet

### Common Complexities

$$
O(1)
$$

$$
O(\log n)
$$

$$
O(n)
$$

$$
O(n\log n)
$$

$$
O(n^2)
$$

$$
O(n^3)
$$

$$
O(2^n)
$$

$$
O(n!)
$$

### Sequential Work

$$
O(n)+O(n)=O(n)
$$

### Nested Work

$$
O(n)\times O(n)=O(n^2)
$$

### Linear × Logarithmic

$$
O(n)\times O(\log n)
=
O(n\log n)
$$

### Triangular Sum

$$
1+2+\cdots+n
=
\frac{n(n+1)}{2}
$$

Therefore:

$$
O(n^2)
$$

### Binary Search

$$
n\rightarrow\frac{n}{2}\rightarrow\frac{n}{4}\rightarrow...
$$

$$
O(\log n)
$$

### Array of Size N

$$
O(n)\text{ space}
$$

### Matrix of Size N × N

$$
O(n^2)\text{ space}
$$

### Recursive Chain

$$
O(n)\text{ stack space}
$$

### Recursive Halving

$$
O(\log n)\text{ stack space}
$$

---

# 41. Quick Revision

> [!summary] One-Minute Revision

~~~text
Time Complexity
→ How runtime grows with input size.

Space Complexity
→ How memory usage grows.

O(1)
→ Constant.

O(log n)
→ Repeatedly divide by a constant factor.

O(n)
→ One full pass.

O(n log n)
→ n work across log n levels.

O(n²)
→ Two nested linear loops.

O(n³)
→ Three nested linear loops.

O(2^n)
→ Common in naive branching recursion.

O(n!)
→ Common in brute-force permutations.

Sequential loops
→ Add complexities.

Nested loops
→ Multiply complexities.

3n
→ O(n).

n² + n + 10
→ O(n²).

i *= 2
→ O(log n).

i /= 2
→ O(log n).

new int[n]
→ O(n) extra space.

new int[n][n]
→ O(n²) extra space.

Recursive f(n-1)
→ Usually O(n) depth.

Recursive f(n/2)
→ Usually O(log n) depth.

Always check:
→ Number of iterations
→ Nesting
→ Input reduction
→ Recursive branching
→ Extra memory
~~~

## Golden Memory Trick

**Count how the work grows: one-by-one means `n`, repeatedly halving means `log n`, nested growth means multiplication, and extra storage means space complexity.**

## One-Line Recognition

**When analyzing code, count the loop iterations or recursive levels for time, then count the additional data structures and recursion stack for space.**