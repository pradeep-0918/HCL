---
type: concept
subject: aptitude
topic: "Successive Increase"
parent: "03. Percentage > Percentage Change"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - percentage
  - successive-increase
  - quantitative-aptitude
wikilinks:
  - "[[03. Percentage]]"
  - "[[Percentage Increase]]"
  - "[[Percentage Decrease]]"
  - "[[Successive Decrease]]"
  - "[[Net Percentage Change]]"
  - "[[Reverse Percentage]]"
---

# Successive Increase

## 1. Core Concept

> [!summary] Definition
> **Successive increase** means a quantity is increased by a percentage and then increased again by another percentage.

The second increase is calculated on the **already increased value**, not the original value.

This is the most important idea.

---

# 2. Why We Cannot Simply Add Percentages

Suppose a number increases by:

- `10%`
- then `20%`

A common mistake is:

$$
10\%+20\%=30\%
$$

This is **wrong**.

Why?

Because the second `20%` is calculated on the new value after the first increase.

---

# 3. Basic Example

Start with:

$$
100
$$

First increase = `10%`

$$
100\times1.10
=
110
$$

Second increase = `20%`

$$
110\times1.20
=
132
$$

Final value:

$$
\boxed{132}
$$

Net increase:

$$
132-100=32
$$

Therefore:

$$
\boxed{32\%}
$$

---

# 4. Main Formula

For successive increases of `a%` and `b%`:

$$
\boxed{
\text{Final}
=
\text{Original}
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
}
$$

---

# 5. Net Successive Increase Formula

For two successive increases:

$$
\boxed{
\text{Net Increase}
=
a+b+\frac{ab}{100}
}
$$

This is one of the most important aptitude shortcuts.

---

# 6. Derivation

Start with:

$$
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
$$

Expand:

$$
1+\frac a{100}+\frac b{100}
+\frac{ab}{10000}
$$

Therefore:

$$
=
1+
\frac{a+b}{100}
+
\frac{ab}{10000}
$$

Convert the additional percentage:

$$
\frac{ab}{10000}
=
\frac{ab/100}{100}
$$

Therefore net percentage increase:

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

---

# 7. Example — 10% and 20%

Using the shortcut:

$$
10+20+\frac{10\times20}{100}
$$

$$
=30+2
$$

$$
=\boxed{32\%}
$$

---

# 8. Example — 20% and 30%

$$
20+30+\frac{20\times30}{100}
$$

$$
=50+6
$$

$$
=\boxed{56\%}
$$

---

# 9. Example — 25% and 20%

$$
25+20+\frac{25\times20}{100}
$$

$$
=45+5
$$

$$
=\boxed{50\%}
$$

---

# 10. Example — 10% and 10%

$$
10+10+\frac{10\times10}{100}
$$

$$
=20+1
$$

$$
=\boxed{21\%}
$$

Therefore:

> Two successive `10%` increases produce a `21%` increase, not `20%`.

---

# 11. Example — 20% and 20%

$$
20+20+\frac{20\times20}{100}
$$

$$
=40+4
$$

$$
=\boxed{44\%}
$$

Therefore:

$$
\boxed{
20\%+20\%\text{ successive increase}=44\%
}
$$

---

# 12. Example — 50% and 50%

$$
50+50+\frac{50\times50}{100}
$$

$$
=100+25
$$

$$
=\boxed{125\%}
$$

So a quantity becomes:

$$
\boxed{225\%}
$$

of its original value.

---

# 13. Important Difference

If a value increases successively by `20%` and `20%`:

Net increase:

$$
44\%
$$

Final value:

$$
100\%+44\%
=
\boxed{144\%}
$$

Therefore:

$$
\boxed{
\text{Net increase}=44\%
}
$$

while:

$$
\boxed{
\text{Final value}=144\%\text{ of original}
}
$$

---

# 14. Multiplier Method

The safest method is to multiply the increase factors.

For `a%` increase:

$$
\boxed{
1+\frac a{100}
}
$$

