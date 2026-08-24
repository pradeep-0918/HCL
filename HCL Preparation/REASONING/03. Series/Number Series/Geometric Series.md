---
type: concept
subject: reasoning
topic: "Geometric Series"
parent: "03. Series"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - series
  - geometric-series
  - geometric-progression
  - gp
  - number-series
  - logical-reasoning
  - hcl
wikilinks:
  - "[[03. Series]]"
  - "[[Number Series]]"
  - "[[Missing Number Series]]"
  - "[[Wrong Number Series]]"
  - "[[Arithmetic Series]]"
  - "[[Mixed Pattern Series]]"
---

# Geometric Series

## 1. Core Concept

> [!summary]
> A **Geometric Progression (GP)** is a sequence in which every term is obtained by multiplying or dividing the previous term by the same constant number. This constant is called the **common ratio**.

Example:

$$
2,\ 6,\ 18,\ 54,\ 162
$$

Check the ratio:

$$
\frac{6}{2}=3
$$

$$
\frac{18}{6}=3
$$

$$
\frac{54}{18}=3
$$

Therefore:

$$
\boxed{r=3}
$$

The pattern is:

$$
\times3
$$

### Core Intuition

Think:

> **"Multiply by the same number every time."**

If the ratio is constant, immediately think:

$$
\boxed{\text{Geometric Progression (GP)}}
$$

---

# 2. Basic Meaning

A geometric progression has the form:

$$
a,\ ar,\ ar^2,\ ar^3,\ldots
$$

where:

- $a$ = first term
- $r$ = common ratio
- $n$ = position of the term
- $a_n$ = $n$th term

### Example

$$
3,\ 12,\ 48,\ 192,\ldots
$$

Here:

$$
a=3
$$

and:

$$
r=4
$$

Therefore:

$$
a_n=3(4^{n-1})
$$

---

# 3. Main Formula

## 3.1 Common Ratio

The common ratio is:

$$
\boxed{r=\frac{a_2}{a_1}}
$$

More generally:

$$
\boxed{r=\frac{a_n}{a_{n-1}}}
$$

---

## 3.2 nth Term

The most important GP formula is:

$$
\boxed{a_n=ar^{n-1}}
$$

where:

- $a$ = first term
- $r$ = common ratio
- $n$ = term position

### Example

Find the 6th term:

$$
2,\ 6,\ 18,\ 54,\ldots
$$

Here:

$$
a=2
$$

$$
r=3
$$

$$
n=6
$$

Therefore:

$$
a_6=2(3^{6-1})
$$

$$
=2(3^5)
$$

$$
=2(243)
$$

$$
=486
$$

### Answer

$$
\boxed{486}
$$

---

## 3.3 Sum of First n Terms

For:

$$
r\neq1
$$

the sum is:

$$
\boxed{S_n=a\frac{r^n-1}{r-1}}
$$

An equivalent form is:

$$
\boxed{S_n=a\frac{1-r^n}{1-r}}
$$

Both formulas give the same result.

---

## 3.4 Sum When $r=1$

If:

$$
r=1
$$

then all terms are equal:

$$
a,\ a,\ a,\ a,\ldots
$$

Therefore:

$$
\boxed{S_n=na}
$$

---

## 3.5 Infinite Geometric Series

An infinite GP has a finite sum only when:

$$
\boxed{|r|<1}
$$

The formula is:

$$
\boxed{S_\infty=\frac{a}{1-r}}
$$

Example:

$$
10+5+2.5+1.25+\cdots
$$

Here:

$$
a=10
$$

$$
r=\frac12
$$

Therefore:

$$
S_\infty=\frac{10}{1-\frac12}
$$

$$
=20
$$

### Answer

$$
\boxed{20}
$$

---

# 4. Important Properties

## Property 1 — Constant Ratio

In a GP:

$$
\frac{a_2}{a_1}
=
\frac{a_3}{a_2}
=
\frac{a_4}{a_3}
$$

Therefore:

$$
\boxed{\text{Ratio is constant}}
$$

---

## Property 2 — Ratio Greater Than 1

If:

$$
r>1
$$

and $a>0$, the terms grow in magnitude.

