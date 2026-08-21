---
type: concept
subject: aptitude
topic: "Irrational Numbers"
parent: "01. Number System"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - irrational-numbers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Rational Numbers]]"
  - "[[Real Numbers]]"
  - "[[Integers]]"
---

# Irrational Numbers

## 1. Overview

> [!summary] Core Idea
> An irrational number is a real number that **cannot be expressed in the form `p/q`**, where `p` and `q` are integers and `q ≠ 0`.

In other words:

$$
\boxed{\text{Irrational Number}\neq\frac{p}{q}}
$$

where:

$$
p,q\in\mathbb{Z},\qquad q\neq0
$$

### Common Examples

$$
\sqrt{2},\quad\sqrt{3},\quad\sqrt{5},\quad\sqrt{7},\quad\pi
$$

Examples of irrational numbers:

- $\sqrt{2}$
- $\sqrt{3}$
- $\sqrt{5}$
- $\sqrt{7}$
- $\pi$
- $e$

---

## 2. Rational vs Irrational Numbers

> [!important] Fundamental Difference

| Rational Numbers | Irrational Numbers |
|---|---|
| Can be written as `p/q` | Cannot be written as `p/q` |
| Decimal terminates or repeats | Decimal is non-terminating and non-repeating |
| Examples: `1/2`, `3/4`, `0.25` | Examples: `√2`, `√3`, `π` |

### Decimal Representation

#### Rational

A rational number has a decimal expansion that is:

- Terminating, or
- Non-terminating recurring

Examples:

$$
\frac{1}{2}=0.5
$$

$$
\frac{1}{3}=0.333\ldots
$$

#### Irrational

An irrational number has a decimal expansion that is:

- Non-terminating
- Non-repeating

Example:

$$
\sqrt{2}=1.41421356237\ldots
$$

> [!tip] Recognition Pattern
> **Terminating → Rational**
>
> **Recurring → Rational**
>
> **Non-terminating + Non-repeating → Irrational**

---

# 3. Square Roots

Square roots are one of the most common sources of irrational numbers.

### Perfect Squares

The square root of a perfect square is rational.

Examples:

$$
\sqrt{1}=1
$$

$$
\sqrt{4}=2
$$

$$
\sqrt{9}=3
$$

$$
\sqrt{16}=4
$$

$$
\sqrt{25}=5
$$

Therefore:

$$
\boxed{\sqrt{\text{Perfect Square}}=\text{Rational}}
$$

---

### Non-Perfect Squares

The square root of a positive integer that is **not a perfect square** is irrational.

Examples:

$$
\sqrt{2},\quad\sqrt{3},\quad\sqrt{5},\quad\sqrt{6},\quad\sqrt{7}
$$

Therefore:

$$
\boxed{\sqrt{\text{Non-Perfect Square}}=\text{Irrational}}
$$

> [!important] Exam Shortcut
> For a positive integer `n`:
>
> $$\sqrt n$$
>
> is rational **if and only if `n` is a perfect square**.

---

# 4. Simplifying Surds

A square root may look irrational but can sometimes simplify.

Example:

$$
\sqrt{12}
$$

Factor `12`:

$$
12=4\times3
$$

Therefore:

$$
\sqrt{12}
=
\sqrt{4\times3}
$$

$$
=2\sqrt3
$$

Since $\sqrt3$ is irrational:

$$
\boxed{2\sqrt3\text{ is irrational}}
$$

---

## 5. Perfect-Square Factor Method

To simplify:

$$
\sqrt{72}
$$

Factor:

$$
72=36\times2
$$

Therefore:

$$
\sqrt{72}
=
\sqrt{36\times2}
$$

$$
=6\sqrt2
$$

Hence:

$$
\boxed{\sqrt{72}=6\sqrt2}
$$

> [!tip] Shortcut
> **Take the largest perfect-square factor outside the square root.**

---

# 6. Important Properties of Irrational Numbers

## 6.1 Irrational + Rational

If an irrational number is added to a rational number, the result is irrational.

$$
\boxed{\text{Irrational}+\text{Rational}=\text{Irrational}}
$$

Example:

$$
\sqrt2+3
$$

is irrational.

---

## 6.2 Irrational − Rational

$$
\boxed{\text{Irrational}-\text{Rational}=\text{Irrational}}
$$

Example:

$$
\sqrt5-2
$$

is irrational.

---

## 6.3 Non-Zero Rational × Irrational

If a non-zero rational number is multiplied by an irrational number, the result is irrational.

$$
\boxed{\text{Non-zero Rational}\times\text{Irrational}=\text{Irrational}}
$$

Example:

$$
3\sqrt2
$$

is irrational.

> [!warning] Important Exception
> The rational number must be **non-zero**.
>
> $$0\times\sqrt2=0$$
>
> and `0` is rational.

---