For `b%` increase:

$$
\boxed{
1+\frac b{100}
}
$$

Then multiply.

---

# 15. Example — Multiplier Method

Successive increases:

`15%`, then `20%`.

Multipliers:

$$
1.15
$$

and:

$$
1.20
$$

Multiply:

$$
1.15\times1.20
=
1.38
$$

Therefore final value:

$$
138\%
$$

of original.

Net increase:

$$
\boxed{38\%}
$$

---

# 16. Example With Actual Value

Original:

$$
₹1000
$$

First increase:

`20%`

$$
1000\times1.2
=
1200
$$

Second increase:

`30%`

$$
1200\times1.3
=
1560
$$

Final:

$$
\boxed{₹1560}
$$

Net increase:

$$
1560-1000
=
560
$$

Therefore:

$$
\frac{560}{1000}\times100
=
\boxed{56\%}
$$

---

# 17. Example — Salary

Salary:

$$
₹40,000
$$

First increase:

`10%`

$$
40000\times1.1
=
44000
$$

Second increase:

`20%`

$$
44000\times1.2
=
52800
$$

Final salary:

$$
\boxed{₹52,800}
$$

Net increase:

$$
32\%
$$

---

# 18. Example — Price

Original price:

$$
₹800
$$

First increase:

`25%`

$$
800\times1.25
=
1000
$$

Second increase:

`20%`

$$
1000\times1.2
=
1200
$$

Final:

$$
\boxed{₹1200}
$$

Net increase:

$$
\boxed{50\%}
$$

---

# 19. Example — Population

Population:

$$
50,000
$$

First year growth:

`10%`

$$
50000\times1.1
=
55000
$$

Second year growth:

`20%`

$$
55000\times1.2
=
66000
$$

Final population:

$$
\boxed{66,000}
$$

Net growth:

$$
\boxed{32\%}
$$

---

# 20. Three Successive Increases

For three increases:

$$
a\%,b\%,c\%
$$

use:

$$
\boxed{
\text{Final multiplier}
=
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
\left(1+\frac c{100}\right)
}
$$

---

# 21. Example — 10%, 20%, 30%

Multipliers:

$$
1.1,\quad1.2,\quad1.3
$$

Multiply:

$$
1.1\times1.2\times1.3
=
1.716
$$

Therefore final value:

$$
171.6\%
$$

of original.

Net increase:

$$
\boxed{71.6\%}
$$

---

# 22. Example — Three 10% Increases

$$
1.1\times1.1\times1.1
$$

$$
=1.331
$$

Therefore:

$$
\boxed{33.1\%\text{ net increase}}
$$

Not:

$$
30\%
$$

---

# 23. Four Successive Increases

For four increases:

$$
a\%,b\%,c\%,d\%
$$

use:

$$
\boxed{
\prod
\left(1+\frac{x_i}{100}\right)
}
$$

This means multiply all four increase factors.

---

# 24. Example — 10% Four Times

$$
1.1^4
=
1.4641
$$

Therefore:

$$
\boxed{46.41\%\text{ net increase}}
$$

---

# 25. Same Percentage Repeatedly

If a value increases by `r%` repeatedly for `n` times:

$$
\boxed{
\text{Final}
=
\text{Original}
\left(1+\frac r{100}\right)^n
}
$$

Net increase:

$$
\boxed{
\left[
\left(1+\frac r{100}\right)^n-1
\right]\times100\%
}
$$

---

# 26. Example — 10% for 3 Years

Initial population:

$$
100
$$

Growth:

`10%` every year.

After 3 years:

$$
100(1.1)^3
$$

$$
=133.1
$$

Net increase:

$$
\boxed{33.1\%}
$$

---

# 27. Successive Increase Is Compounding

> [!important]
> Successive percentage increase behaves like **compound growth**.

Example:

A population grows `10%` every year.

It is not:

$$
10\%+10\%+10\%=30\%
$$

Instead:

$$
(1.1)^3-1
=
0.331
$$

Therefore:

$$
\boxed{33.1\%}
$$

---

# 28. Why Compounding Happens

Suppose original value is:

$$
100
$$

After first `10%`:

$$
110
$$

The second `10%` is calculated on `110`:

$$
11
$$

not on `100`.

So:

$$
110+11=121
$$

The third increase is calculated on `121`.

Therefore:

$$
121+12.1=133.1
$$

---

# 29. Important Trap

> [!warning]
> **Successive percentages are not normally added directly.**

Wrong:

$$
10\%+20\%=30\%
$$

Correct:

$$
1.1\times1.2
=
1.32
$$

Therefore:

$$
\boxed{32\%}
$$

---

# 30. Increase Then Another Increase

Suppose a price increases by:

`20%`

and then:

`10%`.

Using formula:

$$
20+10+\frac{20\times10}{100}
$$

$$
=30+2
$$

$$
=\boxed{32\%}
$$

---

# 31. Reverse Problem

A value is increased successively by:

`10%` and `20%`.

Final value:

$$
₹1320
$$

Find the original.

Combined multiplier:

$$
1.1\times1.2
=
1.32
$$

Therefore:

$$
\text{Original}
=
\frac{1320}{1.32}
$$

$$
=\boxed{₹1000}
$$

---

# 32. Reverse Formula

For successive increases:

$$
a\%,b\%
$$

and final value `F`:

$$
\boxed{
\text{Original}
=
\frac{F}
{
(1+a/100)(1+b/100)
}
}
$$

---

# 33. Successive Increase With Fractions

Suppose a value increases by:

$$
\frac15
$$

and then:

$$
\frac14
$$

Convert:

$$
\frac15=20\%
$$

$$
\frac14=25\%
$$

Net increase:

$$
20+25+\frac{20\times25}{100}
$$

$$
=45+5
$$

$$
=\boxed{50\%}
$$

---

# 34. Successive Increase With Decimal Multipliers

Suppose:

$$
A\rightarrow1.2A
$$

and then:

$$
1.5
$$

times the result.

Final:

$$
A\times1.2\times1.5
=
1.8A
$$

Therefore:

$$
\boxed{80\%\text{ net increase}}
$$

---

# 35. Comparing Two Successive Increases

Suppose:

### Case A

`10%` then `20%`

$$
1.1\times1.2=1.32
$$

Net:

$$
\boxed{32\%}
$$

### Case B

`20%` then `10%`

$$
1.2\times1.1=1.32
$$

Net:

$$
\boxed{32\%}
$$

Therefore:

> [!important]
> For multiplication-based percentage changes, **the order of successive increases does not matter**.

---

# 36. Why Order Does Not Matter

Because multiplication is commutative:

$$
a\times b=b\times a
$$

Therefore:

$$
(1+\frac a{100})(1+\frac b{100})
$$

equals:

$$
(1+\frac b{100})(1+\frac a{100})
$$

---

# 37. Three Increase Order

Even for:

`10%`, `20%`, `30%`

any order gives:

$$
1.1\times1.2\times1.3
=
1.716
$$

Therefore:

$$
\boxed{71.6\%}
$$

regardless of order.

---

# 38. Successive Increase vs Single Increase

Suppose:

`20%` then `30%`.

Net increase:

$$
56\%
$$

Therefore the two successive increases are equivalent to one:

$$
\boxed{56\%\text{ increase}}
$$

---

# 39. Equivalent Single Increase

For successive increases:

$$
a\%,b\%
$$

equivalent increase:

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

Example:

$$
15\%,25\%
$$

Equivalent:

$$
15+25+\frac{15\times25}{100}
$$

$$
=40+3.75
$$

$$
=\boxed{43.75\%}
$$

---

# 40. Comparing With Direct Increase

Suppose a quantity increases:

### Method 1

Directly by `40%`.

Multiplier:

$$
1.4
$$

### Method 2

First `20%`, then `20%`.

