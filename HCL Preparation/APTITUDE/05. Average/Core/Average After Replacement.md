---
type: concept
subject: aptitude
topic: "Average After Replacement"
parent: "05. Average"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - average
  - average-after-replacement
  - quantitative-aptitude
wikilinks:
  - "[[05. Average]]"
  - "[[Average of Numbers]]"
  - "[[Average After Addition]]"
  - "[[Average After Removal]]"
  - "[[Combined Average]]"
---

# Average After Replacement

## 1. Core Concept

> [!summary]
> In a **replacement** problem, one or more existing values are removed and replaced by new values.
>
> The **number of observations remains the same**, but the **total changes**.

The key idea is:

> **Find the change in total, then divide that change by the unchanged count.**

---

# 2. Golden Formula — One Value Replaced

Suppose:

- Number of observations = `n`
- Old average = `A`
- Old value = `x`
- New value = `y`

Change in total:

$$
y-x
$$

Since the count remains `n`:

$$
\boxed{
New\ Average
=
A+\frac{y-x}{n}
}
$$

---

# 3. Basic Example

Average of 10 numbers is `25`.

One value `20` is replaced by `40`.

Change:

$$
40-20=20
$$

Average increase:

$$
\frac{20}{10}=2
$$

New average:

$$
25+2
=
\boxed{27}
$$

---

# 4. Total Method

The same problem can be solved using totals.

Old total:

$$
10(25)=250
$$

Remove old value:

$$
250-20=230
$$

Add new value:

$$
230+40=270
$$

Count remains:

$$
10
$$

New average:

$$
\boxed{27}
$$

---

# 5. Most Important Insight

> [!important]
> **Replacement changes the total but does NOT change the number of observations.**

Compare:

### Addition

$$
n\rightarrow n+1
$$

### Removal

$$
n\rightarrow n-1
$$

### Replacement

$$
\boxed{n\rightarrow n}
$$

This distinction is extremely important.

---

# 6. Replacement Formula

$$
\boxed{
New\ Average
=
Old\ Average+
\frac{New\ Value-Old\ Value}{n}
}
$$

---

# 7. If New Value Is Greater

If:

$$
y>x
$$

then:

$$
\boxed{New\ Average>Old\ Average}
$$

Example:

Old = 30

New = 50

Count = 10

Increase:

$$
\frac{50-30}{10}=2
$$

New average:

$$
\boxed{32}
$$

---

# 8. If New Value Is Smaller

If:

$$
y<x
$$

then:

$$
\boxed{New\ Average<Old\ Average}
$$

Example:

Old = 50

New = 30

Count = 10

Change:

$$
\frac{30-50}{10}
=
-2
$$

New average:

$$
\boxed{48}
$$

---

# 9. If New Value Equals Old Value

If:

$$
y=x
$$

then:

$$
y-x=0
$$

Therefore:

$$
\boxed{New\ Average=Old\ Average}
$$

---

# 10. Finding the New Average

Average of 20 students is `60`.

A student scoring `40` is replaced by a student scoring `80`.

Change:

$$
80-40=40
$$

Average increase:

$$
40/20=2
$$

New average:

$$
\boxed{62}
$$

---

# 11. Finding the Old Value

Average of 10 numbers is `30`.

One number is replaced by `50`.

New average becomes `33`.

Find the old number.

Using:

$$
33=
30+\frac{50-x}{10}
$$

$$
3=\frac{50-x}{10}
$$

$$
30=50-x
$$

$$
\boxed{x=20}
$$

---

# 12. Formula for Old Value

Given:

- Old average = `A`
- New average = `B`
- New value = `y`
- Count = `n`

From:

$$
B=A+\frac{y-x}{n}
$$

we get:

$$
B-A=\frac{y-x}{n}
$$

Therefore:

$$
\boxed{
x=y-n(B-A)
}
$$

Equivalent form:

$$
\boxed{
x=y+n(A-B)
}
$$

---

# 13. Finding the New Value

Average of 15 numbers is `40`.

One value `30` is replaced.

New average becomes `42`.

Find the new value.

Increase in total:

$$
(42-40)(15)=30
$$

Therefore:

$$
New-30=30
$$

