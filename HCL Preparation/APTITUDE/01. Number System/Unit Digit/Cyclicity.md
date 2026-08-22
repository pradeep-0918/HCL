---
type: concept
subject: aptitude
topic: "Cyclicity"
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
  - cyclicity
  - powers
  - modular-arithmetic
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Unit Digit]]"
  - "[[Last Digit]]"
  - "[[Last Two Digits]]"
  - "[[Powers and Unit Digits]]"
  - "[[Cyclic Remainders]]"
  - "[[Remainders]]"
---

# Cyclicity

## 1. Core Concept

> [!summary] Definition
> **Cyclicity** is the repeating pattern formed by the last digits of successive powers of a number.

For example:

$$
2^1=2
$$

$$
2^2=4
$$

$$
2^3=8
$$

$$
2^4=16
$$

$$
2^5=32
$$

The last digits are:

$$
\boxed{2,4,8,6,2,4,8,6,\ldots}
$$

The pattern repeats every `4` powers.

Therefore:

$$
\boxed{\text{Cyclicity of }2=4}
$$

---

# 2. Why Cyclicity Matters

A question may ask:

$$
2^{2026}
$$

Finding the complete value is impossible.

But the last digit follows a cycle:

$$
2,4,8,6
$$

So we only need:

$$
2026\bmod4
$$

Therefore:

$$
2026\bmod4=2
$$

Take the second element:

$$
\boxed4
$$

> [!tip] Exam Principle
> **Huge exponent → find the cycle → reduce the exponent → select the position.**

---

# 3. Basic Cyclicity Method

For:

$$
a^n
$$

when the question asks for the last digit:

### Step 1

Take only the last digit of `a`.

### Step 2

Write the powers until the last digits repeat.

### Step 3

Find the cycle length.

### Step 4

Calculate:

$$
n\bmod\text{cycle length}
$$

### Step 5

Use that remainder as the position.

### Step 6

If the remainder is `0`, use the final element of the cycle.

---

# 4. Complete Cyclicity Table

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

> [!important] Memorize
>
> $$ 
> 2,3,7,8\rightarrow4
> $$
>
> $$
> 4,9\rightarrow2
> $$
>
> $$
> 0,1,5,6\rightarrow1
> $$

---

# 5. Cycle of `2`

Powers:

$$
2^1=2
$$

$$
2^2=4
$$

$$
2^3=8
$$

$$
2^4=16
$$

Last digits:

$$
\boxed{2,4,8,6}
$$

Therefore:

$$
\boxed{\text{Cycle length}=4}
$$

---

# 6. Cycle of `3`

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

Therefore:

$$
\boxed{3,9,7,1}
$$

Cycle length:

$$
\boxed4
$$

---

# 7. Cycle of `4`

$$
4^1\rightarrow4
$$

$$
4^2\rightarrow6
$$

$$
4^3\rightarrow4
$$

Therefore:

$$
\boxed{4,6}
$$

Cycle length:

$$
\boxed2
$$

---

# 8. Cycle of `7`

$$
7^1\rightarrow7
$$

$$
7^2\rightarrow9
$$

$$
7^3\rightarrow3
$$

$$
7^4\rightarrow1
$$

Therefore:

$$
\boxed{7,9,3,1}
$$

Cycle length:

$$
\boxed4
$$

---

# 9. Cycle of `8`

$$
8^1\rightarrow8
$$

$$
8^2\rightarrow4
$$

$$
8^3\rightarrow2
$$

$$
8^4\rightarrow6
$$

Therefore:

$$
\boxed{8,4,2,6}
$$

Cycle length:

$$
\boxed4
$$

---

# 10. Cycle of `9`

$$
9^1\rightarrow9
$$

$$
9^2\rightarrow1
$$

Therefore:

$$
\boxed{9,1}
$$

Cycle length:

$$
\boxed2
$$

---

# 11. Fixed Cycles

The following numbers do not change their last digit when raised to positive powers.

### `0`

$$
0^n\rightarrow0
$$

### `1`

$$
1^n\rightarrow1
$$

### `5`

$$
5^n\rightarrow5
$$

### `6`

$$
6^n\rightarrow6
$$

Therefore:

$$
\boxed{
0,1,5,6\rightarrow\text{cycle length }1
}
$$

---

# 12. Cycle Position Formula

Let:

$$
k=\text{cycle length}
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

# 13. Example — `2^100`

Cycle:

$$
2,4,8,6
$$

Length:

$$
4
$$

Calculate:

$$
100\bmod4=0
$$

Since the remainder is `0`, use the 4th element:

