---
type: concept
subject: aptitude
topic: "Successive Profit and Loss"
parent: "06. Profit Loss and Discount"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - profit-loss
  - successive-profit
  - successive-loss
  - percentage
  - quantitative-aptitude
wikilinks:
  - "[[06. Profit Loss and Discount]]"
  - "[[Profit Percentage]]"
  - "[[Loss Percentage]]"
  - "[[Finding CP]]"
  - "[[Finding SP]]"
---

# Successive Profit and Loss

## 1. Core Concept

> [!summary]
> **Successive Profit and Loss** problems involve multiple profit/loss changes applied one after another.
>
> The most important rule:
>
> > **Successive percentages are applied to the updated value, not the original value.**
>
> Therefore, percentages usually **cannot simply be added or subtracted**.

Example:

An article undergoes:

- 20% profit
- followed by 10% profit

The total increase is **not 30%**.

It is:

$$
20+10+\frac{20\times10}{100}
$$

$$
=32\%
$$

So:

$$
\boxed{32\%\text{ increase}}
$$

---

# 2. Why Successive Percentages Are Different

Suppose the original value is:

$$
100
$$

First increase by 20%:

$$
100+20=120
$$

Then increase 10% on the **new value**:

$$
120+12=132
$$

Final value:

$$
132
$$

Therefore:

$$
\boxed{32\%\text{ total increase}}
$$

Not 30%.

---

# 3. Golden Multiplier Method

The safest method is to convert each percentage into a multiplier.

### Profit of `p%`

$$
\boxed{
Multiplier=\frac{100+p}{100}
}
$$

### Loss of `l%`

$$
\boxed{
Multiplier=\frac{100-l}{100}
}
$$

Then multiply the successive multipliers.

---

# 4. Two Successive Profits

Suppose profits are:

- `a%`
- `b%`

First multiplier:

$$
\frac{100+a}{100}
$$

Second multiplier:

$$
\frac{100+b}{100}
$$

Therefore:

$$
Final=
Initial
\times
\frac{100+a}{100}
\times
\frac{100+b}{100}
$$

Net profit:

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

---

# 5. Example — 20% and 10% Profit

Assume:

$$
CP=100
$$

First 20% profit:

$$
100(1.2)=120
$$

Second 10% profit:

$$
120(1.1)=132
$$

Therefore:

$$
\boxed{32\%\text{ profit}}
$$

Shortcut:

$$
20+10+\frac{20(10)}{100}
$$

$$
=30+2
$$

$$
\boxed{32\%}
$$

---

# 6. Three Successive Profits

Suppose successive profits are:

$$
a\%,b\%,c\%
$$

Then:

$$
Final=
Initial
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
\left(1+\frac c{100}\right)
$$

Net profit percentage:

$$
\boxed{
\left[
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
\left(1+\frac c{100}\right)-1
\right]100
}
$$

---

# 7. Example — Three Successive Profits

Profits:

- 10%
- 20%
- 30%

Multiplier:

$$
1.1\times1.2\times1.3
$$

$$
=1.716
$$

Therefore:

$$
\boxed{71.6\%\text{ profit}}
$$

---

# 8. Successive Losses

Suppose losses are:

- `a%`
- `b%`

Multipliers:

$$
\frac{100-a}{100}
$$

and:

$$
\frac{100-b}{100}
$$

Therefore:

$$
Final=
Initial
\times
\frac{100-a}{100}
\times
\frac{100-b}{100}
$$

Net loss:

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

---

# 9. Example — 20% and 10% Loss

Assume:

$$
Initial=100
$$

First 20% loss:

$$
100(0.8)=80
$$

Second 10% loss:

$$
80(0.9)=72
$$

Final:

$$
72
$$

Therefore:

$$
100-72=28
$$

$$
\boxed{28\%\text{ loss}}
$$

Shortcut:

$$
20+10-\frac{20(10)}{100}
$$

$$
=30-2
$$

$$
\boxed{28\%}
$$

---

# 10. Three Successive Losses

For losses `a%`, `b%`, and `c%`:

$$
Final=
Initial
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
\left(1-\frac c{100}\right)
$$

Net loss:

$$
\boxed{
100-
100
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
\left(1-\frac c{100}\right)
}
$$

---

# 11. Profit Followed by Loss

This is a very common pattern.

Suppose:

- first profit = `a%`
- then loss = `b%`

Multiplier:

$$
\left(1+\frac a{100}\right)
\left(1-\frac b{100}\right)
$$

