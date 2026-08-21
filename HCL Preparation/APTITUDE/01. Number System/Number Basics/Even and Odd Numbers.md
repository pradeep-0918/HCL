---
type: concept
subject: aptitude
topic: "Even and Odd Numbers"
parent: "01. Number System"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - even-odd
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Natural Numbers]]"
  - "[[Whole Numbers]]"
  - "[[Integers]]"
  - "[[Rational Numbers]]"
---

# Even and Odd Numbers

## 1. Overview

> [!summary] Core Idea
> Every integer is either **even** or **odd**.
>
> An even number is exactly divisible by `2`.
>
> An odd number is not exactly divisible by `2`.

---

## 2. Even Numbers

An integer is **even** if it is divisible by `2` with remainder `0`.

$$
\boxed{n=2k}
$$

where `k` is an integer.

### Examples

$$
\ldots,-6,-4,-2,0,2,4,6,8,\ldots
$$

Therefore:

$$
\boxed{\text{Even Number}=2k}
$$

> [!important] Remember
> `0` is an **even number** because:
>
> $$0=2\times0$$

---

## 3. Odd Numbers

An integer is **odd** if it is not divisible by `2`.

General form:

$$
\boxed{n=2k+1}
$$

where `k` is an integer.

### Examples

$$
\ldots,-5,-3,-1,1,3,5,7,\ldots
$$

Therefore:

$$
\boxed{\text{Odd Number}=2k+1}
$$

---

# 4. Quick Identification

The last digit can be used to identify even and odd numbers.

### Even

A positive integer is even if its last digit is:

$$
\boxed{0,2,4,6,8}
$$

### Odd

A positive integer is odd if its last digit is:

$$
\boxed{1,3,5,7,9}
$$

### Examples

| Number | Last Digit | Type |
|---:|---:|---|
| `124` | `4` | Even |
| `357` | `7` | Odd |
| `890` | `0` | Even |
| `1268` | `8` | Even |
| `913` | `3` | Odd |

> [!tip] Shortcut
> For large numbers, **look only at the last digit**.

---

# 5. Addition Patterns

These patterns are extremely important for aptitude.

### Even + Even

$$
\boxed{\text{Even}+\text{Even}=\text{Even}}
$$

Example:

$$
8+12=20
$$

---

### Odd + Odd

$$
\boxed{\text{Odd}+\text{Odd}=\text{Even}}
$$

Example:

$$
7+9=16
$$

---

### Even + Odd

$$
\boxed{\text{Even}+\text{Odd}=\text{Odd}}
$$

Example:

$$
8+7=15
$$

---

## 6. Addition Pattern Table

| First Number | Second Number | Result |
|---|---|---|
| Even | Even | Even |
| Odd | Odd | Even |
| Even | Odd | Odd |
| Odd | Even | Odd |

> [!tip] Memory Trick
> **Same parity → Even**
>
> **Different parity → Odd**

---

# 7. Subtraction Patterns

### Even − Even

$$
\boxed{\text{Even}-\text{Even}=\text{Even}}
$$

Example:

$$
12-8=4
$$

### Odd − Odd

$$
\boxed{\text{Odd}-\text{Odd}=\text{Even}}
$$

Example:

$$
11-7=4
$$

### Even − Odd

$$
\boxed{\text{Even}-\text{Odd}=\text{Odd}}
$$

Example:

$$
12-7=5
$$

### Odd − Even

$$
\boxed{\text{Odd}-\text{Even}=\text{Odd}}
$$

Example:

$$
11-4=7
$$

---

# 8. Multiplication Patterns

### Even × Even

$$
\boxed{\text{Even}\times\text{Even}=\text{Even}}
$$

### Even × Odd

$$
\boxed{\text{Even}\times\text{Odd}=\text{Even}}
$$

### Odd × Even

$$
\boxed{\text{Odd}\times\text{Even}=\text{Even}}
$$

### Odd × Odd

$$
\boxed{\text{Odd}\times\text{Odd}=\text{Odd}}
$$

> [!important] Golden Rule
> **If at least one factor is even, the product is even.**
>
> The product is odd **only when every factor is odd**.

---

# 9. Division Patterns

Division is different from addition, subtraction, and multiplication.

An integer divided by another integer may or may not produce an integer.

Examples:

$$
\frac{8}{2}=4
$$

but:

$$
\frac{7}{2}=3.5
$$

Therefore, do not apply simple even/odd rules to division without checking the actual result.

> [!warning] Common Trap
> **Even ÷ Odd** is not always an integer.
>
> Example:
>
> $$8\div3=\frac83$$
>
> which is not an integer.

---

# 10. Consecutive Numbers

Consecutive integers differ by `1`.

Example:

$$
1,2,3,4,5,6
$$

The parity alternates:

$$
\text{Odd},\text{Even},\text{Odd},\text{Even},\ldots
$$

