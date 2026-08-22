---
type: concept
subject: aptitude
topic: "Number of Digits"
parent: "01. Number System/Digit Problems"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - digit-problems
  - number-of-digits
  - logarithms
  - powers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Digit Problems]]"
  - "[[Number Formation]]"
  - "[[Digit Sum]]"
  - "[[Reverse of Number]]"
  - "[[Digit-Based Equations]]"
---

# Number of Digits

## 1. Core Concept

> [!summary] Definition
> The **number of digits** tells us how many digits are required to write a positive integer in decimal form.

Examples:

$$
7
$$

has `1` digit.

$$
85
$$

has `2` digits.

$$
472
$$

has `3` digits.

$$
58291
$$

has `5` digits.

---

# 2. Basic Range Pattern

The number of digits can be determined using powers of `10`.

### 1-digit numbers

$$
1\le N\le9
$$

### 2-digit numbers

$$
10\le N\le99
$$

### 3-digit numbers

$$
100\le N\le999
$$

### 4-digit numbers

$$
1000\le N\le9999
$$

Therefore:

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

means `N` has exactly `n` digits.

---

# 3. Main Formula Using Logarithms

For a positive integer `N`:

$$
\boxed{
\text{Number of digits}
=
\lfloor\log_{10}N\rfloor+1
}
$$

This is the most important formula for large numbers.

---

# 4. Example

Find the number of digits in:

$$
N=5832
$$

We know:

$$
1000\le5832<10000
$$

Therefore:

$$
\boxed4
$$

digits.

---

# 5. Example Using Logarithm

Find the number of digits in:

$$
10^7
$$

Using:

$$
\log_{10}(10^7)=7
$$

Therefore:

$$
\lfloor7\rfloor+1
$$

$$
\boxed8
$$

So:

$$
10^7
$$

has `8` digits.

---

# 6. Important Power of 10 Pattern

For:

$$
10^n
$$

the number has:

$$
\boxed{n+1}
$$

digits.

Examples:

$$
10^1=10
$$

has `2` digits.

$$
10^2=100
$$

has `3` digits.

$$
10^5=100000
$$

has `6` digits.

Therefore:

$$
\boxed{
\text{Digits in }10^n=n+1
}
$$

---

# 7. Number of Digits in `10^n - 1`

For:

$$
10^n-1
$$

the number is:

$$
999\ldots999
$$

with exactly `n` digits.

Therefore:

$$
\boxed{
\text{Digits in }10^n-1=n
}
$$

### Examples

$$
10^2-1=99
$$

has `2` digits.

$$
10^5-1=99999
$$

has `5` digits.

---

# 8. Important Range

All `n`-digit positive integers lie in:

$$
\boxed{
[10^{n-1},10^n-1]
}
$$

### Example

All 6-digit numbers lie between:

$$
10^5
$$

and:

$$
10^6-1
$$

Therefore:

$$
\boxed{
100000\le N\le999999
}
$$

---

# 9. Counting `n`-Digit Numbers

The number of positive `n`-digit integers is:

$$
(10^n-1)-(10^{n-1}-1)
$$

Therefore:

$$
\boxed{
9\times10^{n-1}
}
$$

### Example

Number of 4-digit numbers:

$$
9\times10^3
$$

$$
\boxed{9000}
$$

---

# 10. Counting Numbers With a Fixed Number of Digits

### 1-digit

$$
9
$$

### 2-digit

$$
90
$$

### 3-digit

$$
900
$$

### 4-digit

$$
9000
$$

In general:

$$
\boxed{
9\times10^{n-1}
}
$$

---

# 11. Number of Digits in a Product

Suppose:

$$
A\times B=N
$$

Then:

$$
\boxed{
\text{Digits in }N
=
\lfloor\log_{10}(A B)\rfloor+1
}
$$

Using logarithm properties:

$$
\log_{10}(AB)
=
\log_{10}A+\log_{10}B
$$

Therefore:

$$
\boxed{
\text{Digits in }AB
=
\left\lfloor
\log_{10}A+\log_{10}B
\right\rfloor+1
}
$$

---

# 12. Example — Digits in `2 × 5`

$$
2\times5=10
$$

So:

$$
\log_{10}2+\log_{10}5
$$

Since:

$$
\log_{10}10=1
$$

number of digits:

$$
\boxed2
$$

---

# 13. Number of Digits in a Power

For:

$$
N=a^n
$$

the number of digits is:

$$
\boxed{
\lfloor n\log_{10}a\rfloor+1
}
$$

This is extremely important for aptitude.

---

# 14. Example — Digits in `2^10`

Use:

$$
\log_{10}2\approx0.3010
$$

Therefore:

$$
10\log_{10}2
\approx3.010
$$

Then:

$$
\lfloor3.010\rfloor+1
$$

$$
\boxed4
$$

Indeed:

$$
2^{10}=1024
$$

which has `4` digits.

---

# 15. Example — Digits in `3^20`

Use:

$$
\log_{10}3\approx0.4771
$$

Then:

$$
20(0.4771)=9.542
$$

Therefore:

$$
\lfloor9.542\rfloor+1
$$

$$
\boxed{10}
$$

So:

$$
3^{20}
$$

has `10` digits.

---

# 16. Formula for `a^n`

> [!important] Must Remember

For:

$$
a>0
$$

and:

$$
a\ne1
$$

the number of digits in:

$$
a^n
$$

is:

$$
\boxed{
\lfloor n\log_{10}a\rfloor+1
}
$$

---

# 17. Important Special Case — `1^n`

For:

$$
1^n=1
$$

the number of digits is:

$$
\boxed1
$$

The logarithm formula gives:

$$
\log_{10}1=0
$$

so:

$$
0+1=1
$$

---

# 18. Important Special Case — `0`

The standard logarithm formula:

$$
\lfloor\log_{10}N\rfloor+1
$$

is only for:

$$
\boxed{N>0}
$$

Do not apply it to:

$$
N=0
$$

The number `0` has:

$$
\boxed1
$$

digit.

---

# 19. Digits in `10^n × k`

Suppose:

$$
N=k\times10^n
$$

If `k` is a positive integer, multiplying by `10^n` appends `n` zeros.

Therefore:

$$
\boxed{
\text{Digits in }k\times10^n
=
\text{Digits in }k+n
}
$$

### Example

$$
35\times10^4
=
350000
$$

`35` has `2` digits.

Therefore:

$$
2+4=6
$$

digits.

---

# 20. Example

Find the number of digits in:

$$
72\times10^6
$$

`72` has `2` digits.

Appending six zeros gives:

$$
\boxed8
$$

digits.

---

# 21. Digits in Factorial

For small factorials, calculate directly.

For very large factorials, logarithms can be used:

$$
\boxed{
\text{Digits in }n!
=
\lfloor\log_{10}(n!)\rfloor+1
}
$$

Since:

$$
\log_{10}(n!)
=
\log_{10}1+\log_{10}2+\cdots+\log_{10}n
$$

we get:

$$
\boxed{
\text{Digits in }n!
=
\left\lfloor
\sum_{k=1}^{n}\log_{10}k
\right\rfloor+1
}
$$

---

# 22. Example — Digits in `5!`

$$
5!=120
$$

Therefore:

$$
\boxed3
$$

digits.

---

# 23. Number of Digits After Reversal

Normally reversal keeps the same number of digits.

Example:

$$
12345\rightarrow54321
$$

Both have `5` digits.

But trailing zeros disappear.

Example:

$$
12000\rightarrow21
$$

Therefore:

> [!important]
> **The number of digits after reversal equals the original number of digits minus its trailing zeros.**

---

# 24. Example

Consider:

$$
45000
$$

It has:

$$
5
$$

digits.

It has `3` trailing zeros.

Reverse:

$$
00054
$$

Numerically:

$$
54
$$

which has:

$$
\boxed2
$$

digits.

Therefore:

$$
5-3=2
$$

---

# 25. Number of Digits in a Product of Powers

Suppose:

$$
N=a^m b^n
$$

Then:

$$
\log_{10}N
=
m\log_{10}a+n\log_{10}b
$$

Therefore:

$$
\boxed{
\text{Digits}
=
\left\lfloor
m\log_{10}a+n\log_{10}b
\right\rfloor+1
}
$$

---

# 26. Example — `2^10 × 3^5`

Approximate:

$$
\log_{10}2\approx0.3010
$$

$$
\log_{10}3\approx0.4771
$$

Therefore:

$$
10(0.3010)+5(0.4771)
$$

$$
=3.010+2.3855
$$

$$
=5.3955
$$

Number of digits:

$$
\lfloor5.3955\rfloor+1
$$

$$
\boxed6
$$

---

# 27. Number of Digits in a Fraction

