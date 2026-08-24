---
type: concept
subject: aptitude
topic: "Weighted Average"
parent: "05. Average"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - average
  - weighted-average
  - quantitative-aptitude
wikilinks:
  - "[[05. Average]]"
  - "[[Basic Average]]"
  - "[[Average of Numbers]]"
  - "[[Combined Average]]"
  - "[[Average-Based Applications]]"
---

# Weighted Average

## 1. Core Concept

> [!summary]
> A **weighted average** is an average in which different values have different levels of importance, frequency, quantity, or weight.

The basic formula is:

$$
\boxed{
Weighted\ Average=
\frac{\sum(wx)}{\sum w}
}
$$

Where:

- `x` = value
- `w` = weight
- `wx` = weighted contribution

---

# 2. Why Weighted Average?

In a simple average, every value has equal importance.

Example:

$$
60,\ 80
$$

Simple average:

$$
\frac{60+80}{2}=70
$$

But suppose `60` represents 80 students and `80` represents 20 students.

Then `60` should have greater influence.

So we use a weighted average.

---

# 3. Basic Formula

For values:

$$
x_1,x_2,\ldots,x_n
$$

with weights:

$$
w_1,w_2,\ldots,w_n
$$

the weighted average is:

$$
\boxed{
\frac{
w_1x_1+w_2x_2+\cdots+w_nx_n
}{
w_1+w_2+\cdots+w_n
}
}
$$

---

# 4. Basic Example

Values:

- `10` with weight `2`
- `20` with weight `3`

Calculate:

$$
\frac{10(2)+20(3)}{2+3}
$$

$$
=\frac{20+60}{5}
$$

$$
\boxed{16}
$$

---

# 5. Simple Average vs Weighted Average

Suppose:

$$
10,\ 20
$$

### Simple Average

$$
\frac{10+20}{2}=15
$$

### Weighted Average

If weights are `1:3`:

$$
\frac{10(1)+20(3)}{1+3}
$$

$$
=\frac{70}{4}
$$

$$
\boxed{17.5}
$$

Because `20` has greater weight, the result moves closer to `20`.

---

# 6. Golden Rule

> [!important]
> **The weighted average always gives more influence to values with larger weights.**

If:

$$
w_1>w_2
$$

then `x₁` has greater influence than `x₂`.

---

# 7. Weighted Average Using Ratio

Suppose values are:

$$
40,\ 60
$$

and their weights are:

$$
2:3
$$

Then:

$$
Weighted\ Average
=
\frac{40(2)+60(3)}{2+3}
$$

$$
=
\frac{80+180}{5}
$$

$$
\boxed{52}
$$

---

# 8. Weight as Frequency

A frequency is simply a weight.

Example:

| Value | Frequency |
|---:|---:|
| 10 | 2 |
| 20 | 5 |
| 30 | 3 |

Weighted average:

$$
\frac{10(2)+20(5)+30(3)}
{2+5+3}
$$

$$
=
\frac{20+100+90}{10}
$$

$$
\boxed{21}
$$

---

# 9. Frequency Formula

If a value `x` occurs `f` times:

$$
\boxed{
Average=
\frac{\sum fx}{\sum f}
}
$$

This is exactly a weighted average.

---

# 10. Weighted Average of Marks

Suppose:

- Mathematics = 80, weight 3
- Physics = 70, weight 2
- Chemistry = 90, weight 1

Weighted average:

$$
\frac{
80(3)+70(2)+90(1)
}{
3+2+1
}
$$

$$
=
\frac{240+140+90}{6}
$$

$$
=\frac{470}{6}
$$

$$
\boxed{78.33}
$$

---

# 11. Weighted Average of Exam Scores

Suppose:

- Internal = 70, weight 30%
- Final = 80, weight 70%

Then:

$$
70(0.30)+80(0.70)
$$

$$
=21+56
$$

$$
\boxed{77}
$$

---

# 12. Percentage Weights

If weights are percentages:

$$
\boxed{
Weighted\ Average=
\frac{x_1w_1+x_2w_2+\cdots}
{w_1+w_2+\cdots}
}
$$

If the weights total `100%`, the denominator can be treated as `100`.

Example:

`60` with 40% weight and `80` with 60% weight:

$$
\frac{60(40)+80(60)}{100}
$$

$$
=\boxed{72}
$$

---

# 13. Important Shortcut

If weights are already percentages that add to `100%`:

$$
\boxed{
Weighted\ Average=
\frac{\sum wx}{100}
}
$$

Example:

