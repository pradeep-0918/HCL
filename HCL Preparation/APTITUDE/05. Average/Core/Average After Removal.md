---
type: concept
subject: aptitude
topic: "Average After Removal"
parent: "05. Average"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - average
  - average-after-removal
  - quantitative-aptitude
wikilinks:
  - "[[05. Average]]"
  - "[[Average of Numbers]]"
  - "[[Average After Addition]]"
  - "[[Average After Replacement]]"
  - "[[Combined Average]]"
---

# Average After Removal

## 1. Core Concept

> [!summary]
> When one or more values are removed from a group, both the **total** and the **number of observations** decrease.

The safest method is:

> **Old Average → Old Total → Remove Total → New Count → New Average**

---

# 2. Golden Formula — One Value Removed

If:

- Original number of values = `n`
- Original average = `A`
- Removed value = `x`

Original total:

$$
nA
$$

New total:

$$
nA-x
$$

New count:

$$
n-1
$$

Therefore:

$$
\boxed{
New\ Average=
\frac{nA-x}{n-1}
}
$$

---

# 3. Basic Example

The average of 5 numbers is `20`.

One number `30` is removed.

### Old total

$$
5(20)=100
$$

### New total

$$
100-30=70
$$

### New count

$$
5-1=4
$$

### New average

$$
\frac{70}{4}
=
\boxed{17.5}
$$

---

# 4. Most Important Insight

> [!important]
> Compare the removed value with the old average.

### If:

$$
x>A
$$

removing `x` causes the average to **decrease**.

### If:

$$
x<A
$$

removing `x` causes the average to **increase**.

### If:

$$
x=A
$$

the average **remains unchanged**.

---

# 5. Example — Average Decreases

Average of 10 numbers = `25`.

Remove `35`.

Since:

$$
35>25
$$

the average must decrease.

Old total:

$$
10(25)=250
$$

New total:

$$
250-35=215
$$

New count:

$$
9
$$

New average:

$$
\boxed{\frac{215}{9}\approx23.89}
$$

---

# 6. Example — Average Increases

Average of 10 numbers = `25`.

Remove `15`.

Since:

$$
15<25
$$

the average must increase.

Old total:

$$
250
$$

New total:

$$
250-15=235
$$

New count:

$$
9
$$

New average:

$$
\boxed{\frac{235}{9}\approx26.11}
$$

---

# 7. Example — Average Remains Same

Average of 10 numbers = `25`.

Remove one value equal to `25`.

Old total:

$$
250
$$

New total:

$$
250-25=225
$$

New count:

$$
9
$$

New average:

$$
\frac{225}{9}
=
\boxed{25}
$$

---

# 8. Shortcut for Change in Average

If one value `x` is removed:

$$
\boxed{
New\ Average-Old\ Average
=
\frac{A-x}{n-1}
}
$$

Therefore:

$$
\boxed{
New\ Average=
A+\frac{A-x}{n-1}
}
$$

This is useful for fast aptitude calculations.

---

# 9. Example — Shortcut

Average of 9 numbers = `40`.

Remove `32`.

Change:

$$
\frac{40-32}{8}
=
1
$$

New average:

$$
40+1
=
\boxed{41}
$$

---

# 10. Example — Shortcut With Decrease

Average of 9 numbers = `40`.

Remove `48`.

Change:

$$
\frac{40-48}{8}
=
-1
$$

New average:

$$
40-1
=
\boxed{39}
$$

---

# 11. Why the Shortcut Works

Original average:

$$
A
$$

Original total:

$$
nA
$$

After removing `x`:

$$
A'=\frac{nA-x}{n-1}
$$

Change:

$$
A'-A
=
\frac{nA-x}{n-1}-A
$$

$$
=
\frac{nA-x-A(n-1)}
{n-1}
$$

$$
=
\frac{A-x}{n-1}
$$

Therefore:

$$
\boxed{
Change=\frac{A-x}{n-1}
}
$$

---

# 12. Finding the Removed Number

Average of `10` numbers is `20`.

After removing one number, average becomes `18`.

Original total:

$$
10(20)=200
$$

New total:

$$
9(18)=162
$$

Removed number:

$$
200-162
=
\boxed{38}
$$

---

# 13. Shortcut for Finding Removed Number

If:

- Original count = `n`
- Original average = `A`
- New average = `B`

then:

$$
\boxed{
Removed\ Number=nA-(n-1)B
}
$$

---

# 14. Example

Average of 8 numbers = `25`.

After removing one number, average becomes `22`.

Removed number:

$$
8(25)-7(22)
$$

$$
=200-154
$$

$$
\boxed{46}
$$

---

# 15. Finding Original Count

Original average = `20`.

After removing `35`, average becomes `18`.

Let original count be `n`.

$$
18=
\frac{20n-35}{n-1}
$$

Therefore:

$$
18n-18=20n-35
$$

$$
17=2n
$$

$$
\boxed{n=8.5}
$$

Since the number of observations must be an integer, these given values do not produce a valid integer-sized group.

> [!warning]
> In aptitude questions, if the calculated count is not a positive integer, recheck the equation and given data.

---

# 16. Valid Example — Finding Original Count

Original average = `30`.

After removing `50`, average becomes `28`.

Let original count be `n`.

$$
28=
\frac{30n-50}{n-1}
$$

$$
28n-28=30n-50
$$

$$
22=2n
$$

$$
\boxed{n=11}
$$

---

# 17. Formula for Original Count

If:

- Original average = `A`
- New average = `B`
- Removed value = `x`

then:

$$
B=
\frac{nA-x}{n-1}
$$

Solving:

$$
Bn-B=nA-x
$$

$$
n(A-B)=x-B
$$

Therefore:

$$
\boxed{
n=
\frac{x-B}{A-B}
}
$$

---

# 18. Removing Multiple Values

Suppose:

- Original count = `n`
- Original average = `A`
- `m` values are removed
- Sum of removed values = `S`

Original total:

$$
nA
$$

New total:

$$
nA-S
$$

New count:

$$
n-m
$$

Therefore:

$$
\boxed{
New\ Average=
\frac{nA-S}{n-m}
}
$$

---

# 19. Example — Multiple Values

Average of 10 numbers = `20`.

Three numbers with sum `45` are removed.

Original total:

$$
10(20)=200
$$

New total:

$$
200-45=155
$$

New count:

$$
10-3=7
$$

New average:

$$
\boxed{\frac{155}{7}\approx22.14}
$$

---

# 20. Removing a Group With Known Average

A class has 30 students with average marks `60`.

10 students with average marks `50` leave.

Original total:

$$
30(60)=1800
$$

Removed total:

$$
10(50)=500
$$

Remaining total:

$$
1800-500=1300
$$

Remaining students:

$$
20
$$

New average:

$$
\boxed{65}
$$

---

# 21. Multiple-Removal Formula

If:

- Original group → `n`, average `A`
- Removed group → `m`, average `B`

then:

$$
\boxed{
Remaining\ Average=
\frac{nA-mB}
{n-m}
}
$$

---

# 22. Example

50 employees have average salary ₹40,000.

10 employees with average salary ₹30,000 leave.

Remaining average:

$$
\frac{50(40000)-10(30000)}
{40}
$$

$$
=
\frac{2000000-300000}{40}
$$

$$
\boxed{₹42,500}
$$

Because the removed group had a lower average salary.

---

# 23. Important Insight — Removing a Lower Average

If the removed group's average is:

$$
B<A
$$

then:

$$
\boxed{
Remaining\ Average>A
}
$$

The average increases.

---

# 24. Important Insight — Removing a Higher Average

If:

$$
B>A
$$

then:

$$
\boxed{
Remaining\ Average<A
}
$$

The average decreases.

---

# 25. Removing a Group With the Same Average

If:

$$
B=A
$$

then:

$$
\boxed{
Remaining\ Average=A
}
$$

Example:

50 students average 60.

Remove 10 students whose average is also 60.

Remaining average:

$$
\boxed{60}
$$

---

# 26. Bounds After Removing One Value

If the removed value is greater than the old average:

$$
x>A
$$

then:

$$
\boxed{
New\ Average<A
}
$$

