---
type: concept
subject: aptitude
topic: "Divisibility Rules"
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
  - divisibility-rules
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 4]]"
  - "[[Divisibility by 5]]"
  - "[[Divisibility by 6]]"
  - "[[Divisibility by 7]]"
  - "[[Divisibility by 8]]"
  - "[[Divisibility by 9]]"
  - "[[Divisibility by 11]]"
  - "[[Factors]]"
  - "[[Remainders]]"
---

# Divisibility Rules

## 1. Overview

> [!summary] Core Idea
> A number is divisible by another number if the division leaves **remainder `0`**.

For integers `a` and `b`, where:

$$
b\neq0
$$

`a` is divisible by `b` if:

$$
\boxed{a=b\times k}
$$

for some integer `k`.

Equivalently:

$$
\boxed{a\div b=\text{integer}}
$$

and:

$$
\boxed{a\bmod b=0}
$$

### Example

Is `24` divisible by `6`?

$$
24\div6=4
$$

Remainder:

$$
0
$$

Therefore:

$$
\boxed{24\text{ is divisible by }6}
$$

---

# 2. Divisor, Dividend, Quotient and Remainder

In:

$$
17\div5
$$

we have:

- Dividend = `17`
- Divisor = `5`
- Quotient = `3`
- Remainder = `2`

The fundamental division relationship is:

$$
\boxed{\text{Dividend}=(\text{Divisor}\times\text{Quotient})+\text{Remainder}}
$$

Therefore:

$$
17=(5\times3)+2
$$

$$
17=15+2
$$

---

# 3. Divisibility Condition

A number `N` is divisible by `d` if:

$$
\boxed{N=dq}
$$

for some integer `q`.

Another way:

$$
\boxed{N\bmod d=0}
$$

### Example

Check whether `84` is divisible by `7`.

$$
84=7\times12
$$

Therefore:

$$
\boxed{84\text{ is divisible by }7}
$$

---

# 4. Why Divisibility Rules Matter

> [!important] Aptitude Importance
> Divisibility rules allow you to determine whether a number is divisible by another number **without performing complete division**.

They are especially useful in:

- HCF
- LCM
- Prime factorization
- Remainders
- Number formation
- Digit problems
- Unit-digit problems
- Large-number calculations

---

# 5. Master Divisibility Table

> [!important] Must Memorize

| Divisor | Divisibility Rule |
|---:|---|
| `2` | Last digit is `0, 2, 4, 6, 8` |
| `3` | Sum of digits is divisible by `3` |
| `4` | Last two digits are divisible by `4` |
| `5` | Last digit is `0` or `5` |
| `6` | Divisible by both `2` and `3` |
| `7` | Double the last digit and subtract from remaining number |
| `8` | Last three digits are divisible by `8` |
| `9` | Sum of digits is divisible by `9` |
| `11` | Difference between alternating digit sums is `0` or a multiple of `11` |

> [!tip] High-Priority Rules
> Memorize `2, 3, 4, 5, 6, 8, 9, 11` first.
>
> The rule for `7` requires more practice.

---

# 6. Divisibility by 2

A number is divisible by `2` if its last digit is:

$$
\boxed{0,2,4,6,8}
$$

### Examples

`124`:

Last digit = `4`

Therefore:

$$
\boxed{124\text{ is divisible by }2}
$$

`137`:

Last digit = `7`

Therefore:

$$
\boxed{137\text{ is not divisible by }2}
$$

> [!tip] Shortcut
> **Only check the last digit.**

---

# 7. Divisibility by 3

A number is divisible by `3` if the sum of its digits is divisible by `3`.

### Example

Check `123`.

Digit sum:

$$
1+2+3=6
$$

Since:

$$
6\div3=2
$$

Therefore:

$$
\boxed{123\text{ is divisible by }3}
$$

### Example

Check `124`.

$$
1+2+4=7
$$

`7` is not divisible by `3`.

Therefore:

$$
\boxed{124\text{ is not divisible by }3}
$$

> [!tip] Shortcut
> **Add the digits. Ignore the actual size of the number.**

---

# 8. Divisibility by 4

A number is divisible by `4` if its **last two digits** form a number divisible by `4`.

### Example

Check `2316`.

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
\boxed{2316\text{ is divisible by }4}
$$

### Example

Check `1258`.

Last two digits:

$$
58
$$

Since:

$$
58\div4
$$

is not an integer:

$$
\boxed{1258\text{ is not divisible by }4}
$$

> [!tip] Shortcut
> **For divisibility by `4`, ignore everything except the last two digits.**

---

# 9. Divisibility by 5

A number is divisible by `5` if its last digit is:

$$
\boxed{0\text{ or }5}
$$

### Examples

`125` → divisible by `5`

`340` → divisible by `5`

`123` → not divisible by `5`

> [!tip] Shortcut
> **Last digit = `0` or `5`.**

---

# 10. Divisibility by 6

A number is divisible by `6` if it is divisible by both:

$$
2
$$

and:

$$
3
$$

Therefore:

$$
\boxed{\text{Divisible by 6}=\text{Divisible by 2 AND 3}}
$$

### Example

Check `234`.

#### Test for 2

Last digit = `4`

So it is divisible by `2`.

#### Test for 3

Digit sum:

$$
2+3+4=9
$$

`9` is divisible by `3`.

Therefore:

$$
\boxed{234\text{ is divisible by }6}
$$

> [!important] Pattern
> **6 = 2 × 3**
>
> So check both divisibility rules.

---

# 11. Divisibility by 7

The divisibility rule for `7` is slightly different.

### Rule

1. Separate the last digit.
2. Double the last digit.
3. Subtract the result from the remaining number.
4. Repeat if necessary.
5. If the final result is divisible by `7`, the original number is divisible by `7`.

### Example

Check `203`.

Last digit:

$$
3
$$

Double:

$$
2\times3=6
$$

Remaining number:

$$
20
$$

Subtract:

$$
20-6=14
$$

Since:

$$
14\div7=2
$$

Therefore:

$$
\boxed{203\text{ is divisible by }7}
$$

### Another Example

Check `371`.

Last digit:

$$
1
$$

Double:

$$
2
$$

Remaining:

$$
37
$$

Subtract:

$$
37-2=35
$$

Since:

$$
35\div7=5
$$

Therefore:

$$
\boxed{371\text{ is divisible by }7}
$$

> [!tip] Pattern
> **Double last digit → Subtract → Repeat**

---

# 12. Divisibility by 8

A number is divisible by `8` if its **last three digits** form a number divisible by `8`.

### Example

Check `5128`.

Last three digits:

$$
128
$$

Since:

$$
128\div8=16
$$

Therefore:

$$
\boxed{5128\text{ is divisible by }8}
$$

### Example

Check `4314`.

Last three digits:

$$
314
$$

Since `314` is not divisible by `8`:

$$
\boxed{4314\text{ is not divisible by }8}
$$

> [!tip] Shortcut
> **For `8`, check only the last three digits.**

---

# 13. Divisibility by 9

A number is divisible by `9` if the sum of its digits is divisible by `9`.

### Example

Check `729`.

$$
7+2+9=18
$$

Since:

$$
18\div9=2
$$

Therefore:

$$
\boxed{729\text{ is divisible by }9}
$$

### Example

Check `725`.

$$
7+2+5=14
$$

`14` is not divisible by `9`.

Therefore:

$$
\boxed{725\text{ is not divisible by }9}
$$

> [!tip] Important
> The rules for `3` and `9` are similar:
>
> **Divisibility by `3` → digit sum divisible by `3`.**
>
> **Divisibility by `9` → digit sum divisible by `9`.**

---

# 14. Divisibility by 11

A number is divisible by `11` if the difference between the sums of alternating digits is:

$$
\boxed{0\text{ or a multiple of }11}
$$

### Example

Check `121`.

Separate alternating positions:

$$
(1+1)-2
$$

$$
=2-2
$$

$$
=0
$$

Therefore:

$$
\boxed{121\text{ is divisible by }11}
$$

---

### Example

Check `1331`.

$$
(1+3)-(3+1)
$$

$$
4-4=0
$$

Therefore:

$$
\boxed{1331\text{ is divisible by }11}
$$

---

### Example

Check `2728`.

$$
(2+2)-(7+8)
$$

$$
4-15=-11
$$

Since `-11` is a multiple of `11`:

$$
\boxed{2728\text{ is divisible by }11}
$$

> [!tip] Shortcut
> **Alternating digit sum → Difference → Check multiple of `11`.**

---

# 15. Divisibility by Composite Numbers

Sometimes a divisibility rule can be created from smaller factors.

For example:

$$
6=2\times3
$$

Therefore:

$$
\boxed{\text{Divisible by 6} \iff \text{Divisible by 2 and 3}}
$$

Similarly:

$$
10=2\times5
$$

So:

$$
\boxed{\text{Divisible by 10} \iff \text{Last digit is 0}}
$$

And:

$$
15=3\times5
$$

Therefore a number divisible by both `3` and `5` is divisible by `15`.

> [!important] Pattern
> If two factors are **coprime**, divisibility by both implies divisibility by their product.

---

