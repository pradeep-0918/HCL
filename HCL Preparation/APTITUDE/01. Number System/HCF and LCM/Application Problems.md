---
type: concept
subject: aptitude
topic: "HCF and LCM Application Problems"
parent: "01. Number System/HCF and LCM"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - hcf
  - lcm
  - application-problems
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[HCF and LCM]]"
  - "[[HCF]]"
  - "[[LCM]]"
  - "[[HCF-LCM Relationship]]"
  - "[[HCF and LCM of Fractions]]"
  - "[[Remainders]]"
  - "[[Factors]]"
  - "[[Multiples]]"
---

# HCF and LCM Application Problems

## 1. Core Concept

> [!summary] How to Recognize the Question
> HCF and LCM application problems are usually **word problems** where the mathematical operation is hidden inside the wording.

The most important skill is:

$$
\boxed{
\text{Understand the situation}
\rightarrow
\text{Identify HCF or LCM}
\rightarrow
\text{Apply the formula}
}
$$

---

# 2. HCF vs LCM — First Decision

| Question wording | Usually use |
|---|---|
| Greatest possible size | HCF |
| Largest possible length | HCF |
| Maximum number of equal groups | HCF |
| Greatest measure | HCF |
| Largest number that divides | HCF |
| Same remainder, greatest divisor | HCF of differences |
| Smallest number divisible by all | LCM |
| Least common multiple | LCM |
| When will events happen together? | LCM |
| When will cycles repeat together? | LCM |
| Bells ring together | LCM |
| Traffic lights synchronize | LCM |
| Smallest number leaving same remainder | LCM + remainder |

> [!important] Golden Recognition
>
> **HCF → "largest/greatest possible common division"**
>
> **LCM → "smallest/least possible common occurrence"**

---

# 3. Application Type 1 — Greatest Possible Size

This is one of the most common HCF patterns.

### Example

A rectangular sheet is:

$$
48\text{ cm}\times60\text{ cm}
$$

It must be divided into the **largest possible equal squares**.

What is the side of each square?

### Step 1 — Identify

Largest equal square means:

$$
\boxed{HCF}
$$

### Step 2 — Calculate

$$
HCF(48,60)=12
$$

Therefore:

$$
\boxed{12\text{ cm}}
$$

---

# 4. Why HCF?

The square side must divide both:

$$
48
$$

and:

$$
60
$$

We need the **largest** such number.

Therefore:

$$
\boxed{\text{HCF}}
$$

---

# 5. Application Type 2 — Greatest Length

> Find the greatest length that can exactly measure rods of lengths `24 m`, `36 m`, and `60 m`.

The word **greatest** and the requirement that it divides all lengths indicate HCF.

$$
HCF(24,36,60)
$$

First:

$$
HCF(24,36)=12
$$

Then:

$$
HCF(12,60)=12
$$

Therefore:

$$
\boxed{12\text{ m}}
$$

---

# 6. Recognition Pattern — Greatest Measure

Whenever you see:

- greatest length
- greatest size
- largest possible piece
- maximum equal size
- longest measuring unit

think:

$$
\boxed{HCF}
$$

---

# 7. Application Type 3 — Maximum Equal Groups

Suppose there are:

- `48` boys
- `60` girls

They must be divided into the **maximum number of identical groups**.

The number of groups must divide both:

$$
48
$$

and:

$$
60
$$

Therefore:

$$
\boxed{
\text{Number of groups}=HCF(48,60)
}
$$

$$
=12
$$

Therefore:

$$
\boxed{12\text{ groups}}
$$

---

# 8. Finding Members in Each Group

If there are `12` groups:

Boys per group:

$$
48\div12=4
$$

Girls per group:

$$
60\div12=5
$$

Therefore each group contains:

$$
\boxed{4\text{ boys and }5\text{ girls}}
$$

> [!tip] Important
> HCF gives the **number of maximum equal groups**.
>
> Divide the original quantities by the HCF to find the contents of each group.

---

# 9. Application Type 4 — Identical Packages

