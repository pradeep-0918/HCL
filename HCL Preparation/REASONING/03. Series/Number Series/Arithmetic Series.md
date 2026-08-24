---
type: concept
subject: reasoning
topic: "Arithmetic Series"
parent: "03. Series"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - reasoning
  - series
  - arithmetic-series
  - arithmetic-progression
  - ap
  - number-series
  - hcl
  - quantitative-reasoning
wikilinks:
  - "[[03. Series]]"
  - "[[Number Series]]"
  - "[[Missing Number Series]]"
  - "[[Wrong Number Series]]"
  - "[[Geometric Series]]"
  - "[[Mixed Pattern Series]]"
---

# Arithmetic Series

## 1. Core Concept

> [!summary]
> An **Arithmetic Series** in aptitude reasoning is a sequence in which the difference between every two consecutive terms remains constant.

Example:

$$
5,\ 9,\ 13,\ 17,\ 21
$$

Calculate the differences:

$$
9-5=4
$$

$$
13-9=4
$$

$$
17-13=4
$$

$$
21-17=4
$$

Therefore, the common difference is:

$$
\boxed{d=4}
$$

The sequence follows:

$$
\boxed{+4}
$$

### Core Intuition

Think:

> **"Every next number changes by the same amount."**

If the difference is constant, immediately think:

$$
\boxed{\text{Arithmetic Progression (AP)}}
$$

---

# 2. Basic Meaning

An arithmetic progression is a sequence:

$$
a,\ a+d,\ a+2d,\ a+3d,\ldots
$$

where:

- $a$ = first term
- $d$ = common difference
- $n$ = position of the term
- $a_n$ = $n$th term

### Example

$$
3,\ 7,\ 11,\ 15,\ 19
$$

Here:

$$
a=3
$$

and:

$$
d=4
$$

Therefore:

$$
a_n=3+(n-1)4
$$

---

# 3. Main Formula

## 3.1 Common Difference

The common difference is:

$$
\boxed{d=a_2-a_1}
$$

or generally:

$$
\boxed{d=a_n-a_{n-1}}
$$

---

## 3.2 nth Term

The most important formula is:

$$
\boxed{a_n=a+(n-1)d}
$$

where:

- $a$ = first term
- $n$ = term position
- $d$ = common difference

### Example

Find the 10th term of:

$$
4,\ 7,\ 10,\ 13,\ldots
$$

Here:

$$
a=4
$$

$$
d=3
$$

$$
n=10
$$

Therefore:

$$
a_{10}=4+(10-1)3
$$

$$
=4+27
$$

$$
=31
$$

Answer:

$$
\boxed{31}
$$

---

## 3.3 Sum of First n Terms

The sum of the first $n$ terms is:

$$
\boxed{S_n=\frac{n}{2}[2a+(n-1)d]}
$$

Another useful formula is:

$$
\boxed{S_n=\frac{n}{2}(a+l)}
$$

where:

- $a$ = first term
- $l$ = last term

---

## 3.4 Last Term

If the first term, number of terms, and common difference are known:

$$
\boxed{l=a+(n-1)d}
$$

---

## 3.5 Number of Terms

If first term, last term, and common difference are known:

$$
\boxed{n=\frac{l-a}{d}+1}
$$

This is extremely useful in aptitude questions.

---

# 4. Important Properties

### Property 1 — Constant Difference

In an AP:

$$
a_2-a_1=a_3-a_2=a_4-a_3
$$

Therefore:

$$
\boxed{\text{Difference is constant}}
$$

---

### Property 2 — Positive Difference

If:

$$
d>0
$$

the sequence is increasing.

Example:

$$
5,\ 8,\ 11,\ 14
$$

---

### Property 3 — Negative Difference

If:

$$
d<0
$$

the sequence is decreasing.

Example:

$$
20,\ 16,\ 12,\ 8
$$

---

### Property 4 — Zero Difference