# 16. Divisibility by 10

A number is divisible by `10` if its last digit is:

$$
\boxed{0}
$$

Examples:

$$
120,\quad450,\quad1000
$$

are divisible by `10`.

---

# 17. Divisibility by 12

Since:

$$
12=3\times4
$$

a number is divisible by `12` if it is divisible by both `3` and `4`.

### Example

Check `312`.

Digit sum:

$$
3+1+2=6
$$

So it is divisible by `3`.

Last two digits:

$$
12
$$

`12` is divisible by `4`.

Therefore:

$$
\boxed{312\text{ is divisible by }12}
$$

---

# 18. Divisibility by 15

Since:

$$
15=3\times5
$$

a number is divisible by `15` if it is divisible by both `3` and `5`.

### Example

Check `345`.

Digit sum:

$$
3+4+5=12
$$

So divisible by `3`.

Last digit:

$$
5
$$

So divisible by `5`.

Therefore:

$$
\boxed{345\text{ is divisible by }15}
$$

---

# 19. Divisibility by 18

Since:

$$
18=2\times9
$$

a number is divisible by `18` if it is divisible by both `2` and `9`.

### Example

Check `126`.

Last digit = `6` → divisible by `2`.

Digit sum:

$$
1+2+6=9
$$

→ divisible by `9`.

Therefore:

$$
\boxed{126\text{ is divisible by }18}
$$

---

# 20. Divisibility by 20

Since:

$$
20=4\times5
$$

A number is divisible by `20` when its last two digits are divisible by `20`.

Possible last two digits include:

$$
00,20,40,60,80
$$

Therefore:

$$
\boxed{\text{Last two digits must be a multiple of 20}}
$$

---

# 21. Divisibility by 25

A number is divisible by `25` if its last two digits are:

$$
\boxed{00,25,50,75}
$$

### Examples

`125` → last two digits `25` → divisible by `25`.

`450` → last two digits `50` → divisible by `25`.

`725` → last two digits `25` → divisible by `25`.

> [!tip] Shortcut
> **For `25`, memorize: `00, 25, 50, 75`.**

---

# 22. Divisibility by 100

A number is divisible by `100` if its last two digits are:

$$
\boxed{00}
$$

Examples:

$$
500,\quad1200,\quad7500
$$

---

# 23. Divisibility by 1000

A number is divisible by `1000` if its last three digits are:

$$
\boxed{000}
$$

Examples:

$$
5000,\quad12000,\quad75000
$$

---

# 24. Important Aptitude Patterns

## Pattern 1 — Find a Missing Digit

### Question

Find the value of `x` so that:

$$
52x
$$

is divisible by `3`.

For divisibility by `3`, digit sum must be divisible by `3`.

$$
5+2+x=7+x
$$

Possible values:

$$
7+x\equiv0\pmod3
$$

Therefore:

$$
x=2,5,8
$$

So:

$$
\boxed{x\in\{2,5,8\}}
$$

---

## Pattern 2 — Missing Digit for Divisibility by 9

Find `x` so that:

$$
73x
$$

is divisible by `9`.

Digit sum:

$$
7+3+x=10+x
$$

Need:

$$
10+x
$$

to be divisible by `9`.

Therefore:

$$
x=8
$$

because:

$$
10+8=18
$$

Hence:

$$
\boxed{x=8}
$$

---

# 25. Pattern — Divisibility by Multiple Numbers

### Question

Is `540` divisible by `6`?

For `6`, check:

- Divisible by `2`
- Divisible by `3`

Last digit:

$$
0
$$

Therefore divisible by `2`.

Digit sum:

$$
5+4+0=9
$$

Therefore divisible by `3`.

Hence:

$$
\boxed{540\text{ is divisible by }6}
$$

---

# 26. Pattern — Find the Smallest Number to Add

Suppose a number leaves remainder `r` when divided by `d`.

The smallest number that must be **added** to make it divisible by `d` is:

$$
\boxed{d-r}
$$

### Example

Find the smallest number to add to `47` to make it divisible by `6`.

$$
47\div6
$$

Remainder:

$$
5
$$

Therefore:

$$
6-5=1
$$

Answer:

$$
\boxed{1}
$$

---

# 27. Pattern — Find the Smallest Number to Subtract

If a number leaves remainder `r` when divided by `d`, the smallest number to subtract to make it divisible by `d` is:

$$
\boxed{r}
$$

### Example

Find the smallest number to subtract from `47` to make it divisible by `6`.

Remainder:

$$
47\bmod6=5
$$

Therefore:

$$
\boxed{5}
$$

Because:

$$
47-5=42
$$

and:

$$
42\div6=7
$$

