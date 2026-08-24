---
type: concept
subject: coding
topic: "Composite Number"
parent: "Number Basics"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - number-problems
  - number-basics
  - composite-number
  - java
  - factors
  - divisibility
wikilinks:
  - "[[Number Basics]]"
  - "[[Prime Number]]"
  - "[[GCD and LCM]]"
  - "[[Divisibility]]"
  - "[[Factorial]]"
---

# Composite Number

## 1. Core Concept

> [!summary]
> A **composite number** is a positive integer greater than `1` that has **more than two positive factors**.
>
> In simple words:
>
> **If a number greater than 1 can be divided exactly by a number other than `1` and itself, it is composite.**

Example:

$$
6
$$

Factors:

$$
1,2,3,6
$$

Since it has more than two factors:

$$
\boxed{6\text{ is Composite}}
$$

A number greater than `1` is either:

- Prime
- Composite

except that `1` belongs to neither category.

---

# 2. Basic Meaning

## Prime Number

A prime number has exactly two positive factors:

$$
1\text{ and itself}
$$

Example:

$$
7\rightarrow 1,7
$$

Therefore:

$$
\boxed{7\text{ is Prime}}
$$

## Composite Number

A composite number has more than two positive factors.

Example:

$$
12\rightarrow1,2,3,4,6,12
$$

Therefore:

$$
\boxed{12\text{ is Composite}}
$$

---

# 3. Main Formula

For an integer $n$:

$$
\boxed{n>1}
$$

and if there exists some integer $d$ such that:

$$
1<d<n
$$

and:

$$
n\%d=0
$$

then:

$$
\boxed{n\text{ is Composite}}
$$

Another useful relationship:

$$
\boxed{\text{Composite}=\text{Greater than 1 and Not Prime}}
$$

---

# 4. Important Properties

## Property 1 — Composite Numbers Are Greater Than 1

Examples:

$$
4,6,8,9,10,12,\ldots
$$

All are greater than `1`.

---

## Property 2 — 1 Is Not Composite

The number `1` has only one positive factor:

$$
1
$$

Therefore:

$$
\boxed{1\text{ is Neither Prime nor Composite}}
$$

---

## Property 3 — 0 Is Not Composite

Composite numbers must be positive integers greater than `1`.

Therefore:

$$
\boxed{0\text{ is Not Composite}}
$$

---

## Property 4 — Negative Numbers Are Not Composite

Composite numbers are positive integers greater than `1`.

Therefore:

$$
-4,-6,-8
$$

are not composite numbers under the standard definition.

---

## Property 5 — Every Even Number Greater Than 2 Is Composite

Any even number greater than `2` is divisible by:

$$
2
$$

Example:

$$
18\%2=0
$$

Therefore:

$$
\boxed{18\text{ is Composite}}
$$

---

## Property 6 — Every Composite Number Has a Factor Pair

Example:

$$
20
$$

Factor pairs:

$$
1\times20
$$

$$
2\times10
$$

$$
4\times5
$$

Therefore, `20` is composite.

---

## Property 7 — Every Composite Number Has a Prime Factor

Example:

$$
84=2^2\times3\times7
$$

Its prime factors are:

$$
2,3,7
$$

---

# 5. Basic Examples

## Example 1 — Check 4

### Question

Is `4` composite?

### Factors

$$
1,2,4
$$

There are more than two factors.

Therefore:

$$
\boxed{4\text{ is Composite}}
$$

---

## Example 2 — Check 9

### Question

Is `9` composite?

Factors:

$$
1,3,9
$$

There are three factors.

Therefore:

$$
\boxed{9\text{ is Composite}}
$$

---

## Example 3 — Check 15

### Question

Is `15` composite?

We find:

$$
15\%3=0
$$

Since `3` is neither `1` nor `15`, a proper divisor exists.

Therefore:

$$
\boxed{15\text{ is Composite}}
$$

---

# 6. Prime vs Composite

