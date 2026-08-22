---
type: concept
subject: aptitude
topic: "Recurring Decimals"
parent: "02. Simplification and Approximation"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - simplification
  - approximation
  - decimals
  - recurring-decimals
  - quantitative-aptitude
wikilinks:
  - "[[02. Simplification and Approximation]]"
  - "[[BODMAS]]"
  - "[[Fractions]]"
  - "[[Decimals]]"
  - "[[Surds]]"
  - "[[Indices and Exponents]]"
  - "[[Approximation]]"
  - "[[Simplification Tricks]]"
---

# Recurring Decimals

## 1. Core Concept

> [!summary] Definition
> A **recurring decimal** is a decimal in which one or more digits repeat indefinitely.
>
> Examples:
>
> $$
> 0.\overline{3}=0.3333\ldots
> $$
>
> $$
> 0.\overline{27}=0.272727\ldots
> $$
>
> $$
> 0.1\overline{6}=0.16666\ldots
> $$

The repeating part is called the **repetend**.

---

# 2. Types of Recurring Decimals

There are two major types.

### Pure Recurring Decimal

The repetition begins immediately after the decimal point.

Examples:

$$
0.\overline3
$$

$$
0.\overline{27}
$$

$$
0.\overline{142}
$$

---

### Mixed Recurring Decimal

There are non-repeating digits before the repeating part.

Examples:

$$
0.1\overline6
$$

$$
0.23\overline7
$$

$$
0.12\overline{34}
$$

---

# 3. Notation

A bar over digits indicates repetition.

$$
0.\overline3
$$

means:

$$
0.333333\ldots
$$

while:

$$
0.\overline{27}
$$

means:

$$
0.27272727\ldots
$$

The entire block under the bar repeats.

---

# 4. Pure Recurring Decimal to Fraction

For:

$$
0.\overline{a}
$$

the fraction is:

$$
\boxed{
\frac{a}{9}
}
$$

### Example

$$
0.\overline3
$$

Therefore:

$$
\boxed{
0.\overline3=\frac13
}
$$

---

# 5. One-Digit Repetend

If one digit repeats:

$$
0.\overline d
$$

then:

$$
\boxed{
0.\overline d=\frac d9
}
$$

Examples:

$$
0.\overline2=\frac29
$$

$$
0.\overline5=\frac59
$$

$$
0.\overline7=\frac79
$$

---

# 6. Why the Denominator Is `9`

Let:

$$
x=0.\overline3
$$

Then:

$$
x=0.3333\ldots
$$

Multiply by `10`:

$$
10x=3.3333\ldots
$$

Subtract:

$$
10x-x=3
$$

Therefore:

$$
9x=3
$$

So:

$$
\boxed{x=\frac39=\frac13}
$$

---

# 7. Two-Digit Repetend

For:

$$
0.\overline{ab}
$$

the fraction is:

$$
\boxed{
\frac{ab}{99}
}
$$

where `ab` is treated as a two-digit number.

---

# 8. Example

Convert:

$$
0.\overline{27}
$$

to a fraction.

Since two digits repeat:

$$
\frac{27}{99}
$$

Simplify:

$$
\frac{27}{99}
=
\boxed{\frac3{11}}
$$

Therefore:

$$
\boxed{
0.\overline{27}=\frac3{11}
}
$$

---

# 9. Three-Digit Repetend

For:

$$
0.\overline{abc}
$$

the fraction is:

$$
\boxed{
\frac{abc}{999}
}
$$

Example:

$$
0.\overline{123}
=
\frac{123}{999}
$$

Simplify if possible.

---

# 10. General Pure Recurring Formula

If exactly `n` digits repeat:

$$
\boxed{
0.\overline{A}
=
\frac{A}{10^n-1}
}
$$

Since:

$$
10^n-1
$$

contains `n` nines:

$$
10^1-1=9
$$

$$
10^2-1=99
$$

$$
10^3-1=999
$$

$$
10^4-1=9999
$$

---

# 11. Pure Recurring Examples

### One digit

$$
0.\overline7
=
\frac79
$$

### Two digits

$$
0.\overline{45}
=
\frac{45}{99}
=
\boxed{\frac5{11}}
$$

### Three digits

$$
0.\overline{125}
=
\frac{125}{999}
$$

---

# 12. Important Pattern

> [!important]

If:

$$
n=\text{number of repeating digits}
$$

then:

$$
\boxed{
\text{Denominator}=10^n-1
}
$$

