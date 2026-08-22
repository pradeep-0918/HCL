---
type: concept
subject: aptitude
topic: "Basic Remainder"
parent: "01. Number System/Remainders"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - remainders
  - division
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Remainders]]"
  - "[[Divisibility Rules]]"
  - "[[HCF]]"
  - "[[LCM]]"
---

# Basic Remainder

## 1. Core Concept

> [!summary] Definition
> When an integer `N` is divided by a positive integer `d`, the **remainder** is the amount left after taking out as many complete groups of `d` as possible.

The fundamental division equation is:

$$
\boxed{
N=dq+r
}
$$

where:

- `N` = dividend
- `d` = divisor
- `q` = quotient
- `r` = remainder

The remainder always satisfies:

$$
\boxed{
0\le r<d
}
$$

---

# 2. Fundamental Formula

For any integer `N` divided by positive integer `d`:

$$
\boxed{
N=dq+r
}
$$

Therefore:

$$
\boxed{
r=N-dq
}
$$

If the quotient is known:

$$
\boxed{
r=N-(d\times q)
}
$$

---

# 3. Example

Find the remainder when:

$$
47
$$

is divided by:

$$
5
$$

We know:

$$
47=5\times9+2
$$

Therefore:

$$
\boxed{r=2}
$$

---

# 4. Parts of Division

For:

$$
47=5\times9+2
$$

we have:

| Term | Value |
|---|---:|
| Dividend | `47` |
| Divisor | `5` |
| Quotient | `9` |
| Remainder | `2` |

So:

$$
\boxed{
Dividend=Divisor\times Quotient+Remainder
}
$$

---

# 5. Most Important Rule

> [!important] Remainder Range

If the divisor is:

$$
d
$$

then the remainder must satisfy:

$$
\boxed{
0\le r<d
}
$$

### Example

If the divisor is `7`, possible remainders are:

$$
0,1,2,3,4,5,6
$$

Therefore:

$$
\boxed{r\in\{0,1,2,3,4,5,6\}}
$$

A remainder of `7` is impossible.

---

# 6. Remainder Cannot Equal Divisor

Suppose:

$$
N
$$

is divided by:

$$
8
$$

The remainder cannot be:

$$
8
$$

because:

$$
8=8\times1+0
$$

So an additional complete group can be taken.

Therefore:

$$
\boxed{
r<d
}
$$

---

# 7. Remainder Zero

If:

$$
N=dq
$$

then:

$$
r=0
$$

Therefore:

$$
\boxed{
N\text{ is exactly divisible by }d
}
$$

### Example

$$
36=6\times6+0
$$

Therefore:

$$
\boxed{36\bmod6=0}
$$

---

# 8. Remainder and Divisibility

A number is divisible by another number exactly when the remainder is zero.

Therefore:

$$
\boxed{
d\mid N
\iff
N\bmod d=0
}
$$

This is one of the most important connections between:

- Divisibility
- Remainders
- Factors

---

# 9. Remainder Notation

The remainder of `N` divided by `d` can be written as:

$$
\boxed{
N\bmod d
}
$$

### Example

$$
29\bmod6
$$

Since:

$$
29=6\times4+5
$$

we get:

$$
\boxed{29\bmod6=5}
$$

---

# 10. Basic Remainder Pattern

When the number is not very large:

### Step 1

Divide the number by the divisor.

### Step 2

Take the largest possible integer quotient.

### Step 3

Subtract:

$$
\boxed{
R=N-(D\times Q)
}
$$

---

# 11. Example

Find:

$$
83\bmod7
$$

Largest multiple of `7` below `83`:

$$
7\times11=77
$$

Therefore:

$$
83-77=6
$$

So:

$$
\boxed{83\bmod7=6}
$$

---

# 12. Remainder Using Nearest Multiple

Find:

$$
125\bmod9
$$

Nearest lower multiple:

$$
9\times13=117
$$

Therefore:

$$
125-117=8
$$

Hence:

$$
\boxed{8}
$$

---

# 13. If Number Is Smaller Than Divisor

If:

$$
N<d
$$

then the quotient is `0`.

Therefore:

$$
N=d(0)+N
$$

So:

$$
\boxed{N\bmod d=N}
$$

### Example

$$
5\bmod12=5
$$

---