| Number | Factors | Classification |
|---:|---|---|
| 1 | 1 | Neither |
| 2 | 1, 2 | Prime |
| 3 | 1, 3 | Prime |
| 4 | 1, 2, 4 | Composite |
| 5 | 1, 5 | Prime |
| 6 | 1, 2, 3, 6 | Composite |
| 7 | 1, 7 | Prime |
| 8 | 1, 2, 4, 8 | Composite |
| 9 | 1, 3, 9 | Composite |
| 10 | 1, 2, 5, 10 | Composite |

> [!important]
> The easiest classification rule is:
>
> `1` → Neither
>
> `2 or more` → Prime or Composite
>
> Exactly two factors → Prime
>
> More than two factors → Composite

---

# 7. Basic Java Program

## Example 4

### Question

Write a Java program to check whether a number is composite.

### Code

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            boolean isComposite = false;

            if (n > 3) {

                for (int i = 2; i < n; i++) {

                    if (n % i == 0) {
                        isComposite = true;
                        break;
                    }
                }
            }

            if (isComposite) {
                System.out.println("Composite");
            } else {
                System.out.println("Not Composite");
            }
        }
    }

### Logic

    n <= 1
    → Not Composite

    n > 1
    → Search for a proper divisor

    divisor found
    → Composite

    no divisor
    → Prime

---

# 8. Optimized Composite Check

There is no need to test every number up to `n - 1`.

We only need to check up to:

$$
\sqrt n
$$

### Code

    static boolean isComposite(int n) {

        if (n <= 3) {
            return false;
        }

        for (int i = 2; i * i <= n; i++) {

            if (n % i == 0) {
                return true;
            }
        }

        return false;
    }

### Complexity

$$
\boxed{O(\sqrt n)}
$$

> [!important]
> A composite number must have at least one factor less than or equal to $\sqrt n$.

---

# 9. Example — Composite Check Using √N

## Example 5

### Question

Check whether `49` is composite.

### Step 1

$$
49>1
$$

### Step 2

$$
\sqrt{49}=7
$$

Check divisors:

$$
2,3,4,5,6,7
$$

At `7`:

$$
49\%7=0
$$

Therefore:

$$
\boxed{49\text{ is Composite}}
$$

---

# 10. Example — Number 29

## Example 6

### Question

Is `29` composite?

Calculate:

$$
\sqrt{29}\approx5.38
$$

Check:

$$
2,3,4,5
$$

None divides `29`.

Therefore:

$$
\boxed{29\text{ is Not Composite}}
$$

Since `29 > 1` and is not composite:

$$
\boxed{29\text{ is Prime}}
$$

---

# 11. Shortcut — Even Numbers

> [!tip]
> If:
>
> $$n>2$$
>
> and `n` is even, immediately conclude:
>
> $$\boxed{Composite}$$

Example:

$$
42
$$

Since:

$$
42\%2=0
$$

and:

$$
42>2
$$

therefore:

$$
\boxed{42\text{ is Composite}}
$$

---

# 12. Shortcut — Numbers Ending in 5

For a number greater than `5`, if the last digit is `5`, it is divisible by `5`.

Example:

$$
125
$$

$$
125\%5=0
$$

Since:

$$
125>5
$$

therefore:

$$
\boxed{125\text{ is Composite}}
$$

> [!important]
> `5` itself is prime.
>
> Therefore, the shortcut applies to numbers **greater than 5**.

---

# 13. Shortcut — Divisibility by 3

If the digit sum is divisible by `3`, the number is divisible by `3`.

Example:

$$
123
$$

Digit sum:

$$
1+2+3=6
$$

Since:

$$
6\%3=0
$$

and:

$$
123>3
$$

therefore:

$$
\boxed{123\text{ is Composite}}
$$

---

# 14. Example — Quick Composite Detection

## Example 7

### Question

Is `231` composite?

Digit sum:

$$
2+3+1=6
$$

Since:

$$
6\%3=0
$$

`231` is divisible by `3`.

Therefore:

$$
\boxed{231\text{ is Composite}}
$$

No square-root calculation is required.

---

# 15. Example — Large Even Number

## Example 8

### Question

Is:

$$
98765432
$$

composite?

The last digit is:

$$
2
$$

Therefore the number is even.

It is also greater than `2`.

Hence:

$$
\boxed{98765432\text{ is Composite}}
$$

No complete division is needed.

---

# 16. Composite Number Recognition

> [!important]
> **If the question says "Check whether N is composite":**
>
> Think:
>
> 1. Is $n\leq1$?
> 2. If yes → Not Composite.
> 3. Otherwise search for a divisor from `2` to $\sqrt n$.
> 4. If any divisor exists → Composite.
> 5. Otherwise → Prime, so not composite.

---

# 17. Example — Count Composite Numbers

## Example 9

### Question

How many composite numbers are there from `1` to `10`?

Numbers:

    1 → Neither
    2 → Prime
    3 → Prime
    4 → Composite
    5 → Prime
    6 → Composite
    7 → Prime
    8 → Composite
    9 → Composite
    10 → Composite

Composite numbers:

$$
4,6,8,9,10
$$

Count:

$$
5
$$

### Answer

$$
\boxed{5}
$$

---

# 18. Formula — Count Composite Numbers

For positive integers from `1` to `N`:

$$
\boxed{
\text{Composite Count}
=
N-\text{Prime Count}-1
}
$$

Why subtract `1`?

Because `1` is neither prime nor composite.

### Example

From `1` to `10`:

$$
N=10
$$

Prime numbers:

$$
2,3,5,7
$$

Prime count:

$$
4
$$

Therefore:

$$
10-4-1=5
$$

### Answer

$$
\boxed{5}
$$

---

# 19. Example — Count Composite Numbers from 1 to 20

Prime numbers:

    2 3 5 7 11 13 17 19

Prime count:

$$
8
$$

Total numbers:

$$
20
$$

Number `1` is neither.

Therefore:

$$
20-8-1=11
$$

### Answer

$$
\boxed{11\text{ Composite Numbers}}
$$

---

# 20. Composite Numbers in a Range

For the range:

$$
[L,R]
$$

the number of integers is:

$$
R-L+1
$$

If you know the number of primes in the range, then:

$$
\boxed{
\text{Composite Count}
=
(R-L+1)-\text{Prime Count}-\text{Neither Count}
}
$$

For ranges containing only numbers greater than `1`, there is no "neither" value.

Therefore:

$$
\boxed{
\text{Composite Count}
=
\text{Total Count}-\text{Prime Count}
}
$$

---

# 21. Example — Composite Numbers in a Range

## Example 10

### Question

How many composite numbers are between `5` and `15`, inclusive?

Numbers:

    5 6 7 8 9 10 11 12 13 14 15

Total:

$$
15-5+1=11
$$

Prime numbers:

    5 7 11 13

Prime count:

$$
4
$$

All numbers are greater than `1`.

Therefore:

$$
11-4=7
$$

### Answer

$$
\boxed{7}
$$

---

# 22. Example — Sum of Composite Numbers

## Example 11

### Question

Find the sum of composite numbers from `1` to `10`.

Composite numbers:

    4 6 8 9 10

Calculation:

$$
4+6+8+9+10=37
$$

### Answer

$$
\boxed{37}
$$

---

# 23. Example — Largest Composite Number

## Example 12

### Question

Find the largest composite number less than `20`.

The largest candidates:

    19 → Prime
    18 → Composite

Therefore:

$$
\boxed{18}
$$

---

# 24. Example — Smallest Composite Number

## Example 13

### Question

Find the smallest composite number.

Check:

$$
1\rightarrow Neither
$$

$$
2\rightarrow Prime
$$

$$
3\rightarrow Prime
$$

$$
4\rightarrow Composite
$$

Therefore:

$$
\boxed{4}
$$

> [!important]
> **4 is the smallest composite number.**

---

# 25. Composite Factorization

A composite number can be expressed as a product of smaller positive integers.

Example:

$$
12=3\times4
$$

or:

$$
12=2\times6
$$

or prime factorization:

$$
12=2^2\times3
$$

Therefore, `12` is composite.

