---
type: concept
subject: aptitude
topic: "Divisibility by 8"
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
  - divisibility-by-8
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 4]]"
  - "[[Divisibility by 16]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
---

# Divisibility by 8

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `8` if division by `8` leaves remainder `0`.

Mathematically:

$$
\boxed{n\equiv0\pmod8}
$$

or:

$$
\boxed{n=8k}
$$

where `k` is an integer.

---

# 2. Divisibility Rule

A number is divisible by `8` if its **last three digits form a number divisible by `8`**.

$$
\boxed{\text{Check only the last 3 digits}}
$$

### Example

Check:

$$
5128
$$

Last three digits:

$$
128
$$

Since:

$$
128\div8=16
$$

therefore:

$$
\boxed{5128\text{ is divisible by 8}}
$$

---

# 3. Why Only the Last Three Digits Matter

Every decimal number can be written as:

$$
N=1000k+r
$$

where `r` represents the last three digits.

Since:

$$
1000=8\times125
$$

we know:

$$
1000k
$$

is always divisible by `8`.

Therefore:

$$
N\equiv r\pmod8
$$

Hence:

$$
\boxed{\text{Divisibility by 8 depends only on the last 3 digits}}
$$

> [!important] Golden Rule
> **For divisibility by `8`, ignore everything except the last three digits.**

---

# 4. Basic Examples

## Example 1

Check:

$$
1232
$$

Last three digits:

$$
232
$$

Since:

$$
232\div8=29
$$

therefore:

$$
\boxed{1232\text{ is divisible by 8}}
$$

---

## Example 2

Check:

$$
4314
$$

Last three digits:

$$
314
$$

Since:

$$
314\div8
$$

is not an integer:

$$
\boxed{4314\text{ is not divisible by 8}}
$$

---

## Example 3

Check:

$$
987654312
$$

Last three digits:

$$
312
$$

Since:

$$
312\div8=39
$$

therefore:

$$
\boxed{987654312\text{ is divisible by 8}}
$$

---

# 5. The 2 → 4 → 8 Pattern

This is one of the most important patterns in aptitude.

### Divisibility by 2

Check:

$$
\boxed{\text{Last 1 digit}}
$$

### Divisibility by 4

Check:

$$
\boxed{\text{Last 2 digits}}
$$

### Divisibility by 8

Check:

$$
\boxed{\text{Last 3 digits}}
$$

Therefore:

$$
\boxed{2\rightarrow4\rightarrow8}
$$

corresponds to:

$$
\boxed{1\text{ digit}\rightarrow2\text{ digits}\rightarrow3\text{ digits}}
$$

> [!tip] Memory Trick
> **2 = 1 digit**
>
> **4 = 2 digits**
>
> **8 = 3 digits**

---

# 6. Connection With Divisibility by 4

Since:

$$
8=2\times4
$$

every number divisible by `8` must also be divisible by `4`.

Therefore:

$$
\boxed{\text{Divisible by 8}\Rightarrow\text{Divisible by 4}}
$$

But the reverse is not always true.

### Example

`12` is divisible by `4`:

$$
12\div4=3
$$

but:

$$
12\div8=1.5
$$

Therefore:

$$
\boxed{12\text{ is not divisible by 8}}
$$

---

# 7. Connection With Divisibility by 2

Since:

$$
8=2^3
$$

every number divisible by `8` is also divisible by `2`.

Therefore:

$$
\boxed{\text{Divisible by 8}\Rightarrow\text{Even}}
$$

But:

$$
\boxed{\text{Even}\not\Rightarrow\text{Divisible by 8}}
$$

Example:

$$
14
$$

is even but not divisible by `8`.

---

# 8. Multiples of 8

Useful multiples:

$$
8,16,24,32,40,48,56,64
$$

$$
72,80,88,96,104,112,120,128
$$

$$
136,144,152,160,168,176,184,192
$$

Knowing common multiples helps with fast recognition.

---

# 9. Missing Digit Problems

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
52x
$$

is divisible by `8`.

Since the number has only three digits, check the whole number:

$$
520+x
$$

Possible values:

$$
520,521,\ldots,529
$$

Multiples of `8`:

$$
520,528
$$

Therefore:

$$
\boxed{x\in\{0,8\}}
$$

---

# 10. Pattern — Largest Missing Digit

Find the largest digit `x` such that:

$$
37x
$$

is divisible by `8`.

Possible numbers:

$$
370,371,\ldots,379
$$

Multiples of `8` in this range:

$$
376
$$

Therefore:

$$
\boxed{x=6}
$$

---

# 11. Pattern — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
61x
$$

is divisible by `8`.

Possible numbers:

$$
610,611,\ldots,619
$$

The multiple of `8` is:

$$
616
$$

Therefore:

$$
\boxed{x=6}
$$

---

# 12. Pattern — Missing Last Two Digits

Suppose:

$$
45xy
$$

must be divisible by `8`.

Only the last three digits matter:

$$
5xy
$$

Therefore:

$$
\boxed{5xy\text{ must be divisible by 8}}
$$

The problem can then be solved by listing multiples of `8` between:

$$
500\text{ and }599
$$

or by modular arithmetic.

> [!important] Key Pattern
> **For divisibility by `8`, the final three positions determine everything.**

---

# 13. Pattern — Remainder of a Large Number

Find:

$$
9876543219876\bmod8
$$

Only the last three digits matter:

$$
876
$$

Now:

$$
876=8\times109+4
$$

Therefore:

$$
\boxed{9876543219876\bmod8=4}
$$

---

# 14. Pattern — Divisibility of a Large Number

Check:

$$
123456789123456
$$

for divisibility by `8`.

Last three digits:

$$
456
$$

Since:

$$
456\div8=57
$$

therefore:

$$
\boxed{\text{The number is divisible by 8}}
$$

No other digits matter.

---

# 15. Pattern — Count Multiples of 8

The number of positive multiples of `8` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N8\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `8`?

$$
\left\lfloor\frac{100}{8}\right\rfloor
$$

$$
=12
$$

Therefore:

$$
\boxed{12}
$$

---

# 16. Pattern — Multiples in a Range

The number of integers divisible by `8` from `A` to `B`, inclusive:

$$
\boxed{
\left\lfloor\frac B8\right\rfloor
-
\left\lfloor\frac{A-1}{8}\right\rfloor
}
$$

### Example

How many numbers from `20` to `100` are divisible by `8`?

$$
\left\lfloor\frac{100}{8}\right\rfloor
-
\left\lfloor\frac{19}{8}\right\rfloor
$$

$$
=12-2
$$

$$
\boxed{10}
$$

---

# 17. Divisibility by 16

The same pattern continues.

Since:

$$
16=2^4
$$

for divisibility by `16`, check the **last four digits**.

### Example

Check:

$$
123456
$$

Last four digits:

$$
3456
$$

Since:

$$
3456\div16=216
$$

therefore:

$$
\boxed{123456\text{ is divisible by 16}}
$$

> [!tip] Pattern
>
> $$2\rightarrow4\rightarrow8\rightarrow16$$
>
> $$1\rightarrow2\rightarrow3\rightarrow4\text{ ending digits}$$

For most aptitude questions, `2`, `4`, and `8` are the essential rules.

---

# 18. Divisibility by 24

Since:

$$
24=3\times8
$$

a number is divisible by `24` if it is divisible by both:

$$
3
$$

and:

$$
8
$$

### Example

Check:

$$
312
$$

For `3`:

$$
3+1+2=6
$$

So divisible by `3`.

For `8`:

$$
312\div8=39
$$

So divisible by `8`.

Therefore:

$$
\boxed{312\text{ is divisible by 24}}
$$

---

# 19. Divisibility by 40

Since:

$$
40=5\times8
$$

a number is divisible by `40` if it is divisible by both `5` and `8`.

A useful direct pattern is:

$$
\boxed{\text{Last two digits are }00,40,80}
$$

Examples:

$$
120,\quad240,\quad360,\quad480
$$

are divisible by `40`.

---

