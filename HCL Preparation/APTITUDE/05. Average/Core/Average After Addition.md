---
type: concept
subject: aptitude
topic: "Average After Addition"
parent: "05. Average"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - average
  - average-after-addition
  - quantitative-aptitude
wikilinks:
  - "[[05. Average]]"
  - "[[Basic Average]]"
  - "[[Average of Numbers]]"
  - "[[Combined Average]]"
  - "[[Average After Removal]]"
  - "[[Average After Replacement]]"
---

# Average After Addition

## 1. Core Concept

> [!summary]
> When one or more new values are added to a group, the **total and the number of observations both change**.

The safest method is:

> **Old Average → Old Total → Add New Total → New Count → New Average**

---

# 2. Golden Formula — One Value Added

If:

- Old number of observations = `n`
- Old average = `A`
- New value = `x`

Old total:

$$
nA
$$

New total:

$$
nA+x
$$

New count:

$$
n+1
$$

Therefore:

$$
\boxed{
New\ Average=
\frac{nA+x}{n+1}
}
$$

---

# 3. Basic Example

Average of 5 numbers is `20`.

A new number `30` is added.

### Old total

$$
5\times20=100
$$

### New total

$$
100+30=130
$$

### New count

$$
5+1=6
$$

### New average

$$
\frac{130}{6}
=
\boxed{21.67}
$$

---

# 4. The Most Important Insight

> [!important]
> Compare the added value with the old average.

### If:

$$
x>A
$$

Average **increases**.

### If:

$$
x<A
$$

Average **decreases**.

### If:

$$
x=A
$$

Average **remains unchanged**.

---

# 5. Example — Average Increases

Average of 10 numbers = `25`.

New number = `35`.

Since:

$$
35>25
$$

the average must increase.

Old total:

$$
10(25)=250
$$

New total:

$$
285
$$

New count:

$$
11
$$

New average:

$$
\boxed{\frac{285}{11}\approx25.91}
$$

---

# 6. Example — Average Decreases

Average of 10 numbers = `25`.

New number = `15`.

Old total:

$$
10(25)=250
$$

New total:

$$
250+15=265
$$

New count:

$$
11
$$

New average:

$$
\boxed{\frac{265}{11}\approx24.09}
$$

---

# 7. Example — Average Remains Same

Average of 10 numbers = `25`.

Add another `25`.

Old total:

$$
250
$$

New total:

$$
250+25=275
$$

New count:

$$
11
$$

New average:

$$
\frac{275}{11}
=
\boxed{25}
$$

---

# 8. Shortcut for Average Increase

Suppose:

- Old average = `A`
- Number of observations = `n`
- Added value = `x`

The increase in average is:

$$
\boxed{
New\ Average-Old\ Average
=
\frac{x-A}{n+1}
}
$$

Therefore:

$$
\boxed{
New\ Average=
A+\frac{x-A}{n+1}
}
$$

This is a very useful shortcut.

---

# 9. Example — Shortcut

Average of 9 numbers = `40`.

Add `50`.

Increase:

$$
\frac{50-40}{10}
=
1
$$

New average:

$$
40+1
=
\boxed{41}
$$

No need to calculate the total.

---

# 10. Example — Shortcut With Decrease

Average of 9 numbers = `40`.

Add `30`.

Change:

$$
\frac{30-40}{10}
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

Old total:

$$
nA
$$

New average:

$$
\frac{nA+x}{n+1}
$$

Subtract old average:

$$
\frac{nA+x}{n+1}-A
$$

$$
=
\frac{nA+x-A(n+1)}{n+1}
$$

$$
=
\frac{x-A}{n+1}
$$

Therefore:

$$
\boxed{
Change=
\frac{x-A}{n+1}
}
$$

---

# 12. Finding the Added Number

Average of `10` numbers is `20`.

After adding one number, average becomes `22`.

Old total:

$$
10(20)=200
$$

New total:

$$
11(22)=242
$$

Added number:

$$
242-200
=
\boxed{42}
$$

---

# 13. Shortcut for Finding Added Number

If:

