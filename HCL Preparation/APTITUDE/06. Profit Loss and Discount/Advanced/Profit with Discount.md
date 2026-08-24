---
type: concept
subject: aptitude
topic: "Profit with Discount"
parent: "06. Profit Loss and Discount"
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - profit-loss
  - profit
  - discount
  - marked-price
  - selling-price
  - quantitative-aptitude
wikilinks:
  - "[[06. Profit Loss and Discount]]"
  - "[[Cost Price]]"
  - "[[Selling Price]]"
  - "[[Marked Price]]"
  - "[[Discount Percentage]]"
  - "[[Successive Discounts]]"
---

# Profit with Discount

## 1. Core Concept

> [!summary]
> **Profit with Discount** problems combine three important quantities:
>
> $$\boxed{CP\rightarrow MP\rightarrow SP}$$
>
> - **CP** = Cost Price
> - **MP** = Marked Price
> - **SP** = Selling Price
>
> The seller first marks the product above CP and then gives a discount on MP.
>
> Even after giving a discount, the seller can still make a profit if the final SP is greater than CP.

---

# 2. Complete Transaction Flow

```text
Cost Price (CP)
      ↓
    Markup
      ↓
Marked Price (MP)
      ↓
   Discount
      ↓
Selling Price (SP)
      ↓
Compare SP with CP
      ↓
Profit / Loss
```

The most important relationships are:

$$
\boxed{
MP>CP
}
$$

usually when markup is given, and:

$$
\boxed{
SP<MP
}
$$

when a discount is given.

Finally:

```text
SP > CP → Profit
SP = CP → No Profit / No Loss
SP < CP → Loss
```

---

# 3. Basic Formulas

### Profit

$$
\boxed{
Profit=SP-CP
}
$$

### Profit Percentage

$$
\boxed{
Profit\%=
\frac{SP-CP}{CP}\times100
}
$$

### Discount

$$
\boxed{
Discount=MP-SP
}
$$

### Discount Percentage

$$
\boxed{
Discount\%=
\frac{MP-SP}{MP}\times100
}
$$

---

# 4. The Most Important Distinction

> [!important]
> **Profit percentage and discount percentage have different bases.**

### Profit %

Based on:

$$
\boxed{CP}
$$

### Discount %

Based on:

$$
\boxed{MP}
$$

Example:

CP = ₹1,000

MP = ₹1,500

SP = ₹1,200.

Profit:

$$
1200-1000=₹200
$$

Profit %:

$$
\frac{200}{1000}\times100
=
\boxed{20\%}
$$

Discount:

$$
1500-1200=₹300
$$

Discount %:

$$
\frac{300}{1500}\times100
=
\boxed{20\%}
$$

Both happen to be 20%, but their bases are different.

---

# 5. Markup Percentage

Markup is the increase from CP to MP.

$$
\boxed{
Markup=MP-CP
}
$$

Markup percentage:

$$
\boxed{
Markup\%=
\frac{MP-CP}{CP}\times100
}
$$

If markup = `m%`:

$$
\boxed{
MP=CP\frac{100+m}{100}
}
$$

---

# 6. Discount Percentage

If discount = `d%`:

$$
\boxed{
SP=MP\frac{100-d}{100}
}
$$

Therefore, when both markup and discount are involved:

$$
\boxed{
CP\rightarrow Markup\rightarrow MP
\rightarrow Discount\rightarrow SP
}
$$

---

# 7. Basic Example

CP = ₹1,000

Markup = 50%

Discount = 20%.

### Step 1 — Find MP

$$
MP=1000\times\frac{150}{100}
$$

$$
MP=₹1500
$$

### Step 2 — Find SP

$$
SP=1500\times\frac{80}{100}
$$

$$
SP=₹1200
$$

### Step 3 — Find Profit

$$
Profit=1200-1000
$$

$$
=₹200
$$

### Step 4 — Profit %

$$
\frac{200}{1000}\times100
$$

$$
\boxed{20\%}
$$

---

# 8. Fast Percentage Method

Assume:

$$
CP=100
$$

Markup = 50%.

Therefore:

$$
MP=150
$$

Discount = 20%.

