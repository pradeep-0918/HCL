---
type: concept
subject: aptitude
topic: "Combined Average"
parent: "05. Average"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - average
  - combined-average
  - quantitative-aptitude
wikilinks:
  - "[[05. Average]]"
  - "[[Basic Average]]"
  - "[[Average of Numbers]]"
  - "[[Weighted Average]]"
  - "[[Average-Based Applications]]"
---

# Combined Average

## 1. Core Concept

> [!summary]
> **Combined average** is the average of two or more groups considered together.

The key idea is:

> **Convert each group's average into its total, combine the totals, then divide by the combined number of observations.**

---

# 2. Golden Formula

For two groups:

- Group 1 → `n₁` observations, average `A₁`
- Group 2 → `n₂` observations, average `A₂`

Then:

$$
\boxed{
Combined\ Average=
\frac{n_1A_1+n_2A_2}
{n_1+n_2}
}
$$

---

# 3. Why This Formula Works

For Group 1:

$$
Total_1=n_1A_1
$$

For Group 2:

$$
Total_2=n_2A_2
$$

Combined total:

$$
n_1A_1+n_2A_2
$$

Combined number:

$$
n_1+n_2
$$

Therefore:

$$
\boxed{
Combined\ Average=
\frac{Combined\ Total}
{Combined\ Number}
}
$$

---

# 4. Basic Example

Class A:

- 20 students
- Average marks = 60

Class B:

- 30 students
- Average marks = 70

### Step 1 — Find totals

Class A:

$$
20\times60=1200
$$

Class B:

$$
30\times70=2100
$$

### Step 2 — Combine

$$
Total=1200+2100=3300
$$

Students:

$$
20+30=50
$$

### Step 3 — Combined average

$$
\frac{3300}{50}
=
\boxed{66}
$$

---

# 5. Most Important Rule

> [!important]
> **Never simply average two group averages unless the groups have equal sizes.**

Wrong:

$$
\frac{60+70}{2}=65
$$

Correct:

$$
\frac{20(60)+30(70)}{20+30}
=
\boxed{66}
$$

---

# 6. Equal-Sized Groups

If two groups have the same number of observations:

$$
n_1=n_2
$$

then:

$$
\boxed{
Combined\ Average=
\frac{A_1+A_2}{2}
}
$$

Example:

Group A average = 60.

Group B average = 80.

Both have 20 students.

Therefore:

$$
\frac{60+80}{2}
=
\boxed{70}
$$

---

# 7. Three Groups

For three groups:

$$
\boxed{
A_c=
\frac{
n_1A_1+n_2A_2+n_3A_3
}{
n_1+n_2+n_3
}
}
$$

Example:

| Group | Number | Average |
|---|---:|---:|
| A | 10 | 50 |
| B | 20 | 60 |
| C | 30 | 70 |

Total:

$$
10(50)+20(60)+30(70)
$$

$$
=500+1200+2100
$$

$$
=3800
$$

Total people:

$$
10+20+30=60
$$

Combined average:

$$
\frac{3800}{60}
=
\boxed{63.33}
$$

---

# 8. Four Groups

For four groups:

$$
\boxed{
A_c=
\frac{
n_1A_1+n_2A_2+n_3A_3+n_4A_4
}{
n_1+n_2+n_3+n_4
}
}
$$

The same principle works for any number of groups.

---

# 9. Combined Average as Weighted Average

> [!important]
> **Combined average is a weighted average.**

The:

- group average = value
- group size = weight

Therefore:

$$
\boxed{
Combined\ Average=
\frac{\sum(nA)}
{\sum n}
}
$$

---

# 10. Example

Group 1:

`15` people, average `40`.

Group 2:

`25` people, average `60`.

Combined:

$$
\frac{15(40)+25(60)}
{15+25}
$$

$$
=
\frac{600+1500}{40}
$$

$$
\boxed{52.5}
$$

---

# 11. Combined Average Must Lie Between Group Averages

If:

$$
A_1<A_2
$$

then:

$$
\boxed{
A_1<A_c<A_2
}
$$

for positive group sizes.

Example:

Average 40 and 60.

Combined average must lie between:

$$
\boxed{40\text{ and }60}
$$

---

# 12. Quick Checking Trick

Suppose your answer is `75` when the group averages are:

$$
40,\ 60
$$

Impossible.

The combined average cannot exceed `60`.

> [!tip]
> Always check whether your answer lies between the group averages.

---

# 13. Finding Combined Total

If:

- Group 1: 20 people, average 50
- Group 2: 30 people, average 70

Total:

$$
20(50)+30(70)
$$

$$
=1000+2100
$$

$$
\boxed{3100}
$$

---

# 14. Finding Combined Number

If:

Group A has 25 students.

Group B has 35 students.

Combined:

$$
25+35
=
\boxed{60}
$$

---

# 15. Finding Combined Average From Totals

If:

Total of Group A = 1200.

Total of Group B = 1800.

Numbers:

- Group A = 20
- Group B = 30

Combined total:

$$
1200+1800=3000
$$

Combined count:

$$
20+30=50
$$

Combined average:

$$
\boxed{60}
$$

---

# 16. Finding Missing Group Average

Group A:

- 20 people
- average = 50

Group B:

- 30 people
- average = `x`

Combined average = 60.

Use:

$$
\frac{20(50)+30x}{50}=60
$$

$$
1000+30x=3000
$$

$$
30x=2000
$$

$$
\boxed{x=66.67}
$$

---

# 17. Finding Missing Group Size

Group A:

- 20 people
- average = 50

Group B:

- `x` people
- average = 70

Combined average = 60.

$$
\frac{20(50)+70x}{20+x}=60
$$

$$
1000+70x=1200+60x
$$

$$
10x=200
$$

$$
\boxed{x=20}
$$

---

# 18. Finding Group Size Using Deviation

Suppose:

- Group A average = 40
- Group B average = 60
- Combined average = 50

Since 50 is exactly halfway between 40 and 60:

$$
\boxed{
Group\ sizes=1:1
}
$$

---

# 19. Important Weight-Ratio Formula

If:

- Group A average = `A`
- Group B average = `B`
- Combined average = `C`

then:

$$
\boxed{
n_A:n_B=(B-C):(C-A)
}
$$

provided:

$$
A<C<B
$$

This is the same idea as alligation.

---

# 20. Example — Find Group Size Ratio

Group A average = 40.

Group B average = 70.

Combined average = 50.

Then:

$$
n_A:n_B
=
(70-50):(50-40)
$$

$$
=20:10
$$

$$
\boxed{2:1}
$$

So Group A has twice as many observations as Group B.

---

# 21. Another Example

Average of boys = 60.

Average of girls = 80.

Combined average = 68.

Find number ratio.

$$
Boys:Girls
=
(80-68):(68-60)
$$

$$
=12:8
$$

$$
\boxed{3:2}
$$

---

# 22. Combined Average With Three Groups

Group A:

- 10 people
- average 20

Group B:

- 20 people
- average 30

Group C:

- 30 people
- average 40

Combined total:

$$
10(20)+20(30)+30(40)
$$

$$
=200+600+1200
$$

$$
=2000
$$

Combined count:

$$
60
$$

Average:

$$
\frac{2000}{60}
=
\boxed{33.33}
$$

---

# 23. Combined Average of Classes

Class A:

`40` students, average marks `55`.

Class B:

`60` students, average marks `65`.

Combined:

$$
\frac{40(55)+60(65)}
{100}
$$

$$
=\frac{2200+3900}{100}
$$

$$
\boxed{61}
$$

---

# 24. Combined Average of Ages

Group A:

10 people, average age 20.

Group B:

15 people, average age 30.

Combined:

$$
\frac{10(20)+15(30)}
{25}
$$

$$
=\frac{650}{25}
$$

$$
\boxed{26}
$$

---

# 25. Combined Average Salary

Department A:

20 employees, average salary ₹30,000.

Department B:

30 employees, average salary ₹40,000.

Combined salary:

$$
20(30000)+30(40000)
$$

$$
=600000+1200000
$$

$$
=1800000
$$

Total employees:

$$
50
$$

Average salary:

$$
\frac{1800000}{50}
$$

$$
\boxed{₹36,000}
$$

---

# 26. Combined Average Marks

Class A:

25 students, average = 72.

Class B:

35 students, average = 78.

Combined:

$$
\frac{25(72)+35(78)}
{60}
$$

$$
=\frac{1800+2730}{60}
$$

$$
=\frac{4530}{60}
$$

$$
\boxed{75.5}
$$

---

# 27. Combined Average Cost

10 products cost an average of ₹100.

20 products cost an average of ₹150.

Combined average:

$$
\frac{10(100)+20(150)}
{30}
$$

$$
=\frac{4000}{30}
$$

$$
\boxed{₹133.33}
$$

---

# 28. Combined Average Price

20 kg rice costs average ₹40/kg.

30 kg rice costs average ₹50/kg.

Combined:

$$
\frac{20(40)+30(50)}
{50}
$$

$$
=\frac{2300}{50}
$$

$$
\boxed{₹46/kg}
$$

---

# 29. Combined Average Percentage

Group A:

100 people, 20% passed.

Group B:

300 people, 40% passed.

Combined pass percentage:

$$
\frac{100(20)+300(40)}
{400}
$$

$$
=\frac{14000}{400}
$$

$$
\boxed{35\%}
$$

> [!warning]
> Do not calculate:

$$
\frac{20+40}{2}=30\%
$$

because the group sizes differ.

---

# 30. Combined Average Speed

Average speed should be handled using:

$$
\boxed{
Average\ Speed=
\frac{Total\ Distance}
{Total\ Time}
}
$$

Do not automatically use the combined-average formula on speeds.

The correct weights depend on the time or distance involved.

---

# 31. Combined Average With Equal Time

If a vehicle travels for equal amounts of time at speeds:

$$
40,\ 60
$$

then:

$$
Average=
\frac{40+60}{2}
$$

$$
\boxed{50\text{ km/h}}
$$

Here, equal time means equal weights.

---

# 32. Combined Average With Equal Distance

If a vehicle travels equal distances at:

$$
40,\ 60
$$

then average speed is:

$$
\boxed{
\frac{2(40)(60)}
{40+60}
}
$$

$$
\boxed{48\text{ km/h}}
$$

Not `50 km/h`.

---

# 33. Combined Average After Adding a Group

Suppose:

Current group:

- 20 people
- average = 50

Another group of 10 people has average 70.

New combined average:

$$
\frac{20(50)+10(70)}
{30}
$$

$$
=\frac{1700}{30}
$$

$$
\boxed{56.67}
$$

---

# 34. Combined Average After Removing a Group

A group contains 50 students with average 60.

A subgroup of 10 students has average 50.

Remaining 40 students' average:

Old total:

$$
50(60)=3000
$$

Removed total:

$$
10(50)=500
$$

Remaining total:

$$
3000-500=2500
$$

Remaining students:

$$
40
$$

Average:

$$
\boxed{62.5}
$$

---

# 35. Finding Remaining Group Average

General formula:

$$
\boxed{
A_{remaining}
=
\frac{nA-n_rA_r}
{n-n_r}
}
$$

Where:

- `n` = original number
- `A` = original average
- `nᵣ` = removed number
- `Aᵣ` = removed group's average

---

# 36. Example — Remaining Group

100 students have average marks 60.

20 students have average 75.

Find average of remaining 80.

Original total:

$$
100(60)=6000
$$

Removed total:

$$
20(75)=1500
$$

Remaining total:

$$
4500
$$

Remaining average:

$$
4500/80
=
\boxed{56.25}
$$

---

# 37. Combined Average After Replacement of a Group

Group A:

50 people, average 60.

20 people are replaced by another group whose average is 80.

Old total contribution of replaced group:

$$
20(60)=1200
$$

New contribution:

$$
20(80)=1600
$$

Total increase:

$$
400
$$

Since total group size remains 50:

Average increase:

$$
400/50=8
$$

New average:

$$
\boxed{68}
$$

---

# 38. Replacement of an Individual vs Group

