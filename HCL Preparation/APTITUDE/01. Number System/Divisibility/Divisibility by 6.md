---
type: concept
subject: aptitude
topic: "Divisibility by 6"
parent: "01. Number System/Divisibility"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - divisibility
  - divisibility-by-6
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 4]]"
  - "[[Divisibility by 5]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
---

# Divisibility by 6

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `6` if it is divisible by **both `2` and `3`**.

Since:

$$
6=2\times3
$$

the divisibility condition is:

$$
\boxed{\text{Divisible by 6}\iff\text{Divisible by 2 AND 3}}
$$

---

# 2. Divisibility Rule

To check whether a number is divisible by `6`, perform **two tests**.

### Test 1 — Divisibility by 2

The last digit must be:

$$
\boxed{0,2,4,6,8}
$$

### Test 2 — Divisibility by 3

The sum of the digits must be divisible by:

$$
\boxed{3}
$$

### Final Condition

Both must be true:

$$
\boxed{
\text{Last digit even}
\quad\text{AND}\quad
\text{Digit sum divisible by 3}
}
$$

---

# 3. Why This Rule Works

Since:

$$
6=2\times3
$$

and `2` and `3` are coprime, a number divisible by both is divisible by their product.

Therefore:

$$
\boxed{2\mid n\text{ and }3\mid n\Rightarrow6\mid n}
$$

---

# 4. Basic Examples

## Example 1

Check:

$$
234
$$

### Step 1 — Divisibility by 2

Last digit:

$$
4
$$

So it is divisible by `2`.

### Step 2 — Divisibility by 3

Digit sum:

$$
2+3+4=9
$$

`9` is divisible by `3`.

Therefore:

$$
\boxed{234\text{ is divisible by 6}}
$$

---

## Example 2

Check:

$$
245
$$

Last digit:

$$
5
$$

Since `5` is odd:

$$
245
$$

is not divisible by `2`.

Therefore:

$$
\boxed{245\text{ is not divisible by 6}}
$$

No need to perform the second test.

> [!tip] Fast Approach
> If the last digit is odd, immediately reject divisibility by `6`.

---

## Example 3

Check:

$$
312
$$

Last digit:

$$
2
$$

So it is divisible by `2`.

Digit sum:

$$
3+1+2=6
$$

`6` is divisible by `3`.

Therefore:

$$
\boxed{312\text{ is divisible by 6}}
$$

---

# 5. Important Shortcut

> [!important] Golden Rule
> **For divisibility by `6`:**
>
> 1. Check whether the last digit is even.
> 2. Check whether the digit sum is divisible by `3`.
> 3. Both conditions must be satisfied.

Think:

$$
\boxed{6=2\times3}
$$

---

# 6. Four Possible Cases

| Divisible by 2 | Divisible by 3 | Divisible by 6 |
|:---:|:---:|:---:|
| ✅ | ✅ | ✅ |
| ✅ | ❌ | ❌ |
| ❌ | ✅ | ❌ |
| ❌ | ❌ | ❌ |

> [!important] Key Idea
> **Both conditions are required.**

---

# 7. Example — Divisible by 2 but Not 6

Consider:

$$
124
$$

Last digit:

$$
4
$$

So:

$$
124\div2=62
$$

It is divisible by `2`.

But digit sum:

$$
1+2+4=7
$$

`7` is not divisible by `3`.

Therefore:

$$
\boxed{124\text{ is not divisible by 6}}
$$

---

# 8. Example — Divisible by 3 but Not 6

Consider:

$$
123
$$

Digit sum:

$$
1+2+3=6
$$

So it is divisible by `3`.

But last digit:

$$
3
$$

is odd.

Therefore it is not divisible by `2`.

Hence:

$$
\boxed{123\text{ is not divisible by 6}}
$$

---

# 9. Missing Digit Problems

This is one of the most important aptitude patterns.

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
45x
$$

is divisible by `6`.

### Condition 1 — Divisible by 2

`x` must be even:

$$
x\in\{0,2,4,6,8\}
$$

### Condition 2 — Divisible by 3

Digit sum:

$$
4+5+x=9+x
$$

For divisibility by `3`:

$$
9+x\equiv0\pmod3
$$

Therefore:

$$
x\in\{0,3,6,9\}
$$

### Take the intersection

$$
\{0,2,4,6,8\}
\cap
\{0,3,6,9\}
$$