Suppose a shop has:

- `72` apples
- `108` oranges

The shop wants to make the **maximum number of identical fruit packages**.

Number of packages:

$$
HCF(72,108)
$$

Prime factorization:

$$
72=2^3\times3^2
$$

$$
108=2^2\times3^3
$$

HCF:

$$
2^2\times3^2
$$

$$
=36
$$

Therefore:

$$
\boxed{36\text{ packages}}
$$

Each package contains:

$$
72/36=2
$$

apples and:

$$
108/36=3
$$

oranges.

---

# 10. Application Type 5 — Cutting Objects

Suppose rods have lengths:

$$
18,\ 24,\ 30\text{ cm}
$$

You want to cut them into pieces of the **largest possible equal length**, with no material wasted.

Use:

$$
HCF(18,24,30)
$$

$$
HCF(18,24)=6
$$

$$
HCF(6,30)=6
$$

Therefore:

$$
\boxed{6\text{ cm}}
$$

---

# 11. Number of Pieces

If the piece length is `6 cm`:

From `18 cm`:

$$
18/6=3
$$

From `24 cm`:

$$
24/6=4
$$

From `30 cm`:

$$
30/6=5
$$

Total pieces:

$$
3+4+5
$$

$$
\boxed{12}
$$

> [!important] Pattern
> **HCF finds the largest possible piece size.**
>
> Then:
>
> $$\text{Number of pieces}=\frac{\text{length}}{\text{piece size}}$$

---

# 12. Application Type 6 — Bells

Now we switch to LCM.

Suppose three bells ring every:

- `6 minutes`
- `8 minutes`
- `12 minutes`

When will they ring together again?

The events repeat periodically.

Therefore:

$$
\boxed{LCM}
$$

Calculate:

$$
LCM(6,8,12)=24
$$

Therefore:

$$
\boxed{24\text{ minutes}}
$$

---

# 13. Why LCM?

We need the **smallest positive time** that is simultaneously a multiple of:

$$
6,\ 8,\ 12
$$

Therefore:

$$
\boxed{LCM}
$$

---

# 14. Application Type 7 — Bells Starting Together

Suppose three bells ring at `8:00 AM`.

They ring every:

- `12 minutes`
- `18 minutes`
- `30 minutes`

When will they ring together again?

Calculate:

$$
LCM(12,18,30)
$$

Prime factorization:

$$
12=2^2\times3
$$

$$
18=2\times3^2
$$

$$
30=2\times3\times5
$$

Therefore:

$$
LCM=2^2\times3^2\times5
$$

$$
=180\text{ minutes}
$$

Convert:

$$
180\text{ minutes}=3\text{ hours}
$$

Therefore:

$$
\boxed{11:00\text{ AM}}
$$

---

# 15. Important Time Conversion

Always convert the LCM result into the required unit.

### Useful conversions

$$
60\text{ seconds}=1\text{ minute}
$$

$$
60\text{ minutes}=1\text{ hour}
$$

$$
24\text{ hours}=1\text{ day}
$$

> [!warning] Common Trap
> Do not give `180 minutes` when the question asks for the time of day. Convert it to `3 hours`.

---

# 16. Application Type 8 — Traffic Lights

Three traffic lights change every:

$$
20,\ 30,\ 45\text{ seconds}
$$

When will they change together again?

Use:

$$
LCM(20,30,45)
$$

Prime factorization:

$$
20=2^2\times5
$$

$$
30=2\times3\times5
$$

$$
45=3^2\times5
$$

Therefore:

$$
LCM=2^2\times3^2\times5
$$

$$
=180
$$

Therefore:

$$
\boxed{180\text{ seconds}}
$$

or:

$$
\boxed{3\text{ minutes}}
$$

---

# 17. Application Type 9 — Machines

Machine A completes a cycle every:

$$
12\text{ minutes}
$$

Machine B completes a cycle every:

$$
18\text{ minutes}
$$

Machine C completes a cycle every:

$$
30\text{ minutes}
$$

If all start together, when will they complete a cycle together again?

