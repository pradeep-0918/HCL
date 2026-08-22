---
type: concept
subject: aptitude
topic: "Reverse Decrease"
parent: "03. Percentage > Reverse Percentage"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - percentage
  - reverse-percentage
  - reverse-decrease
  - quantitative-aptitude
wikilinks:
  - "[[03. Percentage]]"
  - "[[Percentage Increase]]"
  - "[[Percentage Decrease]]"
  - "[[Finding Original Value]]"
  - "[[Reverse Increase]]"
  - "[[Net Percentage Change]]"
---

# Reverse Decrease

## 1. Core Concept

> [!summary] Definition
> **Reverse decrease** means finding the **original value** when the final value is known after a percentage decrease.

If a value decreases by `x%`:

$$
\text{Final}
=
\text{Original}
\left(1-\frac{x}{100}\right)
$$

Therefore:

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{1-x/100}
}
$$

---

# 2. Golden Rule

> [!important]
> **After a percentage decrease, to find the original value, DIVIDE the final value by the remaining multiplier.**

Forward:

$$
\text{Original}\times\text{Multiplier}
=
\text{Final}
$$

Reverse:

$$
\boxed{
\text{Final}\div\text{Multiplier}
=
\text{Original}
}
$$

---

# 3. Decrease Multiplier

For an `x%` decrease:

$$
\boxed{
1-\frac{x}{100}
}
$$

Examples:

| Decrease | Remaining Multiplier |
|---:|---:|
| `10%` | `0.90` |
| `20%` | `0.80` |
| `25%` | `0.75` |
| `30%` | `0.70` |
| `40%` | `0.60` |
| `50%` | `0.50` |
| `75%` | `0.25` |

---

# 4. Main Formula

If:

- Original = `P`
- Final = `F`
- Decrease = `x%`

then:

$$
F=P\left(1-\frac{x}{100}\right)
$$

Therefore:

$$
\boxed{
P=\frac{F}{1-x/100}
}
$$

---

# 5. Shortcut Formula

Multiply numerator and denominator by `100`:

$$
P=
\frac{100F}{100-x}
$$

Therefore:

$$
\boxed{
\text{Original}
=
\frac{100\times\text{Final}}
{100-\text{Decrease \%}}
}
$$

---

# 6. Basic Example

A number is decreased by `20%` and becomes `400`.

Find the original.

Remaining percentage:

$$
100\%-20\%
=
80\%
$$

Therefore:

$$
400=80\%\text{ of Original}
$$

$$
\text{Original}
=
\frac{400}{0.8}
$$

$$
=\boxed{500}
$$

---

# 7. Same Example Using Shortcut

$$
\text{Original}
=
\frac{100\times400}{100-20}
$$

$$
=
\frac{40000}{80}
$$

$$
=\boxed{500}
$$

---

# 8. Example — 10% Decrease

A salary becomes `₹36,000` after a `10%` decrease.

Original:

$$
\frac{36000}{0.9}
$$

$$
=\boxed{₹40,000}
$$

---

# 9. Example — 25% Decrease

A price becomes `₹750` after a `25%` decrease.

Remaining:

$$
75\%=\frac34
$$

Original:

$$
750\times\frac43
$$

$$
=\boxed{₹1000}
$$

---

# 10. Example — 50% Decrease

A number becomes `300` after a `50%` decrease.

Remaining:

$$
50\%=\frac12
$$

Original:

$$
300\times2
$$

$$
=\boxed{600}
$$

---

# 11. Example — 75% Decrease

A quantity becomes `200` after a `75%` decrease.

Remaining:

$$
25\%=\frac14
$$

Original:

$$
200\times4
$$

$$
=\boxed{800}
$$

---

# 12. Reverse Decrease Using Percentages

Suppose:

> A number is decreased by `20%` and becomes `640`.

A `20%` decrease means:

$$
80\%\text{ remains}
$$

Therefore:

$$
640=80\%\text{ of Original}
$$

$$
\text{Original}
=
640\times\frac{100}{80}
$$

$$
=\boxed{800}
$$

---

# 13. Reverse Decrease Using Fractions

A `20%` decrease means:

$$
20\%=\frac15
$$

Remaining:

$$
1-\frac15
=
\frac45
$$

Therefore:

$$
\text{Final}
=
\frac45\text{ Original}
$$

So:

$$
\boxed{
\text{Original}
=
\text{Final}\times\frac54
}
$$

---

# 14. Important Shortcut Values

### 10% Decrease

Remaining:

$$
90\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac{10}{9}
}
$$

### 20% Decrease

Remaining:

$$
80\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac54
}
$$

### 25% Decrease

Remaining:

$$
75\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac43
}
$$

### 50% Decrease

Remaining:

$$
50\%
$$

Original:

$$
\boxed{
\text{Final}\times2
}
$$

---

# 15. Reverse Decrease Table

| Decrease | Final is | Original = Final × |
|---:|---:|---:|
| `5%` | `95%` | `20/19` |
| `10%` | `90%` | `10/9` |
| `20%` | `80%` | `5/4` |
| `25%` | `75%` | `4/3` |
| `30%` | `70%` | `10/7` |
| `40%` | `60%` | `5/3` |
| `50%` | `50%` | `2` |
| `60%` | `40%` | `5/2` |
| `75%` | `25%` | `4` |

---

# 16. Why You Cannot Add the Percentage to the Final

Suppose final value is:

$$
400
$$

after a `20%` decrease.

Wrong:

$$
400+20\%\text{ of }400
$$

$$
400+80=480
$$

Wrong.

Correct:

$$
400\div0.8
=
\boxed{500}
$$

---

# 17. Why the Wrong Method Fails

Original:

$$
500
$$

Decrease:

$$
20\%\text{ of }500=100
$$

Final:

$$
500-100=400
$$

The decrease was calculated from `500`.

But the wrong method calculates:

$$
20\%\text{ of }400=80
$$

So:

$$
400+80=480
$$

which is not the original.

> [!important]
> **The percentage decrease is based on the original value, not the final value.**

---

# 18. Reverse Decrease From Decrease Amount

A number decreases by `20%`, and the decrease itself is `₹100`.

Since:

$$
20\%\text{ of Original}=100
$$

Therefore:

$$
\frac{20}{100}P=100
$$

$$
P=\boxed{500}
$$

Final:

$$
500-100
=
\boxed{400}
$$

---

# 19. Reverse Decrease From Difference

A number decreases by `25%`, and the decrease is `₹150`.

Since:

$$
25\%\text{ of Original}=150
$$

Therefore:

$$
\frac14P=150
$$

$$
P=\boxed{600}
$$

Final:

$$
600-150
=
\boxed{450}
$$

---

# 20. Reverse Decrease From Ratio

Suppose:

$$
\text{Final}:\text{Original}=4:5
$$

Then:

$$
\frac45=80\%
$$

Therefore final is `80%` of original.

Decrease:

$$
100-80
=
\boxed{20\%}
$$

To recover original:

$$
\boxed{
\text{Original}
=
\text{Final}\times\frac54
}
$$

---

# 21. Reverse Decrease From Decimal

Suppose:

$$
\text{Final}=0.75\times\text{Original}
$$

Then:

$$
\text{Original}
=
\frac{\text{Final}}{0.75}
$$

Since:

$$
0.75=\frac34
$$

we get:

$$
\boxed{
\text{Original}
=
\text{Final}\times\frac43
}
$$

---

# 22. Reverse Decrease With Salary

A salary decreases by `20%` and becomes:

$$
₹40,000
$$

Original:

$$
\frac{40000}{0.8}
$$

$$
=\boxed{₹50,000}
$$

Check:

$$
50000\times0.8
=
40000
$$

---

# 23. Reverse Decrease With Price

A product's price decreases by `25%` and becomes:

$$
₹900
$$

Original:

$$
900\times\frac43
$$

$$
=\boxed{₹1200}
$$

---

# 24. Reverse Decrease With Population

Population decreases by `10%` and becomes:

$$
72,000
$$

Original:

$$
\frac{72000}{0.9}
$$

$$
=\boxed{80,000}
$$

---

# 25. Reverse Decrease With Marks

Marks decrease by `20%` and become:

$$
320
$$

Original:

$$
\frac{320}{0.8}
$$

$$
=\boxed{400}
$$

---

# 26. Reverse Decrease With Production

Production decreases by `25%` and becomes:

$$
900
$$

Original:

$$
900\times\frac43
$$

