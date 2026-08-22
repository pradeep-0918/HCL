---
type: concept
subject: aptitude
topic: "Approximation"
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
  - quantitative-aptitude
wikilinks:
  - "[[02. Simplification and Approximation]]"
  - "[[BODMAS]]"
  - "[[Fractions]]"
  - "[[Decimals]]"
  - "[[Recurring Decimals]]"
  - "[[Surds]]"
  - "[[Indices and Exponents]]"
  - "[[Simplification Tricks]]"
---

# Approximation

## 1. Core Concept

> [!summary] Definition
> **Approximation** means replacing an exact value with a nearby value that is easier to calculate.
>
> Example:
>
> $$
> 49.8\approx50
> $$
>
> The goal in aptitude questions is usually to obtain a value that is sufficiently close to the exact answer with much less calculation.

---

# 2. Exact vs Approximate

Exact equality:

$$
49+1=50
$$

Approximation:

$$
49.8\approx50
$$

Use:

$$
\boxed{=}
$$

for exact equality.

Use:

$$
\boxed{\approx}
$$

for approximate equality.

---

# 3. Why Approximation Is Important

Approximation is useful when:

- calculations contain large numbers
- decimals are difficult
- square roots are involved
- answer choices are far apart
- exact calculation is unnecessarily long
- the question explicitly asks for an approximate value

> [!tip]
> In aptitude exams, **speed matters**. If the options are sufficiently separated, approximation can save significant time.

---

# 4. Basic Rounding Rule

To round a number:

1. Identify the required place.
2. Look at the digit immediately after it.
3. If that digit is `5` or greater, increase the required digit by `1`.
4. If it is less than `5`, leave the required digit unchanged.
5. Remove the remaining digits.

---

# 5. Rounding to the Nearest Integer

Example:

$$
47.3
$$

The decimal part is:

$$
0.3
$$

Since:

$$
0.3<0.5
$$

therefore:

$$
\boxed{47}
$$

---

# 6. Example

Round:

$$
47.8
$$

Since:

$$
0.8>0.5
$$

increase `47` to:

$$
\boxed{48}
$$

---

# 7. Rounding to One Decimal Place

Example:

$$
8.64
$$

Keep:

$$
8.6
$$

Next digit:

$$
4
$$

Since:

$$
4<5
$$

answer:

$$
\boxed{8.6}
$$

---

# 8. Example

Round:

$$
8.67
$$

to one decimal place.

Keep:

$$
8.6
$$

Next digit:

$$
7
$$

Since:

$$
7\ge5
$$

increase `6` to `7`.

Therefore:

$$
\boxed{8.7}
$$

---

# 9. Rounding to Two Decimal Places

Example:

$$
12.346
$$

Keep:

$$
12.34
$$

Next digit:

$$
6
$$

Therefore:

$$
\boxed{12.35}
$$

---

# 10. Approximation of Large Numbers

Example:

$$
4,982,731
$$

For quick calculation:

$$
4,982,731\approx5,000,000
$$

This may be useful when only an approximate answer is required.

---

# 11. Nearest Power of 10

Useful approximations:

$$
998\approx1000
$$

$$
9,970\approx10,000
$$

$$
99,800\approx100,000
$$

Therefore:

> [!tip]
> Numbers close to powers of `10` are often easier to calculate using the nearby power of `10`.

---

# 12. Approximation Using Nearby Integers

Example:

$$
49.7\times20
$$

Instead of calculating directly:

$$
49.7\approx50
$$

Therefore:

$$
50\times20
=
\boxed{1000}
$$

The exact answer is:

$$
994
$$

so the approximation is close.

---

# 13. Numbers Near `100`

If a number is close to `100`, rewrite it as:

$$
100\pm x
$$

Examples:

$$
98=100-2
$$

$$
103=100+3
$$

$$
99.8=100-0.2
$$

This is useful for fast multiplication.

---

# 14. Numbers Near `1000`

Similarly:

$$
998=1000-2
$$

$$
1004=1000+4
$$

$$
999.5=1000-0.5
$$

General pattern:

$$
\boxed{
N\approx1000
}
$$

when `N` is sufficiently close to `1000`.

---

# 15. Approximation of Multiplication

If:

$$
a\approx A
$$

and:

$$
b\approx B
$$

then:

$$
\boxed{
ab\approx AB
}
$$

Example:

$$
19.8\times5.1
$$

Approximate:

$$
19.8\approx20
$$

$$
5.1\approx5
$$

Therefore:

$$
20\times5
=
\boxed{100}
$$

---

# 16. Approximation of Division

Example:

$$
99.5\div5.02
$$

Approximate:

$$
99.5\approx100
$$

and:

$$
5.02\approx5
$$

Therefore:

$$
100\div5
=
\boxed{20}
$$

---

# 17. Approximation of Addition

Example:

$$
49.8+20.2+10.1
$$

Approximate:

$$
50+20+10
$$

Therefore:

$$
\boxed{80}
$$

---

# 18. Approximation of Subtraction

Example:

$$
100.2-49.7
$$

Approximate:

$$
100-50
$$

Therefore:

$$
\boxed{50}
$$

---

# 19. Important Pattern — Compensating Error

Sometimes rounding one number upward and another downward gives a better estimate.

Example:

$$
49.8+30.2
$$

Instead of:

$$
50+30
$$

we get exactly:

$$
\boxed{80}
$$

because:

$$
49.8=50-0.2
$$

and:

$$
30.2=30+0.2
$$

The errors cancel.

---

# 20. Error Cancellation

If:

$$
a=A-\epsilon
$$

and:

$$
b=B+\epsilon
$$

then:

$$
a+b=A+B
$$

because the errors cancel.

This is useful in approximation questions.

---

# 21. Approximation of Square Roots

Find nearby perfect squares.

Example:

$$
\sqrt{50}
$$

We know:

$$
49<50<64
$$

Therefore:

$$
7<\sqrt{50}<8
$$

Since `50` is close to `49`:

$$
\boxed{
\sqrt{50}\approx7.07
}
$$

For rough aptitude calculations:

$$
\boxed{
\sqrt{50}\approx7
}
$$

may be sufficient depending on the answer choices.

---

# 22. Common Square Roots

Memorize approximate values:

$$
\sqrt2\approx1.414
$$

$$
\sqrt3\approx1.732
$$

$$
\sqrt5\approx2.236
$$

$$
\sqrt6\approx2.449
$$

$$
\sqrt7\approx2.646
$$

$$
\sqrt8\approx2.828
$$

$$
\sqrt{10}\approx3.162
$$

---

# 23. Square Root Bounds

If:

$$
a^2<N<(a+1)^2
$$

then:

$$
\boxed{
a<\sqrt N<a+1
}
$$

Example:

$$
64<70<81
$$

Therefore:

$$
\boxed{
8<\sqrt{70}<9
}
$$

---

# 24. Approximation of Cube Roots

Find nearby perfect cubes.

Example:

$$
\sqrt[3]{65}
$$

Since:

$$
4^3=64
$$

and `65` is very close to `64`:

$$
\boxed{
\sqrt[3]{65}\approx4
}
$$

---

# 25. Cube Root Bounds

If:

$$
a^3<N<(a+1)^3
$$

then:

$$
\boxed{
a<\sqrt[3]N<a+1
}
$$

Example:

$$
27<30<64
$$

Therefore:

$$
\boxed{
3<\sqrt[3]{30}<4
}
$$

---

# 26. Approximation of Fractions

Example:

$$
\frac{99}{101}
$$

Since numerator and denominator are close:

$$
\frac{99}{101}\approx1
$$

More precisely:

$$
\frac{99}{101}
=
1-\frac2{101}
$$

Therefore:

$$
\boxed{
\frac{99}{101}\approx0.98
}
$$

---

# 27. Fraction Near 1

Important pattern:

$$
\boxed{
\frac{n-a}{n}
=
1-\frac an
}
$$

Example:

$$
\frac{97}{100}
=
1-\frac3{100}
=
0.97
$$

This is very useful for approximation.

---

# 28. Fraction Near 0

If the numerator is much smaller than the denominator:

$$
\frac an
$$

may be approximated quickly.

Example:

$$
\frac3{1000}=0.003
$$

Therefore:

$$
\boxed{
\frac3{1000}\approx0
}
$$

for rough calculations.