$$
\boxed{New=60}
$$

---

# 14. Formula for New Value

Given:

- Old average = `A`
- New average = `B`
- Old value = `x`
- Count = `n`

Then:

$$
\boxed{
y=x+n(B-A)
}
$$

---

# 15. Example

Average of 12 numbers = `35`.

One value `25` is replaced.

New average = `40`.

New value:

$$
25+12(40-35)
$$

$$
=25+60
$$

$$
\boxed{85}
$$

---

# 16. Finding the Number of Observations

Old average = `30`.

Old value = `20`.

New value = `50`.

New average = `33`.

Find `n`.

Change in average:

$$
33-30=3
$$

Change in value:

$$
50-20=30
$$

Therefore:

$$
n=\frac{30}{3}
$$

$$
\boxed{10}
$$

---

# 17. Formula for Number of Observations

$$
B-A=\frac{y-x}{n}
$$

Therefore:

$$
\boxed{
n=
\frac{y-x}{B-A}
}
$$

Use absolute values when only the magnitude of change is being considered:

$$
\boxed{
n=
\frac{|y-x|}
{|B-A|}
}
$$

---

# 18. Replacement and Total Change

If one value changes from `x` to `y`:

$$
\boxed{
Change\ in\ Total=y-x
}
$$

Therefore:

$$
\boxed{
Change\ in\ Average=
\frac{y-x}{n}
}
$$

This is the fastest way to think about replacement problems.

---

# 19. Example — Direct Shortcut

Average of 25 numbers = `48`.

A value `38` is replaced by `63`.

Change:

$$
63-38=25
$$

Average change:

$$
25/25=1
$$

New average:

$$
\boxed{49}
$$

---

# 20. Replacement of Multiple Values

Suppose:

- `n` observations
- old average = `A`
- `m` values are replaced

Let:

- Sum of old values = `S_old`
- Sum of new values = `S_new`

Change in total:

$$
S_{new}-S_{old}
$$

Therefore:

$$
\boxed{
New\ Average
=
A+
\frac{S_{new}-S_{old}}
{n}
}
$$

---

# 21. Example — Two Values Replaced

Average of 20 numbers = `50`.

Values `30` and `40` are replaced by `60` and `70`.

Old sum:

$$
30+40=70
$$

New sum:

$$
60+70=130
$$

Change:

$$
130-70=60
$$

Average increase:

$$
60/20=3
$$

New average:

$$
\boxed{53}
$$

---

# 22. Multiple Replacement Formula

If:

- `m` values are replaced
- old replaced group average = `A₁`
- new replacement group average = `A₂`

then:

Old replaced total:

$$
mA_1
$$

New replaced total:

$$
mA_2
$$

Change:

$$
m(A_2-A_1)
$$

Therefore:

$$
\boxed{
New\ Average
=
A+
\frac{m(A_2-A_1)}
{n}
}
$$

---

# 23. Example — Group Replacement

Average of 50 employees = ₹40,000.

10 employees with average salary ₹30,000 are replaced by 10 employees with average salary ₹50,000.

Change in replaced group average:

$$
50000-30000
=
20000
$$

Change in total:

$$
10(20000)=200000
$$

Average increase:

$$
200000/50
=
4000
$$

New average:

$$
\boxed{₹44,000}
$$

---

# 24. Replacement Does Not Change Count

Suppose:

100 students are in a class.

5 students are replaced.

The class still has:

$$
\boxed{100}
$$

students.

This means the denominator in the average remains `100`.

---

# 25. Addition vs Replacement

Suppose average = 50 for 10 values.

### Add 70

New count:

$$
11
$$

New average:

$$
\frac{500+70}{11}
=
\boxed{51.82}
$$

### Replace one value 30 with 70

Count remains:

$$
10
$$

New average:

$$
50+\frac{70-30}{10}
=
\boxed{54}
$$

> [!warning]
> Do not treat replacement as addition.

---

# 26. Removal vs Replacement

Suppose:

- Average = 50
- Count = 10
- Remove 30

New average:

$$
\frac{500-30}{9}
=
\boxed{52.22}
$$

If instead 30 is replaced by 70:

