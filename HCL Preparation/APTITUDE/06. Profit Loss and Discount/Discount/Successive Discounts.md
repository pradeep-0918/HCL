---
type: concept
subject: aptitude
topic: "Successive Discounts"
parent: "06. Profit Loss and Discount"
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - profit-loss
  - discount
  - successive-discount
  - marked-price
  - selling-price
  - quantitative-aptitude
wikilinks:
  - "[[06. Profit Loss and Discount]]"
  - "[[Discount Basics]]"
  - "[[Discount Percentage]]"
  - "[[Marked Price]]"
  - "[[Selling Price After Discount]]"
---

# Successive Discounts

## 1. Core Concept

> [!summary]
> **Successive Discounts** means two or more discounts are applied one after another.
>
> The crucial rule is:
>
> > **The second discount is applied to the reduced price, not the original Marked Price.**
>
> Therefore, successive discounts cannot normally be added directly.

For discounts `a%` and `b%`:

$$
\boxed{
Net\ Discount\%=
a+b-\frac{ab}{100}
}
$$

---

# 2. Why Successive Discounts Matter

Suppose a product has:

- First discount = 20%
- Second discount = 10%

A common mistake is:

$$
20+10=30\%
$$

This is wrong.

The second 10% discount is applied after the first 20% discount.

Correct answer:

$$
\boxed{28\%}
$$

---

# 3. Basic Example

Take:

$$
MP=100
$$

First discount = 20%.

$$
100-20=80
$$

Second discount = 10% of 80:

$$
80-\frac{10}{100}(80)
$$

$$
=80-8
$$

$$
=72
$$

Final price:

$$
\boxed{72}
$$

Therefore total discount:

$$
100-72=28
$$

So:

$$
\boxed{28\%\ discount}
$$

---

# 4. Golden Multiplier Method

This is the safest method.

For a discount of `d%`:

$$
\boxed{
Multiplier=\frac{100-d}{100}
}
$$

Therefore:

```text
10% discount → × 0.90
20% discount → × 0.80
25% discount → × 0.75
30% discount → × 0.70
40% discount → × 0.60
50% discount → × 0.50
```

For successive discounts, multiply all the multipliers.

---

# 5. Two Successive Discounts

For discounts `a%` and `b%`:

$$
SP=
MP
\left(\frac{100-a}{100}\right)
\left(\frac{100-b}{100}\right)
$$

Therefore:

$$
\boxed{
SP=
MP
\frac{(100-a)(100-b)}{10000}
}
$$

---

# 6. Deriving the Net Discount Formula

We know:

$$
SP=
MP
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
$$

Expand:

$$
SP=
MP
\left(
1-\frac a{100}-\frac b{100}
+\frac{ab}{10000}
\right)
$$

Therefore the total reduction is:

$$
\frac a{100}
+
\frac b{100}
-
\frac{ab}{10000}
$$

Multiplying by 100:

$$
\boxed{
Net\ Discount\%=
a+b-\frac{ab}{100}
}
$$

---

# 7. Example — 20% and 10%

Using the shortcut:

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

# 8. Example — 25% and 20%

$$
25+20-\frac{25(20)}{100}
$$

$$
=45-5
$$

$$
\boxed{40\%}
$$

Therefore two discounts of 25% and 20% are equivalent to a single:

$$
\boxed{40\%\ discount}
$$

---

# 9. Example — 30% and 10%

$$
30+10-\frac{30(10)}{100}
$$

$$
=40-3
$$

$$
\boxed{37\%}
$$

---

# 10. Example — 40% and 20%

$$
40+20-\frac{40(20)}{100}
$$

$$
=60-8
$$

$$
\boxed{52\%}
$$

---

# 11. Example With Actual MP

MP = ₹5,000

Discounts:

- 20%
- 10%

First discount:

$$
5000(0.8)=₹4000
$$

Second discount:

$$
4000(0.9)=₹3600
$$

Therefore:

$$
\boxed{SP=₹3600}
$$

Total discount:

$$
5000-3600
=
₹1400
$$

Discount percentage:

$$
\frac{1400}{5000}\times100
=
\boxed{28\%}
$$

---

# 12. Fast Method With Net Discount

MP = ₹5,000

Discounts = 20%, 10%.

Net discount:

$$
20+10-\frac{20(10)}{100}
=
28\%
$$

Therefore:

$$
SP=5000(0.72)
$$

$$
\boxed{₹3600}
$$

This is faster than calculating each discount separately.

---

# 13. Three Successive Discounts

For discounts `a%`, `b%`, and `c%`:

$$
\boxed{
SP=
MP
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
\left(1-\frac c{100}\right)
}
$$

This multiplier method is preferred for three or more discounts.