---

# 29. Approximation of Percentages

Example:

$$
49.7\%
$$

can be approximated as:

$$
\boxed{50\%}
$$

This is particularly useful for mental calculations.

---

# 30. Percentage Approximation

Example:

Find approximately `19.8%` of `501`.

Approximate:

$$
19.8\%\approx20\%
$$

and:

$$
501\approx500
$$

Therefore:

$$
20\%\times500
=
100
$$

Answer:

$$
\boxed{\approx100}
$$

---

# 31. Approximation Using Fractions

Useful conversions:

$$
50\%=\frac12
$$

$$
25\%=\frac14
$$

$$
75\%=\frac34
$$

$$
20\%=\frac15
$$

$$
10\%=\frac1{10}
$$

$$
12.5\%=\frac18
$$

These make percentage approximation faster.

---

# 32. Approximation of Products Near 1

Suppose:

$$
(1+x)(1+y)
$$

Expanding:

$$
1+x+y+xy
$$

If `x` and `y` are very small:

$$
xy
$$

may be negligible.

Therefore:

$$
\boxed{
(1+x)(1+y)\approx1+x+y
}
$$

when `xy` is sufficiently small.

---

# 33. Example

Approximate:

$$
1.01\times1.02
$$

Exact:

$$
1+0.01+0.02+(0.01)(0.02)
$$

The final term is:

$$
0.0002
$$

Therefore:

$$
1.01\times1.02\approx1.03
$$

The exact answer is:

$$
1.0302
$$

---

# 34. Approximation of Reciprocal

If `x` is close to `1`:

$$
\frac1{1+x}
\approx1-x
$$

when `x` is small.

Example:

$$
\frac1{1.02}
\approx1-0.02
=
\boxed{0.98}
$$

The exact value is slightly less than `0.98`.

---

# 35. Approximation Around `100`

For:

$$
\frac{100}{98}
$$

we can write:

$$
98=100-2
$$

Therefore:

$$
\frac{100}{98}
=
\frac1{0.98}
\approx1.0204
$$

For rough answer selection:

$$
\boxed{\approx1.02}
$$

---

# 36. Approximation in Answer Choices

> [!important]
> **Do not automatically calculate the exact answer.**
>
> First inspect the answer choices.

Example:

If the options are:

- `98`
- `120`
- `145`
- `170`

and your approximation gives:

$$
\approx121
$$

you can immediately select:

$$
\boxed{120}
$$

if the approximation is sufficiently reliable.

---

# 37. Range-Based Approximation

Sometimes it is safer to establish a range instead of calculating an approximate value.

Example:

$$
19.8\times5.1
$$

We know:

$$
19<19.8<20
$$

and:

$$
5<5.1<6
$$

Therefore:

$$
95<19.8\times5.1<120
$$

This can eliminate answer choices quickly.

---

# 38. Important Pattern — Upper and Lower Bounds

If:

$$
a<x<b
$$

and:

$$
c<y<d
$$

for positive quantities, then:

$$
\boxed{
ac<xy<bd
}
$$

This is useful when answer choices are widely separated.

---

# 39. Approximation of Complex Expressions

Example:

$$
\frac{49.8\times20.1}{9.9}
$$

Approximate:

$$
49.8\approx50
$$

$$
20.1\approx20
$$

$$
9.9\approx10
$$

Therefore:

$$
\frac{50\times20}{10}
=
\boxed{100}
$$

---

# 40. Cancellation Before Approximation

Do not approximate too early if exact cancellation is obvious.

Example:

$$
\frac{49.9\times20}{9.98}
$$

Since:

$$
9.98\approx10
$$

but:

$$
\frac{20}{10}=2
$$

so:

$$
49.9\times2
\approx
\boxed{100}
$$

Look for simplification before rounding.

---

# 41. Approximation Strategy

Use this order:

1. **Simplify**
2. **Cancel**
3. **Convert**
4. **Approximate**
5. **Calculate**
6. **Compare with options**

This prevents unnecessary approximation errors.

---

# 42. Important Rule — Approximate at the Right Time

Bad approach:

$$
\frac{49.8\times20.2}{9.9}
$$

Round everything aggressively before checking structure.

Better:

$$
\frac{49.8\times20.2}{9.9}
$$

Observe:

$$
20.2\div9.9\approx2
$$

Then:

$$
49.8\times2\approx100
$$

Therefore:

$$
\boxed{\approx100}
$$

---

# 43. Approximation and Significant Figures

A value can be rounded to a specified number of significant figures.

Example:

$$
4387
$$

to `2` significant figures:

$$
\boxed{4400}
$$

Example:

$$
0.004387
$$

to `2` significant figures:

$$
\boxed{0.0044}
$$

---

# 44. Absolute Error

If exact value is `E` and approximate value is `A`:

$$
\boxed{
\text{Absolute Error}=|E-A|
}
$$

Example:

Exact:

$$
100
$$

Approximation:

$$
98
$$

Absolute error:

$$
|100-98|
=
\boxed2
$$

---

# 45. Relative Error

$$
\boxed{
\text{Relative Error}
=
\frac{|E-A|}{|E|}
}
$$

Example:

Exact:

$$
100
$$

Approximation:

$$
98
$$

Therefore:

$$
\frac{|100-98|}{100}
=
\frac2{100}
=
\boxed{0.02}
$$

---

# 46. Percentage Error

Multiply relative error by `100`.

$$
\boxed{
\text{Percentage Error}
=
\frac{|E-A|}{|E|}\times100\%
}
$$

For the previous example:

$$
\frac2{100}\times100\%
=
\boxed2\%
$$

---

# 47. Approximation Error

If:

$$
A=E+\epsilon
$$

then:

$$
\boxed{
\text{Error}=\epsilon
}
$$

If:

$$
A<E
$$

the approximation is an **underestimate**.

If:

$$
A>E
$$

the approximation is an **overestimate**.

---

# 48. Underestimate vs Overestimate

Example:

$$
9.8\approx10
$$

Since:

$$
10>9.8
$$

`10` is an:

$$
\boxed{\text{Overestimate}}
$$

Example:

$$
9.8\approx9
$$

Since:

$$
9<9.8
$$

`9` is an:

$$
\boxed{\text{Underestimate}}
$$

---

# 49. Important Approximation Values

Memorize:

$$
\sqrt2\approx1.414
$$

$$
\sqrt3\approx1.732
$$

$$
\sqrt5\approx2.236
$$

$$
\sqrt7\approx2.646
$$

$$
\sqrt{10}\approx3.162
$$

Also:

$$
\frac13\approx0.333
$$

$$
\frac23\approx0.667
$$

$$
\frac15=0.2
$$

$$
\frac18=0.125
$$

---

# 50. Common Approximation Patterns

### Near 10

$$
9.8\approx10
$$

### Near 100

$$
99.7\approx100
$$

### Near 1000

$$
998\approx1000
$$

### Near 1

$$
0.99\approx1
$$

### Near 0

$$
0.002\approx0
$$

The appropriate approximation depends on the required precision.

---

# 51. Common Traps

> [!warning] Must Avoid

- ❌ Rounding every number immediately.
- ❌ Approximating before simplifying obvious fractions.
- ❌ Using an approximation that is too rough for close answer choices.
- ❌ Assuming the nearest integer is always sufficient.
- ❌ Ignoring the denominator when approximating fractions.
- ❌ Forgetting whether your result is an overestimate or underestimate.
- ❌ Confusing truncation with rounding.
- ❌ Treating an approximation as exact.
- ❌ Ignoring error accumulation in multiple operations.
- ❌ Using decimal approximations when exact surd form is required.

---

# 52. Approximation Decision Rule

> [!tip] Exam Strategy

Ask these questions:

### Question 1

**Are the answer choices far apart?**

If yes:

$$
\boxed{\text{Approximate aggressively}}
$$

### Question 2

**Can I simplify or cancel first?**

If yes:

$$
\boxed{\text{Simplify first}}
$$

### Question 3

**Are the answer choices very close?**

If yes:

$$
\boxed{\text{Use a more accurate calculation}}
$$

### Question 4

**Is an exact answer required?**

If yes:

$$
\boxed{\text{Do not approximate}}
$$

---

# 53. Formula Sheet

> [!important] Must Remember

### Rounding