$$
50+\frac{70-30}{10}
=
\boxed{54}
$$

Different operations produce different answers.

---

# 27. Replacement of a Group

Suppose:

- Total group size = `n`
- `m` members are replaced
- Old replaced group average = `A₁`
- New replaced group average = `A₂`

Then:

$$
\boxed{
New\ Average
=
A+
\frac{m(A_2-A_1)}
{n}
}
$$

---

# 28. Finding Number Replaced

Old average = `50`.

New average = `52`.

Old replaced group average = `40`.

New replaced group average = `60`.

Let `m` people be replaced.

$$
52=
50+
\frac{m(60-40)}
{n}
$$

If `n=100`:

$$
2=\frac{20m}{100}
$$

$$
200=20m
$$

$$
\boxed{m=10}
$$

---

# 29. Formula for Number Replaced

From:

$$
B-A=
\frac{m(A_2-A_1)}
{n}
$$

we get:

$$
\boxed{
m=
\frac{n(B-A)}
{A_2-A_1}
}
$$

---

# 30. Replacement With Same Average

If:

$$
A_1=A_2
$$

then:

$$
A_2-A_1=0
$$

Therefore:

$$
\boxed{New\ Average=Old\ Average}
$$

---

# 31. Example

A class has 40 students with average marks 70.

5 students with average marks 70 are replaced by another 5 students with average marks 70.

New average:

$$
\boxed{70}
$$

---

# 32. Replacement With Higher Average

If:

$$
A_2>A_1
$$

then:

$$
\boxed{New\ Average>Old\ Average}
$$

The average increases.

---

# 33. Replacement With Lower Average

If:

$$
A_2<A_1
$$

then:

$$
\boxed{New\ Average<Old\ Average}
$$

The average decreases.

---

# 34. Replacement Change Depends on Two Things

The change in average depends on:

1. Difference between old and new values
2. Total number of observations

Formula:

$$
\boxed{
Average\ Change=
\frac{Value\ Change}{Total\ Count}
}
$$

For group replacement:

$$
\boxed{
Average\ Change=
\frac{Number\ Replaced\times Average\ Difference}
{Total\ Count}
}
$$

---

# 35. Larger Group Means Smaller Impact

Suppose a value changes by `20`.

### 10 observations

$$
20/10=2
$$

Average changes by `2`.

### 100 observations

$$
20/100=0.2
$$

Average changes by only `0.2`.

> [!important]
> The larger the total group, the smaller the effect of replacing a single value.

---

# 36. Finding Required Replacement Value

Average of 20 numbers = `45`.

One value `25` must be replaced so that average becomes `47`.

Required total increase:

$$
(47-45)(20)=40
$$

Therefore:

$$
New-25=40
$$

$$
\boxed{New=65}
$$

---

# 37. Finding Required Replacement Value — Shortcut

$$
\boxed{
New\ Value=
Old\ Value+n(New\ Average-Old\ Average)
}
$$

---

# 38. Example

Average = `60`.

Count = `25`.

Old value = `45`.

Required new average = `62`.

New value:

$$
45+25(62-60)
$$

$$
=45+50
$$

$$
\boxed{95}
$$

---

# 39. Finding Required Old Value

Average = `60`.

Count = `25`.

New value = `80`.

Required new average = `62`.

Old value:

$$
80-25(62-60)
$$

$$
=80-50
$$

$$
\boxed{30}
$$

---

# 40. Finding Number of Observations

Old value = `40`.

New value = `70`.

Average changes from `50` to `52`.

Change in value:

$$
70-40=30
$$

Change in average:

$$
52-50=2
$$

Therefore:

$$
n=30/2
$$

$$
\boxed{15}
$$

---

# 41. Replacement With Percentage Change

Suppose a value is replaced and the average increases by `5%`.

If old average = `40`:

New average:

$$
40(1.05)=42
$$

Average increase:

$$
2
$$

For `n` observations:

$$
New-Old=n(2)
$$

Therefore:

$$
\boxed{
New\ Value=
Old\ Value+2n
}
$$

---

# 42. Example

Average of 20 numbers = `50`.

After replacement, average increases by `10%`.

New average:

$$
50(1.10)=55
$$

