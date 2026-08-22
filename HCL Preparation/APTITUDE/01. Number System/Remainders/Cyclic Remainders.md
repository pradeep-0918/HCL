---
type: concept
subject: aptitude
topic: "Cyclic Remainders"
parent: "01. Number System/Remainders"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - remainders
  - cyclic-remainders
  - modular-arithmetic
  - powers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Remainders]]"
  - "[[Basic Remainder]]"
  - "[[Remainder Theorem]]"
  - "[[Large Number Remainders]]"
  - "[[Remainder Patterns]]"
  - "[[Unit Digit]]"
---

# Cyclic Remainders

## 1. Core Concept

> [!summary] Definition
> When powers of a number are divided by a fixed divisor, their remainders may repeat in a fixed pattern.
>
> This repeating pattern is called a **cycle** or **cyclicity**.

For example, consider powers of `2` modulo `10`:

$$
2^1\bmod10=2
$$

$$
2^2\bmod10=4
$$

$$
2^3\bmod10=8
$$

$$
2^4\bmod10=6
$$

$$
2^5\bmod10=2
$$

The pattern is:

$$
\boxed{2,4,8,6}
$$

Then it repeats.

So the cycle length is:

$$
\boxed4
$$

---

# 2. Why Cyclicity Is Important

Questions may contain enormous powers such as:

$$
2^{1000}
$$

or:

$$
7^{2026}
$$

Calculating the complete power is impossible in an aptitude exam.

Instead:

$$
\boxed{
\text{Find the cycle}
\rightarrow
\text{Find exponent position}
\rightarrow
\text{Take corresponding remainder}
}
$$

---

# 3. Basic Cycle Method

Suppose:

$$
a^n\bmod m
$$

is required.

### Step 1

Calculate:

$$
a^1\bmod m
$$

$$
a^2\bmod m
$$

$$
a^3\bmod m
$$

and continue until the remainders repeat.

### Step 2

Find the cycle length.

Let it be:

$$
k
$$

### Step 3

Find:

$$
n\bmod k
$$

### Step 4

Use the corresponding position in the cycle.

---

# 4. Example — Power of 2 Modulo 10

Find:

$$
2^{100}\bmod10
$$

Cycle:

| Power | Remainder |
|---:|---:|
| $2^1$ | `2` |
| $2^2$ | `4` |
| $2^3$ | `8` |
| $2^4$ | `6` |
| $2^5$ | `2` |

Cycle:

$$
\boxed{2,4,8,6}
$$

Cycle length:

$$
4
$$

Now:

$$
100\bmod4=0
$$

A remainder of `0` means we take the **last element of the cycle**.

Therefore:

$$
\boxed6
$$

---

# 5. The Most Important Rule

> [!important] Remainder `0` Rule

If:

$$
n\bmod k=0
$$

do **not** take the first element.

Take the:

$$
\boxed{k^{th}\text{ element}}
$$

of the cycle.

### Example

Cycle:

$$
2,4,8,6
$$

For:

$$
2^{100}
$$

we have:

$$
100\bmod4=0
$$

Therefore take the 4th element:

$$
\boxed6
$$

---

# 6. Example — `3^100`

Find:

$$
3^{100}\bmod10
$$

Cycle of `3`:

$$
3^1\rightarrow3
$$

$$
3^2\rightarrow9
$$

$$
3^3\rightarrow7
$$

$$
3^4\rightarrow1
$$

$$
3^5\rightarrow3
$$

Cycle:

$$
\boxed{3,9,7,1}
$$

Cycle length:

$$
4
$$

Now:

$$
100\bmod4=0
$$

Take the 4th element:

$$
\boxed1
$$

---

# 7. Example — `7^2026`

Find:

$$
7^{2026}\bmod10
$$

Cycle:

$$
7,9,3,1
$$

Cycle length:

$$
4
$$

Calculate:

$$
2026\bmod4=2
$$

Take the 2nd element:

$$
\boxed9
$$

Therefore:

$$
\boxed{7^{2026}\bmod10=9}
$$

---

# 8. Example — `9^999`

Find:

$$
9^{999}\bmod10
$$

Cycle:

$$
9,1
$$

Cycle length:

$$
2
$$

Calculate:

$$
999\bmod2=1
$$

Take the 1st element:

$$
\boxed9
$$

---

# 9. Example — `4^123`

Find:

$$
4^{123}\bmod10
$$

Cycle:

$$
4,6
$$

Cycle length:

$$
2
$$

Calculate:

$$
123\bmod2=1
$$

Therefore:

$$
\boxed4
$$

---

