---
type: concept
subject: aptitude
topic: "Divisibility by 2"
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
  - divisibility-by-2
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 3]]"
  - "[[Even and Odd Numbers]]"
  - "[[Factors]]"
  - "[[Remainders]]"
---

# Divisibility by 2

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `2` if its remainder is `0` when divided by `2`.

Mathematically:

$$
\boxed{n\equiv0\pmod2}
$$

or:

$$
\boxed{n=2k}
$$

where `k` is an integer.

---

## 2. Divisibility Rule

A number is divisible by `2` if its **last digit is even**.

The possible last digits are:

$$
\boxed{0,2,4,6,8}
$$

### Therefore

| Last Digit | Divisible by 2? |
|---:|:---:|
| `0` | ✅ |
| `1` | ❌ |
| `2` | ✅ |
| `3` | ❌ |
| `4` | ✅ |
| `5` | ❌ |
| `6` | ✅ |
| `7` | ❌ |
| `8` | ✅ |
| `9` | ❌ |

> [!important] Golden Rule
> **For divisibility by `2`, check ONLY the last digit.**

---

# 3. Why Only the Last Digit Matters

Every decimal number can be written as:

$$
10a+b
$$

where `b` is the last digit.

Since:

$$
10a
$$

is always divisible by `2`, divisibility depends only on `b`.

Therefore:

$$
\boxed{\text{Divisibility by 2 depends only on the last digit}}
$$

### Example

Consider:

$$
73846
$$

The last digit is:

$$
6
$$

Since `6` is divisible by `2`:

$$
\boxed{73846\text{ is divisible by }2}
$$

---

# 4. Examples

### Example 1

Is `124` divisible by `2`?

Last digit:

$$
4
$$

Since `4` is even:

$$
\boxed{\text{Yes}}
$$

---

### Example 2

Is `357` divisible by `2`?

Last digit:

$$
7
$$

Since `7` is odd:

$$
\boxed{\text{No}}
$$

---

### Example 3

Is `890` divisible by `2`?

Last digit:

$$
0
$$

Therefore:

$$
\boxed{\text{Yes}}
$$

---

### Example 4

Is `12,345,678` divisible by `2`?

Last digit:

$$
8
$$

Therefore:

$$
\boxed{\text{Yes}}
$$

No complete division is required.

---

# 5. Connection With Even Numbers

A number divisible by `2` is an **even number**.

Therefore:

$$
\boxed{\text{Divisible by 2}\iff\text{Even}}
$$

### Even Number Form

Every even integer can be written as:

$$
\boxed{2k}
$$

where:

$$
k\in\mathbb Z
$$

Examples:

$$
2=2(1)
$$

$$
8=2(4)
$$

$$
24=2(12)
$$

$$
100=2(50)
$$

---

# 6. Odd Numbers

A number that is not divisible by `2` is odd.

General form:

$$
\boxed{2k+1}
$$

Examples:

$$
1,3,5,7,9,11,\ldots
$$

Therefore:

$$
\boxed{\text{Odd number}\iff\text{Not divisible by 2}}
$$

---

# 7. Negative Numbers

The rule also works for negative integers.

Examples:

$$
-24
$$

Last digit is `4`.

Therefore:

$$
\boxed{-24\text{ is divisible by 2}}
$$

Similarly:

$$
-37
$$

is not divisible by `2`.

> [!important] Remember
> The sign does not affect divisibility by `2`.

---

# 8. Zero

Zero is divisible by `2`.

Because:

$$
0=2\times0
$$

Therefore:

$$
\boxed{0\div2=0}
$$

and:

$$
\boxed{0\text{ is divisible by 2}}
$$

This also confirms that `0` is even.

---

# 9. Divisibility and Remainder

If a number is divisible by `2`:

$$
\boxed{n\bmod2=0}
$$

If a number is not divisible by `2`:

$$
\boxed{n\bmod2=1}
$$

