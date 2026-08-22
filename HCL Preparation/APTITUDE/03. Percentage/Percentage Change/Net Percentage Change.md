---
type: concept
subject: aptitude
topic: "Net Percentage Change"
parent: "03. Percentage > Percentage Change"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - percentage
  - net-percentage-change
  - quantitative-aptitude
wikilinks:
  - "[[03. Percentage]]"
  - "[[Percentage Increase]]"
  - "[[Percentage Decrease]]"
  - "[[Successive Increase]]"
  - "[[Successive Decrease]]"
  - "[[Reverse Percentage]]"
---

# Net Percentage Change

## 1. Core Concept

> [!summary] Definition
> **Net percentage change** tells us the overall percentage increase or decrease after one or more percentage changes are applied successively.

The safest method is:

$$
\boxed{
\text{Multiply the percentage-change multipliers}
}
$$

Then compare the final multiplier with `1`.

---

# 2. The Master Method

For every percentage change:

### Increase by `x%`

$$
\boxed{
1+\frac{x}{100}
}
$$

### Decrease by `x%`

$$
\boxed{
1-\frac{x}{100}
}
$$

Multiply all the multipliers.

Then:

$$
\boxed{
\text{Net Change}
=
(\text{Final Multiplier}-1)\times100\%
}
$$

---

# 3. Basic Example

A value increases by `20%` and then decreases by `10%`.

Increase multiplier:

$$
1.2
$$

Decrease multiplier:

$$
0.9
$$

Combined:

$$
1.2\times0.9
=
1.08
$$

Therefore:

$$
(1.08-1)\times100
=
\boxed{8\%\text{ increase}}
$$

---

# 4. Why We Need Net Percentage Change

Suppose:

- First increase = `20%`
- Second decrease = `10%`

A common mistake:

$$
20\%-10\%=10\%
$$

This happens to give the correct answer in this particular case? No—the correct answer is:

$$
\boxed{8\%\text{ increase}}
$$

The reason is that the `10%` decrease applies to the **new increased value**.

---

# 5. Step-by-Step Example

Start with:

$$
100
$$

Increase by `20%`:

$$
100\times1.2=120
$$

Decrease by `10%`:

$$
120\times0.9=108
$$

Final:

$$
108
$$

Original:

$$
100
$$

Net increase:

$$
108-100=8
$$

Therefore:

$$
\boxed{8\%}
$$

---

# 6. Master Formula

For percentage changes:

$$
x_1,x_2,x_3,\ldots,x_n
$$

where increases use `+` and decreases use `-`:

$$
\boxed{
F
=
P
\prod
\left(1\pm\frac{x_i}{100}\right)
}
$$

Then:

$$
\boxed{
\text{Net Change}
=
\left[
\prod
\left(1\pm\frac{x_i}{100}\right)-1
\right]\times100\%
}
$$

---

# 7. Two Successive Increases

For increases of `a%` and `b%`:

$$
\boxed{
\text{Net Increase}
=
a+b+\frac{ab}{100}
}
$$

Example:

$$
10\%,20\%
$$

$$
10+20+\frac{10\times20}{100}
$$

$$
=\boxed{32\%}
$$

---

# 8. Two Successive Decreases

For decreases of `a%` and `b%`:

$$
\boxed{
\text{Net Decrease}
=
a+b-\frac{ab}{100}
}
$$

Example:

$$
10\%,20\%
$$

$$
10+20-\frac{10\times20}{100}
$$

$$
=\boxed{28\%}
$$

---

# 9. Increase Followed by Decrease

For:

- `a%` increase
- `b%` decrease

use:

$$
\boxed{
\text{Final Multiplier}
=
\left(1+\frac a{100}\right)
\left(1-\frac b{100}\right)
}
$$

Expanding:

$$
1+\frac a{100}
-\frac b{100}
-\frac{ab}{10000}
$$

Therefore:

$$
\boxed{
\text{Net Change}
=
a-b-\frac{ab}{100}
}
$$

if the result is positive.

If the result is negative, it represents a decrease.

---

# 10. Example — 20% Increase, 10% Decrease

$$
20-10-\frac{20\times10}{100}
$$

$$
=10-2
$$

$$
=\boxed{8\%\text{ increase}}
$$

---

# 11. Example — 30% Increase, 20% Decrease

$$
30-20-\frac{30\times20}{100}
$$

$$
=10-6
$$

$$
=\boxed{4\%\text{ increase}}
$$

---

# 12. Example — 20% Increase, 30% Decrease

$$
20-30-\frac{20\times30}{100}
$$

