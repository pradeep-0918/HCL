---
type: concept
subject: aptitude
topic: "General Divisibility Problems"
parent: "01. Number System/Divisibility"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - divisibility
  - divisibility-problems
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 4]]"
  - "[[Divisibility by 5]]"
  - "[[Divisibility by 6]]"
  - "[[Divisibility by 7]]"
  - "[[Divisibility by 8]]"
  - "[[Divisibility by 9]]"
  - "[[Divisibility by 11]]"
  - "[[Remainders]]"
  - "[[Factors]]"
  - "[[LCM]]"
  - "[[HCF]]"
---

# General Divisibility Problems

## 1. Core Concept

> [!summary] What Are General Divisibility Problems?
> These problems combine different divisibility rules to solve questions involving:
>
> - Missing digits
> - Number formation
> - Counting multiples
> - Divisibility by multiple numbers
> - Remainders
> - Smallest/largest numbers
> - Consecutive numbers
> - Common multiples
> - HCF and LCM
> - Digit conditions

The main skill is:

$$
\boxed{\text{Recognize the divisor} \rightarrow \text{Apply the correct rule}}
$$

---

# 2. Divisibility Rules — Master Table

> [!important] Must Memorize

| Divisor | Main Rule |
|---:|---|
| `2` | Last digit is `0, 2, 4, 6, 8` |
| `3` | Digit sum divisible by `3` |
| `4` | Last 2 digits divisible by `4` |
| `5` | Last digit is `0` or `5` |
| `6` | Divisible by `2` and `3` |
| `7` | Double last digit and subtract |
| `8` | Last 3 digits divisible by `8` |
| `9` | Digit sum divisible by `9` |
| `10` | Last digit is `0` |
| `11` | Difference of alternate digit sums is divisible by `11` |

---

# 3. Pattern Recognition

Before solving a divisibility question, identify what type of problem it is.

### Pattern A

> Is this number divisible by `d`?

Use the divisibility rule.

### Pattern B

> Find `x` so that the number is divisible by `d`.

Use the divisibility rule to create a condition on `x`.

### Pattern C

> How many numbers are divisible by `d`?

Use:

$$
\boxed{\left\lfloor\frac Nd\right\rfloor}
$$

or the range formula.

### Pattern D

> Divisible by both `a` and `b`.

Usually think about:

$$
\boxed{\operatorname{LCM}(a,b)}
$$

### Pattern E

> Divisible by `a` but not `b`.

Count multiples of `a` and remove those also divisible by `b`.

---

# 4. Missing Digit — Basic Pattern

Suppose:

$$
52x
$$

must be divisible by `3`.

Digit sum:

$$
5+2+x=7+x
$$

Need:

$$
7+x\equiv0\pmod3
$$

Therefore:

$$
\boxed{x\in\{2,5,8\}}
$$

---

# 5. Missing Digit — Divisibility by 4

Suppose:

$$
73x
$$

must be divisible by `4`.

Only the last two digits matter:

$$
3x
$$

Possible values:

$$
30,31,\ldots,39
$$

Multiples of `4`:

$$
32,36
$$

Therefore:

$$
\boxed{x\in\{2,6\}}
$$

---

# 6. Missing Digit — Divisibility by 5

Suppose:

$$
84x
$$

must be divisible by `5`.

Last digit must be:

$$
0\text{ or }5
$$

Therefore:

$$
\boxed{x\in\{0,5\}}
$$

---

# 7. Missing Digit — Divisibility by 6

Suppose:

$$
45x
$$

must be divisible by `6`.

### Divisibility by 2

$$
x\in\{0,2,4,6,8\}
$$

### Divisibility by 3

$$
4+5+x=9+x
$$

Therefore:

$$
x\in\{0,3,6,9\}
$$

Intersection:

$$
\boxed{x\in\{0,6\}}
$$

> [!important] Pattern
> For composite divisors, solve each condition and take the **intersection**.

---

# 8. Missing Digit — Divisibility by 9

Suppose:

$$
73x
$$

must be divisible by `9`.

Digit sum:

$$
7+3+x=10+x
$$

Need a multiple of `9`.

Therefore:

$$
10+x=18
$$

So:

$$
\boxed{x=8}
$$

---

# 9. Missing Digit — Divisibility by 11

Suppose:

$$
4x35
$$

must be divisible by `11`.

Alternate sums:

$$
4+3=7
$$

and:

$$
x+5
$$

Therefore:

$$
7-(x+5)
$$

must be a multiple of `11`.

$$
2-x=0
$$

