---
type: concept
subject: aptitude
topic: "Successive Decrease"
parent: "03. Percentage > Percentage Change"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - percentage
  - successive-decrease
  - quantitative-aptitude
wikilinks:
  - "[[03. Percentage]]"
  - "[[Percentage Increase]]"
  - "[[Percentage Decrease]]"
  - "[[Successive Increase]]"
  - "[[Net Percentage Change]]"
  - "[[Reverse Percentage]]"
---

# Successive Decrease

## 1. Core Concept

> [!summary] Definition
> **Successive decrease** means a quantity is decreased by a percentage and then decreased again by another percentage.
>
> The second decrease is calculated on the **already decreased value**, not the original value.

This is the key idea.

---

# 2. Why We Cannot Simply Add Percentages

Suppose a quantity decreases by:

- `10%`
- then `20%`

A common mistake is:

$$
10\%+20\%=30\%
$$

This is **wrong**.

The second `20%` is calculated on the value remaining after the first decrease.

---

# 3. Basic Example

Start with:

$$
100
$$

First decrease = `10%`

$$
100\times0.9
=
90
$$

Second decrease = `20%`

$$
90\times0.8
=
72
$$

Final value:

$$
\boxed{72}
$$

Total decrease:

$$
100-72=28
$$

Therefore:

$$
\boxed{28\%}
$$

---

# 4. Main Formula

For successive decreases of `a%` and `b%`:

$$
\boxed{
\text{Final}
=
\text{Original}
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
}
$$

---

# 5. Net Successive Decrease Formula

For two successive decreases:

$$
\boxed{
\text{Net Decrease}
=
a+b-\frac{ab}{100}
}
$$

This is one of the most important aptitude shortcuts.

---

# 6. Derivation

Start with:

$$
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
$$

Expand:

$$
1-\frac a{100}-\frac b{100}
+\frac{ab}{10000}
$$

Therefore:

$$
=
1-
\left(
\frac{a+b}{100}
-
\frac{ab}{10000}
\right)
$$

Hence:

$$
\boxed{
\text{Net Decrease}
=
a+b-\frac{ab}{100}
}
$$

---

# 7. Example — 10% and 20%

Using the shortcut:

$$
10+20-\frac{10\times20}{100}
$$

$$
=30-2
$$

$$
=\boxed{28\%}
$$

---

# 8. Example — 20% and 30%

$$
20+30-\frac{20\times30}{100}
$$

$$
=50-6
$$

$$
=\boxed{44\%}
$$

---

# 9. Example — 25% and 20%

$$
25+20-\frac{25\times20}{100}
$$

$$
=45-5
$$

$$
=\boxed{40\%}
$$

---

# 10. Example — 10% and 10%

$$
10+10-\frac{10\times10}{100}
$$

$$
=20-1
$$

$$
=\boxed{19\%}
$$

Therefore:

> Two successive `10%` decreases produce a `19%` decrease, not `20%`.

---

# 11. Example — 20% and 20%

$$
20+20-\frac{20\times20}{100}
$$

$$
=40-4
$$

$$
=\boxed{36\%}
$$

Therefore:

$$
\boxed{
20\%\text{ decrease twice}=36\%\text{ net decrease}
}
$$

---

# 12. Multiplier Method

The safest method is to multiply the decrease factors.

For `a%` decrease:

$$
\boxed{
1-\frac a{100}
}
$$

For `b%` decrease:

$$
\boxed{
1-\frac b{100}
}
$$

Then multiply.

---

# 13. Example — 15% and 20%

Multipliers:

$$
0.85
$$

and:

$$
0.80
$$

Multiply:

$$
0.85\times0.80
=
0.68
$$

Therefore final value is:

$$
68\%
$$

of original.

Net decrease:

$$
100\%-68\%
=
\boxed{32\%}
$$

---

# 14. Example With Actual Value

Original:

$$
₹1000
$$

First decrease:

`20%`

$$
1000\times0.8
=
800
$$

Second decrease:

`30%`

$$
800\times0.7
=
560
$$

Final:

$$
\boxed{₹560}
$$

Net decrease:

$$
1000-560
=
440
$$

Therefore:

$$
\boxed{44\%}
$$

