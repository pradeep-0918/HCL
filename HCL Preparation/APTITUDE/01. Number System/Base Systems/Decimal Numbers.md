---
type: concept
subject: aptitude
topic: "Decimal Numbers"
parent: "01. Number System/Base Systems"
company: HCL
difficulty: easy
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - base-systems
  - decimal
  - decimal-numbers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Base Systems]]"
  - "[[Binary Numbers]]"
  - "[[Number Base Conversion]]"
  - "[[Base-Based Problems]]"
---

# Decimal Numbers

## 1. Core Concept

> [!summary] Definition
> The **decimal number system** is a **base-10** number system.
>
> It uses ten digits:
>
> $$
> \boxed{0,1,2,3,4,5,6,7,8,9}
> $$
>
> Decimal is the standard number system used in everyday mathematics.

---

# 2. Decimal Place Values

In the decimal system, every position represents a power of `10`.

From right to left:

$$
\boxed{
10^0,\ 10^1,\ 10^2,\ 10^3,\ldots
}
$$

Therefore:

| Position | Power | Value |
|---|---:|---:|
| Units | \(10^0\) | `1` |
| Tens | \(10^1\) | `10` |
| Hundreds | \(10^2\) | `100` |
| Thousands | \(10^3\) | `1000` |
| Ten-thousands | \(10^4\) | `10000` |

---

# 3. Decimal Representation

For a decimal number:

$$
d_nd_{n-1}\ldots d_2d_1d_0
$$

its value is:

$$
\boxed{
d_n10^n+d_{n-1}10^{n-1}+\cdots+d_210^2+d_110+d_0
}
$$

---

# 4. Example

Represent:

$$
5832
$$

using place values.

$$
5832
=
5(1000)+8(100)+3(10)+2
$$

Therefore:

$$
\boxed{
5832=5\times10^3+8\times10^2+3\times10+2
}
$$

---

# 5. General Decimal Formula

For:

$$
N=d_nd_{n-1}\ldots d_1d_0
$$

we have:

$$
\boxed{
N=\sum_{i=0}^{n}d_i10^i
}
$$

This is the decimal equivalent of the binary representation formula.

---

# 6. Decimal Digits

Every decimal digit must satisfy:

$$
\boxed{
0\le d\le9
}
$$

Therefore:

- `0` is valid
- `5` is valid
- `9` is valid
- `10` is **not** a single decimal digit

---

# 7. Why Base 10?

The decimal system has:

$$
10
$$

possible digits:

$$
0,1,2,3,4,5,6,7,8,9
$$

Therefore:

$$
\boxed{
\text{Base}=10
}
$$

---

# 8. Decimal Number System vs Binary

| Property | Decimal | Binary |
|---|---:|---:|
| Base | `10` | `2` |
| Digits | `0–9` | `0,1` |
| Place values | \(10^n\) | \(2^n\) |
| Maximum digit | `9` | `1` |
| Common use | Mathematics | Computers |

---

# 9. Decimal Number With Digits

For a two-digit number:

$$
\boxed{
10a+b
}
$$

For a three-digit number:

$$
\boxed{
100a+10b+c
}
$$

For a four-digit number:

$$
\boxed{
1000a+100b+10c+d
}
$$

This place-value representation is very important in aptitude.

---

# 10. Decimal Fraction

Decimal numbers can also contain a fractional part.

Example:

$$
123.456
$$

The digits after the decimal point represent negative powers of `10`.

Therefore:

$$
123.456
=
1(10^2)+2(10^1)+3(10^0)
+4(10^{-1})+5(10^{-2})+6(10^{-3})
$$

---

# 11. Decimal Place Values After the Point

From left to right after the decimal:

| Position | Power | Value |
|---|---:|---:|
| Tenths | \(10^{-1}\) | `0.1` |
| Hundredths | \(10^{-2}\) | `0.01` |
| Thousandths | \(10^{-3}\) | `0.001` |
| Ten-thousandths | \(10^{-4}\) | `0.0001` |

---

# 12. Example — Decimal Fraction

Consider:

$$
45.372
$$

Then:

$$
45.372
=
4(10)+5(1)+3(0.1)+7(0.01)+2(0.001)
$$

Therefore:

$$
\boxed{
45.372=40+5+0.3+0.07+0.002
}
$$

---

# 13. Decimal Expansion

A decimal fraction can be written as a fraction whose denominator is a power of `10`.

Example:

$$
0.5
=
\frac5{10}
=
\frac12
$$

Therefore:

$$
\boxed{
0.5=\frac12
}
$$