Use:

$$
LCM(12,18,30)
$$

$$
=180
$$

Therefore:

$$
\boxed{180\text{ minutes}}
$$

---

# 18. Application Type 10 — Buses

Three buses leave a station every:

- `15 minutes`
- `20 minutes`
- `30 minutes`

If they leave together now, when will they next leave together?

$$
LCM(15,20,30)
$$

Prime factorization:

$$
15=3\times5
$$

$$
20=2^2\times5
$$

$$
30=2\times3\times5
$$

Therefore:

$$
LCM=2^2\times3\times5
$$

$$
\boxed{60\text{ minutes}}
$$

So they meet again after:

$$
\boxed{1\text{ hour}}
$$

---

# 19. Application Type 11 — Smallest Number Divisible by Several Numbers

> Find the smallest number divisible by `8`, `12`, and `18`.

The keyword is:

**smallest number divisible by all**

Therefore:

$$
\boxed{LCM}
$$

Calculate:

$$
LCM(8,12,18)
$$

$$
=72
$$

Therefore:

$$
\boxed{72}
$$

---

# 20. Application Type 12 — Smallest Number Leaving Same Remainder

> Find the smallest number which leaves remainder `3` when divided by `4`, `6`, and `8`.

Since the remainder is the same:

$$
N-3
$$

must be divisible by:

$$
4,\ 6,\ 8
$$

Therefore:

$$
N-3=LCM(4,6,8)
$$

Calculate:

$$
LCM(4,6,8)=24
$$

Therefore:

$$
N=24+3
$$

$$
\boxed{27}
$$

---

# 21. General Formula — Same Remainder

If a number must leave the same remainder `r` when divided by:

$$
a,b,c
$$

then:

$$
N-r
$$

must be a common multiple.

Therefore the smallest candidate is:

$$
\boxed{
N=LCM(a,b,c)+r
}
$$

provided the remainder is valid for each divisor.

---

# 22. Application Type 13 — Greatest Number Leaving Same Remainder

This is an HCF pattern.

Suppose:

> Find the greatest number that divides `43`, `67`, and `91`, leaving the same remainder.

Take differences:

$$
67-43=24
$$

$$
91-67=24
$$

Then:

$$
HCF(24,24)=24
$$

Therefore:

$$
\boxed{24}
$$

---

# 23. General Formula — Same Remainder

For numbers:

$$
a,b,c
$$

the greatest divisor leaving the same remainder is:

$$
\boxed{
HCF(a-b,b-c)
}
$$

You can also use all pairwise differences:

$$
\boxed{
HCF(|a-b|,|b-c|,|c-a|)
}
$$

---

# 24. Application Type 14 — Ratio + HCF

Two numbers are in the ratio:

$$
3:5
$$

and their HCF is:

$$
12
$$

Find the numbers.

Since:

$$
HCF(3,5)=1
$$

multiply both terms by `12`:

$$
3\times12=36
$$

$$
5\times12=60
$$

Therefore:

$$
\boxed{36,\ 60}
$$

---

# 25. General Formula — Ratio + HCF

If two numbers are in ratio:

$$
m:n
$$

and:

$$
HCF(m,n)=1
$$

with HCF `H`, then:

$$
\boxed{
a=Hm,\quad b=Hn
}
$$

---

# 26. Application Type 15 — Ratio + LCM

Two numbers are in the ratio:

$$
3:5
$$

and their LCM is:

$$
60
$$

Find the numbers.

Let the numbers be:

$$
3x,\ 5x
$$

Since `3` and `5` are coprime:

$$
LCM=15x
$$

Therefore:

$$
15x=60
$$

$$
x=4
$$

Numbers:

$$
3(4)=12
$$

$$
5(4)=20
$$

Therefore:

$$
\boxed{12,\ 20}
$$

---

# 27. General Formula — Ratio + LCM

If:

$$
a:b=m:n
$$

and:

$$
HCF(m,n)=1
$$

then:

$$
LCM=Hmn
$$

Therefore:

$$
\boxed{
H=\frac{LCM}{mn}
}
$$

Then:

$$
\boxed{
a=Hm,\quad b=Hn
}
$$

---

# 28. Application Type 16 — HCF and LCM Given

Suppose two numbers have:

$$
HCF=6
$$

and:

$$
LCM=180
$$

One number is:

$$
30
$$

Find the other.

Use:

$$
HCF\times LCM=a\times b
$$

Therefore:

$$
6\times180=30b
$$

$$
1080=30b
$$

$$
b=36
$$

Therefore:

$$
\boxed{36}
$$

---

# 29. Application Type 17 — Greatest Number Dividing Several Numbers

Suppose you need the greatest number that divides:

$$
84,\ 126,\ 210
$$

The wording says:

**greatest number that divides all**

Therefore:

$$
\boxed{HCF}
$$

Calculate:

$$
HCF(84,126,210)
$$

$$
=42
$$

Therefore:

$$
\boxed{42}
$$

---

# 30. Application Type 18 — Largest Equal Pieces

Lengths are:

$$
72,\ 108,\ 180\text{ cm}
$$

Find the largest possible equal piece length.

Use:

$$
HCF(72,108,180)
$$

$$
=36
$$

Therefore:

$$
\boxed{36\text{ cm}}
$$

Number of pieces:

$$
72/36=2
$$

$$
108/36=3
$$

$$
180/36=5
$$

Total:

$$
\boxed{10\text{ pieces}}
$$

---

# 31. Application Type 19 — Maximum Number of Identical Groups

Suppose there are:

- `84` pencils
- `126` pens
- `210` erasers

Find the maximum number of identical sets.

Use:

$$
HCF(84,126,210)
$$

$$
=42
$$

Therefore:

$$
\boxed{42\text{ sets}}
$$

Each set contains:

$$
84/42=2
$$

pencils,

$$
126/42=3
$$

pens,

and:

$$
210/42=5
$$

erasers.

---

# 32. Application Type 20 — Repeating Events With a Starting Time

Three events occur every:

$$
8,\ 12,\ 18\text{ minutes}
$$

They start together at `9:20 AM`.

Find the next time they occur together.

First:

$$
LCM(8,12,18)
$$

$$
=72
$$

So they repeat together after:

$$
72\text{ minutes}
$$

Add to starting time:

$$
9:20+72\text{ minutes}
$$

$$
=10:32\text{ AM}
$$

Therefore:

$$
\boxed{10:32\text{ AM}}
$$

---

# 33. Application Type 21 — Days

Suppose three workers take leave every:

- `6 days`
- `8 days`
- `12 days`

They take leave together today.

When will they next take leave together?

Use:

$$
LCM(6,8,12)=24
$$

Therefore:

$$
\boxed{24\text{ days}}
$$

---

# 34. Application Type 22 — Weeks

Suppose three events repeat every:

- `2 weeks`
- `3 weeks`
- `5 weeks`

They occur together today.

Next common occurrence:

$$
LCM(2,3,5)=30
$$

Therefore:

$$
\boxed{30\text{ weeks}}
$$

---

# 35. Application Type 23 — Circular/Repeating Patterns

If patterns repeat after:

$$
a,\ b,\ c
$$

steps, the entire combined pattern repeats after:

$$
\boxed{LCM(a,b,c)}
$$

This appears in:

- rotating schedules
- repeating lights
- periodic signals
- machine cycles
- event schedules

---

# 36. Application Type 24 — Count Common Occurrences

Suppose two events occur every:

$$
6
$$

and:

$$
8
$$

days.

How many times will they occur together in `100` days?

First:

$$
LCM(6,8)=24
$$

Every common occurrence is a multiple of `24`.

Number of complete occurrences:

$$
\left\lfloor\frac{100}{24}\right\rfloor
$$

$$
\boxed{4}
$$

> [!important] Pattern
>
> **Find LCM first → divide range by LCM.**

---

# 37. Application Type 25 — Number of Common Multiples in a Range

If:

$$
L=LCM(a,b)
$$

then the number of common multiples from `1` to `N` is:

$$
\boxed{
\left\lfloor\frac NL\right\rfloor
}
$$

For a range `[A,B]`:

$$
\boxed{
\left\lfloor\frac BL\right\rfloor
-
\left\lfloor\frac{A-1}{L}\right\rfloor
}
$$

---

# 38. Example — Range Counting

How many numbers from `50` to `200` are divisible by both `6` and `8`?

First:

$$
LCM(6,8)=24
$$

Multiples of `24` in `[50,200]`:

$$
\left\lfloor\frac{200}{24}\right\rfloor
-
\left\lfloor\frac{49}{24}\right\rfloor
$$

$$
=8-2
$$

$$
\boxed{6}
$$

---

# 39. Application Type 26 — Greatest Number That Leaves Different Remainders

Suppose a divisor leaves:

- remainder `2` when dividing `20`
- remainder `3` when dividing `31`

Then:

$$
20-2=18
$$

and:

$$
31-3=28
$$

The divisor must divide both:

$$
18
$$

and:

$$
28
$$

Therefore:

$$
HCF(18,28)=2
$$

But a divisor must be **greater than both remainders** for them to be valid.

Here:

$$
2<3
$$

so the proposed divisor is invalid.

> [!warning] Important
> Always check:
>
> $$\boxed{\text{remainder}<\text{divisor}}
> $$

---

# 40. Application Type 27 — Least Number With Different Remainders

When remainders differ, the simple:

$$
LCM+r
$$

shortcut does not work.

For example:

$$
N\equiv2\pmod5
$$

and:

$$
N\equiv3\pmod7
$$

This requires solving simultaneous congruences.

> [!important] Exam Recognition
>
> **Same remainder → LCM shortcut**
>
> **Different remainders → Congruence/CRT-type problem**

---

# 41. Application Type 28 — HCF of Differences

If:

$$
a,b,c
$$

leave the same remainder when divided by `d`, then:

$$
a\equiv b\equiv c\pmod d
$$

Therefore:

$$
d\mid(a-b)
$$

and:

$$
d\mid(b-c)
$$

Hence:

$$
\boxed{
d=HCF(a-b,b-c)
}
$$

This is one of the most important hidden HCF patterns.

---

# 42. Application Type 29 — HCF in Fractions

If the question asks for the greatest fractional measure that exactly divides:

$$
\frac ab,\frac cd
$$

use:

$$
\boxed{
HCF=
\frac{HCF(a,c)}
{LCM(b,d)}
}
$$

Example:

$$
\frac34,\frac58
$$

Numerator HCF:

$$
HCF(3,5)=1
$$

Denominator LCM:

$$
LCM(4,8)=8
$$

Therefore:

$$
\boxed{\frac18}
$$

---

# 43. Application Type 30 — LCM in Fractions

If the question asks for the least common fractional quantity:

$$
\boxed{
LCM=
\frac{LCM(\text{numerators})}
{HCF(\text{denominators})}
}
$$

Always separate numerator and denominator calculations.

---

# 44. Universal HCF Recognition

> [!important] If You See These Words → Think HCF

- greatest
- largest
- maximum
- highest
- greatest possible size
- largest possible piece
- maximum equal groups
- greatest length
- greatest measure
- largest number that divides
- same remainder + greatest divisor

---

# 45. Universal LCM Recognition

> [!important] If You See These Words → Think LCM

- smallest
- least
- first common occurrence
- happen together again
- repeat together
- synchronize
- smallest number divisible by all
- common multiple
- bells
- buses
- traffic lights
- alarms
- cycles
- same remainder + smallest number

---

# 46. Master Decision Tree

> [!tip] Use This in the Exam

### Step 1

Ask:

**Am I looking for the greatest common division?**

If yes:

$$
\boxed{HCF}
$$

### Step 2

Ask:

**Am I looking for the smallest common occurrence/multiple?**

If yes:

$$
\boxed{LCM}
$$

### Step 3