$$
=-10-6
$$

$$
=\boxed{16\%\text{ decrease}}
$$

---

# 13. Decrease Followed by Increase

For:

- `a%` decrease
- `b%` increase

use:

$$
\boxed{
\left(1-\frac a{100}\right)
\left(1+\frac b{100}\right)
}
$$

Example:

`20% decrease`, then `30% increase`:

$$
0.8\times1.3
=
1.04
$$

Therefore:

$$
\boxed{4\%\text{ increase}}
$$

---

# 14. Important Insight — Order

For pure percentage changes applied multiplicatively:

$$
(1+\frac a{100})(1-\frac b{100})
$$

and:

$$
(1-\frac b{100})(1+\frac a{100})
$$

are equal.

Therefore:

> [!important]
> If the same percentage changes are applied to the same quantity, **their order does not affect the final multiplier**.

---

# 15. Equal Increase and Decrease

Suppose a value:

- increases by `r%`
- decreases by `r%`

Multiplier:

$$
\left(1+\frac r{100}\right)
\left(1-\frac r{100}\right)
$$

Using:

$$
(a+b)(a-b)=a^2-b^2
$$

we get:

$$
1-\frac{r^2}{10000}
$$

Therefore net change:

$$
\boxed{
\frac{r^2}{100}\%\text{ decrease}
}
$$

---

# 16. Example — 20% Increase and 20% Decrease

$$
\frac{20^2}{100}
=
\boxed{4\%\text{ decrease}}
$$

Check:

$$
100\rightarrow120\rightarrow96
$$

Therefore:

$$
\boxed{4\%\text{ decrease}}
$$

---

# 17. Example — 10% Increase and 10% Decrease

$$
\frac{10^2}{100}
=
\boxed{1\%\text{ decrease}}
$$

Check:

$$
100\rightarrow110\rightarrow99
$$

---

# 18. Example — 50% Increase and 50% Decrease

$$
\frac{50^2}{100}
=
\boxed{25\%\text{ decrease}}
$$

Check:

$$
100\rightarrow150\rightarrow75
$$

---

# 19. Net Change From Multipliers

This is the most reliable technique.

Suppose:

- increase `25%`
- decrease `20%`
- increase `10%`

Multipliers:

$$
1.25,\quad0.8,\quad1.1
$$

Multiply:

$$
1.25\times0.8\times1.1
$$

$$
=1.1
$$

Therefore:

$$
\boxed{10\%\text{ net increase}}
$$

---

# 20. Example With Actual Value

Original:

$$
₹10,000
$$

Changes:

- `20%` increase
- `10%` decrease
- `25%` increase

Final:

$$
10000\times1.2\times0.9\times1.25
$$

$$
=13500
$$

Therefore:

$$
\boxed{₹13,500}
$$

Net increase:

$$
\frac{13500-10000}{10000}\times100
=
\boxed{35\%}
$$

---

# 21. Three Successive Increases

For:

`10%`, `20%`, `30%`

$$
1.1\times1.2\times1.3
=
1.716
$$

Therefore:

$$
\boxed{71.6\%\text{ net increase}}
$$

---

# 22. Three Successive Decreases

For:

`10%`, `20%`, `30%`

$$
0.9\times0.8\times0.7
=
0.504
$$

Therefore:

$$
1-0.504
=
0.496
$$

So:

$$
\boxed{49.6\%\text{ net decrease}}
$$

---

# 23. Repeated Increase

If a quantity increases by `r%` for `n` periods:

$$
\boxed{
F=P\left(1+\frac r{100}\right)^n
}
$$

Net percentage increase:

$$
\boxed{
\left[
\left(1+\frac r{100}\right)^n-1
\right]\times100\%
}
$$

---

# 24. Example — 10% Increase for 3 Periods

$$
(1.1)^3
=
1.331
$$

Therefore:

$$
\boxed{33.1\%\text{ net increase}}
$$

---

# 25. Repeated Decrease

If a quantity decreases by `r%` for `n` periods:

$$
\boxed{
F=P\left(1-\frac r{100}\right)^n
}
$$

Net percentage decrease:

$$
\boxed{
\left[
1-\left(1-\frac r{100}\right)^n
\right]\times100\%
}
$$

---

# 26. Example — 10% Decrease for 3 Periods

$$
(0.9)^3
=
0.729
$$

Therefore:

$$
1-0.729
=
0.271
$$

So:

$$
\boxed{27.1\%\text{ net decrease}}
$$

---

# 27. Net Percentage Change From Initial and Final Values

