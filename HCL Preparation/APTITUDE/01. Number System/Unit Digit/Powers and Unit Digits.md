---
type: concept
subject: aptitude
topic: "Powers and Unit Digits"
parent: "01. Number System/Unit Digit"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - unit-digit
  - powers
  - cyclicity
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Unit Digit]]"
  - "[[Last Digit]]"
  - "[[Last Two Digits]]"
  - "[[Cyclicity]]"
  - "[[Remainders]]"
---

# Powers and Unit Digits

## 1. Core Concept

> [!summary] Main Idea
> When a question asks for the **unit digit of a power**, only the **last digit of the base** matters.
>
> Then use the repeating cycle of that last digit.

For:

$$
a^n
$$

the unit digit is:

$$
\boxed{
a^n\bmod10
}
$$

Since:

$$
a\bmod10
$$

contains the only information needed, we can replace `a` by its last digit.

---

# 2. Golden Rule

$$
\boxed{
\text{Unit digit of }a^n
=
\text{Unit digit of }(a\bmod10)^n
}
$$

### Example

Find the unit digit of:

$$
1234567^{100}
$$

Only the last digit `7` matters:

$$
7^{100}
$$

Now use the cycle of `7`:

$$
7,9,3,1
$$

Since:

$$
100\bmod4=0
$$

take the 4th element:

$$
\boxed1
$$

---

# 3. Complete Unit-Digit Cycle Table

| Last digit of base | Power cycle | Cycle length |
|---:|---|---:|
| `0` | `0` | `1` |
| `1` | `1` | `1` |
| `2` | `2, 4, 8, 6` | `4` |
| `3` | `3, 9, 7, 1` | `4` |
| `4` | `4, 6` | `2` |
| `5` | `5` | `1` |
| `6` | `6` | `1` |
| `7` | `7, 9, 3, 1` | `4` |
| `8` | `8, 4, 2, 6` | `4` |
| `9` | `9, 1` | `2` |

> [!important] Must Memorize
>
> $$ 
> 2,3,7,8\rightarrow\text{cycle length }4
> $$
>
> $$
> 4,9\rightarrow\text{cycle length }2
> $$
>
> $$
> 0,1,5,6\rightarrow\text{cycle length }1
> $$

---

# 4. Bases Ending in `0`

Any positive power of a number ending in `0` ends in `0`.

$$
\boxed{
0^n\rightarrow0
}
$$

### Example

$$
450^{2026}
$$

Unit digit:

$$
\boxed0
$$

No cycle calculation is needed.

---

# 5. Bases Ending in `1`

Any positive power of a number ending in `1` ends in `1`.

$$
\boxed{
1^n\rightarrow1
}
$$

### Example

$$
781^{9999}
$$

Unit digit:

$$
\boxed1
$$

---

# 6. Bases Ending in `5`

Every positive power of a number ending in `5` ends in `5`.

$$
\boxed{
5^n\rightarrow5
}
$$

### Example

$$
12345^{2026}
$$

Unit digit:

$$
\boxed5
$$

---

# 7. Bases Ending in `6`

Every positive power of a number ending in `6` ends in `6`.

$$
\boxed{
6^n\rightarrow6
}
$$

### Example

$$
8765436^{100000}
$$

Unit digit:

$$
\boxed6
$$

---

# 8. Base Ending in `2`

Cycle:

$$
\boxed{2,4,8,6}
$$

Therefore:

$$
\boxed{
2^n\bmod10
}
$$

depends on:

$$
n\bmod4
$$

### Position Table

| `n mod 4` | Unit digit |
|---:|---:|
| `1` | `2` |
| `2` | `4` |
| `3` | `8` |
| `0` | `6` |

---

# 9. Example — `2^37`

Calculate:

$$
37\bmod4=1
$$

Therefore take position `1`:

$$
\boxed2
$$

---

# 10. Base Ending in `3`

Cycle:

$$
\boxed{3,9,7,1}
$$

Therefore:

$$
\boxed{
3^n\bmod10
}
$$

depends on:

$$
n\bmod4
$$

### Position Table

| `n mod 4` | Unit digit |
|---:|---:|
| `1` | `3` |
| `2` | `9` |
| `3` | `7` |
| `0` | `1` |

---

# 11. Example — `3^2025`

Calculate:

$$
2025\bmod4=1
$$

Therefore:

$$
\boxed3
$$

---

# 12. Base Ending in `4`

Cycle:

$$
\boxed{4,6}
$$

Therefore only the parity of the exponent matters.

### Odd exponent

$$
\boxed4
$$

### Even exponent

$$
\boxed6
$$

---

# 13. Example — `4^999`

Since `999` is odd:

$$
\boxed4
$$

---

# 14. Example — `4^1000`

Since `1000` is even:

$$
\boxed6
$$

---

# 15. Base Ending in `7`

Cycle:

$$
\boxed{7,9,3,1}
$$

### Position Table

| `n mod 4` | Unit digit |
|---:|---:|
| `1` | `7` |
| `2` | `9` |
| `3` | `3` |
| `0` | `1` |

---

# 16. Example — `7^2026`

Calculate:

$$
2026\bmod4=2
$$

Therefore:

$$
\boxed9
$$

---

# 17. Base Ending in `8`

Cycle:

$$
\boxed{8,4,2,6}
$$

### Position Table

| `n mod 4` | Unit digit |
|---:|---:|
| `1` | `8` |
| `2` | `4` |
| `3` | `2` |
| `0` | `6` |

---

# 18. Example — `8^123`

Calculate:

$$
123\bmod4=3
$$

Therefore:

$$
\boxed2
$$

---

# 19. Base Ending in `9`

Cycle:

$$
\boxed{9,1}
$$

### Odd exponent

$$
\boxed9
$$

### Even exponent

$$
\boxed1
$$

---

# 20. Example — `9^2026`

`2026` is even.

Therefore:

$$
\boxed1
$$

---

# 21. Master Unit-Digit Formula

For:

$$
a^n
$$

### Step 1

Find:

$$
d=a\bmod10
$$

where `d` is the last digit of the base.

### Step 2

Find the cycle of `d`.

### Step 3

Let the cycle length be `k`.

Calculate:

$$
\boxed{
p=n\bmod k
}
$$

### Step 4

If:

$$
p=0
$$

use the last element of the cycle.

Otherwise use the `p`th element.

---

# 22. Example — Complete Method

Find the unit digit of:

$$
987654321^{2026}
$$

### Step 1 — Last digit of base

$$
987654321\rightarrow1
$$

### Step 2 — Cycle

$$
1
$$

### Step 3

No calculation is required.

Therefore:

$$
\boxed1
$$

---

# 23. Example — Large Base

Find the unit digit of:

$$
987654327^{2026}
$$

### Step 1

Last digit:

$$
7
$$

### Step 2

Cycle:

$$
7,9,3,1
$$

### Step 3

Cycle length:

$$
4
$$

### Step 4

Calculate:

$$
2026\bmod4=2
$$

### Step 5

Take the 2nd element:

$$
\boxed9
$$

---

# 24. Product of Powers

For:

$$
a^m\times b^n
$$

find the unit digit of each power separately.

Then multiply the resulting digits and keep only the last digit.

### Example

Find the unit digit of:

$$
2^{20}\times7^{15}
$$

For `2`:

$$
20\bmod4=0
$$

Therefore:

$$
2^{20}\rightarrow6
$$

For `7`:

$$
15\bmod4=3
$$

Therefore:

$$
7^{15}\rightarrow3
$$

Multiply:

$$
6\times3=18
$$

Therefore:

$$
\boxed8
$$

---

# 25. Sum of Powers

For:

$$
a^m+b^n
$$

find the unit digit of each term.

### Example

Find the unit digit of:

$$
2^{20}+3^{15}
$$

For `2`:

$$
2^{20}\rightarrow6
$$

For `3`:

$$
15\bmod4=3
$$

Therefore:

$$
3^{15}\rightarrow7
$$

Then:

$$
6+7=13
$$

Unit digit:

$$
\boxed3
$$

---

# 26. Difference of Powers

For:

$$
a^m-b^n
$$

find the unit digits first.

### Example

Find the unit digit of:

$$
7^{10}-3^{15}
$$

For `7`:

$$
10\bmod4=2
$$

Therefore:

$$
7^{10}\rightarrow9
$$

For `3`:

$$
15\bmod4=3
$$

Therefore:

$$
3^{15}\rightarrow7
$$

Then:

$$
9-7=2
$$

Answer:

$$
\boxed2
$$

---

# 27. Product Contains `0`