Example:

$$
2,\ 6,\ 18,\ 54
$$

---

## Property 3 — Ratio Between 0 and 1

If:

$$
0<r<1
$$

the terms decrease toward zero.

Example:

$$
100,\ 50,\ 25,\ 12.5
$$

---

## Property 4 — Negative Ratio

If:

$$
r<0
$$

the signs alternate.

Example:

$$
2,\ -4,\ 8,\ -16,\ 32
$$

Here:

$$
r=-2
$$

---

## Property 5 — Ratio Equal to 1

If:

$$
r=1
$$

all terms are equal.

Example:

$$
7,\ 7,\ 7,\ 7
$$

---

## Property 6 — Ratio Equal to -1

If:

$$
r=-1
$$

the terms alternate between two values.

Example:

$$
5,\ -5,\ 5,\ -5
$$

---

## Property 7 — Middle Term Property

For three consecutive GP terms:

$$
a,\ b,\ c
$$

we have:

$$
\boxed{b^2=ac}
$$

Therefore:

$$
\boxed{b=\sqrt{ac}}
$$

when the positive-root context applies.

### Example

$$
4,\ x,\ 36
$$

Then:

$$
x^2=4(36)
$$

$$
x^2=144
$$

$$
x=12
$$

For a positive GP:

$$
\boxed{x=12}
$$

---

## Property 8 — Product of Equidistant Terms

In a GP:

$$
a_i\times a_j
$$

is constant for positions equally distant from the ends.

For example:

$$
2,\ 6,\ 18,\ 54,\ 162
$$

Then:

$$
2\times162=324
$$

$$
6\times54=324
$$

$$
18\times18=324
$$

Therefore:

$$
\boxed{\text{Equidistant terms have the same product}}
$$

---

# 5. Geometric Progression vs Arithmetic Progression

This comparison is extremely important.

| Property | Arithmetic Progression | Geometric Progression |
|---|---|---|
| Main idea | Constant difference | Constant ratio |
| Formula | $a_n=a+(n-1)d$ | $a_n=ar^{n-1}$ |
| Example | $2,5,8,11$ | $2,6,18,54$ |
| Check | Subtraction | Division |
| Growth | Linear | Multiplicative |

### Recognition

> [!important]
> **Same difference → AP**
>
> **Same ratio → GP**

Example:

$$
3,\ 6,\ 9,\ 12
$$

Differences:

$$
3,3,3
$$

Therefore:

$$
\boxed{AP}
$$

But:

$$
3,\ 6,\ 12,\ 24
$$

Ratios:

$$
2,2,2
$$

Therefore:

$$
\boxed{GP}
$$

---

# 6. Basic Examples

## Example 1 — Identify the Common Ratio

### Question

Find the common ratio:

$$
3,\ 9,\ 27,\ 81
$$

### Calculation

$$
\frac{9}{3}=3
$$

$$
\frac{27}{9}=3
$$

$$
\frac{81}{27}=3
$$

Therefore:

$$
\boxed{r=3}
$$

---

## Example 2 — Find the Next Term

### Question

$$
5,\ 10,\ 20,\ 40,\ ?
$$

Pattern:

$$
\times2
$$

Therefore:

$$
40\times2=80
$$

### Answer

$$
\boxed{80}
$$

---

## Example 3 — Fractional Ratio

### Question

$$
64,\ 32,\ 16,\ 8,\ ?
$$

Pattern:

$$
\div2
$$

Therefore:

$$
8\div2=4
$$

Equivalently:

$$
r=\frac12
$$

### Answer

$$
\boxed{4}
$$

---

## Example 4 — Negative Ratio

### Question

$$
3,\ -6,\ 12,\ -24,\ ?
$$

Ratio:

$$
-2
$$

Therefore:

$$
-24\times(-2)=48
$$

### Answer

$$
\boxed{48}
$$

---

# 7. Finding the nth Term

## Example 5

### Question

Find the 7th term:

$$
2,\ 6,\ 18,\ 54,\ldots
$$

Here:

$$
a=2
$$

$$
r=3
$$

$$
n=7
$$

Use:

$$
a_n=ar^{n-1}
$$

$$
a_7=2(3^6)
$$

$$
=2(729)
$$

$$
=1458
$$

### Answer

$$
\boxed{1458}
$$

---

## Example 6

### Question

Find the 8th term:

$$
81,\ 27,\ 9,\ 3,\ldots
$$

Here:

$$
a=81
$$

$$
r=\frac13
$$

$$
n=8
$$

Therefore:

$$
a_8=81\left(\frac13\right)^7
$$

Since:

$$
81=3^4
$$

we get:

$$
a_8=3^4\cdot3^{-7}
$$

$$
=3^{-3}
$$

$$
=\frac1{27}
$$

### Answer

$$
\boxed{\frac1{27}}
$$

---

# 8. Finding the Common Ratio

## Example 7

### Question

The first term is $4$ and the 5th term is $324$. Find the common ratio.

Use:

$$
a_n=ar^{n-1}
$$

Therefore:

$$
324=4r^4
$$

$$
r^4=81
$$

Since:

$$
81=3^4
$$

we get:

$$
r=3
$$

### Answer

$$
\boxed{3}
$$

> [!important]
> In algebraic problems, the equation may have multiple mathematical roots. Aptitude questions usually provide enough context or options to identify the intended ratio.

---

# 9. Finding the First Term

## Example 8

### Question

The 6th term of a GP is $160$ and the common ratio is $2$. Find the first term.

Given:

$$
a_6=160
$$

$$
r=2
$$

Use:

$$
a_n=ar^{n-1}
$$

$$
160=a(2^5)
$$

$$
160=32a
$$

Therefore:

$$
a=5
$$

### Answer

$$
\boxed{5}
$$

---

# 10. Finding the Number of Terms

## Example 9

### Question

How many terms are there in:

$$
3,\ 6,\ 12,\ 24,\ldots,384
$$

Here:

$$
a=3
$$

$$
r=2
$$

$$
l=384
$$

Use:

$$
384=3(2^{n-1})
$$

Therefore:

$$
2^{n-1}=128
$$

Since:

$$
128=2^7
$$

we get:

$$
n-1=7
$$

$$
n=8
$$

### Answer

$$
\boxed{8}
$$

---

# 11. Missing Term in a GP

## Example 10

### Question

Find the missing number:

$$
2,\ 6,\ ?,\ 54
$$

Check ratio:

$$
\frac62=3
$$

Therefore:

$$
6\times3=18
$$

Verify:

$$
18\times3=54
$$

### Answer

$$
\boxed{18}
$$

---

## Example 11 — Middle Term Shortcut

### Question

Find $x$:

$$
4,\ x,\ 36
$$

For three consecutive GP terms:

$$
x^2=4(36)
$$

$$
x^2=144
$$

Therefore:

$$
x=12
$$

### Answer

$$
\boxed{12}
$$

---

# 12. Multiple Missing Terms

## Example 12

### Question

Find the missing numbers:

$$
3,\ ?,\ 27,\ ?,\ 243
$$

Assume constant ratio:

$$
r=3
$$

Then:

$$
3\times3=9
$$

$$
27\times3=81
$$

Therefore:

$$
\boxed{9,\ 81}
$$

---

# 13. Sum of a Finite GP

## Example 13

### Question

Find:

$$
2+6+18+54+162
$$

Here:

$$
a=2
$$

$$
r=3
$$

$$
n=5
$$

Use:

$$
S_n=a\frac{r^n-1}{r-1}
$$

$$
S_5=2\frac{3^5-1}{3-1}
$$

$$
=2\frac{243-1}{2}
$$

$$
=242
$$

### Answer

$$
\boxed{242}
$$

---

## Example 14 — Ratio Less Than 1

### Question

Find:

$$
100+50+25+12.5
$$

Here:

$$
a=100
$$

$$
r=\frac12
$$

$$
n=4
$$

Therefore:

$$
S_4
=
100\frac{1-(\frac12)^4}{1-\frac12}
$$

$$
=
100\frac{1-\frac1{16}}{\frac12}
$$

$$
=
100\frac{15}{16}\times2
$$

$$
=187.5
$$

