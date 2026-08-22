---
type: concept
subject: aptitude
topic: "HCF-LCM Relationship"
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
  - hcf-lcm
  - factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[HCF and LCM]]"
  - "[[HCF]]"
  - "[[LCM]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Factorization]]"
  - "[[HCF and LCM of Fractions]]"
  - "[[Application Problems]]"
---

# HCF-LCM Relationship

## 1. Core Concept

> [!summary] Main Relationship
> For two positive integers `a` and `b`, the product of their HCF and LCM is equal to the product of the two numbers.

The most important formula is:

$$
\boxed{
\operatorname{HCF}(a,b)
\times
\operatorname{LCM}(a,b)
=
a\times b
}
$$

This is one of the most important formulas in the **Number System** section.

---

# 2. Main Formula

Let:

$$
H=\operatorname{HCF}(a,b)
$$

and:

$$
L=\operatorname{LCM}(a,b)
$$

Then:

$$
\boxed{H\times L=a\times b}
$$

Therefore:

$$
\boxed{
L=\frac{ab}{H}
}
$$

and:

$$
\boxed{
H=\frac{ab}{L}
}
$$

---

# 3. Basic Example

Find the LCM of `12` and `18`, given their HCF is `6`.

Use:

$$
H\times L=a\times b
$$

Substitute:

$$
6\times L=12\times18
$$

$$
6L=216
$$

Therefore:

$$
L=\frac{216}{6}
$$

$$
\boxed{36}
$$

---

# 4. Find HCF When LCM Is Given

Suppose:

$$
a=24,\quad b=36
$$

and:

$$
LCM=72
$$

Find HCF.

Use:

$$
H\times72=24\times36
$$

$$
H=\frac{24\times36}{72}
$$

$$
H=12
$$

Therefore:

$$
\boxed{HCF=12}
$$

---

# 5. Find a Missing Number

Suppose:

- First number = `18`
- HCF = `6`
- LCM = `72`

Find the second number.

Use:

$$
H\times L=a\times b
$$

Therefore:

$$
6\times72=18\times b
$$

$$
432=18b
$$

$$
b=24
$$

Therefore:

$$
\boxed{24}
$$

---

# 6. Why Does the Formula Work?

Suppose:

$$
a=H\times x
$$

and:

$$
b=H\times y
$$

where:

$$
\operatorname{HCF}(x,y)=1
$$

Then:

$$
a\times b
=
H^2xy
$$

The LCM of `a` and `b` is:

$$
Hxy
$$

Therefore:

$$
H\times L
=
H\times Hxy
$$

$$
=H^2xy
$$

which equals:

$$
a\times b
$$

Hence:

$$
\boxed{HCF\times LCM=Product}
$$

---

# 7. Prime Factorization Proof

Suppose:

$$
a=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

and:

$$
b=p_1^{b_1}p_2^{b_2}\cdots p_k^{b_k}
$$

Then:

### HCF

Take minimum exponents:

$$
H=
\prod p_i^{\min(a_i,b_i)}
$$

### LCM

Take maximum exponents:

$$
L=
\prod p_i^{\max(a_i,b_i)}
$$

For every exponent:

$$
\min(a_i,b_i)+\max(a_i,b_i)
=
a_i+b_i
$$

Therefore:

$$
H\times L
=
\prod p_i^{a_i+b_i}
$$

which is:

$$
a\times b
$$

Hence:

$$
\boxed{H\times L=a\times b}
$$

---

# 8. Example Using Prime Powers

Let:

$$
a=2^3\times3^2
$$

and:

$$
b=2^2\times3\times5
$$

### HCF

Take minimum powers:

$$
H=2^2\times3
$$

$$
H=12
$$

### LCM

Take maximum powers:

$$
L=2^3\times3^2\times5
$$

$$
L=360
$$

Now:

$$
H\times L
=
12\times360
$$

$$
=4320
$$

And:

$$
a\times b
=
72\times60
$$

$$
=4320
$$

Therefore:

$$
\boxed{H\times L=a\times b}
$$

---

# 9. Most Important Exam Pattern

> [!important] Pattern 1

If the question gives:

- Two numbers
- HCF
- asks for LCM

Immediately use:

$$
\boxed{
LCM=\frac{a\times b}{HCF}
}
$$