$$
=\boxed{1200}
$$

---

# 27. Reverse Decrease With Consumption

Consumption decreases by `20%` and becomes:

$$
64\text{ kg}
$$

Original:

$$
64\times\frac54
$$

$$
=\boxed{80\text{ kg}}
$$

---

# 28. Reverse Decrease With Expenditure

Monthly expenditure decreases by `10%` and becomes:

$$
₹18,000
$$

Original:

$$
\frac{18000}{0.9}
$$

$$
=\boxed{₹20,000}
$$

---

# 29. Reverse Decrease With Multiple Changes

A quantity is:

1. decreased by `20%`
2. decreased by `25%`

Final:

$$
₹600
$$

Combined multiplier:

$$
0.8\times0.75
=
0.6
$$

Original:

$$
\frac{600}{0.6}
=
\boxed{₹1000}
$$

---

# 30. Reverse Decrease With Three Changes

A value decreases by:

- `10%`
- `20%`
- `30%`

Final:

$$
₹504
$$

Combined multiplier:

$$
0.9\times0.8\times0.7
=
0.504
$$

Original:

$$
\frac{504}{0.504}
=
\boxed{₹1000}
$$

---

# 31. Reverse Mixed Changes

A value:

1. decreases by `20%`
2. increases by `25%`
3. decreases by `10%`

Final:

$$
₹900
$$

Combined multiplier:

$$
0.8\times1.25\times0.9
=
0.9
$$

Original:

$$
\frac{900}{0.9}
=
\boxed{₹1000}
$$

---

# 32. Reverse Decrease Using Algebra

Suppose original value is `x`.

After a `30%` decrease:

$$
x-\frac{30x}{100}
=
0.7x
$$

If final is `560`:

$$
0.7x=560
$$

Therefore:

$$
x=\boxed{800}
$$

---

# 33. Reverse Decrease — Word Problem

> A company's employee count decreased by `25%` and became `1,500`. Find the original number of employees.

Remaining:

$$
75\%
$$

Therefore:

$$
\text{Original}
=
1500\times\frac{100}{75}
$$

$$
=\boxed{2000}
$$

---

# 34. Reverse Decrease — Population

> A town's population decreased by `20%` and became `64,000`. Find the previous population.

$$
\text{Original}
=
64000\times\frac54
$$

$$
=\boxed{80,000}
$$

---

# 35. Reverse Decrease — Salary

> A salary was reduced by `25%` and became `₹45,000`. Find the old salary.

$$
45000\times\frac43
$$

$$
=\boxed{₹60,000}
$$

---

# 36. Reverse Decrease — Price

> A product's price was reduced by `20%` and became `₹800`. Find the original price.

$$
800\times\frac54
$$

$$
=\boxed{₹1000}
$$

---

# 37. Reverse Decrease — Marks

> Marks decreased by `10%` and became `360`. Find the original marks.

$$
360\times\frac{10}{9}
$$

$$
=\boxed{400}
$$

---

# 38. Reverse Decrease — Discount

A product is sold for `₹960` after a `20%` discount.

The selling price is:

$$
80\%
$$

of marked price.

Therefore:

$$
\text{Marked Price}
=
\frac{960}{0.8}
$$

$$
=\boxed{₹1200}
$$

> [!tip]
> Discount problems are often reverse-decrease problems.

---

# 39. Reverse Decrease — Depreciation

A machine depreciates by `10%` and is now worth `₹72,000`.

Original value:

$$
\frac{72000}{0.9}
$$

$$
=\boxed{₹80,000}
$$

---

# 40. Reverse Decrease — Compound Depreciation

A machine depreciates by `10%` annually for `2` years and is worth `₹81,000`.

Final multiplier:

$$
(0.9)^2
=
0.81
$$

Original:

$$
\frac{81000}{0.81}
=
\boxed{₹100,000}
$$

---

# 41. Reverse Decrease — Repeated Reduction

If a value decreases by `r%` for `n` periods:

$$
F=P\left(1-\frac r{100}\right)^n
$$

Therefore:

$$
\boxed{
P=
\frac{F}
{\left(1-\frac r{100}\right)^n}
}
$$

---

# 42. Reverse Decrease and "Less Than"

If A is `20% less than B`:

$$
A=0.8B
$$