If:

$$
d=0
$$

all terms are equal.

Example:

$$
7,\ 7,\ 7,\ 7
$$

---

### Property 5 — Middle Term Property

For three consecutive AP terms:

$$
a,\ b,\ c
$$

the middle term is the average of the other two:

$$
\boxed{2b=a+c}
$$

Therefore:

$$
\boxed{b=\frac{a+c}{2}}
$$

---

### Property 6 — Equidistant Terms

In an AP:

$$
a_n+a_{m}=a_p+a_q
$$

whenever:

$$
n+m=p+q
$$

This is useful for fast calculations.

---

### Property 7 — Average of AP

The average of the first and last terms is:

$$
\boxed{\text{Average}=\frac{a+l}{2}}
$$

For an AP, this is also the average of all terms.

---

### Property 8 — Terms Equally Spaced

Example:

$$
4,\ 8,\ 12,\ 16,\ 20
$$

The terms are equally spaced by:

$$
4
$$

---

# 5. Arithmetic Series vs Arithmetic Progression

These terms are often used interchangeably in aptitude questions, but mathematically they are different.

| Concept | Meaning |
|---|---|
| Arithmetic Progression | Sequence of terms |
| Arithmetic Series | Sum of terms of an AP |

### Example

AP:

$$
2,\ 5,\ 8,\ 11
$$

Arithmetic Series:

$$
2+5+8+11
$$

Therefore:

> [!important]
> **Sequence = AP**
>
> **Sum of sequence = Arithmetic Series**

In reasoning number-series questions, "arithmetic series" commonly refers to the constant-difference pattern.

---

# 6. Basic Examples

## Example 1 — Identify the Common Difference

### Question

Find the common difference:

$$
7,\ 12,\ 17,\ 22,\ 27
$$

### Calculation

$$
12-7=5
$$

$$
17-12=5
$$

$$
22-17=5
$$

$$
27-22=5
$$

Therefore:

$$
\boxed{d=5}
$$

### Pattern

$$
+5
$$

---

## Example 2 — Find the Next Term

### Question

$$
4,\ 9,\ 14,\ 19,\ ?
$$

### Pattern

$$
d=5
$$

Therefore:

$$
19+5=24
$$

### Answer

$$
\boxed{24}
$$

---

## Example 3 — Decreasing AP

### Question

$$
50,\ 44,\ 38,\ 32,\ ?
$$

### Pattern

$$
d=-6
$$

Therefore:

$$
32-6=26
$$

### Answer

$$
\boxed{26}
$$

---

## Example 4 — Zero Difference

### Question

$$
8,\ 8,\ 8,\ 8,\ ?
$$

Here:

$$
d=0
$$

Therefore:

$$
\boxed{8}
$$

---

# 7. Finding the nth Term

## Example 5

### Question

Find the 20th term:

$$
3,\ 7,\ 11,\ 15,\ldots
$$

### Step 1 — Identify Values

$$
a=3
$$

$$
d=4
$$

$$
n=20
$$

### Step 2 — Apply Formula

$$
a_n=a+(n-1)d
$$

$$
a_{20}=3+(20-1)4
$$

$$
=3+76
$$

$$
=79
$$

### Answer

$$
\boxed{79}
$$

---

## Example 6

### Question

Find the 15th term:

$$
20,\ 17,\ 14,\ 11,\ldots
$$

Here:

$$
a=20
$$

$$
d=-3
$$

$$
n=15
$$

Therefore:

$$
a_{15}=20+(15-1)(-3)
$$

$$
=20-42
$$

$$
=-22
$$

### Answer

$$
\boxed{-22}
$$

> [!important]
> A decreasing AP can cross zero and produce negative terms.

---

# 8. Finding the Number of Terms

## Example 7

### Question

How many terms are there in:

$$
5,\ 9,\ 13,\ldots, 101
$$

### Step 1

$$
a=5
$$

