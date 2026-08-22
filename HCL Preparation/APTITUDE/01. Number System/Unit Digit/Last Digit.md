---
type: concept
subject: aptitude
topic: "Last Digit"
parent: "01. Number System/Unit Digit"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - unit-digit
  - last-digit
  - powers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Unit Digit]]"
  - "[[Remainders]]"
  - "[[Cyclic Remainders]]"
  - "[[Powers and Unit Digits]]"
---

# Last Digit

## 1. Core Concept

> [!summary] Definition
> The **last digit** of a number is the digit in its units place.

For example:

$$
45873
$$

The last digit is:

$$
\boxed3}
$$

Mathematically:

$$
\boxed{
\text{Last digit of }N=N\bmod10
}
$$

---

# 2. Fundamental Formula

The last digit of `N` is:

$$
\boxed{
N\bmod10
}
$$

### Examples

$$
123\bmod10=3
$$

$$
786\bmod10=6
$$

$$
450\bmod10=0
$$

Therefore:

> **To find the last digit, only the remainder after division by `10` matters.**

---

# 3. Only the Last Digit Matters

Suppose we need the last digit of:

$$
123456789
$$

We do not need the complete number.

Simply look at:

$$
\boxed9
$$

Therefore:

$$
123456789\bmod10=9
$$

---

# 4. Last Digit of a Sum

For:

$$
A+B
$$

only the last digits of `A` and `B` are needed.

$$
\boxed{
(A+B)\bmod10
=
[(A\bmod10)+(B\bmod10)]\bmod10
}
$$

### Example

Find the last digit of:

$$
347+582
$$

Last digits:

$$
7+2=9
$$

Therefore:

$$
\boxed9
$$

---

# 5. Last Digit of a Product

For:

$$
A\times B
$$

use only the last digits.

$$
\boxed{
AB\bmod10
=
[(A\bmod10)(B\bmod10)]\bmod10
}
$$

### Example

Find the last digit of:

$$
1234\times5678
$$

Only:

$$
4\times8=32
$$

Therefore:

$$
32\bmod10=2
$$

Answer:

$$
\boxed2
$$

---

# 6. Last Digit of Multiple Factors

For:

$$
A\times B\times C
$$

take the last digit of each factor.

### Example

Find the last digit of:

$$
123\times456\times789
$$

Last digits:

$$
3,\ 6,\ 9
$$

Calculate:

$$
3\times6\times9=162
$$

Therefore:

$$
\boxed2
$$

---

# 7. Zero Shortcut

If any factor ends in `0`, the entire product ends in `0`.

### Example

$$
123\times450\times789
$$

Since `450` ends in `0`:

$$
\boxed{\text{Last digit}=0}
$$

---

# 8. Even Number × Multiple of 5

If a product contains:

- an even number
- a number ending in `5`

then the product ends in `0`.

### Example

$$
24\times35
$$

Since:

$$
24\times35=840
$$

the last digit is:

$$
\boxed0
$$

> [!tip] Shortcut
> `2 × 5 = 10`, so an even factor combined with a factor ending in `5` gives last digit `0`.

---

# 9. Last Digit of a Power

For:

$$
a^n
$$

only the last digit of `a` matters.

Therefore:

$$
\boxed{
a^n\bmod10
=
(a\bmod10)^n\bmod10
}
$$

### Example

Find the last digit of:

$$
123^5
$$

Only the last digit `3` matters:

$$
3^5
$$

The powers of `3` cycle:

$$
3,9,7,1
$$

Since:

$$
5\bmod4=1
$$

the answer is:

$$
\boxed3
$$

---

# 10. Unit-Digit Cycles

For powers, the last digit often repeats.

### Base `2`

$$
2,4,8,6,\boxed{2,4,8,6,\ldots}
$$

Cycle length:

$$
\boxed4
$$

### Base `3`

$$
3,9,7,1
$$

Cycle length:

$$
\boxed4
$$

### Base `4`

$$
4,6
$$

Cycle length:

$$
\boxed2
$$

### Base `7`

$$
7,9,3,1
$$

Cycle length:

$$
\boxed4
$$

### Base `8`

$$
8,4,2,6
$$

Cycle length:

$$
\boxed4
$$

### Base `9`

$$
9,1
$$

Cycle length:

$$
\boxed2
$$

---

# 11. Complete Last-Digit Cycle Table

| Last digit of base | Cycle | Cycle length |
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
> For last-digit questions, cycle lengths are only:
>
> $$\boxed{1,\ 2,\ 4}
> $$

---

# 12. Bases With Fixed Last Digit

The following bases always produce the same last digit for positive powers:

### Base ending in `0`

$$
0^n\rightarrow0
$$

### Base ending in `1`

$$
1^n\rightarrow1
$$

### Base ending in `5`

$$
5^n\rightarrow5
$$