For integers, these are the only possible remainders when dividing by `2`.

### Example

$$
17\div2
$$

Quotient:

$$
8
$$

Remainder:

$$
1
$$

Therefore:

$$
17\bmod2=1
$$

and `17` is odd.

---

# 10. Important Aptitude Patterns

## Pattern 1 — Direct Divisibility

### Question

Is `98342` divisible by `2`?

Check the last digit:

$$
2
$$

Since `2` is even:

$$
\boxed{\text{Yes}}
$$

---

## Pattern 2 — Large Number

### Question

Is:

$$
928374928374928374
$$

divisible by `2`?

Ignore all digits except the last:

$$
4
$$

Therefore:

$$
\boxed{\text{Yes}}
$$

> [!tip] Exam Shortcut
> **Huge number? Don't calculate it. Check the last digit.**

---

# 11. Pattern — Find a Missing Digit

### Question

Find possible values of `x` so that:

$$
437x
$$

is divisible by `2`.

The last digit must be even.

Therefore:

$$
\boxed{x\in\{0,2,4,6,8\}}
$$

---

## 12. Pattern — Find the Largest Possible Digit

### Question

Find the largest value of `x` such that:

$$
583x
$$

is divisible by `2`.

Possible values:

$$
0,2,4,6,8
$$

Largest:

$$
\boxed{x=8}
$$

---

# 13. Pattern — Find the Smallest Possible Digit

### Question

Find the smallest value of `x` such that:

$$
721x
$$

is divisible by `2`.

Possible values:

$$
0,2,4,6,8
$$

Smallest:

$$
\boxed{x=0}
$$

> [!warning] Read the Question Carefully
> If the question says the number must be a **positive number** or a certain digit cannot be zero, then `0` may not be allowed.

---

# 14. Pattern — Two-Digit Number

### Question

How many two-digit numbers are divisible by `2`?

Two-digit numbers range from:

$$
10\text{ to }99
$$

The even numbers are:

$$
10,12,14,\ldots,98
$$

Using the arithmetic progression formula:

$$
n=\frac{98-10}{2}+1
$$

$$
=44+1
$$

$$
\boxed{45}
$$

Therefore, there are:

$$
\boxed{45}
$$

two-digit numbers divisible by `2`.

---

# 15. Pattern — Count Multiples of 2 in a Range

To find the number of multiples of `2` from `1` to `N`:

$$
\boxed{\left\lfloor\frac N2\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `2`?

$$
\left\lfloor\frac{100}{2}\right\rfloor
=
\boxed{50}
$$

### Example

How many numbers from `1` to `99` are divisible by `2`?

$$
\left\lfloor\frac{99}{2}\right\rfloor
=
\boxed{49}
$$

---

# 16. Pattern — Multiples in an Inclusive Range

To find the number of multiples of `d` from `A` to `B`:

$$
\boxed{
\left\lfloor\frac Bd\right\rfloor
-
\left\lfloor\frac{A-1}{d}\right\rfloor
}
$$

For divisibility by `2`:

$$
\boxed{
\left\lfloor\frac B2\right\rfloor
-
\left\lfloor\frac{A-1}{2}\right\rfloor
}
$$

### Example

How many numbers from `20` to `80` are divisible by `2`?

$$
\left\lfloor\frac{80}{2}\right\rfloor
-
\left\lfloor\frac{19}{2}\right\rfloor
$$

$$
=40-9
$$

$$
\boxed{31}
$$

---

# 17. Pattern — Consecutive Numbers

Among every two consecutive integers:

$$
\boxed{\text{Exactly one is divisible by 2}}
$$

Example:

$$
15,16
$$

`16` is divisible by `2`.

Another pair:

$$
28,29
$$

`28` is divisible by `2`.

Therefore:

$$
\boxed{\text{Every pair of consecutive integers contains exactly one even number}}
$$

---

# 18. Pattern — Consecutive Integers

Among `n` consecutive integers, the number of even integers is either:

$$
\boxed{\left\lfloor\frac n2\right\rfloor}
$$

or:

$$
\boxed{\left\lceil\frac n2\right\rceil}
$$

depending on the starting number.

### Example

Among `10` consecutive integers:

$$
20,21,22,\ldots,29
$$

Even numbers:

$$
20,22,24,26,28
$$

There are:

$$
\boxed{5}
$$

---

# 19. Divisibility by 2 and Powers of 2

Divisibility by higher powers of `2` depends on more ending digits.

### Divisible by `2`

Check:

$$
\boxed{\text{Last 1 digit}}
$$

### Divisible by `4`

Check:

$$
\boxed{\text{Last 2 digits}}
$$

### Divisible by `8`

Check:

$$
\boxed{\text{Last 3 digits}}
$$

### Divisible by `16`

Check:

$$
\boxed{\text{Last 4 digits}}
$$

> [!important] Pattern
> For divisibility by:
>
> $$2^n$$
>
> the required number of ending digits increases accordingly in decimal representation.

For aptitude, memorize the standard rules for `2`, `4`, and `8`.

---

# 20. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking the entire number unnecessarily.
- ❌ Looking at the first digit instead of the last digit.
- ❌ Thinking numbers ending in `5` are divisible by `2`.
- ❌ Forgetting that numbers ending in `0` are divisible by `2`.
- ❌ Thinking negative even numbers are not divisible by `2`.
- ❌ Forgetting that `0` is divisible by `2`.
- ❌ Confusing divisibility by `2` with divisibility by `4`.
- ❌ Performing complete division when the last digit gives the answer immediately.

---

# 21. Exam Strategy

> [!tip] 2-Second Method

When asked:

> "Is this number divisible by `2`?"

Do only this:

### Step 1

Look at the last digit.

### Step 2

Check whether it is:

$$
0,2,4,6,8
$$

### Step 3

Answer immediately.

No full division is required.

---

# 22. HCL Preparation Priority

**Priority:** 🔥 Very High

This is a basic rule, but it becomes extremely useful in:

- Missing-digit problems
- Number formation
- Even/odd questions
- Factorization
- HCF and LCM
- Remainder problems
- Counting problems
- Divisibility combinations

---

# 23. Practice Checklist

- [ ] Memorize the rule
- [ ] Identify even numbers instantly
- [ ] Identify odd numbers instantly
- [ ] Practice large-number questions
- [ ] Practice missing-digit questions
- [ ] Practice smallest/largest digit questions
- [ ] Practice counting multiples
- [ ] Practice range-based questions
- [ ] Practice consecutive-number questions
- [ ] Connect divisibility by `2` with even/odd patterns

---

# 24. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 3]]
- [[Divisibility by 4]]
- [[Divisibility by 5]]
- [[Even and Odd Numbers]]
- [[Factors]]
- [[Multiples]]
- [[Remainders]]
- [[Digit Problems]]
- [[Number Formation]]

---

# 25. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{\text{Last digit}\in\{0,2,4,6,8\}}
$$

$$
\Longrightarrow
\boxed{\text{Divisible by 2}}
$$

### Even Number

$$
\boxed{n=2k}
$$

### Remainder

$$
\boxed{n\bmod2=0}
$$

for an even number.

### Odd Number

$$
\boxed{n=2k+1}
$$

### Count Multiples from `1` to `N`

$$
\boxed{\left\lfloor\frac N2\right\rfloor}
$$

### Count Multiples from `A` to `B`

$$
\boxed{
\left\lfloor\frac B2\right\rfloor
-
\left\lfloor\frac{A-1}{2}\right\rfloor
}
$$

### Key Pattern

> **Divisibility by `2` = Check only the last digit.**

> **`0, 2, 4, 6, 8` → divisible by `2`.**