$$
d=4
$$

$$
l=101
$$

### Step 2

Use:

$$
n=\frac{l-a}{d}+1
$$

$$
n=\frac{101-5}{4}+1
$$

$$
=\frac{96}{4}+1
$$

$$
=24+1
$$

$$
=25
$$

### Answer

$$
\boxed{25\text{ terms}}
$$

---

## Example 8

### Question

How many terms are there in:

$$
100,\ 95,\ 90,\ldots, 5
$$

Here:

$$
a=100
$$

$$
d=-5
$$

$$
l=5
$$

Using:

$$
n=\frac{l-a}{d}+1
$$

$$
n=\frac{5-100}{-5}+1
$$

$$
=19+1
$$

$$
=20
$$

### Answer

$$
\boxed{20}
$$

---

# 9. Finding the Last Term

## Example 9

### Question

Find the last term of an AP where:

$$
a=6,\quad d=7,\quad n=12
$$

Use:

$$
l=a+(n-1)d
$$

$$
l=6+(12-1)7
$$

$$
=6+77
$$

$$
=83
$$

### Answer

$$
\boxed{83}
$$

---

# 10. Finding the First Term

Rearrange:

$$
a_n=a+(n-1)d
$$

Therefore:

$$
\boxed{a=a_n-(n-1)d}
$$

## Example 10

### Question

The 12th term of an AP is $50$ and the common difference is $3$. Find the first term.

Given:

$$
a_{12}=50
$$

$$
d=3
$$

Use:

$$
a=a_n-(n-1)d
$$

$$
a=50-(12-1)3
$$

$$
=50-33
$$

$$
=17
$$

### Answer

$$
\boxed{17}
$$

---

# 11. Finding the Common Difference

## Example 11

### Question

The first term is $8$ and the 10th term is $44$. Find $d$.

Use:

$$
a_n=a+(n-1)d
$$

$$
44=8+(10-1)d
$$

$$
44=8+9d
$$

$$
36=9d
$$

$$
d=4
$$

### Answer

$$
\boxed{4}
$$

---

# 12. Missing Term in an AP

## Example 12

### Question

Find the missing number:

$$
7,\ 11,\ ?,\ 19,\ 23
$$

### Pattern

Differences:

$$
+4
$$

Therefore:

$$
11+4=15
$$

Verify:

$$
15+4=19
$$

### Answer

$$
\boxed{15}
$$

---

## Example 13 — Middle Term Shortcut

### Question

Find $x$:

$$
12,\ x,\ 28
$$

Since these are consecutive AP terms:

$$
2x=12+28
$$

$$
2x=40
$$

$$
x=20
$$

### Answer

$$
\boxed{20}
$$

> [!tip]
> For three consecutive AP terms, immediately use:
>
> $$2b=a+c$$

---

# 13. Advanced AP Examples

## Example 14 — Three Consecutive AP Terms

### Question

Three consecutive AP terms have a sum of $48$. If the common difference is $4$, find the terms.

Let the terms be:

$$
x-4,\ x,\ x+4
$$

Their sum:

$$
(x-4)+x+(x+4)=48
$$

$$
3x=48
$$

$$
x=16
$$

Therefore:

$$
12,\ 16,\ 20
$$

### Answer

$$
\boxed{12,\ 16,\ 20}
$$

---

## Example 15 — Three Terms with Known Sum

### Question

Three consecutive AP terms have sum $60$ and common difference $5$. Find them.

Let:

$$
x-5,\ x,\ x+5
$$

Then:

$$
x-5+x+x+5=60
$$

$$
3x=60
$$

$$
x=20
$$

Therefore:

$$
15,\ 20,\ 25
$$

### Answer

$$
\boxed{15,\ 20,\ 25}
$$

---

## Example 16 — Sum of First n Terms

### Question

Find the sum:

$$
5+8+11+14+\ldots+50
$$

### Step 1 — Identify AP