---

# 14. Decimal to Fraction

If there are `n` digits after the decimal point:

$$
\boxed{
\text{Denominator}=10^n
}
$$

### Example

$$
0.375
$$

There are `3` decimal places.

Therefore:

$$
0.375=\frac{375}{1000}
$$

Simplify:

$$
\boxed{
0.375=\frac38
}
$$

---

# 15. Example

Convert:

$$
0.24
$$

to a fraction.

There are `2` decimal places:

$$
0.24=\frac{24}{100}
$$

Simplify:

$$
\boxed{
\frac6{25}
}
$$

---

# 16. Fraction to Decimal

To convert a fraction to decimal:

> **Divide numerator by denominator.**

Example:

$$
\frac34
$$

Perform:

$$
3\div4
$$

Therefore:

$$
\boxed{0.75}
$$

---

# 17. Terminating Decimal

A fraction has a terminating decimal if, after simplification, its denominator contains only the prime factors:

$$
\boxed{2\text{ and }5}
$$

### Examples

$$
\frac12=0.5
$$

$$
\frac14=0.25
$$

$$
\frac58=0.625
$$

All terminate.

---

# 18. Non-Terminating Recurring Decimal

If the simplified denominator contains a prime factor other than `2` or `5`, the decimal expansion does not terminate.

### Example

$$
\frac13
=
0.3333\ldots
$$

Therefore:

$$
\boxed{
\frac13=0.\overline3
}
$$

---

# 19. Important Pattern — Decimal Termination

For:

$$
\frac pq
$$

in lowest terms:

### Terminating

if:

$$
\boxed{
q=2^a5^b
}
$$

### Non-terminating recurring

if `q` has any prime factor other than `2` or `5`.

---

# 20. Example

Determine whether:

$$
\frac7{40}
$$

terminates.

Factor:

$$
40=2^3\times5
$$

Only `2` and `5` occur.

Therefore:

$$
\boxed{\text{Terminating}}
$$

---

# 21. Example

Determine whether:

$$
\frac5{12}
$$

terminates.

Factor:

$$
12=2^2\times3
$$

Since `3` is present:

$$
\boxed{\text{Non-terminating recurring}}
$$

---

# 22. Decimal Place Shifting

Multiplying by `10` moves the decimal point one place right.

$$
12.34\times10=123.4
$$

Therefore:

$$
\boxed{
N\times10
}
$$

shifts the decimal point one place to the right.

---

# 23. Multiplication by Powers of 10

Multiplying by:

$$
10^n
$$

moves the decimal point `n` places right.

Example:

$$
4.567\times1000
$$

$$
\boxed{4567}
$$

because:

$$
1000=10^3
$$

---

# 24. Division by Powers of 10

Dividing by:

$$
10^n
$$

moves the decimal point `n` places left.

Example:

$$
4567\div100
$$

$$
\boxed{45.67}
$$

---

# 25. Important Pattern — Appending Zeros

For an integer:

$$
25
$$

multiplying by `10` gives:

$$
250
$$

Multiplying by `100`:

$$
2500
$$

Therefore:

$$
\boxed{
N\times10^k
}
$$

appends `k` zeros to an integer.

---

# 26. Leading Zeros

Leading zeros do not change the value.

Example:

$$
0075=75
$$

Therefore:

$$
\boxed{
0075=75
}
$$

But in fixed-width representations, leading zeros may be intentionally displayed.

---

# 27. Trailing Zeros

Trailing zeros in an integer affect the written representation but not the value when they are produced by multiplication by powers of `10`.

Example:

$$
75\times100=7500
$$

Therefore:

$$
\boxed{7500}
$$

---

# 28. Decimal Comparison

To compare decimal numbers:

1. Compare integer parts.
2. If equal, compare decimal digits from left to right.
3. Add trailing zeros if necessary.

### Example

Compare:

$$
0.45
$$

and:

$$
0.405
$$

Write:

$$
0.450
$$

and:

$$
0.405
$$

Therefore:

$$
\boxed{0.45>0.405}
$$

---

# 29. Adding Trailing Zeros

Appending zeros after the decimal point does not change the value.

Examples:

$$
0.5=0.50=0.500
$$

Therefore:

$$
\boxed{
0.5=0.500
}
$$

This is useful when comparing decimals.

---

# 30. Decimal Addition

Align decimal points before adding.

Example:

$$
12.45+3.7
$$

Write:

$$
12.45
$$

$$
+3.70
$$

Therefore:

$$
\boxed{16.15}
$$

---

# 31. Decimal Subtraction