If only the original and final values are given:

$$
\boxed{
\text{Net Change}
=
\frac{\text{Final}-\text{Original}}
{\text{Original}}
\times100
}
$$

If positive:

> Increase.

If negative:

> Decrease.

---

# 28. Example

Original:

$$
500
$$

Final:

$$
575
$$

Net change:

$$
\frac{575-500}{500}\times100
$$

$$
=\boxed{15\%\text{ increase}}
$$

---

# 29. Example — Decrease

Original:

$$
800
$$

Final:

$$
680
$$

Net change:

$$
\frac{680-800}{800}\times100
$$

$$
=-15\%
$$

Therefore:

$$
\boxed{15\%\text{ decrease}}
$$

---

# 30. Percentage Change vs Absolute Change

Suppose:

Original:

$$
1000
$$

Final:

$$
1200
$$

Absolute change:

$$
200
$$

Net percentage change:

$$
\frac{200}{1000}\times100
=
\boxed{20\%}
$$

Therefore:

$$
\boxed{
\text{Absolute change}=200
}
$$

while:

$$
\boxed{
\text{Percentage change}=20\%
}
$$

---

# 31. Net Change Using Ratio

Suppose:

$$
\text{Final}:\text{Original}=6:5
$$

Then:

$$
\frac65=1.2
$$

Therefore:

$$
\boxed{20\%\text{ net increase}}
$$

---

# 32. Ratio for Decrease

Suppose:

$$
\text{Final}:\text{Original}=4:5
$$

Then:

$$
\frac45=0.8
$$

Therefore:

$$
\boxed{20\%\text{ net decrease}}
$$

---

# 33. Net Change Using Fraction

Suppose:

$$
\text{Final}=\frac54\text{ Original}
$$

Then:

$$
\frac54-1
=
\frac14
$$

Therefore:

$$
\boxed{25\%\text{ increase}}
$$

---

# 34. Net Change Using Decimal

Suppose:

$$
\text{Final}=0.72\text{ Original}
$$

Then:

$$
1-0.72
=
0.28
$$

Therefore:

$$
\boxed{28\%\text{ decrease}}
$$

---

# 35. Reverse Net Percentage Change

Suppose a value undergoes a net increase of `20%` and becomes `600`.

Final multiplier:

$$
1.2
$$

Original:

$$
\frac{600}{1.2}
=
\boxed{500}
$$

---

# 36. Reverse Net Decrease

Suppose a value undergoes a net decrease of `20%` and becomes `400`.

Final multiplier:

$$
0.8
$$

Original:

$$
\frac{400}{0.8}
=
\boxed{500}
$$

---

# 37. Net Change and Successive Increase

If the changes are all increases:

$$
\boxed{
\text{Net Change}
=
\prod(1+\frac{x_i}{100})-1
}
$$

Example:

`10%`, `20%`:

$$
1.1\times1.2-1
=
0.32
$$

Therefore:

$$
\boxed{32\%}
$$

---

# 38. Net Change and Successive Decrease

If all changes are decreases:

$$
\boxed{
\text{Net Change}
=
1-\prod(1-\frac{x_i}{100})
}
$$

Example:

`10%`, `20%`:

$$
1-0.9\times0.8
$$

$$
=1-0.72
$$

$$
=\boxed{28\%}
$$

---

# 39. Mixed Percentage Changes

Mixed changes include both increases and decreases.

Example:

- `20%` increase
- `10%` decrease
- `15%` increase
- `5%` decrease

Multipliers:

$$
1.2,\quad0.9,\quad1.15,\quad0.95
$$

Multiply:

$$
1.2\times0.9\times1.15\times0.95
$$

$$
=1.18035
$$

Therefore:

$$
\boxed{18.035\%\text{ net increase}}
$$

---

# 40. The Universal Multiplier Method

> [!tip] Best Exam Method

For every change:

### Increase

$$
x\%\rightarrow1+\frac{x}{100}
$$

### Decrease

$$
x\%\rightarrow1-\frac{x}{100}
$$

Then:

$$
\boxed{
M=M_1M_2M_3\cdots M_n
}
$$

Finally:

### If `M > 1`

$$
\boxed{
(M-1)\times100\%\text{ increase}
}
$$

### If `M < 1`

$$
\boxed{
(1-M)\times100\%\text{ decrease}
}
$$

---

# 41. Important Trap — Adding Mixed Percentages

Suppose:

- `30%` increase
- `20%` decrease

Wrong:

$$
30-20=10\%
$$

Correct:

$$
1.3\times0.8
=
1.04
$$

Therefore:

$$
\boxed{4\%\text{ increase}}
$$

---

# 42. Important Trap — Equal Changes

Suppose:

`30%` increase followed by `30%` decrease.

Wrong:

$$
30-30=0\%
$$

Correct:

$$
1.3\times0.7
=
0.91
$$

Therefore:

$$
\boxed{9\%\text{ decrease}}
$$

---

# 43. Important Trap — Final Percentage vs Net Change

Suppose:

$$
M=1.32
$$

This means final value is:

$$
\boxed{132\%\text{ of original}}
$$

But the net increase is:

$$
132-100
=
\boxed{32\%}
$$

Do not confuse these.

---

# 44. Percentage Points

Suppose a success rate changes:

$$
40\%\rightarrow50\%
$$

Percentage-point change:

$$
\boxed{10\text{ percentage points}}
$$

Net percentage increase:

$$
\frac{50-40}{40}\times100
=
\boxed{25\%}
$$

Therefore:

$$
\boxed{
10\text{ percentage points}
\ne
25\%\text{ increase}
}
$$

---

# 45. Net Percentage Change in Salary

Salary:

$$
₹40,000
$$

First increase:

`10%`

Second decrease:

`5%`

Final:

$$
40000\times1.1\times0.95
$$

$$
=41800
$$

Net:

$$
\frac{41800-40000}{40000}\times100
=
\boxed{4.5\%\text{ increase}}
$$

---

# 46. Net Percentage Change in Price

Price:

$$
₹1000
$$

Increase:

`20%`

Decrease:

`25%`

Final:

$$
1000\times1.2\times0.75
=
900
$$

Therefore:

$$
\boxed{10\%\text{ decrease}}
$$

---

# 47. Net Percentage Change in Population

Population:

$$
80,000
$$

Increase:

`10%`

then decrease:

`10%`

Final:

$$
80000\times1.1\times0.9
$$

$$
=79200
$$

Net:

$$
\boxed{1\%\text{ decrease}}
$$

---

# 48. Net Percentage Change in Marks

Marks:

$$
500
$$

Increase:

`20%`

then decrease:

`10%`

Final:

$$
500\times1.2\times0.9
=
540
$$

Net:

$$
\boxed{8\%\text{ increase}}
$$

---

# 49. Fixed Expenditure and Net Change

If price changes and expenditure remains constant, consumption changes inversely.

If price multiplier is:

$$
M
$$

then consumption multiplier is:

$$
\boxed{\frac1M}
$$

This is a high-value aptitude pattern.

Example:

Price increases `20%`:

$$
M=1.2
$$

Consumption multiplier:

$$
\frac1{1.2}
=
\frac56
$$

Therefore consumption decreases by:

$$
1-\frac56
=
\frac16
$$

$$
=\boxed{16\frac23\%}
$$

---

# 50. Net Change and Reciprocal Relationship

If:

$$
A=1.2B
$$

then:

$$
B=\frac{A}{1.2}
=
\frac56A
$$

Therefore:

A is `20%` more than B.

But B is:

$$
\boxed{16\frac23\%}
$$

less than A.

---

# 51. Net Change in Area

If the side of a square increases by `10%`, each side becomes:

$$
1.1
$$

times the original.

Area multiplier:

$$
1.1^2
=
1.21
$$

Therefore area increases by:

$$
\boxed{21\%}
$$

This is an important application of successive percentage multiplication.

---

# 52. Net Change in Volume

If all three dimensions of a cuboid increase by `10%`:

Volume multiplier:

$$
1.1^3
=
1.331
$$

Therefore volume increases by:

$$
\boxed{33.1\%}
$$

---

# 53. Net Change in Square Area

If side decreases by `20%`:

Side multiplier:

$$
0.8
$$

Area multiplier:

$$
0.8^2
=
0.64
$$

Therefore area decreases by:

$$
\boxed{36\%}
$$

---

# 54. Net Change in Cube Volume

If side decreases by `20%`:

Volume multiplier:

$$
0.8^3
=
0.512
$$

Therefore:

$$
1-0.512
=
\boxed{48.8\%\text{ decrease}}
$$

---

# 55. General Dimension Pattern

If every dimension of an `n`-dimensional quantity changes by `r%`:

### Increase

$$
\boxed{
\left(1+\frac r{100}\right)^n
}
$$

### Decrease

$$
\boxed{
\left(1-\frac r{100}\right)^n
}
$$

This is useful in geometry-based aptitude questions.

---

# 56. Formula Sheet