$$
a=5
$$

$$
d=3
$$

$$
l=50
$$

### Step 2 — Find Number of Terms

$$
n=\frac{50-5}{3}+1
$$

$$
=\frac{45}{3}+1
$$

$$
=15+1
$$

$$
=16
$$

### Step 3 — Sum

$$
S_n=\frac{n}{2}(a+l)
$$

$$
S_{16}=\frac{16}{2}(5+50)
$$

$$
=8\times55
$$

$$
=440
$$

### Answer

$$
\boxed{440}
$$

---

# 14. Sum of First n Natural Numbers

A common special AP is:

$$
1,2,3,\ldots,n
$$

Here:

$$
a=1
$$

$$
d=1
$$

The sum is:

$$
\boxed{\frac{n(n+1)}{2}}
$$

### Example

Find:

$$
1+2+3+\cdots+100
$$

$$
S=\frac{100(101)}{2}
$$

$$
=5050
$$

### Answer

$$
\boxed{5050}
$$

---

# 15. Sum of First n Even Numbers

The first $n$ even numbers are:

$$
2,4,6,\ldots,2n
$$

Their sum is:

$$
\boxed{n(n+1)}
$$

### Example

Find:

$$
2+4+6+\cdots+20
$$

There are:

$$
n=10
$$

Therefore:

$$
S=10(11)
$$

$$
=110
$$

### Answer

$$
\boxed{110}
$$

---

# 16. Sum of First n Odd Numbers

The first $n$ odd numbers are:

$$
1,3,5,\ldots,(2n-1)
$$

Their sum is:

$$
\boxed{n^2}
$$

### Example

Find:

$$
1+3+5+\cdots+19
$$

The 10th odd number is:

$$
19
$$

Therefore:

$$
n=10
$$

$$
S=10^2
$$

$$
=100
$$

### Answer

$$
\boxed{100}
$$

---

# 17. Average of an AP

For an AP:

$$
\boxed{\text{Average}=\frac{a+l}{2}}
$$

This is one of the fastest formulas in aptitude.

## Example 17

### Question

Find the average of:

$$
7,\ 12,\ 17,\ 22,\ 27
$$

First term:

$$
a=7
$$

Last term:

$$
l=27
$$

Therefore:

$$
Average=\frac{7+27}{2}
$$

$$
=\frac{34}{2}
$$

$$
=17
$$

### Answer

$$
\boxed{17}
$$

---

# 18. Middle Term Shortcut

For an AP with an odd number of terms:

$$
\boxed{\text{Average}=\text{Middle Term}}
$$

### Example 18

Find the middle term of:

$$
10,\ 15,\ 20,\ 25,\ 30
$$

Middle term:

$$
\boxed{20}
$$

Also:

$$
\frac{10+30}{2}=20
$$

---

# 19. Equidistant Term Property

In an AP:

$$
a_1+a_n=a_2+a_{n-1}=a_3+a_{n-2}
$$

### Example 19

Consider:

$$
5,\ 9,\ 13,\ 17,\ 21
$$

Then:

$$
5+21=26
$$

$$
9+17=26
$$

$$
13+13=26
$$

Therefore:

$$
\boxed{\text{Equidistant terms have the same sum}}
$$

---

# 20. Advanced Placement Pattern — Find a Term Without Listing

## Example 20

### Question

Find the 25th term of:

$$
7,\ 12,\ 17,\ 22,\ldots
$$

Do not list all terms.

Use:

$$
a_n=a+(n-1)d
$$

Here:

$$
a=7
$$

$$
d=5
$$

$$
n=25
$$

Therefore:

$$
a_{25}=7+24(5)
$$

$$
=7+120
$$

$$
=127
$$

### Answer

$$
\boxed{127}
$$

> [!tip]
> Never manually generate all terms when the nth-term formula can solve the problem directly.

---

# 21. Advanced Placement Pattern — Which Term?