Multiplier:

$$
1.2\times1.2
=
1.44
$$

Therefore:

$$
\boxed{
20\%+20\%\text{ successive}
>
40\%\text{ single}
}
$$

Difference:

$$
44\%-40\%
=
\boxed{4\%}
$$

---

# 41. General Insight

For positive `a` and `b`:

$$
a+b+\frac{ab}{100}
>
a+b
$$

Therefore:

> [!important]
> Two positive successive increases always produce a result **greater than their simple sum**.

---

# 42. Small Percentage Approximation

When percentages are very small, the product term:

$$
\frac{ab}{100}
$$

may be small.

So approximately:

$$
\text{Net increase}\approx a+b
$$

But in exact aptitude problems, use the exact formula.

---

# 43. Example — 2% and 3%

Exact:

$$
2+3+\frac{2\times3}{100}
$$

$$
=5+0.06
$$

$$
=\boxed{5.06\%}
$$

Approximately:

$$
5\%
$$

But exact answer:

$$
\boxed{5.06\%}
$$

---

# 44. Percentage Increase on Percentage

Suppose a success rate increases from:

$$
40\%
$$

to:

$$
50\%
$$

The increase in percentage points is:

$$
10
$$

But percentage increase relative to `40%`:

$$
\frac{10}{40}\times100
=
\boxed{25\%}
$$

> [!warning]
> Do not confuse percentage-point increase with percentage increase.

---

# 45. Successive Increase in Salary

Salary:

$$
₹30,000
$$

First increase:

`10%`

Second increase:

`15%`

Combined multiplier:

$$
1.1\times1.15
=
1.265
$$

Final salary:

$$
30000\times1.265
=
\boxed{₹37,950}
$$

Net increase:

$$
\boxed{26.5\%}
$$

---

# 46. Successive Increase in Price

Original:

$$
₹2000
$$

Increase:

`20%`

then:

`10%`

Final:

$$
2000\times1.2\times1.1
$$

$$
=\boxed{₹2640}
$$

Net increase:

$$
\boxed{32\%}
$$

---

# 47. Successive Increase in Population

Original:

$$
100,000
$$

Growth:

`5%`

then:

`10%`

Multiplier:

$$
1.05\times1.10
=
1.155
$$

Final population:

$$
100000\times1.155
=
\boxed{115,500}
$$

Net growth:

$$
\boxed{15.5\%}
$$

---

# 48. Successive Increase in Marks

Original marks:

$$
400
$$

First increase:

`10%`

Second increase:

`5%`

Final:

$$
400\times1.1\times1.05
$$

$$
=462
$$

Net increase:

$$
\frac{62}{400}\times100
=
\boxed{15.5\%}
$$

---

# 49. Important Pattern — Increase Twice by Same Rate

If a quantity increases twice by `r%`:

$$
\boxed{
\text{Net increase}
=
2r+\frac{r^2}{100}
}
$$

Example:

`10%` twice:

$$
20+\frac{100}{100}
=
\boxed{21\%}
$$

---

# 50. Important Pattern — Three Equal Increases

If the increase is `r%` three times:

$$
\boxed{
\text{Final multiplier}
=
\left(1+\frac r{100}\right)^3
}
$$

Example:

`10%` three times:

$$
1.1^3=1.331
$$

Net:

$$
\boxed{33.1\%}
$$

---

# 51. Successive Increase and Compound Interest

Compound interest uses the same mathematical idea.

If money grows at `r%` per period for `n` periods:

$$
\boxed{
A=P\left(1+\frac r{100}\right)^n
}
$$

The same multiplier concept is used in successive percentage growth.

---

# 52. Successive Increase and Population Growth

Population growth also follows:

$$
\boxed{
P_n
=
P_0
\left(1+\frac r{100}\right)^n
}
$$

This is a common application of successive percentage increase.

---

# 53. Successive Increase and Depreciation

Depreciation is usually a decrease, but repeated depreciation also uses multiplication.

