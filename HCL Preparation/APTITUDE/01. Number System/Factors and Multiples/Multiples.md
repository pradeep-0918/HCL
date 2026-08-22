---
type: concept
subject: aptitude
topic: "Multiples"
parent: "01. Number System/Factors and Multiples"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - multiples
  - factors-and-multiples
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Factors and Multiples]]"
  - "[[Factors]]"
  - "[[Number of Factors]]"
  - "[[HCF]]"
  - "[[LCM]]"
  - "[[Divisibility Rules]]"
  - "[[Remainders]]"
---

# Multiples

## 1. Core Concept

> [!summary] Definition
> A **multiple** of a number is obtained by multiplying that number by an integer.

If:

$$
N=a\times k
$$

then:

$$
\boxed{N\text{ is a multiple of }a}
$$

where `k` is an integer.

For positive multiples, we usually take:

$$
k=1,2,3,4,\ldots
$$

---

# 2. Basic Example

Multiples of `5` are:

$$
5\times1=5
$$

$$
5\times2=10
$$

$$
5\times3=15
$$

$$
5\times4=20
$$

Therefore:

$$
\boxed{5,10,15,20,25,30,\ldots}
$$

are multiples of `5`.

---

# 3. Factor vs Multiple

This distinction is extremely important.

Consider:

$$
3\times8=24
$$

Then:

- `3` is a factor of `24`.
- `8` is a factor of `24`.
- `24` is a multiple of `3`.
- `24` is a multiple of `8`.

Therefore:

$$
\boxed{\text{Factors divide a number}}
$$

while:

$$
\boxed{\text{Multiples are produced by multiplication}}
$$

---

# 4. Important Relationship

If:

$$
a\mid N
$$

then:

$$
\boxed{N\text{ is a multiple of }a}
$$

Equivalently:

$$
\boxed{N=a\times k}
$$

for some integer `k`.

### Example

Since:

$$
7\mid35
$$

we know:

$$
\boxed{35\text{ is a multiple of 7}}
$$

---

# 5. First Multiple

For a positive integer `a`, the first positive multiple is:

$$
\boxed{a}
$$

because:

$$
a\times1=a
$$

Example:

First positive multiple of `12`:

$$
\boxed{12}
$$

---

# 6. Is Zero a Multiple?

Mathematically:

$$
0=a\times0
$$

Therefore:

$$
\boxed{0\text{ is a multiple of every integer}}
$$

However, aptitude questions asking for **positive multiples** normally begin with:

$$
a,2a,3a,\ldots
$$

> [!important] Exam Convention
> If the question says **positive multiples**, do not include `0`.

---

# 7. Negative Multiples

If integers are allowed, negative multiples also exist.

For `6`:

$$
\ldots,-18,-12,-6,0,6,12,18,\ldots
$$

But standard aptitude questions generally focus on positive multiples unless stated otherwise.

---

# 8. Multiples Form an Arithmetic Progression

The positive multiples of `a` are:

$$
a,2a,3a,4a,\ldots
$$

The common difference is:

$$
a
$$

Therefore:

$$
\boxed{\text{Multiples of }a\text{ form an AP}}
$$

### Example

Multiples of `7`:

$$
7,14,21,28,35,\ldots
$$

Common difference:

$$
7
$$

---

# 9. General Formula for Multiples

The `n`th positive multiple of `a` is:

$$
\boxed{T_n=an}
$$

### Example

Find the `15`th positive multiple of `8`.

$$
T_{15}=8\times15
$$

$$
\boxed{120}
$$

---

# 10. Number of Multiples from 1 to N

The number of positive multiples of `a` from `1` to `N` is:

$$
\boxed{
\left\lfloor\frac Na\right\rfloor
}
$$

where:

$$
\lfloor x\rfloor
$$

means the greatest integer less than or equal to `x`.

### Example

How many positive multiples of `7` are there from `1` to `100`?

$$
\left\lfloor\frac{100}{7}\right\rfloor
$$

$$
=14
$$

Therefore:

$$
\boxed{14}
$$

---

# 11. Multiples in a Range

For the inclusive range:

$$
A\le N\le B
$$

the number of multiples of `a` is:

$$
\boxed{
\left\lfloor\frac Ba\right\rfloor
-
\left\lfloor\frac{A-1}{a}\right\rfloor
}
$$

### Example

How many multiples of `6` are between `20` and `100`?