| Score | Weight |
|---:|---:|
| 70 | 20% |
| 80 | 30% |
| 90 | 50% |

$$
\frac{70(20)+80(30)+90(50)}{100}
$$

$$
=
\frac{1400+2400+4500}{100}
$$

$$
\boxed{83}
$$

---

# 14. Weighted Average of Two Groups

Group A:

- 20 students
- Average = 60

Group B:

- 30 students
- Average = 70

The group sizes act as weights.

Therefore:

$$
\frac{20(60)+30(70)}{20+30}
$$

$$
=\frac{1200+2100}{50}
$$

$$
\boxed{66}
$$

---

# 15. Combined Average Is a Weighted Average

> [!important]
> **Combined average is simply a weighted average of group averages, where the group sizes are the weights.**

Formula:

$$
\boxed{
A_c=
\frac{n_1A_1+n_2A_2}
{n_1+n_2}
}
$$

---

# 16. Why Simple Average of Group Averages Can Fail

Group A:

`10` students, average `50`.

Group B:

`90` students, average `80`.

Wrong:

$$
\frac{50+80}{2}=65
$$

Correct:

$$
\frac{10(50)+90(80)}
{100}
$$

$$
=\frac{7700}{100}
$$

$$
\boxed{77}
$$

The second group has much greater weight.

---

# 17. Equal Weights

If all weights are equal:

$$
w_1=w_2=\cdots=w_n
$$

then weighted average becomes the normal average.

Example:

Weights:

$$
2:2:2
$$

Values:

$$
10,20,30
$$

Weighted average:

$$
\frac{10(2)+20(2)+30(2)}6
$$

$$
=\boxed{20}
$$

Same as ordinary average.

---

# 18. Weight Ratio Shortcut

If weights are:

$$
a:b
$$

then:

$$
\boxed{
WA=\frac{ax+by}{a+b}
}
$$

Example:

Values:

$$
40,\ 70
$$

Weights:

$$
3:2
$$

$$
WA=
\frac{40(3)+70(2)}5
$$

$$
=\frac{260}{5}
$$

$$
\boxed{52}
$$

---

# 19. Weighted Average Lies Between Values

For positive weights, the weighted average lies between the smallest and largest values.

If:

$$
40\le x\le80
$$

then:

$$
\boxed{40\le WA\le80}
$$

This is a useful checking technique.

---

# 20. Closer to the Heavier Value

Values:

$$
20,\ 80
$$

Weights:

$$
1:4
$$

Weighted average:

$$
\frac{20(1)+80(4)}5
$$

$$
=\frac{340}{5}
$$

$$
\boxed{68}
$$

The answer is closer to `80` because `80` has greater weight.

---

# 21. Weighted Average as Balance Point

Think of the weighted average as a **balance point**.

Example:

`20` has weight 1.

`80` has weight 4.

The heavier value pulls the average toward itself.

Therefore:

$$
\boxed{WA=68}
$$

---

# 22. Deviation Method for Weighted Average

Choose a convenient reference value `A`.

Then:

$$
\boxed{
WA=A+\frac{\sum wd}{\sum w}
}
$$

where:

$$
d=x-A
$$

This is useful when values are close together.

---

# 23. Example — Weighted Deviation

Values:

$$
48,\ 52,\ 54
$$

Weights:

$$
2,\ 3,\ 5
$$

Take assumed value:

$$
50
$$

Deviations:

$$
-2,\ +2,\ +4
$$

Weighted deviations:

$$
2(-2)=-4
$$

$$
3(2)=6
$$

$$
5(4)=20
$$

Total weighted deviation:

$$
22
$$

Total weight:

$$
10
$$

Therefore:

$$
WA=50+\frac{22}{10}
$$

$$
\boxed{52.2}
$$

---

# 24. Weighted Average and Percentage Change

Suppose two products have prices:

$$
₹100,\ ₹200
$$

with quantities:

$$
10,\ 5
$$

Average price per item:

$$
\frac{100(10)+200(5)}
{10+5}
$$

$$
=\frac{2000}{15}
$$

$$
\boxed{₹133.33}
$$

The quantities are the weights.

---

# 25. Average Cost

If:

- 5 items cost ₹100 each
- 10 items cost ₹150 each

Weighted average cost:

$$
\frac{5(100)+10(150)}
{5+10}
$$

$$
=\frac{2000}{15}
$$

$$
\boxed{₹133.33}
$$

---

# 26. Average Price

Suppose:

- 20 kg purchased at ₹40/kg
- 30 kg purchased at ₹50/kg