Memory:

- `1` repeating digit → `9`
- `2` repeating digits → `99`
- `3` repeating digits → `999`
- `4` repeating digits → `9999`

---

# 13. Mixed Recurring Decimal

Consider:

$$
0.1\overline6
$$

The digit `1` does not repeat.

The digit `6` repeats.

We need a different formula.

---

# 14. Mixed Recurring Decimal Formula

For a mixed recurring decimal:

$$
0.\text{non-repeating digits}\overline{\text{repeating digits}}
$$

use:

$$
\boxed{
\frac{
\text{number formed by all digits}
-
\text{number formed by non-repeating digits}
}{
\underbrace{99\ldots9}_{\text{repeating digits}}
\underbrace{00\ldots0}_{\text{non-repeating digits}}
}
}
$$

This is one of the most important formulas.

---

# 15. Example — `0.1̅6`

Convert:

$$
0.1\overline6
$$

to a fraction.

All digits:

$$
16
$$

Non-repeating digits:

$$
1
$$

Repeating digits:

`1` digit → denominator begins with one `9`.

Non-repeating digits:

`1` digit → append one `0`.

Therefore:

$$
\frac{16-1}{90}
$$

$$
=\frac{15}{90}
$$

$$
\boxed{\frac16}
$$

---

# 16. Another Mixed Example

Convert:

$$
0.23\overline7
$$

to a fraction.

All digits:

$$
237
$$

Non-repeating part:

$$
23
$$

Repeating digits:

`7` → one digit.

Non-repeating digits:

`23` → two digits.

Denominator:

$$
900
$$

Therefore:

$$
\frac{237-23}{900}
$$

$$
=\frac{214}{900}
$$

Simplify:

$$
\boxed{\frac{107}{450}}
$$

---

# 17. Mixed Recurring Shortcut

Remember the structure:

$$
\boxed{
\frac{\text{All digits}-\text{Non-repeating digits}}
{\text{9s followed by 0s}}
}
$$

The number of:

- `9`s = number of repeating digits
- `0`s = number of non-repeating digits

---

# 18. Example — Two Repeating Digits

Convert:

$$
0.12\overline{34}
$$

Here:

- Non-repeating digits = `12`
- Repeating digits = `34`

All digits:

$$
1234
$$

Denominator:

$$
9900
$$

Therefore:

$$
\frac{1234-12}{9900}
$$

$$
=\frac{1222}{9900}
$$

Simplify:

$$
\boxed{\frac{611}{4950}}
$$

---

# 19. Why the Mixed Formula Works

Suppose:

$$
x=0.12\overline{34}
$$

There are:

- `2` non-repeating digits
- `2` repeating digits

Multiply first by:

$$
10^2
$$

Then:

$$
100x=12.\overline{34}
$$

Multiply again by:

$$
10^2
$$

giving:

$$
10000x=1234.\overline{34}
$$

Subtract:

$$
10000x-100x=1222
$$

Therefore:

$$
9900x=1222
$$

Hence:

$$
x=\frac{1222}{9900}
$$

which simplifies to:

$$
\boxed{\frac{611}{4950}}
$$

---

# 20. Pure Recurring vs Mixed Recurring

| Type | Example | Formula |
|---|---|---|
| Pure | \(0.\overline3\) | Repeating digits / `9`s |
| Pure | \(0.\overline{27}\) | `27 / 99` |
| Mixed | \(0.1\overline6\) | `(16 - 1) / 90` |
| Mixed | \(0.23\overline7\) | `(237 - 23) / 900` |

---

# 21. Terminating vs Recurring

A decimal can be:

### Terminating

$$
0.25
$$

### Pure recurring

$$
0.\overline3
$$

### Mixed recurring

$$
0.1\overline6
$$

---

# 22. Fraction and Decimal Relationship

For a fraction in lowest terms:

$$
\frac pq
$$

if:

$$
q=2^a5^b
$$

then the decimal terminates.

Otherwise, it repeats.

Therefore:

$$
\boxed{
q=2^a5^b
\Rightarrow
\text{terminating decimal}
}
$$

and:

$$
\boxed{
q\text{ has another prime factor}
\Rightarrow
\text{recurring decimal}
}
$$

---

# 23. Example — Terminating

Consider:

$$
\frac7{40}
$$

Factor denominator:

$$
40=2^3\times5
$$

Only `2` and `5`.

Therefore:

$$
\boxed{\text{Terminating}}
$$

---