But the new average will generally remain within the range of the remaining observations.

---

# 27. Finding Removed Group Average

Original:

- 50 students
- average = 60

Remaining:

- 40 students
- average = 62.5

Find average of removed 10 students.

Original total:

$$
50(60)=3000
$$

Remaining total:

$$
40(62.5)=2500
$$

Removed total:

$$
3000-2500=500
$$

Removed average:

$$
500/10
=
\boxed{50}
$$

---

# 28. Formula for Removed Group Average

If:

- Original count = `n`
- Original average = `A`
- Remaining count = `r`
- Remaining average = `R`
- Removed count = `m`

then:

$$
\boxed{
Removed\ Average=
\frac{nA-rR}{m}
}
$$

where:

$$
m=n-r
$$

---

# 29. Finding Number Removed

Original:

- 50 students
- average = 60

Removed students:

- average = 50

Remaining average = 65.

Let number removed = `x`.

$$
\frac{50(60)-50x}{50-x}=65
$$

$$
3000-50x=3250-65x
$$

$$
15x=250
$$

$$
\boxed{x=\frac{50}{3}}
$$

This is not an integer, so these values are inconsistent with a whole-number group size.

---

# 30. Valid Example — Finding Number Removed

Original:

- 50 students
- average = 60

Removed students average = 50.

Remaining average = 62.5.

Let removed students = `x`.

$$
\frac{50(60)-50x}
{50-x}
=
62.5
$$

$$
3000-50x=3125-62.5x
$$

$$
12.5x=125
$$

$$
\boxed{x=10}
$$

---

# 31. Removal and Alligation

If:

- Original average = `A`
- Removed group average = `B`
- Remaining average = `R`

then the group sizes can often be found using weighted-average/alligation relationships.

Remember:

> Original group = Remaining group + Removed group.

---

# 32. Example

Original average = `60`.

Removed group average = `40`.

Remaining average = `65`.

Find:

$$
Remaining:Removed
$$

Using alligation:

$$
Remaining:Removed
=
(60-40):(65-60)
$$

$$
=20:5
$$

$$
\boxed{4:1}
$$

---

# 33. Removal as Reverse Addition

> [!important]
> **Removal problems are the reverse of addition problems.**

### Addition

$$
New\ Total=Old\ Total+Added\ Total
$$

### Removal

$$
New\ Total=Old\ Total-Removed\ Total
$$

This makes the two topics easy to connect.

---

# 34. Addition vs Removal

| Situation | Total | Count |
|---|---|---|
| Add one value | `+x` | `+1` |
| Remove one value | `-x` | `-1` |
| Add `m` values | `+S` | `+m` |
| Remove `m` values | `-S` | `-m` |

---

# 35. Average Change Comparison

### Addition

$$
\boxed{
Change=
\frac{x-A}{n+1}
}
$$

### Removal

$$
\boxed{
Change=
\frac{A-x}{n-1}
}
$$

Notice the signs are reversed.

---

# 36. Example — Addition vs Removal

Average = `50`.

Count = `10`.

### Add 60

Change:

$$
\frac{60-50}{11}
=
\boxed{\frac{10}{11}}
$$

### Remove 60

Change:

$$
\frac{50-60}{9}
=
\boxed{-\frac{10}{9}}
$$

Removing the high value causes a larger average decrease because the new denominator is smaller.

---

# 37. Average After Removing the Average

If the removed value equals the original average:

$$
x=A
$$

then:

$$
\boxed{
New\ Average=A
}
$$

This is a very common shortcut.

---

# 38. Example

Average of 20 numbers = `35`.

One number equal to `35` is removed.

New average:

$$
\boxed{35}
$$

No calculation is needed.

---

# 39. Removing Multiple Values With Same Average

Suppose:

- 50 values
- average = 40

10 values are removed, and their average is also 40.

Then:

$$
\boxed{
Remaining\ Average=40
}
$$

---

# 40. Removing Extreme Values

Removing an unusually large value generally lowers the average.

Example:

$$
10,20,30,40,100
$$

Average:

$$
40
$$

Remove `100`.

