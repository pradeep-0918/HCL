---
type: concept
subject: aptitude
topic: "GST and Tax Applications"
parent: "06. Profit Loss and Discount"
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - gst
  - tax
  - percentage
  - price-after-tax
  - profit-loss
---

# GST and Tax Applications

## 1. GST Basics

> [!summary]
> **GST (Goods and Services Tax)** is a percentage-based tax added to the taxable price of a product or service.
>
> In aptitude problems, GST is mainly tested through:
>
> - Finding GST amount
> - Finding price after GST
> - Finding original price from GST-inclusive price
> - Finding tax percentage
> - Combining discount and GST
> - Reverse GST calculations

The basic flow is:

$$
\boxed{
Original\ Price
\rightarrow
GST
\rightarrow
Final\ Price
}
$$

---

# 2. Basic GST Formula

If:

- Original price = `P`
- GST rate = `g%`

then:

$$
\boxed{
GST=P\times\frac{g}{100}
}
$$

Final price:

$$
\boxed{
Final=P+GST
}
$$

Therefore:

$$
\boxed{
Final=P\left(1+\frac{g}{100}\right)
}
$$

---

# 3. GST Multiplier

Convert GST percentage into a multiplier.

| GST | Multiplier |
|---:|---:|
| 5% | 1.05 |
| 12% | 1.12 |
| 18% | 1.18 |
| 28% | 1.28 |

Therefore:

$$
\boxed{
Price\ After\ GST=
Original\ Price\times GST\ Multiplier
}
$$

---

# 4. Example — 18% GST

Original price:

$$
₹1000
$$

GST:

$$
18\%
$$

GST amount:

$$
1000\times\frac{18}{100}
=
₹180
$$

Final price:

$$
1000+180
=
\boxed{₹1180}
$$

Using multiplier:

$$
1000(1.18)
=
\boxed{₹1180}
$$

---

# 5. Example — 5% GST

Price:

$$
₹2000
$$

GST:

$$
5\%
$$

GST:

$$
2000(0.05)
=
₹100
$$

Final price:

$$
\boxed{₹2100}
$$

---

# 6. Example — 12% GST

Price:

$$
₹5000
$$

GST:

$$
12\%
$$

GST amount:

$$
5000(0.12)
=
₹600
$$

Final price:

$$
5000+600
=
\boxed{₹5600}
$$

---

# 7. Example — 28% GST

Price:

$$
₹2500
$$

GST:

$$
28\%
$$

GST:

$$
2500(0.28)
=
₹700
$$

Final:

$$
2500+700
=
\boxed{₹3200}
$$

---

# 8. Tax Percentage

The same percentage principle applies to any tax.

If:

- Taxable price = `P`
- Tax rate = `t%`

then:

$$
\boxed{
Tax=P\frac{t}{100}
}
$$

Price after tax:

$$
\boxed{
Final=P\left(1+\frac{t}{100}\right)
}
$$

---

# 9. Example — Tax Percentage

Taxable amount:

$$
₹8000
$$

Tax:

$$
15\%
$$

Tax amount:

$$
8000(0.15)
=
₹1200
$$

Final price:

$$
8000+1200
=
\boxed{₹9200}
$$

---

# 10. Finding Tax Percentage

Suppose:

Original price:

$$
₹4000
$$

Final price:

$$
₹4720
$$

Tax:

$$
4720-4000
=
₹720
$$

Tax percentage:

$$
\frac{720}{4000}\times100
$$

$$
\boxed{18\%}
$$

---

# 11. General Tax Percentage Formula

If:

- Original price = `P`
- Final price = `F`

then:

$$
Tax=F-P
$$

Therefore:

$$
\boxed{
Tax\%=
\frac{F-P}{P}\times100
}
$$

---

# 12. Price After Tax

If price = `P` and tax = `t%`:

$$
\boxed{
Price\ After\ Tax=
P\frac{100+t}{100}
}
$$

Example:

Price = ₹6,000