Hence:

$$
\boxed{x=2}
$$

---

# 10. Divisibility by Multiple Numbers

Suppose a number must be divisible by:

$$
2,\ 3,\ 5
$$

Since:

$$
2\times3\times5=30
$$

and these are pairwise coprime:

$$
\boxed{\text{Divisible by 2, 3 and 5}\iff\text{Divisible by 30}}
$$

### Example

Is `450` divisible by `30`?

Last digit:

$$
0
$$

So divisible by `2` and `5`.

Digit sum:

$$
4+5=9
$$

So divisible by `3`.

Therefore:

$$
\boxed{450\text{ is divisible by 30}}
$$

---

# 11. LCM Pattern

If a number must be divisible by two or more numbers, think:

$$
\boxed{\operatorname{LCM}}
$$

### Example

Find the smallest number divisible by:

$$
4,\ 6,\ 8
$$

Prime factorizations:

$$
4=2^2
$$

$$
6=2\times3
$$

$$
8=2^3
$$

Therefore:

$$
\operatorname{LCM}(4,6,8)=2^3\times3
$$

$$
=24
$$

Therefore:

$$
\boxed{24}
$$

---

# 12. Counting Multiples

The number of multiples of `d` from `1` to `N` is:

$$
\boxed{
\left\lfloor\frac Nd\right\rfloor
}
$$

### Example

How many numbers from `1` to `100` are divisible by `7`?

$$
\left\lfloor\frac{100}{7}\right\rfloor
=
14
$$

Therefore:

$$
\boxed{14}
$$

---

# 13. Counting Multiples in a Range

For integers from `A` to `B`, inclusive:

$$
\boxed{
\left\lfloor\frac Bd\right\rfloor
-
\left\lfloor\frac{A-1}{d}\right\rfloor
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

# 14. Count Numbers Divisible by Both

Suppose we need numbers divisible by both `4` and `6`.

Use:

$$
\operatorname{LCM}(4,6)
$$

$$
=12
$$

Therefore:

$$
\boxed{\text{Divisible by both 4 and 6}\iff\text{Divisible by 12}}
$$

### Example

How many numbers from `1` to `100` are divisible by both `4` and `6`?

$$
\left\lfloor\frac{100}{12}\right\rfloor
$$

$$
\boxed{8}
$$

---

# 15. Count Numbers Divisible by Either

For two divisors `a` and `b`:

$$
\boxed{
\text{Count}(a\text{ or }b)
=
\text{Count}(a)
+
\text{Count}(b)
-
\text{Count}(\operatorname{LCM}(a,b))
}
$$

This is the **inclusion-exclusion principle**.

### Example

How many numbers from `1` to `100` are divisible by `3` or `5`?

Multiples of `3`:

$$
\left\lfloor\frac{100}{3}\right\rfloor=33
$$

Multiples of `5`:

$$
\left\lfloor\frac{100}{5}\right\rfloor=20
$$

Multiples of both:

$$
\operatorname{LCM}(3,5)=15
$$

$$
\left\lfloor\frac{100}{15}\right\rfloor=6
$$

Therefore:

$$
33+20-6
$$

$$
\boxed{47}
$$

> [!important] Why subtract?
> Multiples of `15` were counted twice, so subtract them once.

---

# 16. Count Numbers Divisible by A but Not B

Suppose we need numbers divisible by `3` but not by `6`.

### Step 1

Count multiples of `3`.

### Step 2

Remove multiples of `6`.

From `1` to `100`:

$$
\left\lfloor\frac{100}{3}\right\rfloor=33
$$

$$
\left\lfloor\frac{100}{6}\right\rfloor=16
$$

Therefore:

$$
33-16
$$

$$
\boxed{17}
$$

---

# 17. Number Formation Pattern

Suppose you need to form a number divisible by `5`.

The units digit has:

$$
\boxed{2\text{ choices}}
$$

namely:

$$
0,5
$$

For divisibility by `2`:

$$
\boxed{5\text{ choices}}
$$

namely:

$$
0,2,4,6,8
$$

For divisibility by `10`:

$$
\boxed{1\text{ choice}}
$$

namely:

$$
0
$$

---

# 18. Number Formation — Divisible by 6

To make a number divisible by `6`, both conditions must be satisfied:

$$
\boxed{\text{Even last digit}}
$$

and:

$$
\boxed{\text{Digit sum divisible by 3}}
$$

This is a common counting-problem pattern.

> [!tip] Strategy
> First restrict the units digit using divisibility by `2`, then use the digit-sum condition for `3`.

---

# 19. Smallest Number Divisible by Several Numbers

### Question

Find the smallest number divisible by:

$$
6,\ 8,\ 12
$$

Find the LCM.

Prime factors:

$$
6=2\times3
$$

$$
8=2^3
$$

$$
12=2^2\times3
$$

Therefore:

$$
\operatorname{LCM}=2^3\times3
$$

$$
\boxed{24}
$$

---

# 20. Largest Number Divisible by a Given Number

### Question

Find the largest multiple of `7` below `100`.

Calculate:

$$
\left\lfloor\frac{99}{7}\right\rfloor
$$

$$
=14
$$

Therefore:

$$
14\times7=98
$$

Answer:

$$
\boxed{98}
$$

> [!tip] Pattern
> **Largest multiple below `N`:**
>
> $$\boxed{\left\lfloor\frac{N-1}{d}\right\rfloor\times d}$$

---

# 21. Smallest Multiple Greater Than a Number

Find the smallest multiple of `8` greater than `50`.

$$
\left\lfloor\frac{50}{8}\right\rfloor=6
$$

Next multiple:

$$
(6+1)\times8
$$

$$
\boxed{56}
$$

---

# 22. Consecutive Numbers

Among every `d` consecutive integers, exactly one is divisible by `d`.

### Example

Among:

$$
21,22,23,24,25,26,27
$$

there is exactly one multiple of `7`:

$$
21
$$

The next one is:

$$
28
$$

Therefore:

$$
\boxed{\text{Every 7 consecutive integers contain exactly one multiple of 7}}
$$

---

# 23. Divisibility and Remainders

If:

$$
N
$$

is divided by `d`:

$$
N=dq+r
$$

where:

$$
\boxed{0\le r<d}
$$

If `r = 0`:

$$
\boxed{d\mid N}
$$

If `r \ne 0`:

$$
\boxed{d\nmid N}
$$

---

# 24. Divisibility of an Expression

Suppose:

$$
N=6k
$$

Then automatically:

$$
2\mid N
$$

and:

$$
3\mid N
$$

because:

$$
6k=2(3k)
$$

and:

$$
6k=3(2k)
$$

> [!important] Pattern
> Expressing a number as:
>
> $$N=dk$$
>
> immediately proves divisibility by `d`.

---

# 25. Algebraic Divisibility Pattern

If:

$$
a\mid b
$$

then:

$$
\boxed{a\mid kb}
$$

for every integer `k`.

### Example

Since:

$$
5\mid20
$$

then:

$$
5\mid100
$$

because:

$$
100=5\times20
$$

---

# 26. Sum and Difference Pattern

If:

$$
d\mid a
$$

and:

$$
d\mid b
$$

then:

$$
\boxed{d\mid(a+b)}
$$

and:

$$
\boxed{d\mid(a-b)}
$$

### Example

Since `3` divides both:

$$
12
$$

and:

$$
21
$$

then `3` divides:

$$
12+21=33
$$

and:

$$
21-12=9
$$

---

# 27. Important Composite Divisibility Pattern

If:

$$
\gcd(a,b)=1
$$

then:

$$
\boxed{
ab\mid n
\iff
a\mid n\text{ and }b\mid n
}
$$

Example:

$$
2\text{ and }3
$$

are coprime.

Therefore:

$$
\boxed{
6\mid n
\iff
2\mid n\text{ and }3\mid n
}
$$

This is why the divisibility rule for `6` works.

---

# 28. Common Divisibility Combinations

> [!important] High-Yield Table

| Divisor | Conditions |
|---:|---|
| `6` | `2` and `3` |
| `10` | `2` and `5` |
| `12` | `3` and `4` |
| `14` | `2` and `7` |
| `15` | `3` and `5` |
| `18` | `2` and `9` |
| `20` | `4` and `5` |
| `21` | `3` and `7` |
| `22` | `2` and `11` |
| `24` | `3` and `8` |
| `30` | `2`, `3`, and `5` |
| `33` | `3` and `11` |
| `35` | `5` and `7` |
| `40` | `5` and `8` |
| `45` | `5` and `9` |
| `55` | `5` and `11` |
| `60` | `3`, `4`, and `5` |

---

# 29. General Formula Sheet

> [!important] Must Remember

### Multiples from `1` to `N`

$$
\boxed{
\left\lfloor\frac Nd\right\rfloor
}
$$

### Multiples from `A` to `B`

$$
\boxed{
\left\lfloor\frac Bd\right\rfloor
-
\left\lfloor\frac{A-1}{d}\right\rfloor
}
$$

### Divisible by Both

$$
\boxed{
\operatorname{LCM}(a,b)
}
$$

### Count Divisible by `a` or `b`

$$
\boxed{
\left\lfloor\frac Na\right\rfloor
+
\left\lfloor\frac Nb\right\rfloor
-
\left\lfloor\frac N{\operatorname{LCM}(a,b)}\right\rfloor
}
$$

### Division Algorithm

$$
\boxed{
N=dq+r
}
$$

where:

$$
\boxed{0\le r<d}
$$

### Divisibility

$$
\boxed{d\mid N\iff N\bmod d=0}
$$

---

# 30. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Adding counts without removing overlap.
- ❌ Using product instead of LCM for common divisibility.
- ❌ Forgetting that a missing digit must be between `0` and `9`.
- ❌ Checking only one condition for a composite divisor.
- ❌ Confusing "divisible by" with "remainder".
- ❌ Forgetting whether the range is inclusive.
- ❌ Allowing `0` as the first digit of a number.
- ❌ Using the divisibility-by-`3` rule for `9` without checking the actual multiple.
- ❌ Using the divisibility-by-`4` rule for `8`.
- ❌ Forgetting to check all conditions in number-formation questions.

---

# 31. Exam Decision Tree

> [!tip] Fast Recognition

When you see a divisibility question:

### Step 1 — Identify the divisor

Ask:

> Which rule applies?

### Step 2 — If divisor is simple

Use the direct rule:

$$
2,\ 3,\ 4,\ 5,\ 7,\ 8,\ 9,\ 11
$$

### Step 3 — If divisor is composite

Break it into prime factors or useful components.

Example:

$$
12=3\times4
$$

So check:

$$
3\text{ and }4
$$

### Step 4 — If counting is involved

Use:

$$
\boxed{\left\lfloor N/d\right\rfloor}
$$

### Step 5 — If "both" appears

Think:

$$
\boxed{\operatorname{LCM}}
$$

### Step 6 — If "either" appears

Think:

$$
\boxed{\text{Inclusion-Exclusion}}
$$

### Step 7 — If "not" appears

Subtract the unwanted multiples.

---

# 32. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

General divisibility problems combine almost everything learned in this section.

### Master These Patterns

1. Direct divisibility
2. Missing digit
3. Multiple missing digits
4. Composite divisibility
5. Counting multiples
6. Range counting
7. LCM-based divisibility
8. Inclusion-exclusion
9. Number formation
10. Largest/smallest multiple
11. Remainder connection
12. Consecutive-number patterns

---

# 33. Practice Checklist

- [ ] Revise all divisibility rules
- [ ] Practice missing-digit problems
- [ ] Practice composite divisibility
- [ ] Practice LCM problems
- [ ] Practice counting multiples
- [ ] Practice range problems
- [ ] Practice inclusion-exclusion
- [ ] Practice number formation
- [ ] Practice largest multiple problems
- [ ] Practice smallest multiple problems
- [ ] Practice remainder problems
- [ ] Practice consecutive-number problems
- [ ] Practice HCL-level mixed questions

---

# 34. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 4]]
- [[Divisibility by 5]]
- [[Divisibility by 6]]
- [[Divisibility by 7]]
- [[Divisibility by 8]]
- [[Divisibility by 9]]
- [[Divisibility by 11]]
- [[Factors]]
- [[Multiples]]
- [[HCF]]
- [[LCM]]
- [[Remainders]]
- [[Digit Problems]]

---

# 35. Quick Revision

> [!summary] One-Minute Revision

### Direct Rule

$$
\boxed{d\mid N\iff N\bmod d=0}
$$

### Count Multiples

$$
\boxed{
\left\lfloor\frac Nd\right\rfloor
}
$$

### Count in Range

$$
\boxed{
\left\lfloor\frac Bd\right\rfloor
-
\left\lfloor\frac{A-1}{d}\right\rfloor
}
$$

### Divisible by Both

Think:

$$
\boxed{\operatorname{LCM}}
$$

### Divisible by Either

Think:

$$
\boxed{
A+B-\text{overlap}
}
$$

### Composite Divisor

Break it into useful factors.

Example:

$$
30=2\times3\times5
$$

Therefore check:

$$
\boxed{2,\ 3,\ 5}
$$

### Missing Digit

Translate the divisibility rule into an equation.

### Key Pattern

> **Don't calculate the whole number blindly. Recognize the divisor → choose the shortcut → solve the condition.**