$$
\left\lfloor\frac{100}{6}\right\rfloor
-
\left\lfloor\frac{19}{6}\right\rfloor
$$

$$
=16-3
$$

$$
\boxed{13}
$$

---

# 12. Smallest Multiple Greater Than N

To find the smallest multiple of `a` greater than `N`:

If:

$$
N=aq+r
$$

where:

$$
0<r<a
$$

then the next multiple is:

$$
\boxed{a(q+1)}
$$

### Example

Find the smallest multiple of `8` greater than `50`.

$$
50=8(6)+2
$$

Next multiple:

$$
8(7)=56
$$

Therefore:

$$
\boxed{56}
$$

---

# 13. Smallest Multiple Greater Than or Equal to N

If the question says:

> Smallest multiple of `a` **greater than or equal to** `N`

then:

$$
\boxed{
a\left\lceil\frac Na\right\rceil
}
$$

where:

$$
\lceil x\rceil
$$

means the smallest integer greater than or equal to `x`.

### Example

Find the smallest multiple of `8` greater than or equal to `50`.

$$
\left\lceil\frac{50}{8}\right\rceil=7
$$

Therefore:

$$
7\times8
$$

$$
\boxed{56}
$$

---

# 14. Largest Multiple Less Than N

If:

$$
N=aq+r
$$

then the largest multiple of `a` less than `N` is:

$$
\boxed{aq}
$$

### Example

Find the largest multiple of `7` less than `50`.

$$
50=7(7)+1
$$

Therefore:

$$
7\times7=49
$$

Answer:

$$
\boxed{49}
$$

---

# 15. Largest Multiple Less Than or Equal to N

The formula is:

$$
\boxed{
a\left\lfloor\frac Na\right\rfloor
}
$$

### Example

Largest multiple of `7` less than or equal to `50`:

$$
7\left\lfloor\frac{50}{7}\right\rfloor
$$

$$
=7\times7
$$

$$
\boxed{49}
$$

---

# 16. Multiples and LCM

When a problem asks for a number that is a multiple of **two or more numbers**, think:

$$
\boxed{\operatorname{LCM}}
$$

### Example

Find the smallest number that is a multiple of `6` and `8`.

Prime factors:

$$
6=2\times3
$$

$$
8=2^3
$$

Therefore:

$$
\operatorname{LCM}(6,8)=2^3\times3
$$

$$
\boxed{24}
$$

So:

$$
24,48,72,96,\ldots
$$

are common multiples of `6` and `8`.

---

# 17. Common Multiples

A number that is a multiple of two numbers is called a **common multiple**.

For `4` and `6`:

Multiples of `4`:

$$
4,8,12,16,20,24,\ldots
$$

Multiples of `6`:

$$
6,12,18,24,30,\ldots
$$

Common multiples:

$$
12,24,36,48,\ldots
$$

The smallest positive common multiple is:

$$
\boxed{12}
$$

Therefore:

$$
\boxed{\operatorname{LCM}(4,6)=12}
$$

---

# 18. Every Common Multiple Is a Multiple of the LCM

If:

$$
L=\operatorname{LCM}(a,b)
$$

then every common multiple of `a` and `b` is a multiple of `L`.

### Example

For `4` and `6`:

$$
\operatorname{LCM}=12
$$

Common multiples:

$$
12,24,36,48,\ldots
$$

All are multiples of `12`.

Therefore:

$$
\boxed{\text{Common multiples}=L,2L,3L,\ldots}
$$

---

# 19. Number of Common Multiples in a Range

Suppose we need numbers divisible by both `a` and `b`.

First find:

$$
L=\operatorname{LCM}(a,b)
$$

Then count multiples of `L`.

### Example

How many numbers from `1` to `100` are divisible by both `6` and `8`?

First:

$$
\operatorname{LCM}(6,8)=24
$$

Then:

$$
\left\lfloor\frac{100}{24}\right\rfloor
$$

$$
\boxed{4}
$$

The numbers are:

$$
24,48,72,96
$$

---

# 20. Multiples and HCF

HCF and LCM have different roles.

### HCF

Finds the **largest common factor**.

### LCM

Finds the **smallest common multiple**.

Therefore:

$$
\boxed{\text{HCF → Factors}}
$$

$$
\boxed{\text{LCM → Multiples}}
$$

> [!tip] Memory Trick
> **HCF looks downward at factors.**
>
> **LCM looks upward at multiples.**

---

# 21. Multiples of a Multiple

If:

$$
b=ak
$$

then every multiple of `b` is also a multiple of `a`.

### Example

Since:

$$
12=6\times2
$$

every multiple of `12` is also a multiple of `6`.

For example:

$$
12,24,36,48,\ldots
$$

are all multiples of `6`.

Therefore:

$$
\boxed{12\mid N\Rightarrow6\mid N}
$$

---

# 22. Common Multiple of Consecutive Numbers

For two consecutive integers:

$$
n,\ n+1
$$

their HCF is always:

$$
\boxed{1}
$$

Therefore their LCM is:

$$
\boxed{n(n+1)}
$$

### Example

For `7` and `8`:

$$
\operatorname{LCM}(7,8)=7\times8
$$

$$
\boxed{56}
$$

---

# 23. Product of Two Numbers and HCF-LCM

For positive integers `a` and `b`:

$$
\boxed{
\operatorname{HCF}(a,b)\times\operatorname{LCM}(a,b)=a\times b
}
$$

### Example

For `12` and `18`:

$$
\operatorname{HCF}=6
$$

$$
\operatorname{LCM}=36
$$

Therefore:

$$
6\times36=216
$$

and:

$$
12\times18=216
$$

Correct.

---

# 24. Multiples and Divisibility

If:

$$
a\mid b
$$

then:

$$
\boxed{b\text{ is a multiple of }a}
$$

If:

$$
b\mid c
$$

then:

$$
\boxed{c\text{ is a multiple of }b}
$$

Therefore:

$$
a\mid b,\quad b\mid c
$$

implies:

$$
\boxed{a\mid c}
$$

---

# 25. Pattern — Multiples Between Two Numbers

### Question

How many multiples of `12` are between `100` and `500`?

Use:

$$
\left\lfloor\frac{500}{12}\right\rfloor
-
\left\lfloor\frac{99}{12}\right\rfloor
$$

$$
=41-8
$$

$$
\boxed{33}
$$

---

# 26. Pattern — Sum of First n Multiples

The first `n` positive multiples of `a` are:

$$
a,2a,3a,\ldots,na
$$

Their sum is:

$$
a(1+2+3+\cdots+n)
$$

Since:

$$
1+2+\cdots+n=\frac{n(n+1)}2
$$

we get:

$$
\boxed{
\text{Sum of first n multiples of }a
=
\frac{an(n+1)}2
}
$$

### Example

Find the sum of the first `10` multiples of `6`.

$$
\frac{6\times10\times11}{2}
$$

$$
=330
$$

Therefore:

$$
\boxed{330}
$$

---

# 27. Average of First n Multiples

The first `n` multiples of `a` are:

$$
a,2a,\ldots,na
$$

Since they form an arithmetic progression:

$$
\text{Average}
=
\frac{a+na}{2}
$$

Therefore:

$$
\boxed{
\text{Average}=\frac{a(n+1)}2
}
$$

### Example

Average of the first `10` multiples of `4`:

$$
\frac{4(10+1)}2
$$

$$
=22
$$

Therefore:

$$
\boxed{22}
$$

---

# 28. Product of First n Multiples

The first `n` multiples of `a` are:

$$
a,2a,3a,\ldots,na
$$

Their product is:

$$
a\times2a\times3a\cdots na
$$

Therefore:

$$
\boxed{
a^n\times n!
}
$$

### Example

Product of the first `4` multiples of `3`:

$$
3\times6\times9\times12
$$

Using the formula:

$$
3^4\times4!
$$

$$
=81\times24
$$

$$
\boxed{1944}
$$

---

# 29. Multiples and Remainders

If:

$$
N=ak+r
$$

then `r` is the remainder when `N` is divided by `a`.

If:

$$
r=0
$$

then:

$$
\boxed{N\text{ is a multiple of }a}
$$

### Example

$$
53=7\times7+4
$$

Therefore:

$$
53\bmod7=4
$$

So `53` is not a multiple of `7`.

---

# 30. Important Formula Sheet

> [!important] Must Remember

### nth Positive Multiple

$$
\boxed{T_n=an}
$$

### Number of Multiples from `1` to `N`

$$
\boxed{
\left\lfloor\frac Na\right\rfloor
}
$$

### Number of Multiples from `A` to `B`

$$
\boxed{
\left\lfloor\frac Ba\right\rfloor
-
\left\lfloor\frac{A-1}{a}\right\rfloor
}
$$

### Largest Multiple ≤ N