$$
SP=150\times0.8
$$

$$
=120
$$

Since:

$$
CP=100
$$

Profit:

$$
120-100=20
$$

Therefore:

$$
\boxed{20\%\ profit}
$$

> [!tip]
> In pure percentage problems, taking **CP = 100** is often the fastest method.

---

# 9. Direct Formula

If:

- Markup = `m%`
- Discount = `d%`

then:

$$
MP=CP\frac{100+m}{100}
$$

and:

$$
SP=MP\frac{100-d}{100}
$$

Therefore:

$$
\boxed{
SP=
CP
\frac{(100+m)(100-d)}{10000}
}
$$

---

# 10. Net Profit Formula

Profit percentage is:

$$
\boxed{
Profit\%=
m-d-\frac{md}{100}
}
$$

This is one of the most important formulas in Profit-Loss-Discount aptitude.

---

# 11. Derivation of Net Profit Formula

Assume:

$$
CP=100
$$

After markup `m%`:

$$
MP=100+m
$$

After discount `d%`:

$$
SP=(100+m)\frac{100-d}{100}
$$

Expand:

$$
SP=
100+m-d-\frac{md}{100}
$$

Since CP = 100:

$$
Profit\%=
SP-100
$$

Therefore:

$$
\boxed{
Profit\%=
m-d-\frac{md}{100}
}
$$

---

# 12. Example — Markup 40%, Discount 10%

Using the shortcut:

$$
Profit\%=40-10-\frac{40(10)}{100}
$$

$$
=40-10-4
$$

$$
\boxed{26\%}
$$

---

# 13. Example — Markup 50%, Discount 20%

$$
Profit\%=50-20-\frac{50(20)}{100}
$$

$$
=50-20-10
$$

$$
\boxed{20\%}
$$

---

# 14. Example — Markup 30%, Discount 10%

$$
Profit\%=30-10-\frac{30(10)}{100}
$$

$$
=30-10-3
$$

$$
\boxed{17\%}
$$

---

# 15. Example — Markup 25%, Discount 20%

$$
Profit\%=25-20-\frac{25(20)}{100}
$$

$$
=25-20-5
$$

$$
\boxed{0\%}
$$

Therefore:

$$
\boxed{\text{No Profit, No Loss}}
$$

---

# 16. Example — Markup 20%, Discount 25%

$$
Profit\%=20-25-\frac{20(25)}{100}
$$

$$
=20-25-5
$$

$$
\boxed{-10\%}
$$

Therefore:

$$
\boxed{10\%\ loss}
$$

---

# 17. Quick Decision Rule

For markup `m%` and discount `d%`:

$$
Profit\%=m-d-\frac{md}{100}
$$

Therefore:

```text
Result > 0 → Profit
Result = 0 → No Profit / No Loss
Result < 0 → Loss
```

---

# 18. Finding Selling Price Directly

If:

CP = `C`

Markup = `m%`

Discount = `d%`

then:

$$
\boxed{
SP=
C
\left(\frac{100+m}{100}\right)
\left(\frac{100-d}{100}\right)
}
$$

This is usually faster than separately calculating MP if only SP is required.

---

# 19. Example

CP = ₹2,000

Markup = 40%

Discount = 10%.

$$
SP=
2000(1.4)(0.9)
$$

$$
=₹2520
$$

Profit:

$$
2520-2000
=
₹520
$$

Profit percentage:

$$
\frac{520}{2000}\times100
=
\boxed{26\%}
$$

---

# 20. Finding CP

If:

MP = ₹3,000

Markup = 50%.

Then:

$$
MP=CP(1.5)
$$

Therefore:

$$
CP=\frac{3000}{1.5}
$$

$$
\boxed{₹2000}
$$

---

# 21. Finding MP

If:

CP = ₹2,500

Markup = 40%.

$$
MP=
2500(1.4)
$$

$$
\boxed{₹3500}
$$

---

# 22. Finding SP

If:

MP = ₹3,500

Discount = 20%.

$$
SP=
3500(0.8)
$$

$$
\boxed{₹2800}
$$

---

# 23. Finding Profit

CP = ₹2,500

MP = ₹3,500