### Answer

$$
\boxed{187.5}
$$

---

# 14. Infinite Geometric Series

## Example 15

### Question

Find:

$$
8+4+2+1+\frac12+\cdots
$$

Here:

$$
a=8
$$

$$
r=\frac12
$$

Since:

$$
|r|<1
$$

the infinite sum exists.

Use:

$$
S_\infty=\frac{a}{1-r}
$$

$$
S_\infty=\frac8{1-\frac12}
$$

$$
=\frac8{\frac12}
$$

$$
=16
$$

### Answer

$$
\boxed{16}
$$

---

## Example 16 — Infinite GP with Negative Ratio

### Question

Find:

$$
10-5+2.5-1.25+\cdots
$$

Here:

$$
a=10
$$

$$
r=-\frac12
$$

Since:

$$
\left|-\frac12\right|<1
$$

the sum exists.

Therefore:

$$
S_\infty=
\frac{10}{1-(-\frac12)}
$$

$$
=
\frac{10}{\frac32}
$$

$$
=\frac{20}{3}
$$

### Answer

$$
\boxed{\frac{20}{3}}
$$

---

# 15. When Infinite GP Does Not Have a Finite Sum

## Example 17

Consider:

$$
2+4+8+16+\cdots
$$

Here:

$$
r=2
$$

Since:

$$
|r|>1
$$

the terms do not approach zero.

Therefore, there is no finite infinite sum.

### Answer

$$
\boxed{\text{No finite sum}}
$$

> [!warning]
> The infinite GP formula:
>
> $$S_\infty=\frac{a}{1-r}$$
>
> is valid only when:
>
> $$|r|<1$$

---

# 16. GP with Negative Ratio

Negative ratios create alternating signs.

## Example 18

### Question

Find the next two terms:

$$
5,\ -10,\ 20,\ -40,\ ?
$$

Ratio:

$$
r=-2
$$

Therefore:

$$
-40\times(-2)=80
$$

Next:

$$
80\times(-2)=-160
$$

### Answer

$$
\boxed{80,\ -160}
$$

### Recognition

> [!important]
> If signs alternate:

$$
+,-,+,-,+,\ldots
$$

check for a **negative common ratio**.

---

# 17. Powers as Geometric Progression

Many power sequences are GP.

## Example 19

### Question

$$
2,\ 4,\ 8,\ 16,\ 32,\ ?
$$

This can be written as:

$$
2^1,\ 2^2,\ 2^3,\ 2^4,\ 2^5
$$

The ratio is:

$$
2
$$

Therefore:

$$
32\times2=64
$$

### Answer

$$
\boxed{64}
$$

---

# 18. Advanced Pattern — Increasing Multiplier

Not every rapidly growing sequence is a GP.

## Example 20

### Question

$$
2,\ 4,\ 12,\ 48,\ 240,\ ?
$$

Ratios are:

$$
2,\ 3,\ 4,\ 5
$$

The ratio is not constant.

Therefore this is **not a GP**.

The pattern is:

$$
\times2,\times3,\times4,\times5
$$

Next:

$$
240\times6=1440
$$

### Answer

$$
\boxed{1440}
$$

> [!warning]
> Do not call every multiplication-based sequence a GP. A GP requires the **same ratio** at every step.

---

# 19. Advanced Pattern — GP with Sign Changes

## Example 21

### Question

Find the missing number:

$$
2,\ -6,\ 18,\ ?,\ 162
$$

Ratio:

$$
-3
$$

Therefore:

$$
18\times(-3)=-54
$$

Verify:

$$
-54\times(-3)=162
$$

### Answer

$$
\boxed{-54}
$$

---

# 20. Advanced Pattern — Fractional GP

## Example 22

### Question

Find the next term:

$$
81,\ 27,\ 9,\ 3,\ ?
$$

Ratio:

$$
\frac13
$$

Therefore:

$$
3\times\frac13=1
$$

### Answer

$$
\boxed{1}
$$

---

# 21. Advanced Placement Pattern — Find a Term from Two Terms

## Example 23

### Question

The 3rd term of a GP is $20$ and the 6th term is $160$. Find the common ratio.