$$
\boxed6
$$

---

# 14. Example — `3^101`

Cycle:

$$
3,9,7,1
$$

Calculate:

$$
101\bmod4=1
$$

Take position `1`:

$$
\boxed3
$$

---

# 15. Example — `7^2026`

Cycle:

$$
7,9,3,1
$$

Calculate:

$$
2026\bmod4=2
$$

Take position `2`:

$$
\boxed9
$$

---

# 16. Example — `4^123`

Cycle:

$$
4,6
$$

Calculate:

$$
123\bmod2=1
$$

Take position `1`:

$$
\boxed4
$$

---

# 17. Example — `9^2026`

Cycle:

$$
9,1
$$

Calculate:

$$
2026\bmod2=0
$$

Take the 2nd element:

$$
\boxed1
$$

---

# 18. The `0` Position Rule

This is one of the most important cyclicity rules.

Suppose:

$$
\text{Cycle}=a,b,c,d
$$

and:

$$
n\bmod4=0
$$

The answer is:

$$
\boxed d
$$

not `a`.

### Example

For:

$$
2^{20}
$$

we have:

$$
20\bmod4=0
$$

Cycle:

$$
2,4,8,6
$$

Answer:

$$
\boxed6
$$

---

# 19. Shortcut for Cycle Length `4`

For bases ending in:

$$
2,3,7,8
$$

calculate:

$$
\boxed{n\bmod4}
$$

Then:

| `n mod 4` | Position |
|---:|---:|
| `1` | 1st |
| `2` | 2nd |
| `3` | 3rd |
| `0` | 4th |

This single table handles most unit-digit questions.

---

# 20. Shortcut for Cycle Length `2`

For bases ending in:

$$
4,9
$$

calculate:

$$
\boxed{n\bmod2}
$$

Then:

| `n mod 2` | Position |
|---:|---:|
| `1` | 1st |
| `0` | 2nd |

Therefore:

### `4`

Odd:

$$
\boxed4
$$

Even:

$$
\boxed6
$$

### `9`

Odd:

$$
\boxed9
$$

Even:

$$
\boxed1
$$

---

# 21. Shortcut for Cycle Length `1`

For:

$$
0,1,5,6
$$

the exponent does not matter as long as:

$$
n>0
$$

Therefore:

$$
\boxed{
0\rightarrow0
}
$$

$$
\boxed{
1\rightarrow1
}
$$

$$
\boxed{
5\rightarrow5
}
$$

$$
\boxed{
6\rightarrow6
}
$$

---

# 22. Large Base

For:

$$
1234567^{2026}
$$

only the last digit of the base matters.

Therefore:

$$
1234567\rightarrow7
$$

Now solve:

$$
7^{2026}
$$

Cycle:

$$
7,9,3,1
$$

Since:

$$
2026\bmod4=2
$$

answer:

$$
\boxed9
$$

> [!important] Golden Rule
> **For unit-digit cyclicity, ignore every digit except the last digit of the base.**

---

# 23. Large Exponent

The exponent can be extremely large.

For example:

$$
8^{987654321}
$$

Cycle length:

$$
4
$$

Only calculate:

$$
987654321\bmod4
$$

Since:

$$
987654321\bmod4=1
$$

take the first element of:

$$
8,4,2,6
$$

Answer:

$$
\boxed8
$$

---

# 24. Nested Powers

Consider:

$$
2^{3^{100}}
$$

The cycle of `2` has length:

$$
4
$$

Therefore we need:

$$
3^{100}\bmod4
$$

Now:

$$
3^2\equiv1\pmod4
$$

Since `100` is even:

$$
3^{100}\equiv1\pmod4
$$

Therefore the outer cycle uses position `1`.

Answer:

$$
\boxed2
$$

---

# 25. Nested Power Strategy

For:

$$
a^{b^c}
$$

### Step 1

Find the cycle length of `a`.

### Step 2

Calculate:

$$
b^c\bmod(\text{outer cycle length})
$$

### Step 3

Use the result as the outer cycle position.

Therefore:

$$
\boxed{
\text{Outer cycle first → Inner exponent second}
}
$$

---

# 26. Product of Powers

For:

$$
2^{20}\times3^{15}
$$

solve each base separately.

### `2`

$$
20\bmod4=0
$$

Therefore:

$$
2^{20}\rightarrow6
$$

### `3`

$$
15\bmod4=3
$$

Therefore:

$$
3^{15}\rightarrow7
$$

Multiply:

$$
6\times7=42
$$

Last digit:

$$
\boxed2
$$

---