# 10. Standard Unit-Digit Cycles

These cycles are extremely important for aptitude.

> [!important] Memorize

### Base `2`

$$
\boxed{2,4,8,6}
$$

Cycle length:

$$
\boxed4
$$

### Base `3`

$$
\boxed{3,9,7,1}
$$

Cycle length:

$$
\boxed4
$$

### Base `4`

$$
\boxed{4,6}
$$

Cycle length:

$$
\boxed2
$$

### Base `7`

$$
\boxed{7,9,3,1}
$$

Cycle length:

$$
\boxed4
$$

### Base `8`

$$
\boxed{8,4,2,6}
$$

Cycle length:

$$
\boxed4
$$

### Base `9`

$$
\boxed{9,1}
$$

Cycle length:

$$
\boxed2
$$

---

# 11. Bases `0`, `1`, `5`, and `6`

These are extremely easy.

### Base `0`

$$
0^n=0
$$

Therefore:

$$
\boxed0
$$

### Base `1`

$$
1^n=1
$$

Therefore:

$$
\boxed1
$$

### Base `5`

Every positive power ends in:

$$
\boxed5
$$

### Base `6`

Every positive power ends in:

$$
\boxed6
$$

Therefore:

$$
\boxed{
0,1,5,6
}
$$

have cycle length `1` for unit-digit questions.

---

# 12. Complete Unit-Digit Cycle Table

| Last digit of base | Cycle | Length |
|---:|---|---:|
| `0` | `0` | 1 |
| `1` | `1` | 1 |
| `2` | `2, 4, 8, 6` | 4 |
| `3` | `3, 9, 7, 1` | 4 |
| `4` | `4, 6` | 2 |
| `5` | `5` | 1 |
| `6` | `6` | 1 |
| `7` | `7, 9, 3, 1` | 4 |
| `8` | `8, 4, 2, 6` | 4 |
| `9` | `9, 1` | 2 |

> [!tip] Important
> For unit-digit questions, **only the last digit of the base matters**.

---

# 13. Why Only the Last Digit Matters

Suppose:

$$
123^5
$$

is required modulo `10`.

Since:

$$
123\bmod10=3
$$

we can replace:

$$
123
$$

with:

$$
3
$$

Therefore:

$$
123^5\bmod10
=
3^5\bmod10
$$

So:

$$
\boxed{\text{Last digit of base is enough for unit digit}}
$$

---

# 14. Example — Large Base

Find the unit digit of:

$$
1234567^{2026}
$$

Only the last digit matters:

$$
1234567\rightarrow7
$$

So calculate:

$$
7^{2026}
$$

Cycle:

$$
7,9,3,1
$$

Now:

$$
2026\bmod4=2
$$

Take the 2nd element:

$$
\boxed9
$$

---

# 15. Cycle Position Formula

Suppose cycle length is:

$$
k
$$

Then calculate:

$$
\boxed{
p=n\bmod k
}
$$

If:

$$
p\ne0
$$

use the `p`th element.

If:

$$
p=0
$$

use the `k`th element.

Therefore:

$$
\boxed{
\text{Position}=
\begin{cases}
n\bmod k,&n\bmod k\ne0\\
k,&n\bmod k=0
\end{cases}
}
$$

---

# 16. Example — Position `0`

Cycle:

$$
3,9,7,1
$$

Find:

$$
3^{48}\bmod10
$$

Cycle length:

$$
4
$$

Exponent:

$$
48\bmod4=0
$$

Therefore use position:

$$
4
$$

4th element:

$$
\boxed1
$$

---

# 17. Example — Position `3`

Find:

$$
8^{27}\bmod10
$$

Cycle:

$$
8,4,2,6
$$

Cycle length:

$$
4
$$

Calculate:

$$
27\bmod4=3
$$

Take the 3rd element:

$$
\boxed2
$$

---

# 18. Example — Position `1`

Find:

$$
3^{101}\bmod10
$$

Cycle:

$$
3,9,7,1
$$

Cycle length:

$$
4
$$

Calculate:

$$
101\bmod4=1
$$

Take the 1st element:

$$
\boxed3
$$

---

# 19. Cyclicity Beyond Unit Digits

Cyclic remainders are not limited to modulo `10`.

For example:

$$
2^n\bmod7
$$

Calculate:

$$
2^1\bmod7=2
$$

$$
2^2\bmod7=4
$$

$$
2^3\bmod7=1
$$

Then:

$$
2^4\bmod7=2
$$

The cycle is:

$$
\boxed{2,4,1}
$$

Cycle length:

$$
\boxed3
$$

---