We know:

$$
a_3=ar^2=20
$$

and:

$$
a_6=ar^5=160
$$

Divide:

$$
\frac{a_6}{a_3}
=
\frac{ar^5}{ar^2}
$$

Therefore:

$$
\frac{160}{20}=r^3
$$

$$
8=r^3
$$

Thus:

$$
r=2
$$

### Answer

$$
\boxed{2}
$$

> [!tip]
> When two GP terms are known, **divide them** to eliminate the first term.

---

# 22. Advanced Placement Pattern — Find Another Term

## Example 24

### Question

The 4th term of a GP is $24$ and the 7th term is $192$. Find the 10th term.

Given:

$$
a_4=ar^3=24
$$

$$
a_7=ar^6=192
$$

Divide:

$$
\frac{a_7}{a_4}=r^3
$$

$$
\frac{192}{24}=8
$$

Therefore:

$$
r^3=8
$$

$$
r=2
$$

We need the 10th term.

From the 7th term to the 10th term, there are 3 multiplication steps:

$$
a_{10}=a_7r^3
$$

$$
=192(8)
$$

$$
=1536
$$

### Answer

$$
\boxed{1536}
$$

---

# 23. Advanced Placement Pattern — Product of Terms

## Example 25

### Question

Three consecutive positive GP terms have product $216$. Find the middle term.

Let the terms be:

$$
\frac{x}{r},\ x,\ xr
$$

Their product is:

$$
\frac{x}{r}\times x\times xr=x^3
$$

Therefore:

$$
x^3=216
$$

$$
x=6
$$

### Answer

$$
\boxed{6}
$$

> [!important]
> For three consecutive positive GP terms, the middle term is the **geometric mean** of the other two.

---

# 24. Geometric Mean

For positive numbers $a$ and $b$, their geometric mean is:

$$
\boxed{GM=\sqrt{ab}}
$$

If $a$, $G$, $b$ are consecutive GP terms:

$$
\boxed{G=\sqrt{ab}}
$$

### Example 26

Find the geometric mean of $4$ and $100$.

$$
GM=\sqrt{4\times100}
$$

$$
=\sqrt{400}
$$

$$
=20
$$

### Answer

$$
\boxed{20}
$$

---

# 25. Arithmetic Mean vs Geometric Mean

| Mean | Formula | Used For |
|---|---|---|
| Arithmetic Mean | $\frac{a+b}{2}$ | AP |
| Geometric Mean | $\sqrt{ab}$ | GP |

### Example

For $4$ and $36$:

Arithmetic mean:

$$
AM=\frac{4+36}{2}=20
$$

Geometric mean:

$$
GM=\sqrt{4\times36}=12
$$

Therefore:

$$
\boxed{AM=20,\quad GM=12}
$$

---

# 26. Recognition Tricks

## Pattern 1 — Constant Ratio

> [!important]
> If dividing consecutive terms gives the same value, think **GP**.

Example:

$$
5,\ 15,\ 45,\ 135
$$

Ratio:

$$
3
$$

Therefore:

$$
\boxed{GP}
$$

---

## Pattern 2 — Rapid Growth

> [!important]
> If numbers grow very quickly, check multiplication before addition.

Example:

$$
2,\ 8,\ 32,\ 128
$$

Think:

$$
\times4
$$

---

## Pattern 3 — Rapid Decrease

> [!important]
> If terms decrease rapidly, check division.

Example:

$$
256,\ 128,\ 64,\ 32
$$

Think:

$$
\div2
$$

---

## Pattern 4 — Alternating Signs

> [!important]
> If signs alternate:

$$
+,-,+,-,+
$$

check for a negative ratio.

Example:

$$
3,-6,12,-24
$$

Think:

$$
\times(-2)
$$

---

## Pattern 5 — Fractions

> [!important]
> If each term becomes a fixed fraction of the previous term:

$$
100,\ 50,\ 25,\ 12.5
$$

think:

$$
r=\frac12
$$

---

## Pattern 6 — Middle Term

> [!important]
> For three consecutive positive GP terms:

$$
a,\ x,\ c
$$

use:

$$
\boxed{x=\sqrt{ac}}
$$

---

## Pattern 7 — nth Term

> [!important]
> If the question asks for the $n$th term:

$$
\boxed{a_n=ar^{n-1}}
$$

---

## Pattern 8 — Sum of Finite GP

> [!important]
> If the question asks for:

$$
a+ar+ar^2+\cdots
$$

use:

$$
\boxed{S_n=a\frac{r^n-1}{r-1}}
$$

for $r\neq1$.

---

## Pattern 9 — Infinite Sum

> [!important]
> If the sequence continues forever and:

$$
|r|<1
$$

use:

$$
\boxed{S_\infty=\frac{a}{1-r}}
$$

---

## Pattern 10 — Two Known Terms

> [!important]
> If two terms are given:

$$
a_m,\ a_n
$$

divide them to eliminate $a$:

$$
\boxed{\frac{a_n}{a_m}=r^{n-m}}
$$

This is extremely useful in placement aptitude.

---

# 27. Shortcuts

> [!tip]
> **Shortcut 1 — Check division before subtraction for fast-growing terms**

For:

$$
3,\ 9,\ 27,\ 81
$$

do:

$$
9\div3=3
$$

rather than calculating large differences.

---

> [!tip]
> **Shortcut 2 — Three consecutive GP terms**

For:

$$
a,\ x,\ c
$$

immediately use:

$$
\boxed{x^2=ac}
$$

---

> [!tip]
> **Shortcut 3 — Two known terms**

If:

$$
a_m,\ a_n
$$

are known, divide:

$$
\boxed{\frac{a_n}{a_m}=r^{n-m}}
$$

This removes the first term.

---

> [!tip]
> **Shortcut 4 — Sum when first and last terms are powers**

For sequences such as:

$$
2,\ 4,\ 8,\ldots,128
$$

first determine $n$ using powers of $2$, then apply the GP sum formula.

---

> [!tip]
> **Shortcut 5 — Negative ratio**

If the signs alternate, immediately test:

$$
r<0
$$

Example:

$$
4,-12,36,-108
$$

gives:

$$
r=-3
$$

---

> [!tip]
> **Shortcut 6 — Infinite GP**

The moment you see:

> "continues indefinitely"

check:

$$
|r|<1
$$

before using:

$$
S_\infty=\frac{a}{1-r}
$$

---

> [!tip]
> **Shortcut 7 — Powers**

If terms are:

$$
3,\ 9,\ 27,\ 81
$$

rewrite them as:

$$
3^1,\ 3^2,\ 3^3,\ 3^4
$$

This makes the GP structure obvious.

---

# 28. Common Exam Patterns

> [!important] Must Master

### Basic GP Patterns

1. Identify geometric progression
2. Find common ratio
3. Find next term
4. Find previous term
5. Find missing term
6. Find wrong term

### Term-Based Problems

7. Find nth term
8. Find first term
9. Find common ratio
10. Find number of terms
11. Find last term
12. Find which term contains a given number
13. Check whether a number belongs to the GP

### Sum-Based Problems

14. Sum of first $n$ terms
15. Sum of finite GP
16. Sum of infinite GP
17. Sum of decreasing GP
18. Sum of alternating GP

### Advanced GP

19. Three consecutive GP terms
20. Geometric mean
21. Product of consecutive terms
22. Two known terms and find ratio
23. Two known terms and find another term
24. Find missing middle term
25. Find first term from nth term
26. Find ratio from two terms

### Special Patterns

27. Powers of 2
28. Powers of 3
29. Powers of 10
30. Fractional ratio
31. Negative ratio
32. Alternating signs
33. Ratio less than 1
34. Ratio greater than 1

---

# 29. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing AP and GP

AP checks:

$$
\boxed{\text{Difference}}
$$

GP checks:

$$
\boxed{\text{Ratio}}
$$

---

### Mistake 2 — Using the wrong nth-term formula

GP uses:

$$
\boxed{a_n=ar^{n-1}}
$$

not:

$$
a+(n-1)d
$$

That formula belongs to AP.

---

### Mistake 3 — Forgetting the exponent $(n-1)$

For the 5th term:

$$
a_5=ar^4
$$

not:

$$
ar^5
$$

---

### Mistake 4 — Ignoring negative ratios

For:

$$
2,-6,18,-54
$$

the ratio is:

$$
\boxed{-3}
$$

not $3$.

---

### Mistake 5 — Using infinite-sum formula incorrectly

The formula:

$$
S_\infty=\frac{a}{1-r}
$$

works only when:

$$
\boxed{|r|<1}
$$

---

### Mistake 6 — Assuming every multiplication sequence is GP

Consider:

$$
2,\ 4,\ 12,\ 48
$$

Ratios:

$$
2,\ 3,\ 4
$$

Not constant.

Therefore:

$$
\boxed{\text{Not GP}}
$$

---

### Mistake 7 — Forgetting fractional ratios

A sequence can be GP even when it divides:

$$
100,\ 50,\ 25,\ 12.5
$$

Here:

$$
r=\frac12
$$

---

### Mistake 8 — Ignoring zero terms

A GP containing zero requires care.

For example:

$$
0,\ 0,\ 0
$$

can be represented with ratio $r$ in a degenerate sense, but dividing consecutive terms to find the ratio is not valid.

> [!important]
> In ordinary aptitude problems, use the ratio method only when the relevant previous term is non-zero.

---

# 30. Formula Sheet

## Common Ratio

$$
\boxed{r=\frac{a_n}{a_{n-1}}}
$$

## nth Term

$$
\boxed{a_n=ar^{n-1}}
$$

## Sum of First n Terms

$$
\boxed{S_n=a\frac{r^n-1}{r-1}}
$$

for:

$$
r\neq1
$$

Equivalent form:

$$
\boxed{S_n=a\frac{1-r^n}{1-r}}
$$

## If $r=1$

$$
\boxed{S_n=na}
$$

## Infinite GP

$$
\boxed{S_\infty=\frac{a}{1-r}}
$$

valid when:

$$
\boxed{|r|<1}
$$

## Three Consecutive GP Terms

$$
\boxed{\frac{x}{r},\ x,\ xr}
$$

## Middle Term

$$
\boxed{x^2=ac}
$$

## Geometric Mean

$$
\boxed{GM=\sqrt{ab}}
$$

## Ratio from Two Terms

$$
\boxed{\frac{a_n}{a_m}=r^{n-m}}
$$

## nth Term from Two Known Terms

If $a_m$ and $a_n$ are known:

$$
\boxed{r=\left(\frac{a_n}{a_m}\right)^{\frac1{n-m}}}
$$

when the real root is appropriate for the problem.

---

# 31. Quick Revision

> [!summary] One-Minute Revision

## Geometric Series / GP

A GP has a **constant common ratio**.

### Recognition

$$
\boxed{
\frac{a_2}{a_1}
=
\frac{a_3}{a_2}
=
\frac{a_4}{a_3}
}
$$

### Most Important Formula

$$
\boxed{a_n=ar^{n-1}}
$$

### Finite Sum

$$
\boxed{S_n=a\frac{r^n-1}{r-1}}
$$

### Infinite Sum

$$
\boxed{S_\infty=\frac{a}{1-r}}
$$

only when:

$$
\boxed{|r|<1}
$$

### Three Consecutive Terms

$$
\boxed{\frac{x}{r},\ x,\ xr}
$$

### Middle Term

$$
\boxed{x^2=ac}
$$

### Geometric Mean

$$
\boxed{GM=\sqrt{ab}}
$$

### Fast Recognition

If:

$$
\text{Difference is constant}
$$

think:

$$
\boxed{AP}
$$

If:

$$
\text{Ratio is constant}
$$

think:

$$
\boxed{GP}
$$

If the signs alternate, check:

$$
\boxed{r<0}
$$

If the terms shrink toward zero, check:

$$
\boxed{0<|r|<1}
$$

### Golden Memory Trick

**"AP adds the same amount; GP multiplies by the same ratio."**

# One-Line Recognition

**When consecutive terms are obtained by multiplying or dividing by the same constant number, recognize a Geometric Progression and use the GP term, ratio, or sum formulas.**