# 27. Same Base — Combine First

If the bases are the same:

$$
a^m\times a^n
$$

then:

$$
\boxed{
a^m\times a^n=a^{m+n}
}
$$

### Example

$$
2^{20}\times2^{30}
$$

becomes:

$$
2^{50}
$$

Now:

$$
50\bmod4=2
$$

Therefore:

$$
\boxed4
$$

---

# 28. Power of a Power

Use:

$$
\boxed{
(a^m)^n=a^{mn}
}
$$

### Example

Find the last digit of:

$$
(7^2)^{100}
$$

Rewrite:

$$
7^{200}
$$

Now:

$$
200\bmod4=0
$$

Cycle:

$$
7,9,3,1
$$

Take 4th element:

$$
\boxed1
$$

---

# 29. Different Bases Cannot Be Combined

For:

$$
2^{10}\times3^{10}
$$

do not write:

$$
6^{20}
$$

Instead:

$$
2^{10}\rightarrow4
$$

and:

$$
3^{10}\rightarrow9
$$

Then:

$$
4\times9=36
$$

Last digit:

$$
\boxed6
$$

---

# 30. Cycle of a Product

Sometimes the product itself can have a cycle.

For example:

$$
6^n
$$

always ends in:

$$
6
$$

So instead of finding separate cycles, recognize the product's last digit if it becomes obvious.

> [!tip] Strategy
> Always look for the **simplest representation** before calculating cycles.

---

# 31. Negative Base

For:

$$
(-a)^n
$$

the parity of `n` matters.

### Even exponent

$$
(-a)^n=a^n
$$

### Odd exponent

$$
(-a)^n=-a^n
$$

### Example

Find the last digit of:

$$
(-7)^{101}
$$

Since `101` is odd:

$$
(-7)^{101}=-7^{101}
$$

For:

$$
7^{101}
$$

we have:

$$
101\bmod4=1
$$

so its last digit is `7`.

Therefore:

$$
-7\equiv3\pmod{10}
$$

Answer:

$$
\boxed3
$$

---

# 32. Cyclicity and Remainders

Cyclicity is simply a special application of modular arithmetic.

For unit digits:

$$
\boxed{
a^n\bmod10
}
$$

The repeated remainders form the cycle.

Therefore:

$$
\boxed{
\text{Cyclicity = repeating modular pattern}
}
$$

---

# 33. Cyclicity vs Remainder Pattern

### Cyclicity

Focuses mainly on:

$$
a^n
$$

and repeated powers.

### Remainder Patterns

Broader concept involving:

- sums
- products
- powers
- divisibility
- common remainders
- algebraic simplification

Therefore:

$$
\boxed{
\text{Cyclicity is one important remainder pattern}
}
$$

---

# 34. Important Pattern — Cycle Length Is Not Always the Same

Do not memorize that every number has cycle length `4`.

For unit digits:

$$
2,3,7,8\rightarrow4
$$

but:

$$
4,9\rightarrow2
$$

and:

$$
0,1,5,6\rightarrow1
$$

Therefore:

> [!warning]
> **First identify the base's last digit. Then identify its cycle length.**

---

# 35. Important Pattern — Exponent `1`

For every base:

$$
a^1=a
$$

Therefore the first cycle position is always the last digit of the base.

---

# 36. Important Pattern — Exponent `0`

For non-zero base:

$$
a^0=1
$$

Therefore:

$$
\boxed{
a^0=1,\quad a\ne0
}
$$

> [!warning] Special Case
> `0^0` is not treated as an ordinary positive-power aptitude case. Do not apply the normal power rule blindly.

---

# 37. Important Pattern — Exponents Differ by Cycle Length

If the cycle length is `4`, then:

$$
a^n
$$

and:

$$
a^{n+4}
$$

have the same last digit.

Similarly:

$$
a^n,\ a^{n+8},\ a^{n+12},\ldots
$$

all have the same cycle position.

Therefore:

$$
\boxed{
\text{Exponents differing by a multiple of the cycle length give the same position}
}
$$

---

# 38. Example

For powers of `3`:

$$
3,9,7,1
$$

Cycle length:

$$
4
$$

Therefore:

$$
3^{10}
$$

and:

$$
3^{14}
$$

have the same last digit.

Both have:

$$
n\bmod4=2
$$

Therefore:

$$
\boxed9
$$

---

# 39. Fast Recognition Table