- Old average = `A`
- New average = `B`
- Old count = `n`

then:

$$
\boxed{
Added\ Number=(n+1)B-nA
}
$$

---

# 14. Example

Average of 8 numbers = `25`.

After adding one number, average becomes `28`.

Added number:

$$
9(28)-8(25)
$$

$$
=252-200
$$

$$
\boxed{52}
$$

---

# 15. Finding Number of Original Observations

Average = `20`.

After adding `40`, average becomes `22`.

Let original count be `n`.

Using:

$$
22=
\frac{20n+40}{n+1}
$$

Therefore:

$$
22n+22=20n+40
$$

$$
2n=18
$$

$$
\boxed{n=9}
$$

---

# 16. Formula for Original Count

If:

- Old average = `A`
- New average = `B`
- Added value = `x`

then:

$$
B=
\frac{nA+x}{n+1}
$$

Solving for `n`:

$$
Bn+B=nA+x
$$

$$
n(B-A)=x-B
$$

Therefore:

$$
\boxed{
n=\frac{x-B}{B-A}
}
$$

---

# 17. Example

Old average = `30`.

New value = `50`.

New average = `32`.

Then:

$$
n=
\frac{50-32}{32-30}
$$

$$
=\frac{18}{2}
$$

$$
\boxed{9}
$$

---

# 18. Adding Multiple Values

Suppose:

- Old count = `n`
- Old average = `A`
- `m` new values are added
- Sum of new values = `S`

Then:

Old total:

$$
nA
$$

New total:

$$
nA+S
$$

New count:

$$
n+m
$$

Therefore:

$$
\boxed{
New\ Average=
\frac{nA+S}{n+m}
}
$$

---

# 19. Example — Multiple Values

Average of 10 numbers = `20`.

Three new numbers with sum `90` are added.

Old total:

$$
10(20)=200
$$

New total:

$$
200+90=290
$$

New count:

$$
13
$$

New average:

$$
\boxed{\frac{290}{13}\approx22.31}
$$

---

# 20. Adding Several Numbers With Known Average

Average of 20 students = `60`.

5 new students have average `70`.

First find their total:

$$
5(70)=350
$$

Old total:

$$
20(60)=1200
$$

Combined:

$$
\frac{1200+350}{25}
$$

$$
\boxed{62}
$$

---

# 21. Multiple-Addition Formula

If:

- Old count = `n`
- Old average = `A`
- New group count = `m`
- New group average = `B`

then:

$$
\boxed{
New\ Average=
\frac{nA+mB}{n+m}
}
$$

This is simply a combined-average problem.

---

# 22. Example

A class has 30 students with average marks `60`.

10 new students join with average `80`.

New average:

$$
\frac{30(60)+10(80)}
{40}
$$

$$
=
\frac{1800+800}{40}
$$

$$
\boxed{65}
$$

---

# 23. Finding New Group Average

A group has:

- 30 students
- average = 60

After 10 new students join, the overall average becomes `65`.

Find the average of the new students.

Old total:

$$
30(60)=1800
$$

New total:

$$
40(65)=2600
$$

New students' total:

$$
2600-1800=800
$$

Their average:

$$
800/10
=
\boxed{80}
$$

---

# 24. Finding Number of New Values

Old group:

- 20 students
- average = 50

New students have average = 70.

Combined average = 60.

Let new students = `x`.

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

# 25. Adding a Value Equal to the Average

If:

$$
New\ Value=Old\ Average
$$

then:

$$
\boxed{New\ Average=Old\ Average}
$$

Example:

Old average = `45`.

Add `45`.

New average:

$$
\boxed{45}
$$

---

# 26. Adding a Value Greater Than Average

If:

$$
x>A
$$

then:

$$
\boxed{New\ Average>A}
$$

But:

$$
\boxed{New\ Average<x}
$$

So the new average lies between the old average and the added value.

Example:

Old average = 20.

Added value = 50.

New average must satisfy:

$$
\boxed{20<New\ Average<50}
$$

---

# 27. Adding a Value Less Than Average

If:

$$
x<A
$$