Net percentage:

$$
a-b-\frac{ab}{100}
$$

Therefore:

$$
\boxed{
Net\%=a-b-\frac{ab}{100}
}
$$

If the result is positive → profit.

If negative → loss.

---

# 12. Example — 20% Profit Then 10% Loss

Assume:

$$
CP=100
$$

20% profit:

$$
100(1.2)=120
$$

10% loss:

$$
120(0.9)=108
$$

Final:

$$
108
$$

Therefore:

$$
\boxed{8\%\text{ profit}}
$$

Shortcut:

$$
20-10-\frac{20(10)}{100}
$$

$$
=20-10-2
$$

$$
\boxed{8\%}
$$

---

# 13. Loss Followed by Profit

Suppose:

- first loss = `a%`
- then profit = `b%`

Multiplier:

$$
\left(1-\frac a{100}\right)
\left(1+\frac b{100}\right)
$$

Net percentage:

$$
\boxed{
b-a-\frac{ab}{100}
}
$$

---

# 14. Example — 20% Loss Then 10% Profit

Assume:

$$
100
$$

20% loss:

$$
100(0.8)=80
$$

10% profit:

$$
80(1.1)=88
$$

Therefore:

$$
\boxed{12\%\text{ overall loss}}
$$

Shortcut:

$$
10-20-\frac{20(10)}{100}
$$

$$
=10-20-2
$$

$$
\boxed{-12\%}
$$

Negative means:

$$
\boxed{12\%\text{ loss}}
$$

---

# 15. Profit and Loss of Equal Percentage

Suppose:

- `p%` profit
- `p%` loss

Then:

$$
(1+\frac p{100})(1-\frac p{100})
$$

Using:

$$
(a+b)(a-b)=a^2-b^2
$$

we get:

$$
1-\frac{p^2}{10000}
$$

Therefore:

$$
\boxed{
Loss\%=\frac{p^2}{100}
}
$$

---

# 16. Example — 20% Profit Then 20% Loss

Assume:

$$
100
$$

20% profit:

$$
120
$$

20% loss:

$$
120(0.8)=96
$$

Final:

$$
96
$$

Loss:

$$
100-96=4
$$

Therefore:

$$
\boxed{4\%\ loss}
$$

---

# 17. Important Trap

> [!warning]
> **20% profit followed by 20% loss does NOT give zero.**

Why?

Because the 20% loss is calculated on the increased amount.

$$
100
\rightarrow120
\rightarrow96
$$

Therefore:

$$
\boxed{4\%\ loss}
$$

---

# 18. Reverse Order

20% loss followed by 20% profit:

$$
100
\rightarrow80
\rightarrow96
$$

Again:

$$
\boxed{4\%\ loss}
$$

So for equal percentages:

> The order does not change the final result.

---

# 19. Unequal Profit and Loss — Order Matters

Suppose:

- 20% profit
- 10% loss

Result:

$$
1.2\times0.9=1.08
$$

So:

$$
\boxed{8\%\ profit}
$$

Reverse:

- 10% loss
- 20% profit

$$
0.9\times1.2=1.08
$$

Still:

$$
\boxed{8\%\ profit}
$$

For simple percentage multipliers, the final result is actually unchanged because multiplication is commutative.

---

# 20. General Rule

For successive changes:

$$
\boxed{
Final=
Initial\times
\prod(1+\text{percentage change})
}
$$

For a profit:

$$
1+\frac p{100}
$$

For a loss:

$$
1-\frac l{100}
$$

---

# 21. Profit → Profit → Loss

Example:

20% profit

10% profit

15% loss

Multiplier:

$$
1.2\times1.1\times0.85
$$

$$
=1.122
$$

Therefore:

$$
\boxed{12.2\%\ profit}
$$

---

# 22. Loss → Loss → Profit

Example:

10% loss

20% loss

25% profit

Multiplier:

$$
0.9\times0.8\times1.25
$$

$$
=0.9
$$

Therefore:

$$
\boxed{10\%\ loss}
$$

---

# 23. Successive Profit With Actual CP

Suppose:

CP = ₹2,000

First profit = 20%

Second profit = 10%.

First SP:

$$
2000(1.2)=₹2400
$$

Second transaction:

$$
2400(1.1)=₹2640
$$

Final:

$$
\boxed{₹2640}
$$

Overall profit:

$$
2640-2000
=
₹640
$$

Profit percentage:

$$
\frac{640}{2000}\times100
=
\boxed{32\%}
$$

---

# 24. Successive Loss With Actual CP

CP = ₹5,000

First loss = 20%

Second loss = 10%.

First value:

$$
5000(0.8)=₹4000
$$

Second:

$$
4000(0.9)=₹3600
$$

Total loss:

$$
5000-3600
=
₹1400
$$

Loss percentage:

$$
\frac{1400}{5000}\times100
=
\boxed{28\%}
$$

---

# 25. Mixed Profit and Loss

Suppose:

CP = ₹10,000

Profit = 30%

Then loss = 20%.

First:

$$
10000(1.3)=₹13000
$$

Second:

$$
13000(0.8)=₹10400
$$

Overall profit:

$$
10400-10000
=
₹400
$$

Therefore:

$$
\boxed{4\%\ profit}
$$

---

# 26. Shortcut for Profit Then Loss

Profit = `a%`

Loss = `b%`

Net:

$$
\boxed{
a-b-\frac{ab}{100}
}
$$

Example:

30% profit and 20% loss:

$$
30-20-\frac{30(20)}{100}
$$

$$
=10-6
$$

$$
\boxed{4\%\ profit}
$$

---

# 27. Shortcut for Loss Then Profit

Loss = `a%`

Profit = `b%`

Net:

$$
\boxed{
b-a-\frac{ab}{100}
}
$$

Example:

30% loss and 20% profit:

$$
20-30-\frac{30(20)}{100}
$$

$$
=-10-6
$$

$$
\boxed{16\%\ loss}
$$

---

# 28. Equal Profit and Loss — Quick Formula

If the same percentage `p%` is applied once as profit and once as loss:

$$
\boxed{
Loss=\frac{p^2}{100}\%
}
$$

Examples:

| p | Overall result |
|---:|---:|
| 10% | 1% loss |
| 20% | 4% loss |
| 25% | 6.25% loss |
| 30% | 9% loss |
| 40% | 16% loss |
| 50% | 25% loss |

---

# 29. Successive Percentage Increase

The same concept applies beyond profit/loss.

If a value increases successively by `a%` and `b%`:

$$
\boxed{
Net\ Increase=
a+b+\frac{ab}{100}
}
$$

Example:

20% followed by 30%:

$$
20+30+6
=
\boxed{56\%}
$$

---

# 30. Successive Percentage Decrease

If a value decreases successively by `a%` and `b%`:

$$
\boxed{
Net\ Decrease=
a+b-\frac{ab}{100}
}
$$

Example:

20% followed by 30%:

$$
20+30-6
=
\boxed{44\%}
$$

---

# 31. Increase Followed by Decrease

Increase = `a%`

Decrease = `b%`

Net:

$$
\boxed{
a-b-\frac{ab}{100}
}
$$

Example:

Increase = 25%

Decrease = 20%.

$$
25-20-\frac{25(20)}{100}
$$

$$
=25-20-5
$$

$$
\boxed{0\%}
$$

So the final value returns to the original value.

---

# 32. Percentage Needed to Recover a Loss

A very important reverse pattern:

If a value decreases by `l%`, what percentage increase is required to return to the original?

Formula:

$$
\boxed{
Required\ Increase=
\frac{100l}{100-l}
}
$$

---

# 33. Example — 20% Loss

Suppose:

Original = 100

After 20% loss:

$$
100(0.8)=80
$$

To return from 80 to 100:

Increase:

$$
20
$$

Percentage relative to 80:

$$
\frac{20}{80}\times100
=
\boxed{25\%}
$$

Therefore:

> 20% loss requires **25% increase** to recover.

---

# 34. Recovery Table

| Initial Loss | Required Increase |
|---:|---:|
| 10% | 11.11% |
| 20% | 25% |
| 25% | 33.33% |
| 30% | 42.86% |
| 40% | 66.67% |
| 50% | 100% |
| 60% | 150% |
| 75% | 300% |

> [!important]
> **Loss % and required recovery % are not equal.**

---

# 35. Percentage Increase Needed After Profit

If a value increases by `p%`, then the percentage decrease required to return to the original is:

$$
\boxed{
Required\ Decrease=
\frac{100p}{100+p}
}
$$

Example:

Value increases by 25%.

Required decrease:

$$
\frac{100(25)}{125}
=
\boxed{20\%}
$$

Check:

$$
100\rightarrow125
$$

20% of 125:

$$
25
$$

$$
125-25=100
$$

