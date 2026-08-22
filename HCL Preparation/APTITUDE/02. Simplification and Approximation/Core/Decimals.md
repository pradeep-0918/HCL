---
type: concept
subject: aptitude
topic: "Decimals"
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
  - quantitative-aptitude
wikilinks:
  - "[[02. Simplification and Approximation]]"
  - "[[BODMAS]]"
  - "[[Fractions]]"
  - "[[Recurring Decimals]]"
  - "[[Surds]]"
  - "[[Indices and Exponents]]"
  - "[[Approximation]]"
  - "[[Simplification Tricks]]"
---

# Decimals

## 1. Core Concept

> [!summary] Definition
> A **decimal** is a way of representing a number using powers of `10`.
>
> Example:
>
> $$
> 25.437
> $$
>
> The digits after the decimal point represent:
>
> $$
> 10^{-1},10^{-2},10^{-3},\ldots
> $$

Therefore:

$$
25.437
=
25+\frac4{10}+\frac3{100}+\frac7{1000}
$$

---

# 2. Decimal Place Values

For:

$$
123.456
$$

the place values are:

| Digit | Place | Value |
|---:|---|---:|
| `1` | Hundreds | `100` |
| `2` | Tens | `10` |
| `3` | Ones | `1` |
| `4` | Tenths | `0.1` |
| `5` | Hundredths | `0.01` |
| `6` | Thousandths | `0.001` |

Therefore:

$$
\boxed{
123.456
=
1(100)+2(10)+3+\frac4{10}+\frac5{100}+\frac6{1000}
}
$$

---

# 3. Decimal Representation

Every finite decimal can be written as a fraction whose denominator is a power of `10`.

For example:

$$
0.75=\frac{75}{100}
$$

and:

$$
2.375=\frac{2375}{1000}
$$

Therefore:

$$
\boxed{
\text{Finite decimal}
=
\frac{\text{integer}}{10^n}
}
$$

---

# 4. Decimal to Fraction

Remove the decimal point and divide by the appropriate power of `10`.

### Example

Convert:

$$
0.45
$$

There are two decimal places:

$$
0.45=\frac{45}{100}
$$

Simplify:

$$
\frac{45}{100}
=
\boxed{\frac9{20}}
$$

---

# 5. Decimal to Fraction — Shortcut

For a decimal with `n` digits after the decimal point:

$$
\boxed{
\text{Decimal}
=
\frac{\text{number without decimal point}}{10^n}
}
$$

Then simplify.

### Example

$$
0.625
$$

Three decimal places:

$$
\frac{625}{1000}
$$

Simplify:

$$
\boxed{\frac58}
$$

---

# 6. Fraction to Decimal

Divide numerator by denominator.

Example:

$$
\frac34
$$

$$
3\div4=0.75
$$

Therefore:

$$
\boxed{\frac34=0.75}
$$

---

# 7. Decimal to Percentage

Multiply by `100`.

$$
\boxed{
\text{Decimal}\times100=\text{Percentage}
}
$$

Example:

$$
0.35\times100=35
$$

Therefore:

$$
\boxed{0.35=35\%}
$$

---

# 8. Percentage to Decimal

Divide by `100`.

$$
\boxed{
x\%=\frac{x}{100}
}
$$

Example:

$$
72\%
=
\frac{72}{100}
=
\boxed{0.72}
$$

---

# 9. Decimal ↔ Fraction ↔ Percentage

The three representations are interchangeable.

Example:

$$
0.75
$$

Fraction:

$$
\frac34
$$

Percentage:

$$
75\%
$$

Therefore:

$$
\boxed{
0.75=\frac34=75\%
}
$$

---

# 10. Comparing Decimals

To compare decimals, first align the decimal points.

Example:

$$
0.7
\quad\text{and}\quad
0.65
$$

Write:

$$
0.70
$$

and:

$$
0.65
$$

Therefore:

$$
\boxed{
0.70>0.65
}
$$

So:

$$
\boxed{
0.7>0.65
}
$$

---

# 11. Important Pattern — Trailing Zeros

Adding zeros to the right of a decimal does not change its value.

$$
\boxed{
0.5=0.50=0.500
}
$$

Similarly:

$$
2.7=2.70=2.700
$$

This is useful when comparing decimals.

---

# 12. Leading Zeros

Zeros immediately after the decimal point and before a non-zero digit affect place value.

Example:

$$
0.05\ne0.5
$$

because:

$$
0.05=\frac5{100}
$$

while:

$$
0.5=\frac5{10}
$$

Therefore:

$$
\boxed{
0.05<0.5
}
$$

---

# 13. Decimal Addition

Align decimal points vertically.

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

# 14. Decimal Subtraction

Again, align decimal points.

Example:

$$
15.20-7.35
$$

$$
=7.85
$$

Therefore:

$$
\boxed{7.85}
$$

---

# 15. Decimal Multiplication

Multiply as integers first.

Then count the total number of decimal places in both numbers.

### Example

$$
2.5\times1.2
$$

Ignore decimal points:

$$
25\times12=300
$$

Total decimal places:

$$
1+1=2
$$

Place the decimal two digits from the right:

$$
\boxed{3.00}
$$

Therefore:

$$
\boxed{2.5\times1.2=3}
$$

---

# 16. Decimal Multiplication Rule

If:

- first number has `m` decimal places
- second number has `n` decimal places

then the product has:

$$
\boxed{m+n}
$$

decimal places before removing trailing zeros.

---

# 17. Example

Calculate:

$$
0.25\times0.04
$$

Ignore decimals:

$$
25\times4=100
$$

Total decimal places:

$$
2+2=4
$$

Therefore:

$$
0.0100
$$

Simplify:

$$
\boxed{0.01}
$$

---

# 18. Multiplication by 10

Move the decimal point one place to the right.

$$
\boxed{
x\times10
}
$$

Example:

$$
4.73\times10=47.3
$$

---

# 19. Multiplication by 100

Move the decimal point two places to the right.

$$
\boxed{
x\times100
}
$$

Example:

$$
4.73\times100=473
$$

---

# 20. Multiplication by 1000

Move the decimal point three places to the right.

$$
\boxed{
x\times1000
}
$$

Example:

$$
4.73\times1000=4730
$$

---

# 21. Division by 10

Move the decimal point one place to the left.

$$
\boxed{
x\div10
}
$$

Example:

$$
47.3\div10=4.73
$$

---

# 22. Division by 100

Move the decimal point two places to the left.

$$
\boxed{
x\div100
}
$$

Example:

$$
473\div100=4.73
$$

---

# 23. Division by 1000

Move the decimal point three places to the left.

$$
\boxed{
x\div1000
}
$$

Example:

$$
4730\div1000=4.73
$$

---

# 24. Decimal Division

To divide decimals, make the divisor an integer.

Example:

$$
12.6\div0.3
$$

Multiply both by `10`:

$$
126\div3
$$

Therefore:

$$
\boxed{42}
$$

---

# 25. General Decimal Division Rule

If the divisor has `n` decimal places, multiply both dividend and divisor by:

$$
\boxed{10^n}
$$

This does not change the quotient.

Example:

$$
4.56\div0.12
$$

Multiply both by `100`:

$$
456\div12
$$

Therefore:

$$
\boxed{38}
$$

---

# 26. Decimal Division Shortcut

Example:

$$
7.5\div0.25
$$

Since:

$$
0.25=\frac14
$$

we can write:

$$
7.5\div\frac14
=
7.5\times4
$$

$$
\boxed{30}
$$

---

# 27. Important Decimal Values

Memorize these:

| Decimal | Fraction | Percentage |
|---:|---:|---:|
| `0.1` | `1/10` | `10%` |
| `0.2` | `1/5` | `20%` |
| `0.25` | `1/4` | `25%` |
| `0.5` | `1/2` | `50%` |
| `0.75` | `3/4` | `75%` |
| `0.125` | `1/8` | `12.5%` |
| `0.375` | `3/8` | `37.5%` |
| `0.625` | `5/8` | `62.5%` |
| `0.875` | `7/8` | `87.5%` |

---

# 28. Decimal as Powers of 10

Important:

$$
0.1=10^{-1}
$$

$$
0.01=10^{-2}
$$

$$
0.001=10^{-3}
$$

Therefore:

$$
\boxed{
0.00\ldots01=10^{-n}
}
$$

when there are `n` decimal places.

---

# 29. Place Value Formula

A decimal:

$$
a.bc
$$

can be represented as:

$$
\boxed{
a+\frac b{10}+\frac c{100}
}
$$

For:

$$
12.345
$$

we get:

$$
12+\frac3{10}+\frac4{100}+\frac5{1000}
$$

---

# 30. Decimal Expansion of a Fraction

For:

$$
\frac{a}{10^n}
$$

the decimal point is placed `n` positions from the right.

Example:

$$
\frac{375}{1000}
=
\boxed{0.375}
$$

---

# 31. Terminating Decimal

A decimal that ends after a finite number of digits is called a **terminating decimal**.