then:

$$
\boxed{x<New\ Average<A}
$$

Example:

Old average = 50.

Added value = 20.

New average lies between:

$$
\boxed{20\text{ and }50}
$$

---

# 28. Important Bound

When one value is added:

> [!important]
> The new average always lies between the old average and the added value.

Unless the added value is exactly equal to the old average, in which case the average remains unchanged.

---

# 29. Average Increase Given

Average of 15 numbers is `40`.

After adding one number, average increases by `2`.

New average:

$$
42
$$

Added number:

$$
(15+1)(42)-15(40)
$$

$$
=672-600
$$

$$
\boxed{72}
$$

---

# 30. Direct Formula From Average Increase

If the average increases by `d` after adding one value:

$$
New\ Average=A+d
$$

Added value:

$$
(n+1)(A+d)-nA
$$

Simplifying:

$$
\boxed{
Added\ Value=A+(n+1)d
}
$$

---

# 31. Example

Average of 20 numbers = `30`.

After adding one number, average increases by `2`.

Added number:

$$
30+(21)(2)
$$

$$
=30+42
$$

$$
\boxed{72}
$$

---

# 32. Average Decrease Given

Average of 10 numbers = `50`.

After adding one number, average decreases by `3`.

New average:

$$
47
$$

Added value:

$$
11(47)-10(50)
$$

$$
=517-500
$$

$$
\boxed{17}
$$

---

# 33. Direct Formula for Average Decrease

If average decreases by `d`:

$$
\boxed{
Added\ Value=A-(n+1)d
}
$$

Example:

Average = `50`.

`n=10`.

Decrease = `3`.

$$
50-11(3)
=
\boxed{17}
$$

---

# 34. Adding a Group — Change in Average

Old group:

- `n` observations
- average `A`

New group:

- `m` observations
- average `B`

The change in combined average is:

$$
\boxed{
A_c-A=
\frac{m(B-A)}{n+m}
}
$$

This tells us how much the new group pulls the average.

---

# 35. Example

20 students average `50`.

10 new students average `70`.

Change:

$$
\frac{10(70-50)}{30}
$$

$$
=\frac{200}{30}
$$

$$
\boxed{6.67}
$$

New average:

$$
50+6.67
=
\boxed{56.67}
$$

---

# 36. Large Existing Group

If the existing group is very large, adding a small group has a smaller effect.

Example:

1000 employees average salary = ₹30,000.

One new employee earns ₹50,000.

Increase:

$$
\frac{50000-30000}{1001}
$$

$$
\approx₹19.98
$$

New average:

$$
\boxed{₹30,019.98}
$$

---

# 37. Small Existing Group

If the existing group is small, the same new value has a greater effect.

5 people average `30`.

Add `50`.

Increase:

$$
\frac{50-30}{6}
=
\frac{20}{6}
$$

New average:

$$
\boxed{33.33}
$$

---

# 38. Adding a Group With the Same Average

Existing:

20 people, average 60.

New:

10 people, average 60.

Combined average:

$$
\frac{20(60)+10(60)}
{30}
$$

$$
\boxed{60}
$$

Adding a group with the same average does not change the average.

---

# 39. Adding a Group With Higher Average

Existing:

20 people, average 60.

New:

10 people, average 90.

Combined:

$$
\frac{20(60)+10(90)}
{30}
$$

$$
=\frac{2100}{30}
$$

$$
\boxed{70}
$$

---

# 40. Adding a Group With Lower Average

Existing:

20 people, average 60.

New:

10 people, average 30.

Combined:

$$
\frac{20(60)+10(30)}
{30}
$$

$$
=\frac{1500}{30}
$$

$$
\boxed{50}
$$

---

# 41. Average After Adding Equal Values

If `k` is added to every existing observation and the number of observations does not change:

$$
\boxed{
New\ Average=Old\ Average+k
}
$$

But this is different from **adding a new observation whose value is `k`**.

> [!warning]
> Do not confuse:
>
> **adding `k` to every value**  
> with  
> **adding one new value `k`**.

---

# 42. Example of the Difference

