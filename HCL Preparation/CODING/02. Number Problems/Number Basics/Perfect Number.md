---
type: concept
subject: coding
topic: "Perfect Number"
parent: "Number Basics"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - number-problems
  - number-basics
  - perfect-number
  - java
  - factors
  - divisors
wikilinks:
  - "[[Number Basics]]"
  - "[[Prime Number]]"
  - "[[Composite Number]]"
  - "[[Divisibility]]"
  - "[[GCD and LCM]]"
---

# Perfect Number

## 1. Core Concept

> [!summary]
> A **perfect number** is a positive integer that is equal to the **sum of its proper positive divisors**, excluding the number itself.
>
> The smallest perfect number is:
>
> $$6$$
>
> Its proper divisors are:
>
> $$1,2,3$$
>
> and:
>
> $$1+2+3=6$$
>
> Therefore:
>
> $$\boxed{6\text{ is a Perfect Number}}$$

The key idea is:

$$
\boxed{\text{Sum of Proper Divisors}=\text{Number}}
$$

---

# 2. Basic Meaning

A **proper divisor** of a number is a positive divisor that is **smaller than the number itself**.

For example, for `12`:

All positive divisors:

$$
1,2,3,4,6,12
$$

Proper divisors:

$$
1,2,3,4,6
$$

We exclude `12`.

Their sum is:

$$
1+2+3+4+6=16
$$

Since:

$$
16\neq12
$$

`12` is not perfect.

---

# 3. Main Formula

Let $n$ be a positive integer.

A number is perfect if:

$$
\boxed{
\sum_{\substack{d\mid n\\d<n}}d=n
}
$$

In simple programming terms:

$$
\boxed{\text{sum of proper divisors}=n}
$$

### Classification

| Condition | Result |
|---|---|
| Sum of proper divisors = $n$ | Perfect |
| Sum of proper divisors < $n$ | Deficient |
| Sum of proper divisors > $n$ | Abundant |

Examples:

$$
6\rightarrow Perfect
$$

$$
8\rightarrow Deficient
$$

$$
12\rightarrow Abundant
$$

---

# 4. Important Properties

## Property 1 — The Number Itself Is Excluded

For:

$$
6
$$

do not include `6` in the divisor sum.

Correct:

$$
1+2+3=6
$$

Wrong:

$$
1+2+3+6=12
$$

> [!warning]
> The number itself is **not** a proper divisor.

---

## Property 2 — The Smallest Perfect Number Is 6

The first few positive integers do not work.

For `6`:

$$
1+2+3=6
$$

Therefore:

$$
\boxed{6}
$$

is the smallest perfect number.

---

## Property 3 — Perfect Numbers Are Rare

The first few known perfect numbers are:

$$
6,28,496,8128,\ldots
$$

They become very large very quickly.

---

## Property 4 — Every Known Perfect Number Is Even

All known perfect numbers are even.

However, whether an odd perfect number exists is an unsolved problem in mathematics.

For programming and aptitude problems, you normally work with known perfect numbers and direct divisor checks.

---

## Property 5 — Perfect Numbers Are Related to Divisors

The entire problem is based on finding divisors.

Therefore:

> [!important]
> When you see **perfect number**, immediately think:
>
> **Find proper divisors → add them → compare with N.**

---

# 5. Basic Example — 6

## Example 1

### Question

Check whether `6` is a perfect number.

### Step 1 — Find proper divisors

Divisors of `6`:

$$
1,2,3,6
$$

Exclude `6`.

Proper divisors:

$$
1,2,3
$$

### Step 2 — Find the sum

$$
1+2+3=6
$$

### Step 3 — Compare

$$
6=6
$$

### Answer

$$
\boxed{6\text{ is a Perfect Number}}
$$

---

# 6. Basic Example — 8

## Example 2

### Question

Check whether `8` is perfect.

Proper divisors:

$$
1,2,4
$$