Therefore:

$$
\boxed{x\in\{0,6\}}
$$

---

# 10. Pattern — Largest Missing Digit

Find the largest digit `x` such that:

$$
72x
$$

is divisible by `6`.

### Divisible by 2

$$
x\in\{0,2,4,6,8\}
$$

### Divisible by 3

$$
7+2+x=9+x
$$

Therefore:

$$
x\in\{0,3,6,9\}
$$

Intersection:

$$
\{0,6\}
$$

Largest:

$$
\boxed{x=6}
$$

---

# 11. Pattern — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
81x
$$

is divisible by `6`.

### Divisible by 2

$$
x\in\{0,2,4,6,8\}
$$

### Divisible by 3

$$
8+1+x=9+x
$$

Possible:

$$
x\in\{0,3,6,9\}
$$

Intersection:

$$
\{0,6\}
$$

Smallest:

$$
\boxed{x=0}
$$

---

# 12. Pattern — Multiple Missing Digits

Suppose:

$$
35xy
$$

must be divisible by `6`.

We need:

### Condition 1

`y` must be even:

$$
\boxed{y\in\{0,2,4,6,8\}}
$$

### Condition 2

Digit sum:

$$
3+5+x+y
$$

$$
=8+x+y
$$

must be divisible by `3`.

Therefore:

$$
\boxed{x+y\equiv1\pmod3}
$$

> [!tip] Pattern
> For multiple missing digits:
>
> **Use the last digit for divisibility by `2`.**
>
> **Use the total digit sum for divisibility by `3`.**

---

# 13. Remainder Pattern

A number divisible by `6` has:

$$
\boxed{N\bmod6=0}
$$

Possible remainders when dividing by `6` are:

$$
0,1,2,3,4,5
$$

Only remainder `0` means divisibility.

---

# 14. Count Multiples of 6

The number of positive multiples of `6` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N6\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `6`?

$$
\left\lfloor\frac{100}{6}\right\rfloor
$$

$$
=16
$$

Therefore:

$$
\boxed{16}
$$

---

# 15. Multiples in a Range

The number of integers divisible by `6` between `A` and `B`, inclusive:

$$
\boxed{
\left\lfloor\frac B6\right\rfloor
-
\left\lfloor\frac{A-1}{6}\right\rfloor
}
$$

### Example

How many numbers from `20` to `100` are divisible by `6`?

$$
\left\lfloor\frac{100}{6}\right\rfloor
-
\left\lfloor\frac{19}{6}\right\rfloor
$$

$$
=16-3
$$

$$
\boxed{13}
$$

---

# 16. Relationship With Even Multiples

Every multiple of `6` is even.

Why?

$$
6=2\times3
$$

Therefore:

$$
\boxed{6k=2(3k)}
$$

So every multiple of `6` is divisible by `2`.

---

# 17. Relationship With Multiples of 3

Every multiple of `6` is also a multiple of `3`.

Examples:

$$
6,12,18,24,30,\ldots
$$

All are divisible by `3`.

Therefore:

$$
\boxed{6\mid n\Rightarrow3\mid n}
$$

But:

$$
3\mid n\not\Rightarrow6\mid n
$$

Example:

$$
9
$$

is divisible by `3`, but not by `6`.

---

# 18. Relationship With Divisibility by 12

Since:

$$
12=2\times6
$$

a number divisible by `12` must also be divisible by `6`.

Therefore:

$$
\boxed{12\mid n\Rightarrow6\mid n}
$$

But the reverse is not always true.

Example:

$$
18
$$

is divisible by `6` but not by `12`.

---

# 19. Relationship With Divisibility by 18

Since:

$$
18=3\times6
$$

every number divisible by `18` is divisible by `6`.

Therefore:

$$
\boxed{18\mid n\Rightarrow6\mid n}
$$

---

# 20. Pattern — Divisibility by 30

Since:

$$
30=2\times3\times5
$$

a number is divisible by `30` if it is divisible by:

$$
2,\quad3,\quad5
$$

A simpler condition:

- Last digit must be `0`.
- Digit sum must be divisible by `3`.

### Example

Check:

$$
450
$$

Last digit:

$$
0
$$

So divisible by `2` and `5`.

Digit sum:

$$
4+5+0=9
$$

So divisible by `3`.

Therefore:

$$
\boxed{450\text{ is divisible by 30}}
$$

---

# 21. Pattern — Divisibility by 60

Since:

$$
60=2^2\times3\times5
$$

a number divisible by `60` must be divisible by:

$$
4,\quad3,\quad5
$$

### Example

Check:

$$
120
$$

Divisible by `4`:

$$
20\div4=5
$$

Divisible by `3`:

$$
1+2+0=3
$$

Divisible by `5`:

Last digit `0`.

Therefore:

$$
\boxed{120\text{ is divisible by 60}}
$$

---

# 22. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `6` | Divisible by `2` and `3` |
| Divisibility by `2` | Last digit even |
| Divisibility by `3` | Digit sum divisible by `3` |
| Remainder when divisible by `6` | `0` |
| Multiples from `1` to `N` | `⌊N/6⌋` |
| Multiples from `A` to `B` | `⌊B/6⌋ − ⌊(A−1)/6⌋` |
| Divisibility by `30` | Divisible by `2`, `3`, and `5` |
| Divisibility by `60` | Divisible by `4`, `3`, and `5` |

---

# 23. Important Patterns

> [!important] Remember These

### Pattern 1

$$
\boxed{6=2\times3}
$$

### Pattern 2

$$
\boxed{\text{Divisible by 6}\iff\text{Divisible by 2 AND 3}}
$$

### Pattern 3

$$
\boxed{\text{Last digit even}}
$$

AND

$$
\boxed{\text{Digit sum divisible by 3}}
$$

### Pattern 4

For missing-digit questions:

$$
\boxed{\text{Intersection of conditions}}
$$

Do not solve the two conditions separately and forget to combine them.

---

# 24. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking only whether the number is even.
- ❌ Checking only whether the digit sum is divisible by `3`.
- ❌ Assuming divisibility by `3` means divisibility by `6`.
- ❌ Forgetting that both conditions must hold.
- ❌ Using only the last digit for the `3` test.
- ❌ Forgetting to intersect possible missing-digit values.
- ❌ Performing complete division unnecessarily.
- ❌ Confusing divisibility by `6` with divisibility by `12`.

---

# 25. Exam Strategy

> [!tip] Fast 5-Second Method

When you see a divisibility-by-`6` question:

### Step 1

Look at the last digit.

If it is odd:

$$
\boxed{\text{STOP → Not divisible by 6}}
$$

### Step 2

If it is even, calculate the digit sum.

### Step 3

Check whether the digit sum is divisible by `3`.

### Step 4

If both pass:

$$
\boxed{\text{Divisible by 6}}
$$

---

# 26. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. `6 = 2 × 3`
2. Combined divisibility rule
3. Last-digit test
4. Digit-sum test
5. Missing-digit problems
6. Largest/smallest digit problems
7. Multiple missing digits
8. Counting multiples
9. Range-based questions
10. Connections with `12`, `18`, `30`, and `60`

---

# 27. Practice Checklist

- [ ] Memorize `6 = 2 × 3`
- [ ] Practice direct divisibility questions
- [ ] Practice last-digit filtering
- [ ] Practice digit-sum filtering
- [ ] Practice missing-digit questions
- [ ] Practice largest/smallest digit questions
- [ ] Practice multiple missing digits
- [ ] Practice remainder questions
- [ ] Practice counting multiples
- [ ] Practice range-based questions
- [ ] Practice composite divisibility patterns
- [ ] Revise common traps

---

# 28. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 4]]
- [[Divisibility by 5]]
- [[Factors]]
- [[Multiples]]
- [[HCF]]
- [[LCM]]
- [[Remainders]]
- [[Digit Problems]]

---

# 29. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 6}
\iff
N\text{ is divisible by 2 and 3}
}
$$

### Test 1

Last digit:

$$
\boxed{0,2,4,6,8}
$$

### Test 2

Digit sum:

$$
\boxed{\text{Must be divisible by 3}}
$$

### Example

$$
438
$$

Last digit:

$$
8
$$

→ divisible by `2`.

Digit sum:

$$
4+3+8=15
$$

→ divisible by `3`.

Therefore:

$$
\boxed{438\text{ is divisible by 6}}
$$

### Counting Multiples

$$
\boxed{\left\lfloor\frac N6\right\rfloor}
$$

### Key Pattern

> **Divisibility by `6` = EVEN + DIGIT SUM divisible by `3`.**