Increase:

$$
5
$$

Total increase required:

$$
20(5)=100
$$

If old value = `30`:

$$
New=30+100
$$

$$
\boxed{130}
$$

---

# 43. Replacement and Percentage Error

If one incorrect value is replaced with the correct value, the average changes by:

$$
\boxed{
\frac{Correct-Incorrect}{n}
}
$$

This is useful in average-error problems.

---

# 44. Example — Incorrect Entry

Average of 20 numbers was calculated using `45` instead of `65`.

Correct average:

$$
Old\ Average+
\frac{65-45}{20}
$$

$$
=Old\ Average+1
$$

So the correct average is:

$$
\boxed{Old\ Average+1}
$$

---

# 45. Incorrect Number Formula

If an incorrect value `x` was used instead of correct value `y`:

$$
\boxed{
Correct\ Average=
Wrong\ Average+
\frac{y-x}{n}
}
$$

---

# 46. Example — Wrong Average

Average of 30 numbers is calculated as `40`.

One number `25` was entered instead of `55`.

Correct average:

$$
40+\frac{55-25}{30}
$$

$$
=40+1
$$

$$
\boxed{41}
$$

---

# 47. Average and Data Correction

This pattern frequently appears in aptitude questions:

> "The average was calculated incorrectly because one value was recorded wrongly."

Think:

$$
\boxed{
Correct\ Average=
Wrong\ Average+
\frac{Correct\ Value-Wrong\ Value}
{Number\ of\ Values}
}
$$

---

# 48. Multiple Incorrect Entries

If several values are corrected:

$$
\boxed{
Correct\ Average=
Wrong\ Average+
\frac{
\sum Correct-\sum Wrong
}
{n}
}
$$

---

# 49. Example — Multiple Corrections

Average of 50 values was `30`.

Two values `20` and `25` were entered instead of `30` and `35`.

Correction:

$$
(30+35)-(20+25)
$$

$$
=65-45
$$

$$
=20
$$

Average correction:

$$
20/50
=
0.4
$$

Correct average:

$$
\boxed{30.4}
$$

---

# 50. Replacement and Average Difference

Suppose:

Old average = `A`.

New average = `B`.

Then:

$$
\boxed{
Total\ Change=n(B-A)
}
$$

For one replacement:

$$
\boxed{
New-Old=n(B-A)
}
$$

---

# 51. Example

Average of 40 students increases from `65` to `67`.

Total increase:

$$
40(67-65)
$$

$$
\boxed{80}
$$

Therefore the replacement increased the total marks by `80`.

---

# 52. Multiple Replacement Using Total Difference

Old replaced values:

$$
20,\ 30,\ 40
$$

New values:

$$
40,\ 50,\ 60
$$

Old total:

$$
90
$$

New total:

$$
150
$$

Total increase:

$$
60
$$

If total observations = `30`:

Average increase:

$$
60/30
=
\boxed{2}
$$

---

# 53. Replacement and Weighted Average

If a subgroup is replaced, treat the old and new subgroup averages as two values with the same weight `m`.

Old contribution:

$$
mA_1
$$

New contribution:

$$
mA_2
$$

Difference:

$$
m(A_2-A_1)
$$

---

# 54. Replacement in Salary Problems

A company has 100 employees with average salary ₹30,000.

An employee earning ₹20,000 is replaced by an employee earning ₹50,000.

Increase in total:

$$
50000-20000=30000
$$

Average increase:

$$
30000/100
=
300
$$

New average:

$$
\boxed{₹30,300}
$$

---

# 55. Replacement in Marks Problems

A class has 50 students with average marks 60.

A student who scored 40 is replaced by one who scored 90.

Change:

$$
90-40=50
$$

Average increase:

$$
50/50=1
$$

New average:

$$
\boxed{61}
$$

---

# 56. Replacement in Age Problems

A group has 20 people with average age 30.

A person aged 20 leaves and a person aged 40 joins.

Change:

$$
40-20=20
$$

Average increase:

$$
20/20=1
$$

New average:

$$
\boxed{31}
$$

---

# 57. Replacement in Cost Problems

A shop has 25 products with average cost ₹500.