Sum:

$$
1+2+4=7
$$

Compare:

$$
7\neq8
$$

Therefore:

$$
\boxed{8\text{ is Not a Perfect Number}}
$$

It is actually a deficient number.

---

# 7. Basic Example — 12

## Example 3

### Question

Check whether `12` is perfect.

Proper divisors:

$$
1,2,3,4,6
$$

Sum:

$$
1+2+3+4+6=16
$$

Since:

$$
16\neq12
$$

Therefore:

$$
\boxed{12\text{ is Not a Perfect Number}}
$$

It is abundant because:

$$
16>12
$$

---

# 8. Important Perfect Numbers

The first few perfect numbers are:

| Perfect Number | Proper Divisors |
|---:|---|
| 6 | 1, 2, 3 |
| 28 | 1, 2, 4, 7, 14 |
| 496 | 1, 2, 4, 8, 16, 31, 62, 124, 248 |
| 8128 | Proper divisors sum to 8128 |

For aptitude and basic coding questions, remember:

$$
\boxed{6,28,496,8128}
$$

---

# 9. Example — 28

## Example 4

### Question

Check whether `28` is perfect.

### Proper divisors

$$
1,2,4,7,14
$$

### Sum

$$
1+2+4+7+14=28
$$

Therefore:

$$
\boxed{28\text{ is a Perfect Number}}
$$

> [!tip]
> Memorizing `6` and `28` is useful because they are common examples used to explain perfect numbers.

---

# 10. Basic Java Program

## Example 5

### Question

Write a Java program to check whether a number is perfect.

### Code

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            int sum = 0;

            for (int i = 1; i < n; i++) {

                if (n % i == 0) {
                    sum += i;
                }
            }

            if (n > 0 && sum == n) {
                System.out.println("Perfect Number");
            } else {
                System.out.println("Not a Perfect Number");
            }
        }
    }

### Logic

    Start sum = 0

    Check every i from 1 to n - 1

    If n % i == 0
    → i is a proper divisor

    Add i to sum

    Finally:
    if sum == n
    → Perfect

---

# 11. Optimized Perfect Number Check

The basic method checks every number from:

$$
1\text{ to }n-1
$$

This is unnecessary.

Divisors occur in pairs.

If:

$$
d\mid n
$$

then:

$$
\frac nd
$$

is also a divisor.

Therefore, we can search only up to:

$$
\sqrt n
$$

---

# 12. Divisor Pair Technique

Suppose:

$$
n=36
$$

Divisor pairs are:

$$
1\times36
$$

$$
2\times18
$$

$$
3\times12
$$

$$
4\times9
$$

$$
6\times6
$$

If we find `2`, we automatically know `18` is also a divisor.

This allows us to process divisors in pairs.

> [!important]
> **For divisor-based problems, always think about divisor pairs and √N optimization.**

---

# 13. Optimized Java Program

## Example 6

### Code

    static boolean isPerfect(int n) {

        if (n <= 1) {
            return false;
        }

        int sum = 1;

        for (int i = 2; i * i <= n; i++) {

            if (n % i == 0) {

                sum += i;

                int other = n / i;

                if (other != i) {
                    sum += other;
                }
            }
        }

        return sum == n;
    }

### Why Start With `sum = 1`?

For every number:

$$
n>1
$$

`1` is always a proper divisor.

So we include:

$$
1
$$

before starting the loop from `2`.

### Complexity

Time:

$$
\boxed{O(\sqrt n)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 14. Example — Optimized Check for 28

## Example 7

### Question

Check `28` using divisor pairs.

$$
\sqrt{28}\approx5.29
$$

Check:

$$
2,3,4,5
$$

For `2`:

$$
28/2=14
$$

Add:

$$
2+14
$$

For `4`:

$$
28/4=7
$$

Add:

$$
4+7
$$

Start with `1`.

Total:

$$
1+2+14+4+7=28
$$

Therefore:

$$
\boxed{28\text{ is Perfect}}
$$

---

# 15. Important Duplicate Factor Case

Consider:

$$
n=36
$$

At:

$$
i=6
$$

we get:

$$
36/6=6
$$

The same divisor appears twice.

Therefore, do **not** add it twice.

Correct:

$$
6
$$

not:

$$
6+6
$$

### Code

    if (other != i) {
        sum += other;
    }

> [!warning]
> This is one of the most important bugs in divisor-pair implementations.

---

# 16. Example — Why Duplicate Handling Matters

Suppose:

$$
n=36
$$

At:

$$
i=6
$$

we have:

$$
i=\frac ni
$$

because:

$$
6=\frac{36}{6}
$$

This happens whenever:

$$
i^2=n
$$

Therefore:

> [!important]
> If `i * i == n`, add the divisor only once.

---

# 17. Pattern Recognition — Perfect Number

> [!important]
> **If the question says:**
>
> "Check whether N is a perfect number."
>
> Immediately think:
>
> $$\boxed{\text{Sum of proper divisors}=N}
> $$
>
> Steps:
>
> 1. Find proper divisors.
> 2. Add them.
> 3. Compare the sum with N.

---

# 18. Pattern Recognition — Divisor Pair

> [!important]
> **If the problem involves factors or divisors of N:**
>
> Think:
>
> $$\boxed{i\text{ and }N/i}
> $$
>
> and check only:
>
> $$\boxed{i\leq\sqrt N}
> $$

This converts many:

$$
O(n)
$$

solutions into:

$$
O(\sqrt n)
$$

solutions.

---

# 19. Pattern Recognition — Proper Divisors

> [!important]
> If the question says:
>
> "Sum of factors excluding the number itself"
>
> think:
>
> **Proper divisors.**
>
> Example for `10`:
>
> All divisors:
>
> $$1,2,5,10$$
>
> Proper divisors:
>
> $$1,2,5$$

---

# 20. Pattern Recognition — Perfect vs Composite

A perfect number is always composite.

Why?

A perfect number has at least:

$$
1
$$

and other proper divisors whose sum reaches the number.

For example:

$$
6=1+2+3
$$

Therefore:

$$
\boxed{\text{Every perfect number greater than 1 is composite}}
$$

> [!important]
> But not every composite number is perfect.
>
> Example:
>
> $$8$$
>
> is composite but not perfect.

---

# 21. Perfect vs Deficient vs Abundant

The sum of proper divisors determines the category.

| Category | Condition | Example |
|---|---|---|
| Perfect | Sum = N | 6 |
| Deficient | Sum < N | 8 |
| Abundant | Sum > N | 12 |

### Example

For `6`:

$$
1+2+3=6
$$

Perfect.

For `8`:

$$
1+2+4=7<8
$$

Deficient.

For `12`:

$$
1+2+3+4+6=16>12
$$

Abundant.

---

# 22. Example — Classify 18

## Example 8

### Question

Classify `18` as perfect, deficient, or abundant.

Proper divisors:

$$
1,2,3,6,9
$$

Sum:

$$
1+2+3+6+9=21
$$

Compare:

$$
21>18
$$

Therefore:

$$
\boxed{18\text{ is Abundant}}
$$

---

# 23. Example — Classify 15

## Example 9

### Question

Classify `15`.

Proper divisors:

$$
1,3,5
$$

Sum:

$$
1+3+5=9
$$

Compare:

$$
9<15
$$

Therefore:

$$
\boxed{15\text{ is Deficient}}
$$

---

# 24. Example — Find Perfect Numbers in a Range

## Example 10

### Question

Find perfect numbers from `1` to `100`.

Known perfect numbers in this range:

$$
6,28
$$

Therefore:

$$
\boxed{6,28}
$$

---

# 25. Java Program — Perfect Numbers in a Range

### Code

    static boolean isPerfect(int n) {

        if (n <= 1) {
            return false;
        }

        int sum = 1;

        for (int i = 2; i * i <= n; i++) {

            if (n % i == 0) {

                sum += i;

                int other = n / i;

                if (other != i) {
                    sum += other;
                }
            }
        }

        return sum == n;
    }

    for (int n = 1; n <= 100; n++) {

        if (isPerfect(n)) {
            System.out.print(n + " ");
        }
    }

### Output

    6 28

---

# 26. Example — Count Perfect Numbers

## Example 11

### Question

How many perfect numbers are there from `1` to `100`?

Perfect numbers:

$$
6,28
$$

Count:

$$
2
$$

### Answer

$$
\boxed{2}
$$

---

# 27. Example — Sum of Perfect Numbers

## Example 12

### Question

Find the sum of perfect numbers from `1` to `100`.

Perfect numbers:

$$
6,28
$$

Sum:

$$
6+28=34
$$

### Answer

$$
\boxed{34}
$$

---

# 28. Example — Perfect Number from Factors

## Example 13

### Question

Determine whether `496` is perfect.

Proper divisors:

$$
1,2,4,8,16,31,62,124,248
$$

Sum:

$$
1+2+4+8+16+31+62+124+248
$$

$$
=496
$$

Therefore:

$$
\boxed{496\text{ is a Perfect Number}}
$$

---

# 29. Example — Non-Perfect Number

## Example 14

### Question

Determine whether `20` is perfect.

Proper divisors:

$$
1,2,4,5,10
$$

Sum:

$$
1+2+4+5+10=22
$$

Since:

$$
22\neq20
$$

Therefore:

$$
\boxed{20\text{ is Not a Perfect Number}}
$$

It is abundant because:

$$
22>20
$$

---

# 30. Example — Negative and Zero Inputs

## Example 15

### Question

Check whether:

    -6
    0
    1
    6

are perfect.

### Analysis

    -6 → Not Perfect
     0 → Not Perfect
     1 → Not Perfect
     6 → Perfect

### Answer

$$
\boxed{6\text{ only is Perfect}}
$$

> [!warning]
> Always handle:

$$
n\leq1
$$

before divisor calculations.

---

# 31. Example — Perfect Number in an Array

## Example 16

### Question

Count perfect numbers in:

    6 8 28 12 496 20

Perfect values:

    6
    28
    496

Count:

$$
3
$$

### Answer

$$
\boxed{3}
$$

---

# 32. Example — Sum Perfect Numbers in an Array

## Example 17

### Question

Find the sum of perfect numbers in:

    6 10 28 15 496

Perfect numbers:

$$
6,28,496
$$

Sum:

$$
6+28+496=530
$$

### Answer

$$
\boxed{530}
$$

---

# 33. Mathematical Pattern — Euclid-Euler Form

There is a deeper mathematical relationship between perfect numbers and Mersenne primes.

Every known even perfect number has the form:

$$
\boxed{2^{p-1}(2^p-1)}
$$

where:

$$
2^p-1
$$

is prime.

These are called **Mersenne primes**.

### Example

Take:

$$
p=2
$$

Then:

$$
2^2-1=3
$$

which is prime.

Perfect number:

$$
2^{2-1}(2^2-1)
$$

$$
=2\times3
$$

$$
=6
$$

---

# 34. Example — Generate 28

Take:

$$
p=3
$$

Then:

$$
2^3-1=7
$$

which is prime.

Therefore:

$$
2^{3-1}(2^3-1)
$$

$$
=4\times7
$$

$$
=28
$$

### Answer

$$
\boxed{28}
$$

> [!important]
> This is useful as mathematical background, but for normal placement coding questions, direct divisor checking is usually much simpler.

---

# 35. Perfect Number and Mersenne Prime Relationship

For a prime $p$ where:

$$
2^p-1
$$

is prime, the corresponding even perfect number is:

$$
\boxed{2^{p-1}(2^p-1)}
$$

Examples:

| $p$ | Mersenne Prime | Perfect Number |
|---:|---:|---:|
| 2 | 3 | 6 |
| 3 | 7 | 28 |
| 5 | 31 | 496 |
| 7 | 127 | 8128 |

---

# 36. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Perfect Number

Find proper divisors and calculate their sum.

---

### Pattern 2 — Optimized Perfect Number

Use divisor pairs:

$$
i,\frac ni
$$

and check:

$$
i\leq\sqrt n
$$

---

### Pattern 3 — Perfect Numbers in a Range

Run the perfect-number check for each number.

---

### Pattern 4 — Count Perfect Numbers

Check each number and increment the counter.

---

### Pattern 5 — Sum Perfect Numbers

Check each number and add it when perfect.

---

### Pattern 6 — Classify Number

Compare:

$$
\text{Proper Divisor Sum}
$$

with:

$$
N
$$

Equal → Perfect.

Less → Deficient.

Greater → Abundant.

---

### Pattern 7 — Array of Numbers

For each element:

    if (isPerfect(num)) {
        count++;
    }

---

### Pattern 8 — Divisor Pair Optimization

Whenever divisors are required, think:

$$
\boxed{i\text{ and }n/i}
$$

---

# 37. Shortcuts

> [!tip]
> **Shortcut 1 — Smallest Perfect Number**
>
> Memorize:
>
> $$\boxed{6}$$

> [!tip]
> **Shortcut 2 — First Four Perfect Numbers**
>
> $$\boxed{6,28,496,8128}$$

> [!tip]
> **Shortcut 3 — Start Sum at 1**
>
> For $n>1$, `1` is always a proper divisor.
>
> So:
>
>     int sum = 1;
>
> and begin checking from `2`.

> [!tip]
> **Shortcut 4 — √N Optimization**
>
> Check divisor pairs only up to:
>
> $$\boxed{\sqrt n}$$

> [!tip]
> **Shortcut 5 — Duplicate Square Root Factor**
>
> If:
>
> $$i\times i=n$$
>
> add `i` only once.

> [!tip]
> **Shortcut 6 — Perfect Classification**
>
> Compute:
>
> $$S=\text{sum of proper divisors}$$
>
> Then:
>
> $$S=n\rightarrow Perfect$$
>
> $$S<n\rightarrow Deficient$$
>
> $$S>n\rightarrow Abundant$$

> [!tip]
> **Shortcut 7 — Proving Not Perfect**
>
> You do not need all divisors if you can show the divisor sum is different from `N`.
>
> However, in code, calculate the complete proper-divisor sum safely.

---

# 38. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Including N Itself

For `6`:

Wrong:

$$
1+2+3+6=12
$$

Correct:

$$
1+2+3=6
$$

---

### Mistake 2 — Treating 1 as Perfect

`1` has proper divisor sum:

$$
0
$$

under the positive proper-divisor definition.

Therefore:

$$
\boxed{1\text{ is Not Perfect}}
$$

---

### Mistake 3 — Starting With Sum = 0 and Missing 1

If the loop starts from `2`, you must separately include `1`.

Correct:

    int sum = 1;

for:

$$
n>1
$$

---

### Mistake 4 — Adding the Square Root Divisor Twice

For:

$$
36
$$

the pair at `6` is:

$$
6,6
$$

Add only one `6`.

---

### Mistake 5 — Checking All Numbers Up to N

This works but is unnecessarily slow.

Prefer:

$$
\boxed{O(\sqrt n)}
$$

---

### Mistake 6 — Confusing Perfect With Prime

`6` is perfect but not prime.

In fact:

$$
6=2\times3
$$

So:

$$
\boxed{6\text{ is Composite and Perfect}}
$$

---

### Mistake 7 — Assuming Every Composite Number Is Perfect

False.

Example:

$$
8
$$

is composite, but:

$$
1+2+4=7\neq8
$$

Therefore:

$$
\boxed{8\text{ is Not Perfect}}
$$

---

# 39. Time and Space Complexity

## Basic Method

Check:

$$
1\text{ to }n-1
$$

Time:

$$
\boxed{O(n)}
$$

Space:

$$
\boxed{O(1)}
$$

---

## Optimized Method

Check divisor pairs up to:

$$
\sqrt n
$$

Time:

$$
\boxed{O(\sqrt n)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 40. Recognition Checklist

> [!important] Must Recognize Quickly

**"Check whether N is perfect."**

Think:

$$
\boxed{\text{Proper divisor sum}=N}
$$

---

**"Factors excluding N."**

Think:

$$
\boxed{\text{Proper divisors}}
$$

---

**"Find divisors efficiently."**

Think:

$$
\boxed{i,\ n/i}
$$

and:

$$
\boxed{i\leq\sqrt n}
$$

---

**"Perfect, deficient, or abundant?"**

Think:

$$
S=\text{sum of proper divisors}
$$

Then:

$$
S=N\rightarrow Perfect
$$

$$
S<N\rightarrow Deficient
$$

$$
S>N\rightarrow Abundant
$$

---

**"Find perfect numbers in a range."**

Think:

    for each n
    → calculate proper divisor sum
    → compare with n

---

# 41. Formula Sheet

## Perfect Number

$$
\boxed{
\sum_{\substack{d\mid n\\d<n}}d=n
}
$$

## Proper Divisor

$$
\boxed{d\mid n,\quad d<n}
$$

## Divisor Pair

$$
\boxed{d,\frac nd}
$$

## Optimization Boundary

$$
\boxed{d\leq\sqrt n}
$$

## Classification

$$
\boxed{S=n\rightarrow Perfect}
$$

$$
\boxed{S<n\rightarrow Deficient}
$$

$$
\boxed{S>n\rightarrow Abundant}
$$

## First Perfect Numbers

$$
\boxed{6,28,496,8128}
$$

## Euclid-Euler Form

$$
\boxed{2^{p-1}(2^p-1)}
$$

where:

$$
2^p-1
$$

is prime.

## Complexity

Basic:

$$
\boxed{O(n)}
$$

Optimized:

$$
\boxed{O(\sqrt n)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 42. Quick Revision

> [!summary] One-Minute Revision

    Perfect number
    → Sum of proper divisors equals the number.

    Proper divisor
    → Divisor smaller than N.
    → N itself is excluded.

    Smallest perfect number
    → 6.

    First perfect numbers
    → 6, 28, 496, 8128.

    6:
    → 1 + 2 + 3 = 6.

    28:
    → 1 + 2 + 4 + 7 + 14 = 28.

    Perfect:
    → Divisor sum = N.

    Deficient:
    → Divisor sum < N.

    Abundant:
    → Divisor sum > N.

    1:
    → Not Perfect.

    0:
    → Not Perfect.

    Negative numbers:
    → Not Perfect.

    Basic algorithm:
    → Find proper divisors.
    → Add them.
    → Compare with N.

    Optimized algorithm:
    → Use divisor pairs.
    → Check only up to √N.

    Divisor pair:
    → i and N/i.

    Square-root factor:
    → Add only once.

    Complexity:
    → O(√N).

    Space:
    → O(1).

    Important distinction:
    → Perfect ≠ Prime.
    → 6 is Perfect and Composite.

    Classification:
    → Sum = N → Perfect.
    → Sum < N → Deficient.
    → Sum > N → Abundant.

---

## Golden Memory Trick

**A perfect number gives back itself when you add all its positive divisors except the number itself.**

## One-Line Recognition

**When you see "perfect number," think `proper divisors → sum → compare with N`, preferably using divisor pairs up to `√N`.**