---

# 10. Pattern — Find HCF

If the question gives:

- Two numbers
- LCM
- asks for HCF

Use:

$$
\boxed{
HCF=\frac{a\times b}{LCM}
}
$$

---

# 11. Pattern — Find Missing Number

If:

$$
a,\ b
$$

have HCF `H` and LCM `L`, then:

$$
\boxed{
b=\frac{H\times L}{a}
}
$$

Similarly:

$$
\boxed{
a=\frac{H\times L}{b}
}
$$

---

# 12. Important Condition

> [!warning] Very Important
> The relationship:
>
> $$HCF\times LCM=a\times b$$
>
> is directly valid for **two positive integers**.

Do not blindly apply the same equation to three or more numbers.

For three numbers, use prime factorization or calculate HCF/LCM appropriately.

---

# 13. Coprime Numbers

If:

$$
HCF(a,b)=1
$$

then:

$$
1\times LCM=a\times b
$$

Therefore:

$$
\boxed{
LCM(a,b)=a\times b
}
$$

### Example

For:

$$
8,\ 15
$$

HCF:

$$
1
$$

Therefore:

$$
LCM=8\times15
$$

$$
\boxed{120}
$$

---

# 14. Equal Numbers

If:

$$
a=b
$$

then:

$$
HCF(a,a)=a
$$

and:

$$
LCM(a,a)=a
$$

Therefore:

$$
a\times a=a\times a
$$

So:

$$
\boxed{HCF=LCM=a}
$$

### Example

For:

$$
12,\ 12
$$

we have:

$$
\boxed{HCF=12}
$$

and:

$$
\boxed{LCM=12}
$$

---

# 15. When One Number Divides Another

If:

$$
a\mid b
$$

then:

$$
HCF(a,b)=a
$$

and:

$$
LCM(a,b)=b
$$

Therefore:

$$
a\times b=a\times b
$$

### Example

For:

$$
6,\ 24
$$

HCF:

$$
6
$$

LCM:

$$
24
$$

Therefore:

$$
\boxed{6\times24=6\times24}
$$

---

# 16. Consecutive Numbers

For:

$$
n,\ n+1
$$

we know:

$$
HCF=1
$$

Therefore:

$$
\boxed{
LCM=n(n+1)
}
$$

### Example

For:

$$
14,\ 15
$$

HCF:

$$
1
$$

LCM:

$$
14\times15
$$

$$
\boxed{210}
$$

---

# 17. HCF and LCM Bounds

For positive integers `a` and `b`:

$$
\boxed{
HCF(a,b)\le a
}
$$

and:

$$
\boxed{
HCF(a,b)\le b
}
$$

Therefore:

$$
\boxed{
HCF(a,b)\le\min(a,b)
}
$$

Similarly:

$$
\boxed{
LCM(a,b)\ge\max(a,b)
}
$$

Therefore:

$$
\boxed{
LCM(a,b)\ge\max(a,b)
}
$$

---

# 18. Important Inequality

For positive integers:

$$
\boxed{
HCF\le\min(a,b)\le\max(a,b)\le LCM
}
$$

This is useful for eliminating impossible answer choices.

### Example

For:

$$
12,\ 18
$$

we have:

$$
6\le12\le18\le36
$$

Correct.

---

# 19. Ratio of Two Numbers

Suppose:

$$
a=Hx
$$

and:

$$
b=Hy
$$

where:

$$
H=HCF(a,b)
$$

and:

$$
HCF(x,y)=1
$$

Then:

$$
\boxed{
a:b=x:y
}
$$

The reduced ratio is obtained by dividing both numbers by their HCF.

### Example

$$
84:126
$$

HCF:

$$
42
$$

Therefore:

$$
84:126
=
2:3
$$

---

# 20. Product of Reduced Numbers

If:

$$
a=Hx
$$

and:

$$
b=Hy
$$

with:

$$
HCF(x,y)=1
$$

then:

$$
LCM(a,b)=Hxy
$$

Therefore:

$$
\boxed{
LCM=H\times x\times y
}
$$

---

# 21. HCF-LCM Using Ratio

Suppose two numbers are in the ratio:

$$
m:n
$$

and their HCF is:

$$
H
$$

If:

$$
HCF(m,n)=1
$$