---

# 14. Example — 10%, 20%, 30%

Take:

$$
MP=100
$$

After 10%:

$$
100(0.9)=90
$$

After 20%:

$$
90(0.8)=72
$$

After 30%:

$$
72(0.7)=50.4
$$

Therefore:

$$
SP=50.4
$$

Net discount:

$$
100-50.4
=
\boxed{49.6\%}
$$

---

# 15. Example With Actual MP

MP = ₹10,000

Discounts:

10%, 20%, 25%.

$$
SP=
10000(0.9)(0.8)(0.75)
$$

$$
=10000(0.54)
$$

$$
\boxed{₹5400}
$$

Net discount:

$$
100-54
=
\boxed{46\%}
$$

---

# 16. Successive Discounts Table

| Discounts | Equivalent Discount |
|---|---:|
| 10%, 10% | 19% |
| 10%, 20% | 28% |
| 10%, 30% | 37% |
| 20%, 20% | 36% |
| 20%, 30% | 44% |
| 25%, 20% | 40% |
| 25%, 25% | 43.75% |
| 30%, 30% | 51% |
| 40%, 20% | 52% |
| 50%, 20% | 60% |

---

# 17. Equal Successive Discounts

If the same discount `d%` is applied twice:

$$
Net\ Discount
=
d+d-\frac{d^2}{100}
$$

Therefore:

$$
\boxed{
Net\ Discount=
2d-\frac{d^2}{100}
}
$$

---

# 18. Example — Two 20% Discounts

$$
20+20-\frac{20^2}{100}
$$

$$
=40-4
$$

$$
\boxed{36\%}
$$

So:

```text
20% + 20%
≠ 40%
= 36%
```

---

# 19. Example — Two 25% Discounts

$$
25+25-\frac{25^2}{100}
$$

$$
=50-6.25
$$

$$
\boxed{43.75\%}
$$

---

# 20. Three Equal Discounts

If discount `d%` is applied three times:

$$
SP=
MP
\left(1-\frac d{100}\right)^3
$$

Therefore:

$$
\boxed{
Net\ Discount\%=
\left[
1-\left(1-\frac d{100}\right)^3
\right]100
}
$$

Example:

Three 20% discounts:

$$
SP=MP(0.8)^3
$$

$$
=0.512MP
$$

Therefore:

$$
\boxed{48.8\%\ discount}
$$

---

# 21. Successive Discount vs Single Discount

Suppose:

Single discount = 30%.

Then:

$$
SP=70\%\ MP
$$

Suppose:

Two discounts = 20% and 10%.

Then:

$$
SP=80\%\times90\%
$$

$$
=72\%
$$

Therefore:

- Single 30% discount → SP = 70% MP
- Successive 20% + 10% → SP = 72% MP

So:

$$
\boxed{30\%\ discount\ is\ better}
$$

---

# 22. Comparing Discount Offers

MP = ₹10,000.

### Offer A

30% single discount:

$$
SP_A=10000(0.7)
=
₹7000
$$

### Offer B

20% + 10%:

$$
SP_B=10000(0.8)(0.9)
$$

$$
=₹7200
$$

Therefore:

$$
\boxed{
Offer\ A\ saves\ ₹200\ more
}
$$

---

# 23. Equivalent Single Discount

For two discounts `a%` and `b%`:

$$
\boxed{
Equivalent\ Discount=
a+b-\frac{ab}{100}
}
$$

This is one of the most important aptitude formulas.

---

# 24. Finding the Second Discount

Suppose:

First discount = `a%`

Equivalent discount = `D%`

Second discount = `x%`.

Then:

$$
D=a+x-\frac{ax}{100}
$$

Rearrange:

$$
D-a=x\left(1-\frac a{100}\right)
$$

Therefore:

$$
\boxed{
x=
\frac{100(D-a)}{100-a}
}
$$

---

# 25. Example — Find Second Discount

First discount = 20%.

Equivalent discount = 40%.

Let second discount = `x`.

$$
x=
\frac{100(40-20)}{100-20}
$$

$$
=\frac{2000}{80}
$$

$$
\boxed{25\%}
$$

Check:

$$
20+25-\frac{20(25)}{100}
$$

$$
=45-5
=
40\%
$$

Correct.

---

# 26. Finding First Discount

Suppose:

Second discount = 20%.

Equivalent discount = 40%.

By symmetry:

$$
\boxed{First\ discount=25\%}
$$

Because:

$$
25+20-\frac{25(20)}{100}
=
40\%
$$

---

# 27. Finding Unknown Discount Using Multipliers

Suppose:

First discount = 20%.

Second discount = `x%`.

Equivalent discount = 36%.

Final percentage:

$$
100-36=64\%
$$