# 24. Example — Recurring

Consider:

$$
\frac5{12}
$$

Factor:

$$
12=2^2\times3
$$

Since `3` is present:

$$
\boxed{\text{Recurring}}
$$

Indeed:

$$
\frac5{12}=0.41666\ldots
$$

---

# 25. Example — Recurring

Consider:

$$
\frac7{15}
$$

Factor:

$$
15=3\times5
$$

Since `3` is present:

$$
\boxed{\text{Recurring}}
$$

---

# 26. Pure Recurring Fraction Conversion

Suppose:

$$
x=0.\overline{45}
$$

Multiply by `100` because two digits repeat:

$$
100x=45.\overline{45}
$$

Subtract:

$$
100x-x=45
$$

$$
99x=45
$$

Therefore:

$$
x=\frac{45}{99}
$$

$$
\boxed{x=\frac5{11}}
$$

---

# 27. Important Pattern — Repeating `9`

A famous identity:

$$
\boxed{
0.\overline9=1
}
$$

Because:

$$
0.9999\ldots=1
$$

This is mathematically exact.

---

# 28. Proof

Let:

$$
x=0.\overline9
$$

Then:

$$
10x=9.\overline9
$$

Subtract:

$$
10x-x=9
$$

Therefore:

$$
9x=9
$$

and:

$$
\boxed{x=1}
$$

---

# 29. Important Identities

Memorize:

$$
\boxed{
0.\overline3=\frac13
}
$$

$$
\boxed{
0.\overline6=\frac23
}
$$

$$
\boxed{
0.\overline9=1
}
$$

$$
\boxed{
0.\overline{27}=\frac3{11}
}
$$

$$
\boxed{
0.\overline{45}=\frac5{11}
}
$$

---

# 30. Recurring Decimal to Percentage

Multiply by `100%`.

Example:

$$
0.\overline3
$$

Since:

$$
0.\overline3=\frac13
$$

percentage:

$$
\frac13\times100\%
$$

Therefore:

$$
\boxed{33.\overline3\%}
$$

---

# 31. Recurring Decimal in Simplification

Example:

$$
0.\overline3+\frac16
$$

Convert:

$$
0.\overline3=\frac13
$$

Therefore:

$$
\frac13+\frac16
$$

$$
=\frac26+\frac16
$$

$$
=\boxed{\frac12}
$$

---

# 32. Example — Recurring Decimal Subtraction

Calculate:

$$
0.\overline6-\frac13
$$

Since:

$$
0.\overline6=\frac23
$$

then:

$$
\frac23-\frac13
=
\boxed{\frac13}
$$

---

# 33. Example — Recurring Decimal Multiplication

Calculate:

$$
0.\overline3\times9
$$

Convert:

$$
0.\overline3=\frac13
$$

Therefore:

$$
\frac13\times9
=
\boxed3
$$

---

# 34. Recurring Decimal Comparison

Convert recurring decimals to fractions when comparison is difficult.

Example:

Compare:

$$
0.\overline6
$$

and:

$$
0.65
$$

First:

$$
0.\overline6=\frac23
$$

and:

$$
0.65=\frac{13}{20}
$$

Compare:

$$
\frac23
\quad\text{and}\quad
\frac{13}{20}
$$

Cross multiply:

$$
2(20)=40
$$

$$
13(3)=39
$$

Therefore:

$$
\boxed{
0.\overline6>0.65
}
$$

---

# 35. Important Pattern — Number of 9s

If the repeating block contains:

### 1 digit

$$
9
$$

### 2 digits

$$
99
$$

### 3 digits

$$
999
$$

### 4 digits

$$
9999
$$

Therefore:

$$
\boxed{
10^n-1
}
$$

---

# 36. Mixed Decimal Denominator Pattern

If there are:

- `r` repeating digits
- `n` non-repeating digits

then denominator is:

$$
\boxed{
(10^r-1)\times10^n
}
$$

Equivalent representation:

$$
\boxed{
\underbrace{99\ldots9}_{r}
\underbrace{00\ldots0}_{n}
}
$$

---

# 37. Example

For:

$$
0.123\overline{45}
$$

we have:

- repeating digits = `2`
- non-repeating digits = `3`

Therefore denominator:

$$
99\times1000
$$

$$
\boxed{99000}
$$

---

# 38. General Mixed Formula

For:

$$
0.A\overline{B}
$$

where:

- `A` has `n` digits
- `B` has `r` digits

then:

$$
\boxed{
0.A\overline B
=
\frac{
AB-A
}{
(10^r-1)10^n
}
}
$$

where `AB` means the digits of `A` followed by `B`.

---

# 39. Recurring Decimal as Infinite Geometric Series

For:

$$
0.\overline a
$$

we can write:

$$
\frac a{10}
+
\frac a{10^2}
+
\frac a{10^3}
+\cdots
$$

This is a geometric progression.

Using:

$$
S=\frac{a_1}{1-r}
$$

we get:

$$
\boxed{
0.\overline a=\frac a9
}
$$

This provides another way to understand the formula.

---

# 40. Example Using GP

Find:

$$
0.\overline2
$$

Write:

$$
\frac2{10}
+
\frac2{100}
+
\frac2{1000}
+\cdots
$$

Here:

$$
a_1=\frac2{10}
$$

and:

$$
r=\frac1{10}
$$

Therefore:

$$
S=
\frac{\frac2{10}}
{1-\frac1{10}}
$$

$$
=
\frac{\frac2{10}}{\frac9{10}}
$$

$$
=\boxed{\frac29}
$$

---

# 41. Recurring Decimal with Integer Part

Suppose:

$$
2.\overline3
$$

Separate:

$$
2+0.\overline3
$$

Therefore:

$$
2+\frac13
=
\boxed{\frac73}
$$

---

# 42. Example

Convert:

$$
4.\overline{27}
$$

to a fraction.

Separate:

$$
4+\frac3{11}
$$

Therefore:

$$
\frac{44+3}{11}
$$

$$
\boxed{\frac{47}{11}}
$$

---

# 43. Mixed Recurring With Integer Part

Consider:

$$
3.1\overline6
$$

First:

$$
0.1\overline6=\frac16
$$

Therefore:

$$
3+\frac16
=
\boxed{\frac{19}{6}}
$$

---

# 44. Shortcut — Integer Part

For a recurring decimal with an integer part:

$$
N+\text{recurring part}
$$

convert the recurring part first, then add `N`.

This is usually faster than treating the entire number at once.

---

# 45. Recurring Decimal and Approximation

Recurring decimals are infinite, so aptitude questions may ask for approximate values.

Example:

$$
\frac13
=
0.3333\ldots
$$

To three decimal places:

$$
\boxed{0.333}
$$

To two decimal places:

$$
\boxed{0.33}
$$

---

# 46. Common Traps

> [!warning] Must Avoid

- ❌ Putting `9`s only for the non-repeating digits.
- ❌ Forgetting the `0`s in mixed recurring decimals.
- ❌ Using `99` when only one digit repeats.
- ❌ Treating `0.27̅` as `0.\overline{27}`.
- ❌ Forgetting to simplify the resulting fraction.
- ❌ Confusing terminating and recurring decimals.
- ❌ Assuming every non-terminating decimal is irrational.
- ❌ Forgetting that recurring decimals are rational.
- ❌ Rounding a recurring decimal when an exact fraction is required.
- ❌ Forgetting the integer part.

---

# 47. Important Fact — Recurring Decimals Are Rational

Every recurring decimal can be expressed as a fraction of integers.

Therefore:

$$
\boxed{
\text{Recurring decimal}\Rightarrow\text{Rational number}
}
$$

Examples:

$$
0.\overline3=\frac13
$$

$$
0.\overline{27}=\frac3{11}
$$

---

# 48. Important Fact — Non-Terminating Does Not Mean Irrational

A non-terminating decimal can be either:

### Rational

$$
0.\overline3
$$

### Irrational

$$
\sqrt2=1.41421356\ldots
$$

The difference is:

> **Rational non-terminating decimals repeat. Irrational decimals do not repeat periodically.**

---

# 49. Recurring vs Irrational

| Number | Decimal Type | Classification |
|---|---|---|
| \(0.25\) | Terminating | Rational |
| \(0.\overline3\) | Recurring | Rational |
| \(0.\overline{27}\) | Recurring | Rational |
| \(\sqrt2\) | Non-terminating, non-recurring | Irrational |
| \(\pi\) | Non-terminating, non-recurring | Irrational |

---

# 50. Aptitude Recognition Pattern

If you see:

$$
0.\overline3
$$

immediately think:

$$
\boxed{\frac13}
$$

If you see:

$$
0.\overline{27}
$$

think:

$$
\boxed{\frac{27}{99}}
$$

If you see:

$$
0.1\overline6
$$