---

# 26. Example — Determine Composite Using Factor Pair

## Example 14

### Question

Is `35` composite?

Find a factor pair:

$$
35=5\times7
$$

Since both factors are smaller than `35`:

$$
\boxed{35\text{ is Composite}}
$$

---

# 27. Factor Pair Shortcut

> [!tip]
> To prove that a number is composite, you only need to find **one proper factor**.
>
> Example:
>
> $$77\%7=0$$
>
> Therefore:
>
> $$77=7\times11$$
>
> So:
>
> $$\boxed{77\text{ is Composite}}$$

You do not need to find all factors.

---

# 28. Example — Prove Composite Quickly

## Example 15

### Question

Prove that `91` is composite.

Find a divisor:

$$
91\%7=0
$$

Therefore:

$$
91=7\times13
$$

Hence:

$$
\boxed{91\text{ is Composite}}
$$

---

# 29. Pattern Recognition — Proper Divisor

> [!important]
> If a number greater than `1` has a divisor other than `1` and itself:
>
> Think:
>
> $$\boxed{Composite}$$

Example:

$$
27\%3=0
$$

Therefore:

$$
\boxed{27\text{ is Composite}}
$$

---

# 30. Pattern Recognition — Factor Pair

> [!important]
> If you can write:
>
> $$n=a\times b$$
>
> where:
>
> $$1<a<n$$
>
> and:
>
> $$1<b<n$$
>
> then:
>
> $$\boxed{n\text{ is Composite}}
> $$

Example:

$$
36=4\times9
$$

Therefore:

$$
\boxed{36\text{ is Composite}}
$$

---

# 31. Pattern Recognition — Even Number

> [!important]
> If:
>
> $$n>2$$
>
> and `n` is even:
>
> $$\boxed{Composite}$$

---

# 32. Pattern Recognition — Number Ending in 5

> [!important]
> If:
>
> $$n>5
> $$
>
> and the last digit is `5`:
>
> $$\boxed{Composite}$$

---

# 33. Pattern Recognition — Digit Sum Divisible by 3

> [!important]
> If the digit sum is divisible by `3` and the number is greater than `3`:
>
> $$\boxed{Composite}$$

Example:

$$
222
$$

Digit sum:

$$
2+2+2=6
$$

Therefore divisible by `3`.

So:

$$
\boxed{222\text{ is Composite}}
$$

---

# 34. Prime and Composite Relationship

For every integer:

$$
n>1
$$

exactly one of the following is true:

$$
\boxed{Prime}
$$

or:

$$
\boxed{Composite}
$$

A number cannot be both.

Example:

`17` is prime, so it is not composite.

`18` is composite, so it is not prime.

> [!important]
> The exception is `1`, which is neither.

---

# 35. Advanced Example — Classify Several Numbers

## Example 16

### Question

Classify:

    1, 2, 4, 7, 9, 13, 15, 17, 21

### Analysis

    1  → Neither
    2  → Prime
    4  → Composite
    7  → Prime
    9  → Composite
    13 → Prime
    15 → Composite
    17 → Prime
    21 → Composite

### Answer

Prime:

$$
\boxed{2,7,13,17}
$$

Composite:

$$
\boxed{4,9,15,21}
$$

Neither:

$$
\boxed{1}
$$

---

# 36. Advanced Example — Composite Using √N

## Example 17

### Question

Check whether `221` is composite.

Calculate:

$$
\sqrt{221}\approx14.86
$$

Check possible divisors:

$$
2,3,5,7,11,13
$$

We find:

$$
221\%13=0
$$

Therefore:

$$
221=13\times17
$$

Hence:

$$
\boxed{221\text{ is Composite}}
$$

---

# 37. Advanced Example — Candidate Number

## Example 18

### Question

Check whether `101` is composite.

Calculate:

$$
\sqrt{101}\approx10.05
$$

Possible divisors:

$$
2,3,5,7
$$

Also check:

$$
11>\sqrt{101}
$$

so no need to check `11`.