# 20. Example — `2^100 mod 7`

Cycle:

$$
2,4,1
$$

Cycle length:

$$
3
$$

Calculate:

$$
100\bmod3=1
$$

Take the 1st element:

$$
\boxed2
$$

Therefore:

$$
\boxed{2^{100}\bmod7=2}
$$

---

# 21. Example — `3^100 mod 7`

Calculate the cycle:

$$
3^1\bmod7=3
$$

$$
3^2\bmod7=2
$$

$$
3^3\bmod7=6
$$

$$
3^4\bmod7=4
$$

$$
3^5\bmod7=5
$$

$$
3^6\bmod7=1
$$

Cycle:

$$
\boxed{3,2,6,4,5,1}
$$

Length:

$$
6
$$

Now:

$$
100\bmod6=4
$$

4th element:

$$
\boxed4
$$

---

# 22. How to Find a Cycle

For:

$$
a^n\bmod m
$$

### Step 1

Calculate:

$$
a\bmod m
$$

### Step 2

Calculate successive powers.

### Step 3

Reduce each result modulo `m`.

### Step 4

Stop when the initial remainder pattern repeats.

### Step 5

Record the cycle length.

### Step 6

Calculate:

$$
n\bmod\text{cycle length}
$$

### Step 7

Select the corresponding position.

---

# 23. Important Pattern — Cycle Starts Immediately

For many common unit-digit bases, the cycle begins from:

$$
a^1
$$

Example:

$$
2,4,8,6
$$

However, in more general modular problems, the sequence may have a **pre-period** before entering a cycle.

> [!warning] Aptitude Tip
> For standard unit-digit questions, the simple cycle table is usually enough.
>
> For general modular arithmetic, do not assume every sequence begins with a cycle from the first power.

---

# 24. Cycle Length and Divisor

If the cycle length is:

$$
k
$$

then exponents separated by multiples of `k` give the same position:

$$
n,\ n+k,\ n+2k,\ldots
$$

Therefore:

$$
\boxed{
a^n\bmod m
=
a^{n+k}\bmod m
}
$$

when the sequence is in the repeating cycle.

---

# 25. Example

For unit digit of powers of `2`:

Cycle length:

$$
4
$$

Therefore:

$$
2^{10}
$$

and:

$$
2^{14}
$$

have the same unit digit.

Indeed:

$$
2^{10}\rightarrow4
$$

and:

$$
2^{14}\rightarrow4
$$

---

# 26. Exponent Reduction

If the cycle length is `k`, reduce:

$$
n\bmod k
$$

before selecting the cycle position.

This can turn a huge exponent into a tiny number.

### Example

$$
7^{1000000001}
$$

Cycle length:

$$
4
$$

Calculate:

$$
1000000001\bmod4=1
$$

Therefore use the first element of:

$$
7,9,3,1
$$

Answer:

$$
\boxed7
$$

---

# 27. Power of a Power

Suppose:

$$
(a^p)^q=a^{pq}
$$

Therefore, for unit-digit questions:

$$
(a^p)^q\bmod10
$$

can be treated as:

$$
a^{pq}\bmod10
$$

But be careful with very large exponents.

> [!tip] Shortcut
> First simplify the exponent algebraically, then apply cyclicity.

---

# 28. Example — Power of a Power

Find the unit digit of:

$$
(2^3)^{100}
$$

Rewrite:

$$
(2^3)^{100}=2^{300}
$$

Cycle of `2`:

$$
2,4,8,6
$$

Calculate:

$$
300\bmod4=0
$$

Therefore take the 4th element:

$$
\boxed6
$$

---

# 29. Product of Powers

Suppose:

$$
a^m\times a^n
$$

Then:

$$
\boxed{
a^m\times a^n=a^{m+n}
}
$$

Therefore simplify the exponent first.

### Example

Find the unit digit of:

$$
2^{20}\times2^{30}
$$

Combine:

$$
2^{20+30}=2^{50}
$$

Now:

$$
50\bmod4=2
$$

Second element of:

$$
2,4,8,6
$$

is:

$$
\boxed4
$$

---

# 30. Different Bases

For:

$$
2^{20}\times3^{15}
$$

you cannot combine the bases.

Instead, calculate each cyclic remainder separately.

For unit digit:

### `2`

Cycle length:

$$
4
$$

$$
20\bmod4=0
$$

Therefore:

$$
2^{20}\rightarrow6
$$

### `3`

Cycle length:

$$
4
$$

$$
15\bmod4=3
$$

Therefore:

$$
3^{15}\rightarrow7
$$

Now:

$$
6\times7=42
$$

Unit digit:

$$
\boxed2
$$

---

# 31. Nested Powers

Nested powers can become tricky.

For example:

$$
2^{3^{100}}
$$

The exponent is itself huge.

For unit digit of `2`, cycle length is:

$$
4
$$

Therefore we only need:

$$
3^{100}\bmod4
$$

Now:

$$
3^1\bmod4=3
$$

$$
3^2\bmod4=1
$$

Cycle:

$$
3,1
$$

Since `100` is even:

$$
3^{100}\bmod4=1
$$

Therefore:

$$
2^{3^{100}}
$$

corresponds to position `1` in the cycle of `2`.

Hence:

$$
\boxed2
$$

> [!important] Pattern
> **Nested power → first find the exponent modulo the outer cycle length.**

---

# 32. Example — Nested Power

Find the unit digit of:

$$
3^{2^{100}}
$$

Cycle of `3`:

$$
3,9,7,1
$$

Need:

$$
2^{100}\bmod4
$$

Since:

$$
2^2=4
$$

all higher powers of `2` are divisible by `4`.

Therefore:

$$
2^{100}\bmod4=0
$$

Position `0` means take the 4th element of the cycle:

$$
\boxed1
$$

---

# 33. Important Nested-Power Pattern

For:

$$
a^{b^c}\bmod m
$$

### Step 1

Find the cycle length of `a` modulo `m`.

### Step 2

Reduce:

$$
b^c
$$

modulo that cycle length.

### Step 3

Use the resulting position.

This often requires another cycle calculation.

---

# 34. Common Unit-Digit Cycle Shortcut

For bases ending in:

$$
2,3,7,8
$$

cycle length:

$$
\boxed4
$$

For bases ending in:

$$
4,9
$$

cycle length:

$$
\boxed2
$$

For bases ending in:

$$
0,1,5,6
$$

cycle length:

$$
\boxed1
$$

This is extremely important for aptitude.

---

# 35. Unit-Digit Shortcut Table

| Base ends in | Cycle length |
|---:|---:|
| `0` | 1 |
| `1` | 1 |
| `2` | 4 |
| `3` | 4 |
| `4` | 2 |
| `5` | 1 |
| `6` | 1 |
| `7` | 4 |
| `8` | 4 |
| `9` | 2 |

> [!tip] Fastest Recognition
>
> **Only 3 cycle lengths are needed for unit digits:**
>
> $$\boxed{1,\ 2,\ 4}$$

---

# 36. Example — Huge Exponent

Find the unit digit of:

$$
8^{20252026}
$$

Cycle:

$$
8,4,2,6
$$

Cycle length:

$$
4
$$

Now:

$$
20252026\bmod4=2
$$

Take the second element:

$$
\boxed4
$$

---

# 37. Example — Base Ending in 6

Find the unit digit of:

$$
876543216^{999999}
$$

Only the last digit matters:

$$
6
$$

Every positive power of `6` ends in `6`.

Therefore:

$$
\boxed6
$$

No cycle calculation is required.

---

# 38. Example — Base Ending in 5

Find:

$$
12345675^{2026}
$$

Only the last digit matters:

$$
5
$$

Every positive power of `5` ends in `5`.

Therefore:

$$
\boxed5
$$

---

# 39. Example — Base Ending in 9

Find:

$$
9999999^{2026}
$$

Only last digit:

$$
9
$$

Cycle:

$$
9,1
$$

Since:

$$
2026\bmod2=0
$$

take the 2nd element:

$$
\boxed1
$$

---

# 40. Cycle vs Direct Remainder

Do not automatically use cyclicity for every remainder question.

### Use direct reduction when:

$$
a\bmod m
$$

is already easy.

### Use cyclicity when:

$$
a^n\bmod m
$$

has a very large exponent.

> [!important] Recognition
>
> **Huge exponent → think cycle.**
>
> **Small exponent → direct calculation may be faster.**

---

# 41. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Forgetting to find the cycle length.
- ❌ Using `n mod cycle` incorrectly.
- ❌ When the result is `0`, taking the first element instead of the last.
- ❌ Using the cycle of the wrong base.
- ❌ Forgetting that only the last digit matters for unit-digit questions.
- ❌ Combining different bases incorrectly.
- ❌ Forgetting exponent rules for powers of powers.
- ❌ Assuming every modular sequence starts immediately with a pure cycle.
- ❌ Confusing cycle length with the divisor.
- ❌ Calculating enormous powers directly.

---

# 42. Exam Strategy

> [!tip] 10-Second Method

For:

$$
a^n\bmod10
$$