Therefore:

$$
B=\frac{A}{0.8}
=
1.25A
$$

So:

$$
\boxed{
B\text{ is 25\% more than A}
}
$$

---

# 43. Less-Than Reverse Formula

If A is `x% less than B`, then B is:

$$
\boxed{
\frac{x}{100-x}\times100\%
}
$$

more than A.

Example:

A is `20% less than B`.

$$
\frac{20}{80}\times100
=
\boxed{25\%}
$$

---

# 44. Important Less/More Table

| A is less than B by | B is more than A by |
|---:|---:|
| `10%` | `11.11%` |
| `20%` | `25%` |
| `25%` | `33.33%` |
| `30%` | `42.86%` |
| `40%` | `66.67%` |
| `50%` | `100%` |
| `75%` | `300%` |

---

# 45. Reverse Decrease in Area

A square's side decreases by `20%`, and its final area is:

$$
256\text{ cm}^2
$$

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

Original area:

$$
\frac{256}{0.64}
=
\boxed{400\text{ cm}^2}
$$

---

# 46. Reverse Decrease in Volume

A cube's side decreases by `20%`, and final volume is:

$$
512\text{ cm}^3
$$

Volume multiplier:

$$
0.8^3
=
0.512
$$

Original volume:

$$
\frac{512}{0.512}
=
\boxed{1000\text{ cm}^3}
$$

---

# 47. Reverse Decrease — Area Pattern

If side decreases by `x%`:

$$
\boxed{
\text{Area multiplier}
=
\left(1-\frac{x}{100}\right)^2
}
$$

Therefore:

$$
\boxed{
\text{Original Area}
=
\frac{\text{Final Area}}
{(1-x/100)^2}
}
$$

---

# 48. Reverse Decrease — Volume Pattern

If side decreases by `x%`:

$$
\boxed{
\text{Volume multiplier}
=
\left(1-\frac{x}{100}\right)^3
}
$$

Therefore:

$$
\boxed{
\text{Original Volume}
=
\frac{\text{Final Volume}}
{(1-x/100)^3}
}
$$

---

# 49. Important Comparison Trap

A value decreases from:

$$
100\rightarrow80
$$

Percentage decrease:

$$
\frac{20}{100}\times100
=
\boxed{20\%}
$$

But going backward:

$$
80\rightarrow100
$$

Percentage increase:

$$
\frac{20}{80}\times100
=
\boxed{25\%}
$$

Therefore:

$$
\boxed{
20\%\text{ decrease}\ne20\%\text{ reverse increase}
}
$$

---

# 50. Reverse Decrease vs Reverse Increase

| Situation | Reverse Formula |
|---|---|
| Final after `x%` increase | `Final ÷ (1+x/100)` |
| Final after `x%` decrease | `Final ÷ (1-x/100)` |
| Increase shortcut | `Final × 100/(100+x)` |
| Decrease shortcut | `Final × 100/(100-x)` |

---

# 51. Common Mistakes

> [!warning] Avoid These

### Mistake 1

Adding the decrease percentage to the final.

Wrong.

### Mistake 2

Calculating the decrease percentage using the final value.

Wrong.

### Mistake 3

Using `100+x` for a decrease.

Wrong.

Use:

$$
100-x
$$

### Mistake 4

Forgetting the remaining percentage.

Example:

`25% decrease`

Remaining:

$$
75\%
$$

not `25%`.

### Mistake 5

Adding successive decreases directly.

Wrong.

Use multipliers.

---

# 52. Fast Exam Method

> [!tip]

When you see:

> "After decreasing by `x%`, the value becomes `F`. Find the original."

Immediately write:

$$
\boxed{
\text{Original}
=
F\times\frac{100}{100-x}
}
$$

Example:

Final = `640`

Decrease = `20%`

$$
640\times\frac{100}{80}
$$

$$
=\boxed{800}
$$

---

# 53. Universal Reverse Method

### Step 1

Identify the final value.

### Step 2

Identify the percentage decrease.

### Step 3

Find the remaining percentage:

$$
100-x
$$

### Step 4

Convert it to a multiplier:

$$
\frac{100-x}{100}
$$

### Step 5

Divide final by that multiplier.

Therefore:

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{(100-x)/100}
}
$$

---

# 54. Formula Sheet