Examples:

$$
0.5
$$

$$
0.25
$$

$$
2.375
$$

---

# 32. Recurring Decimal

A decimal whose digits repeat indefinitely is called a **recurring decimal**.

Examples:

$$
0.\overline3
$$

$$
0.\overline{27}
$$

Detailed recurring-decimal conversion will be covered in:

[[Recurring Decimals]]

---

# 33. Terminating Decimal Condition

For a fraction in lowest terms:

$$
\frac pq
$$

the decimal terminates if and only if:

$$
\boxed{
q=2^m5^n
}
$$

where:

$$
m,n\ge0
$$

Example:

$$
\frac7{40}
$$

Since:

$$
40=2^3\times5
$$

the decimal terminates.

---

# 34. Decimal Places

The number of digits after the decimal point is the number of decimal places.

Example:

$$
23.4567
$$

has:

$$
\boxed4
$$

decimal places.

---

# 35. Decimal Digits

A decimal number may have:

- ones
- tenths
- hundredths
- thousandths
- ten-thousandths
- etc.

For:

$$
0.1234
$$

the digits represent:

$$
\frac1{10}
+
\frac2{100}
+
\frac3{1000}
+
\frac4{10000}
$$

---

# 36. Rounding Decimals

To round a number to a specified decimal place:

1. Identify the required digit.
2. Look at the next digit.
3. If the next digit is `5` or greater, increase the required digit by `1`.
4. If it is less than `5`, leave the required digit unchanged.
5. Remove remaining digits.

---

# 37. Example — Round to 2 Decimal Places

Round:

$$
7.386
$$

to two decimal places.

Required:

$$
7.38
$$

Next digit:

$$
6
$$

Since:

$$
6\ge5
$$

increase `8` to `9`.

Therefore:

$$
\boxed{7.39}
$$

---

# 38. Example — Round to 2 Decimal Places

Round:

$$
5.432
$$

The required form begins:

$$
5.43
$$

Next digit:

$$
2
$$

Since:

$$
2<5
$$

answer:

$$
\boxed{5.43}
$$

---

# 39. Decimal Truncation

**Truncation** means simply cutting off digits without rounding.

Example:

$$
7.389
$$

to two decimal places:

$$
\boxed{7.38}
$$

Notice:

- Rounding → `7.39`
- Truncation → `7.38`

---

# 40. Approximation vs Exact Value

Exact:

$$
\frac13=0.333333\ldots
$$

Approximate:

$$
\frac13\approx0.333
$$

Use:

$$
\boxed{\approx}
$$

for approximate values.

Use:

$$
\boxed{=}
$$

when the values are exactly equal.

---

# 41. Significant Digits

Significant digits are the digits that contribute to the precision of a number.

Example:

$$
0.00452
$$

The leading zeros are not significant.

Therefore significant digits are:

$$
4,\ 5,\ 2
$$

So:

$$
\boxed3
$$

significant digits.

---

# 42. Leading Zeros

Zeros before the first non-zero digit are generally not significant.

Example:

$$
0.00072
$$

has:

$$
\boxed2
$$

significant digits:

`7` and `2`.

---

# 43. Trailing Zeros

Trailing zeros after a decimal point can be significant depending on the stated precision.

For example:

$$
2.50
$$

indicates precision to the hundredths place.

Therefore:

$$
2.5=2.50
$$

numerically, but they may communicate different precision.

---

# 44. Decimal Comparison Shortcut

When comparing:

$$
a.bcd
$$

and:

$$
x.yz
$$

compare in this order:

1. Integer part
2. Tenths
3. Hundredths
4. Thousandths
5. Continue as required

Example:

$$
4.729
$$

and:

$$
4.72
$$

Write:

$$
4.729
$$

$$
4.720
$$

Therefore:

$$
\boxed{4.729>4.720}
$$

---

# 45. Decimal Multiplication by Fractions

Example:

$$
0.8\times\frac54
$$

Convert:

$$
0.8=\frac45
$$

Then:

$$
\frac45\times\frac54
$$

Cancel:

$$
\boxed1
$$

This shows why fraction conversion can simplify decimal calculations.

---

# 46. Decimal Addition Shortcut

When adding several decimals, align the decimal point.

Example:

$$
12.5+0.75+3.125
$$

Write:

$$
12.500
$$

$$
0.750
$$

$$
3.125
$$

Therefore:

$$
\boxed{16.375}
$$

---

# 47. Decimal Subtraction Shortcut

Add trailing zeros if necessary.

Example:

$$
8.5-2.375
$$