then the numbers are:

$$
\boxed{Hm,\ Hn}
$$

Their LCM is:

$$
\boxed{Hmn}
$$

### Example

Two numbers are in the ratio:

$$
2:3
$$

and their HCF is `12`.

Since:

$$
HCF(2,3)=1
$$

the numbers are:

$$
24,\ 36
$$

Their LCM:

$$
12\times2\times3
$$

$$
\boxed{72}
$$

---

# 22. Important Pattern — Ratio + HCF

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
\boxed{
a=Hm,\quad b=Hn
}
$$

Therefore:

$$
\boxed{
LCM=Hmn
}
$$

This pattern appears frequently in aptitude questions.

---

# 23. Important Pattern — Ratio + LCM

Suppose:

$$
a:b=m:n
$$

where:

$$
HCF(m,n)=1
$$

and LCM is:

$$
L
$$

Then:

$$
L=Hmn
$$

Therefore:

$$
\boxed{
H=\frac{L}{mn}
}
$$

Then:

$$
\boxed{
a=Hm,\quad b=Hn
}
$$

---

# 24. Example — Ratio + LCM

Two numbers are in the ratio:

$$
3:5
$$

Their LCM is:

$$
60
$$

Find the numbers.

Since:

$$
HCF(3,5)=1
$$

we have:

$$
LCM=H\times3\times5
$$

Therefore:

$$
60=15H
$$

$$
H=4
$$

Numbers:

$$
3\times4=12
$$

and:

$$
5\times4=20
$$

Therefore:

$$
\boxed{12,\ 20}
$$

---

# 25. Example — Ratio + HCF

Two numbers are in the ratio:

$$
4:7
$$

Their HCF is:

$$
6
$$

Find the numbers.

Since:

$$
HCF(4,7)=1
$$

numbers are:

$$
4\times6
$$

and:

$$
7\times6
$$

Therefore:

$$
\boxed{24,\ 42}
$$

Their LCM:

$$
6\times4\times7
$$

$$
\boxed{168}
$$

---

# 26. HCF and LCM as Prime-Power Operations

This is a very important way to remember the relationship.

Suppose:

$$
a=2^5\times3^2
$$

and:

$$
b=2^3\times3^4
$$

Then:

### HCF

Take:

$$
\min(5,3)=3
$$

and:

$$
\min(2,4)=2
$$

Therefore:

$$
\boxed{HCF=2^3\times3^2}
$$

### LCM

Take:

$$
\max(5,3)=5
$$

and:

$$
\max(2,4)=4
$$

Therefore:

$$
\boxed{LCM=2^5\times3^4}
$$

---

# 27. Exponent Identity

For any two exponents `a` and `b`:

$$
\boxed{
\min(a,b)+\max(a,b)=a+b
}
$$

This is the mathematical reason:

$$
\boxed{HCF\times LCM=a\times b}
$$

works.

---

# 28. HCF-LCM Relationship for Three Numbers

For three numbers:

$$
a,b,c
$$

there is no simple universal formula:

$$
HCF\times LCM=abc
$$

Instead, use prime factorization.

### Example

$$
12=2^2\times3
$$

$$
18=2\times3^2
$$

$$
30=2\times3\times5
$$

HCF:

$$
2^1\times3^1
$$

$$
=6
$$

LCM:

$$
2^2\times3^2\times5
$$

$$
=180
$$

Therefore:

$$
HCF\times LCM
=
6\times180
=
1080
$$

while:

$$
12\times18\times30=6480
$$

So:

$$
\boxed{HCF\times LCM\ne abc}
$$

---

# 29. LCM of Three Numbers Using Pairwise LCM

For three numbers:

$$
a,b,c
$$

calculate:

$$
L_1=LCM(a,b)
$$

then:

$$
\boxed{
LCM(a,b,c)=LCM(L_1,c)
}
$$

### Example

Find:

$$
LCM(8,12,18)
$$

First:

$$
LCM(8,12)=24
$$

Then:

$$
LCM(24,18)=72
$$

Therefore:

$$
\boxed{72}
$$

---

# 30. HCF of Three Numbers

Similarly:

$$
\boxed{
HCF(a,b,c)
=
HCF(HCF(a,b),c)
}
$$

### Example