For positive values less than `1`, the ordinary formula for integer digit count does not apply directly.

For aptitude, first determine whether the question asks for:

- digits before decimal
- digits after decimal
- decimal places
- significant digits

> [!warning]
> **Do not automatically use the integer digit formula for decimal numbers.**

---

# 28. Number of Digits Between Powers of 10

If:

$$
10^a\le N<10^b
$$

then:

$$
\boxed{
a+1\le\text{digits}(N)\le b
}
$$

### Example

If:

$$
10^4\le N<10^7
$$

then `N` can have:

$$
\boxed5,\ 6,\text{ or }7
$$

digits.

---

# 29. Finding Number of Digits From a Range

Suppose:

$$
1000\le N\le99999
$$

The smallest number has:

$$
4
$$

digits.

The largest has:

$$
5
$$

digits.

Therefore the range contains numbers with:

$$
\boxed4\text{ or }5\text{ digits}
$$

---

# 30. Important Pattern — Powers of 10

Memorize:

$$
10^0=1
$$

$$
10^1=10
$$

$$
10^2=100
$$

$$
10^3=1000
$$

$$
10^4=10000
$$

Therefore:

$$
\boxed{
10^n\text{ has }n+1\text{ digits}
}
$$

---

# 31. Important Pattern — Largest `n`-Digit Number

The largest `n`-digit number is:

$$
\boxed{
10^n-1
}
$$

Examples:

$$
9
$$

$$
99
$$

$$
999
$$

$$
9999
$$

---

# 32. Important Pattern — Smallest `n`-Digit Number

The smallest `n`-digit number is:

$$
\boxed{
10^{n-1}
}
$$

Examples:

### 2-digit

$$
10
$$

### 3-digit

$$
100
$$

### 5-digit

$$
10000
$$

---

# 33. Important Pattern — Difference

The number of `n`-digit numbers is:

$$
(10^n-1)-10^{n-1}+1
$$

Therefore:

$$
\boxed{
9\times10^{n-1}
}
$$

---

# 34. Number of Digits in `a^n` Without Calculating It

For:

$$
2^{100}
$$

do not calculate the power.

Use:

$$
\text{digits}
=
\lfloor100\log_{10}2\rfloor+1
$$

Since:

$$
\log_{10}2\approx0.30103
$$

we get:

$$
100(0.30103)=30.103
$$

Therefore:

$$
\boxed{31}
$$

digits.

---

# 35. Example — `5^20`

Use:

$$
\log_{10}5\approx0.6990
$$

Then:

$$
20(0.6990)=13.98
$$

Therefore:

$$
\lfloor13.98\rfloor+1
$$

$$
\boxed{14}
$$

digits.

---

# 36. Comparing Number of Digits

To compare:

$$
a^m
$$

and:

$$
b^n
$$

you can compare:

$$
m\log_{10}a
$$

and:

$$
n\log_{10}b
$$

The larger value corresponds to the larger number.

This is useful when the actual numbers are enormous.

---

# 37. Example — Compare `2^100` and `3^60`

Approximate:

$$
100\log_{10}2
\approx30.103
$$

and:

$$
60\log_{10}3
\approx28.626
$$

Therefore:

$$
2^{100}>3^{60}
$$

because the logarithm is larger.

---

# 38. Important Pattern — Same Number of Digits

If:

$$
10^{n-1}\le A<10^n
$$

and:

$$
10^{n-1}\le B<10^n
$$

then both have:

$$
\boxed n
$$

digits.

This can be used for quick comparison questions.

---

# 39. Number of Digits in `999...999`

If there are `n` copies of `9`:

$$
\boxed{
999\ldots999=10^n-1
}
$$

Therefore it has exactly:

$$
\boxed n
$$

digits.

---

# 40. Number of Digits in `111...111`

For a number consisting of `n` ones:

$$
111\ldots111
$$

it clearly has:

$$
\boxed n
$$

digits.

The same applies to any fixed non-zero digit repeated `n` times.

---

# 41. Number of Digits in a Concatenated Number

If two numbers are concatenated, the number of digits is the sum of their digit counts, provided the second part is treated as a fixed-width digit block.

Example:

$$
123|4567
$$

has:

$$
3+4=7
$$

digits.

Therefore:

$$
\boxed7
$$

---

# 42. Common Trap — `10^n`

A frequent mistake is:

$$
10^n\rightarrow n\text{ digits}
$$

This is wrong.

Correct:

$$
\boxed{
10^n\rightarrow n+1\text{ digits}
}
$$

because:

$$
10^n=1\underbrace{00\ldots00}_{n\text{ zeros}}
$$

---

# 43. Common Trap — `10^n - 1`

Another common mistake:

$$
10^n-1\rightarrow n+1\text{ digits}
$$

Wrong.

Correct:

$$
\boxed{
10^n-1\rightarrow n\text{ digits}
}
$$

---

# 44. Common Trap — Leading Zeros

Leading zeros do not increase the numerical digit count.

Example:

$$
000123
$$

is:

$$
123
$$

Therefore it has:

$$
\boxed3
$$

digits.

---

# 45. Common Trap — Trailing Zeros

Trailing zeros do count as digits in the original number.

Example:

$$
12000
$$

has:

$$
\boxed5
$$

digits.

But after reversal:

$$
00021
$$

becomes:

$$
21
$$

which has `2` digits.

---

# 46. Formula Sheet

> [!important] Must Remember

### Digits of Positive Integer

$$
\boxed{
\lfloor\log_{10}N\rfloor+1
}
$$

### `n`-Digit Range

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

### Smallest `n`-Digit Number

$$
\boxed{
10^{n-1}
}
$$

### Largest `n`-Digit Number

$$
\boxed{
10^n-1
}
$$

### Number of `n`-Digit Numbers

$$
\boxed{
9\times10^{n-1}
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

### Digits in `a^n`

$$
\boxed{
\lfloor n\log_{10}a\rfloor+1
}
$$

---

# 47. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
10^{n-1}\le N\le10^n-1
}
$$

→ `N` has `n` digits.

### Pattern 2

$$
\boxed{
\text{Digits}(N)=\lfloor\log_{10}N\rfloor+1
}
$$

### Pattern 3

$$
\boxed{
10^n\rightarrow n+1\text{ digits}
}
$$

### Pattern 4

$$
\boxed{
10^n-1\rightarrow n\text{ digits}
}
$$

### Pattern 5

$$
\boxed{
\text{Number of }n\text{-digit numbers}=9\times10^{n-1}
}
$$

### Pattern 6

$$
\boxed{
\text{Digits}(a^n)=\lfloor n\log_{10}a\rfloor+1
}
$$

### Pattern 7

$$
\boxed{
\text{Trailing zeros disappear after reversal}
}
$$

---

# 48. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

This topic becomes especially important when combined with:

- powers
- logarithms
- factorials
- number formation
- comparison
- digit problems

### Master These First

1. Digit ranges
2. Powers of `10`
3. Smallest/largest `n`-digit number
4. Count of `n`-digit numbers
5. Logarithm digit formula
6. Digits in powers
7. Digits in products
8. Digits in factorials
9. Comparing huge powers
10. Leading/trailing zero behavior

---

# 49. Practice Checklist

- [ ] Identify number of digits directly
- [ ] `10^n`
- [ ] `10^n-1`
- [ ] `n`-digit ranges
- [ ] Count `n`-digit numbers
- [ ] Digits in powers
- [ ] Digits in products
- [ ] Digits in factorials
- [ ] Compare huge powers
- [ ] Leading zeros
- [ ] Trailing zeros
- [ ] Digits after reversal
- [ ] Repeated-digit numbers

---

# 50. Related Topics

- [[Digit Problems]]
- [[Number Formation]]
- [[Digit Sum]]
- [[Reverse of Number]]
- [[Digit-Based Equations]]
- [[Powers and Unit Digits]]
- [[Logarithms]]
- [[Factorials]]

---

# 51. Quick Revision

> [!summary] One-Minute Revision

### Basic Range

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

### Smallest `n`-Digit Number

$$
\boxed{
10^{n-1}
}
$$

### Largest `n`-Digit Number

$$
\boxed{
10^n-1
}
$$

### Count of `n`-Digit Numbers

$$
\boxed{
9\times10^{n-1}
}
$$

### Power of 10

$$
\boxed{
10^n\text{ has }n+1\text{ digits}
}
$$

### Power

$$
\boxed{
\text{Digits in }a^n
=
\lfloor n\log_{10}a\rfloor+1
}
$$

### Golden Memory Trick

> **To count digits, find which two consecutive powers of `10` surround the number.**

### One-Line Recognition

> **Huge number or huge power + "how many digits?" → think powers of `10` or `floor(log₁₀N) + 1`.**