think:

$$
\boxed{\frac{16-1}{90}}
$$

---

# 51. Formula Sheet

> [!important] Must Remember

### One Repeating Digit

$$
\boxed{
0.\overline a=\frac a9
}
$$

### Two Repeating Digits

$$
\boxed{
0.\overline{ab}=\frac{ab}{99}
}
$$

### Three Repeating Digits

$$
\boxed{
0.\overline{abc}=\frac{abc}{999}
}
$$

### `n` Repeating Digits

$$
\boxed{
0.\overline A
=
\frac{A}{10^n-1}
}
$$

### Mixed Recurring Decimal

$$
\boxed{
\frac{
\text{All digits}-\text{Non-repeating digits}
}{
\text{9s followed by 0s}
}
}
$$

### Mixed Denominator

$$
\boxed{
(10^r-1)10^n
}
$$

where:

- `r` = repeating digits
- `n` = non-repeating digits

### Terminating Condition

$$
\boxed{
q=2^a5^b
}
$$

for a fraction in lowest terms.

---

# 52. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
0.\overline a=\frac a9
}
$$

### Pattern 2

$$
\boxed{
0.\overline{ab}=\frac{ab}{99}
}
$$

### Pattern 3

$$
\boxed{
0.\overline{abc}=\frac{abc}{999}
}
$$

### Pattern 4

$$
\boxed{
\text{Pure recurring}\rightarrow\text{9s}
}
$$

### Pattern 5

$$
\boxed{
\text{Mixed recurring}\rightarrow\text{9s followed by 0s}
}
$$

### Pattern 6

$$
\boxed{
\text{Numerator}=
\text{all digits}-\text{non-repeating digits}
}
$$

### Pattern 7

$$
\boxed{
\text{Recurring decimal}\Rightarrow\text{rational}
}
$$

### Pattern 8

$$
\boxed{
0.\overline9=1
}
$$

### Pattern 9

$$
\boxed{
q=2^a5^b
\Rightarrow
\text{terminating}
}
$$

### Pattern 10

$$
\boxed{
q\text{ has another prime factor}
\Rightarrow
\text{recurring}
}
$$

---

# 53. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Very High

Master these first:

1. Pure recurring → fraction
2. Mixed recurring → fraction
3. `9`, `99`, `999` pattern
4. `9s + 0s` pattern
5. Terminating vs recurring
6. Fraction → recurring decimal
7. Recurring decimal arithmetic
8. Recurring decimal comparison
9. Recurring decimal with integer part
10. Recurring decimal approximation

---

# 54. Practice Checklist

- [ ] Identify recurring decimal
- [ ] Pure recurring decimal
- [ ] Mixed recurring decimal
- [ ] One-digit repetend
- [ ] Two-digit repetend
- [ ] Three-digit repetend
- [ ] General recurring formula
- [ ] Mixed recurring formula
- [ ] Decimal → fraction
- [ ] Fraction → recurring decimal
- [ ] Terminating vs recurring
- [ ] Recurring decimal arithmetic
- [ ] Recurring decimal comparison
- [ ] Integer + recurring decimal
- [ ] Approximate recurring decimals

---

# 55. Related Topics

- [[02. Simplification and Approximation]]
- [[BODMAS]]
- [[Fractions]]
- [[Decimals]]
- [[Surds]]
- [[Indices and Exponents]]
- [[Approximation]]
- [[Simplification Tricks]]
- [[Rational Numbers]]
- [[Irrational Numbers]]

---

# 56. Quick Revision

> [!summary] One-Minute Revision

### Pure Recurring

$$
\boxed{
0.\overline A
=
\frac{A}{10^n-1}
}
$$

### One Digit

$$
\boxed{
0.\overline a=\frac a9
}
$$

### Two Digits

$$
\boxed{
0.\overline{ab}=\frac{ab}{99}
}
$$

### Mixed Recurring

$$
\boxed{
\frac{
\text{All digits}-\text{Non-repeating digits}
}{
\text{9s + 0s}
}
}
$$

### Terminating

$$
\boxed{
q=2^a5^b
}
$$

### Recurring

$$
\boxed{
\text{Any other prime factor in }q
}
$$

### Golden Memory Trick

> **Pure recurring → put the repeating digits over 9s. Mixed recurring → subtract the non-repeating part, then use 9s followed by 0s.**

### One-Line Recognition

> **See a repeating bar → convert it to a fraction first; this usually makes the aptitude calculation much easier.**