Remaining:

$$
10,20,30,40
$$

Average:

$$
25
$$

So:

$$
\boxed{40\rightarrow25}
$$

---

# 41. Removing a Small Value

Numbers:

$$
10,20,30,40,50
$$

Average:

$$
30
$$

Remove `10`.

Remaining average:

$$
\frac{20+30+40+50}{4}
=
\boxed{35}
$$

Removing a low value raises the average.

---

# 42. Removing Two Values

Average of 8 numbers = `30`.

Two values `20` and `10` are removed.

Original total:

$$
8(30)=240
$$

Removed total:

$$
20+10=30
$$

Remaining total:

$$
210
$$

Remaining count:

$$
6
$$

New average:

$$
\boxed{35}
$$

---

# 43. Removing Values With Known Average

Average of 12 numbers = `25`.

Four numbers with average `15` are removed.

Original total:

$$
12(25)=300
$$

Removed total:

$$
4(15)=60
$$

Remaining total:

$$
240
$$

Remaining count:

$$
8
$$

New average:

$$
\boxed{30}
$$

---

# 44. Finding Removed Value From Average Increase

Average of 10 numbers = `30`.

After removing one number, average becomes `32`.

Removed number:

$$
10(30)-9(32)
$$

$$
=300-288
$$

$$
\boxed{12}
$$

Since `12 < 30`, removing it increases the average.

---

# 45. Finding Removed Value From Average Decrease

Average of 10 numbers = `30`.

After removing one number, average becomes `28`.

Removed value:

$$
10(30)-9(28)
$$

$$
=300-252
$$

$$
\boxed{48}
$$

Since `48 > 30`, removing it decreases the average.

---

# 46. Finding Original Average

After removing one value `20` from 10 numbers, the new average is `30`.

Original average = `A`.

Original total:

$$
10A
$$

Remaining total:

$$
9(30)=270
$$

Therefore:

$$
10A-20=270
$$

$$
10A=290
$$

$$
\boxed{A=29}
$$

---

# 47. Finding Original Average Formula

If:

- Original count = `n`
- Removed value = `x`
- New average = `B`

then:

$$
nA-x=(n-1)B
$$

Therefore:

$$
\boxed{
A=
\frac{(n-1)B+x}{n}
}
$$

---

# 48. Example

12 students remain after one student leaves.

Remaining average = `70`.

The student who left scored `50`.

Original number:

$$
13
$$

Original total:

$$
12(70)+50
$$

$$
=840+50
$$

$$
=890
$$

Original average:

$$
890/13
$$

$$
\boxed{68.46}
$$

---

# 49. Removal of a Group — Total Method

Whenever a group leaves:

### Step 1

Find original total.

$$
nA
$$

### Step 2

Find removed total.

$$
mB
$$

### Step 3

Subtract.

$$
nA-mB
$$

### Step 4

Find remaining count.

$$
n-m
$$

### Step 5

Divide.

$$
\boxed{
Remaining\ Average=
\frac{nA-mB}{n-m}
}
$$

---

# 50. Average After Removal of Employees

A company has 100 employees with average salary ₹50,000.

20 employees with average salary ₹40,000 leave.

Remaining average:

$$
\frac{100(50000)-20(40000)}
{80}
$$

$$
=\frac{5,000,000-800,000}
{80}
$$

$$
\boxed{₹52,500}
$$

---

# 51. Average After Removal of Students

A class has 40 students with average marks 70.

10 students with average marks 60 leave.

Remaining:

$$
\frac{40(70)-10(60)}
{30}
$$

$$
=\frac{2800-600}{30}
$$

$$
\boxed{73.33}
$$

---

# 52. Average After Removal of Customers

50 customers have average spending ₹1,000.

10 customers with average spending ₹700 leave.

Remaining average:

$$
\frac{50(1000)-10(700)}
{40}
$$

$$
=\frac{43000}{40}
$$

$$
\boxed{₹1,075}
$$

---

# 53. Average After Removal of Products

A warehouse has 100 products with average cost ₹500.

20 products with average cost ₹300 are removed.

Remaining average:

$$
\frac{100(500)-20(300)}
{80}
$$

