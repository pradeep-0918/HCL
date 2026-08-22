---
type: concept
subject: aptitude
topic: "Finding Original Value"
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
  - original-value
  - quantitative-aptitude
wikilinks:
  - "[[03. Percentage]]"
  - "[[Percentage Increase]]"
  - "[[Percentage Decrease]]"
  - "[[Reverse Increase]]"
  - "[[Reverse Decrease]]"
  - "[[Net Percentage Change]]"
---

# Finding Original Value

## 1. Core Concept

> [!summary] Definition
> **Finding original value** means calculating the value that existed **before a percentage increase or decrease**.

This is called a **reverse percentage problem**.

The most important rule:

> **Do not subtract/add the percentage from the final value. Divide by the appropriate multiplier.**

---

# 2. The Master Idea

If a value is increased by `x%`:

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

If a value is decreased by `x%`:

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

# 3. The Most Important Rule

> [!important]
> **When going backward, DIVIDE by the multiplier.**

Forward:

$$
\text{Original}\times\text{Multiplier}
=
\text{Final}
$$

Backward:

$$
\boxed{
\text{Final}\div\text{Multiplier}
=
\text{Original}
}
$$

---

# 4. Reverse After Increase

Suppose a number increases by `20%` and becomes `600`.

A `20%` increase means:

$$
100\%\rightarrow120\%
$$

Therefore:

$$
\text{Final}=120\%\text{ of Original}
$$

So:

$$
600=1.2\times\text{Original}
$$

Therefore:

$$
\text{Original}
=
\frac{600}{1.2}
$$

$$
=\boxed{500}
$$

---

# 5. Shortcut Formula — Increase

If final value is `F` after an increase of `x%`:

$$
\boxed{
\text{Original}
=
\frac{100F}{100+x}
}
$$

Example:

Final = `600`

Increase = `20%`

$$
\frac{100\times600}{120}
$$

$$
=\boxed{500}
$$

---

# 6. Reverse After Decrease

Suppose a number decreases by `20%` and becomes `400`.

A `20%` decrease means:

$$
100\%-20\%=80\%
$$

Therefore:

$$
400=0.8\times\text{Original}
$$

Original:

$$
\frac{400}{0.8}
=
\boxed{500}
$$

---

# 7. Shortcut Formula — Decrease

If final value is `F` after a decrease of `x%`:

$$
\boxed{
\text{Original}
=
\frac{100F}{100-x}
}
$$

Example:

Final = `400`

Decrease = `20%`

$$
\frac{100\times400}{80}
$$

$$
=\boxed{500}
$$

---

# 8. Increase vs Decrease

| Situation | Final Multiplier | Original |
|---|---:|---:|
| Increase `x%` | `1 + x/100` | `Final ÷ multiplier` |
| Decrease `x%` | `1 - x/100` | `Final ÷ multiplier` |

Shortcut:

### Increase

$$
\boxed{
\frac{100F}{100+x}
}
$$

### Decrease

$$
\boxed{
\frac{100F}{100-x}
}
$$

---

# 9. Example — 25% Increase

A price becomes `₹1000` after a `25%` increase.

Remaining relationship:

$$
125\%= \frac54
$$

Therefore:

$$
\text{Original}
=
1000\times\frac45
$$

$$
=\boxed{₹800}
$$

---

# 10. Example — 25% Decrease

A price becomes `₹750` after a `25%` decrease.

Remaining:

$$
75\%=\frac34
$$

Therefore:

$$
\text{Original}
=
750\times\frac43
$$

$$
=\boxed{₹1000}
$$

---

# 11. Example — 10% Increase

Final:

$$
₹880
$$

Increase:

`10%`

Multiplier:

$$
1.1
$$

Original:

$$
\frac{880}{1.1}
=
\boxed{₹800}
$$

---

# 12. Example — 10% Decrease

Final:

$$
₹720
$$

Decrease:

`10%`

Multiplier:

$$
0.9
$$

Original:

$$
\frac{720}{0.9}
=
\boxed{₹800}
$$

---

# 13. Percentage Language

These statements mean the same thing:

### "A increases by 20%"