---

# 15. Important Decrease Multipliers

| Decrease | Remaining Multiplier |
|---:|---:|
| `5%` | `0.95` |
| `10%` | `0.90` |
| `20%` | `0.80` |
| `25%` | `0.75` |
| `30%` | `0.70` |
| `40%` | `0.60` |
| `50%` | `0.50` |
| `60%` | `0.40` |
| `75%` | `0.25` |
| `90%` | `0.10` |

---

# 16. Decrease Multipliers as Fractions

| Decrease | Remaining Fraction |
|---:|---:|
| `10%` | `9/10` |
| `20%` | `4/5` |
| `25%` | `3/4` |
| `30%` | `7/10` |
| `40%` | `3/5` |
| `50%` | `1/2` |
| `60%` | `2/5` |
| `75%` | `1/4` |

> [!tip]
> Fraction multipliers make many aptitude calculations much faster.

---

# 17. Example — Fraction Method

A quantity decreases successively by:

`20%` and `25%`.

Convert:

$$
20\%=\frac45\text{ remaining}
$$

$$
25\%=\frac34\text{ remaining}
$$

Therefore:

$$
\frac45\times\frac34
=
\frac35
$$

So `60%` remains.

Therefore decrease:

$$
100\%-60\%
=
\boxed{40\%}
$$

---

# 18. Finding Final Value

For successive decreases:

$$
a\%,b\%
$$

use:

$$
\boxed{
F
=
P
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
}
$$

where:

- `P` = original value
- `F` = final value

---

# 19. Example — Price

Original price:

$$
₹2000
$$

First decrease:

`10%`

Second decrease:

`20%`

Final:

$$
2000\times0.9\times0.8
$$

$$
=\boxed{₹1440}
$$

Net decrease:

$$
\frac{2000-1440}{2000}\times100
=
\boxed{28\%}
$$

---

# 20. Example — Salary

Original salary:

$$
₹50,000
$$

First decrease:

`10%`

Second decrease:

`20%`

Final:

$$
50000\times0.9\times0.8
$$

$$
=\boxed{₹36,000}
$$

Net decrease:

$$
\boxed{28\%}
$$

---

# 21. Example — Population

Original population:

$$
100,000
$$

First decrease:

`10%`

Second decrease:

`20%`

Final:

$$
100000\times0.9\times0.8
$$

$$
=\boxed{72,000}
$$

Net decrease:

$$
\boxed{28\%}
$$

---

# 22. Example — Production

Original production:

$$
5000
$$

First decrease:

`20%`

Second decrease:

`10%`

Final:

$$
5000\times0.8\times0.9
$$

$$
=\boxed{3600}
$$

Net decrease:

$$
\boxed{28\%}
$$

---

# 23. Three Successive Decreases

For three decreases:

$$
a\%,b\%,c\%
$$

use:

$$
\boxed{
F=
P
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
\left(1-\frac c{100}\right)
}
$$

---

# 24. Example — 10%, 20%, 30%

Multipliers:

$$
0.9,\quad0.8,\quad0.7
$$

Multiply:

$$
0.9\times0.8\times0.7
=
0.504
$$

Therefore:

$$
50.4\%
$$

of the original remains.

Net decrease:

$$
100-50.4
=
\boxed{49.6\%}
$$

---

# 25. Example — Three 10% Decreases

$$
0.9^3
=
0.729
$$

Therefore final value:

$$
72.9\%
$$

of original.

Net decrease:

$$
100-72.9
=
\boxed{27.1\%}
$$

Not:

$$
30\%
$$

---

# 26. Repeated Decrease

If a quantity decreases by `r%` repeatedly for `n` times:

$$
\boxed{
F
=
P
\left(1-\frac r{100}\right)^n
}
$$

Net decrease:

$$
\boxed{
\left[
1-
\left(1-\frac r{100}\right)^n
\right]\times100\%
}
$$

---

# 27. Example — 10% Decrease for 3 Years

Initial:

$$
100
$$

After 3 years:

$$
100(0.9)^3
$$

$$
=72.9
$$

Net decrease:

$$
100-72.9
=
\boxed{27.1\%}
$$

---

# 28. Successive Decrease Is Compounding