### One value replaced

$$
\boxed{
New\ Average=
Old\ Average+
\frac{New-Old}{n}
}
$$

### A subgroup replaced

$$
\boxed{
New\ Average=
Old\ Average+
\frac{
n_r(A_{new}-A_{old})
}{n}
}
$$

---

# 39. Combined Average and Weighted Average

Remember:

$$
\boxed{
Combined\ Average=
Weighted\ Average
}
$$

where:

$$
\boxed{
Weight=Group\ Size
}
$$

This connection makes many problems easier.

---

# 40. Combined Average and Alligation

If two group averages are:

$$
A,\ B
$$

and combined average is `C`, then:

$$
\boxed{
n_A:n_B
=
(B-C):(C-A)
}
$$

This can save significant time.

---

# 41. Example — Alligation Shortcut

Group A average = 50.

Group B average = 80.

Combined average = 60.

Then:

$$
A:B
=
(80-60):(60-50)
$$

$$
=20:10
$$

$$
\boxed{2:1}
$$

---

# 42. Finding Exact Group Sizes

If ratio of group sizes is:

$$
2:1
$$

and total people = `60`:

Total ratio parts:

$$
2+1=3
$$

One part:

$$
60/3=20
$$

Therefore:

$$
\boxed{40,\ 20}
$$

---

# 43. Finding Group Sizes From Ratio

If:

$$
n_1:n_2=3:2
$$

and total = `100`:

Total parts:

$$
5
$$

One part:

$$
20
$$

Group sizes:

$$
\boxed{60,\ 40}
$$

---

# 44. Combined Average With Equal Group Size

Three groups each contain 20 students.

Averages:

$$
60,\ 70,\ 80
$$

Since sizes are equal:

$$
Combined=
\frac{60+70+80}{3}
$$

$$
\boxed{70}
$$

---

# 45. Combined Average With Different Group Sizes

Three groups:

| Group | Size | Average |
|---|---:|---:|
| A | 10 | 50 |
| B | 20 | 70 |
| C | 30 | 90 |

Combined:

$$
\frac{
10(50)+20(70)+30(90)
}{
60
}
$$

$$
=
\frac{500+1400+2700}{60}
$$

$$
=\frac{4600}{60}
$$

$$
\boxed{76.67}
$$

---

# 46. Important Observation

The largest group has the greatest influence.

In the previous example:

- A → 10 people
- B → 20 people
- C → 30 people

C has the highest average and the largest size.

Therefore the combined average is pulled strongly toward `90`.

---

# 47. Fast Estimation

Suppose:

- 10 people → average 40
- 90 people → average 80

Because the second group dominates:

$$
Combined\ Average
$$

should be close to `80`.

Exact:

$$
\frac{10(40)+90(80)}{100}
=
\boxed{76}
$$

---

# 48. Important Bounds

If:

$$
A_1<A_2<A_3
$$

then combined average must satisfy:

$$
\boxed{
A_1<A_c<A_3
}
$$

It will generally be closer to the average of the group with the largest size.

---

# 49. Finding Original Average

Suppose:

- 20 people have average `50`
- 30 people have average `70`

Combined average = `x`.

$$
x=
\frac{20(50)+30(70)}
{50}
$$

$$
\boxed{x=62}
$$

---

# 50. Finding Group Average From Combined Average

Group 1:

20 people, average 50.

Group 2:

30 people, average `x`.

Combined average = 65.

$$
\frac{20(50)+30x}{50}=65
$$

$$
1000+30x=3250
$$

$$
30x=2250
$$

$$
\boxed{x=75}
$$

---

# 51. Finding Group Size From Combined Average

Group A:

Average 40.

Group B:

Average 70.

Combined average 60.

Let sizes be:

$$
x:y
$$

Using alligation:

$$
x:y=(70-60):(60-40)
$$

$$
=10:20
$$

$$
\boxed{1:2}
$$

---

# 52. Combined Average of Ages After Joining

20 employees have average age 30.

10 new employees have average age 40.

New average:

$$
\frac{20(30)+10(40)}
{30}
$$

$$
=\frac{1000}{30}
$$