# 14. If Number Equals Divisor

If:

$$
N=d
$$

then:

$$
N=d\times1+0
$$

Therefore:

$$
\boxed{N\bmod d=0}
$$

### Example

$$
8\bmod8=0
$$

---

# 15. Negative Remainders — Aptitude Convention

In standard aptitude problems, the remainder is generally taken as the **non-negative remainder**.

Therefore:

$$
\boxed{0\le r<d}
$$

For example:

$$
-3
$$

divided by `5` can be represented as:

$$
-3=5(-1)+2
$$

Therefore the standard non-negative remainder is:

$$
\boxed{2}
$$

> [!warning] Exam Tip
> Always use the non-negative remainder unless the question explicitly defines another convention.

---

# 16. Remainder of a Sum

If:

$$
a\equiv r_1\pmod d
$$

and:

$$
b\equiv r_2\pmod d
$$

then:

$$
\boxed{
(a+b)\bmod d
=
(r_1+r_2)\bmod d
}
$$

### Example

Find:

$$
(27+38)\bmod5
$$

First:

$$
27\bmod5=2
$$

$$
38\bmod5=3
$$

Then:

$$
(2+3)\bmod5=0
$$

Therefore:

$$
\boxed{0}
$$

---

# 17. Remainder of a Difference

Similarly:

$$
\boxed{
(a-b)\bmod d
=
(r_1-r_2)\bmod d
}
$$

where the final answer is converted to the standard range:

$$
0\le r<d
$$

### Example

Find:

$$
(47-23)\bmod6
$$

Remainders:

$$
47\bmod6=5
$$

$$
23\bmod6=5
$$

Therefore:

$$
5-5=0
$$

Hence:

$$
\boxed{0}
$$

---

# 18. Remainder of a Product

If:

$$
a\equiv r_1\pmod d
$$

and:

$$
b\equiv r_2\pmod d
$$

then:

$$
\boxed{
ab\bmod d
=
(r_1r_2)\bmod d
}
$$

### Example

Find:

$$
(17\times23)\bmod5
$$

Reduce first:

$$
17\bmod5=2
$$

$$
23\bmod5=3
$$

Then:

$$
2\times3=6
$$

Therefore:

$$
6\bmod5=1
$$

Hence:

$$
\boxed{1}
$$

---

# 19. Remainder of a Power

If:

$$
a\bmod d=r
$$

then:

$$
\boxed{
a^n\bmod d=r^n\bmod d
}
$$

This is extremely useful for large powers.

### Example

Find:

$$
7^3\bmod5
$$

Since:

$$
7\bmod5=2
$$

we calculate:

$$
2^3=8
$$

Therefore:

$$
8\bmod5=3
$$

Hence:

$$
\boxed{3}
$$

---

# 20. Remainder of a Polynomial Expression

Suppose:

$$
N=f(x)
$$

and we need:

$$
f(x)\bmod d
$$

First find:

$$
x\bmod d
$$

Then replace `x` by its remainder.

### Example

Find:

$$
(13^2+13+5)\bmod6
$$

Since:

$$
13\bmod6=1
$$

replace `13` with `1`:

$$
1^2+1+5
$$

$$
=7
$$

Therefore:

$$
7\bmod6=1
$$

Hence:

$$
\boxed{1}
$$

---

# 21. Important Property — Reduce Before Calculation

> [!important] Golden Rule

When calculating a remainder modulo `d`, you can replace a number by its remainder before performing:

- Addition
- Subtraction
- Multiplication
- Powers

In notation:

$$
\boxed{
a\equiv r\pmod d
}
$$

means `a` and `r` have the same remainder when divided by `d`.

---

# 22. Example — Large Multiplication

Find:

$$
1234\times5678\bmod7
$$

Reduce:

$$
1234\bmod7=2
$$

and:

$$
5678\bmod7=4
$$

Therefore:

$$
1234\times5678\bmod7
$$

becomes:

$$
2\times4=8
$$

Then:

$$
8\bmod7=1
$$

Therefore:

$$
\boxed{1}
$$

---

# 23. Remainder of a Sum of Many Numbers

For:

$$
a_1+a_2+\cdots+a_n
$$

we can calculate each remainder separately:

$$
\boxed{
(a_1+a_2+\cdots+a_n)\bmod d
=
(r_1+r_2+\cdots+r_n)\bmod d
}
$$

### Example

Find:

$$
17+29+41+56\bmod5
$$

Remainders:

$$
2+4+1+1
$$

$$
=8
$$

Therefore:

$$
8\bmod5=3
$$

Hence:

$$
\boxed{3}
$$

---

# 24. Remainder of a Product of Many Numbers

Similarly:

$$
\boxed{
(a_1a_2\cdots a_n)\bmod d
=
(r_1r_2\cdots r_n)\bmod d
}
$$

Reduce every number before multiplying.

This prevents very large intermediate values.

---

# 25. Important Zero Pattern

If any factor has remainder `0`, the entire product has remainder `0`.

If:

$$
a\bmod d=0
$$

then:

$$
ab\bmod d=0
$$

for any integer `b`.

Therefore:

$$
\boxed{
\text{One divisible factor → product divisible}
}
$$

### Example

$$
18\times37\bmod6
$$

Since:

$$
18\bmod6=0
$$

the answer is immediately:

$$
\boxed{0}
$$

---

# 26. Important One Pattern

If:

$$
a\bmod d=1
$$

then:

$$
a^n\bmod d=1
$$

for every positive integer `n`.

### Example

Since:

$$
11\bmod5=1
$$

then:

$$
11^{100}\bmod5=1
$$

Therefore:

$$
\boxed{1}
$$

---

# 27. Important Minus-One Pattern

If:

$$
a\bmod d=d-1
$$

then:

$$
a\equiv-1\pmod d
$$

Therefore:

$$
a^n\equiv(-1)^n\pmod d
$$

So:

### If `n` is even

$$
\boxed{a^n\bmod d=1}
$$

### If `n` is odd

$$
\boxed{a^n\bmod d=d-1}
$$

### Example

Find:

$$
9^{101}\bmod10
$$

Since:

$$
9\equiv-1\pmod{10}
$$

and `101` is odd:

$$
\boxed{9}
$$

---

# 28. Remainder and Quotient Relationship

From:

$$
N=dq+r
$$

we can derive:

$$
\boxed{
q=\frac{N-r}{d}
}
$$

and:

$$
\boxed{
r=N-dq
}
$$

This is useful when any two of the three quantities are known.

---

# 29. Finding the Number From Remainder

If a number gives quotient `q` and remainder `r` when divided by `d`, then:

$$
\boxed{
N=dq+r
}
$$

### Example

A number gives quotient `13` and remainder `4` when divided by `7`.

Then:

$$
N=7(13)+4
$$

$$
=91+4
$$

$$
\boxed{95}
$$

---

# 30. Finding the Divisor

Suppose:

$$
N=dq+r
$$

Then:

$$
d=\frac{N-r}{q}
$$

provided the result is a positive integer and:

$$
r<d
$$

### Example

A number is `95`, quotient is `13`, remainder is `4`.

Then:

$$
d=\frac{95-4}{13}
$$

$$
=\frac{91}{13}
$$

$$
\boxed7
$$

---

# 31. Finding the Quotient

Suppose:

$$
N=95
$$

is divided by:

$$
7
$$

with remainder:

$$
4
$$

Then:

$$
q=\frac{95-4}{7}
$$

$$
=\frac{91}{7}
$$

$$
\boxed{13}
$$

---

# 32. Remainder of a Number Plus a Multiple

If:

$$
N=dk+r
$$

then:

$$
\boxed{
N\bmod d=r
}
$$

Therefore adding any multiple of the divisor does not change the remainder.

### Example

Since:

$$
37\bmod5=2
$$

then:

$$
37+5(100)
$$

also has remainder:

$$
\boxed2
$$

---

# 33. Remainder Pattern

If:

$$
a\bmod d=r
$$

then:

$$
a+kd
$$

has the same remainder for every integer `k`.

Therefore:

$$
\boxed{
a,\ a+d,\ a+2d,\ a+3d,\ldots
}
$$

all have remainder `r` when divided by `d`.

---

# 34. Example — Same Remainder

Find the remainder of:

$$
47,\ 57,\ 67,\ 77
$$

when divided by `10`.

All end in `7`.

Therefore:

$$
\boxed7
$$

This is a simple example of numbers differing by multiples of the divisor.