Write:

$$
8.500-2.375
$$

Therefore:

$$
\boxed{6.125}
$$

---

# 48. Multiplication by `0.5`

Since:

$$
0.5=\frac12
$$

therefore:

$$
\boxed{
x\times0.5=\frac x2
}
$$

Example:

$$
84\times0.5=42
$$

---

# 49. Multiplication by `0.25`

Since:

$$
0.25=\frac14
$$

therefore:

$$
\boxed{
x\times0.25=\frac x4
}
$$

Example:

$$
80\times0.25=20
$$

---

# 50. Multiplication by `0.75`

Since:

$$
0.75=\frac34
$$

therefore:

$$
\boxed{
x\times0.75=\frac{3x}{4}
}
$$

Example:

$$
80\times0.75
=
60
$$

---

# 51. Multiplication by `0.125`

Since:

$$
0.125=\frac18
$$

therefore:

$$
\boxed{
x\times0.125=\frac x8
}
$$

Example:

$$
80\times0.125=10
$$

---

# 52. Division by `0.5`

Since:

$$
0.5=\frac12
$$

division becomes:

$$
x\div0.5=x\times2
$$

Therefore:

$$
\boxed{
x\div0.5=2x
}
$$

Example:

$$
35\div0.5=70
$$

---

# 53. Division by `0.25`

Since:

$$
0.25=\frac14
$$

therefore:

$$
\boxed{
x\div0.25=4x
}
$$

Example:

$$
20\div0.25=80
$$

---

# 54. Division by `0.125`

Since:

$$
0.125=\frac18
$$

therefore:

$$
\boxed{
x\div0.125=8x
}
$$

Example:

$$
12\div0.125=96
$$

---

# 55. Important Decimal Shortcuts

Memorize:

$$
\boxed{
0.5=\frac12
}
$$

$$
\boxed{
0.25=\frac14
}
$$

$$
\boxed{
0.75=\frac34
}
$$

$$
\boxed{
0.125=\frac18
}
$$

$$
\boxed{
0.375=\frac38
}
$$

$$
\boxed{
0.625=\frac58
}
$$

$$
\boxed{
0.875=\frac78
}
$$

These are extremely useful in aptitude calculations.

---

# 56. Decimal and Powers of 10

Moving the decimal point:

### ×10

Move right by `1`.

### ×100

Move right by `2`.

### ×1000

Move right by `3`.

### ÷10

Move left by `1`.

### ÷100

Move left by `2`.

### ÷1000

Move left by `3`.

---

# 57. Common Aptitude Pattern — `9.99...`

Numbers close to powers of `10` can be rewritten.

Example:

$$
9.99
=
10-0.01
$$

Similarly:

$$
99.9=100-0.1
$$

Therefore:

$$
\boxed{
9.99=10-0.01
}
$$

This is useful for fast multiplication and approximation.

---

# 58. Example — Fast Multiplication

Calculate:

$$
9.99\times20
$$

Rewrite:

$$
9.99=10-0.01
$$

Therefore:

$$
(10-0.01)\times20
$$

$$
=200-0.2
$$

$$
\boxed{199.8}
$$

---

# 59. Important Pattern — Decimal Near an Integer

If a decimal is close to an integer:

$$
x=a-\epsilon
$$

or:

$$
x=a+\epsilon
$$

use the nearby integer for faster calculation.

Example:

$$
49.9=50-0.1
$$

$$
99.8=100-0.2
$$

$$
0.99=1-0.01
$$

---

# 60. Decimal Error

If exact value is `E` and approximate value is `A`:

Absolute error:

$$
\boxed{
|E-A|
}
$$

Relative error:

$$
\boxed{
\frac{|E-A|}{|E|}
}
$$

Percentage error:

$$
\boxed{
\frac{|E-A|}{|E|}\times100\%
}
$$

These become important in approximation problems.

---

# 61. Common Traps

> [!warning] Must Avoid

- ❌ Thinking `0.5 < 0.05`.
- ❌ Forgetting to align decimal points during addition/subtraction.
- ❌ Misplacing the decimal after multiplication.
- ❌ Moving the decimal in the wrong direction.
- ❌ Forgetting that `0.50 = 0.5`.
- ❌ Confusing rounding with truncation.
- ❌ Treating a recurring decimal as terminating.
- ❌ Forgetting to simplify decimal-to-fraction conversions.
- ❌ Assuming more decimal digits always means a larger number.
- ❌ Ignoring leading zeros when determining place value.

---

# 62. Formula Sheet

> [!important] Must Remember