> [!important]
> Repeated percentage decreases behave like **compound depreciation**.

Example:

A machine loses `10%` of its value every year.

It does not lose:

$$
10\%+10\%+10\%=30\%
$$

Instead:

$$
(0.9)^3
=
0.729
$$

So:

$$
\boxed{27.1\%\text{ total decrease}}
$$

---

# 29. Why Compounding Happens

Start with:

$$
100
$$

First `10%` decrease:

$$
100\rightarrow90
$$

Second `10%` decrease:

$$
90\rightarrow81
$$

Third `10%` decrease:

$$
81\rightarrow72.9
$$

The base keeps changing.

---

# 30. Important Trap

> [!warning]
> Never simply add successive decreases.

Wrong:

$$
10\%+20\%=30\%
$$

Correct:

$$
0.9\times0.8
=
0.72
$$

Therefore:

$$
\boxed{28\%\text{ decrease}}
$$

---

# 31. Successive Decrease vs Single Decrease

Suppose:

`20%` then `30%`.

Net decrease:

$$
44\%
$$

Therefore these two decreases are equivalent to one:

$$
\boxed{44\%\text{ decrease}}
$$

---

# 32. Equivalent Single Decrease

For two successive decreases:

$$
a\%,b\%
$$

equivalent decrease:

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

Example:

$$
15\%,25\%
$$

Equivalent decrease:

$$
15+25-\frac{15\times25}{100}
$$

$$
=40-3.75
$$

$$
=\boxed{36.25\%}
$$

---

# 33. Comparing Direct and Successive Decrease

Suppose:

### Direct decrease

`40%`

Remaining:

$$
60\%
$$

### Successive decrease

`20%`, then `20%`

Remaining:

$$
0.8\times0.8
=
64\%
$$

Therefore net decrease:

$$
36\%
$$

So:

$$
\boxed{
20\%+20\%\text{ successive}=36\%
}
$$

while:

$$
\boxed{
40\%\text{ single}=40\%
}
$$

The successive decrease is smaller.

---

# 34. General Insight

For positive `a` and `b`:

$$
a+b-\frac{ab}{100}
<
a+b
$$

Therefore:

> [!important]
> Two positive successive decreases always produce a result **smaller than their simple sum**.

---

# 35. Same Percentage Repeated Twice

If a quantity decreases twice by `r%`:

$$
\boxed{
\text{Net Decrease}
=
2r-\frac{r^2}{100}
}
$$

Example:

`20%` twice:

$$
40-\frac{400}{100}
$$

$$
=40-4
$$

$$
=\boxed{36\%}
$$

---

# 36. Three Equal Decreases

If a quantity decreases by `r%` three times:

$$
\boxed{
F
=
P\left(1-\frac r{100}\right)^3
}
$$

Example:

`10%` three times:

$$
(0.9)^3
=
0.729
$$

Net decrease:

$$
\boxed{27.1\%}
$$

---

# 37. Four Equal Decreases

For `10%` decrease four times:

$$
(0.9)^4
=
0.6561
$$

Therefore:

$$
100-65.61
=
\boxed{34.39\%}
$$

net decrease.

---

# 38. Reverse Problem

A quantity is decreased successively by:

`10%` and `20%`.

Final value:

$$
₹720
$$

Find the original.

Combined remaining multiplier:

$$
0.9\times0.8
=
0.72
$$

Therefore:

$$
\text{Original}
=
\frac{720}{0.72}
$$

$$
=\boxed{₹1000}
$$

---

# 39. Reverse Formula

For successive decreases:

$$
a\%,b\%
$$

and final value `F`:

$$
\boxed{
P
=
\frac{F}
{
(1-a/100)(1-b/100)
}
}
$$

---

# 40. Successive Decrease With Fractions

Suppose a quantity decreases by:

$$
\frac15
$$

and then:

$$
\frac14
$$

Remaining after first:

$$
1-\frac15
=
\frac45
$$

Remaining after second:

$$
1-\frac14
=
\frac34
$$

Combined:

$$
\frac45\times\frac34
=
\frac35
$$

Therefore:

$$
60\%
$$

remains.

Net decrease:

$$
\boxed{40\%}
$$