$$
\boxed{
a\left\lfloor\frac Na\right\rfloor
}
$$

### Smallest Multiple ≥ N

$$
\boxed{
a\left\lceil\frac Na\right\rceil
}
$$

### Sum of First `n` Multiples

$$
\boxed{
\frac{an(n+1)}2
}
$$

### Average of First `n` Multiples

$$
\boxed{
\frac{a(n+1)}2
}
$$

### Product of First `n` Multiples

$$
\boxed{
a^n n!
}
$$

---

# 31. Important Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{\text{nth multiple of }a=an}
$$

### Pattern 2

$$
\boxed{\text{Count multiples}=\left\lfloor N/a\right\rfloor}
$$

### Pattern 3

For common multiples:

$$
\boxed{\text{Use LCM}}
$$

### Pattern 4

All common multiples are:

$$
\boxed{L,2L,3L,\ldots}
$$

where:

$$
L=\operatorname{LCM}
$$

### Pattern 5

For sum:

$$
\boxed{\text{Sum of first n multiples}=
\frac{an(n+1)}2}
$$

### Pattern 6

For range questions:

$$
\boxed{
\text{Count up to B}
-
\text{Count up to A-1}
}
$$

---

# 32. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Confusing factors with multiples.
- ❌ Including `0` when the question asks for positive multiples.
- ❌ Forgetting whether the range is inclusive.
- ❌ Using `N/a` without taking the floor when counting.
- ❌ Using product instead of LCM for common multiples.
- ❌ Confusing "greater than" with "greater than or equal to".
- ❌ Confusing "less than" with "less than or equal to".
- ❌ Forgetting that common multiples are multiples of the LCM.

---

# 33. Exam Strategy

> [!tip] Fast Decision Tree

### "Find the nth multiple"

Use:

$$
\boxed{an}
$$

### "How many multiples up to N?"

Use:

$$
\boxed{\left\lfloor N/a\right\rfloor}
$$

### "How many in a range?"

Use:

$$
\boxed{
\left\lfloor B/a\right\rfloor
-
\left\lfloor(A-1)/a\right\rfloor
}
$$

### "Common multiple"

Think:

$$
\boxed{\operatorname{LCM}}
$$

### "Largest multiple"

Use floor.

### "Smallest multiple"

Use ceiling.

### "Sum of multiples"

Use:

$$
\boxed{\frac{an(n+1)}2}
$$

---

# 34. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

### Master These First

1. Factor vs multiple
2. nth multiple
3. Counting multiples
4. Range counting
5. Largest/smallest multiple
6. Common multiples
7. LCM connection
8. Sum of multiples
9. Average of multiples
10. Product of multiples
11. Multiples and remainders
12. HCF-LCM relationship

---

# 35. Practice Checklist

- [ ] Understand factor vs multiple
- [ ] Find nth multiples
- [ ] Count multiples
- [ ] Count multiples in ranges
- [ ] Find largest multiple
- [ ] Find smallest multiple
- [ ] Find common multiples
- [ ] Practice LCM-based questions
- [ ] Find sum of multiples
- [ ] Find average of multiples
- [ ] Practice remainder problems
- [ ] Practice HCF-LCM questions
- [ ] Revise common traps

---

# 36. Related Topics

- [[Factors and Multiples]]
- [[Factors]]
- [[Number of Factors]]
- [[Sum of Factors]]
- [[Product of Factors]]
- [[Factorization]]
- [[HCF]]
- [[LCM]]
- [[Divisibility Rules]]
- [[Remainders]]

---

# 37. Quick Revision

> [!summary] One-Minute Revision

### Definition

$$
\boxed{
N\text{ is a multiple of }a
\iff
N=ak
}
$$

### nth Multiple

$$
\boxed{an}
$$

### Count

$$
\boxed{
\left\lfloor\frac Na\right\rfloor
}
$$

### Range

$$
\boxed{
\left\lfloor\frac Ba\right\rfloor
-
\left\lfloor\frac{A-1}{a}\right\rfloor
}
$$

### Common Multiples

$$
\boxed{\operatorname{LCM}}
$$

### Sum

$$
\boxed{
\frac{an(n+1)}2
}
$$

### Key Pattern

> **Factors divide a number. Multiples are generated from a number.**

### Golden Connection

$$
\boxed{
\text{HCF}\rightarrow\text{Factors}
}
$$

$$
\boxed{
\text{LCM}\rightarrow\text{Multiples}
}
$$