### Base ending in `6`

$$
6^n\rightarrow6
$$

Therefore:

$$
\boxed{
0,1,5,6
}
$$

need no cycle calculation.

---

# 13. Example — Base Ending in 6

Find the last digit of:

$$
4567896^{2026}
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

---

# 14. Example — Base Ending in 5

Find the last digit of:

$$
9876545^{999999}
$$

Only the last digit:

$$
5
$$

Therefore:

$$
\boxed5
$$

---

# 15. Cycle Position Formula

Suppose the cycle length is:

$$
k
$$

Then:

$$
\boxed{
p=n\bmod k
}
$$

If:

$$
p\ne0
$$

take the `p`th element.

If:

$$
p=0
$$

take the `k`th element.

---

# 16. Example — Last Digit of `2^100`

Cycle:

$$
2,4,8,6
$$

Cycle length:

$$
4
$$

Calculate:

$$
100\bmod4=0
$$

Therefore use the 4th element:

$$
\boxed6
$$

---

# 17. Example — Last Digit of `7^2026`

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

---

# 18. Example — Last Digit of `4^123`

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

Take the 1st element:

$$
\boxed4
$$

---

# 19. Example — Exponent Remainder Zero

Find the last digit of:

$$
3^{100}
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
100\bmod4=0
$$

Take the 4th element:

$$
\boxed1
$$

> [!warning] Common Trap
> If exponent modulo cycle length is `0`, **do not take the first element**.
>
> Take the **last element of the cycle**.

---

# 20. Last Digit of a Sum of Powers

Suppose:

$$
2^{100}+3^{100}
$$

Find the last digit.

### First term

Cycle of `2`:

$$
2,4,8,6
$$

Since:

$$
100\bmod4=0
$$

last digit:

$$
6
$$

### Second term

Cycle of `3`:

$$
3,9,7,1
$$

Again:

$$
100\bmod4=0
$$

last digit:

$$
1
$$

Now:

$$
6+1=7
$$

Therefore:

$$
\boxed7
$$

---

# 21. Last Digit of a Product of Powers

Find the last digit of:

$$
2^{20}\times3^{15}
$$

### For `2`

$$
20\bmod4=0
$$

Last digit:

$$
6
$$

### For `3`

$$
15\bmod4=3
$$

Last digit:

$$
7
$$

Now:

$$
6\times7=42
$$

Therefore:

$$
\boxed2
$$

---

# 22. Simplify Exponents First

Use:

$$
a^m\times a^n=a^{m+n}
$$

and:

$$
\boxed{
(a^m)^n=a^{mn}
}
$$

before applying cyclicity.

### Example

Find the last digit of:

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

2nd element of:

$$
2,4,8,6
$$

is:

$$
\boxed4
$$

---

# 23. Different Bases Cannot Be Combined

For:

$$
2^{20}\times3^{30}
$$

do **not** write:

$$
6^{50}
$$

That is incorrect.

Instead calculate the last digit of each term separately.

> [!warning] Rule
> You can combine exponents only when the **base is the same**.

---

# 24. Nested Powers

Consider:

$$
2^{3^{100}}
$$

The outer base is `2`.

Its cycle length is:

$$
4
$$

Therefore we need:

$$
3^{100}\bmod4
$$

Since:

$$
3^2\equiv1\pmod4
$$

and `100` is even:

$$
3^{100}\bmod4=1
$$

Therefore the outer power uses position `1`.

Answer:

$$
\boxed2
$$

---

# 25. Last Digit of a Number Ending in 2

For any number ending in `2`, its powers follow:

$$
\boxed{2,4,8,6}
$$

### Position Mapping

| Exponent position | Last digit |
|---:|---:|
| `1` | `2` |
| `2` | `4` |
| `3` | `8` |
| `0` | `6` |

Here `0` means exponent is divisible by `4`.

---

# 26. Last Digit of a Number Ending in 3

Cycle:

$$
\boxed{3,9,7,1}
$$

Mapping:

| Exponent mod `4` | Last digit |
|---:|---:|
| `1` | `3` |
| `2` | `9` |
| `3` | `7` |
| `0` | `1` |

---

# 27. Last Digit of a Number Ending in 7

Cycle:

$$
\boxed{7,9,3,1}
$$

Mapping:

| Exponent mod `4` | Last digit |
|---:|---:|
| `1` | `7` |
| `2` | `9` |
| `3` | `3` |
| `0` | `1` |

---

# 28. Last Digit of a Number Ending in 8

Cycle:

$$
\boxed{8,4,2,6}
$$

Mapping:

| Exponent mod `4` | Last digit |
|---:|---:|
| `1` | `8` |
| `2` | `4` |
| `3` | `2` |
| `0` | `6` |

---

# 29. Last Digit of a Number Ending in 4