Therefore:

$$
0.8(1-\frac{x}{100})=0.64
$$

So:

$$
1-\frac{x}{100}=0.8
$$

Hence:

$$
\boxed{x=20\%}
$$

---

# 28. Successive Discount With Profit

A product is marked above CP and then successive discounts are given.

Example:

CP = ₹1,000

Markup = 50%.

Discounts = 20%, 10%.

First find MP:

$$
MP=1000(1.5)
=
₹1500
$$

Apply discounts:

$$
SP=1500(0.8)(0.9)
$$

$$
=₹1080
$$

Profit:

$$
1080-1000
=
₹80
$$

Therefore:

$$
\boxed{8\%\ profit}
$$

---

# 29. Direct Formula — Markup + Successive Discounts

If:

- markup = `m%`
- discounts = `a%`, `b%`

then:

$$
\boxed{
SP=
CP
\left(\frac{100+m}{100}\right)
\left(\frac{100-a}{100}\right)
\left(\frac{100-b}{100}\right)
}
$$

---

# 30. Example

CP = ₹2,000

Markup = 40%

Discounts = 20% and 10%.

$$
SP=
2000(1.4)(0.8)(0.9)
$$

$$
=₹2016
$$

Therefore:

$$
Profit=2016-2000
=
₹16
$$

Profit percentage:

$$
\boxed{0.8\%}
$$

---

# 31. Successive Discounts and No Profit/Loss

Suppose:

CP = ₹1,000

Markup = 50%.

Then:

$$
MP=₹1500
$$

Seller wants no profit/loss.

Required SP:

$$
₹1000
$$

Suppose two successive discounts are 20% and `x%`.

Then:

$$
1500(0.8)(1-\frac{x}{100})
=
1000
$$

Therefore:

$$
1-\frac{x}{100}
=
\frac{1000}{1200}
$$

$$
=\frac56
$$

Thus:

$$
\boxed{x=16\frac23\%}
$$

---

# 32. Successive Discount and Desired Profit

Suppose:

CP = ₹1,000

Markup = 50%.

Desired profit = 8%.

Discounts:

20% and `x%`.

Desired SP:

$$
1000(1.08)=1080
$$

MP:

$$
1000(1.5)=1500
$$

Therefore:

$$
1500(0.8)(1-\frac{x}{100})
=
1080
$$

$$
1200(1-\frac{x}{100})
=
1080
$$

$$
1-\frac{x}{100}=0.9
$$

Hence:

$$
\boxed{x=10\%}
$$

---

# 33. Successive Discounts and Tax

Suppose:

MP = ₹10,000

Discounts = 20% and 10%

Tax = 18%.

First discounts:

$$
SP=10000(0.8)(0.9)
$$

$$
=₹7200
$$

Tax:

$$
7200(0.18)=₹1296
$$

Final payment:

$$
7200+1296
=
\boxed{₹8496}
$$

---

# 34. Reverse Successive Discount

Suppose:

Final SP = ₹7,200

Discounts = 20% and 10%.

Find MP.

Since:

$$
SP=MP(0.8)(0.9)
$$

$$
7200=0.72MP
$$

Therefore:

$$
MP=\frac{7200}{0.72}
$$

$$
\boxed{₹10000}
$$

---

# 35. Reverse Using Equivalent Discount

20% and 10% give:

$$
28\%\ equivalent\ discount
$$

Therefore:

$$
SP=72\%\ MP
$$

If:

$$
SP=₹7200
$$

then:

$$
MP=
7200\times\frac{100}{72}
$$

$$
\boxed{₹10000}
$$

---

# 36. Successive Discount and Recovery

Suppose a price is reduced by 20% and then 10%.

Net discount:

$$
28\%
$$

To return to the original price:

$$
Recovery=
\frac{100(28)}{100-28}
$$

$$
=\frac{2800}{72}
$$

$$
\boxed{38.89\%}
$$

---

# 37. Why Addition Fails

Consider:

$$
MP=1000
$$

20% discount:

$$
1000-200=800
$$

Then 10% discount:

$$
800-80=720
$$

Total discount:

$$
1000-720
=
280
$$

Percentage:

$$
\frac{280}{1000}\times100
=
28\%
$$

The second 10% was applied to **₹800**, not ₹1,000.

---

# 38. Key Pattern

> [!important]
> Every successive discount changes the base.

```text
MP
 ↓ 20%
80% of MP
 ↓ 10%
90% of the new value
 ↓
Final SP
```

Therefore:

$$
\boxed{
Final=MP\times0.8\times0.9
}
$$

---

# 39. Common Exam Shortcut

For two discounts:

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

For three or more discounts:

> Prefer the multiplier method.

Example:

10%, 20%, 30%.

$$
0.9\times0.8\times0.7
=
0.504
$$

Therefore:

$$
\boxed{49.6\%\ discount}
$$

---

# 40. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Adding Discounts

Wrong:

$$
20+10=30\%
$$

Correct:

$$
\boxed{28\%}
$$

### Mistake 2 — Applying Every Discount to MP

The second discount applies to the already discounted price.

### Mistake 3 — Using CP as the Base

Discount percentage is based on MP.

### Mistake 4 — Confusing Successive Discounts With Successive Profits

Both use multipliers, but the sign differs.

Discount:

$$
1-\frac d{100}
$$

Profit:

$$
1+\frac p{100}
$$

### Mistake 5 — Forgetting the Order of Operations

```text
MP
 ↓
Discount 1
 ↓
Discount 2
 ↓
SP
```

---

# 41. High-Yield Exam Patterns

> [!important] Must Master

1. Two successive discounts
2. Three successive discounts
3. Equal successive discounts
4. Equivalent single discount
5. Find final SP
6. Find MP
7. Find second discount
8. Find first discount
9. Compare single vs successive discounts
10. Markup + successive discounts
11. Successive discounts + profit
12. Successive discounts + loss
13. No-profit condition
14. Desired profit
15. Reverse successive discounts
16. Successive discount + tax
17. Customer savings
18. Recovery percentage
19. Mixed percentage chains
20. Multi-step pricing problems

---

# 42. Formula Sheet

> [!important] Must Remember

### Two Successive Discounts

$$
\boxed{
D_{net}=
a+b-\frac{ab}{100}
}
$$

### Final SP

$$
\boxed{
SP=
MP
\frac{(100-a)(100-b)}{10000}
}
$$

### Multiple Discounts

$$
\boxed{
SP=
MP\prod
\left(1-\frac{d_i}{100}\right)
}
$$

### Equivalent Discount

$$
\boxed{
D_{eq}=100\left(1-\prod
\left(1-\frac{d_i}{100}\right)\right)
}
$$

### Second Discount

$$
\boxed{
b=
\frac{100(D-a)}{100-a}
}
$$

### Reverse MP

For two discounts:

$$
\boxed{
MP=
\frac{SP}
{(1-a/100)(1-b/100)}
}
$$

### Recovery After Net Discount

$$
\boxed{
Recovery\%=
\frac{100D}{100-D}
}
$$

### Markup + Two Discounts

$$
\boxed{
SP=
CP
\left(\frac{100+m}{100}\right)
\left(\frac{100-a}{100}\right)
\left(\frac{100-b}{100}\right)
}
$$

---

# 43. Quick Revision

> [!summary] One-Minute Revision

### One Discount

$$
\boxed{
SP=MP\frac{100-d}{100}
}
$$

### Two Discounts

$$
\boxed{
SP=MP
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
}
$$

### Equivalent Discount

$$
\boxed{
a+b-\frac{ab}{100}
}
$$

### Example

20% + 10%:

$$
20+10-2
=
\boxed{28\%}
$$

### Three Discounts

```text
Convert each discount to a multiplier
        ↓
Multiply all multipliers
        ↓
Get final SP
        ↓
Compare with MP
        ↓
Find net discount
```

### Golden Memory Trick

> **Successive discount = MULTIPLY, not ADD.**

```text
20% → ×0.80
10% → ×0.90

0.80 × 0.90 = 0.72

SP = 72% of MP
Net Discount = 28%
```

---

# 44. Exam Recognition Map

```text
SUCCESSIVE DISCOUNTS
│
├── Two Discounts
│   ├── Find SP
│   ├── Find Net Discount
│   └── Equivalent Discount
│
├── Three or More
│   ├── Multiplier Method
│   └── Final SP
│
├── Unknown
│   ├── Find First Discount
│   ├── Find Second Discount
│   └── Find Missing Discount
│
├── Reverse
│   ├── Find MP
│   └── Recover Original Price
│
├── Profit / Loss
│   ├── Markup + Discount
│   ├── Desired Profit
│   └── No Profit/Loss
│
├── Comparison
│   ├── Single Discount
│   ├── Successive Discount
│   └── Better Offer
│
└── Applications
    ├── Customer Savings
    ├── Tax / GST
    └── Multi-step Pricing
```

> [!success]
> **Core skill:** In successive discount problems, each new discount is applied to the **current reduced price**.
>
> $$\boxed{
> SP=
> MP\prod
> \left(1-\frac{d_i}{100}\right)
> }$$
>
> For two discounts:
>
> $$\boxed{
> Net\ Discount\%=
> a+b-\frac{ab}{100}
> }$$
>
> **Never simply add successive discounts.**