For a decrease of `r%` per period:

$$
\boxed{
V_n
=
V_0
\left(1-\frac r{100}\right)^n
}
$$

This will connect with **Successive Decrease**.

---

# 54. Formula Sheet

> [!important] Must Remember

### Two Successive Increases

$$
\boxed{
\text{Net Increase}
=
a+b+\frac{ab}{100}
}
$$

### Final Value

$$
\boxed{
F
=
P
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
}
$$

### Repeated Increase

$$
\boxed{
F
=
P
\left(1+\frac r{100}\right)^n
}
$$

### Original Value

$$
\boxed{
P
=
\frac{F}
{\left(1+\frac r{100}\right)^n}
}
$$

### Equivalent Multiplier

$$
\boxed{
M
=
\prod
\left(1+\frac{x_i}{100}\right)
}
$$

### Net Increase From Multiplier

$$
\boxed{
(M-1)\times100\%
}
$$

---

# 55. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
a\%+b\%
\text{ successively}
\Rightarrow
a+b+\frac{ab}{100}
}
$$

### Pattern 2

$$
\boxed{
10\%+20\%
\Rightarrow32\%
}
$$

### Pattern 3

$$
\boxed{
20\%+20\%
\Rightarrow44\%
}
$$

### Pattern 4

$$
\boxed{
25\%+20\%
\Rightarrow50\%
}
$$

### Pattern 5

$$
\boxed{
\text{Use multipliers when there are 3+ changes}
}
$$

### Pattern 6

$$
\boxed{
10\%\text{ three times}
\Rightarrow33.1\%
}
$$

### Pattern 7

$$
\boxed{
r\%\text{ repeated n times}
\Rightarrow
\left(1+\frac r{100}\right)^n
}
$$

### Pattern 8

> **Second percentage is applied to the already changed value.**

### Pattern 9

> **Successive increases cannot normally be added directly.**

### Pattern 10

> **Order of successive increases does not matter.**

---

# 56. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Master these first:

1. Meaning of successive increase
2. Why percentages cannot simply be added
3. Two successive increases
4. Shortcut formula
5. Multiplier method
6. Three successive increases
7. Repeated equal increases
8. Reverse successive increase
9. Ratio-based successive increase
10. Fraction-based successive increase
11. Salary growth
12. Price growth
13. Population growth
14. Compound growth connection
15. Percentage-point trap

---

# 57. Practice Checklist

- [ ] Two successive increases
- [ ] `10% + 10%`
- [ ] `10% + 20%`
- [ ] `20% + 20%`
- [ ] `20% + 30%`
- [ ] `25% + 20%`
- [ ] Three successive increases
- [ ] Four successive increases
- [ ] Same percentage repeated
- [ ] Multiplier method
- [ ] Shortcut formula
- [ ] Reverse problem
- [ ] Salary growth
- [ ] Price growth
- [ ] Population growth
- [ ] Marks growth
- [ ] Compound growth
- [ ] Percentage-point comparison

---

# 58. Related Topics

- [[03. Percentage]]
- [[Percentage Basics]]
- [[Percentage Comparison]]
- [[Percentage Increase]]
- [[Percentage Decrease]]
- [[Successive Decrease]]
- [[Net Percentage Change]]
- [[Reverse Percentage]]
- [[Population]]
- [[Salary]]
- [[Price]]

---

# 59. Quick Revision

> [!summary] One-Minute Revision

### Two Successive Increases

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

Example:

$$
10\%+20\%
=
10+20+2
=
\boxed{32\%}
$$

### Multiplier Method

$$
\boxed{
(1+\frac a{100})(1+\frac b{100})
}
$$

### Repeated Increase

$$
\boxed{
\left(1+\frac r{100}\right)^n
}
$$

### Golden Memory Trick

> **Successive increase = multiply the growth factors, not the percentages.**

### One-Line Recognition

> **When a percentage increase happens again and again, every new percentage acts on the latest value, creating a compounding effect.**