Discount = 20%.

SP:

$$
3500(0.8)
=
₹2800
$$

Profit:

$$
2800-2500
=
\boxed{₹300}
$$

Profit percentage:

$$
\frac{300}{2500}\times100
=
\boxed{12\%}
$$

---

# 24. Finding Loss

CP = ₹2,500

MP = ₹3,000

Discount = 20%.

SP:

$$
3000(0.8)
=
₹2400
$$

Loss:

$$
2500-2400
=
₹100
$$

Loss percentage:

$$
\frac{100}{2500}\times100
=
\boxed{4\%}
$$

---

# 25. Finding Discount for a Desired Profit

Suppose:

Markup = 50%

Desired profit = 20%.

Find discount.

Formula:

$$
\boxed{
d=
\frac{100(m-p)}{100+m}
}
$$

Substitute:

$$
d=
\frac{100(50-20)}{150}
$$

$$
\boxed{20\%}
$$

---

# 26. Derivation of Required Discount

Suppose:

$$
CP=100
$$

Markup = `m%`.

Therefore:

$$
MP=100+m
$$

Desired profit = `p%`.

Therefore:

$$
SP=100+p
$$

Discount:

$$
d=
\frac{MP-SP}{MP}\times100
$$

Therefore:

$$
d=
\frac{(100+m)-(100+p)}{100+m}\times100
$$

Hence:

$$
\boxed{
d=
\frac{100(m-p)}{100+m}
}
$$

---

# 27. Example — Desired 25% Profit

Markup = 60%

Desired profit = 25%.

$$
d=
\frac{100(60-25)}{160}
$$

$$
=
\frac{3500}{160}
$$

$$
\boxed{21.875\%}
$$

---

# 28. Finding Markup for a Desired Profit

If:

- Desired profit = `p%`
- Discount = `d%`

then:

$$
\boxed{
m=
\frac{100(p+d)}{100-d}
}
$$

Example:

Desired profit = 20%

Discount = 20%.

$$
m=
\frac{100(20+20)}{80}
$$

$$
\boxed{50\%}
$$

---

# 29. Example — Required Markup

Desired profit = 30%

Discount = 20%.

$$
m=
\frac{100(30+20)}{80}
$$

$$
=\frac{5000}{80}
$$

$$
\boxed{62.5\%}
$$

---

# 30. Finding Marked Price for Desired Profit

Suppose:

CP = `C`

Desired profit = `p%`

Discount = `d%`.

Desired SP:

$$
SP=CP\frac{100+p}{100}
$$

But:

$$
SP=MP\frac{100-d}{100}
$$

Therefore:

$$
\boxed{
MP=
CP\frac{100+p}{100-d}
}
$$

---

# 31. Example

CP = ₹2,000

Desired profit = 25%

Discount = 20%.

$$
MP=
2000\times\frac{125}{80}
$$

$$
\boxed{₹3125}
$$

Check:

20% discount:

$$
3125(0.8)
=
₹2500
$$

Profit:

$$
2500-2000
=
₹500
$$

Profit percentage:

$$
\boxed{25\%}
$$

---

# 32. No-Profit / No-Loss Condition

For no profit/loss:

$$
SP=CP
$$

Therefore:

$$
\boxed{
d=
\frac{100m}{100+m}
}
$$

Example:

Markup = 50%.

$$
d=
\frac{5000}{150}
$$

$$
\boxed{33\frac13\%}
$$

---

# 33. Example — No Profit/Loss

CP = ₹1,000

Markup = 50%.

$$
MP=₹1500
$$

To have no profit:

$$
SP=₹1000
$$

Discount:

$$
1500-1000
=
₹500
$$

Discount percentage:

$$
\frac{500}{1500}\times100
=
\boxed{33\frac13\%}
$$

---

# 34. Maximum Discount Without Loss

The maximum discount without loss is exactly the discount that makes:

$$
SP=CP
$$

Therefore:

$$
\boxed{
Maximum\ Discount\%=
\frac{MP-CP}{MP}\times100
}
$$

If markup = `m%`:

$$
\boxed{
Maximum\ Discount\%=
\frac{100m}{100+m}
}
$$