Tax = 10%.

$$
6000\times\frac{110}{100}
$$

$$
\boxed{₹6600}
$$

---

# 13. Reverse Tax Problem

Suppose the final price includes 18% GST.

Final price:

$$
₹5900
$$

Since:

$$
Final=Original(1.18)
$$

Therefore:

$$
Original=
\frac{5900}{1.18}
$$

$$
\boxed{₹5000}
$$

---

# 14. Reverse Tax Formula

If final price includes `t%` tax:

$$
\boxed{
Original=
Final\times\frac{100}{100+t}
}
$$

Example:

Final = ₹11,800

Tax = 18%.

$$
Original=
11800\times\frac{100}{118}
$$

$$
\boxed{₹10,000}
$$

---

# 15. Finding Tax Amount From Inclusive Price

Suppose:

Final price = ₹11,800

GST = 18%.

Original:

$$
11800\times\frac{100}{118}
=
₹10000
$$

GST:

$$
11800-10000
=
\boxed{₹1800}
$$

---

# 16. Direct GST Component Formula

If final price already includes `t%` GST:

$$
\boxed{
GST=
Final\times\frac{t}{100+t}
}
$$

Example:

Final = ₹5,900

GST = 18%.

$$
GST=
5900\times\frac{18}{118}
$$

$$
\boxed{₹900}
$$

---

# 17. Tax as Percentage of Final Price

> [!important]
> If GST is 18% of the original taxable price, it is **not** 18% of the final price.

For 18% GST:

$$
GST\% \text{ of final}
=
\frac{18}{118}\times100
$$

$$
\boxed{15.254\%}
$$

---

# 18. Discount + GST

This is one of the most important mixed patterns.

Suppose:

MP = ₹10,000

Discount = 20%

GST = 18%.

### Step 1 — Discount

$$
10000(0.8)
=
₹8000
$$

### Step 2 — GST

$$
8000(1.18)
=
₹9440
$$

Therefore:

$$
\boxed{Final\ Price=₹9440}
$$

---

# 19. Direct Formula — Discount + GST

If:

- MP = `M`
- Discount = `d%`
- GST = `g%`

then:

$$
\boxed{
Final=
M
\left(1-\frac d{100}\right)
\left(1+\frac g{100}\right)
}
$$

---

# 20. Example

MP = ₹20,000

Discount = 15%

GST = 18%.

Discounted price:

$$
20000(0.85)
=
₹17000
$$

GST:

$$
17000(0.18)
=
₹3060
$$

Final:

$$
\boxed{₹20060}
$$

---

# 21. Net Effect of Discount and GST

For discount `d%` followed by GST `g%`:

$$
Net\ Multiplier=
\left(1-\frac d{100}\right)
\left(1+\frac g{100}\right)
$$

Net percentage change:

$$
\boxed{
g-d-\frac{gd}{100}
}
$$

Example:

Discount = 20%

GST = 18%.

$$
18-20-\frac{18\times20}{100}
$$

$$
=18-20-3.6
$$

$$
\boxed{-5.6\%}
$$

So final price is 5.6% below the original marked price.

---

# 22. Tax and Profit-Loss

Suppose:

CP = ₹5,000

SP before tax = ₹6,000

GST = 18%.

Customer payment:

$$
6000(1.18)
=
₹7080
$$

Business profit:

$$
6000-5000
=
₹1000
$$

Profit percentage:

$$
\frac{1000}{5000}\times100
=
\boxed{20\%}
$$

> [!important]
> When GST is collected as tax, the GST amount is generally not treated as business profit in aptitude calculations.

---

# 23. Markup + Discount + GST

Suppose:

CP = ₹10,000

Markup = 50%

Discount = 20%

GST = 18%.

### Marked Price

$$
MP=10000(1.5)
=
₹15000
$$

### Selling Price Before GST

$$
SP=15000(0.8)
=
₹12000
$$

### GST

$$
GST=12000(0.18)
=
₹2160
$$