## Example 21

### Question

Which term of the AP

$$
5,\ 9,\ 13,\ 17,\ldots
$$

is $101$?

Given:

$$
a=5
$$

$$
d=4
$$

$$
a_n=101
$$

Use:

$$
101=5+(n-1)4
$$

$$
96=4(n-1)
$$

$$
24=n-1
$$

$$
n=25
$$

### Answer

$$
\boxed{101\text{ is the 25th term}}
$$

---

# 22. Advanced Placement Pattern — Is a Number in the AP?

## Example 22

### Question

Is $100$ a term of:

$$
4,\ 9,\ 14,\ 19,\ldots
$$

Here:

$$
a=4
$$

$$
d=5
$$

For $100$ to be a term:

$$
100=4+(n-1)5
$$

$$
96=5(n-1)
$$

$$
n-1=19.2
$$

This is not an integer.

Therefore:

$$
\boxed{100\text{ is not a term}}
$$

### Fast Method

Calculate:

$$
\frac{100-4}{5}=19.2
$$

Since the result is not an integer:

$$
\boxed{\text{Not in AP}}
$$

---

# 23. Advanced Placement Pattern — Sum Between Two Terms

## Example 23

### Question

Find the sum of all terms from $10$ to $50$ in the AP:

$$
2,\ 6,\ 10,\ 14,\ldots
$$

### Step 1 — Identify AP

$$
a=2
$$

$$
d=4
$$

### Step 2 — Find Position of 10

$$
10=2+(n-1)4
$$

$$
8=4(n-1)
$$

$$
n=3
$$

### Step 3 — Find Position of 50

$$
50=2+(n-1)4
$$

$$
48=4(n-1)
$$

$$
n=13
$$

### Step 4 — Number of Terms

$$
13-3+1=11
$$

### Step 5 — Sum

$$
S=\frac{11}{2}(10+50)
$$

$$
=\frac{11}{2}(60)
$$

$$
=330
$$

### Answer

$$
\boxed{330}
$$

---

# 24. Arithmetic Series Recognition

## How to Recognize

> [!important]
> If the difference between consecutive numbers is constant, immediately think **Arithmetic Progression**.

### Example

$$
11,\ 17,\ 23,\ 29,\ 35
$$

Differences:

$$
+6,+6,+6,+6
$$

Therefore:

$$
\boxed{\text{AP with }d=6}
$$

---

## What If the Difference Is Negative?

Example:

$$
40,\ 34,\ 28,\ 22,\ 16
$$

Differences:

$$
-6,-6,-6,-6
$$

Still an AP.

Therefore:

$$
\boxed{d=-6}
$$

---

## What If the Difference Is Zero?

Example:

$$
8,\ 8,\ 8,\ 8
$$

Then:

$$
\boxed{d=0}
$$

---

# 25. Shortcuts

> [!tip]
> **Shortcut 1 — Three-Term AP**

For:

$$
a,\ b,\ c
$$

if they are consecutive AP terms:

$$
\boxed{2b=a+c}
$$

This is faster than calculating $d$.

---

> [!tip]
> **Shortcut 2 — Average of AP**

For any AP:

$$
\boxed{Average=\frac{First+Last}{2}}
$$

You do not need to add every term.

---

> [!tip]
> **Shortcut 3 — Sum of AP**

Use:

$$
\boxed{S_n=\frac{n}{2}(First+Last)}
$$

when first, last, and number of terms are known.

---

> [!tip]
> **Shortcut 4 — Find Number of Terms**

Use:

$$
\boxed{n=\frac{Last-First}{d}+1}
$$

Do not count terms manually.

---

> [!tip]
> **Shortcut 5 — Find a Middle Term**

For equally spaced terms:

$$
\boxed{Middle=\frac{First+Last}{2}}
$$

when the endpoints are equally distant from the middle.

---

> [!tip]
> **Shortcut 6 — Check AP Membership**