### Important Pattern

Among any **two consecutive integers**:

$$
\boxed{\text{One is even and one is odd}}
$$

Example:

$$
20,21
$$

`20` → Even  
`21` → Odd

---

# 11. Consecutive Even Numbers

Consecutive even numbers differ by `2`.

General form:

$$
\boxed{2n,\ 2n+2,\ 2n+4,\ldots}
$$

Example:

$$
4,6,8,10,12
$$

### Number of Terms

If the first term is `a` and last term is `b`:

$$
\boxed{n=\frac{b-a}{2}+1}
$$

---

# 12. Consecutive Odd Numbers

Consecutive odd numbers also differ by `2`.

General form:

$$
\boxed{2n+1,\ 2n+3,\ 2n+5,\ldots}
$$

Example:

$$
3,5,7,9,11
$$

### Number of Terms

If the first term is `a` and last term is `b`:

$$
\boxed{n=\frac{b-a}{2}+1}
$$

---

# 13. Sum of First `n` Even Numbers

The first `n` even numbers are:

$$
2,4,6,\ldots,2n
$$

Their sum is:

$$
\boxed{S=n(n+1)}
$$

### Example

Find the sum of the first `10` even numbers.

$$
S=10(11)
$$

$$
\boxed{110}
$$

---

# 14. Sum of First `n` Odd Numbers

The first `n` odd numbers are:

$$
1,3,5,\ldots,(2n-1)
$$

Their sum is:

$$
\boxed{S=n^2}
$$

### Example

Find the sum of the first `10` odd numbers.

$$
S=10^2
$$

$$
\boxed{100}
$$

> [!tip] Must Memorize
>
> **First `n` even numbers → `n(n+1)`**
>
> **First `n` odd numbers → `n²`**

---

# 15. Product Patterns

### Product of Consecutive Integers

If two consecutive integers are:

$$
n,\ n+1
$$

then their product is:

$$
\boxed{n(n+1)}
$$

Since one of two consecutive integers is always even:

$$
\boxed{\text{Product of two consecutive integers is always even}}
$$

### Example

$$
11\times12=132
$$

Therefore, the product is even.

---

# 16. Product of Consecutive Integers

Among any:

- `2` consecutive integers → at least one is divisible by `2`
- `3` consecutive integers → at least one is divisible by `3`
- `4` consecutive integers → at least one is divisible by `4`
- `n` consecutive integers → their product is divisible by `n!`

For example:

$$
5\times6\times7
$$

is divisible by:

$$
3!=6
$$

> [!important] Advanced Pattern
> The product of `n` consecutive integers is always divisible by:
>
> $$\boxed{n!}$$

---

# 17. Important Aptitude Patterns

## Pattern 1 — Determine the Result Without Calculation

### Question

Is the following sum even or odd?

$$
12345+67890
$$

Check the parity:

`12345` → Odd

`67890` → Even

Therefore:

$$
\boxed{\text{Odd}+\text{Even}=\text{Odd}}
$$

No actual addition is required.

> [!tip] Exam Pattern
> If the question asks only for **even/odd**, do not calculate the entire expression.

---

## Pattern 2 — Product Sign

### Question

Is:

$$
37\times48\times91
$$

even or odd?

Since `48` is even:

$$
\boxed{\text{Product is even}}
$$

You do not need to multiply.

---

## Pattern 3 — Multiple Odd Numbers

### Question

Determine whether:

$$
13\times17\times21
$$

is even or odd.

All three factors are odd.

Therefore:

$$
\boxed{\text{Odd}}
$$

---

## Pattern 4 — Sum of Several Odd Numbers

### Important Rule

The sum of:

- Even number of odd numbers → Even
- Odd number of odd numbers → Odd

### Example

$$
1+3+5+7
$$

There are `4` odd numbers.

Therefore:

$$
\boxed{\text{Even}}
$$

### Another Example

$$
1+3+5+7+9
$$

There are `5` odd numbers.

Therefore:

$$
\boxed{\text{Odd}}
$$

> [!tip] Shortcut
> **Count the number of odd terms.**
>
> Even count → Even sum.
>
> Odd count → Odd sum.

---

# 18. Power Patterns

## Even Number Raised to Any Positive Integer

If `n` is even:

$$
\boxed{n^k=\text{Even}}
$$

for every positive integer `k`.

Example:

$$
4^5
$$

is even.

---

## Odd Number Raised to Any Positive Integer

If `n` is odd:

$$
\boxed{n^k=\text{Odd}}
$$

for every positive integer `k`.

Example:

$$
7^{100}
$$

is odd.

> [!important] Shortcut
> **Even base → Even power**
>
> **Odd base → Odd power**

---

# 19. Algebraic Parity Patterns

Let:

$$
n\in\mathbb Z
$$

### If `n` is even

$$
n=2k
$$

Then:

$$
n^2=(2k)^2=4k^2
$$