If there is a remainder:

**Same remainder?**

Then:

- Greatest divisor → HCF of differences
- Smallest number → LCM + remainder

### Step 4

If there is a repeating event:

$$
\boxed{LCM}
$$

### Step 5

If there are equal groups or equal pieces:

$$
\boxed{HCF}
$$

---

# 47. Master Formula Sheet

> [!important] HCF Formulas

### Two Numbers

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### Greatest Equal Size

$$
\boxed{HCF}
$$

### Same Remainder

$$
\boxed{
HCF(\text{differences})
}
$$

### Fraction HCF

$$
\boxed{
\frac{HCF(N)}{LCM(D)}
}
$$

---

> [!important] LCM Formulas

### Two Numbers

$$
\boxed{
LCM=\frac{ab}{HCF}
}
$$

### Repeating Events

$$
\boxed{LCM}
$$

### Smallest Number Divisible by All

$$
\boxed{LCM}
$$

### Same Remainder

$$
\boxed{
N=LCM+r
}
$$

### Fraction LCM

$$
\boxed{
\frac{LCM(N)}{HCF(D)}
}
$$

---

# 48. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using LCM for maximum equal groups.
- ❌ Using HCF for repeating events.
- ❌ Confusing "largest" and "smallest" in word problems.
- ❌ Forgetting to convert time units.
- ❌ Forgetting to add the starting time.
- ❌ Using `LCM + r` when remainders are different.
- ❌ Forgetting to check that remainder < divisor.
- ❌ Using `HCF × LCM = abc` for three numbers.
- ❌ Forgetting to divide quantities by HCF when finding group contents.
- ❌ Forgetting that HCF gives the piece size, not automatically the number of pieces.

---

# 49. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

These application patterns are more important than memorizing isolated formulas because companies often hide HCF/LCM inside word problems.

### Master These First

1. Largest equal pieces
2. Maximum equal groups
3. Greatest measuring length
4. Bells
5. Traffic lights
6. Buses
7. Repeating cycles
8. Smallest divisible number
9. Same remainder
10. Ratio + HCF
11. Ratio + LCM
12. HCF/LCM with fractions
13. Common multiples in a range

---

# 50. Practice Checklist

- [ ] Largest equal square problems
- [ ] Largest equal piece problems
- [ ] Maximum group problems
- [ ] Greatest measure problems
- [ ] Bell problems
- [ ] Traffic-light problems
- [ ] Bus problems
- [ ] Machine-cycle problems
- [ ] Smallest divisible number
- [ ] Same-remainder problems
- [ ] Ratio + HCF
- [ ] Ratio + LCM
- [ ] Fraction HCF/LCM
- [ ] Count common multiples
- [ ] Mixed HCF-LCM word problems

---

# 51. Related Topics

- [[HCF and LCM]]
- [[HCF]]
- [[LCM]]
- [[HCF-LCM Relationship]]
- [[HCF and LCM of Fractions]]
- [[Remainders]]
- [[Factors]]
- [[Multiples]]
- [[Factorization]]
- [[Divisibility Rules]]

---

# 52. Quick Revision

> [!summary] One-Minute Revision

### HCF

$$
\boxed{
\text{Greatest common division}
}
$$

Think:

> **Largest equal piece / group / measure**

### LCM

$$
\boxed{
\text{Smallest common multiple}
}
$$

Think:

> **Next common occurrence / synchronization**

### Same Remainder — Greatest Divisor

$$
\boxed{
HCF(\text{differences})
}
$$

### Same Remainder — Smallest Number

$$
\boxed{
LCM(\text{divisors})+r
}
$$

### Two Numbers

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### Golden Recognition

> **HCF = Divide things as equally as possible with the biggest common size.**
>
> **LCM = Wait until repeating things meet again at the smallest common time.**

### Final Exam Shortcut

$$
\boxed{
\text{GROUP / CUT / MEASURE → HCF}
}
$$

$$
\boxed{
\text{MEET / REPEAT / SYNCHRONIZE → LCM}
}
$$