## 6.4 Irrational ÷ Non-Zero Rational

$$
\boxed{
\frac{\text{Irrational}}{\text{Non-zero Rational}}
=
\text{Irrational}
}
$$

Example:

$$
\frac{\sqrt3}{5}
$$

is irrational.

---

# 7. Irrational × Irrational

The result can be either rational or irrational.

### Example 1 — Rational Result

$$
\sqrt2\times\sqrt2
$$

$$
=2
$$

Therefore:

$$
\boxed{\text{Rational}}
$$

### Example 2 — Irrational Result

$$
\sqrt2\times\sqrt3
$$

$$
=\sqrt6
$$

Since `6` is not a perfect square:

$$
\boxed{\sqrt6\text{ is irrational}}
$$

> [!warning] Common Trap
> Do **not** assume:
>
> $$\text{Irrational}\times\text{Irrational}=\text{Irrational}$$
>
> This is not always true.

---

# 8. Irrational + Irrational

The result can also be either rational or irrational.

### Example 1 — Rational Result

$$
\sqrt2+(-\sqrt2)=0
$$

Therefore:

$$
\boxed{\text{Rational}}
$$

### Example 2 — Irrational Result

$$
\sqrt2+\sqrt3
$$

is irrational.

> [!warning] Important
> **Irrational + Irrational** can be rational or irrational.

---

# 9. Real Number Relationship

Every irrational number is a real number.

$$
\boxed{\text{Irrational}\subset\text{Real}}
$$

The real numbers consist of:

$$
\boxed{\text{Real Numbers}=\text{Rational Numbers}\cup\text{Irrational Numbers}}
$$

Therefore:

$$
\boxed{\mathbb R=\mathbb Q\cup\mathbb I}
$$

where:

- $\mathbb Q$ → Rational numbers
- $\mathbb I$ → Irrational numbers

Also:

$$
\boxed{\mathbb Q\cap\mathbb I=\varnothing}
$$

because a number cannot be both rational and irrational.

---

# 10. Important Number System Hierarchy

The complete hierarchy is:

$$
\boxed{
\mathbb N
\subset
\mathbb W
\subset
\mathbb Z
\subset
\mathbb Q
\subset
\mathbb R
}
$$

And:

$$
\boxed{\mathbb R=\mathbb Q\cup\mathbb I}
$$

Visual structure:

> [!summary] Number System

**Natural**

↓  

**Whole**

↓

**Integers**

↓

**Rational**

↙        ↘

**Rational** + **Irrational**

↓

**Real Numbers**

---

# 11. Important Aptitude Patterns

## Pattern 1 — Identify an Irrational Number

### Question

Which of the following is irrational?

$$
\frac{3}{4},\quad0.25,\quad\sqrt2,\quad5
$$

Check:

- $\frac34$ → Rational
- `0.25` → Rational
- $\sqrt2$ → Irrational
- `5` → Rational

Therefore:

$$
\boxed{\sqrt2}
$$

---

## Pattern 2 — Perfect Square Test

### Question

Determine whether:

$$
\sqrt{81}
$$

is rational or irrational.

Since:

$$
81=9^2
$$

Therefore:

$$
\sqrt{81}=9
$$

Hence:

$$
\boxed{\text{Rational}}
$$

---

## Pattern 3 — Non-Perfect Square Test

### Question

Determine whether:

$$
\sqrt{50}
$$

is rational or irrational.

Since `50` is not a perfect square:

$$
\boxed{\sqrt{50}\text{ is irrational}}
$$

Even after simplification:

$$
\sqrt{50}=5\sqrt2
$$

which is still irrational.

---

## Pattern 4 — Simplify a Surd

### Question

Simplify:

$$
\sqrt{180}
$$

Find the largest perfect-square factor:

$$
180=36\times5
$$

Therefore:

$$
\sqrt{180}
=
\sqrt{36\times5}
$$

$$
=6\sqrt5
$$

Answer:

$$
\boxed{6\sqrt5}
$$

---

## Pattern 5 — Rational + Irrational

### Question

Determine the type of:

$$
7+\sqrt3
$$

Since:

- `7` is rational
- $\sqrt3$ is irrational

Therefore:

$$
\boxed{7+\sqrt3\text{ is irrational}}
$$

---

## Pattern 6 — Irrational × Irrational

### Question

Determine the type of:

$$
\sqrt5\times\sqrt5
$$

$$
=5
$$

Therefore:

$$
\boxed{\text{Rational}}
$$

> [!tip] Pattern
> Two identical square roots may produce a perfect square:
>
> $$\sqrt a\times\sqrt a=a$$

---

## Pattern 7 — Find an Irrational Number Between Two Numbers

Between any two distinct real numbers, there are infinitely many irrational numbers.

Example:

Find an irrational number between:

$$
1\quad\text{and}\quad2
$$