Calculations:

    101 % 2 != 0
    101 % 3 != 0
    101 % 5 != 0
    101 % 7 != 0

No divisor exists.

Therefore:

$$
\boxed{101\text{ is Prime}}
$$

So:

$$
\boxed{101\text{ is Not Composite}}
$$

---

# 38. Advanced Example — Count Composite Numbers in an Array

## Example 19

### Question

Count composite numbers in:

    2 4 7 9 11 15 17 20

### Classification

    2  → Prime
    4  → Composite
    7  → Prime
    9  → Composite
    11 → Prime
    15 → Composite
    17 → Prime
    20 → Composite

Composite values:

    4 9 15 20

Count:

$$
4
$$

### Answer

$$
\boxed{4}
$$

---

# 39. Java Function for Composite Number

A clean reusable method:

    static boolean isComposite(int n) {

        if (n <= 3) {
            return false;
        }

        for (int i = 2; i * i <= n; i++) {

            if (n % i == 0) {
                return true;
            }
        }

        return false;
    }

Usage:

    if (isComposite(n)) {
        System.out.println("Composite");
    } else {
        System.out.println("Not Composite");
    }

---

# 40. Composite Number and Prime Number Together

A useful approach is to create one prime-check function.

    static boolean isPrime(int n) {

        if (n < 2) {
            return false;
        }

        for (int i = 2; i * i <= n; i++) {

            if (n % i == 0) {
                return false;
            }
        }

        return true;
    }

Then:

    if (n > 1 && !isPrime(n)) {
        System.out.println("Composite");
    }

This works because every integer greater than `1` that is not prime is composite.

> [!tip]
> In many coding problems, it is easier to implement `isPrime()` once and derive composite status from it.

---

# 41. Time Complexity

### Basic Composite Check

If we check every divisor from:

$$
2\text{ to }n-1
$$

complexity:

$$
\boxed{O(n)}
$$

### Optimized Composite Check

If we stop at:

$$
\sqrt n
$$

complexity:

$$
\boxed{O(\sqrt n)}
$$

### Space Complexity

Only a few variables are required:

$$
\boxed{O(1)}
$$

---

# 42. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Composite

Check whether any divisor exists between:

$$
2\text{ and }\sqrt n
$$

---

### Pattern 2 — Count Composite Numbers

Loop through the range and count composite values.

---

### Pattern 3 — Sum Composite Numbers

Check each number and add it when composite.

---

### Pattern 4 — Find Smallest Composite

Remember:

$$
\boxed{4}
$$

---

### Pattern 5 — Find Largest Composite Below N

Start from:

$$
N-1
$$

and move downward until a composite number is found.

---

### Pattern 6 — Composite in a Range

For numbers greater than `1`:

$$
\text{Composite Count}
=
\text{Total Count}-\text{Prime Count}
$$

---

### Pattern 7 — Prove Composite

Find one proper divisor.

---

### Pattern 8 — Large Number

Use quick divisibility checks first, then:

$$
\sqrt n
$$

---

# 43. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Calling 1 Composite

Wrong:

$$
1\rightarrow Composite
$$

Correct:

$$
\boxed{1\text{ is Neither Prime nor Composite}}
$$

---

### Mistake 2 — Calling 2 Composite

`2` is even, but it is the only even prime.

Therefore:

$$
\boxed{2\text{ is Prime}}
$$

---

### Mistake 3 — Assuming Every Odd Number Is Prime

Wrong:

$$
91\rightarrow Prime
$$

Correct:

$$
91=7\times13
$$

Therefore:

$$
\boxed{91\text{ is Composite}}
$$

---

### Mistake 4 — Checking All Divisors

You do not need to check up to `n - 1`.

Use:

$$
\boxed{\sqrt n}
$$

---

### Mistake 5 — Forgetting the Number Must Be Greater Than 1

Numbers:

    -5
    -1
    0
    1

are not composite.

---

### Mistake 6 — Confusing "Not Prime" With "Composite"

For integers greater than `1`:

$$
Not\ Prime=Composite
$$

But for `1`:

$$
1=Neither
$$