> [!important] Must Remember

### Forward Decrease

$$
\boxed{
F=P\left(1-\frac{x}{100}\right)
}
$$

### Reverse Decrease

$$
\boxed{
P=\frac{F}{1-x/100}
}
$$

### Shortcut

$$
\boxed{
P=\frac{100F}{100-x}
}
$$

### Fraction Method

If decrease is `x%`:

$$
\boxed{
P=F\times\frac{100}{100-x}
}
$$

### Repeated Decrease

$$
\boxed{
P=
\frac{F}
{(1-x/100)^n}
}
$$

### Less/More Reverse

If A is `x% less than B`:

$$
\boxed{
B\text{ is }
\frac{x}{100-x}\times100\%
\text{ more than A}
}
$$

---

# 55. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
20\%\text{ decrease}
\Rightarrow
\text{Original}=\text{Final}\times\frac54
}
$$

### Pattern 2

$$
\boxed{
25\%\text{ decrease}
\Rightarrow
\text{Original}=\text{Final}\times\frac43
}
$$

### Pattern 3

$$
\boxed{
50\%\text{ decrease}
\Rightarrow
\text{Original}=2\times\text{Final}
}
$$

### Pattern 4

$$
\boxed{
75\%\text{ decrease}
\Rightarrow
\text{Original}=4\times\text{Final}
}
$$

### Pattern 5

$$
\boxed{
\text{Reverse decrease}=\text{divide by remaining multiplier}
}
$$

### Pattern 6

> **20% decrease means final = 80% of original.**

### Pattern 7

> **25% decrease means final = 75% of original.**

### Pattern 8

> **50% decrease means final = 50% of original.**

### Pattern 9

$$
\boxed{
A\text{ is 20\% less than B}
\Rightarrow
B\text{ is 25\% more than A}
}
$$

### Pattern 10

> **Forward → multiply. Reverse → divide.**

---

# 56. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Master these first:

1. Reverse decrease formula
2. Remaining percentage
3. Decrease multiplier
4. Shortcut formula
5. Fraction method
6. Reverse salary
7. Reverse price
8. Reverse population
9. Reverse marks
10. Reverse production
11. Reverse expenditure
12. Reverse discount
13. Reverse depreciation
14. Reverse successive decreases
15. Reverse mixed changes
16. Less-than / more-than conversion
17. Area reverse problems
18. Volume reverse problems
19. Compound depreciation

---

# 57. Practice Checklist

- [ ] Reverse `10%` decrease
- [ ] Reverse `20%` decrease
- [ ] Reverse `25%` decrease
- [ ] Reverse `30%` decrease
- [ ] Reverse `50%` decrease
- [ ] Reverse `75%` decrease
- [ ] Salary
- [ ] Price
- [ ] Population
- [ ] Marks
- [ ] Production
- [ ] Expenditure
- [ ] Discount
- [ ] Depreciation
- [ ] Decrease amount
- [ ] Difference
- [ ] Ratio
- [ ] Fraction
- [ ] Decimal multiplier
- [ ] Successive decreases
- [ ] Mixed changes
- [ ] Less/more conversion
- [ ] Area
- [ ] Volume
- [ ] Compound depreciation

---

# 58. Related Topics

- [[03. Percentage]]
- [[Percentage Basics]]
- [[Percentage Comparison]]
- [[Percentage Increase]]
- [[Percentage Decrease]]
- [[Successive Increase]]
- [[Successive Decrease]]
- [[Net Percentage Change]]
- [[Finding Original Value]]
- [[Reverse Increase]]
- [[Percentage Error]]
- [[Percentage Difference]]
- [[Mixed Percentage Problems]]

---

# 59. Quick Revision

> [!summary] One-Minute Revision

### Main Formula

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{1-x/100}
}
$$

### Shortcut

$$
\boxed{
\text{Original}
=
\frac{100\times\text{Final}}
{100-x}
}
$$

### Example

Final = `400`, decrease = `20%`

$$
400\times\frac{100}{80}
=
\boxed{500}
$$

### Golden Memory Trick

> **A decrease leaves `100 − x%`. To reverse it, divide the final value by that remaining percentage.**

### One-Line Recognition

> **If the question says "after decreasing by x%, the value becomes F," immediately divide F by `(1 − x/100)`.**