Correct.

---

# 36. Recovery After Profit — Table

| Initial Increase | Required Decrease |
|---:|---:|
| 10% | 9.09% |
| 20% | 16.67% |
| 25% | 20% |
| 50% | 33.33% |
| 100% | 50% |

---

# 37. Profit-Loss Recovery Connection

These are inverse relationships.

### After `l%` loss:

$$
\boxed{
Recovery\%= \frac{100l}{100-l}
}
$$

### After `p%` profit:

$$
\boxed{
Reduction\%= \frac{100p}{100+p}
}
$$

---

# 38. Finding Unknown Successive Percentage

Suppose:

A value increases by 20%, then by `x%`, resulting in a total 44% increase.

Use:

$$
1.2\left(1+\frac{x}{100}\right)=1.44
$$

Therefore:

$$
1+\frac{x}{100}
=
\frac{1.44}{1.2}
$$

$$
=1.2
$$

So:

$$
\boxed{x=20\%}
$$

---

# 39. Finding Unknown Loss

A product undergoes 20% loss followed by `x%` loss and finally has 36% total loss.

Final multiplier:

$$
1-0.36=0.64
$$

Therefore:

$$
0.8(1-\frac{x}{100})=0.64
$$

$$
1-\frac{x}{100}=0.8
$$

Thus:

$$
\boxed{x=20\%}
$$

---

# 40. Finding Unknown Profit

A value increases by 20% and then by `x%`, giving 32% total increase.

$$
1.2(1+\frac{x}{100})=1.32
$$

Therefore:

$$
1+\frac{x}{100}=1.1
$$

Hence:

$$
\boxed{x=10\%}
$$

---

# 41. Finding Unknown Discount

Suppose an article is marked up by 50% and then discounted by `d%`, resulting in 20% profit.

We know:

$$
1.5(1-\frac d{100})=1.2
$$

Therefore:

$$
1-\frac d{100}
=
\frac{1.2}{1.5}
$$

$$
=0.8
$$

Hence:

$$
\boxed{d=20\%}
$$

---

# 42. Successive Discounts vs Successive Profit

Both follow multiplication.

### Successive discounts

$$
\boxed{
Final=Initial(1-a/100)(1-b/100)
}
$$

### Successive profits

$$
\boxed{
Final=Initial(1+a/100)(1+b/100)
}
$$

### Mixed

$$
\boxed{
Final=Initial
\prod
\left(1\pm\frac{x}{100}\right)
}
$$

---

# 43. Successive Discount Example

MP = ₹10,000

Discounts:

- 20%
- 10%

First:

$$
10000(0.8)=8000
$$

Second:

$$
8000(0.9)=7200
$$

Final SP:

$$
\boxed{₹7200}
$$

Net discount:

$$
28\%
$$

---

# 44. Successive Markup Example

CP = ₹10,000

Markup 20%, then another 10%.

First:

$$
10000(1.2)=12000
$$

Second:

$$
12000(1.1)=13200
$$

Final:

$$
\boxed{₹13200}
$$

Net increase:

$$
\boxed{32\%}
$$

---

# 45. Mixed Transaction Chain

Consider:

```text
CP
 ↓
+20%
 ↓
-10%
 ↓
+25%
 ↓
Final SP
```

Multiplier:

$$
1.2\times0.9\times1.25
$$

$$
=1.35
$$

Therefore:

$$
\boxed{35\%\ overall\ profit}
$$

---

# 46. Actual Value Method vs Formula Method

### Method 1 — Assume 100

Best for percentage-only problems.

Example:

20% profit → 10% loss.

$$
100\rightarrow120\rightarrow108
$$

Answer:

$$
8\%\ profit
$$

### Method 2 — Multiplier

$$
1.2\times0.9=1.08
$$

Answer:

$$
8\%\ profit
$$

### Method 3 — Direct Formula

$$
20-10-\frac{20(10)}{100}
=
8\%
$$

> [!tip]
> Use the **multiplier method** when there are many successive changes.

---

# 47. How to Recognize a Successive Problem

Look for words such as:

- first
- then
- afterward
- subsequently
- followed by
- next
- again
- another
- successive
- twice
- repeatedly
- after increasing
- after decreasing

Example:

> "A price is increased by 20% and then reduced by 10%."

This is a **successive percentage** problem.

---

# 48. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Direct Addition

Wrong:

$$
20\%+10\%=30\%
$$

for successive increases.

Correct:

$$
\boxed{32\%}
$$