$$
A_{\text{new}}=120\%\text{ of }A_{\text{old}}
$$

### "A becomes 120% of its original"

$$
A_{\text{new}}=1.2A_{\text{old}}
$$

### "A is 20% more than its original"

Same relationship.

Therefore:

$$
\boxed{
\text{20\% increase}\rightarrow120\%\text{ of original}
}
$$

---

# 14. Decrease Language

### "A decreases by 20%"

$$
A_{\text{new}}=80\%\text{ of original}
$$

### "A becomes 80% of original"

Same relationship.

### "A is 20% less than original"

Same relationship.

Therefore:

$$
\boxed{
20\%\text{ decrease}\rightarrow80\%\text{ of original}
}
$$

---

# 15. Common Trap

Suppose a price after a `20%` increase is `₹600`.

Wrong method:

$$
600-20\%\text{ of }600
$$

$$
=600-120
=
480
$$

Wrong answer.

Correct:

$$
\frac{600}{1.2}
=
\boxed{500}
$$

> [!warning]
> The `20%` was calculated using the **original value**, not the final value.

---

# 16. Why Subtracting the Percentage Is Wrong

Suppose original = `500`.

Increase by `20%`:

$$
500\times1.2=600
$$

Now if you calculate `20%` of the final value:

$$
600\times0.2=120
$$

But the actual increase was:

$$
500\times0.2=100
$$

Therefore:

$$
600-120=480
$$

which is not the original.

---

# 17. Reverse Percentage Using Ratio

Suppose final is `125%` of original.

Then:

$$
\text{Final}:\text{Original}=125:100
$$

Simplify:

$$
5:4
$$

Therefore:

$$
\boxed{
\text{Original}=\text{Final}\times\frac45
}
$$

---

# 18. Reverse Percentage Table — Increase

| Increase | Final % of Original | Original = Final × |
|---:|---:|---:|
| `5%` | `105%` | `100/105` |
| `10%` | `110%` | `10/11` |
| `20%` | `120%` | `5/6` |
| `25%` | `125%` | `4/5` |
| `50%` | `150%` | `2/3` |
| `100%` | `200%` | `1/2` |
| `200%` | `300%` | `1/3` |

---

# 19. Reverse Percentage Table — Decrease

| Decrease | Final % of Original | Original = Final × |
|---:|---:|---:|
| `10%` | `90%` | `10/9` |
| `20%` | `80%` | `5/4` |
| `25%` | `75%` | `4/3` |
| `30%` | `70%` | `10/7` |
| `40%` | `60%` | `5/3` |
| `50%` | `50%` | `2` |
| `75%` | `25%` | `4` |

---

# 20. Finding Original Price

A product is sold for `₹960` after a `20%` discount.

Original price:

$$
\frac{960}{0.8}
$$

$$
=\boxed{₹1200}
$$

---

# 21. Finding Original Salary

A person's salary becomes `₹54,000` after a `10%` increase.

Original salary:

$$
\frac{54000}{1.1}
$$

$$
=\boxed{₹49,090.91}
$$

If the problem expects an exact integer salary, the given values would normally be chosen accordingly.

---

# 22. Finding Original Population

Population after a `20%` decrease is:

$$
64,000
$$

Original:

$$
\frac{64000}{0.8}
$$

$$
=\boxed{80,000}
$$

---

# 23. Finding Original Marks

After a `25%` increase, marks become:

$$
500
$$

Original:

$$
\frac{500}{1.25}
$$

$$
=\boxed{400}
$$

---

# 24. Finding Original Consumption

After a `20%` decrease, consumption becomes:

$$
80\text{ kg}
$$

Original:

$$
\frac{80}{0.8}
=
\boxed{100\text{ kg}}
$$

---

# 25. Reverse Increase — Fraction Method

Suppose final value is `₹900` after a `50%` increase.

A `50%` increase means:

$$
150\%=\frac32
$$

Therefore:

$$
\text{Original}
=
900\times\frac23
$$

$$
=\boxed{₹600}
$$

---

# 26. Reverse Decrease — Fraction Method

Suppose final value is `₹600` after a `25%` decrease.

Remaining:

$$
75\%=\frac34
$$