So always check:

$$
n>1
$$

first.

---

# 44. Shortcuts

> [!tip]
> **Shortcut 1 — Even Number**
>
> If $n>2$ and even:
>
> $$\boxed{Composite}$$

> [!tip]
> **Shortcut 2 — Last Digit 5**
>
> If $n>5$ and ends in `5`:
>
> $$\boxed{Composite}$$

> [!tip]
> **Shortcut 3 — Digit Sum**
>
> If digit sum is divisible by `3` and $n>3$:
>
> $$\boxed{Composite}$$

> [!tip]
> **Shortcut 4 — One Factor Is Enough**
>
> To prove composite, you only need one proper divisor.

> [!tip]
> **Shortcut 5 — √N**
>
> For a complete check, stop at:
>
> $$\boxed{\sqrt n}$$

> [!tip]
> **Shortcut 6 — Smallest Composite**
>
> Memorize:
>
> $$\boxed{4}$$

> [!tip]
> **Shortcut 7 — Count Composite Numbers**
>
> For numbers from `2` to `N`:
>
> $$\boxed{Composite=N-1-PrimeCount}$$

---

# 45. Recognition Checklist

> [!important] Must Recognize Quickly

**"Is N composite?"**

Think:

$$
n\leq1\rightarrow Not\ Composite
$$

Otherwise:

$$
\text{Search divisor up to }\sqrt n
$$

---

**"Find a composite number."**

Think:

**Find any number greater than `1` having a proper divisor.**

---

**"Prove N is composite."**

Think:

**Find one divisor other than `1` and N.**

---

**"Count composite numbers from 1 to N."**

Think:

$$
\boxed{N-PrimeCount-1}
$$

---

**"Number is even and greater than 2."**

Think:

$$
\boxed{Composite}
$$

---

**"Number ends with 5 and is greater than 5."**

Think:

$$
\boxed{Composite}
$$

---

**"Digit sum divisible by 3 and N > 3."**

Think:

$$
\boxed{Composite}
$$

---

# 46. Formula Sheet

## Composite Definition

$$
\boxed{\text{Composite}=\text{Positive integer greater than 1 with more than two factors}}
$$

## Composite Test

$$
\boxed{
n>1
\text{ and }
\exists d,\ 1<d<n,\ n\%d=0
}
$$

## Optimized Test

$$
\boxed{
\exists d,\ 2\leq d\leq\sqrt n,\ n\%d=0
}
$$

## Smallest Composite

$$
\boxed{4}
$$

## Composite Count from 1 to N

$$
\boxed{
N-PrimeCount-1
}
$$

## Composite Count from L to R

For $L\geq2$:

$$
\boxed{
(R-L+1)-PrimeCount(L,R)
}
$$

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

# 47. Quick Revision

> [!summary] One-Minute Revision

    Composite number
    → Positive integer greater than 1.
    → Has more than two positive factors.

    Prime
    → Exactly two positive factors.

    Composite
    → More than two positive factors.

    1
    → Neither Prime nor Composite.

    0
    → Not Composite.

    Negative numbers
    → Not Composite.

    Smallest composite
    → 4.

    Every even number greater than 2
    → Composite.

    Number greater than 5 ending in 5
    → Composite.

    Number greater than 3 with digit sum divisible by 3
    → Composite.

    To prove composite
    → Find one proper divisor.

    Complete composite check
    → Test divisors up to √N.

    Composite complexity
    → O(√N).

    Composite count from 1 to N
    → N - PrimeCount - 1.

    Composite count from 2 to N
    → N - 1 - PrimeCount.

    Prime factorization
    → Every composite number can be broken into prime factors.

    Main coding condition
    → n % i == 0.

    Main optimization
    → Stop when i * i > n.

    Main trap
    → "Not Prime" and "Composite" are equivalent only when n > 1.

---

## Golden Memory Trick

**A number greater than 1 is composite as soon as you find one divisor other than 1 and itself.**

## One-Line Recognition

**When you see "composite," think `n > 1` and search for any divisor from `2` through `√n`.**