One example is:

$$
\boxed{\sqrt2}
$$

because:

$$
1<\sqrt2<2
$$

---

# 12. Common Irrational Numbers

> [!important] Must Know

| Number | Type |
|---|---|
| $\sqrt2$ | Irrational |
| $\sqrt3$ | Irrational |
| $\sqrt5$ | Irrational |
| $\sqrt7$ | Irrational |
| $\sqrt{10}$ | Irrational |
| $\pi$ | Irrational |
| $e$ | Irrational |
| $\sqrt4=2$ | Rational |
| $\sqrt9=3$ | Rational |
| $\sqrt{16}=4$ | Rational |
| $\sqrt{25}=5$ | Rational |

---

# 13. Important Formula and Pattern Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Rational number | `p/q`, where `p,q ∈ Z` and `q ≠ 0` |
| Irrational number | Cannot be written as `p/q` |
| Perfect-square root | Rational |
| Non-perfect-square integer root | Irrational |
| Rational + Irrational | Irrational |
| Irrational − Rational | Irrational |
| Non-zero Rational × Irrational | Irrational |
| Irrational ÷ Non-zero Rational | Irrational |
| Irrational + Irrational | Could be Rational or Irrational |
| Irrational × Irrational | Could be Rational or Irrational |
| Real numbers | Rational + Irrational |

---

# 14. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Thinking every square root is irrational.
- ❌ Forgetting that $\sqrt4=2$ is rational.
- ❌ Assuming irrational + irrational is always irrational.
- ❌ Assuming irrational × irrational is always irrational.
- ❌ Forgetting the zero exception in `Rational × Irrational`.
- ❌ Confusing recurring decimals with irrational numbers.
- ❌ Thinking $\sqrt{12}$ is already in simplest surd form.
- ❌ Assuming $\pi$ is rational.
- ❌ Forgetting that every irrational number is real.

---

# 15. Exam Strategy

> [!tip] Fast Approach

When you see an irrational-number question:

1. Check whether the number is already a fraction of integers.
2. If there is a square root, check whether the number inside is a perfect square.
3. If necessary, factor the number and extract perfect-square factors.
4. For decimal questions:
   - Terminating → Rational
   - Recurring → Rational
   - Non-terminating and non-repeating → Irrational
5. For operations, remember that:
   - Rational + Irrational → Irrational
   - Rational × non-zero Irrational → Irrational
   - Irrational + Irrational → Cannot be determined without calculation
   - Irrational × Irrational → Cannot be determined without calculation

---

# 16. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Rational vs irrational identification
2. Perfect-square test
3. Square-root simplification
4. Surds
5. Decimal representation
6. Rational + irrational properties
7. Irrational × irrational exceptions
8. Real-number classification
9. Number-system hierarchy

---

# 17. Practice Checklist

- [ ] Understand the definition
- [ ] Differentiate rational and irrational numbers
- [ ] Memorize the decimal test
- [ ] Identify perfect squares
- [ ] Identify irrational square roots
- [ ] Simplify basic surds
- [ ] Practice rational + irrational problems
- [ ] Practice irrational × irrational problems
- [ ] Practice number classification
- [ ] Practice finding irrational numbers between two values
- [ ] Revise common traps

---

# 18. Related Topics

- [[01. Number System]]
- [[Rational Numbers]]
- [[Real Numbers]]
- [[Integers]]
- [[Whole Numbers]]
- [[Natural Numbers]]
- [[Surds]]
- [[Decimals]]
- [[Fractions]]
- [[Indices and Exponents]]

---

# 19. Quick Revision

> [!summary] One-Minute Revision

### Definition

$$
\boxed{\text{Irrational}=\text{Cannot be expressed as }\frac pq}
$$

where:

$$
p,q\in\mathbb Z,\qquad q\neq0
$$

### Decimal Pattern

$$
\boxed{\text{Terminating}\Rightarrow\text{Rational}}
$$

$$
\boxed{\text{Recurring}\Rightarrow\text{Rational}}
$$

$$
\boxed{\text{Non-terminating + Non-repeating}\Rightarrow\text{Irrational}}
$$

### Square Root Pattern

$$
\boxed{\sqrt{\text{Perfect Square}}=\text{Rational}}
$$

$$
\boxed{\sqrt{\text{Non-Perfect Square}}=\text{Irrational}}
$$

### Operations

$$
\boxed{\text{Rational}+\text{Irrational}=\text{Irrational}}
$$

$$
\boxed{\text{Non-zero Rational}\times\text{Irrational}=\text{Irrational}}
$$

### Important Exception

> **Irrational + Irrational** → could be rational or irrational.

> **Irrational × Irrational** → could be rational or irrational.

### Key Pattern

> **Before deciding whether `√n` is irrational, always check whether `n` is a perfect square.**