$$
\boxed{33.33}
$$

---

# 53. Combined Average of Two Classes

Class A:

40 students, average 65.

Class B:

60 students, average 75.

Combined:

$$
\frac{40(65)+60(75)}
{100}
$$

$$
=\frac{2600+4500}{100}
$$

$$
\boxed{71}
$$

---

# 54. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Simple Average of Averages

Wrong when group sizes differ.

### Mistake 2 — Forgetting Group Size

Average alone is not enough.

### Mistake 3 — Adding Averages

You must first convert each average into total.

### Mistake 4 — Wrong Combined Count

Always:

$$
n_1+n_2
$$

### Mistake 5 — Ignoring Bounds

Combined average must lie between the group averages.

### Mistake 6 — Wrong Weight

The correct weight depends on the context.

---

# 55. High-Yield Exam Patterns

> [!important] Must Master

1. Two-group combined average
2. Three-group combined average
3. Equal-sized groups
4. Unequal-sized groups
5. Find combined average
6. Find missing group average
7. Find missing group size
8. Find combined total
9. Find remaining group average
10. Add a new group
11. Remove a group
12. Replace a subgroup
13. Combined average of ages
14. Combined average of marks
15. Combined average of salaries
16. Combined average of prices
17. Combined percentage
18. Combined cost
19. Group-size ratio
20. Alligation-based combined average

---

# 56. Formula Sheet

> [!important] Must Remember

### Two Groups

$$
\boxed{
A_c=
\frac{n_1A_1+n_2A_2}
{n_1+n_2}
}
$$

### Three Groups

$$
\boxed{
A_c=
\frac{
n_1A_1+n_2A_2+n_3A_3
}{
n_1+n_2+n_3
}
}
$$

### General

$$
\boxed{
A_c=
\frac{\sum n_iA_i}
{\sum n_i}
}
$$

### Total From Average

$$
\boxed{
Total=nA
}
$$

### Remaining Group

$$
\boxed{
A_r=
\frac{nA-n_1A_1}
{n-n_1}
}
$$

### Group Size Ratio

If:

$$
A_1<A_c<A_2
$$

then:

$$
\boxed{
n_1:n_2=
(A_2-A_c):(A_c-A_1)
}
$$

### Equal Group Sizes

$$
\boxed{
A_c=
\frac{A_1+A_2+\cdots+A_n}{n}
}
$$

---

# 57. Quick Revision

> [!summary] One-Minute Revision

### Main Idea

> **Average → Total → Combine → Divide**

### Step 1

Convert each group into total:

$$
Total=Average\times Number
$$

### Step 2

Add totals:

$$
Combined\ Total=\sum(nA)
$$

### Step 3

Add group sizes:

$$
Combined\ Number=\sum n
$$

### Step 4

Divide:

$$
\boxed{
Combined\ Average=
\frac{\sum(nA)}
{\sum n}
}
$$

---

# 58. Fastest Shortcut

For two groups:

$$
\boxed{
A_c=
\frac{n_1A_1+n_2A_2}
{n_1+n_2}
}
$$

If group sizes are equal:

$$
\boxed{
A_c=\frac{A_1+A_2}{2}
}
$$

If group-size ratio is required:

$$
\boxed{
n_1:n_2=
(A_2-A_c):(A_c-A_1)
}
$$

---

# 59. Exam Recognition Map

```text
COMBINED AVERAGE
│
├── Two Groups
│   ├── Equal Size
│   │   └── Simple Average of Averages
│   │
│   └── Unequal Size
│       └── Weighted Average
│
├── Three or More Groups
│   └── Σ(n × Average) / Σn
│
├── Missing Information
│   ├── Missing Average
│   ├── Missing Group Size
│   └── Missing Total
│
├── Group Changes
│   ├── Add Group
│   ├── Remove Group
│   └── Replace Group
│
└── Shortcut
    └── Alligation / Deviation
```

> [!success]
> **Core skill:** Whenever two or more groups are combined, immediately think:
>
> **`Group Average × Group Size = Group Total`**
>
> Then combine the totals and divide by the combined size.