Average price:

$$
\frac{20(40)+30(50)}
{20+30}
$$

$$
=\frac{2300}{50}
$$

$$
\boxed{₹46/kg}
$$

---

# 27. Mixture Interpretation

Weighted average is heavily used in mixture problems.

If:

- Quantity `q₁` has value `x₁`
- Quantity `q₂` has value `x₂`

then:

$$
\boxed{
Average=
\frac{q_1x_1+q_2x_2}
{q_1+q_2}
}
$$

Here, quantities act as weights.

---

# 28. Mixture Example

10 L of solution contains 20% alcohol.

20 L contains 40% alcohol.

Combined concentration:

$$
\frac{10(20)+20(40)}
{10+20}
$$

$$
=\frac{200+800}{30}
$$

$$
\boxed{33.33\%}
$$

---

# 29. Weighted Average of Concentrations

General formula:

$$
\boxed{
C=
\frac{q_1C_1+q_2C_2}
{q_1+q_2}
}
$$

Where:

- `q` = quantity
- `C` = concentration

---

# 30. Investment and Return

Suppose:

₹10,000 earns 5%.

₹20,000 earns 10%.

Overall return rate:

$$
\frac{10000(5)+20000(10)}
{10000+20000}
$$

$$
=\frac{250000}{30000}
$$

$$
\boxed{8.33\%}
$$

The investment amounts are the weights.

---

# 31. Weighted Average of Interest Rates

If different amounts are invested at different rates:

$$
\boxed{
Overall\ Rate=
\frac{\sum(P\times R)}
{\sum P}
}
$$

where:

- `P` = principal
- `R` = rate

---

# 32. Salary Weighted Average

Suppose:

- 10 employees earn ₹20,000
- 30 employees earn ₹40,000

Average salary:

$$
\frac{10(20000)+30(40000)}
{40}
$$

$$
=\frac{1,400,000}{40}
$$

$$
\boxed{₹35,000}
$$

---

# 33. Weighted Average of Ages

Suppose:

- 10 students have average age 15
- 20 students have average age 18

Combined age:

$$
\frac{10(15)+20(18)}
{30}
$$

$$
=\frac{510}{30}
$$

$$
\boxed{17}
$$

---

# 34. Weighted Average of Marks

Class A:

- 20 students
- average 60

Class B:

- 40 students
- average 75

Combined:

$$
\frac{20(60)+40(75)}
{60}
$$

$$
=\frac{4200}{60}
$$

$$
\boxed{70}
$$

---

# 35. Weighted Average and Frequency

If:

| Value | Frequency |
|---:|---:|
| 5 | 4 |
| 10 | 3 |
| 15 | 2 |
| 20 | 1 |

Then:

$$
WA=
\frac{5(4)+10(3)+15(2)+20(1)}
{4+3+2+1}
$$

$$
=\frac{20+30+30+20}{10}
$$

$$
\boxed{10}
$$

---

# 36. Weighted Average With Fractions

Values:

$$
10,\ 20
$$

Weights:

$$
\frac12,\ \frac32
$$

Formula:

$$
WA=
\frac{
10(\frac12)+20(\frac32)
}{
\frac12+\frac32
}
$$

$$
=
\frac{5+30}{2}
$$

$$
\boxed{17.5}
$$

---

# 37. Weighted Average With Decimals

Values:

$$
20,\ 40
$$

Weights:

$$
0.2,\ 0.8
$$

Then:

$$
WA=
20(0.2)+40(0.8)
$$

$$
=4+32
$$

$$
\boxed{36}
$$

Because weights already sum to `1`.

---

# 38. Normalized Weights

If weights do not add to `1`, divide by their total.

Example:

Weights:

$$
2,\ 3,\ 5
$$

Total:

$$
10
$$

Normalized weights:

$$
0.2,\ 0.3,\ 0.5
$$

Then:

$$
WA=0.2x_1+0.3x_2+0.5x_3
$$

---

# 39. Weighted Average Using Percentages

Suppose:

- 20% weight → score 70
- 30% weight → score 80
- 50% weight → score 90

Then:

$$
WA=
70(0.20)+80(0.30)+90(0.50)
$$

$$
=14+24+45
$$

$$
\boxed{83}
$$

---

# 40. Weighted Average and Total Weight

If:

$$
\sum w=100
$$

then:

$$
\boxed{
WA=\frac{\sum wx}{100}
}
$$

If:

$$
\sum w=1
$$

then:

$$
\boxed{
WA=\sum wx
}
$$

---

# 41. Finding an Unknown Value

