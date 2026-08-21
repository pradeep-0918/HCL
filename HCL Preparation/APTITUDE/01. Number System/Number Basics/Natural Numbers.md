---
type: concept
subject: aptitude
topic: "Natural Numbers"
parent: "01. Number System"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - natural-numbers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Whole Numbers]]"
  - "[[Integers]]"
---

# Natural Numbers

## 1. Overview

> [!summary] Core Idea
> Natural numbers are the numbers used for counting.
>
> **Natural Numbers = `{1, 2, 3, 4, 5, ...}`**

The set of natural numbers is usually denoted by:

$$
\mathbb{N} = \{1,2,3,4,\ldots\}
$$

> [!important] Important
> In standard aptitude mathematics, **0 is not considered a natural number**.
>
> However, some mathematical conventions include `0` in the natural numbers. Always follow the convention given by the question or source.

---

## 2. Important Properties

### 2.1 First Natural Number

The smallest natural number is:

$$
\boxed{1}
$$

### 2.2 There Is No Largest Natural Number

Natural numbers continue indefinitely:

$$
1,2,3,4,\ldots
$$

Therefore, there is **no largest natural number**.

### 2.3 Successor

The successor of a natural number `n` is:

$$
\boxed{n+1}
$$

Example:

$$
\text{Successor of } 25 = 26
$$

### 2.4 Predecessor

For a natural number greater than `1`, its predecessor is:

$$
\boxed{n-1}
$$

Example:

$$
\text{Predecessor of }25=24
$$

> [!warning] Trap
> `1` has no predecessor that is a natural number because `1 - 1 = 0`, and `0` is not included in the standard natural-number set.

---

## 3. Classification

Natural numbers can be divided into:

- Even natural numbers → `2, 4, 6, 8, ...`
- Odd natural numbers → `1, 3, 5, 7, ...`
- Prime natural numbers → `2, 3, 5, 7, ...`
- Composite natural numbers → `4, 6, 8, 9, ...`

> [!important] Special Case
> `1` is **neither prime nor composite**.

---

## 4. Important Formulas

### 4.1 Sum of First `n` Natural Numbers

$$
\boxed{S=\frac{n(n+1)}{2}}
$$

Example:

Sum of the first `10` natural numbers:

$$
S=\frac{10(11)}{2}=55
$$

---

### 4.2 Sum of First `n` Even Numbers

The first `n` even numbers are:

$$
2,4,6,\ldots,2n
$$

Therefore:

$$
\boxed{S=n(n+1)}
$$

Example:

First `10` even numbers:

$$
S=10(11)=110
$$

---

### 4.3 Sum of First `n` Odd Numbers

The first `n` odd numbers are:

$$
1,3,5,\ldots,(2n-1)
$$

Therefore:

$$
\boxed{S=n^2}
$$

Example:

Sum of first `10` odd numbers:

$$
S=10^2=100
$$

> [!tip] Shortcut
> **Sum of first `n` odd numbers = `n²`**

---

## 5. Sum of Consecutive Natural Numbers

For consecutive numbers from `a` to `b`:

### Number of Terms

$$
\boxed{n=b-a+1}
$$

### Sum

$$
\boxed{S=\frac{n(a+b)}{2}}
$$

or

$$
\boxed{S=\frac{(a+b)(b-a+1)}{2}}
$$

### Example

Find the sum:

$$
11+12+13+\cdots+20
$$

Number of terms:

$$
n=20-11+1=10
$$

Therefore:

$$
S=\frac{10(11+20)}{2}
$$

$$
S=155
$$

---

## 6. Average of Consecutive Natural Numbers

For consecutive numbers from `a` to `b`:

$$
\boxed{\text{Average}=\frac{a+b}{2}}
$$

Example:

Average of:

$$
21,22,23,\ldots,31
$$

$$
\text{Average}=\frac{21+31}{2}=26
$$

> [!tip] Shortcut
> For equally spaced consecutive numbers:
>
> **Average = Middle Number**

---

## 7. Important Aptitude Patterns

### Pattern 1 — Sum of First `n` Natural Numbers

**Question type:**

> Find the sum of the first `50` natural numbers.

**Identify:**

The sequence starts from `1` and ends at `n`.

**Formula:**

$$
S=\frac{n(n+1)}{2}
$$

---

### Pattern 2 — Find `n` From the Sum

**Question type:**

> The sum of the first `n` natural numbers is `465`. Find `n`.

**Identify:**

Use:

$$
\frac{n(n+1)}{2}=465
$$

Therefore:

$$
n(n+1)=930
$$

Since:

$$
30\times31=930
$$

Therefore:

$$
\boxed{n=30}
$$

> [!important] Pattern Recognition
> When you see **"sum of first n natural numbers"**, immediately think:
>
> $$\frac{n(n+1)}{2}$$

---

### Pattern 3 — Sum of a Range

**Question type:**

> Find the sum of all natural numbers from `25` to `75`.

**Identify:**

First number = `25`  
Last number = `75`