---

# 28. Important Formula Sheet

> [!important] Must Remember

| Divisor | Rule |
|---:|---|
| `2` | Last digit is `0,2,4,6,8` |
| `3` | Digit sum divisible by `3` |
| `4` | Last 2 digits divisible by `4` |
| `5` | Last digit `0` or `5` |
| `6` | Divisible by `2` and `3` |
| `7` | Double last digit and subtract from remaining number |
| `8` | Last 3 digits divisible by `8` |
| `9` | Digit sum divisible by `9` |
| `10` | Last digit `0` |
| `11` | Alternating digit-sum difference is `0` or multiple of `11` |
| `12` | Divisible by `3` and `4` |
| `15` | Divisible by `3` and `5` |
| `18` | Divisible by `2` and `9` |
| `20` | Last 2 digits divisible by `20` |
| `25` | Last 2 digits `00,25,50,75` |
| `100` | Last 2 digits `00` |
| `1000` | Last 3 digits `000` |

---

# 29. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking the entire number for divisibility by `2`.
- ❌ Checking only the last digit for divisibility by `3`.
- ❌ Checking the last three digits for divisibility by `4`.
- ❌ Forgetting that `6` requires both `2` and `3`.
- ❌ Assuming a number ending in `1,3,7,9` is automatically prime.
- ❌ Using the `7` rule incorrectly.
- ❌ Forgetting alternating positions for divisibility by `11`.
- ❌ Confusing divisibility by `3` with divisibility by `9`.
- ❌ Forgetting that the digit sum can itself be reduced repeatedly.
- ❌ Performing complete division when a divisibility rule is available.

---

# 30. Exam Strategy

> [!tip] Fast Approach

When checking divisibility:

### Step 1

Identify the divisor.

### Step 2

Use the shortest applicable rule.

### Step 3

Avoid full division.

### Step 4

For composite divisors, break them into useful factors.

Examples:

$$
6=2\times3
$$

$$
12=3\times4
$$

$$
15=3\times5
$$

$$
18=2\times9
$$

### Step 5

For missing-digit questions, convert the divisibility rule into an equation.

---

# 31. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

Divisibility is a **core aptitude topic** because it connects directly with:

- Factors
- Multiples
- HCF
- LCM
- Remainders
- Unit digits
- Number formation
- Digit problems

### Master These First

1. Divisibility by `2`
2. Divisibility by `3`
3. Divisibility by `4`
4. Divisibility by `5`
5. Divisibility by `6`
6. Divisibility by `8`
7. Divisibility by `9`
8. Divisibility by `11`
9. Divisibility by `7`
10. Missing-digit problems

---

# 32. Practice Checklist

- [ ] Understand divisibility
- [ ] Memorize the basic rules
- [ ] Practice divisibility by `2`
- [ ] Practice divisibility by `3`
- [ ] Practice divisibility by `4`
- [ ] Practice divisibility by `5`
- [ ] Practice divisibility by `6`
- [ ] Practice divisibility by `7`
- [ ] Practice divisibility by `8`
- [ ] Practice divisibility by `9`
- [ ] Practice divisibility by `11`
- [ ] Practice composite divisors
- [ ] Practice missing-digit problems
- [ ] Practice add/subtract remainder problems
- [ ] Revise common traps

---

# 33. Related Topics

- [[01. Number System]]
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
- [[Unit Digit]]
- [[Digit Problems]]

---

# 34. Quick Revision

> [!summary] One-Minute Revision

### `2`

$$
\boxed{\text{Last digit is even}}
$$

### `3`

$$
\boxed{\text{Digit sum divisible by 3}}
$$

### `4`

$$
\boxed{\text{Last 2 digits divisible by 4}}
$$

### `5`

$$
\boxed{\text{Last digit }0\text{ or }5}
$$

### `6`

$$
\boxed{\text{Divisible by 2 and 3}}
$$

### `7`

$$
\boxed{\text{Double last digit and subtract}}
$$

### `8`

$$
\boxed{\text{Last 3 digits divisible by 8}}
$$

### `9`

$$
\boxed{\text{Digit sum divisible by 9}}
$$

### `11`

$$
\boxed{\text{Alternating digit-sum difference is }0\text{ or a multiple of }11}
$$

### Missing Digit

> **Use the divisibility rule to create an equation for the missing digit.**

### Add to Make Divisible

If remainder is `r`:

$$
\boxed{\text{Add}=d-r}
$$

### Subtract to Make Divisible

$$
\boxed{\text{Subtract}=r}
$$

> [!important] Final Pattern
> **Don't calculate the whole number when a divisibility rule can solve the question in seconds.**