# 20. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `8` | Last 3 digits divisible by `8` |
| Remainder mod `8` | Depends only on last 3 digits |
| Divisibility by `2` | Last 1 digit even |
| Divisibility by `4` | Last 2 digits divisible by `4` |
| Divisibility by `16` | Last 4 digits divisible by `16` |
| Divisibility by `24` | Divisible by `3` and `8` |
| Divisibility by `40` | Divisible by `5` and `8` |
| Multiples from `1` to `N` | `⌊N/8⌋` |
| Multiples from `A` to `B` | `⌊B/8⌋ − ⌊(A−1)/8⌋` |

---

# 21. Important Patterns

> [!important] Must Master

### Pattern 1 — Ending Digits

$$
\boxed{2\rightarrow1\text{ digit}}
$$

$$
\boxed{4\rightarrow2\text{ digits}}
$$

$$
\boxed{8\rightarrow3\text{ digits}}
$$

### Pattern 2

$$
\boxed{\text{Last 3 digits}\div8\text{ with remainder }0}
$$

### Pattern 3

For a huge number:

$$
\boxed{\text{Ignore everything except the last 3 digits}}
$$

### Pattern 4

For missing digits:

$$
\boxed{\text{Work only with the final 3 positions}}
$$

---

# 22. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking only the last digit.
- ❌ Using the last two digits instead of the last three.
- ❌ Assuming every number divisible by `4` is divisible by `8`.
- ❌ Performing complete division on a huge number.
- ❌ Forgetting leading zeros in the final three digits.

### Example

For:

$$
1208
$$

last three digits:

$$
208
$$

For:

$$
120
$$

the last three digits can be viewed as:

$$
120
$$

For a smaller number like `24`, conceptually use:

$$
024
$$

and check:

$$
24\div8=3
$$

Therefore `24` is divisible by `8`.

---

# 23. Exam Strategy

> [!tip] 3-Second Method

When you see:

> **"Is this number divisible by `8`?"**

### Step 1

Take only the last three digits.

### Step 2

Check whether those three digits form a multiple of `8`.

### Step 3

Answer.

### Example

$$
73849216
$$

Last three digits:

$$
216
$$

Since:

$$
216\div8=27
$$

answer:

$$
\boxed{\text{Divisible by 8}}
$$

---

# 24. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Last-three-digit rule
2. `2 → 4 → 8` pattern
3. Large-number divisibility
4. Missing-digit problems
5. Remainder problems
6. Counting multiples
7. Divisibility by `16`
8. Divisibility by `24`
9. Divisibility by `40`
10. Number-formation problems

---

# 25. Practice Checklist

- [ ] Memorize the last-three-digit rule
- [ ] Practice direct divisibility questions
- [ ] Practice huge numbers
- [ ] Practice missing-digit questions
- [ ] Practice largest/smallest digit questions
- [ ] Practice remainder questions
- [ ] Practice counting multiples
- [ ] Practice divisibility by `16`
- [ ] Practice divisibility by `24`
- [ ] Practice divisibility by `40`
- [ ] Revise the `2 → 4 → 8` pattern
- [ ] Revise common traps

---

# 26. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 4]]
- [[Divisibility by 5]]
- [[Divisibility by 6]]
- [[Divisibility by 7]]
- [[Factors]]
- [[Multiples]]
- [[Remainders]]
- [[Digit Problems]]

---

# 27. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 8}
\iff
\text{Last 3 digits are divisible by 8}
}
$$

### The Golden Pattern

$$
\boxed{
2\rightarrow1\text{ digit}
}
$$

$$
\boxed{
4\rightarrow2\text{ digits}
}
$$

$$
\boxed{
8\rightarrow3\text{ digits}
}
$$

### Example

$$
987654312
$$

Last three digits:

$$
312
$$

$$
312\div8=39
$$

Therefore:

$$
\boxed{\text{Divisible by 8}}
$$

### Counting Multiples

$$
\boxed{\left\lfloor\frac N8\right\rfloor}
$$

### Key Pattern

> **Divisibility by `8` → Check only the last THREE digits.**