### Decimal to Fraction

$$
\boxed{
\frac{\text{number without decimal point}}{10^n}
}
$$

### Decimal to Percentage

$$
\boxed{
\text{Decimal}\times100\%
}
$$

### Percentage to Decimal

$$
\boxed{
\text{Percentage}\div100
}
$$

### Multiplication by `10^n`

$$
\boxed{
\text{Move decimal right by }n
}
$$

### Division by `10^n`

$$
\boxed{
\text{Move decimal left by }n
}
$$

### Decimal Multiplication

$$
\boxed{
\text{Total decimal places}
=
\text{places in first}
+
\text{places in second}
}
$$

### Decimal Division

$$
\boxed{
\text{Multiply both numbers by }10^n
}
$$

where `n` makes the divisor an integer.

### Terminating Decimal

$$
\boxed{
q=2^a5^b
}
$$

for a fraction in lowest terms.

### Absolute Error

$$
\boxed{
|E-A|
}
$$

### Percentage Error

$$
\boxed{
\frac{|E-A|}{|E|}\times100\%
}
$$

---

# 63. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
0.5=\frac12
}
$$

### Pattern 2

$$
\boxed{
0.25=\frac14
}
$$

### Pattern 3

$$
\boxed{
0.75=\frac34
}
$$

### Pattern 4

$$
\boxed{
0.125=\frac18
}
$$

### Pattern 5

$$
\boxed{
0.375=\frac38
}
$$

### Pattern 6

$$
\boxed{
0.625=\frac58
}
$$

### Pattern 7

$$
\boxed{
0.875=\frac78
}
$$

### Pattern 8

$$
\boxed{
x\times0.5=\frac x2
}
$$

### Pattern 9

$$
\boxed{
x\times0.25=\frac x4
}
$$

### Pattern 10

$$
\boxed{
x\div0.25=4x
}
$$

### Pattern 11

$$
\boxed{
9.99=10-0.01
}
$$

### Pattern 12

$$
\boxed{
99.9=100-0.1
}
$$

---

# 64. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Very High

Master these first:

1. Decimal ↔ Fraction
2. Decimal ↔ Percentage
3. Decimal addition
4. Decimal subtraction
5. Decimal multiplication
6. Decimal division
7. ×10, ×100, ×1000
8. ÷10, ÷100, ÷1000
9. Common decimal-fraction conversions
10. Terminating decimal condition
11. Rounding
12. Approximation using nearby integers
13. Decimal comparison
14. Error and percentage error

---

# 65. Practice Checklist

- [ ] Decimal place values
- [ ] Decimal → fraction
- [ ] Fraction → decimal
- [ ] Decimal → percentage
- [ ] Percentage → decimal
- [ ] Compare decimals
- [ ] Add decimals
- [ ] Subtract decimals
- [ ] Multiply decimals
- [ ] Divide decimals
- [ ] ×10
- [ ] ×100
- [ ] ×1000
- [ ] ÷10
- [ ] ÷100
- [ ] ÷1000
- [ ] Common decimal fractions
- [ ] Terminating decimals
- [ ] Rounding
- [ ] Truncation
- [ ] Significant digits
- [ ] Decimal approximation
- [ ] Error calculation

---

# 66. Related Topics

- [[02. Simplification and Approximation]]
- [[BODMAS]]
- [[Fractions]]
- [[Recurring Decimals]]
- [[Surds]]
- [[Indices and Exponents]]
- [[Approximation]]
- [[Simplification Tricks]]
- [[Percentages]]

---

# 67. Quick Revision

> [!summary] One-Minute Revision

### Decimal Place

$$
10^{-1},10^{-2},10^{-3},\ldots
$$

### Decimal → Fraction

$$
\boxed{
\frac{\text{number without decimal}}{10^n}
}
$$

### Decimal → Percentage

$$
\boxed{
\times100
}
$$

### ×10

$$
\boxed{\text{decimal right by 1}}
$$

### ×100

$$
\boxed{\text{decimal right by 2}}
$$

### ÷10

$$
\boxed{\text{decimal left by 1}}
$$

### ÷100

$$
\boxed{\text{decimal left by 2}}
$$

### Terminating Decimal

$$
\boxed{
\text{denominator}=2^a5^b
}
$$

### Golden Memory Trick

> **Addition/Subtraction → align decimal points. Multiplication → count decimal places. Division → make the divisor an integer.**

### One-Line Recognition

> **For decimal aptitude questions, first decide whether fraction conversion, powers of `10`, or direct decimal calculation gives the fastest route.**