$$
=\frac{44000}{80}
$$

$$
\boxed{₹550}
$$

---

# 54. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting to Reduce the Count

After removing one value:

$$
n\rightarrow n-1
$$

### Mistake 2 — Subtracting From Average Directly

Wrong:

$$
A-x
$$

Correct:

$$
\boxed{
New\ Average=
\frac{nA-x}{n-1}
}
$$

### Mistake 3 — Using `n` Instead of `n-1`

The denominator changes after removal.

### Mistake 4 — Ignoring the Removed Group Average

For multiple removals, you need the removed group's total.

### Mistake 5 — Not Checking Direction

Removing a value above the average should decrease the average.

Removing a value below the average should increase it.

---

# 55. High-Yield Exam Patterns

> [!important] Must Master

1. Remove one value
2. Find new average
3. Find removed value
4. Find original average
5. Find original count
6. Remove multiple values
7. Remove a group
8. Find remaining average
9. Find removed group average
10. Find number removed
11. Average increase after removal
12. Average decrease after removal
13. Removing value equal to average
14. Removing high value
15. Removing low value
16. Average after students leave
17. Average after employees leave
18. Average after customers leave
19. Alligation-based removal
20. Reverse average problems

---

# 56. Formula Sheet

> [!important] Must Remember

### One Value Removed

$$
\boxed{
A_{new}=
\frac{nA-x}{n-1}
}
$$

### Change in Average

$$
\boxed{
A_{new}-A=
\frac{A-x}{n-1}
}
$$

### Removed Value

$$
\boxed{
x=nA-(n-1)A_{new}
}
$$

### Original Average

$$
\boxed{
A=
\frac{(n-1)A_{new}+x}{n}
}
$$

### Original Count

$$
\boxed{
n=
\frac{x-A_{new}}
{A-A_{new}}
}
$$

### Multiple Values Removed

If removed total = `S`:

$$
\boxed{
A_{new}=
\frac{nA-S}
{n-m}
}
$$

### Group Removed

If removed group has `m` values and average `B`:

$$
\boxed{
A_{remaining}
=
\frac{nA-mB}
{n-m}
}
$$

### Removed Group Average

$$
\boxed{
B=
\frac{nA-(n-m)A_r}
{m}
}
$$

---

# 57. Quick Revision

> [!summary] One-Minute Revision

### Main Method

$$
\boxed{
Old\ Total
\rightarrow
Remove\ Total
\rightarrow
Remaining\ Total
\rightarrow
Remaining\ Count
\rightarrow
New\ Average
}
$$

### One Value

$$
\boxed{
New\ Average=
\frac{nA-x}{n-1}
}
$$

### Removed Value

$$
\boxed{
x=nA-(n-1)A_{new}
}
$$

### Multiple Values

$$
\boxed{
New\ Average=
\frac{nA-mB}
{n-m}
}
$$

### Direction Rule

> Remove a **high** value → average **decreases**.

> Remove a **low** value → average **increases**.

> Remove a value equal to average → average **unchanged**.

### Golden Memory Trick

> **Removal = Addition in Reverse**

For addition:

$$
Total+Added
$$

For removal:

$$
Total-Removed
$$

---

# 58. Exam Recognition Map

```text
AVERAGE AFTER REMOVAL
│
├── One Value Removed
│   ├── Find New Average
│   ├── Find Removed Value
│   ├── Find Original Average
│   └── Find Original Count
│
├── Multiple Values Removed
│   ├── Sum Given
│   └── Average Given
│
├── Group Removed
│   ├── Find Remaining Average
│   ├── Find Removed Average
│   └── Find Number Removed
│
├── Direction
│   ├── Remove High → Average Down
│   ├── Remove Low → Average Up
│   └── Remove Equal → No Change
│
└── Shortcuts
    ├── Total Method
    ├── Average Change
    └── Alligation
```

> [!success]
> **Core skill:** Whenever a value or group is removed, immediately write:
>
> $$\boxed{Old\ Total=Old\ Average\times Old\ Count}$$
>
> Then subtract the removed total and divide by the remaining count.