### Final Customer Price

$$
12000+2160
=
\boxed{₹14160}
$$

### Profit

$$
12000-10000
=
₹2000
$$

Therefore:

$$
\boxed{20\%\ profit}
$$

---

# 24. Reverse Mixed Problem

Final customer price:

$$
₹14160
$$

GST:

$$
18\%
$$

Discount:

$$
20\%
$$

Markup:

$$
50\%
$$

Find CP.

### Remove GST

$$
SP=
\frac{14160}{1.18}
=
₹12000
$$

### Remove Discount

$$
MP=
\frac{12000}{0.8}
=
₹15000
$$

### Remove Markup

$$
CP=
\frac{15000}{1.5}
=
\boxed{₹10000}
$$

---

# 25. Tax After Discount

> [!important]
> Unless the question specifies another order, when a discount is explicitly applied before tax:

$$
\boxed{
Discount\ First
\rightarrow
Tax\ Second
}
$$

Example:

MP = ₹50,000

Discount = 10%

Tax = 18%.

Discounted price:

$$
50000(0.9)
=
₹45000
$$

Tax:

$$
45000(0.18)
=
₹8100
$$

Final:

$$
\boxed{₹53100}
$$

---

# 26. Tax Before Discount

Some questions may explicitly specify that tax is calculated first.

Then follow:

$$
\boxed{
Tax\ First
\rightarrow
Discount\ Second
}
$$

Example:

Price = ₹10,000

Tax = 18%

Discount = 10%.

Taxed price:

$$
10000(1.18)
=
₹11800
$$

After discount:

$$
11800(0.9)
=
\boxed{₹10620}
$$

> [!warning]
> Always follow the order given in the question.

---

# 27. Do Discount and Tax Commute?

Mathematically:

$$
(1-d)(1+t)
$$

and:

$$
(1+t)(1-d)
$$

are equal.

Therefore, if both percentages apply to the same base sequentially:

$$
\boxed{
Discount\ then\ Tax
}
$$

and

$$
\boxed{
Tax\ then\ Discount
}
$$

produce the same mathematical result.

However, real tax rules may define a specific taxable base, so in aptitude questions **follow the stated order/base**.

---

# 28. GST Inclusive vs Exclusive

### GST Exclusive

Price does **not** include GST.

Example:

$$
₹1000+18\%
$$

Final:

$$
₹1180
$$

### GST Inclusive

Price already includes GST.

Example:

$$
₹1180\ including\ 18\%\ GST
$$

Original:

$$
\frac{1180}{1.18}
=
\boxed{₹1000}
$$

---

# 29. Quick Identification

If the question says:

```text
"₹10,000 + 18% GST"
```

Use:

$$
10000(1.18)
$$

If it says:

```text
"₹11,800 including 18% GST"
```

Use:

$$
\frac{11800}{1.18}
$$

---

# 30. CGST and SGST

For an intra-state transaction, total GST may be divided into:

$$
\boxed{
CGST+SGST=Total\ GST
}
$$

If total GST = 18%:

$$
CGST=9\%
$$

$$
SGST=9\%
$$

Example:

Taxable price = ₹10,000.

CGST:

$$
10000(0.09)
=
₹900
$$

SGST:

$$
10000(0.09)
=
₹900
$$

Total GST:

$$
₹1800
$$

Final:

$$
\boxed{₹11800}
$$

---

# 31. IGST

For an inter-state transaction, GST may be represented as IGST.

If:

Taxable value = ₹10,000

IGST = 18%.

$$
IGST=10000(0.18)
=
₹1800
$$

Final:

$$
\boxed{₹11800}
$$

---

# 32. Finding CGST and SGST

Total GST = 18%.

Taxable value = ₹20,000.

Assuming equal split:

$$
CGST=9\%
$$

$$
SGST=9\%
$$

CGST:

$$
20000(0.09)
=
₹1800
$$

SGST:

$$
20000(0.09)
=
₹1800
$$

Total:

$$
\boxed{₹3600}
$$

---

# 33. Price After Tax

If:

Original price = `P`

Tax = `t%`

then:

$$
\boxed{
Price\ After\ Tax=
P\frac{100+t}{100}
}
$$

Example:

P = ₹7,500

Tax = 12%.

$$
7500(1.12)
=
\boxed{₹8400}
$$

---

# 34. Finding Price Before Tax

If:

Price after tax = `F`

Tax = `t%`

then:

$$
\boxed{
Price\ Before\ Tax=
F\frac{100}{100+t}
}
$$

Example:

Final = ₹8,400

Tax = 12%.

$$
8400\times\frac{100}{112}
$$

$$
\boxed{₹7500}
$$

---

# 35. Finding Tax Amount Directly

If final price includes tax:

$$
\boxed{
Tax=
Final\times\frac{t}{100+t}
}
$$

Example:

Final = ₹8,400

Tax = 12%.

$$
Tax=
8400\times\frac{12}{112}
$$

$$
\boxed{₹900}
$$

Original:

$$
8400-900
=
₹7500
$$

---

# 36. Finding Tax Percentage From Price Change

Original price:

$$
₹2500
$$

Final price:

$$
₹2875
$$

Tax:

$$
2875-2500
=
₹375
$$

Tax percentage:

$$
\frac{375}{2500}\times100
=
\boxed{15\%}
$$

---

# 37. Multiple Taxes

If multiple taxes are applied successively:

```text
Tax 1 → Tax 2 → Final
```

Use multipliers.

For taxes `a%` and `b%`:

$$
\boxed{
Final=
P
\left(1+\frac a{100}\right)
\left(1+\frac b{100}\right)
}
$$

Net tax effect:

$$
\boxed{
a+b+\frac{ab}{100}
}
$$

Example:

10% followed by 5%:

$$
10+5+\frac{10(5)}{100}
$$

$$
\boxed{15.5\%}
$$

---

# 38. Tax Increase Example

Original tax = 10%

New tax = 15%

Taxable value = ₹10,000.

Old tax:

$$
₹1000
$$

New tax:

$$
₹1500
$$

Increase:

$$
₹500
$$

Percentage increase in tax:

$$
\frac{500}{1000}\times100
=
\boxed{50\%}
$$

---

# 39. Tax and Discount Example

A product is marked at ₹20,000. A discount of 15% is offered and then 18% GST is charged.

Discount:

$$
20000(0.85)
=
₹17000
$$

GST:

$$
17000(0.18)
=
₹3060
$$

Final:

$$
\boxed{₹20060}
$$

---

# 40. Tax and Profit Example

An article costs ₹8,000. It is sold for ₹10,000 before GST. GST is 18%.

Profit:

$$
10000-8000
=
₹2000
$$

Profit percentage:

$$
\frac{2000}{8000}\times100
=
\boxed{25\%}
$$

GST:

$$
10000(0.18)
=
₹1800
$$

Customer payment:

$$
\boxed{₹11800}
$$

---

# 41. Common Exam Traps

> [!warning] Avoid These

### Trap 1 — Wrong Reverse Formula

For 18% GST:

Wrong:

$$
Final(0.82)
$$

Correct:

$$
\boxed{
\frac{Final}{1.18}
}
$$

---

### Trap 2 — GST Base

GST is calculated on the **taxable value**, not automatically on CP.

---

### Trap 3 — Profit Base

Profit percentage:

$$
\boxed{CP\ is\ the\ base}
$$

---

### Trap 4 — GST Included

If the price already includes GST, do not add GST again.

---

### Trap 5 — Tax Is Not Automatically Profit

If GST is collected and remitted, separate it from the seller's business revenue.

---

### Trap 6 — Discount Base

Discount percentage is based on MP:

$$
\boxed{
Discount\%=
\frac{MP-SP}{MP}\times100
}
$$

---