A product costing ₹300 is replaced by one costing ₹700.

Change:

$$
700-300=400
$$

Average increase:

$$
400/25
=
16
$$

New average:

$$
\boxed{₹516}
$$

---

# 58. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Changing the Count

Replacement does not change the number of observations.

### Mistake 2 — Adding the New Value Without Removing the Old

Wrong:

$$
Total+New
$$

Correct:

$$
\boxed{
Total-Old+New
}
$$

### Mistake 3 — Dividing by `n+1`

Do not do this for replacement.

The count remains `n`.

### Mistake 4 — Forgetting the Direction

If new value is higher, average must increase.

### Mistake 5 — Confusing Value Change With Average Change

If a value changes by `20`, average changes by:

$$
20/n
$$

not `20`.

---

# 59. High-Yield Exam Patterns

> [!important] Must Master

1. One value replacement
2. Find new average
3. Find old value
4. Find new value
5. Find number of observations
6. Multiple values replaced
7. Group replacement
8. Find number replaced
9. Replacement with percentage change
10. Incorrect value correction
11. Multiple incorrect entries
12. Average increase after replacement
13. Average decrease after replacement
14. Marks replacement
15. Salary replacement
16. Age replacement
17. Cost replacement
18. Data correction
19. Reverse replacement
20. Shortcut-based questions

---

# 60. Formula Sheet

> [!important] Must Remember

### One Replacement

$$
\boxed{
A_{new}
=
A+
\frac{New-Old}{n}
}
$$

### Average Change

$$
\boxed{
A_{new}-A=
\frac{New-Old}{n}
}
$$

### New Value

$$
\boxed{
New=
Old+n(A_{new}-A)
}
$$

### Old Value

$$
\boxed{
Old=
New-n(A_{new}-A)
}
$$

### Number of Values

$$
\boxed{
n=
\frac{New-Old}
{A_{new}-A}
}
$$

### Multiple Replacement

$$
\boxed{
A_{new}
=
A+
\frac{
\sum New-\sum Old
}{n}
}
$$

### Group Replacement

$$
\boxed{
A_{new}
=
A+
\frac{m(A_2-A_1)}
{n}
}
$$

### Number Replaced

$$
\boxed{
m=
\frac{
n(A_{new}-A)
}{
A_2-A_1
}
}
$$

### Correcting an Incorrect Value

$$
\boxed{
Correct\ Average
=
Wrong\ Average+
\frac{Correct-Wrong}
{n}
}
$$

---

# 61. Quick Revision

> [!summary] One-Minute Revision

### Golden Rule

> **Replacement = Remove old + Add new**

### Total Change

$$
\boxed{
New-Old
}
$$

### Average Change

$$
\boxed{
\frac{New-Old}{n}
}
$$

### New Average

$$
\boxed{
Old\ Average+
\frac{New-Old}{n}
}
$$

### Key Difference

| Operation | Count |
|---|---:|
| Addition | `n + 1` |
| Removal | `n - 1` |
| Replacement | `n` |

### Fast Recognition

If the question says:

> "One person/value/student is replaced..."

Immediately think:

$$
\boxed{
Average\ Change=
\frac{Replacement\ Difference}{Total\ Count}
}
$$

---

# 62. Exam Recognition Map

```text
AVERAGE AFTER REPLACEMENT
│
├── One Value
│   ├── Find New Average
│   ├── Find Old Value
│   ├── Find New Value
│   └── Find Count
│
├── Multiple Values
│   ├── Sum of Old Values
│   └── Sum of New Values
│
├── Group Replacement
│   ├── Old Group Average
│   ├── New Group Average
│   └── Number Replaced
│
├── Data Correction
│   ├── Wrong Value
│   └── Correct Value
│
└── Shortcut
    └── Average Change
        = (New − Old) / n
```

> [!success]
> **Core skill:** In every replacement problem, remember:
>
> $$\boxed{Count\ stays\ the\ same}$$
>
> Only the total changes:
>
> $$\boxed{New\ Total=Old\ Total-Old\ Value+New\ Value}$$
>
> Therefore:
>
> $$\boxed{
> New\ Average=
> Old\ Average+
> \frac{New-Old}{n}
> }$$