Find:

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
\boxed{12}
$$

---

# 31. Same Remainder Connection

If several numbers leave the same remainder when divided by `d`, then `d` divides their pairwise differences.

Therefore:

$$
\boxed{
d=HCF(\text{differences})
}
$$

### Example

Numbers:

$$
43,\ 67,\ 91
$$

Differences:

$$
24,\ 24
$$

Therefore:

$$
HCF=24
$$

So the greatest divisor producing the same remainder is:

$$
\boxed{24}
$$

---

# 32. LCM + Remainder Connection

If a number leaves the same remainder `r` when divided by:

$$
a,b,c
$$

then:

$$
N-r
$$

is a common multiple of:

$$
a,b,c
$$

The smallest positive candidate is:

$$
\boxed{
N=LCM(a,b,c)+r
}
$$

### Example

Same remainder `3` with divisors:

$$
4,\ 6,\ 8
$$

First:

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

# 33. HCF-LCM Application — Two Numbers From Sum and HCF

Suppose two numbers have:

- HCF = `H`
- Sum = `S`

Write:

$$
a=Hx,\quad b=Hy
$$

where:

$$
HCF(x,y)=1
$$

Then:

$$
H(x+y)=S
$$

Therefore:

$$
\boxed{x+y=\frac SH}
$$

This reduces the problem to finding two coprime numbers with the required sum.

---

# 34. Example — Sum + HCF

Two numbers have HCF `6` and sum `42`.

Write:

$$
a=6x
$$

$$
b=6y
$$

Then:

$$
6(x+y)=42
$$

Therefore:

$$
x+y=7
$$

Possible positive coprime pairs:

$$
(1,6),\ (2,5),\ (3,4)
$$

Therefore possible number pairs include:

$$
(6,36),\ (12,30),\ (18,24)
$$

Each pair has HCF `6`.

> [!important] Insight
> **HCF lets you factor out the common part.**

---

# 35. HCF-LCM Application — Product and HCF

If two numbers have:

$$
HCF=H
$$

and product:

$$
P
$$

then:

$$
H\times L=P
$$

Therefore:

$$
\boxed{
LCM=\frac PH
}
$$

---

# 36. HCF-LCM Application — Product and LCM

If product is `P` and LCM is `L`:

$$
H\times L=P
$$

Therefore:

$$
\boxed{
HCF=\frac PL
}
$$

---

# 37. Important Formula Sheet

> [!important] Must Remember

### Main Relationship

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### LCM

$$
\boxed{
LCM=\frac{a\times b}{HCF}
}
$$

### HCF

$$
\boxed{
HCF=\frac{a\times b}{LCM}
}
$$

### Missing Number

$$
\boxed{
b=\frac{HCF\times LCM}{a}
}
$$

### Coprime Numbers

$$
\boxed{
HCF=1\Rightarrow LCM=ab
}
$$

### Ratio + HCF

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
\boxed{
a=Hm,\quad b=Hn
}
$$

### Ratio + LCM

$$
\boxed{
H=\frac{LCM}{mn}
}
$$

---

# 38. Important Patterns

> [!important] High-Yield

### Pattern 1

Given two numbers + HCF:

$$
\boxed{
LCM=\frac{ab}{HCF}
}
$$

### Pattern 2

Given two numbers + LCM:

$$
\boxed{
HCF=\frac{ab}{LCM}
}
$$

### Pattern 3

Given HCF + LCM + one number:

$$
\boxed{
\text{Missing number}
=
\frac{HCF\times LCM}{\text{known number}}
}
$$

### Pattern 4

Coprime numbers:

$$
\boxed{LCM=Product}
$$

### Pattern 5

One number divides another:

$$
\boxed{HCF=\text{smaller},\quad LCM=\text{larger}}
$$

### Pattern 6

Consecutive numbers:

$$
\boxed{HCF=1,\quad LCM=product}
$$

### Pattern 7

Ratio + HCF:

$$
\boxed{\text{Multiply reduced ratio by HCF}}
$$

### Pattern 8

Same remainder:

$$
\boxed{HCF\text{ of differences}}
$$

### Pattern 9

Same remainder + smallest number:

$$
\boxed{LCM+r}
$$

---

# 39. HCF vs LCM — Final Memory Table