Cycle:

$$
\boxed{4,6}
$$

Mapping:

| Exponent mod `2` | Last digit |
|---:|---:|
| `1` | `4` |
| `0` | `6` |

---

# 30. Last Digit of a Number Ending in 9

Cycle:

$$
\boxed{9,1}
$$

Mapping:

| Exponent mod `2` | Last digit |
|---:|---:|
| `1` | `9` |
| `0` | `1` |

---

# 31. Shortcut — Even/Odd Exponents

For bases ending in `4` or `9`:

### Base `4`

Odd exponent:

$$
\boxed4
$$

Even exponent:

$$
\boxed6
$$

### Base `9`

Odd exponent:

$$
\boxed9
$$

Even exponent:

$$
\boxed1
$$

---

# 32. Shortcut — Last Digit of `2^n`

For:

$$
2^n
$$

only:

$$
n\bmod4
$$

matters.

$$
\boxed{
2^n\bmod10=
\begin{cases}
2,&n\bmod4=1\\
4,&n\bmod4=2\\
8,&n\bmod4=3\\
6,&n\bmod4=0
\end{cases}
}
$$

---

# 33. Shortcut — Last Digit of `3^n`

$$
\boxed{
3^n\bmod10=
\begin{cases}
3,&n\bmod4=1\\
9,&n\bmod4=2\\
7,&n\bmod4=3\\
1,&n\bmod4=0
\end{cases}
}
$$

---

# 34. Shortcut — Last Digit of `7^n`

$$
\boxed{
7^n\bmod10=
\begin{cases}
7,&n\bmod4=1\\
9,&n\bmod4=2\\
3,&n\bmod4=3\\
1,&n\bmod4=0
\end{cases}
}
$$

---

# 35. Shortcut — Last Digit of `8^n`

$$
\boxed{
8^n\bmod10=
\begin{cases}
8,&n\bmod4=1\\
4,&n\bmod4=2\\
2,&n\bmod4=3\\
6,&n\bmod4=0
\end{cases}
}
$$

---

# 36. Negative Bases

For a negative number, the sign of the final answer matters before taking the standard remainder.

For example:

$$
(-2)^n
$$

### Even `n`

$$
(-2)^n=2^n
$$

### Odd `n`

$$
(-2)^n=-2^n
$$

Therefore parity matters.

> [!tip] Exam Tip
> For negative bases, first determine whether the exponent is **even or odd**, then calculate the last digit.

---

# 37. Example — Negative Base

Find the last digit of:

$$
(-3)^{101}
$$

Since `101` is odd:

$$
(-3)^{101}
=
-3^{101}
$$

Last digit of:

$$
3^{101}
$$

Since:

$$
101\bmod4=1
$$

it is:

$$
3
$$

Therefore the number is negative and ends in:

$$
\boxed7
$$

because:

$$
-3\equiv7\pmod{10}
$$

---

# 38. Last Digit of Factorials

For:

$$
n!
$$

when `n≥5`, the last digit is always:

$$
\boxed0
$$

because `n!` contains:

$$
2\times5=10
$$

### Example

$$
10!
$$

ends in:

$$
\boxed0
$$

This is an important shortcut.

---

# 39. Last Digit of a Product — Factor Pair

If a product contains:

$$
2\times5
$$

then it contains a factor of `10`.

Therefore:

$$
\boxed{\text{last digit}=0}
$$

### Example

$$
18\times25\times37
$$

Since:

$$
18\times25
$$

contains:

$$
2\times5
$$

the product ends in:

$$
\boxed0
$$

---

# 40. Last Digit of a Square

The last digit of a perfect square can only be:

$$
\boxed{
0,1,4,5,6,9
}
$$

It can never be:

$$
\boxed{
2,3,7,8
}
$$

### Square Last-Digit Table

| Last digit of number | Last digit of square |
|---:|---:|
| `0` | `0` |
| `1` | `1` |
| `2` | `4` |
| `3` | `9` |
| `4` | `6` |
| `5` | `5` |
| `6` | `6` |
| `7` | `9` |
| `8` | `4` |
| `9` | `1` |

---

# 41. Last Digit of a Cube

Cubes can end in any digit `0–9`.

The mapping is:

| Last digit | Cube last digit |
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

This is useful for checking whether a number can be a perfect cube.

---

# 42. Last Digit Pattern for Even Powers

For many bases, even powers have restricted last digits.

For example:

$$
2^{2k}
$$

will have last digit either:

$$
4\text{ or }6
$$

depending on the exponent modulo `4`.

---

# 43. Last Digit Pattern for Odd Powers

Similarly, odd powers of certain bases follow their corresponding odd positions in the cycle.

For example:

$$
7^n
$$

with odd `n` alternates:

$$
7,3,7,3,\ldots
$$

depending on:

$$
n\bmod4
$$

