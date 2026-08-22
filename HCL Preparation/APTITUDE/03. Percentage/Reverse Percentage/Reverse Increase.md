---
type: concept
subject: aptitude
topic: "Reverse Increase"
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
  - reverse-increase
  - quantitative-aptitude
wikilinks:
  - "[[03. Percentage]]"
  - "[[Percentage Increase]]"
  - "[[Percentage Decrease]]"
  - "[[Finding Original Value]]"
  - "[[Reverse Decrease]]"
  - "[[Net Percentage Change]]"
---

# Reverse Increase

## 1. Core Concept

> [!summary] Definition
> **Reverse increase** means finding the **original value** when the final value is known after a percentage increase.

If a value increases by `x%`:

$$
\text{Final}
=
\text{Original}
\left(1+\frac{x}{100}\right)
$$

Therefore:

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{1+x/100}
}
$$

---

# 2. Golden Rule

> [!important]
> **After a percentage increase, to find the original value, DIVIDE the final value by the increase multiplier.**

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

# 3. Increase Multiplier

For an `x%` increase:

$$
\boxed{
1+\frac{x}{100}
}
$$

Examples:

| Increase | Multiplier |
|---:|---:|
| `10%` | `1.10` |
| `20%` | `1.20` |
| `25%` | `1.25` |
| `30%` | `1.30` |
| `50%` | `1.50` |
| `100%` | `2.00` |

---

# 4. Main Formula

If:

- Original = `P`
- Final = `F`
- Increase = `x%`

then:

$$
F=P\left(1+\frac{x}{100}\right)
$$

Therefore:

$$
\boxed{
P=\frac{F}{1+x/100}
}
$$

---

# 5. Shortcut Formula

Multiply numerator and denominator by `100`:

$$
P
=
\frac{100F}{100+x}
$$

Therefore:

$$
\boxed{
\text{Original}
=
\frac{100\times\text{Final}}
{100+\text{Increase \%}}
}
$$

---

# 6. Basic Example

A number is increased by `20%` and becomes `600`.

Find the original.

### Step 1

Increase multiplier:

$$
1.2
$$

### Step 2

Divide final by multiplier:

$$
\frac{600}{1.2}
$$

$$
=\boxed{500}
$$

---

# 7. Same Example Using Shortcut

$$
\text{Original}
=
\frac{100\times600}{100+20}
$$

$$
=
\frac{60000}{120}
$$

$$
=\boxed{500}
$$

---

# 8. Example — 10% Increase

A salary becomes `₹44,000` after a `10%` increase.

Original:

$$
\frac{44000}{1.1}
$$

$$
=\boxed{₹40,000}
$$

---

# 9. Example — 25% Increase

A price becomes `₹1,000` after a `25%` increase.

Multiplier:

$$
1.25=\frac54
$$

Original:

$$
1000\times\frac45
$$

$$
=\boxed{₹800}
$$

---

# 10. Example — 50% Increase

A number becomes `900` after a `50%` increase.

Multiplier:

$$
1.5=\frac32
$$

Original:

$$
900\times\frac23
$$

$$
=\boxed{600}
$$

---

# 11. Example — 100% Increase

A value becomes `₹1,000` after a `100%` increase.

A `100%` increase means the final is:

$$
200\%
$$

of the original.

Therefore:

$$
\text{Original}
=
\frac{1000}{2}
$$

$$
=\boxed{₹500}
$$

---

# 12. Reverse Increase Using Percentages

Suppose:

> A number is increased by `25%` and becomes `250`.

Since:

$$
25\%\text{ increase}
\Rightarrow125\%\text{ of original}
$$

Therefore:

$$
250=125\%\text{ of original}
$$

$$
\text{Original}
=
250\times\frac{100}{125}
$$

$$
=\boxed{200}
$$

---

# 13. Reverse Increase Using Fractions

A `25%` increase means:

$$
25\%=\frac14
$$

So:

$$
\text{Final}
=
\text{Original}
+
\frac14\text{Original}
$$

$$
=
\frac54\text{Original}
$$

Therefore:

$$
\boxed{
\text{Original}
=
\text{Final}\times\frac45
}
$$

---

# 14. Important Shortcut Values

### 10% Increase

Final:

$$
110\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac{10}{11}
}
$$

### 20% Increase

Final:

$$
120\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac56
}
$$

### 25% Increase

Final:

$$
125\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac45
}
$$

### 50% Increase

Final:

$$
150\%
$$

Original:

$$
\boxed{
\text{Final}\times\frac23
}
$$

---

# 15. Reverse Increase Table