---

# 41. Successive Decrease With Decimal Multipliers

Suppose:

$$
A\rightarrow0.8A
$$

then:

$$
0.75
$$

times the result.

Final:

$$
A\times0.8\times0.75
$$

$$
=0.6A
$$

Therefore:

$$
60\%
$$

remains.

Net decrease:

$$
\boxed{40\%}
$$

---

# 42. Order of Successive Decreases

Suppose decreases are:

`10%` and `20%`.

Case 1:

$$
0.9\times0.8
=
0.72
$$

Case 2:

$$
0.8\times0.9
=
0.72
$$

Same result.

Therefore:

> [!important]
> The order of successive decreases does not matter.

This is because multiplication is commutative.

---

# 43. Three Decrease Order

For:

`10%`, `20%`, `30%`

$$
0.9\times0.8\times0.7
=
0.504
$$

Any order produces the same multiplier.

Therefore net decrease:

$$
\boxed{49.6\%}
$$

---

# 44. Decrease Followed by Increase

Suppose:

- decrease `20%`
- then increase `20%`

Multipliers:

$$
0.8\times1.2
=
0.96
$$

Final value:

$$
96\%
$$

of original.

Therefore:

$$
\boxed{4\%\text{ net decrease}}
$$

---

# 45. Increase Followed by Decrease

Suppose:

- increase `20%`
- then decrease `20%`

Multipliers:

$$
1.2\times0.8
=
0.96
$$

Again:

$$
\boxed{4\%\text{ net decrease}}
$$

The order does not matter for these multiplicative changes.

---

# 46. Equal Increase and Decrease

For an increase of `r%` followed by a decrease of `r%`:

$$
(1+\frac r{100})(1-\frac r{100})
$$

Using:

$$
(a+b)(a-b)=a^2-b^2
$$

we get:

$$
1-\frac{r^2}{10000}
$$

Therefore net decrease:

$$
\boxed{
\frac{r^2}{100}\%
}
$$

Example:

`20%` increase and `20%` decrease:

$$
\frac{20^2}{100}
=
\boxed{4\%}
$$

---

# 47. Reverse of Successive Decrease

Suppose a value is reduced by `20%` twice.

Remaining:

$$
0.8\times0.8
=
0.64
$$

Therefore:

$$
64\%
$$

remains.

Net decrease:

$$
\boxed{36\%}
$$

If the final value is known, divide by `0.64` to recover the original.

---

# 48. Fixed Expenditure Application

Suppose price decreases successively by:

`10%` and `20%`.

Price multiplier:

$$
0.9\times0.8
=
0.72
$$

Price becomes `72%` of original.

If expenditure remains constant:

$$
\text{Consumption multiplier}
=
\frac1{0.72}
$$

So consumption increases by:

$$
\left(\frac1{0.72}-1\right)\times100
$$

$$
=\boxed{38.89\%}
$$

approximately.

---

# 49. Depreciation Application

A machine worth:

$$
₹100,000
$$

depreciates by `10%` every year for 2 years.

Final:

$$
100000(0.9)^2
$$

$$
=\boxed{₹81,000}
$$

Total depreciation:

$$
100000-81000
=
₹19,000
$$

Percentage depreciation:

$$
\boxed{19\%}
$$

---

# 50. Population Decline

Population:

$$
100,000
$$

decreases by `5%` annually for 3 years.

Final:

$$
100000(0.95)^3
$$

$$
=85737.5
$$

Approximately:

$$
\boxed{85,738}
$$

Net decrease:

$$
\boxed{14.2625\%}
$$

---

# 51. Important Comparison

### Successive Increase

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

### Successive Decrease

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

Memorize this pair.

---

# 52. Increase vs Decrease Table

| Situation | Formula |
|---|---|
| Two successive increases | `a + b + ab/100` |
| Two successive decreases | `a + b - ab/100` |
| Increase then decrease | Use multipliers |
| Same increase and decrease | `r²/100` net decrease |
| Repeated increase | `(1 + r/100)^n` |
| Repeated decrease | `(1 - r/100)^n` |

---

# 53. Formula Sheet

> [!important] Must Remember

### Two Successive Decreases