---

# 35. Profit After Discount — Ratio Method

Suppose:

Markup = 50%.

Then:

$$
CP:MP=100:150
$$

If discount = 20%:

$$
SP=80\%\ of\ MP
$$

Therefore:

$$
SP=120
$$

So:

$$
CP:SP=100:120
$$

Profit:

$$
20
$$

Profit percentage:

$$
\boxed{20\%}
$$

---

# 36. CP = 100 Shortcut

For pure percentage questions:

> [!tip]
> Assume:
>
> $$\boxed{CP=100}$$

Then:

```text
Markup m%
↓
MP = 100 + m
↓
Discount d%
↓
SP = (100 + m)(100-d)/100
↓
Compare SP with 100
```

Example:

Markup = 40%

Discount = 10%.

$$
MP=140
$$

$$
SP=140(0.9)
=
126
$$

Therefore:

$$
Profit=126-100
=
\boxed{26\%}
$$

---

# 37. Fraction Method

Suppose:

Markup = 25%

Discount = 20%.

Take:

$$
CP=100
$$

Then:

$$
MP=125
$$

20% discount means retain 80%:

$$
SP=125\times\frac45
$$

$$
=100
$$

Therefore:

$$
\boxed{No\ Profit,\ No\ Loss}
$$

---

# 38. Profit Percentage When Markup Equals Discount

Suppose:

Markup = Discount = `x%`.

Using:

$$
Profit\%=x-x-\frac{x^2}{100}
$$

Therefore:

$$
\boxed{
Loss\%=\frac{x^2}{100}
}
$$

Example:

Markup = 20%

Discount = 20%.

$$
Loss\%=
\frac{20^2}{100}
=
\boxed{4\%}
$$

---

# 39. Important Result

> [!important]
> If the markup percentage and discount percentage are equal, there is **always a loss**, except when both are zero.

Example:

10% markup and 10% discount:

$$
Profit\%=10-10-\frac{100}{100}
$$

$$
\boxed{-1\%}
$$

So:

$$
\boxed{1\%\ loss}
$$

---

# 40. Why Equal Markup and Discount Cause Loss

Take:

$$
CP=100
$$

Markup = 20%.

$$
MP=120
$$

20% discount:

$$
SP=120(0.8)
=
96
$$

Therefore:

$$
CP=100
$$

$$
SP=96
$$

Loss:

$$
\boxed{4\%}
$$

The reason is that 20% discount is calculated on the higher MP.

---

# 41. Required Markup for Equal Discount and Desired Profit

If discount = `d%` and desired profit = `p%`:

$$
\boxed{
m=
\frac{100(p+d)}{100-d}
}
$$

If markup is required to equal discount:

$$
m=d
$$

Then desired profit must be negative:

$$
\boxed{
Loss\%=\frac{d^2}{100}
}
$$

---

# 42. Profit Percentage Greater Than Discount?

This is possible.

Example:

Markup = 50%

Discount = 10%.

$$
Profit\%=50-10-5
$$

$$
\boxed{35\%}
$$

So a small discount does not necessarily mean a small profit.

---

# 43. Discount Greater Than Markup

Example:

Markup = 20%

Discount = 30%.

$$
Profit\%=20-30-6
$$

$$
\boxed{-16\%}
$$

Therefore:

$$
\boxed{16\%\ loss}
$$

---

# 44. Finding Discount When Profit Is Known

Suppose:

Markup = 40%

Profit = 26%.

Find discount.

$$
d=
\frac{100(40-26)}{140}
$$

$$
=
\boxed{10\%}
$$

---

# 45. Finding Markup When Profit Is Known

Suppose:

Discount = 10%

Profit = 26%.

$$
m=
\frac{100(26+10)}{90}
$$

$$
=\frac{3600}{90}
$$

$$
\boxed{40\%}
$$

---

# 46. Finding CP From SP and Profit

If:

SP = ₹1,200

Profit = 20%.

Then:

$$
SP=120\%\ CP
$$

Therefore:

$$
CP=
1200\times\frac{100}{120}
$$

$$
\boxed{₹1000}
$$

---

# 47. Finding SP From CP and Profit

