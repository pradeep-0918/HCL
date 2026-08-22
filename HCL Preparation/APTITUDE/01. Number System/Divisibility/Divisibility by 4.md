---
type: concept
subject: aptitude
topic: "Divisibility by 4"
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
  - divisibility-by-4
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 8]]"
  - "[[Factors]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
---

# Divisibility by 4

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `4` if its remainder is `0` when divided by `4`.

Mathematically:

$$
\boxed{n\equiv0\pmod4}
$$

or:

$$
\boxed{n=4k}
$$

where `k` is an integer.

---

# 2. Divisibility Rule

A number is divisible by `4` if its **last two digits form a number divisible by `4`**.

$$
\boxed{\text{Check only the last 2 digits}}
$$

### Examples

For:

$$
2316
$$

last two digits:

$$
16
$$

Since:

$$
16\div4=4
$$

Therefore:

$$
\boxed{2316\text{ is divisible by 4}}
$$

---

# 3. Why Only the Last Two Digits Matter

Every decimal number can be written as:

$$
N=100k+r
$$

where `r` represents the last two digits.

Since:

$$
100=4\times25
$$

we have:

$$
100k
$$

always divisible by `4`.

Therefore:

$$
N\equiv r\pmod4
$$

Hence:

$$
\boxed{\text{Divisibility by 4 depends only on the last 2 digits}}
$$

> [!important] Golden Rule
> **For divisibility by `4`, ignore everything except the last two digits.**

---

# 4. Last Two Digits

The possible two-digit multiples of `4` are:

$$
04,08,12,16,20,24,28,\ldots
$$

up to:

$$
96
$$

Therefore, if the last two digits are one of these multiples, the entire number is divisible by `4`.

---

# 5. Basic Examples

## Example 1

Check:

$$
124
$$

Last two digits:

$$
24
$$

Since:

$$
24\div4=6
$$

Therefore:

$$
\boxed{124\text{ is divisible by 4}}
$$

---

## Example 2

Check:

$$
125
$$

Last two digits:

$$
25
$$

Since `25` is not divisible by `4`:

$$
\boxed{125\text{ is not divisible by 4}}
$$

---

## Example 3

Check:

$$
73816
$$

Last two digits:

$$
16
$$

Since:

$$
16\div4=4
$$

Therefore:

$$
\boxed{73816\text{ is divisible by 4}}
$$

---

## Example 4

Check:

$$
92347
$$

Last two digits:

$$
47
$$

Since `47` is not divisible by `4`:

$$
\boxed{92347\text{ is not divisible by 4}}
$$

---

# 6. Numbers Ending in 00

Any number ending in `00` is divisible by `4`.

Examples:

$$
100,\quad500,\quad1200,\quad7800
$$

because:

$$
00=0
$$

and `0` is divisible by `4`.

Therefore:

$$
\boxed{\text{Last two digits }00\Rightarrow\text{Divisible by 4}}
$$

---

# 7. Numbers With One Digit

For numbers smaller than `100`, simply check the number itself.

Examples:

$$
4,8,12,16,20,24
$$

are divisible by `4`.

Numbers such as:

$$
5,7,10,14,18
$$

are not divisible by `4`.

---

# 8. Connection With Divisibility by 2

Since:

$$
4=2\times2
$$

every number divisible by `4` must also be divisible by `2`.

Therefore:

$$
\boxed{\text{Divisible by 4}\Rightarrow\text{Divisible by 2}}
$$

But the reverse is not true.

### Example

`14` is divisible by `2`:

$$
14\div2=7
$$

but:

$$
14\div4=3.5
$$

Therefore:

$$
\boxed{14\text{ is not divisible by 4}}
$$

> [!warning] Important
> **Even does not always mean divisible by `4`.**

---

# 9. Connection With Divisibility by 8

The rules follow a pattern:

### Divisibility by 2

Check last:

$$
\boxed{1\text{ digit}}
$$

### Divisibility by 4

Check last:

$$
\boxed{2\text{ digits}}
$$

### Divisibility by 8