Again, align decimal points.

Example:

$$
15.60-7.25
$$

$$
\boxed{8.35}
$$

---

# 32. Decimal Multiplication

Ignore decimal points initially, multiply the numbers, then place the decimal point based on the total number of decimal places.

Example:

$$
1.2\times0.3
$$

Ignore decimals:

$$
12\times3=36
$$

Total decimal places:

$$
1+1=2
$$

Therefore:

$$
\boxed{0.36}
$$

---

# 33. Decimal Division

When dividing by a decimal, multiply both numerator and denominator by a suitable power of `10`.

Example:

$$
4.5\div0.5
$$

Multiply both by `10`:

$$
45\div5
$$

Therefore:

$$
\boxed9
$$

---

# 34. Decimal and Powers of 10

Important values:

$$
10^0=1
$$

$$
10^{-1}=0.1
$$

$$
10^{-2}=0.01
$$

$$
10^{-3}=0.001
$$

$$
10^{-4}=0.0001
$$

Therefore:

$$
\boxed{
10^{-n}=\frac1{10^n}
}
$$

---

# 35. Scientific Notation

Very large or very small decimal numbers can be written in scientific notation:

$$
\boxed{
a\times10^n
}
$$

where:

$$
1\le a<10
$$

### Example

$$
4500000
$$

can be written as:

$$
\boxed{
4.5\times10^6
}
$$

---

# 36. Small Number in Scientific Notation

Example:

$$
0.00032
$$

Move the decimal point four places right:

$$
3.2
$$

Therefore:

$$
\boxed{
0.00032=3.2\times10^{-4}
}
$$

---

# 37. Important Pattern — Scientific Notation

For a positive number:

$$
\boxed{
a\times10^n,\quad1\le a<10
}
$$

The exponent tells how far the decimal point has moved.

---

# 38. Decimal and Percentage

Percentage means "per hundred".

Therefore:

$$
\boxed{
x\%=\frac{x}{100}
}
$$

Examples:

$$
25\%=0.25
$$

$$
50\%=0.5
$$

$$
75\%=0.75
$$

$$
125\%=1.25
$$

---

# 39. Decimal to Percentage

Multiply by `100`.

$$
\boxed{
\text{Percentage}=\text{Decimal}\times100
}
$$

Example:

$$
0.35\times100=35\%
$$

Therefore:

$$
\boxed{0.35=35\%}
$$

---

# 40. Percentage to Decimal

Divide by `100`.

$$
\boxed{
\text{Decimal}=\frac{\text{Percentage}}{100}
}
$$

Example:

$$
72\%=\frac{72}{100}=0.72
$$

---

# 41. Decimal and Fraction Relationship

Important conversions:

| Fraction | Decimal |
|---:|---:|
| \(\frac12\) | `0.5` |
| \(\frac14\) | `0.25` |
| \(\frac34\) | `0.75` |
| \(\frac15\) | `0.2` |
| \(\frac25\) | `0.4` |
| \(\frac35\) | `0.6` |
| \(\frac45\) | `0.8` |
| \(\frac18\) | `0.125` |
| \(\frac38\) | `0.375` |
| \(\frac58\) | `0.625` |
| \(\frac78\) | `0.875` |

These are useful for mental calculations.

---

# 42. Decimal and Rational Numbers

Every terminating decimal can be represented as a rational number.

Example:

$$
0.125=\frac18
$$

Every recurring decimal is also rational.

Example:

$$
0.\overline3=\frac13
$$

Therefore:

$$
\boxed{
\text{Terminating and recurring decimals are rational}
}
$$

---

# 43. Irrational Decimal Numbers

An irrational number has a decimal expansion that is:

- non-terminating
- non-repeating

Examples:

$$
\sqrt2
$$

$$
\pi
$$

Therefore:

$$
\boxed{
\text{Irrational decimal}=\text{non-terminating and non-repeating}
}
$$

---

# 44. Decimal Representation of Real Numbers

Real numbers include:

- terminating decimals
- recurring decimals
- irrational decimals

Therefore:

$$
\boxed{
\mathbb R
=
\text{Rational}\cup\text{Irrational}
}
$$

---

# 45. Decimal Base Formula

For any base `b`, a number:

$$
(a_na_{n-1}\ldots a_0)_b
$$

has value:

$$
\boxed{
\sum_{i=0}^{n}a_i b^i
}
$$

For decimal:

$$
b=10
$$

Therefore:

$$
\boxed{
\sum_{i=0}^{n}a_i10^i
}
$$

---