Number of terms:

$$
n=75-25+1=51
$$

Sum:

$$
S=\frac{51(25+75)}{2}
$$

$$
\boxed{S=2550}
$$

---

### Pattern 4 — Consecutive Numbers From Their Sum

If `n` consecutive natural numbers have a known sum:

$$
\boxed{\text{Average}=\frac{\text{Sum}}{n}}
$$

For consecutive numbers:

$$
\boxed{\text{Average}=\frac{\text{First}+\text{Last}}{2}}
$$

Therefore:

$$
\boxed{\text{First}+\text{Last}=2\times\text{Average}}
$$

This is extremely useful for finding the largest or smallest number.

---

### Pattern 5 — Largest Number in Consecutive Sequence

Suppose there are `n` consecutive numbers with sum `S`.

Average:

$$
A=\frac{S}{n}
$$

Largest number:

$$
\boxed{A+\frac{n-1}{2}}
$$

Smallest number:

$$
\boxed{A-\frac{n-1}{2}}
$$

> [!tip] Fast Pattern
> For `n` consecutive numbers:
>
> **Largest = Average + `(n−1)/2`**
>
> **Smallest = Average − `(n−1)/2`**

---

## 8. Even and Odd Patterns

### Even Numbers

General form:

$$
\boxed{2n}
$$

Examples:

`2, 4, 6, 8, ...`

### Odd Numbers

General form:

$$
\boxed{2n-1}
$$

Examples:

`1, 3, 5, 7, ...`

### Important Relationships

Even + Even:

$$
\boxed{\text{Even}}
$$

Odd + Odd:

$$
\boxed{\text{Even}}
$$

Even + Odd:

$$
\boxed{\text{Odd}}
$$

Even × Any Integer:

$$
\boxed{\text{Even}}
$$

Odd × Odd:

$$
\boxed{\text{Odd}}
$$

---

## 9. Quick Formula Sheet

> [!important] Must Remember

| Concept | Formula |
|---|---|
| First `n` natural numbers | `n(n+1)/2` |
| First `n` even numbers | `n(n+1)` |
| First `n` odd numbers | `n²` |
| Number of integers from `a` to `b` | `b-a+1` |
| Sum from `a` to `b` | `(a+b)(b-a+1)/2` |
| Average of consecutive numbers | `(First + Last)/2` |
| Successor of `n` | `n+1` |
| Predecessor of `n` | `n-1` |
| `n`th even number | `2n` |
| `n`th odd number | `2n-1` |

---

## 10. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Treating `0` as a natural number without checking the convention.
- ❌ Forgetting `+1` when counting numbers from `a` to `b`.
- ❌ Using `n²` for the sum of natural numbers.
- ❌ Confusing the `n`th odd number with the `n`th even number.
- ❌ Forgetting that `1` is neither prime nor composite.
- ❌ Assuming natural numbers have a largest value.

---

## 11. Exam Strategy

> [!tip] How to Solve Quickly

When you see a question involving natural numbers:

1. **Identify the sequence.**
2. Check whether it starts from `1`.
3. Determine the number of terms.
4. Look for a direct formula.
5. For consecutive numbers, use the **average method** whenever possible.
6. Check whether the question is actually testing an **even/odd**, **prime/composite**, **divisibility**, or **sum** pattern.

---

## 12. Priority for HCL Preparation

**Priority:** 🔥 Very High

Master these first:

1. Sum of first `n` natural numbers
2. Sum of consecutive numbers
3. Number of terms in a range
4. Average of consecutive numbers
5. Largest/smallest number from sum and number of terms
6. Even/odd properties
7. Basic number classification

---

## 13. Practice Checklist

- [ ] Understand natural numbers
- [ ] Know natural-number properties
- [ ] Memorize sum formulas
- [ ] Practice consecutive-number problems
- [ ] Practice average-based problems
- [ ] Practice even/odd patterns
- [ ] Practice finding `n` from a given sum
- [ ] Solve HCL-level questions
- [ ] Revise common traps

---

## 14. Related Topics

- [[01. Number System]]
- [[Whole Numbers]]
- [[Integers]]
- [[Even and Odd Numbers]]
- [[Prime and Composite Numbers]]
- [[Factors]]
- [[Multiples]]
- [[Divisibility Rules]]

---

## 15. Quick Revision

> [!summary] One-Minute Revision

**Natural Numbers:**

$$
1,2,3,4,\ldots
$$

**Sum of first `n`:**

$$
\boxed{\frac{n(n+1)}{2}}
$$

**Sum of first `n` even numbers:**

$$
\boxed{n(n+1)}
$$

**Sum of first `n` odd numbers:**

$$
\boxed{n^2}
$$

**Number of terms from `a` to `b`:**

$$
\boxed{b-a+1}
$$

**Average of consecutive numbers:**

$$
\boxed{\frac{\text{First}+\text{Last}}{2}}
$$

**Key pattern:**

> **Consecutive numbers → think Average + Number of Terms.**