To check whether $x$ belongs to an AP:

$$
\boxed{\frac{x-a}{d}}
$$

If the result is a non-negative integer, $x$ is a term of the AP.

---

> [!tip]
> **Shortcut 7 — Equidistant Terms**

In an AP:

$$
\boxed{a_i+a_j=\text{constant}}
$$

when the positions are equally distant from the ends.

---

# 26. Recognition Tricks

## Pattern 1 — Constant Difference

> [!important]
> If:

$$
a_2-a_1=a_3-a_2=a_4-a_3
$$

think:

$$
\boxed{\text{Arithmetic Progression}}
$$

---

## Pattern 2 — Increasing Sequence

> [!important]
> If numbers increase by the same amount:

$$
5,\ 10,\ 15,\ 20
$$

think:

$$
+5
$$

---

## Pattern 3 — Decreasing Sequence

> [!important]
> If numbers decrease by the same amount:

$$
30,\ 25,\ 20,\ 15
$$

think:

$$
-5
$$

---

## Pattern 4 — Missing Middle Term

> [!important]
> If three terms form an AP:

$$
a,\ x,\ c
$$

use:

$$
\boxed{x=\frac{a+c}{2}}
$$

---

## Pattern 5 — Find nth Term

> [!important]
> If the question asks:

> "What is the 20th term?"

immediately use:

$$
\boxed{a_n=a+(n-1)d}
$$

---

## Pattern 6 — Find Number of Terms

> [!important]
> If the question asks:

> "How many terms are there?"

and first, last, and difference are known:

$$
\boxed{n=\frac{l-a}{d}+1}
$$

---

## Pattern 7 — Sum

> [!important]
> If the question asks for the sum:

$$
a+(a+d)+(a+2d)+\cdots+l
$$

think:

$$
\boxed{S_n=\frac{n}{2}(a+l)}
$$

---

## Pattern 8 — Is Number Present?

> [!important]
> To check whether $x$ occurs in an AP:

$$
\boxed{\frac{x-a}{d}}
$$

must be a non-negative integer.

---

## Pattern 9 — Average

> [!important]
> If an AP's first and last terms are known:

$$
\boxed{Average=\frac{a+l}{2}}
$$

---

## Pattern 10 — Three Consecutive Terms

> [!important]
> If three consecutive AP terms are required, use:

$$
\boxed{x-d,\ x,\ x+d}
$$

This representation is often faster in algebra problems.

---

# 27. Common Exam Patterns

> [!important] Must Master

### Series Recognition

1. Identify an AP
2. Find common difference
3. Find next term
4. Find previous term
5. Find missing term
6. Find wrong term

### Term-Based Questions

7. Find nth term
8. Find first term
9. Find last term
10. Find common difference
11. Find number of terms
12. Find which term contains a given number
13. Check whether a number belongs to the AP

### Sum-Based Questions

14. Sum of first $n$ terms
15. Sum between two terms
16. Sum of consecutive AP terms
17. Average of AP terms
18. Sum using first and last term

### Special APs

19. Natural numbers
20. Even numbers
21. Odd numbers
22. Multiples of a number
23. Consecutive integers
24. Decreasing AP
25. Negative-difference AP

### Algebraic AP Problems

26. Three consecutive AP terms
27. Four consecutive AP terms
28. Sum of consecutive AP terms
29. Given nth term
30. Given two terms and find another term
31. Find $a$, $d$, or $n$
32. AP membership problems

---

# 28. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Confusing AP with GP

AP:

$$
2,\ 5,\ 8,\ 11
$$

uses constant **difference**.

GP:

$$
2,\ 6,\ 18,\ 54
$$

uses constant **ratio**.

Do not confuse them.

---

### Mistake 2 — Forgetting $(n-1)$

The nth-term formula is:

$$
a_n=a+(n-1)d
$$

not:

$$
a_n=a+nd
$$

---