Therefore:

$$
\boxed{n^2\text{ is even}}
$$

### If `n` is odd

$$
n=2k+1
$$

Then:

$$
n^2=(2k+1)^2
$$

$$
=4k^2+4k+1
$$

$$
=2(2k^2+2k)+1
$$

Therefore:

$$
\boxed{n^2\text{ is odd}}
$$

---

# 20. Important Formula Sheet

> [!important] Must Remember

| Concept | Formula / Rule |
|---|---|
| Even number | `2n` |
| Odd number | `2n + 1` |
| First `n` even numbers | `2,4,6,...,2n` |
| Sum of first `n` even numbers | `n(n+1)` |
| First `n` odd numbers | `1,3,5,...,2n-1` |
| Sum of first `n` odd numbers | `n²` |
| Consecutive even numbers | `2n, 2n+2, ...` |
| Consecutive odd numbers | `2n+1, 2n+3, ...` |
| Number of consecutive even/odd terms | `(Last-First)/2 + 1` |
| Product of two consecutive integers | Always even |
| Product of `n` consecutive integers | Divisible by `n!` |

---

# 21. Parity Pattern Table

> [!important] Quick Reference

### Addition

| Operation | Result |
|---|---|
| Even + Even | Even |
| Even + Odd | Odd |
| Odd + Even | Odd |
| Odd + Odd | Even |

### Subtraction

| Operation | Result |
|---|---|
| Even − Even | Even |
| Even − Odd | Odd |
| Odd − Even | Odd |
| Odd − Odd | Even |

### Multiplication

| Operation | Result |
|---|---|
| Even × Even | Even |
| Even × Odd | Even |
| Odd × Even | Even |
| Odd × Odd | Odd |

---

# 22. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Thinking `0` is odd.
- ❌ Forgetting that negative numbers can be even or odd.
- ❌ Multiplying large numbers when only parity is required.
- ❌ Assuming even ÷ odd is always an integer.
- ❌ Forgetting that the sum of two odd numbers is even.
- ❌ Thinking odd × even is odd.
- ❌ Confusing consecutive integers with consecutive even/odd integers.
- ❌ Forgetting that consecutive even/odd numbers differ by `2`.
- ❌ Forgetting that the product of two consecutive integers is always even.

---

# 23. Exam Strategy

> [!tip] Fast Approach

When you see an even/odd question:

1. Look at the last digit if dealing with large positive integers.
2. For addition/subtraction, use parity rules.
3. For multiplication, check whether **at least one factor is even**.
4. For powers, check only the base.
5. For a sum of many odd numbers, count the number of terms.
6. For consecutive numbers, identify whether the sequence changes by `1` or `2`.
7. Do not perform unnecessary calculations.

---

# 24. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Even and odd identification
2. Addition parity
3. Subtraction parity
4. Multiplication parity
5. Powers of even/odd numbers
6. Sum of odd numbers
7. Sum of even numbers
8. Consecutive integers
9. Consecutive even/odd numbers
10. Product of consecutive integers

---

# 25. Practice Checklist

- [ ] Identify even numbers quickly
- [ ] Identify odd numbers quickly
- [ ] Memorize `2n` and `2n+1`
- [ ] Practice addition parity
- [ ] Practice subtraction parity
- [ ] Practice multiplication parity
- [ ] Practice power parity
- [ ] Practice sums of odd numbers
- [ ] Practice sums of even numbers
- [ ] Practice consecutive-number patterns
- [ ] Practice parity-based aptitude questions
- [ ] Revise common traps

---

# 26. Related Topics

- [[01. Number System]]
- [[Natural Numbers]]
- [[Whole Numbers]]
- [[Integers]]
- [[Positive and Negative Numbers]]
- [[Prime and Composite Numbers]]
- [[Divisibility Rules]]
- [[Factors]]
- [[Multiples]]
- [[Remainders]]

---

# 27. Quick Revision

> [!summary] One-Minute Revision

### Even

$$
\boxed{2n}
$$

### Odd

$$
\boxed{2n+1}
$$

### Addition

$$
\boxed{
\begin{aligned}
E+E&=E\\
E+O&=O\\
O+O&=E
\end{aligned}
}
$$

### Multiplication

$$
\boxed{
\begin{aligned}
E\times E&=E\\
E\times O&=E\\
O\times O&=O
\end{aligned}
}
$$

### First `n` Even Numbers

$$
\boxed{2,4,6,\ldots,2n}
$$

### Sum

$$
\boxed{n(n+1)}
$$

### First `n` Odd Numbers

$$
\boxed{1,3,5,\ldots,2n-1}
$$

### Sum

$$
\boxed{n^2}
$$

### Key Patterns

> **At least one even factor → Product is even.**

> **All factors odd → Product is odd.**

> **Even number of odd terms → Even sum.**

> **Odd number of odd terms → Odd sum.**