# 46. Decimal to Binary Connection

Decimal numbers can be converted to binary using repeated division by `2`.

Example:

$$
10_{10}=1010_2
$$

Therefore:

$$
\boxed{
10_{10}=1010_2
}
$$

The decimal system is often the starting point for base-conversion questions.

---

# 47. Decimal to Other Bases

To convert decimal integer `N` to base `b`:

1. Divide by `b`.
2. Record the remainder.
3. Divide the quotient by `b`.
4. Continue until quotient becomes `0`.
5. Read remainders from bottom to top.

Therefore:

$$
\boxed{
\text{Repeated division by the target base}
}
$$

---

# 48. Example — Decimal `25` to Binary

Repeatedly divide by `2`:

$$
25\div2=12\ R1
$$

$$
12\div2=6\ R0
$$

$$
6\div2=3\ R0
$$

$$
3\div2=1\ R1
$$

$$
1\div2=0\ R1
$$

Read upward:

$$
\boxed{11001_2}
$$

---

# 49. Decimal to Octal

For base `8`, repeatedly divide by `8`.

Example:

$$
25\div8=3\ R1
$$

$$
3\div8=0\ R3
$$

Read upward:

$$
\boxed{31_8}
$$

Therefore:

$$
25_{10}=31_8
$$

---

# 50. Decimal to Hexadecimal

For base `16`, repeatedly divide by `16`.

Hexadecimal digits are:

$$
0,1,2,\ldots,9,A,B,C,D,E,F
$$

where:

$$
A=10,\ B=11,\ C=12,\ D=13,\ E=14,\ F=15
$$

### Example

$$
26_{10}
$$

Divide:

$$
26\div16=1\ R10
$$

`10` corresponds to `A`.

Therefore:

$$
\boxed{26_{10}=1A_{16}}
$$

---

# 51. Important Pattern — Base Conversion

### From base `b` to decimal

Use:

$$
\boxed{
\text{digit}\times b^{\text{position}}
}
$$

### From decimal to base `b`

Use:

$$
\boxed{
\text{Repeated division by }b
}
$$

---

# 52. Decimal Number of Digits

For a positive integer `N`, the number of decimal digits is:

$$
\boxed{
\lfloor\log_{10}N\rfloor+1
}
$$

Example:

$$
N=999
$$

Then:

$$
\lfloor\log_{10}999\rfloor+1
$$

gives:

$$
\boxed3
$$

digits.

---

# 53. Decimal Range Pattern

An `n`-digit decimal number satisfies:

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

Therefore:

### 3 digits

$$
100\le N\le999
$$

### 5 digits

$$
10000\le N\le99999
$$

---

# 54. Important Pattern — Decimal Powers

For:

$$
10^n
$$

number of digits:

$$
\boxed{n+1}
$$

For:

$$
10^n-1
$$

number of digits:

$$
\boxed n
$$

---

# 55. Decimal Addition and Carry

When adding decimal digits:

$$
9+1=10
$$

A carry is produced.

This is the decimal equivalent of:

$$
1+1=10_2
$$

in binary.

---

# 56. Decimal Subtraction and Borrow

When:

$$
0-1
$$

cannot be performed directly, borrow from the next place.

Example:

$$
100-1=99
$$

This is an important pattern for powers of `10`.

---

# 57. Important Pattern — `10^n - 1`

Subtracting `1` from a power of `10` gives all `9`s.

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

Therefore:

$$
\boxed{
10^n-1=\underbrace{99\ldots9}_{n\text{ digits}}
}
$$

---

# 58. Decimal Multiplication by `10`

For integers:

$$
N\times10
$$

adds one zero.

For decimals:

$$
N\times10
$$

moves the decimal point one position right.

Therefore:

$$
\boxed{
\times10^n\Rightarrow\text{move decimal point }n\text{ places right}
}
$$

---

# 59. Decimal Division by `10`

Similarly:

$$
\boxed{
\div10^n\Rightarrow\text{move decimal point }n\text{ places left}
}
$$

Example:

$$
72.5\div100
=
0.725
$$

---

# 60. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Confusing decimal base `10` with binary base `2`.
- ❌ Forgetting that decimal digits range from `0` to `9`.
- ❌ Using powers of `2` for decimal place values.
- ❌ Forgetting negative powers after the decimal point.
- ❌ Confusing decimal places with number of digits.
- ❌ Forgetting to simplify fractions when checking decimal termination.
- ❌ Assuming every non-terminating decimal is irrational.
- ❌ Forgetting that recurring decimals are rational.
- ❌ Comparing decimals without aligning decimal places.
- ❌ Confusing `10^n` with `10^n-1`.