| Base ends in | What to calculate |
|---:|---|
| `0` | Nothing |
| `1` | Nothing |
| `2` | `n mod 4` |
| `3` | `n mod 4` |
| `4` | `n mod 2` |
| `5` | Nothing |
| `6` | Nothing |
| `7` | `n mod 4` |
| `8` | `n mod 4` |
| `9` | `n mod 2` |

> [!tip] Fastest Exam Table
>
> $$ 
> \boxed{
> 2,3,7,8\rightarrow n\bmod4
> }
> $$
>
> $$ 
> \boxed{
> 4,9\rightarrow n\bmod2
> }
> $$
>
> $$ 
> \boxed{
> 0,1,5,6\rightarrow\text{answer directly}
> }
> $$

---

# 40. Formula Sheet

> [!important] Must Remember

### Last Digit

$$
\boxed{
\text{Last digit}=N\bmod10
}
$$

### Cycle Position

$$
\boxed{
p=n\bmod k
}
$$

### Position `0`

$$
\boxed{
p=0\Rightarrow\text{take }k^{th}\text{ element}
}
$$

### Cycle Length `4`

For:

$$
2,3,7,8
$$

$$
\boxed{
k=4
}
$$

### Cycle Length `2`

For:

$$
4,9
$$

$$
\boxed{
k=2
}
$$

### Cycle Length `1`

For:

$$
0,1,5,6
$$

$$
\boxed{
k=1
}
$$

---

# 41. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Huge power}\rightarrow\text{cycle}
}
$$

### Pattern 2

$$
\boxed{
\text{Only last digit of base matters}
}
$$

### Pattern 3

$$
\boxed{
2,3,7,8\rightarrow\text{cycle length }4
}
$$

### Pattern 4

$$
\boxed{
4,9\rightarrow\text{cycle length }2
}
$$

### Pattern 5

$$
\boxed{
0,1,5,6\rightarrow\text{cycle length }1
}
$$

### Pattern 6

$$
\boxed{
n\bmod k=0\rightarrow\text{last cycle element}
}
$$

### Pattern 7

$$
\boxed{
a^m a^n=a^{m+n}
}
$$

### Pattern 8

$$
\boxed{
(a^m)^n=a^{mn}
}
$$

### Pattern 9

$$
\boxed{
\text{Nested power}\rightarrow\text{reduce inner exponent using outer cycle}
}
$$

---

# 42. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Calculating the entire power.
- ❌ Using the full base instead of its last digit.
- ❌ Assuming every cycle has length `4`.
- ❌ Forgetting the `0` position rule.
- ❌ Combining powers with different bases.
- ❌ Ignoring negative-base parity.
- ❌ Applying cyclicity without checking what modulus is being used.
- ❌ Confusing the cycle length with the cycle position.
- ❌ Forgetting to simplify exponent expressions first.
- ❌ Treating `0^0` like an ordinary power.

---

# 43. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Cyclicity is one of the fastest-scoring concepts in aptitude once memorized.

### Master These First

1. Cycle table
2. Cycle lengths
3. `n mod 4`
4. `n mod 2`
5. Remainder `0`
6. Large exponents
7. Large bases
8. Products of powers
9. Powers of powers
10. Nested powers
11. Negative bases
12. Mixed cyclic expressions

---

# 44. Practice Checklist

- [ ] Cycle of `2`
- [ ] Cycle of `3`
- [ ] Cycle of `4`
- [ ] Cycle of `7`
- [ ] Cycle of `8`
- [ ] Cycle of `9`
- [ ] Fixed cycles `0,1,5,6`
- [ ] Exponent mod `4`
- [ ] Exponent mod `2`
- [ ] Remainder `0`
- [ ] Huge exponents
- [ ] Large bases
- [ ] Products of powers
- [ ] Powers of powers
- [ ] Nested powers
- [ ] Negative bases

---

# 45. Related Topics

- [[Unit Digit]]
- [[Last Digit]]
- [[Last Two Digits]]
- [[Powers and Unit Digits]]
- [[Cyclic Remainders]]
- [[Remainder Patterns]]
- [[Large Number Remainders]]
- [[Remainders]]

---

# 46. Quick Revision

> [!summary] One-Minute Revision

### Main Idea

$$
\boxed{
\text{Power last digits repeat in cycles}
}
$$

### Main Method

$$
\boxed{
\text{Last digit of base}
\rightarrow
\text{cycle}
\rightarrow
n\bmod k
\rightarrow
\text{answer}
}
$$

### Cycle Table

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

### Cycle Length

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

> **Find the cycle first. Reduce the exponent second. If the remainder is `0`, take the last element of the cycle.**

### One-Line Recognition

> **Huge power + last digit → cyclicity is the first pattern you should think of.**