### Step 1

Take the last digit of `a`.

### Step 2

Look up its cycle.

### Step 3

Find cycle length.

### Step 4

Calculate:

$$
n\bmod\text{cycle length}
$$

### Step 5

If result is `0`, use the last cycle element.

### Step 6

Return the corresponding digit.

---

# 43. Master Formula

If cycle is:

$$
r_1,r_2,\ldots,r_k
$$

then:

$$
p=n\bmod k
$$

and:

$$
\boxed{
R=
\begin{cases}
r_p,&p\ne0\\
r_k,&p=0
\end{cases}
}
$$

---

# 44. Formula Sheet

> [!important] Must Remember

### Cycle Position

$$
\boxed{
p=n\bmod k
}
$$

### If `p = 0`

$$
\boxed{
\text{Use }r_k
}
$$

### Unit Digit

$$
\boxed{
a^n\bmod10
}
$$

depends only on the last digit of `a`.

### Unit-Digit Cycle Lengths

$$
\boxed{
0,1,5,6\rightarrow1
}
$$

$$
\boxed{
4,9\rightarrow2
}
$$

$$
\boxed{
2,3,7,8\rightarrow4
}
$$

---

# 45. High-Yield Patterns

> [!important] Must Master

### Pattern 1

Huge power:

$$
\boxed{
\text{Find cycle}
}
$$

### Pattern 2

Cycle length `k`:

$$
\boxed{
n\bmod k
}
$$

### Pattern 3

Remainder `0`:

$$
\boxed{
\text{Take last cycle element}
}
$$

### Pattern 4

Unit digit:

$$
\boxed{
\text{Only last digit of base matters}
}
$$

### Pattern 5

Bases `2,3,7,8`:

$$
\boxed{\text{Cycle length }4}
$$

### Pattern 6

Bases `4,9`:

$$
\boxed{\text{Cycle length }2}
$$

### Pattern 7

Bases `0,1,5,6`:

$$
\boxed{\text{Cycle length }1}
$$

### Pattern 8

Nested power:

$$
\boxed{
\text{Reduce inner exponent modulo outer cycle length}
}
$$

---

# 46. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

This is one of the most important patterns in Number System aptitude.

### Master These First

1. Unit-digit cycles
2. Cycle length
3. Exponent reduction
4. Remainder `0` position
5. Bases ending `2,3,7,8`
6. Bases ending `4,9`
7. Bases ending `0,1,5,6`
8. Huge exponents
9. Product of powers
10. Power of a power
11. Nested powers
12. General modular cycles

---

# 47. Practice Checklist

- [ ] Find cycles of `2`
- [ ] Find cycles of `3`
- [ ] Find cycles of `4`
- [ ] Find cycles of `7`
- [ ] Find cycles of `8`
- [ ] Find cycles of `9`
- [ ] Solve huge unit-digit powers
- [ ] Practice exponent remainder `0`
- [ ] Practice exponent remainder `1`
- [ ] Practice products of powers
- [ ] Practice powers of powers
- [ ] Practice nested powers
- [ ] Practice cycles modulo numbers other than `10`

---

# 48. Related Topics

- [[Remainders]]
- [[Basic Remainder]]
- [[Remainder Theorem]]
- [[Large Number Remainders]]
- [[Remainder Patterns]]
- [[Unit Digit]]
- [[Last Digit]]
- [[Last Two Digits]]
- [[Powers and Unit Digits]]
- [[Divisibility Rules]]

---

# 49. Quick Revision

> [!summary] One-Minute Revision

### Main Idea

$$
\boxed{
\text{Powers repeat remainders}
}
$$

### Method

$$
\boxed{
\text{Find cycle}
\rightarrow
\text{Find cycle length}
\rightarrow
n\bmod k
\rightarrow
\text{select position}
}
$$

### Unit Digit Cycles

$$
2\rightarrow2,4,8,6
$$

$$
3\rightarrow3,9,7,1
$$

$$
4\rightarrow4,6
$$

$$
7\rightarrow7,9,3,1
$$

$$
8\rightarrow8,4,2,6
$$

$$
9\rightarrow9,1
$$

### Cycle Lengths

$$
\boxed{
2,3,7,8\rightarrow4
}
$$

$$
\boxed{
4,9\rightarrow2
}
$$

$$
\boxed{
0,1,5,6\rightarrow1
}
$$

### Golden Rule

> **Exponent remainder = cycle position. If the exponent remainder is `0`, take the last element of the cycle.**

### One-Line Recognition

> **Huge power + fixed divisor → look for a repeating remainder cycle.**