| Situation | Use |
|---|---|
| Greatest common divisor | HCF |
| Smallest common multiple | LCM |
| Greatest equal size | HCF |
| Maximum equal groups | HCF |
| Greatest measuring length | HCF |
| Repeating events together | LCM |
| Smallest number divisible by all | LCM |
| Same remainder, greatest divisor | HCF of differences |
| Same remainder, smallest number | LCM + remainder |
| Prime factorization for HCF | Minimum powers |
| Prime factorization for LCM | Maximum powers |

---

# 40. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Applying `HCF × LCM = product` to three or more numbers.
- ❌ Using maximum powers for HCF.
- ❌ Using minimum powers for LCM.
- ❌ Forgetting that the relationship directly concerns two numbers.
- ❌ Confusing "greatest" with HCF and "least" with LCM without considering context.
- ❌ Using `LCM + r` when the remainders are different.
- ❌ Forgetting to reduce a ratio before using HCF/LCM formulas.
- ❌ Forgetting the coprime condition in ratio-based problems.
- ❌ Assuming HCF and LCM are independent values.

---

# 41. Exam Strategy

> [!tip] Fast Decision Tree

### Given `a`, `b`, and HCF

Immediately:

$$
\boxed{
LCM=\frac{ab}{HCF}
}
$$

### Given `a`, `b`, and LCM

Immediately:

$$
\boxed{
HCF=\frac{ab}{LCM}
}
$$

### Given HCF, LCM, and one number

Immediately:

$$
\boxed{
\text{Missing number}
=
\frac{HCF\times LCM}{\text{known number}}
}
$$

### Given ratio + HCF

Multiply the reduced ratio by HCF.

### Given ratio + LCM

Use:

$$
\boxed{
LCM=Hmn
}
$$

### Given same remainder

- Greatest divisor → HCF of differences
- Smallest number → LCM + remainder

---

# 42. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

This topic combines almost everything you learned in:

- Factors
- Multiples
- Factorization
- HCF
- LCM
- Remainders
- Ratios

### Master These First

1. HCF × LCM relationship
2. Missing-number problems
3. HCF/LCM from prime powers
4. Coprime numbers
5. Ratio + HCF
6. Ratio + LCM
7. Same-remainder problems
8. LCM + remainder problems
9. Sum/product + HCF/LCM
10. Two-number vs three-number distinction

---

# 43. Practice Checklist

- [ ] Find LCM using HCF
- [ ] Find HCF using LCM
- [ ] Find a missing number
- [ ] Solve coprime-number problems
- [ ] Solve ratio + HCF problems
- [ ] Solve ratio + LCM problems
- [ ] Solve same-remainder problems
- [ ] Solve LCM + remainder problems
- [ ] Solve sum + HCF problems
- [ ] Solve product + HCF/LCM problems
- [ ] Practice prime-exponent questions
- [ ] Revise two-number limitation

---

# 44. Related Topics

- [[HCF and LCM]]
- [[HCF]]
- [[LCM]]
- [[Factors]]
- [[Multiples]]
- [[Factorization]]
- [[Remainders]]
- [[Divisibility Rules]]
- [[HCF and LCM of Fractions]]
- [[Application Problems]]

---

# 45. Quick Revision

> [!summary] One-Minute Revision

### Golden Formula

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### Find LCM

$$
\boxed{
LCM=\frac{ab}{HCF}
}
$$

### Find HCF

$$
\boxed{
HCF=\frac{ab}{LCM}
}
$$

### Find Missing Number

$$
\boxed{
b=\frac{HCF\times LCM}{a}
}
$$

### Coprime

$$
\boxed{
HCF=1\Rightarrow LCM=ab
}
$$

### Prime Powers

$$
\boxed{
HCF\rightarrow\min
}
$$

$$
\boxed{
LCM\rightarrow\max
}
$$

### Same Remainder

$$
\boxed{
HCF(\text{differences})
}
$$

### Same Remainder + Smallest Number

$$
\boxed{
LCM+r
}
$$

### Golden Memory Trick

> **HCF takes the common minimum. LCM takes everything at maximum. Their product reconstructs the product of the two original numbers.**

### Critical Warning

> **`HCF × LCM = a × b` is a direct two-number formula. Do not blindly extend it to three numbers.**