Values:

- `20`, weight 2
- `x`, weight 3

Weighted average = `32`.

Then:

$$
\frac{20(2)+3x}{5}=32
$$

$$
40+3x=160
$$

$$
3x=120
$$

$$
\boxed{x=40}
$$

---

# 42. Finding an Unknown Weight

Values:

`20` and `50`.

Weights:

`2` and `x`.

Weighted average = `40`.

$$
\frac{20(2)+50x}{2+x}=40
$$

$$
40+50x=80+40x
$$

$$
10x=40
$$

$$
\boxed{x=4}
$$

Therefore weight ratio:

$$
\boxed{2:4=1:2}
$$

---

# 43. Finding Weight Ratio From Average

Two values are `20` and `50`.

Weighted average is `30`.

Find their weight ratio.

Let weights be:

$$
a:b
$$

Then:

$$
\frac{20a+50b}{a+b}=30
$$

$$
20a+50b=30a+30b
$$

$$
20b=10a
$$

$$
a:b=2:1
$$

Therefore:

$$
\boxed{2:1}
$$

---

# 44. Alligation Connection

For two values:

$$
A,\ B
$$

with weighted average `M`, the weight ratio is:

$$
\boxed{
w_A:w_B=(B-M):(M-A)
}
$$

provided:

$$
A<M<B
$$

This is the basis of **alligation**.

---

# 45. Alligation Example

Mix solutions of:

- 20%
- 50%

to obtain 30%.

Using differences:

$$
50-30=20
$$

$$
30-20=10
$$

Therefore quantity ratio:

$$
20\%:50\%
=
20:10
=
\boxed{2:1}
$$

---

# 46. Alligation Shortcut

For:

$$
A<M<B
$$

ratio of quantities:

$$
\boxed{
A:B=(B-M):(M-A)
}
$$

Example:

20 and 80 to obtain 50:

$$
20:80=(80-50):(50-20)
$$

$$
=30:30
$$

$$
\boxed{1:1}
$$

---

# 47. Weighted Average and Alligation

> [!important]
> These are two sides of the same concept.

### Weighted average

Given values + weights → find average.

### Alligation

Given values + desired average → find weight ratio.

---

# 48. Weighted Average and Mixture

Suppose:

20 kg rice at ₹40/kg.

30 kg rice at ₹60/kg.

Average price:

$$
\frac{20(40)+30(60)}
{50}
$$

$$
=\frac{2600}{50}
$$

$$
\boxed{₹52/kg}
$$

---

# 49. Weighted Average and Profit

Suppose:

₹10,000 invested at 8%.

₹20,000 invested at 12%.

Overall return:

$$
\frac{10000(8)+20000(12)}
{30000}
$$

$$
=\frac{320000}{30000}
$$

$$
\boxed{10.67\%}
$$

---

# 50. Weighted Average and Loss

If different quantities have different loss percentages, the overall loss percentage is based on the appropriate monetary weights.

> [!warning]
> Do not simply average percentages unless the underlying amounts are equal.

---

# 51. Weighted Average of Ratios

Be careful with ratios.

A ratio cannot generally be averaged directly without considering what the ratio represents and its associated weights.

> [!important]
> Identify the actual quantity behind the ratio before applying weighted average.

---

# 52. Weighted Average and Rates

Rates often require weights.

Examples:

- speed
- interest rate
- production rate
- price per unit
- concentration
- percentage return

The correct weight depends on the physical quantity involved.

---

# 53. Average Speed as Weighted Average

If speeds are used for equal time intervals, time acts as the weight:

$$
\boxed{
Average\ Speed=
\frac{\sum(vt)}{\sum t}
}
$$

For equal time:

$$
t_1=t_2
$$

the formula reduces to the ordinary average of speeds.

---

# 54. Average Price as Weighted Average

If prices differ but quantities differ:

$$
\boxed{
Average\ Price=
\frac{\sum(price\times quantity)}
{\sum quantity}
}
$$

Quantity is the weight.

---

# 55. Average Percentage as Weighted Average

If percentages apply to different bases:

$$
\boxed{
Overall\ Percentage=
\frac{\sum(base\times percentage)}
{\sum base}
}
$$

This is important in percentage problems.

---

# 56. Example — Different Bases

A company has:

- 100 employees, 20% passed
- 300 employees, 40% passed

Overall pass percentage:

$$
\frac{100(20)+300(40)}
{100+300}
$$

$$
=\frac{14000}{400}
$$

$$
\boxed{35\%}
$$

Not:

$$
\frac{20+40}{2}=30\%
$$

---

# 57. Weighted Average and Median

Do not confuse:

- weighted average
- weighted median

They are different concepts.

For aptitude, weighted average usually means:

$$
\boxed{
\frac{\sum wx}{\sum w}
}
$$

---

# 58. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Ignoring Weights

Wrong:

$$
\frac{x_1+x_2}{2}
$$

when weights differ.

Correct:

$$
\boxed{
\frac{w_1x_1+w_2x_2}{w_1+w_2}
}
$$

---

### Mistake 2 — Averaging Percentages Directly

Different bases require weighting.

---

### Mistake 3 — Averaging Group Averages Directly

Use group sizes as weights.

---

### Mistake 4 — Forgetting the Denominator

Always divide by:

$$
\boxed{\sum w}
$$

unless weights are already normalized to sum to `1`.

---

### Mistake 5 — Using Wrong Weight

For average price, weight = quantity.

For average salary, weight = number of employees.

For average concentration, weight = quantity of mixture.

---

# 59. High-Yield Exam Patterns

> [!important] Must Master

1. Basic weighted average
2. Weighted average using ratios
3. Weighted average using percentages
4. Frequency-based average
5. Combined average
6. Group average
7. Average marks
8. Average salary
9. Average age
10. Average cost
11. Average price
12. Average concentration
13. Average interest rate
14. Average return
15. Average percentage
16. Finding unknown value
17. Finding unknown weight
18. Finding weight ratio
19. Alligation
20. Mixture problems

---

# 60. Formula Sheet

> [!important] Must Remember

### Basic Weighted Average

$$
\boxed{
WA=\frac{\sum wx}{\sum w}
}
$$

### Two Values

$$
\boxed{
WA=\frac{w_1x_1+w_2x_2}
{w_1+w_2}
}
$$

### Three Values

$$
\boxed{
WA=
\frac{w_1x_1+w_2x_2+w_3x_3}
{w_1+w_2+w_3}
}
$$

### Frequency Average

$$
\boxed{
A=\frac{\sum fx}{\sum f}
}
$$

### Combined Average

$$
\boxed{
A_c=
\frac{n_1A_1+n_2A_2}
{n_1+n_2}
}
$$

### Weighted Percentage

$$
\boxed{
P=
\frac{\sum(base\times rate)}
{\sum base}
}
$$

### Weighted Price

$$
\boxed{
P=
\frac{\sum(quantity\times price)}
{\sum quantity}
}
$$

### Weighted Rate

$$
\boxed{
R=
\frac{\sum(weight\times rate)}
{\sum weight}
}
$$

### Alligation

$$
\boxed{
w_1:w_2=(x_2-M):(M-x_1)
}
$$

### Weighted Deviation

$$
\boxed{
WA=A_0+\frac{\sum wd}{\sum w}
}
$$

---

# 61. Quick Revision

> [!summary] One-Minute Revision

### Core Formula

$$
\boxed{
Weighted\ Average=
\frac{\sum wx}{\sum w}
}
$$

### Think

> **Value × Importance**

Then divide by:

> **Total Importance**

### Example

Values:

$$
20,\ 50
$$

Weights:

$$
2:3
$$

$$
WA=
\frac{20(2)+50(3)}5
$$

$$
=\frac{190}{5}
$$

$$
\boxed{38}
$$

### Key Insight

> **Bigger weight → stronger pull toward that value.**

### Combined Average

> Group size = weight.

### Frequency Average

> Frequency = weight.

### Mixture

> Quantity = weight.

### Price

> Quantity purchased = weight.

### Salary

> Number of employees = weight.

### Percentage

> Base amount = weight.

### Golden Memory Trick

$$
\boxed{
Weighted\ Average=
\frac{Value\times Weight\ total}{Weight\ total}
}
$$

More precisely:

$$
\boxed{
WA=\frac{\sum(Value\times Weight)}
{\sum Weight}
}
$$

---

# 62. Exam Recognition Map

```text
WEIGHTED AVERAGE
│
├── Values + Weights
│   └── Σ(wx) / Σw
│
├── Groups
│   └── Group Size = Weight
│
├── Frequency
│   └── Frequency = Weight
│
├── Mixture
│   └── Quantity = Weight
│
├── Price
│   └── Quantity = Weight
│
├── Salary
│   └── Number of Employees = Weight
│
├── Percentage
│   └── Base Amount = Weight
│
├── Rates
│   └── Relevant Quantity = Weight
│
└── Alligation
    └── Find Weight Ratio