Check last:

$$
\boxed{3\text{ digits}}
$$

> [!tip] Pattern
> Powers of `2` progressively require more ending digits:
>
> $$2\rightarrow1\text{ digit}$$
>
> $$4\rightarrow2\text{ digits}$$
>
> $$8\rightarrow3\text{ digits}$$

---

# 10. Missing Digit Problems

This is a very common aptitude pattern.

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
53x
$$

is divisible by `4`.

Only the last two digits matter:

$$
3x
$$

Possible values:

$$
30,31,32,\ldots,39
$$

Among these:

$$
32
$$

and:

$$
36
$$

are divisible by `4`.

Therefore:

$$
\boxed{x\in\{2,6\}}
$$

---

# 11. Pattern — Largest Missing Digit

Find the largest digit `x` such that:

$$
72x
$$

is divisible by `4`.

Last two digits:

$$
2x
$$

Possible values:

$$
20,21,\ldots,29
$$

Multiples of `4`:

$$
20,24,28
$$

Therefore:

$$
x=0,4,8
$$

Largest:

$$
\boxed{x=8}
$$

---

# 12. Pattern — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
81x
$$

is divisible by `4`.

Last two digits:

$$
1x
$$

Possible multiples of `4`:

$$
12,16
$$

Therefore:

$$
x=2,6
$$

Smallest:

$$
\boxed{x=2}
$$

---

# 13. Pattern — Two Missing Digits

Suppose:

$$
52xy
$$

must be divisible by `4`.

Only the last two digits matter:

$$
xy
$$

Therefore, `xy` must be one of the two-digit multiples of `4`.

For example:

$$
00,04,08,12,16,\ldots,96
$$

Additional conditions in the question determine the final answer.

> [!important] Key Pattern
> **For a missing-digit question involving divisibility by `4`, work only with the final two positions.**

---

# 14. Pattern — Remainder

Find the remainder when:

$$
123456
$$

is divided by `4`.

Only the last two digits matter:

$$
56
$$

Since:

$$
56\div4=14
$$

remainder:

$$
\boxed{0}
$$

Therefore:

$$
\boxed{123456\text{ is divisible by 4}}
$$

---

# 15. Pattern — Remainder of a Large Number

Find:

$$
9876543219876\bmod4
$$

Ignore everything except the last two digits:

$$
76
$$

Since:

$$
76=4\times19
$$

the remainder is:

$$
\boxed{0}
$$

> [!tip] Exam Shortcut
> **Huge number + divisor `4` → inspect the last two digits.**

---

# 16. Pattern — Count Multiples of 4

The number of positive multiples of `4` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N4\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `4`?

$$
\left\lfloor\frac{100}{4}\right\rfloor
$$

$$
\boxed{25}
$$

---

# 17. Pattern — Multiples in a Range

The number of integers divisible by `4` between `A` and `B`, inclusive, is:

$$
\boxed{
\left\lfloor\frac B4\right\rfloor
-
\left\lfloor\frac{A-1}{4}\right\rfloor
}
$$

### Example

How many numbers from `20` to `80` are divisible by `4`?

$$
\left\lfloor\frac{80}{4}\right\rfloor
-
\left\lfloor\frac{19}{4}\right\rfloor
$$

$$
=20-4
$$

$$
\boxed{16}
$$

---

# 18. Pattern — Divisibility by 12

Since:

$$
12=3\times4
$$

a number is divisible by `12` if it is divisible by both `3` and `4`.

### Example

Check `312`.

For `3`:

$$
3+1+2=6
$$

So it is divisible by `3`.

For `4`:

Last two digits:

$$
12
$$

So it is divisible by `4`.

Therefore:

$$
\boxed{312\text{ is divisible by 12}}
$$

---

# 19. Pattern — Divisibility by 20

Since:

$$
20=4\times5
$$

a number divisible by `20` must satisfy both conditions:

- Divisible by `4`
- Divisible by `5`

A simpler rule is:

$$
\boxed{\text{Last two digits must be }00,20,40,60,80}
$$

Examples:

$$
120,\quad240,\quad560,\quad780
$$

are divisible by `20`.

---

# 20. Pattern — Divisibility by 100

Since:

$$
100=4\times25
$$

a number is divisible by `100` if its last two digits are:

$$
\boxed{00}
$$

Examples:

$$
500,\quad1200,\quad4500
$$

---

# 21. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `4` | Last 2 digits divisible by `4` |
| Remainder mod `4` | Depends only on last 2 digits |
| Divisibility by `2` | Last digit even |
| Divisibility by `8` | Last 3 digits divisible by `8` |
| Divisibility by `12` | Divisible by `3` and `4` |
| Divisibility by `20` | Last 2 digits `00,20,40,60,80` |
| Divisibility by `100` | Last 2 digits `00` |
| Multiples from `1` to `N` | `⌊N/4⌋` |
| Multiples from `A` to `B` | `⌊B/4⌋ − ⌊(A−1)/4⌋` |

---

# 22. Important Last-Two-Digit Multiples

> [!tip] Quick Reference

Multiples of `4` from `00` to `99`:

$$
00,04,08,12,16
$$

$$
20,24,28,32,36
$$

$$
40,44,48,52,56
$$

$$
60,64,68,72,76
$$

$$
80,84,88,92,96
$$

You don't necessarily need to memorize all of them. Checking the last two digits by simple division is usually enough.

---

# 23. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking only the last digit.
- ❌ Thinking every even number is divisible by `4`.
- ❌ Checking the last three digits instead of the last two.
- ❌ Performing complete division on a huge number.
- ❌ Forgetting that `00` is divisible by `4`.
- ❌ Confusing divisibility by `4` with divisibility by `8`.
- ❌ Forgetting that divisibility by `4` can be combined with divisibility by `3` to test `12`.

---

# 24. Exam Strategy

> [!tip] 3-Second Method

When you see:

> **"Is this number divisible by `4`?"**

Do this:

### Step 1

Ignore all digits except the last two.

### Step 2

Check whether those two digits form a multiple of `4`.

### Step 3

Answer.

### Example

$$
83749216
$$

Last two digits:

$$
16
$$

Since:

$$
16\div4=4
$$

Answer:

$$
\boxed{\text{Divisible by 4}}
$$

---

# 25. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Last-two-digit rule
2. Connection with even numbers
3. Missing-digit questions
4. Remainder questions
5. Counting multiples
6. Divisibility by `12`
7. Divisibility by `20`
8. Divisibility by `100`
9. Difference between `2`, `4`, and `8`

---

# 26. Practice Checklist

- [ ] Memorize the last-two-digit rule
- [ ] Practice direct divisibility questions
- [ ] Practice large-number questions
- [ ] Practice missing-digit questions
- [ ] Practice largest/smallest digit questions
- [ ] Practice remainder questions
- [ ] Practice counting multiples
- [ ] Practice range-based questions
- [ ] Practice divisibility by `12`
- [ ] Practice divisibility by `20`
- [ ] Revise common traps

---

# 27. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 5]]
- [[Divisibility by 6]]
- [[Divisibility by 8]]
- [[Divisibility by 12]]
- [[Factors]]
- [[Multiples]]
- [[Remainders]]
- [[Digit Problems]]

---

# 28. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 4}
\iff
\text{Last 2 digits are divisible by 4}
}
$$

### Examples

$$
16,\ 24,\ 32,\ 48,\ 64,\ 72,\ 88
$$

are divisible by `4`.

### Large Number

$$
9876543216
$$

Check:

$$
16
$$

Therefore:

$$
\boxed{\text{Divisible by 4}}
$$

### Counting Multiples

From `1` to `N`:

$$
\boxed{\left\lfloor\frac N4\right\rfloor}
$$

From `A` to `B`:

$$
\boxed{
\left\lfloor\frac B4\right\rfloor
-
\left\lfloor\frac{A-1}{4}\right\rfloor
}
$$

### Key Pattern

> **Divisibility by `4` → Ignore everything except the last TWO digits.**