If any factor in a product has unit digit `0`, the whole product has unit digit:

$$
\boxed0
$$

### Example

$$
2^{100}\times5^{20}\times7^{10}
$$

Since:

$$
5^{20}
$$

ends in `5`, and:

$$
2^{100}
$$

is even, the product contains a factor of `10`.

Therefore:

$$
\boxed0
$$

---

# 28. Even Factor × Factor Ending in `5`

This is a very important shortcut.

If one factor is even and another ends in `5`:

$$
\boxed{
\text{unit digit}=0
}
$$

### Example

$$
8^{20}\times5^{15}
$$

`8^20` is even and `5^15` ends in `5`.

Therefore:

$$
\boxed0
$$

---

# 29. Same Base — Combine Powers

If:

$$
a^m\times a^n
$$

then:

$$
\boxed{
a^{m+n}
}
$$

### Example

Find the unit digit of:

$$
3^{20}\times3^{15}
$$

Combine:

$$
3^{35}
$$

Now:

$$
35\bmod4=3
$$

Cycle of `3`:

$$
3,9,7,1
$$

Therefore:

$$
\boxed7
$$

---

# 30. Same Base — Division of Powers

If:

$$
\frac{a^m}{a^n}
$$

then:

$$
\boxed{
a^{m-n}
}
$$

provided the expression is defined.

### Example

$$
\frac{2^{20}}{2^{15}}
=
2^5
$$

Therefore the unit digit is:

$$
\boxed2
$$

> [!warning] Aptitude Caution
> Only simplify exponents after confirming that the original expression is mathematically valid.

---

# 31. Power of a Power

Use:

$$
\boxed{
(a^m)^n=a^{mn}
}
$$

### Example

Find the unit digit of:

$$
(3^2)^{100}
$$

Rewrite:

$$
3^{200}
$$

Now:

$$
200\bmod4=0
$$

Therefore:

$$
\boxed1
$$

---

# 32. Nested Powers

Consider:

$$
2^{3^{100}}
$$

Outer base:

$$
2
$$

Cycle length:

$$
4
$$

So we need:

$$
3^{100}\bmod4
$$

Since:

$$
3^2\equiv1\pmod4
$$

and `100` is even:

$$
3^{100}\equiv1\pmod4
$$

Therefore the outer cycle uses position `1`.

Answer:

$$
\boxed2
$$

---

# 33. Nested Power Recognition

For:

$$
a^{b^c}
$$

think:

$$
\boxed{
\text{Outer cycle first}
}
$$

Then:

$$
\boxed{
\text{Reduce the inner exponent using the outer cycle length}
}
$$

This is a common higher-level aptitude pattern.

---

# 34. Exponent Ends in Zero

If the cycle length is `4`, only the last two bits of the exponent in modular terms matter.

Practically:

$$
n\bmod4
$$

can be determined from the last two digits of `n`.

### Example

$$
2026\bmod4=2
$$

because:

$$
26\bmod4=2
$$

This can make calculations faster.

---

# 35. Exponent Modulo `2`

For bases ending in `4` or `9`, only odd/even matters.

You do not need the full exponent.

### Example

$$
9^{999999999}
$$

Exponent is odd.

Therefore:

$$
\boxed9
$$

---

# 36. Exponent Modulo `4`

For bases ending in:

$$
2,3,7,8
$$

only:

$$
n\bmod4
$$

matters.

### Fast method

Look only at the last two digits of `n`.

Examples:

$$
2026\bmod4=2
$$

$$
2024\bmod4=0
$$

$$
1237\bmod4=1
$$

---

# 37. Pattern — Exponent Ending in `1`

If:

$$
n\bmod4=1
$$

then take the first element of the cycle.

Examples:

### Base `2`

$$
\boxed2
$$

### Base `3`

$$
\boxed3
$$

### Base `7`

$$
\boxed7
$$

### Base `8`

$$
\boxed8
$$

---

# 38. Pattern — Exponent Ending in `2` Modulo 4

If:

$$
n\bmod4=2
$$

then:

### Base `2`

$$
\boxed4
$$

### Base `3`

$$
\boxed9
$$

### Base `7`

$$
\boxed9
$$

### Base `8`

$$
\boxed4
$$

---

# 39. Pattern — Exponent Ending in `3` Modulo 4

If:

$$
n\bmod4=3
$$

then:

### Base `2`

$$
\boxed8
$$

### Base `3`

$$
\boxed7
$$

### Base `7`

$$
\boxed3
$$

### Base `8`

$$
\boxed2
$$

---

# 40. Pattern — Exponent Divisible by 4

If:

$$
n\bmod4=0
$$

then:

### Base `2`

$$
\boxed6
$$

### Base `3`

$$
\boxed1
$$

### Base `7`

$$
\boxed1
$$

### Base `8`

$$
\boxed6
$$

---

# 41. Unit-Digit Shortcut Matrix

| Base | `n mod 4 = 1` | `n mod 4 = 2` | `n mod 4 = 3` | `n mod 4 = 0` |
|---:|---:|---:|---:|---:|
| `2` | `2` | `4` | `8` | `6` |
| `3` | `3` | `9` | `7` | `1` |
| `7` | `7` | `9` | `3` | `1` |
| `8` | `8` | `4` | `2` | `6` |

> [!important] Exam Table
> Memorizing this table can reduce many unit-digit questions to a **5-second calculation**.

---

# 42. Special Unit Digits

These need almost no calculation:

| Base ends in | Answer for positive powers |
|---:|---:|
| `0` | `0` |
| `1` | `1` |
| `5` | `5` |
| `6` | `6` |

Therefore:

$$
\boxed{
0,1,5,6
\rightarrow
\text{direct answer}
}
$$

---

# 43. Last Digit of Factorial

For:

$$
n!
$$

when:

$$
n\ge5
$$

the unit digit is:

$$
\boxed0
$$

Why?

Because factorial contains both:

$$
2
$$

and:

$$
5
$$

Therefore:

$$
2\times5=10
$$

---

# 44. Example — Factorial

Find the unit digit of:

$$
25!
$$

Since:

$$
25\ge5
$$

therefore:

$$
\boxed0
$$

---

# 45. Last Digit of a Square

The possible unit digits of a perfect square are:

$$
\boxed{
0,1,4,5,6,9
}
$$

Therefore a perfect square can never end in:

$$
\boxed{
2,3,7,8
}
$$

### Example

Can `12347` be a perfect square?

It ends in `7`.

Since squares cannot end in `7`:

$$
\boxed{\text{No}}
$$

---

# 46. Last Digit of a Cube

A perfect cube can end in any digit.

Useful mappings:

| Number's last digit | Cube's last digit |
|---:|---:|
| `0` | `0` |
| `1` | `1` |
| `2` | `8` |
| `3` | `7` |
| `4` | `4` |
| `5` | `5` |
| `6` | `6` |
| `7` | `3` |
| `8` | `2` |
| `9` | `9` |

---

# 47. Perfect Power Recognition

Unit digits can eliminate impossible answers.

### Square

Possible:

$$
\boxed{0,1,4,5,6,9}
$$

### Cube

Possible:

$$
\boxed{0,1,2,3,4,5,6,7,8,9}
$$

### Higher powers

The unit-digit cycle can often determine whether a proposed value is possible.

---

# 48. Negative Base

For:

$$
(-a)^n
$$

### Even exponent

$$
(-a)^n=a^n
$$

### Odd exponent

$$
(-a)^n=-a^n
$$

### Example

Find the unit digit of:

$$
(-7)^{101}
$$

Since `101` is odd:

$$
(-7)^{101}=-7^{101}
$$

Now:

$$
101\bmod4=1
$$

Therefore:

$$
7^{101}
$$

has unit digit `7`.

Thus:

$$
-7\equiv3\pmod{10}
$$

Answer:

$$
\boxed3
$$

---

# 49. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Calculating the entire power.
- ❌ Using every digit of the base.
- ❌ Forgetting that only the last digit matters.
- ❌ Assuming every cycle has length `4`.
- ❌ Forgetting the `0` position rule.
- ❌ Combining different bases incorrectly.
- ❌ Ignoring odd/even behavior for negative bases.
- ❌ Forgetting to simplify powers before using cyclicity.
- ❌ Confusing last digit with last two digits.
- ❌ Forgetting that `n!` ends in `0` for `n≥5`.

---

# 50. Exam Decision Tree

> [!tip] 5-Second Recognition

### Step 1

Does the question ask for **unit digit**?

If yes:

$$
\boxed{\bmod10}
$$

### Step 2

Is it a power?

If yes:

$$
\boxed{\text{Use cyclicity}}
$$

### Step 3

Look at the last digit of the base.

### Step 4

Choose:

$$
n\bmod4
$$

for:

$$
2,3,7,8
$$

or:

$$
n\bmod2
$$

for:

$$
4,9
$$

or answer directly for:

$$
0,1,5,6
$$

---

# 51. Formula Sheet

> [!important] Must Remember

### Unit Digit

$$
\boxed{
\text{Unit digit}=N\bmod10
}
$$

### Power

$$
\boxed{
a^n\bmod10
=
[(a\bmod10)^n]\bmod10
}
$$

### Cycle Position

$$
\boxed{
p=n\bmod k
}
$$

### Cycle Length `4`

$$
\boxed{
2,3,7,8\rightarrow4
}
$$

### Cycle Length `2`

$$
\boxed{
4,9\rightarrow2
}
$$

### Cycle Length `1`

$$
\boxed{
0,1,5,6\rightarrow1
}
$$

### Same Base

$$
\boxed{
a^m\times a^n=a^{m+n}
}
$$

### Power of Power

$$
\boxed{
(a^m)^n=a^{mn}
}
$$

---

# 52. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Ignore Most Digits

$$
\boxed{
a\rightarrow a\bmod10
}
$$

### Pattern 2 — Cycle Length `4`

$$
\boxed{
2,3,7,8
}
$$

### Pattern 3 — Cycle Length `2`

$$
\boxed{
4,9
}
$$

### Pattern 4 — Fixed Digit

$$
\boxed{
0,1,5,6
}
$$

### Pattern 5 — Exponent Reduction

$$
\boxed{
n\bmod k
}
$$

### Pattern 6 — Remainder `0`

$$
\boxed{
n\bmod k=0
\rightarrow
\text{last cycle element}
}
$$

### Pattern 7 — Same Base

$$
\boxed{
a^m a^n=a^{m+n}
}
$$

### Pattern 8 — Power of Power

$$
\boxed{
(a^m)^n=a^{mn}
}
$$

### Pattern 9 — Nested Power

$$
\boxed{
\text{Reduce inner exponent modulo outer cycle length}
}
$$

### Pattern 10 — Factorial

$$
\boxed{
n!\rightarrow0,\quad n\ge5
}
$$

---

# 53. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

This is a **must-master aptitude pattern** because many questions can be solved in seconds once the cycles are memorized.

### Master These First

1. Unit digit = modulo `10`
2. Base last-digit reduction
3. Complete cycle table
4. `n mod 4`
5. `n mod 2`
6. Remainder `0`
7. Products of powers
8. Sums of powers
9. Same-base exponent rules
10. Nested powers
11. Negative bases
12. Factorial unit digit
13. Square unit-digit patterns

---

# 54. Practice Checklist

- [ ] Powers ending in `0`
- [ ] Powers ending in `1`
- [ ] Powers ending in `2`
- [ ] Powers ending in `3`
- [ ] Powers ending in `4`
- [ ] Powers ending in `5`
- [ ] Powers ending in `6`
- [ ] Powers ending in `7`
- [ ] Powers ending in `8`
- [ ] Powers ending in `9`
- [ ] Huge exponents
- [ ] Product of powers
- [ ] Sum of powers
- [ ] Difference of powers
- [ ] Same-base powers
- [ ] Power of a power
- [ ] Nested powers
- [ ] Negative bases
- [ ] Factorial
- [ ] Perfect-square checks

---

# 55. Related Topics

- [[Unit Digit]]
- [[Last Digit]]
- [[Last Two Digits]]
- [[Cyclicity]]
- [[Cyclic Remainders]]
- [[Remainder Patterns]]
- [[Large Number Remainders]]
- [[Remainders]]
- [[Factors]]
- [[Factorization]]

---

# 56. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
\text{Unit digit}=N\bmod10
}
$$

### For Powers

$$
\boxed{
\text{Only the last digit of the base matters}
}
$$

### Cycles

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

### Golden Formula

$$
\boxed{
p=n\bmod k
}
$$

If:

$$
p=0
$$

take the last element of the cycle.

### Golden Memory Trick

> **Unit digit → keep the last digit of the base → find its cycle → reduce the exponent.**

### One-Line Recognition

> **Huge power asking for the last digit = cyclicity + exponent reduction.**