Therefore:

$$
\text{Original}
=
600\times\frac43
$$

$$
=\boxed{₹800}
$$

---

# 27. Reverse Percentage With Multiple Changes

Suppose a value:

1. increases by `20%`
2. then decreases by `10%`

Final value:

$$
₹1080
$$

Combined multiplier:

$$
1.2\times0.9
=
1.08
$$

Original:

$$
\frac{1080}{1.08}
=
\boxed{₹1000}
$$

---

# 28. Reverse With Successive Increases

A value increases by:

- `10%`
- then `20%`

Final:

$$
₹1320
$$

Combined multiplier:

$$
1.1\times1.2
=
1.32
$$

Original:

$$
\frac{1320}{1.32}
=
\boxed{₹1000}
$$

---

# 29. Reverse With Successive Decreases

A value decreases by:

- `10%`
- then `20%`

Final:

$$
₹720
$$

Combined multiplier:

$$
0.9\times0.8
=
0.72
$$

Original:

$$
\frac{720}{0.72}
=
\boxed{₹1000}
$$

---

# 30. Reverse Mixed Percentage Changes

A value:

- increases `20%`
- decreases `10%`
- increases `25%`

Final:

$$
₹1500
$$

Combined multiplier:

$$
1.2\times0.9\times1.25
$$

$$
=1.35
$$

Original:

$$
\frac{1500}{1.35}
=
\boxed{₹1111.11}
$$

---

# 31. Reverse Percentage Using Algebra

Suppose a number `x` increases by `25%` and becomes `500`.

Set up:

$$
x+\frac{25}{100}x=500
$$

$$
1.25x=500
$$

Therefore:

$$
x=\boxed{400}
$$

This is useful when the wording is complicated.

---

# 32. Reverse Decrease Using Algebra

Suppose a number `x` decreases by `20%` and becomes `640`.

$$
x-\frac{20}{100}x=640
$$

$$
0.8x=640
$$

Therefore:

$$
x=\boxed{800}
$$

---

# 33. Percentage of Original

Suppose a value after increase is `150%` of original.

If final is:

$$
₹750
$$

then:

$$
750=1.5x
$$

Therefore:

$$
x=\frac{750}{1.5}
$$

$$
=\boxed{₹500}
$$

---

# 34. Percentage of Original — Decrease

Suppose final is `70%` of original.

Final:

$$
₹560
$$

Then:

$$
560=0.7x
$$

Therefore:

$$
x=\frac{560}{0.7}
$$

$$
=\boxed{₹800}
$$

---

# 35. Reverse From Difference

A number increases by `20%`, resulting in an increase of `₹100`.

Since:

$$
20\%\text{ of Original}=100
$$

Therefore:

$$
\frac{20}{100}x=100
$$

$$
x=\boxed{₹500}
$$

Final:

$$
500+100
=
\boxed{₹600}
$$

---

# 36. Reverse From Increase Amount

If a quantity increases by `25%` and the increase is `50`:

$$
25\%\text{ of Original}=50
$$

Therefore:

$$
\frac14x=50
$$

$$
x=\boxed{200}
$$

Final:

$$
200+50
=
\boxed{250}
$$

---

# 37. Reverse From Decrease Amount

If a quantity decreases by `20%` and the decrease is `80`:

$$
20\%\text{ of Original}=80
$$

Therefore:

$$
x=\frac{80}{0.2}
$$

$$
=\boxed{400}
$$

Final:

$$
400-80
=
\boxed{320}
$$

---

# 38. Important Comparison Trap

A value increases from:

$$
80\rightarrow100
$$

Increase:

$$
20
$$

Percentage increase:

$$
\frac{20}{80}\times100
=
\boxed{25\%}
$$

But going backward:

`100 → 80`

Decrease:

$$
\frac{20}{100}\times100
=
\boxed{20\%}
$$

Therefore:

$$
\boxed{
25\%\text{ increase}\ne25\%\text{ decrease}
}
$$

They describe the same two values from different bases.

---

# 39. Reverse Relationship

If A is `25% more than B`:

$$
A=1.25B
$$

Therefore:

$$
B=\frac{A}{1.25}
=
0.8A
$$