### Mistake 2 — Using Original Value for Every Change

The second percentage applies to the **new value**.

### Mistake 3 — Equal Profit and Loss = Zero

Wrong.

20% profit followed by 20% loss:

$$
\boxed{4\%\ loss}
$$

### Mistake 4 — Ignoring Percentage Base

Every successive percentage uses the immediately previous value as its base.

### Mistake 5 — Mixing Profit/Loss Signs

Profit:

$$
+
$$

Loss:

$$
-
$$

Use multipliers to avoid sign errors.

---

# 49. High-Yield Exam Patterns

> [!important] Must Master

1. Two successive profits
2. Three successive profits
3. Two successive losses
4. Three successive losses
5. Profit followed by loss
6. Loss followed by profit
7. Equal profit and loss
8. Successive discounts
9. Successive markups
10. Mixed percentage changes
11. Recovery after loss
12. Recovery after profit
13. Unknown successive percentage
14. Unknown discount
15. Unknown profit
16. Unknown loss
17. Actual-value problems
18. Multiplier problems
19. Reverse percentage
20. Multi-step transaction problems

---

# 50. Formula Sheet

> [!important] Must Remember

### Two Successive Profits

$$
\boxed{
Net\ Profit\%=
a+b+\frac{ab}{100}
}
$$

### Two Successive Losses

$$
\boxed{
Net\ Loss\%=
a+b-\frac{ab}{100}
}
$$

### Profit Then Loss

$$
\boxed{
Net\%=
a-b-\frac{ab}{100}
}
$$

### Loss Then Profit

$$
\boxed{
Net\%=
b-a-\frac{ab}{100}
}
$$

### Equal Profit and Loss

$$
\boxed{
Loss\%=\frac{p^2}{100}
}
$$

### Recovery After Loss

$$
\boxed{
Recovery\%=
\frac{100l}{100-l}
}
$$

### Reduction After Profit

$$
\boxed{
Reduction\%=
\frac{100p}{100+p}
}
$$

### General Multiplier

$$
\boxed{
Final=Initial
\prod
\left(1\pm\frac{x}{100}\right)
}
$$

### Successive Discount

$$
\boxed{
Net\ Discount\%=
a+b-\frac{ab}{100}
}
$$

---

# 51. Quick Revision

> [!summary] One-Minute Revision

### Profit Multiplier

$$
\boxed{
1+\frac{p}{100}
}
$$

### Loss Multiplier

$$
\boxed{
1-\frac{l}{100}
}
$$

### Two Profits

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

### Two Losses

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

### Profit + Loss

$$
\boxed{
a-b-\frac{ab}{100}
}
$$

### Equal Profit/Loss

$$
\boxed{
p^2/100\%\ Loss
}
$$

### Recovery

$$
\boxed{
\text{Loss }l\%
\Rightarrow
\frac{100l}{100-l}\%\ increase
}
$$

### Golden Memory Trick

> **Successive percentages = MULTIPLY, don't simply add.**

```text
+20% → ×1.20
-10% → ×0.90
+30% → ×1.30
-15% → ×0.85
```

Then:

$$
\boxed{
Final=Initial\times\text{all multipliers}
}
$$

---

# 52. Exam Recognition Map

```text
SUCCESSIVE PROFIT / LOSS
│
├── Successive Profit
│   ├── 2 profits
│   ├── 3 profits
│   └── Multiple profits
│
├── Successive Loss
│   ├── 2 losses
│   ├── 3 losses
│   └── Multiple losses
│
├── Mixed
│   ├── Profit → Loss
│   ├── Loss → Profit
│   └── Multiple mixed changes
│
├── Special Patterns
│   ├── Equal profit/loss
│   ├── Recovery
│   └── Reverse percentage
│
├── Discount
│   ├── Successive discounts
│   └── Net discount
│
├── Unknown Percentage
│   ├── Find profit
│   ├── Find loss
│   └── Find discount
│
└── Advanced
    ├── Markup
    ├── Discount
    ├── Tax
    └── Multi-step transactions
```

> [!success]
> **Core skill:** Successive profit/loss is a **multiplier problem**.
>
> Convert every change into a multiplier:
>
> $$\boxed{
> Profit\ p\%\rightarrow1+\frac p{100}
> }$$
>
> $$\boxed{
> Loss\ l\%\rightarrow1-\frac l{100}
> }$$
>
> Then multiply all the changes.
>
> **Never blindly add successive percentages.**