# 42. High-Yield Exam Patterns

> [!important] Must Master

1. Find GST amount
2. Find final price
3. Find original price
4. Find tax percentage
5. Reverse GST
6. GST-inclusive price
7. GST-exclusive price
8. Discount + GST
9. Markup + GST
10. Profit + GST
11. CP + MP + discount + GST
12. CGST + SGST
13. IGST
14. Tax after discount
15. Tax before discount
16. Find discount from final price
17. Find CP from final customer price
18. Find MP from final customer price
19. Multiple tax percentages
20. Mixed profit-loss-tax problems

---

# 43. Formula Sheet

> [!important] Must Remember

### Tax Amount

$$
\boxed{
Tax=P\frac{t}{100}
}
$$

### Price After Tax

$$
\boxed{
Final=P\frac{100+t}{100}
}
$$

### Price Before Tax

$$
\boxed{
Original=Final\frac{100}{100+t}
}
$$

### Tax From Inclusive Price

$$
\boxed{
Tax=Final\frac{t}{100+t}
}
$$

### Tax Percentage

$$
\boxed{
Tax\%=
\frac{Final-Original}{Original}\times100
}
$$

### Discount + Tax

$$
\boxed{
Final=
MP
\left(1-\frac d{100}\right)
\left(1+\frac t{100}\right)
}
$$

### Net Discount + Tax Effect

$$
\boxed{
Net\ Change\%=
t-d-\frac{dt}{100}
}
$$

### Multiple Taxes

$$
\boxed{
Final=
P\prod_i\left(1+\frac{t_i}{100}\right)
}
$$

### Equal CGST + SGST

$$
\boxed{
CGST=SGST=\frac{Total\ GST}{2}
}
$$

---

# 44. Quick Revision

> [!summary] One-Minute Revision

### GST Added

$$
\boxed{
Final=Original(1+GST/100)
}
$$

### GST Included

$$
\boxed{
Original=
\frac{Final}{1+GST/100}
}
$$

### GST Component

$$
\boxed{
GST=
Final\frac{GST\%}{100+GST\%}
}
$$

### Discount + GST

$$
\boxed{
Final=
MP(1-D/100)(1+GST/100)
}
$$

### Basic Example

```text
Price = ₹10,000
GST = 18%
```

$$
GST=₹1800
$$

$$
Final=₹11800
$$

### Reverse Example

```text
Final = ₹11,800
GST = 18%
```

$$
Original=₹10,000
$$

$$
GST=₹1,800
$$

---

# 45. Exam Recognition Map

```text
GST & TAX
│
├── GST Basics
│   ├── GST Amount
│   ├── Taxable Value
│   └── Final Price
│
├── Tax Percentage
│   ├── Find Tax
│   ├── Find Rate
│   └── Find Tax Component
│
├── Price After Tax
│   ├── GST Added
│   ├── Tax Added
│   └── Inclusive Price
│
├── Reverse
│   ├── Find Original Price
│   ├── Find CP
│   └── Find MP
│
├── Discount Applications
│   ├── Discount + GST
│   ├── Discount → Tax
│   └── Tax → Discount
│
├── GST Structure
│   ├── CGST
│   ├── SGST
│   └── IGST
│
└── Mixed
    ├── Profit + GST
    ├── Markup + GST
    ├── CP + Discount + GST
    └── Multi-step Percentage Chain
```

> [!success]
> **Core skill:** GST and tax problems are percentage-multiplier problems.
>
> $$\boxed{
> Tax\ Added
> \rightarrow
> \times\left(1+\frac{t}{100}\right)
> }$$
>
> $$\boxed{
> Tax\ Included
> \rightarrow
> \div\left(1+\frac{t}{100}\right)
> }$$
>
> Always identify:
>
> **1. What is the taxable value?**
>
> **2. Is the quoted price tax-inclusive or tax-exclusive?**
>
> **3. What percentage base is being used?**
>
> **4. Is GST being treated separately from business profit?**