$$
\boxed{
\text{Net Decrease}
=
a+b-\frac{ab}{100}
}
$$

### Final Value

$$
\boxed{
F
=
P
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
}
$$

### Repeated Decrease

$$
\boxed{
F
=
P
\left(1-\frac r{100}\right)^n
}
$$

### Original Value

$$
\boxed{
P
=
\frac{F}
{\left(1-\frac r{100}\right)^n}
}
$$

### Net Decrease From Multiplier

$$
\boxed{
(1-M)\times100\%
}
$$

where `M` is the final multiplier.

### Equal Increase and Decrease

$$
\boxed{
r\%\text{ increase followed by }r\%\text{ decrease}
=
\frac{r^2}{100}\%\text{ net decrease}
}
$$

---

# 54. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
a\%+b\%\text{ successively}
\Rightarrow
a+b-\frac{ab}{100}
}
$$

### Pattern 2

$$
\boxed{
10\%+20\%
\Rightarrow28\%\text{ decrease}
}
$$

### Pattern 3

$$
\boxed{
20\%+20\%
\Rightarrow36\%\text{ decrease}
}
$$

### Pattern 4

$$
\boxed{
25\%+20\%
\Rightarrow40\%\text{ decrease}
}
$$

### Pattern 5

$$
\boxed{
10\%\text{ three times}
\Rightarrow27.1\%\text{ decrease}
}
$$

### Pattern 6

$$
\boxed{
r\%\text{ repeated n times}
\Rightarrow
\left(1-\frac r{100}\right)^n
}
$$

### Pattern 7

$$
\boxed{
r\%\text{ increase then }r\%\text{ decrease}
\Rightarrow
\frac{r^2}{100}\%\text{ decrease}
}
$$

### Pattern 8

> **The second decrease acts on the already reduced value.**

### Pattern 9

> **Successive decreases cannot normally be added directly.**

### Pattern 10

> **Order of successive decreases does not matter.**

---

# 55. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Master these first:

1. Meaning of successive decrease
2. Why percentages cannot simply be added
3. Two successive decreases
4. Shortcut formula
5. Multiplier method
6. Three successive decreases
7. Repeated equal decreases
8. Reverse successive decrease
9. Ratio-based decrease
10. Fraction-based decrease
11. Depreciation
12. Population decline
13. Price reduction
14. Salary reduction
15. Fixed expenditure
16. Increase + decrease combination

---

# 56. Practice Checklist

- [ ] Two successive decreases
- [ ] `10% + 10%`
- [ ] `10% + 20%`
- [ ] `20% + 20%`
- [ ] `20% + 30%`
- [ ] `25% + 20%`
- [ ] Three successive decreases
- [ ] Four successive decreases
- [ ] Same percentage repeated
- [ ] Multiplier method
- [ ] Shortcut formula
- [ ] Reverse problem
- [ ] Depreciation
- [ ] Population decline
- [ ] Price reduction
- [ ] Salary reduction
- [ ] Production reduction
- [ ] Fixed expenditure
- [ ] Increase followed by decrease
- [ ] Equal increase/decrease

---

# 57. Related Topics

- [[03. Percentage]]
- [[Percentage Basics]]
- [[Percentage Comparison]]
- [[Percentage Increase]]
- [[Percentage Decrease]]
- [[Successive Increase]]
- [[Net Percentage Change]]
- [[Reverse Percentage]]
- [[Population]]
- [[Salary]]
- [[Price]]
- [[Consumption]]
- [[Expenditure]]

---

# 58. Quick Revision

> [!summary] One-Minute Revision

### Two Successive Decreases

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

Example:

$$
10\%+20\%
=
10+20-2
=
\boxed{28\%}
$$

### Multiplier Method

$$
\boxed{
(1-\frac a{100})(1-\frac b{100})
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
r\%\uparrow\text{ then }r\%\downarrow
\Rightarrow
\frac{r^2}{100}\%\text{ decrease}
}
$$

### Golden Memory Trick

> **Successive decrease = multiply the remaining percentages, not the decrease percentages.**

### One-Line Recognition

> **When a percentage decrease happens repeatedly, each new decrease acts on the current reduced value, creating a compounding effect.**