So:

$$
\boxed{
B\text{ is 20% less than A}
}
$$

---

# 40. Reverse Percentage Formula

If A is `x% more than B`, then B is:

$$
\boxed{
\frac{x}{100+x}\times100\%
}
$$

less than A.

Example:

A is `25% more than B`.

$$
\frac{25}{125}\times100
=
\boxed{20\%}
$$

---

# 41. If A Is x% Less Than B

If:

$$
A=(1-\frac{x}{100})B
$$

then:

$$
B=\frac{A}{1-x/100}
$$

Therefore B is:

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

# 42. Reverse Percentage Table

| Original → Final | Reverse Final → Original |
|---|---|
| `20% increase` | divide by `1.2` |
| `25% increase` | divide by `1.25` |
| `50% increase` | divide by `1.5` |
| `20% decrease` | divide by `0.8` |
| `25% decrease` | divide by `0.75` |
| `50% decrease` | divide by `0.5` |

---

# 43. Fast Mental Shortcuts

### 20% Increase

Final = `120%`

$$
\boxed{
\text{Original}=\text{Final}\times\frac56
}
$$

### 25% Increase

Final = `125%`

$$
\boxed{
\text{Original}=\text{Final}\times\frac45
}
$$

### 20% Decrease

Final = `80%`

$$
\boxed{
\text{Original}=\text{Final}\times\frac54
}
$$

### 25% Decrease

Final = `75%`

$$
\boxed{
\text{Original}=\text{Final}\times\frac43
}
$$

---

# 44. Reverse Percentage — Common Values

| Change | Quick Reverse |
|---:|---:|
| `10% increase` | × `10/11` |
| `20% increase` | × `5/6` |
| `25% increase` | × `4/5` |
| `50% increase` | × `2/3` |
| `10% decrease` | × `10/9` |
| `20% decrease` | × `5/4` |
| `25% decrease` | × `4/3` |
| `50% decrease` | × `2` |

---

# 45. Reverse Net Percentage Change

If the final value is known after a net change:

### Net increase `x%`

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}{1+x/100}
}
$$

### Net decrease `x%`

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}{1-x/100}
}
$$

---

# 46. Example

A product's price is finally `₹1440` after a net increase of `20%`.

Original:

$$
\frac{1440}{1.2}
=
\boxed{₹1200}
$$

---

# 47. Example

A population is finally `72,000` after a net decrease of `10%`.

Original:

$$
\frac{72000}{0.9}
=
\boxed{80,000}
$$

---

# 48. Reverse Percentage With Area

A square's area becomes `121 cm²` after a `10%` increase in side length.

Side multiplier:

$$
1.1
$$

Area multiplier:

$$
1.1^2
=
1.21
$$

Therefore original area:

$$
\frac{121}{1.21}
=
\boxed{100\text{ cm}^2}
$$

---

# 49. Reverse Percentage With Volume

A cube's volume becomes `1728 cm³` after a `20%` increase in side length.

Volume multiplier:

$$
1.2^3
=
1.728
$$

Original volume:

$$
\frac{1728}{1.728}
=
\boxed{1000\text{ cm}^3}
$$

---

# 50. Important Exam Recognition

Look for words such as:

- originally
- initially
- before increase
- before decrease
- previous price
- original salary
- original population
- initial value
- before discount
- before depreciation
- after increase
- after decrease
- becomes
- reduced to
- increased to

These often indicate a **reverse percentage** problem.

---

# 51. Common Mistakes

> [!warning] Avoid These

### Mistake 1

Subtracting percentage from final after an increase.

Wrong.

### Mistake 2

Adding percentage to final after a decrease.

Wrong.

### Mistake 3

Using the final value as the percentage base.

Wrong.

### Mistake 4

Forgetting that multiple changes compound.

Wrong.

### Mistake 5

Confusing:

`20% more`

with:

`20% less`

They use different bases.

---

# 52. Universal Reverse Method

> [!tip] Exam Shortcut

### Step 1

Identify the **final value**.

### Step 2

Identify each percentage change.

### Step 3

Convert each change to a multiplier.

### Step 4