---

# 44. Exam Strategy

> [!tip] 5-Step Method

For:

$$
a^n
$$

### Step 1

Take only the last digit of `a`.

### Step 2

Identify its cycle.

### Step 3

Find cycle length.

### Step 4

Calculate:

$$
n\bmod\text{cycle length}
$$

### Step 5

Select the corresponding last digit.

---

# 45. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Calculating the full power.
- ❌ Using the entire base instead of its last digit.
- ❌ Forgetting cycle length.
- ❌ Treating exponent remainder `0` as position `1`.
- ❌ Combining powers with different bases incorrectly.
- ❌ Ignoring negative-base parity.
- ❌ Forgetting that factorials from `5!` onward end in `0`.
- ❌ Assuming every square can end in any digit.
- ❌ Confusing last digit with last two digits.
- ❌ Forgetting to reduce the final product to its last digit.

---

# 46. Formula Sheet

> [!important] Must Remember

### Last Digit

$$
\boxed{
\text{Last digit}=N\bmod10
}
$$

### Sum

$$
\boxed{
(A+B)\bmod10
=
[(A\bmod10)+(B\bmod10)]\bmod10
}
$$

### Product

$$
\boxed{
AB\bmod10
=
[(A\bmod10)(B\bmod10)]\bmod10
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

### If `p = 0`

$$
\boxed{
\text{Use the }k^{th}\text{ cycle element}
}
$$

### Factorial

For:

$$
n\ge5
$$

$$
\boxed{
n!\text{ ends in }0
}
$$

---

# 47. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Last Digit

$$
\boxed{
N\bmod10
}
$$

### Pattern 2 — Ignore All Other Digits

For powers:

$$
\boxed{
\text{Only last digit of base matters}
}
$$

### Pattern 3 — Cycle Length

$$
2,3,7,8\rightarrow4
$$

$$
4,9\rightarrow2
$$

$$
0,1,5,6\rightarrow1
$$

### Pattern 4 — Exponent Reduction

$$
\boxed{
n\bmod\text{cycle length}
}
$$

### Pattern 5 — Remainder Zero

$$
\boxed{
n\bmod k=0
\rightarrow
\text{take last cycle element}
}
$$

### Pattern 6 — Product Ending in Zero

$$
\boxed{
2\times5\rightarrow0
}
$$

### Pattern 7 — Factorial

$$
\boxed{
n!\ (n\ge5)\rightarrow0
}
$$

### Pattern 8 — Perfect Square

$$
\boxed{
0,1,4,5,6,9
}
$$

only possible last digits.

---

# 48. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Last-digit questions are usually **fast-scoring pattern questions**.

### Master These First

1. Last digit = modulo `10`
2. Last digit of products
3. Last digit of powers
4. Unit-digit cycles
5. Cycle position
6. Exponent remainder `0`
7. Fixed bases `0,1,5,6`
8. Bases `2,3,7,8`
9. Bases `4,9`
10. Factorial last digit
11. Square last-digit patterns
12. Nested powers

---

# 49. Practice Checklist

- [ ] Last digit of numbers
- [ ] Last digit of sums
- [ ] Last digit of products
- [ ] Last digit of powers
- [ ] Powers ending in `2`
- [ ] Powers ending in `3`
- [ ] Powers ending in `4`
- [ ] Powers ending in `7`
- [ ] Powers ending in `8`
- [ ] Powers ending in `9`
- [ ] Huge exponents
- [ ] Nested powers
- [ ] Negative bases
- [ ] Factorials
- [ ] Perfect-square last digits
- [ ] Mixed power expressions

---

# 50. Related Topics

- [[Unit Digit]]
- [[Last Two Digits]]
- [[Cyclicity]]
- [[Powers and Unit Digits]]
- [[Remainders]]
- [[Cyclic Remainders]]
- [[Large Number Remainders]]
- [[Factors]]
- [[Factorization]]

---

# 51. Quick Revision

> [!summary] One-Minute Revision

### Last Digit

$$
\boxed{
N\bmod10
}
$$

### For Powers

$$
\boxed{
\text{Only the last digit of the base matters}
}
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

### Position

$$
\boxed{
n\bmod k
}
$$

If the result is `0`:

$$
\boxed{\text{take the last cycle element}}
$$

### Product Shortcut

$$
\boxed{
2\times5\rightarrow\text{last digit }0
}
$$

### Factorial

$$
\boxed{
n!\ (n\ge5)\rightarrow\text{last digit }0
}
$$

### Square

$$
\boxed{
\text{Square last digit}\in\{0,1,4,5,6,9\}
}
$$

### Golden Memory Trick

> **Last digit → think modulo `10`. Huge power → think cycle.**

### One-Line Recognition

> **Question asks for the last digit → ignore everything except the units digit and its power cycle.**