---

# 61. Formula Sheet

> [!important] Must Remember

### Decimal Base

$$
\boxed{
b=10
}
$$

### Decimal Representation

$$
\boxed{
N=\sum d_i10^i
}
$$

### Decimal Digit

$$
\boxed{
0\le d\le9
}
$$

### `n`-Digit Range

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

### Number of `n`-Digit Numbers

$$
\boxed{
9\times10^{n-1}
}
$$

### Decimal Digits of `N`

$$
\boxed{
\lfloor\log_{10}N\rfloor+1
}
$$

### Digits in `10^n`

$$
\boxed{
n+1
}
$$

### Digits in `10^n-1`

$$
\boxed{
n
}
$$

### Terminating Fraction

For a fraction in lowest terms:

$$
\boxed{
q=2^a5^b
}
$$

### Decimal to Percentage

$$
\boxed{
\text{Percentage}=100\times\text{Decimal}
}
$$

---

# 62. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Decimal Base

$$
\boxed{
\text{Base}=10
}
$$

### Pattern 2 — Place Values

$$
\boxed{
1,\ 10,\ 100,\ 1000,\ldots
}
$$

### Pattern 3 — Decimal Fraction

$$
\boxed{
10^{-1},10^{-2},10^{-3},\ldots
}
$$

### Pattern 4 — `n`-Digit Range

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

### Pattern 5 — Number of Digits

$$
\boxed{
\lfloor\log_{10}N\rfloor+1
}
$$

### Pattern 6 — Fraction Terminates

$$
\boxed{
\text{Denominator}=2^a5^b
}
$$

### Pattern 7 — Multiply by `10^n`

$$
\boxed{
\text{Decimal point moves }n\text{ places right}
}
$$

### Pattern 8 — Divide by `10^n`

$$
\boxed{
\text{Decimal point moves }n\text{ places left}
}
$$

### Pattern 9 — Percentage

$$
\boxed{
x\%=x/100
}
$$

### Pattern 10 — Power of 10

$$
\boxed{
10^n-1=999\ldots999
}
$$

---

# 63. HCL Preparation Priority

**Priority:** 🔥🔥 High

Focus mainly on:

1. Decimal place value
2. Decimal representation
3. Decimal fractions
4. Fraction-to-decimal conversion
5. Terminating vs recurring decimals
6. Decimal comparison
7. Powers of `10`
8. Decimal-to-binary conversion
9. Decimal-to-octal conversion
10. Decimal-to-hexadecimal conversion
11. Number of decimal digits
12. Decimal percentage relationships

---

# 64. Practice Checklist

- [ ] Decimal place values
- [ ] Decimal representation
- [ ] Decimal fractions
- [ ] Decimal to fraction
- [ ] Fraction to decimal
- [ ] Terminating decimal
- [ ] Recurring decimal
- [ ] Decimal comparison
- [ ] Decimal addition
- [ ] Decimal subtraction
- [ ] Decimal multiplication
- [ ] Decimal division
- [ ] Powers of `10`
- [ ] Decimal to binary
- [ ] Decimal to octal
- [ ] Decimal to hexadecimal
- [ ] Decimal digit count
- [ ] Decimal percentage

---

# 65. Related Topics

- [[Base Systems]]
- [[Binary Numbers]]
- [[Number Base Conversion]]
- [[Base-Based Problems]]
- [[Number of Digits]]
- [[Rational Numbers]]
- [[Irrational Numbers]]
- [[Percentages]]

---

# 66. Quick Revision

> [!summary] One-Minute Revision

### Base

$$
\boxed{
10
}
$$

### Digits

$$
\boxed{
0,1,2,3,4,5,6,7,8,9
}
$$

### Place Values

$$
\boxed{
1,10,100,1000,\ldots
}
$$

### Decimal Fractions

$$
\boxed{
0.1,\ 0.01,\ 0.001,\ldots
}
$$

### `n`-Digit Number

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

### Number of Digits

$$
\boxed{
\lfloor\log_{10}N\rfloor+1
}
$$

### Terminating Fraction

$$
\boxed{
q=2^a5^b
}
$$

### Percentage

$$
\boxed{
x\%=x/100
}
$$

### Golden Memory Trick

> **Decimal → base `10` → every position is a power of `10`.**

### One-Line Recognition

> **Decimal question → identify the place value first; integer side uses `10⁰, 10¹, 10²...`, fractional side uses `10⁻¹, 10⁻², 10⁻³...`.**