> [!important] Must Remember

### Universal Multiplier

$$
\boxed{
\text{Increase }x\%\rightarrow1+\frac{x}{100}
}
$$

$$
\boxed{
\text{Decrease }x\%\rightarrow1-\frac{x}{100}
}
$$

### Net Change

$$
\boxed{
(M-1)\times100\%
}
$$

where `M` is the final multiplier.

### Two Increases

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

### Two Decreases

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

### Increase Then Decrease

$$
\boxed{
a-b-\frac{ab}{100}
}
$$

### Repeated Increase

$$
\boxed{
\left(1+\frac r{100}\right)^n
}
$$

### Repeated Decrease

$$
\boxed{
\left(1-\frac r{100}\right)^n
}
$$

### Equal Increase and Decrease

$$
\boxed{
\frac{r^2}{100}\%\text{ decrease}
}
$$

---

# 57. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Convert every change into a multiplier}
}
$$

### Pattern 2

$$
\boxed{
\text{Multiply all multipliers}
}
$$

### Pattern 3

$$
\boxed{
M>1\Rightarrow(M-1)100\%\text{ increase}
}
$$

### Pattern 4

$$
\boxed{
M<1\Rightarrow(1-M)100\%\text{ decrease}
}
$$

### Pattern 5

$$
\boxed{
20\%\uparrow,\ 10\%\downarrow
\Rightarrow8\%\uparrow
}
$$

### Pattern 6

$$
\boxed{
20\%\downarrow,\ 30\%\uparrow
\Rightarrow4\%\uparrow
}
$$

### Pattern 7

$$
\boxed{
20\%\uparrow,\ 20\%\downarrow
\Rightarrow4\%\downarrow
}
$$

### Pattern 8

$$
\boxed{
10\%\uparrow,\ 10\%\downarrow
\Rightarrow1\%\downarrow
}
$$

### Pattern 9

$$
\boxed{
10\%\uparrow\text{ three times}
\Rightarrow33.1\%\uparrow
}
$$

### Pattern 10

> **Never add successive percentage changes blindly. Multiply the factors.**

---

# 58. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Master these first:

1. Meaning of net percentage change
2. Universal multiplier method
3. Two successive increases
4. Two successive decreases
5. Increase + decrease
6. Decrease + increase
7. Equal increase/decrease
8. Three or more percentage changes
9. Repeated percentage change
10. Reverse net change
11. Ratio-based net change
12. Fraction-based net change
13. Salary applications
14. Price applications
15. Population applications
16. Area and volume applications
17. Fixed expenditure applications
18. Percentage-point traps

---

# 59. Practice Checklist

- [ ] Find net increase
- [ ] Find net decrease
- [ ] Mixed increase/decrease
- [ ] Two successive increases
- [ ] Two successive decreases
- [ ] Increase + decrease
- [ ] Decrease + increase
- [ ] Equal increase/decrease
- [ ] Three changes
- [ ] Four changes
- [ ] Repeated increase
- [ ] Repeated decrease
- [ ] Reverse net change
- [ ] Ratio method
- [ ] Fraction method
- [ ] Salary
- [ ] Price
- [ ] Population
- [ ] Marks
- [ ] Area
- [ ] Volume
- [ ] Fixed expenditure
- [ ] Percentage points

---

# 60. Related Topics

- [[03. Percentage]]
- [[Percentage Basics]]
- [[Percentage Comparison]]
- [[Percentage Increase]]
- [[Percentage Decrease]]
- [[Successive Increase]]
- [[Successive Decrease]]
- [[Reverse Percentage]]
- [[Percentage Error]]
- [[Percentage Difference]]
- [[Mixed Percentage Problems]]

---

# 61. Quick Revision

> [!summary] One-Minute Revision

### Universal Rule

$$
\boxed{
\text{Increase }x\%\rightarrow1+\frac{x}{100}
}
$$

$$
\boxed{
\text{Decrease }x\%\rightarrow1-\frac{x}{100}
}
$$

Then multiply.

### Example

`20% increase → 10% decrease`

$$
1.2\times0.9
=
1.08
$$

Therefore:

$$
\boxed{8\%\text{ net increase}}
$$

### Equal Increase and Decrease

$$
\boxed{
r\%\uparrow+r\%\downarrow
\Rightarrow
\frac{r^2}{100}\%\downarrow
}
$$

### Golden Memory Trick

> **Convert → Multiply → Compare with 1.**

### One-Line Recognition

> **For any complicated percentage-change question, stop thinking in percentages and think in multipliers.**