### Mistake 3 — Ignoring negative difference

For:

$$
20,\ 17,\ 14
$$

the common difference is:

$$
\boxed{-3}
$$

not $3$.

---

### Mistake 4 — Using the sum formula without finding n

For:

$$
S_n=\frac{n}{2}(a+l)
$$

you need the number of terms.

If $n$ is unknown, calculate:

$$
n=\frac{l-a}{d}+1
$$

---

### Mistake 5 — Counting terms manually

For a large AP, never count one by one.

Use:

$$
\boxed{n=\frac{l-a}{d}+1}
$$

---

### Mistake 6 — Forgetting that the common difference can be zero

$$
5,\ 5,\ 5,\ 5
$$

is still an AP with:

$$
d=0
$$

---

### Mistake 7 — Treating every increasing sequence as AP

Example:

$$
1,\ 4,\ 9,\ 16
$$

is increasing, but differences are:

$$
3,5,7
$$

Therefore it is not an AP.

It is a square-number sequence.

---

### Mistake 8 — Using average formula for a non-AP

The shortcut:

$$
\frac{First+Last}{2}
$$

is the average of the terms when the terms are equally spaced.

Do not blindly use it for arbitrary sequences.

---

# 29. Formula Sheet

## Common Difference

$$
\boxed{d=a_n-a_{n-1}}
$$

## nth Term

$$
\boxed{a_n=a+(n-1)d}
$$

## Last Term

$$
\boxed{l=a+(n-1)d}
$$

## First Term

$$
\boxed{a=l-(n-1)d}
$$

## Number of Terms

$$
\boxed{n=\frac{l-a}{d}+1}
$$

## Sum of First n Terms

$$
\boxed{S_n=\frac{n}{2}[2a+(n-1)d]}
$$

## Sum Using First and Last

$$
\boxed{S_n=\frac{n}{2}(a+l)}
$$

## Average

$$
\boxed{Average=\frac{a+l}{2}}
$$

## Three Consecutive Terms

$$
\boxed{x-d,\ x,\ x+d}
$$

## Middle Term

$$
\boxed{2b=a+c}
$$

## AP Membership

$$
\boxed{n=\frac{x-a}{d}+1}
$$

where $n$ must be a positive integer.

## Sum of First n Natural Numbers

$$
\boxed{\frac{n(n+1)}{2}}
$$

## Sum of First n Even Numbers

$$
\boxed{n(n+1)}
$$

## Sum of First n Odd Numbers

$$
\boxed{n^2}
$$

---

# 30. Quick Revision

> [!summary] One-Minute Revision

## Arithmetic Series / AP

An AP has a **constant common difference**.

### Recognition

$$
\boxed{a_2-a_1=a_3-a_2=a_4-a_3}
$$

### Most Important Formula

$$
\boxed{a_n=a+(n-1)d}
$$

### Sum

$$
\boxed{S_n=\frac{n}{2}(a+l)}
$$

### Number of Terms

$$
\boxed{n=\frac{l-a}{d}+1}
$$

### Average

$$
\boxed{Average=\frac{a+l}{2}}
$$

### Three Consecutive Terms

$$
\boxed{x-d,\ x,\ x+d}
$$

### Special Sums

Natural numbers:

$$
\boxed{\frac{n(n+1)}{2}}
$$

Even numbers:

$$
\boxed{n(n+1)}
$$

Odd numbers:

$$
\boxed{n^2}
$$

### Fast Decision

If the difference is constant:

$$
\boxed{\text{AP}}
$$

If the ratio is constant:

$$
\boxed{\text{GP}}
$$

If neither is constant:

$$
\boxed{\text{Check another pattern}}
$$

### Golden Memory Trick

**"AP means Add the same amount every time."**

# One-Line Recognition

**If consecutive terms have a constant difference, immediately identify an Arithmetic Progression and use the AP formulas for terms, sums, averages, and missing values.**