| Increase | Final is | Original = Final × |
|---:|---:|---:|
| `5%` | `105%` | `20/21` |
| `10%` | `110%` | `10/11` |
| `20%` | `120%` | `5/6` |
| `25%` | `125%` | `4/5` |
| `30%` | `130%` | `10/13` |
| `40%` | `140%` | `5/7` |
| `50%` | `150%` | `2/3` |
| `75%` | `175%` | `4/7` |
| `100%` | `200%` | `1/2` |
| `200%` | `300%` | `1/3` |

---

# 16. Why You Cannot Subtract the Increase

Suppose final value is:

$$
600
$$

after a `20%` increase.

Wrong:

$$
600-20\%\text{ of }600
$$

$$
600-120=480
$$

Correct:

$$
600\div1.2
=
\boxed{500}
$$

---

# 17. Why the Wrong Method Fails

Original:

$$
500
$$

Increase:

$$
20\%\text{ of }500=100
$$

Final:

$$
600
$$

The increase is based on `500`, not `600`.

But the wrong method calculates:

$$
20\%\text{ of }600=120
$$

That is a different quantity.

> [!important]
> **Percentage increase always uses the original value as its base.**

---

# 18. Reverse Increase From Increase Amount

A number increases by `20%`, and the increase itself is `₹100`.

Since:

$$
20\%\text{ of Original}=100
$$

Therefore:

$$
\frac{20}{100}P=100
$$

$$
P=500
$$

Final:

$$
500+100
=
\boxed{₹600}
$$

---

# 19. Reverse Increase From Difference

Original and final differ by `150`.

The final value is `25%` greater than original.

Then:

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
600+150
=
\boxed{750}
$$

---

# 20. Reverse Increase From Ratio

Suppose:

$$
\text{Final}:\text{Original}=5:4
$$

Then:

$$
\frac54=1.25
$$

Therefore final is:

$$
125\%
$$

of original.

So increase:

$$
125-100
=
\boxed{25\%}
$$

To recover original:

$$
\boxed{
\text{Original}
=
\text{Final}\times\frac45
}
$$

---

# 21. Reverse Increase From Decimal

Suppose:

$$
\text{Final}=1.25\times\text{Original}
$$

Then:

$$
\text{Original}
=
\frac{\text{Final}}{1.25}
$$

Since:

$$
1.25=\frac54
$$

we can use:

$$
\boxed{
\text{Original}
=
\text{Final}\times\frac45
}
$$

---

# 22. Reverse Increase With Salary

A person's salary increases by `20%` and becomes `₹48,000`.

Original:

$$
\frac{48000}{1.2}
$$

$$
=\boxed{₹40,000}
$$

Increase:

$$
₹8,000
$$

Check:

$$
40000+8000
=
48000
$$

Correct.

---

# 23. Reverse Increase With Price

A product's price increases by `25%` and becomes `₹1,500`.

Original:

$$
1500\times\frac45
$$

$$
=\boxed{₹1,200}
$$

Check:

$$
1200\times1.25
=
1500
$$

---

# 24. Reverse Increase With Population

Population after a `10%` increase is:

$$
55,000
$$

Original:

$$
\frac{55000}{1.1}
$$

$$
=\boxed{50,000}
$$

---

# 25. Reverse Increase With Marks

Marks after a `25%` increase:

$$
500
$$

Original:

$$
500\times\frac45
$$

$$
=\boxed{400}
$$

---

# 26. Reverse Increase With Production

Production after a `20%` increase:

$$
7,200
$$

Original:

$$
\frac{7200}{1.2}
$$

$$
=\boxed{6,000}
$$

---

# 27. Reverse Increase With Consumption

Consumption after a `25%` increase:

$$
100\text{ kg}
$$

Original:

$$
100\times\frac45
=
\boxed{80\text{ kg}}
$$

---

# 28. Reverse Increase With Multiple Changes

A quantity is:

1. increased by `20%`
2. increased by `25%`

Final:

$$
₹1500
$$

Combined multiplier:

$$
1.2\times1.25
=
1.5
$$

Original:

$$
\frac{1500}{1.5}
=
\boxed{₹1000}
$$

---

# 29. Reverse Increase With Three Changes

A value is increased by:

- `10%`
- `20%`
- `30%`

Final:

$$
₹1716
$$

Combined multiplier:

$$
1.1\times1.2\times1.3
=
1.716
$$

Original:

$$
\frac{1716}{1.716}
=
\boxed{₹1000}
$$

---

# 30. Reverse Increase With Mixed Changes

A value:

- increases `20%`
- decreases `10%`
- increases `25%`

Final:

$$
₹1350
$$

Combined multiplier:

$$
1.2\times0.9\times1.25
=
1.35
$$

Original:

$$
\frac{1350}{1.35}
=
\boxed{₹1000}
$$

---

# 31. Reverse Increase Using Algebra

Suppose original value is `x`.

After `30%` increase:

$$
x+\frac{30x}{100}
=
1.3x
$$

If final is `650`:

$$
1.3x=650
$$

Therefore:

$$
x=\boxed{500}
$$

---

# 32. Reverse Increase — Word Problem Pattern

> A company's employee count increased by `25%` and became `2,500`. Find the original number of employees.

Recognize:

$$
\text{Final}=125\%\text{ of Original}
$$

Therefore:

$$
\text{Original}
=
2500\times\frac{100}{125}
$$

$$
=\boxed{2000}
$$

---

# 33. Reverse Increase — Population Pattern

> A town's population increased by `20%` and became `72,000`. Find the previous population.

$$
\text{Original}
=
72000\times\frac56
$$

$$
=\boxed{60,000}
$$

---

# 34. Reverse Increase — Salary Pattern

> A salary was increased by `25%` and became `₹50,000`. Find the old salary.

$$
50000\times\frac45
$$

$$
=\boxed{₹40,000}
$$

---

# 35. Reverse Increase — Price Pattern

> The price of a product increased by `20%` to `₹960`. Find the original price.

$$
960\times\frac56
$$

$$
=\boxed{₹800}
$$

---

# 36. Reverse Increase — Marks Pattern

> A student's marks increased by `10%` to `440`. Find the previous marks.

$$
440\times\frac{10}{11}
$$

$$
=\boxed{400}
$$

---

# 37. Reverse Increase — Expenditure Pattern

> Monthly expenditure increased by `25%` and became `₹25,000`.

Original:

$$
25000\times\frac45
$$

$$
=\boxed{₹20,000}
$$

---

# 38. Reverse Increase — Fixed Difference

A number becomes `360` after a `20%` increase.

Increase:

$$
20\%\text{ of original}
$$

Since:

$$
360=120\%\text{ of original}
$$

Original:

$$
360\times\frac{100}{120}
$$

$$
=\boxed{300}
$$

Increase:

$$
360-300
=
\boxed{60}
$$

---

# 39. Reverse Increase — Finding Percentage

Suppose original = `400` and final = `500`.

Increase:

$$
500-400=100
$$

Percentage:

$$
\frac{100}{400}\times100
=
\boxed{25\%}
$$

This is the reverse direction of the same concept.

---

# 40. Reverse Increase and "More Than"

If A is `20% more than B`:

$$
A=1.2B
$$

Therefore:

$$
B=\frac{A}{1.2}
$$

So B is:

$$
\frac{1}{1.2}
=
\frac56
$$

of A.

Therefore B is:

$$
1-\frac56
=
\frac16
$$

less than A:

$$
\boxed{16\frac23\%}
$$

---

# 41. More-Than Reverse Formula

If A is `x% more than B`, then B is:

$$
\boxed{
\frac{x}{100+x}\times100\%
}
$$

less than A.

Example:

A is `50% more than B`.

$$
\frac{50}{150}\times100
=
\boxed{33\frac13\%}
$$

---

# 42. Important More/Less Table

| A is more than B by | B is less than A by |
|---:|---:|
| `10%` | `9.09%` |
| `20%` | `16.67%` |
| `25%` | `20%` |
| `50%` | `33.33%` |
| `100%` | `50%` |
| `200%` | `66.67%` |

---

# 43. Reverse Increase in Area

Suppose the side of a square was increased by `20%`, making its area `576 cm²`.

Side multiplier:

$$
1.2
$$

Area multiplier:

$$
1.2^2
=
1.44
$$

Original area:

$$
\frac{576}{1.44}
=
\boxed{400\text{ cm}^2}
$$

---

# 44. Reverse Increase in Volume

A cube's side increases by `10%`, and its final volume is `1331 cm³`.

Volume multiplier:

$$
1.1^3
=
1.331
$$

Original volume:

$$
\frac{1331}{1.331}
=
\boxed{1000\text{ cm}^3}
$$

---

# 45. Reverse Increase — Compound Growth

A population grows by `10%` annually for `2` years and becomes `12,100`.

Original:

$$
\frac{12100}{(1.1)^2}
$$

$$
=
\frac{12100}{1.21}
$$

$$
=\boxed{10,000}
$$

---

# 46. Reverse Increase — Repeated Growth

If a value grows by `r%` for `n` periods:

$$
F=P\left(1+\frac r{100}\right)^n
$$

Therefore:

$$
\boxed{
P=
\frac{F}
{\left(1+\frac r{100}\right)^n}
}
$$

---

# 47. Common Mistakes

> [!warning] Avoid These

### Mistake 1

Subtracting the percentage from the final.

Wrong.

### Mistake 2

Calculating the percentage using the final value.

Wrong.

### Mistake 3

Adding successive increases directly.

Wrong.

### Mistake 4

Using:

$$
100-x
$$

for an increase.

Wrong.

For increase, use:

$$
100+x
$$

### Mistake 5

Confusing original with final.

Always identify the timeline:

$$
\boxed{
\text{Original}\rightarrow\text{Increase}\rightarrow\text{Final}
}
$$

---

# 48. Fast Exam Method

> [!tip]

When you see:

> "After an increase of `x%`, the value becomes `F`. Find the original."

Immediately write:

$$
\boxed{
\text{Original}
=
F\times\frac{100}{100+x}
}
$$

Example:

Final = `720`

Increase = `20%`

$$
720\times\frac{100}{120}
$$

$$
=\boxed{600}
$$

---

# 49. Formula Sheet

> [!important] Must Remember

### Forward Increase

$$
\boxed{
F=P\left(1+\frac{x}{100}\right)
}
$$

### Reverse Increase

$$
\boxed{
P=\frac{F}{1+x/100}
}
$$

### Shortcut

$$
\boxed{
P=\frac{100F}{100+x}
}
$$

### Fraction Method

If increase is `x%`:

$$
\boxed{
P=F\times\frac{100}{100+x}
}
$$

### Repeated Increase

$$
\boxed{
P=
\frac{F}
{(1+x/100)^n}
}
$$

### More/Less Reverse

If A is `x% more than B`:

$$
\boxed{
B\text{ is }
\frac{x}{100+x}\times100\%
\text{ less than A}
}
$$

---

# 50. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
20\%\text{ increase}\Rightarrow
\text{Original}=\text{Final}\times\frac56
}
$$

### Pattern 2

$$
\boxed{
25\%\text{ increase}\Rightarrow
\text{Original}=\text{Final}\times\frac45
}
$$

### Pattern 3

$$
\boxed{
50\%\text{ increase}\Rightarrow
\text{Original}=\text{Final}\times\frac23
}
$$

### Pattern 4

$$
\boxed{
100\%\text{ increase}\Rightarrow
\text{Original}=\frac{\text{Final}}2
}
$$

### Pattern 5

$$
\boxed{
\text{Reverse increase}=\text{divide by multiplier}
}
$$

### Pattern 6

> **20% increase means final = 120% of original.**

### Pattern 7

> **25% increase means final = 125% of original.**

### Pattern 8

> **50% increase means final = 150% of original.**

### Pattern 9

> **A is 25% more than B → B is 20% less than A.**

### Pattern 10

> **Forward → multiply. Reverse → divide.**

---

# 51. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Master these first:

1. Reverse increase formula
2. Increase multiplier
3. Shortcut formula
4. Fraction method
5. Reverse salary
6. Reverse price
7. Reverse population
8. Reverse marks
9. Reverse production
10. Reverse expenditure
11. Reverse from increase amount
12. Reverse from difference
13. Reverse from ratio
14. Reverse successive increases
15. Reverse mixed changes
16. More-than / less-than conversion
17. Area reverse problems
18. Volume reverse problems
19. Compound growth reverse problems

---

# 52. Practice Checklist

- [ ] Reverse `10%` increase
- [ ] Reverse `20%` increase
- [ ] Reverse `25%` increase
- [ ] Reverse `50%` increase
- [ ] Reverse `100%` increase
- [ ] Salary
- [ ] Price
- [ ] Population
- [ ] Marks
- [ ] Production
- [ ] Expenditure
- [ ] Increase amount
- [ ] Difference
- [ ] Ratio
- [ ] Fraction
- [ ] Decimal multiplier
- [ ] Successive increases
- [ ] Mixed changes
- [ ] More/less conversion
- [ ] Area
- [ ] Volume
- [ ] Compound growth

---

# 53. Related Topics

- [[03. Percentage]]
- [[Percentage Basics]]
- [[Percentage Comparison]]
- [[Percentage Increase]]
- [[Percentage Decrease]]
- [[Successive Increase]]
- [[Successive Decrease]]
- [[Net Percentage Change]]
- [[Finding Original Value]]
- [[Reverse Decrease]]
- [[Percentage Error]]
- [[Percentage Difference]]
- [[Mixed Percentage Problems]]

---

# 54. Quick Revision

> [!summary] One-Minute Revision

### Main Formula

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{1+x/100}
}
$$

### Shortcut

$$
\boxed{
\text{Original}
=
\frac{100\times\text{Final}}
{100+x}
}
$$

### Example

Final = `600`, increase = `20%`

$$
600\times\frac{100}{120}
=
\boxed{500}
$$

### Golden Memory Trick

> **An increase changes 100% → 100% + x%. To go backward, divide the final value by that new percentage.**

### One-Line Recognition

> **If the question says "after increasing by x%, the value becomes F," immediately divide F by `(1 + x/100)`.**