If:

CP = ₹1,000

Profit = 25%.

$$
SP=
1000\times\frac{125}{100}
$$

$$
\boxed{₹1250}
$$

---

# 48. Finding MP From SP and Discount

If:

SP = ₹2,400

Discount = 20%.

$$
MP=
2400\times\frac{100}{80}
$$

$$
\boxed{₹3000}
$$

If CP = ₹2,000, then profit:

$$
2400-2000
=
₹400
$$

Profit percentage:

$$
\boxed{20\%}
$$

---

# 49. Mixed Example

A shopkeeper buys an article for ₹4,000, marks it 50% above CP, and gives a 20% discount.

### Step 1 — MP

$$
MP=4000(1.5)
=
₹6000
$$

### Step 2 — SP

$$
SP=6000(0.8)
=
₹4800
$$

### Step 3 — Profit

$$
4800-4000
=
₹800
$$

### Step 4 — Profit %

$$
\frac{800}{4000}\times100
=
\boxed{20\%}
$$

---

# 50. Mixed Example — Loss

A shopkeeper buys an article for ₹5,000, marks it 20% above CP, and gives a 30% discount.

MP:

$$
5000(1.2)
=
₹6000
$$

SP:

$$
6000(0.7)
=
₹4200
$$

Loss:

$$
5000-4200
=
₹800
$$

Loss percentage:

$$
\frac{800}{5000}\times100
=
\boxed{16\%}
$$

---

# 51. Mixed Example — Desired Profit

A shopkeeper buys an article for ₹2,500. He wants 20% profit after offering a 20% discount.

Find MP.

Desired SP:

$$
2500(1.2)
=
₹3000
$$

Since 20% discount means SP = 80% MP:

$$
MP=
\frac{3000}{0.8}
$$

$$
\boxed{₹3750}
$$

Markup:

$$
3750-2500
=
₹1250
$$

Markup percentage:

$$
\frac{1250}{2500}\times100
=
\boxed{50\%}
$$

---

# 52. Mixed Example — Find Discount

A product is marked 60% above CP. The seller wants 20% profit. Find the discount.

$$
m=60,\quad p=20
$$

$$
d=
\frac{100(60-20)}{160}
$$

$$
\boxed{25\%}
$$

---

# 53. Mixed Example — Find Markup

A seller offers a 20% discount and still wants 20% profit.

$$
d=20,\quad p=20
$$

$$
m=
\frac{100(20+20)}{80}
$$

$$
\boxed{50\%}
$$

So:

> To offer a 20% discount and still earn 20% profit, the article must be marked **50% above CP**.

---

# 54. Successive Discounts With Profit

Suppose:

Markup = 50%

Discounts = 20% and 10%.

Take:

$$
CP=100
$$

MP:

$$
150
$$

After 20%:

$$
150(0.8)=120
$$

After 10%:

$$
120(0.9)=108
$$

Therefore:

$$
Profit=108-100
$$

$$
\boxed{8\%}
$$

---

# 55. Formula — Markup + Successive Discounts

If discounts are `a%` and `b%`:

$$
\boxed{
SP=
CP
\left(1+\frac m{100}\right)
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
}
$$

Then:

$$
\boxed{
Profit\%=
\left[
\left(1+\frac m{100}\right)
\left(1-\frac a{100}\right)
\left(1-\frac b{100}\right)
-1
\right]100
}
$$

---

# 56. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Calculating Profit % on MP

Wrong:

$$
\frac{SP-CP}{MP}\times100
$$

Correct:

$$
\boxed{
\frac{SP-CP}{CP}\times100
}
$$

### Mistake 2 — Calculating Discount % on CP

Wrong:

$$
\frac{MP-SP}{CP}\times100
$$

Correct:

$$
\boxed{
\frac{MP-SP}{MP}\times100
}
$$

### Mistake 3 — Adding Markup and Discount

Wrong:

$$
50\%-20\%=30\%
$$

Correct:

$$
50-20-\frac{50(20)}{100}
=
\boxed{20\%}
$$

### Mistake 4 — Assuming Equal Markup and Discount Cancel

They do not.

20% markup + 20% discount:

$$
\boxed{4\%\ loss}
$$

### Mistake 5 — Ignoring the Order

```text
CP → Markup → MP → Discount → SP
```

---

# 57. High-Yield Exam Patterns

> [!important] Must Master

1. CP + markup + discount
2. Find SP
3. Find profit
4. Find loss
5. Find profit %
6. Find loss %
7. Find MP
8. Find CP
9. Find markup
10. Find discount
11. Desired profit
12. No profit/loss
13. Maximum discount
14. Equal markup and discount
15. Discount greater than markup
16. Markup greater than discount
17. Successive discounts + profit
18. Reverse problems
19. Ratio/fraction method
20. Mixed profit-loss-discount problems

---

# 58. Formula Sheet

> [!important] Must Remember

### Marked Price

$$
\boxed{
MP=CP\frac{100+m}{100}
}
$$

### Selling Price

$$
\boxed{
SP=MP\frac{100-d}{100}
}
$$

### Direct SP

$$
\boxed{
SP=
CP\frac{(100+m)(100-d)}{10000}
}
$$

### Profit %

$$
\boxed{
Profit\%=
m-d-\frac{md}{100}
}
$$

### Required Discount

$$
\boxed{
d=
\frac{100(m-p)}{100+m}
}
$$

### Required Markup

$$
\boxed{
m=
\frac{100(p+d)}{100-d}
}
$$

### Required MP

$$
\boxed{
MP=
CP\frac{100+p}{100-d}
}
$$

### No Profit / No Loss

$$
\boxed{
d=
\frac{100m}{100+m}
}
$$

### Equal Markup and Discount

$$
\boxed{
Loss\%=
\frac{m^2}{100}
}
$$

when:

$$
m=d
$$

---

# 59. Quick Revision

> [!summary] One-Minute Revision

### Main Flow

$$
\boxed{
CP\rightarrow MP\rightarrow SP
}
$$

### Markup

$$
\boxed{
MP=CP\left(1+\frac m{100}\right)
}
$$

### Discount

$$
\boxed{
SP=MP\left(1-\frac d{100}\right)
}
$$

### Profit

$$
\boxed{
Profit\%=
\frac{SP-CP}{CP}\times100
}
$$

### Fast Formula

$$
\boxed{
Profit\%=m-d-\frac{md}{100}
}
$$

### Example

Markup = 50%

Discount = 20%.

$$
50-20-\frac{50(20)}{100}
$$

$$
=20\%
$$

Therefore:

$$
\boxed{20\%\ profit}
$$

### Memory Trick

```text
CP = 100
     ↓
Markup
     ↓
MP = 100 + m
     ↓
Discount
     ↓
SP = (100+m)(100-d)/100
     ↓
Compare SP with 100
```

---

# 60. Exam Recognition Map

```text
PROFIT WITH DISCOUNT
│
├── Basic
│   ├── CP
│   ├── MP
│   ├── SP
│   └── Discount
│
├── Direct
│   ├── Find SP
│   ├── Find Profit
│   └── Find Profit %
│
├── Reverse
│   ├── Find CP
│   ├── Find MP
│   ├── Find Markup
│   └── Find Discount
│
├── Target
│   ├── Desired Profit
│   ├── No Profit/Loss
│   └── Maximum Discount
│
├── Special
│   ├── Equal Markup & Discount
│   ├── Discount > Markup
│   └── Markup > Discount
│
├── Advanced
│   ├── Successive Discounts
│   ├── Ratio Method
│   └── Fraction Method
│
└── Mixed
    ├── Profit + Discount
    ├── Loss + Discount
    └── Multi-step Pricing
```

> [!success]
> **Core skill:** Never treat markup and discount as simple additions/subtractions.
>
> The correct sequence is:
>
> $$\boxed{
> CP
> \xrightarrow{Markup}
> MP
> \xrightarrow{Discount}
> SP
> }$$
>
> For quick percentage problems:
>
> $$\boxed{
> Profit\%=m-d-\frac{md}{100}
> }$$
>
> **Remember the bases:**
>
> **Markup % → CP**
>
> **Discount % → MP**
>
> **Profit/Loss % → CP**