Existing values:

$$
10,\ 20,\ 30
$$

Average:

$$
20
$$

### Add one new value 10

New set:

$$
10,20,30,10
$$

Average:

$$
\boxed{17.5}
$$

### Add 10 to every existing value

New set:

$$
20,30,40
$$

Average:

$$
\boxed{30}
$$

Completely different operations.

---

# 43. Average After Adding Two Known Values

Average of 8 numbers = `25`.

Add `30` and `40`.

Old total:

$$
8(25)=200
$$

New total:

$$
200+30+40=270
$$

New count:

$$
10
$$

New average:

$$
\boxed{27}
$$

---

# 44. Shortcut for Multiple Added Values

If `m` values are added and their average is `B`:

$$
\boxed{
New\ Average=
\frac{nA+mB}{n+m}
}
$$

Example:

10 values average 20.

5 values average 30.

$$
\frac{10(20)+5(30)}
{15}
$$

$$
=\frac{350}{15}
$$

$$
\boxed{23.33}
$$

---

# 45. Finding Added Group Average

Old:

`15` people, average `40`.

New total group:

`20` people, average `50`.

New group size:

$$
20-15=5
$$

Old total:

$$
15(40)=600
$$

Combined total:

$$
20(50)=1000
$$

New group total:

$$
1000-600=400
$$

New group average:

$$
400/5
=
\boxed{80}
$$

---

# 46. Average After Admission

A class has 40 students with average marks 60.

5 students are admitted with average 80.

New average:

$$
\frac{40(60)+5(80)}
{45}
$$

$$
=\frac{2800}{45}
$$

$$
\boxed{62.22}
$$

---

# 47. Average After Joining Employees

A company has 100 employees with average salary ₹40,000.

10 employees join with average salary ₹50,000.

New average:

$$
\frac{100(40000)+10(50000)}
{110}
$$

$$
=\frac{4,500,000}{110}
$$

$$
\boxed{₹40,909.09}
$$

---

# 48. Average After Adding Customers

A store has 50 customers whose average purchase is ₹800.

10 new customers have average purchase ₹1,200.

Combined average purchase:

$$
\frac{50(800)+10(1200)}
{60}
$$

$$
=\frac{52000}{60}
$$

$$
\boxed{₹866.67}
$$

---

# 49. Finding Required Added Value

Average of 10 numbers is `40`.

What number should be added so that the new average becomes `45`?

Old total:

$$
10(40)=400
$$

Required new total:

$$
11(45)=495
$$

Required number:

$$
495-400
=
\boxed{95}
$$

---

# 50. Finding Required Added Group

Average of 20 students = `50`.

How many new students with average `80` should join to make the combined average `60`?

Let number of new students = `x`.

$$
\frac{20(50)+80x}
{20+x}
=
60
$$

$$
1000+80x=1200+60x
$$

$$
20x=200
$$

$$
\boxed{x=10}
$$

---

# 51. Ratio Shortcut for Required New Group

Existing average = `50`.

New group average = `80`.

Desired average = `60`.

Using alligation:

$$
Existing:New
=
(80-60):(60-50)
$$

$$
=20:10
$$

$$
=2:1
$$

Therefore:

> Existing group : New group = `2 : 1`.

If existing group has 20 students:

$$
\boxed{New\ group=10}
$$

---

# 52. Adding a New Group — Alligation Recognition

When you see:

- old group average
- new group average
- desired combined average
- find number/ratio

think:

$$
\boxed{\text{Alligation}}
$$

---

# 53. Average After Addition — Reverse Problem

After adding a number `x`, average becomes `B`.

Old average was `A`.

If old count is `n`:

$$
\boxed{
x=(n+1)B-nA
}
$$

This is the fastest formula for reverse questions.

---

# 54. Example

Average of 15 numbers = `30`.

After adding one number, average = `32`.

Added number:

$$
16(32)-15(30)
$$

$$
=512-450
$$

$$
\boxed{62}
$$

---

# 55. Average Increase Shortcut

If old average is `A` and new average is `B`:

$$
\boxed{
Increase=B-A
}
$$

But the added value is:

$$
\boxed{
x=(n+1)B-nA
}
$$

Do not confuse the average increase with the value added.

---

# 56. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting the New Count

After adding one value:

$$
n\rightarrow n+1
$$

### Mistake 2 — Adding the New Value to the Average

Wrong:

$$
A+x
$$

You must update the total and count.

### Mistake 3 — Using `n` Instead of `n+1`

For one new value:

$$
\boxed{New\ Count=n+1}
$$

### Mistake 4 — Confusing Added Value With Average Increase

If average increases by `2`, the added number is **not necessarily 2 greater** than the old average.

---

# 57. High-Yield Exam Patterns

> [!important] Must Master

1. Add one number
2. Find new average
3. Find added number
4. Find original count
5. Add multiple numbers
6. Add a group
7. Find new group average
8. Find new group size
9. Find required added value
10. Find required number of new observations
11. Average increase
12. Average decrease
13. Adding value equal to average
14. Adding value above average
15. Adding value below average
16. Average after admission
17. Average after joining employees
18. Average after adding students
19. Alligation-based addition
20. Reverse average problems

---

# 58. Formula Sheet

> [!important] Must Remember

### One Value Added

$$
\boxed{
A_{new}=
\frac{nA+x}{n+1}
}
$$

### Change in Average

$$
\boxed{
A_{new}-A=
\frac{x-A}{n+1}
}
$$

### Added Value

$$
\boxed{
x=(n+1)A_{new}-nA
}
$$

### Original Count

$$
\boxed{
n=
\frac{x-A_{new}}
{A_{new}-A}
}
$$

### Multiple Values Added

If new values have total `S`:

$$
\boxed{
A_{new}=
\frac{nA+S}{n+m}
}
$$

### Multiple Values With Average `B`

$$
\boxed{
A_{new}=
\frac{nA+mB}
{n+m}
}
$$

### New Group Average

$$
\boxed{
B=
\frac{(n+m)A_{new}-nA}
{m}
}
$$

### Required Added Value

If target average is `T`:

$$
\boxed{
x=(n+1)T-nA
}
$$

### Required New Group Size

If:

- old count = `n`
- old average = `A`
- new group average = `B`
- target = `T`

then:

$$
\boxed{
m=
\frac{n(T-A)}
{B-T}
}
$$

---

# 59. Quick Revision

> [!summary] One-Minute Revision

### Main Method

$$
\boxed{
Old\ Average
\rightarrow
Old\ Total
\rightarrow
Add
\rightarrow
New\ Total
\rightarrow
New\ Count
\rightarrow
New\ Average
}
$$

### One Value

$$
\boxed{
A_{new}=
\frac{nA+x}{n+1}
}
$$

### Added Value

$$
\boxed{
x=(n+1)A_{new}-nA
}
$$

### Change

$$
\boxed{
Change=
\frac{x-A}{n+1}
}
$$

### Multiple Values

$$
\boxed{
A_{new}=
\frac{nA+mB}
{n+m}
}
$$

### Golden Recognition

> If the problem says **“a new person/student/value is added”**, immediately ask:
>
> **What is the old total? What is the new total? What is the new count?**

---

# 60. Exam Recognition Map

```text
AVERAGE AFTER ADDITION
│
├── One Value Added
│   ├── Find New Average
│   ├── Find Added Value
│   └── Find Original Count
│
├── Multiple Values Added
│   ├── Values Given
│   ├── Sum Given
│   └── Average Given
│
├── New Group Added
│   ├── Find Combined Average
│   ├── Find Group Average
│   └── Find Group Size
│
├── Target Average
│   ├── Required Value
│   └── Required Number of Values
│
└── Shortcuts
    ├── Change in Average
    ├── Weighted Average
    └── Alligation
```

> [!success]
> **Core skill:** When something is added, remember:
>
> **New Total = Old Total + Added Total**
>
> **New Count = Old Count + Added Count**
>
> Then:
>
> $$\boxed{New\ Average=\frac{New\ Total}{New\ Count}}$$