---

# 35. Important Congruence Idea

When:

$$
a\bmod d=b\bmod d
$$

we can write:

$$
\boxed{
a\equiv b\pmod d
}
$$

This means:

$$
d\mid(a-b)
$$

Therefore:

$$
\boxed{
a-b\text{ is divisible by }d
}
$$

---

# 36. Example — Same Remainder

Consider:

$$
38,\ 53
$$

when divided by `5`.

$$
38\bmod5=3
$$

$$
53\bmod5=3
$$

Therefore:

$$
38\equiv53\pmod5
$$

and:

$$
53-38=15
$$

which is divisible by `5`.

---

# 37. Basic Remainder Pattern — Difference

If:

$$
a\equiv b\pmod d
$$

then:

$$
\boxed{
a-b\equiv0\pmod d
}
$$

Therefore:

$$
\boxed{
d\mid(a-b)
}
$$

This property becomes extremely important in later **Remainder Theorem** and **same-remainder** problems.

---

# 38. Remainder Pattern — Multiple of Divisor

If:

$$
N=dk+r
$$

then:

$$
\boxed{N\bmod d=r}
$$

So whenever a large number can be rewritten as:

$$
\text{multiple of divisor}+\text{small number}
$$

the small number is the remainder.

### Example

Find:

$$
1003\bmod10
$$

Write:

$$
1003=10(100)+3
$$

Therefore:

$$
\boxed3
$$

---

# 39. Remainder Pattern — Last Digit

For division by `10`, the remainder is the last digit.

$$
\boxed{
N\bmod10=\text{last digit of }N
}
$$

Examples:

$$
123\bmod10=3
$$

$$
4587\bmod10=7
$$

$$
920\bmod10=0
$$

This connects directly to the **Unit Digit** section later.

---

# 40. Remainder Pattern — Last Two Digits

For division by `100`, the remainder is determined by the last two digits.

$$
\boxed{
N\bmod100=\text{last two digits}
}
$$

### Example

$$
4587\bmod100=87
$$

Therefore:

$$
\boxed{87}
$$

---

# 41. Remainder Pattern — Last Three Digits

Similarly:

$$
\boxed{
N\bmod1000=\text{last three digits}
}
$$

### Example

$$
123456\bmod1000=456
$$

Therefore:

$$
\boxed{456}
$$

---

# 42. Remainder With Powers of 10

For:

$$
10^k
$$

the remainder is determined by the last `k` digits.

Therefore:

$$
\boxed{
N\bmod10^k
=
\text{last }k\text{ digits}
}
$$

Examples:

$$
N\bmod10
\rightarrow
\text{last digit}
$$

$$
N\bmod100
\rightarrow
\text{last two digits}
$$

$$
N\bmod1000
\rightarrow
\text{last three digits}
$$

---

# 43. Remainder and Factorization

If:

$$
N=ab
$$

and:

$$
a\mid d
$$

then the remainder of `N` modulo `d` may immediately become zero if the entire product contains enough factors of `d`.

### Example

Find:

$$
24\times35\bmod6
$$

Since:

$$
24\bmod6=0
$$

we immediately know:

$$
\boxed0
$$

---

# 44. Basic Remainder — Exam Method

> [!tip] Fast Method

When the numbers are small:

### Method 1

Perform ordinary division.

When the numbers are large:

### Method 2

Rewrite:

$$
N=\text{multiple of divisor}+r
$$

Then:

$$
\boxed{r=\text{answer}}
$$

When expressions are involved:

### Method 3

Reduce every component modulo the divisor first.

---

# 45. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Taking a remainder equal to the divisor.
- ❌ Forgetting that remainder must be non-negative.
- ❌ Using the quotient instead of the remainder.
- ❌ Forgetting to reduce the final answer again.
- ❌ Multiplying huge numbers before reducing them.
- ❌ Ignoring a factor with remainder `0`.
- ❌ Forgetting that numbers differing by a multiple of the divisor have the same remainder.
- ❌ Confusing remainder with divisibility.
- ❌ Forgetting that `N < d` means remainder is `N`.

---

# 46. Important Formula Sheet

> [!important] Must Remember

### Division Algorithm

$$
\boxed{
N=dq+r
}
$$

### Remainder

$$
\boxed{
r=N-dq
}
$$