$$
\boxed{
\text{Next digit}\ge5
\Rightarrow
\text{increase previous digit}
}
$$

### Absolute Error

$$
\boxed{
|E-A|
}
$$

### Relative Error

$$
\boxed{
\frac{|E-A|}{|E|}
}
$$

### Percentage Error

$$
\boxed{
\frac{|E-A|}{|E|}\times100\%
}
$$

### Square Root Bounds

$$
\boxed{
a^2<N<(a+1)^2
\Rightarrow
a<\sqrt N<a+1
}
$$

### Cube Root Bounds

$$
\boxed{
a^3<N<(a+1)^3
\Rightarrow
a<\sqrt[3]N<a+1
}
$$

### Near-1 Product

$$
\boxed{
(1+x)(1+y)
=
1+x+y+xy
}
$$

For small `x,y`:

$$
\boxed{
(1+x)(1+y)\approx1+x+y
}
$$

---

# 54. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Round

$$
\boxed{
\text{Next digit}\ge5\Rightarrow+1
}
$$

### Pattern 2 — Near 100

$$
\boxed{
99.8\approx100
}
$$

### Pattern 3 — Near 1000

$$
\boxed{
999.5\approx1000
}
$$

### Pattern 4 — Near 1

$$
\boxed{
0.99\approx1
}
$$

### Pattern 5 — Near Integer

$$
\boxed{
49.8\approx50
}
$$

### Pattern 6 — Square Root Bound

$$
\boxed{
a^2<N<(a+1)^2
}
$$

### Pattern 7 — Cube Root Bound

$$
\boxed{
a^3<N<(a+1)^3
}
$$

### Pattern 8 — Simplify First

$$
\boxed{
\text{Simplify}\rightarrow\text{Cancel}\rightarrow\text{Approximate}
}
$$

### Pattern 9 — Error

$$
\boxed{
\text{Absolute Error}=|E-A|
}
$$

### Pattern 10 — Percentage Error

$$
\boxed{
\frac{|E-A|}{|E|}\times100\%
}
$$

---

# 55. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Very High

Master these first:

1. Rounding
2. Nearest integer
3. Decimal approximation
4. Approximation of fractions
5. Approximation of multiplication
6. Approximation of division
7. Square-root approximation
8. Cube-root approximation
9. Percentage approximation
10. Error calculation
11. Upper and lower bounds
12. Answer-choice elimination
13. Simplify-before-approximate strategy
14. Overestimate vs underestimate

---

# 56. Practice Checklist

- [ ] Exact vs approximate
- [ ] Rounding
- [ ] Decimal approximation
- [ ] Integer approximation
- [ ] Large-number approximation
- [ ] Approximate addition
- [ ] Approximate subtraction
- [ ] Approximate multiplication
- [ ] Approximate division
- [ ] Square-root approximation
- [ ] Cube-root approximation
- [ ] Fraction approximation
- [ ] Percentage approximation
- [ ] Significant figures
- [ ] Absolute error
- [ ] Relative error
- [ ] Percentage error
- [ ] Upper/lower bounds
- [ ] Overestimate
- [ ] Underestimate
- [ ] Answer-choice elimination

---

# 57. Related Topics

- [[02. Simplification and Approximation]]
- [[BODMAS]]
- [[Fractions]]
- [[Decimals]]
- [[Recurring Decimals]]
- [[Surds]]
- [[Indices and Exponents]]
- [[Simplification Tricks]]
- [[Percentages]]
- [[Error Analysis]]

---

# 58. Quick Revision

> [!summary] One-Minute Revision

### Rounding

$$
\boxed{
5\text{ or more}\rightarrow\text{round up}
}
$$

### Near Integer

$$
\boxed{
49.8\approx50
}
$$

### Near 100

$$
\boxed{
99.8\approx100
}
$$

### Near 1000

$$
\boxed{
998\approx1000
}
$$

### Square Root

$$
\boxed{
a^2<N<(a+1)^2
\Rightarrow
a<\sqrt N<a+1
}
$$

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

### Golden Memory Trick

> **Simplify → cancel → approximate → calculate → compare with options.**

### One-Line Recognition

> **If answer choices are widely separated, don't waste time finding an exact value—use a controlled approximation and eliminate the wrong options.**