Multiply all multipliers.

### Step 5

Divide final value by the combined multiplier.

Therefore:

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{\text{Combined Multiplier}}
}
$$

---

# 53. Formula Sheet

> [!important] Must Remember

### Increase

$$
\boxed{
F=P(1+\frac{x}{100})
}
$$

### Original After Increase

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

---

### Decrease

$$
\boxed{
F=P(1-\frac{x}{100})
}
$$

### Original After Decrease

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

---

### Multiple Changes

$$
\boxed{
P=
\frac{F}
{\prod(1\pm x_i/100)}
}
$$

---

# 54. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
20\%\text{ increase}\Rightarrow\text{divide final by }1.2
}
$$

### Pattern 2

$$
\boxed{
20\%\text{ decrease}\Rightarrow\text{divide final by }0.8
}
$$

### Pattern 3

$$
\boxed{
25\%\text{ increase}\Rightarrow\text{multiply final by }\frac45
}
$$

### Pattern 4

$$
\boxed{
25\%\text{ decrease}\Rightarrow\text{multiply final by }\frac43
}
$$

### Pattern 5

$$
\boxed{
\text{Final}=\text{Original}\times\text{Multiplier}
}
$$

Therefore:

$$
\boxed{
\text{Original}=\frac{\text{Final}}{\text{Multiplier}}
}
$$

### Pattern 6

> **Reverse percentage = divide, not subtract.**

### Pattern 7

> **The percentage is based on the original value.**

### Pattern 8

> **For multiple changes, combine the multipliers first.**

### Pattern 9

$$
\boxed{
A\text{ is 25\% more than B}
\Rightarrow
B\text{ is 20\% less than A}
}
$$

### Pattern 10

$$
\boxed{
A\text{ is 20\% less than B}
\Rightarrow
B\text{ is 25\% more than A}
}
$$

---

# 55. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Master these first:

1. Finding original after increase
2. Finding original after decrease
3. Multiplier method
4. Fraction method
5. Shortcut formulas
6. Reverse salary
7. Reverse price
8. Reverse population
9. Reverse marks
10. Reverse consumption
11. Reverse discount
12. Reverse depreciation
13. Multiple percentage changes
14. Reverse net percentage change
15. More-than / less-than conversion
16. Area and volume reverse problems

---

# 56. Practice Checklist

- [ ] Original after `10%` increase
- [ ] Original after `20%` increase
- [ ] Original after `25%` increase
- [ ] Original after `50%` increase
- [ ] Original after `10%` decrease
- [ ] Original after `20%` decrease
- [ ] Original after `25%` decrease
- [ ] Original after `50%` decrease
- [ ] Reverse salary
- [ ] Reverse price
- [ ] Reverse population
- [ ] Reverse marks
- [ ] Reverse consumption
- [ ] Reverse discount
- [ ] Reverse depreciation
- [ ] Reverse successive changes
- [ ] Reverse mixed changes
- [ ] More vs less conversion
- [ ] Area reverse problems
- [ ] Volume reverse problems

---

# 57. Related Topics

- [[03. Percentage]]
- [[Percentage Basics]]
- [[Percentage Comparison]]
- [[Percentage Increase]]
- [[Percentage Decrease]]
- [[Successive Increase]]
- [[Successive Decrease]]
- [[Net Percentage Change]]
- [[Reverse Increase]]
- [[Reverse Decrease]]
- [[Percentage Error]]
- [[Percentage Difference]]
- [[Mixed Percentage Problems]]

---

# 58. Quick Revision

> [!summary] One-Minute Revision

### After Increase

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{1+x/100}
}
$$

### After Decrease

$$
\boxed{
\text{Original}
=
\frac{\text{Final}}
{1-x/100}
}
$$

### Example

Final = `600`, increase = `20%`

$$
600\div1.2
=
\boxed{500}
$$

### Example

Final = `400`, decrease = `20%`

$$
400\div0.8
=
\boxed{500}
$$

### Golden Memory Trick

> **Forward → multiply. Reverse → divide.**

### One-Line Recognition

> **If the question gives you the value AFTER a percentage change and asks for the value BEFORE it, use reverse percentage.**