### Quotient

$$
\boxed{
q=\frac{N-r}{d}
}
$$

### Remainder Range

$$
\boxed{
0\le r<d
}
$$

### Divisibility

$$
\boxed{
d\mid N\iff N\bmod d=0
}
$$

### Addition

$$
\boxed{
(a+b)\bmod d
=
[(a\bmod d)+(b\bmod d)]\bmod d
}
$$

### Subtraction

$$
\boxed{
(a-b)\bmod d
=
[(a\bmod d)-(b\bmod d)]\bmod d
}
$$

### Multiplication

$$
\boxed{
(ab)\bmod d
=
[(a\bmod d)(b\bmod d)]\bmod d
}
$$

### Power

$$
\boxed{
a^n\bmod d
=
[(a\bmod d)^n]\bmod d
}
$$

---

# 47. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Division Algorithm

$$
\boxed{
N=dq+r
}
$$

### Pattern 2 — Remainder Range

$$
\boxed{
0\le r<d
}
$$

### Pattern 3 — Exact Division

$$
\boxed{
r=0
}
$$

### Pattern 4 — Reduce Before Calculation

$$
\boxed{
a\rightarrow a\bmod d
}
$$

before calculating large expressions.

### Pattern 5 — Product

$$
\boxed{
ab\bmod d
=
[(a\bmod d)(b\bmod d)]\bmod d
}
$$

### Pattern 6 — Sum

$$
\boxed{
(a+b)\bmod d
=
[(a\bmod d)+(b\bmod d)]\bmod d
}
$$

### Pattern 7 — Same Remainder

$$
\boxed{
a\equiv b\pmod d
\Rightarrow
d\mid(a-b)
}
$$

### Pattern 8 — Powers of 10

$$
\boxed{
N\bmod10^k
=
\text{last }k\text{ digits}
}
$$

---

# 48. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

Basic remainder is the foundation for:

- Remainder Theorem
- Large number remainders
- Cyclic remainders
- Remainder patterns
- Unit digits
- Divisibility
- Modular arithmetic

### Master These First

1. Division algorithm
2. Remainder range
3. Exact divisibility
4. Modulo notation
5. Sum property
6. Difference property
7. Product property
8. Power property
9. Same-remainder property
10. Powers of `10`

---

# 49. Practice Checklist

- [ ] Find basic remainders
- [ ] Identify quotient and remainder
- [ ] Find missing number using `N = dq + r`
- [ ] Find missing divisor
- [ ] Find missing quotient
- [ ] Practice remainder of sums
- [ ] Practice remainder of differences
- [ ] Practice remainder of products
- [ ] Practice remainder of powers
- [ ] Practice same-remainder questions
- [ ] Practice modulo `10`, `100`, and `1000`
- [ ] Practice reducing large expressions

---

# 50. Related Topics

- [[Remainders]]
- [[Remainder Theorem]]
- [[Large Number Remainders]]
- [[Cyclic Remainders]]
- [[Remainder Patterns]]
- [[Divisibility Rules]]
- [[Unit Digit]]
- [[Last Digit]]
- [[Last Two Digits]]
- [[HCF]]
- [[LCM]]

---

# 51. Quick Revision

> [!summary] One-Minute Revision

### Fundamental Equation

$$
\boxed{
N=dq+r
}
$$

### Remainder Range

$$
\boxed{
0\le r<d
}
$$

### Exact Divisibility

$$
\boxed{
r=0
}
$$

### Sum

$$
\boxed{
(a+b)\bmod d
=
[(a\bmod d)+(b\bmod d)]\bmod d
}
$$

### Product

$$
\boxed{
ab\bmod d
=
[(a\bmod d)(b\bmod d)]\bmod d
}
$$

### Power

$$
\boxed{
a^n\bmod d
=
[(a\bmod d)^n]\bmod d
}
$$

### Same Remainder

$$
\boxed{
a\equiv b\pmod d
\iff
d\mid(a-b)
}
$$

### Last Digits

$$
\boxed{
N\bmod10^k
=
\text{last }k\text{ digits}
}
$$

### Golden Memory Trick

> **Divide → keep the quotient → whatever is left is the remainder.**

### One-Line Recognition

> **Remainder questions are about what is left after removing complete multiples of the divisor.**