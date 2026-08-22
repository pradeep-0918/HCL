---
type: concept
subject: aptitude
topic: "Remainder Theorem"
parent: "01. Number System/Remainders"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - remainders
  - remainder-theorem
  - polynomials
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Remainders]]"
  - "[[Basic Remainder]]"
  - "[[Large Number Remainders]]"
  - "[[Cyclic Remainders]]"
  - "[[Remainder Patterns]]"
---

# Remainder Theorem

## 1. Core Concept

> [!summary] Definition
> The **Remainder Theorem** is used to find the remainder when a polynomial is divided by a linear expression of the form:
>
> $$x-a$$
>
> without performing the complete division.

If:

$$
P(x)
$$

is divided by:

$$
x-a
$$

then the remainder is:

$$
\boxed{P(a)}
$$

---

# 2. Main Formula

If:

$$
P(x)
$$

is divided by:

$$
x-a
$$

then:

$$
\boxed{\text{Remainder}=P(a)}
$$

### Golden Rule

> **Replace `x` by `a`.**

---

# 3. Basic Example

Find the remainder when:

$$
P(x)=x^2+3x+5
$$

is divided by:

$$
x-2
$$

Since the divisor is:

$$
x-2
$$

we have:

$$
a=2
$$

Therefore:

$$
P(2)=2^2+3(2)+5
$$

$$
=4+6+5
$$

$$
=15
$$

Therefore:

$$
\boxed{15}
$$

---

# 4. Why Does It Work?

By the division algorithm:

$$
P(x)=(x-a)Q(x)+R
$$

where `R` is the remainder.

Since the divisor has degree `1`, the remainder must be a constant.

Put:

$$
x=a
$$

Then:

$$
P(a)=(a-a)Q(a)+R
$$

Since:

$$
a-a=0
$$

we get:

$$
P(a)=R
$$

Therefore:

$$
\boxed{R=P(a)}
$$

---

# 5. Most Important Pattern

> [!important] Memorize

If divisor is:

$$
\boxed{x-a}
$$

then:

$$
\boxed{\text{Remainder}=P(a)}
$$

### Example

Divisor:

$$
x-5
$$

Then:

$$
\boxed{x=5}
$$

Evaluate:

$$
P(5)
$$

---

# 6. Negative Sign Trap

This is one of the most common mistakes.

If the divisor is:

$$
x+3
$$

rewrite it as:

$$
x-(-3)
$$

Therefore:

$$
\boxed{a=-3}
$$

So the remainder is:

$$
\boxed{P(-3)}
$$

---

# 7. Example — Negative Value

Find the remainder when:

$$
P(x)=x^3+2x^2-x+4
$$

is divided by:

$$
x+2
$$

Rewrite:

$$
x+2=x-(-2)
$$

Therefore:

$$
a=-2
$$

Evaluate:

$$
P(-2)
$$

$$
=(-2)^3+2(-2)^2-(-2)+4
$$

$$
=-8+8+2+4
$$

$$
=6
$$

Therefore:

$$
\boxed{6}
$$

---

# 8. Fast Sign Recognition

| Divisor | Substitute |
|---|---:|
| `x - 2` | `2` |
| `x - 5` | `5` |
| `x + 3` | `-3` |
| `x + 7` | `-7` |
| `x - 10` | `10` |
| `x + 10` | `-10` |

> [!tip] Memory Trick
>
> **Change the sign of the constant.**

---

# 9. Example — Quadratic Polynomial

Find the remainder when:

$$
P(x)=2x^2-5x+7
$$

is divided by:

$$
x-3
$$

Substitute:

$$
x=3
$$

Therefore:

$$
P(3)=2(3)^2-5(3)+7
$$

$$
=18-15+7
$$

$$
=10
$$

Therefore:

$$
\boxed{10}
$$

---

# 10. Example — Cubic Polynomial

Find the remainder when:

$$
P(x)=x^3-4x^2+2x+9
$$

is divided by:

$$
x-2
$$

Substitute:

$$
x=2
$$

$$
P(2)=8-16+4+9
$$

$$
=5
$$

Therefore:

$$
\boxed{5}
$$

---

# 11. Example — Large Coefficients

Find the remainder when:

$$
P(x)=5x^4-3x^3+7x^2-8x+11
$$

is divided by:

$$
x-2
$$

Substitute:

$$
x=2
$$

$$
P(2)
=
5(2)^4-3(2)^3+7(2)^2-8(2)+11
$$

$$
=5(16)-3(8)+7(4)-16+11
$$

$$
=80-24+28-16+11
$$

$$
=79
$$

Therefore:

$$
\boxed{79}
$$

---

# 12. Remainder When Dividing by `x`

If:

$$
P(x)
$$

is divided by:

$$
x
$$

then:

$$
x=x-0
$$

Therefore:

$$
\boxed{\text{Remainder}=P(0)}
$$

### Example

$$
P(x)=3x^3+5x^2-7x+9
$$

Then:

$$
P(0)=9
$$

Therefore:

$$
\boxed{9}
$$

> [!important] Shortcut
>
> **Division by `x` → constant term is the remainder.**

---

# 13. Remainder When Dividing by `x+1`

Since:

$$
x+1=x-(-1)
$$

we substitute:

$$
x=-1
$$

Therefore:

$$
\boxed{\text{Remainder}=P(-1)}
$$

### Example

$$
P(x)=x^3+2x^2+4x+7
$$

Then:

$$
P(-1)
=
-1+2-4+7
$$

$$
=4
$$

Therefore:

$$
\boxed4
$$

---

# 14. Remainder When Dividing by `x-1`

For:

$$
x-1
$$

substitute:

$$
x=1
$$

Therefore:

$$
\boxed{
\text{Remainder}=P(1)
}
$$

### Example

$$
P(x)=x^4+3x^2-2x+5
$$

Then:

$$
P(1)=1+3-2+5
$$

$$
\boxed7
$$

---

# 15. Divisibility Test Using Remainder Theorem

This is extremely important.

If:

$$
P(a)=0
$$

then:

$$
x-a
$$

divides:

$$
P(x)
$$

exactly.

Therefore:

$$
\boxed{
P(a)=0
\iff
(x-a)\text{ is a factor of }P(x)
}
$$

---

# 16. Example — Check Whether `x-2` Is a Factor

Given:

$$
P(x)=x^3-3x^2+4
$$

Check whether:

$$
x-2
$$

is a factor.

Calculate:

$$
P(2)
=
2^3-3(2)^2+4
$$

$$
=8-12+4
$$

$$
=0
$$

Therefore:

$$
\boxed{x-2\text{ is a factor}}
$$

---

# 17. Example — Check Whether `x+3` Is a Factor

Given:

$$
P(x)=x^3-4x^2+5x+12
$$

Check:

$$
x+3
$$

Since:

$$
x+3=x-(-3)
$$

calculate:

$$
P(-3)
$$

$$
=-27-36-15+12
$$

$$
=-66
$$

Since:

$$
P(-3)\ne0
$$

therefore:

$$
\boxed{x+3\text{ is not a factor}}
$$

---

# 18. Factor Theorem Connection

> [!important] Factor Theorem

If:

$$
P(a)=0
$$

then:

$$
\boxed{x-a\text{ is a factor of }P(x)}
$$

The Factor Theorem is essentially a direct consequence of the Remainder Theorem.

### Relationship

$$
\boxed{
P(a)=\text{remainder when divided by }x-a
}
$$

Therefore:

$$
\boxed{
P(a)=0
\Rightarrow
x-a\text{ is a factor}
}
$$

---

# 19. Finding an Unknown Constant

This is a very common aptitude pattern.

Suppose:

$$
P(x)=x^2+kx+6
$$

leaves remainder `4` when divided by:

$$
x-2
$$

Find `k`.

By Remainder Theorem:

$$
P(2)=4
$$

Therefore:

$$
2^2+2k+6=4
$$

$$
4+2k+6=4
$$

$$
2k+10=4
$$

$$
2k=-6
$$

$$
\boxed{k=-3}
$$

---

# 20. General Unknown Constant Pattern

If:

$$
P(x)
$$

contains an unknown constant `k`, and the remainder is given when divided by:

$$
x-a
$$

then:

### Step 1

Set:

$$
x=a
$$

### Step 2

Use:

$$
P(a)=\text{given remainder}
$$

### Step 3

Solve for `k`.

Therefore:

$$
\boxed{
P(a)=r
}
$$

---

# 21. Example — Unknown Constant With Factor

Suppose:

$$
P(x)=x^3+kx^2+2x+5
$$

and:

$$
x-1
$$

is a factor.

Since it is a factor:

$$
P(1)=0
$$

Therefore:

$$
1+k+2+5=0
$$

$$
k+8=0
$$

Hence:

$$
\boxed{k=-8}
$$

---

# 22. Finding an Unknown Root

Suppose:

$$
P(x)=x^2-5x+k
$$

and:

$$
x-2
$$

is a factor.

Then:

$$
P(2)=0
$$

Therefore:

$$
4-10+k=0
$$

$$
k=6
$$

So:

$$
\boxed{k=6}
$$

---

# 23. Multiple Factors

If:

$$
P(x)
$$

has factors:

$$
x-a
$$

and:

$$
x-b
$$

then:

$$
\boxed{
P(a)=0
}
$$

and:

$$
\boxed{
P(b)=0
}
$$

This gives multiple equations that can be used to find unknown constants.

---

# 24. Example — Two Unknown Constants

Suppose:

$$
P(x)=x^3+ax^2+bx+6
$$

has factors:

$$
x-1
$$

and:

$$
x-2
$$

Then:

$$
P(1)=0
$$

and:

$$
P(2)=0
$$

### First equation

$$
1+a+b+6=0
$$

Therefore:

$$
a+b=-7
$$

### Second equation

$$
8+4a+2b+6=0
$$

$$
4a+2b=-14
$$

Divide by `2`:

$$
2a+b=-7
$$

Subtract:

$$
(2a+b)-(a+b)=0
$$

Therefore:

$$
a=0
$$

Then:

$$
b=-7
$$

So:

$$
\boxed{a=0,\quad b=-7}
$$

---

# 25. Remainder for a Polynomial Divided by `ax+b`

The standard theorem is usually written for:

$$
x-a
$$

But suppose the divisor is:

$$
ax+b
$$

Set:

$$
ax+b=0
$$

Therefore:

$$
x=-\frac ba
$$

So the remainder is:

$$
\boxed{
P\left(-\frac ba\right)
}
$$

---

# 26. Example — Divisor `2x+3`

Find the remainder when:

$$
P(x)=x^2+4x+5
$$

is divided by:

$$
2x+3
$$

Set divisor equal to zero:

$$
2x+3=0
$$

Therefore:

$$
x=-\frac32
$$

Now evaluate:

$$
P\left(-\frac32\right)
$$

$$
=
\left(-\frac32\right)^2
+
4\left(-\frac32\right)
+5
$$

$$
=\frac94-6+5
$$

$$
=\frac94-1
$$

$$
\boxed{\frac54}
$$

---

# 27. General Linear Divisor

For:

$$
ax+b
$$

the zero of the divisor is:

$$
\boxed{
x=-\frac ba
}
$$

Therefore:

$$
\boxed{
\text{Remainder}
=
P\left(-\frac ba\right)
}
$$

---

# 28. Remainder When Divisor Is `a-x`

Suppose divisor is:

$$
a-x
$$

Set:

$$
a-x=0
$$

Therefore:

$$
x=a
$$

So:

$$
\boxed{
\text{Remainder}=P(a)
}
$$

### Example

If divisor is:

$$
5-x
$$

then:

$$
x=5
$$

Therefore:

$$
\boxed{\text{Remainder}=P(5)}
$$

---

# 29. Polynomial Remainder vs Number Remainder

Do not confuse these two concepts.

### Number Remainder

For:

$$
N\div d
$$

we get:

$$
N=dq+r
$$

where `r` is a number.

### Polynomial Remainder

For:

$$
P(x)\div(x-a)
$$

we get:

$$
P(x)=(x-a)Q(x)+R
$$

where `R` is a constant.

---

# 30. Degree of the Remainder

If a polynomial of degree `n` is divided by a polynomial of degree `m`, then the remainder has degree:

$$
\boxed{<m}
$$

For a linear divisor:

$$
m=1
$$

therefore the remainder has degree:

$$
\boxed0
$$

So the remainder is a constant.

---

# 31. Important Pattern — Divisor `x-a`

Always:

$$
\boxed{
R=P(a)
}
$$

---

# 32. Important Pattern — Divisor `x+a`

Always:

$$
\boxed{
R=P(-a)
}
$$

---

# 33. Important Pattern — Divisor `ax+b`

Use:

$$
\boxed{
R=P\left(-\frac ba\right)
}
$$

---

# 34. Important Pattern — Factor Check

To check whether:

$$
x-a
$$

is a factor:

$$
\boxed{
P(a)=0
}
$$

---

# 35. Important Pattern — Unknown Constant

If remainder is `r`:

$$
\boxed{
P(a)=r
}
$$

Then solve for the unknown.

---

# 36. Important Pattern — Multiple Factors

If:

$$
x-a
$$

and:

$$
x-b
$$

are factors:

$$
\boxed{
P(a)=0,\quad P(b)=0
}
$$

Use both equations.

---

# 37. Shortcut — Sum of Coefficients

When dividing:

$$
P(x)
$$

by:

$$
x-1
$$

the remainder is:

$$
P(1)
$$

which is the **sum of the coefficients**.

### Example

$$
P(x)=2x^3+5x^2-3x+7
$$

Then:

$$
P(1)=2+5-3+7
$$

$$
\boxed{11}
$$

Therefore the remainder is:

$$
\boxed{11}
$$

---

# 38. Shortcut — Alternating Sum

When dividing:

$$
P(x)
$$

by:

$$
x+1
$$

the remainder is:

$$
P(-1)
$$

This produces an alternating sum of coefficients.

### Example

$$
P(x)=2x^3+5x^2-3x+7
$$

Then:

$$
P(-1)
=
-2+5+3+7
$$

$$
\boxed{13}
$$

---

# 39. Example — Sum of Coefficients

Find the remainder when:

$$
7x^4-3x^3+5x^2+2x-8
$$

is divided by:

$$
x-1
$$

Simply add coefficients:

$$
7-3+5+2-8
$$

$$
=3
$$

Therefore:

$$
\boxed3
$$

---

# 40. Example — Alternating Coefficients

Find the remainder when:

$$
7x^4-3x^3+5x^2+2x-8
$$

is divided by:

$$
x+1
$$

Substitute:

$$
x=-1
$$

$$
7+3+5-2-8
$$

$$
=5
$$

Therefore:

$$
\boxed5
$$

---

# 41. Remainder of `P(x)` Divided by `x-a`

If:

$$
P(x)=x^n+c
$$

then:

$$
\boxed{
R=a^n+c
}
$$

### Example

Find remainder of:

$$
x^{10}+7
$$

when divided by:

$$
x-2
$$

Simply:

$$
2^{10}+7
$$

$$
=1024+7
$$

$$
\boxed{1031}
$$

---

# 42. Remainder of `x^n`

For:

$$
P(x)=x^n
$$

divided by:

$$
x-a
$$

the remainder is:

$$
\boxed{a^n}
$$

### Example

$$
x^8\div(x-3)
$$

Remainder:

$$
\boxed{3^8}
$$

$$
=6561
$$

---

# 43. Remainder of Polynomial Products

Suppose:

$$
P(x)=A(x)B(x)
$$

and we divide by:

$$
x-a
$$

Then:

$$
P(a)=A(a)B(a)
$$

Therefore:

$$
\boxed{
R=A(a)B(a)
}
$$

This can make large expressions much easier.

---

# 44. Example — Product Form

Find the remainder when:

$$
(x^2+1)(x^3+2)
$$

is divided by:

$$
x-2
$$

Substitute:

$$
x=2
$$

First factor:

$$
2^2+1=5
$$

Second factor:

$$
2^3+2=10
$$

Therefore:

$$
R=5\times10
$$

$$
\boxed{50}
$$

No expansion is needed.

---

# 45. Remainder of Polynomial Powers

If:

$$
P(x)
$$

is divided by:

$$
x-a
$$

then:

$$
P(x)^n
$$

has remainder:

$$
\boxed{P(a)^n}
$$

### Example

Find the remainder when:

$$
(x^2+3)^5
$$

is divided by:

$$
x-2
$$

Evaluate:

$$
P(2)=2^2+3=7
$$

Therefore:

$$
R=7^5
$$

$$
\boxed{16807}
$$

---

# 46. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Substituting `a` when divisor is `x+a`.
- ❌ Forgetting to change the sign.
- ❌ Performing long division unnecessarily.
- ❌ Assuming the remainder is always `0`.
- ❌ Confusing Factor Theorem with Remainder Theorem.
- ❌ Forgetting that `x-a` means substitute `a`.
- ❌ For `ax+b`, forgetting to use `-b/a`.
- ❌ Expanding a large polynomial when direct substitution is easier.
- ❌ Forgetting that the remainder for a linear divisor is a constant.

---

# 47. Exam Strategy

> [!tip] Fast Method

### Divisor = `x-a`

Write immediately:

$$
\boxed{x=a}
$$

Then:

$$
\boxed{R=P(a)}
$$

### Divisor = `x+a`

Write:

$$
\boxed{x=-a}
$$

Then:

$$
\boxed{R=P(-a)}
$$

### Divisor = `ax+b`

Write:

$$
\boxed{x=-\frac ba}
$$

Then:

$$
\boxed{
R=P\left(-\frac ba\right)
}
$$

### Factor Question

If:

$$
x-a
$$

is claimed to be a factor:

$$
\boxed{P(a)=0}
$$

---

# 48. Formula Sheet

> [!important] Must Remember

### Remainder Theorem

$$
\boxed{
P(x)\div(x-a)
\Rightarrow
R=P(a)
}
$$

### Divisor `x+a`

$$
\boxed{
R=P(-a)
}
$$

### Divisor `ax+b`

$$
\boxed{
R=P\left(-\frac ba\right)
}
$$

### Divisor `x`

$$
\boxed{
R=P(0)
}
$$

### Factor Theorem

$$
\boxed{
P(a)=0
\iff
(x-a)\text{ is a factor}
}
$$

### Divisor `x-1`

$$
\boxed{
R=P(1)=\text{sum of coefficients}
}
$$

### Divisor `x+1`

$$
\boxed{
R=P(-1)=\text{alternating coefficient sum}
}
$$

---

# 49. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
x-a
\rightarrow
\boxed{x=a}
$$

### Pattern 2

$$
x+a
\rightarrow
\boxed{x=-a}
$$

### Pattern 3

$$
ax+b
\rightarrow
\boxed{x=-\frac ba}
$$

### Pattern 4

Factor check:

$$
\boxed{P(a)=0}
$$

### Pattern 5

Unknown constant:

$$
\boxed{P(a)=\text{given remainder}}
$$

### Pattern 6

Dividing by `x-1`:

$$
\boxed{\text{sum of coefficients}}
$$

### Pattern 7

Dividing by `x+1`:

$$
\boxed{\text{alternating sum of coefficients}}
$$

### Pattern 8

Polynomial product:

$$
\boxed{
P(x)Q(x)\div(x-a)
\rightarrow
P(a)Q(a)
}
$$

---

# 50. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

Master this because it gives a very fast method for polynomial remainder questions.

### Master These First

1. Basic Remainder Theorem
2. `x-a` substitution
3. `x+a` sign change
4. Factor Theorem connection
5. Unknown constant problems
6. `ax+b` divisor
7. Sum of coefficients
8. Alternating sum
9. Polynomial products
10. Polynomial powers

---

# 51. Practice Checklist

- [ ] Find remainder for `x-a`
- [ ] Find remainder for `x+a`
- [ ] Find remainder for `x`
- [ ] Find remainder for `ax+b`
- [ ] Check whether a polynomial has a factor
- [ ] Find unknown constants
- [ ] Find unknown coefficients
- [ ] Use sum of coefficients
- [ ] Use alternating sum
- [ ] Handle polynomial products
- [ ] Handle polynomial powers
- [ ] Practice factor/remainder mixed problems

---

# 52. Related Topics

- [[Remainders]]
- [[Basic Remainder]]
- [[Large Number Remainders]]
- [[Cyclic Remainders]]
- [[Remainder Patterns]]
- [[Factorization]]
- [[Factors]]
- [[Divisibility Rules]]

---

# 53. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
P(x)\div(x-a)
\Rightarrow
R=P(a)
}
$$

### Sign Rule

$$
x-a\rightarrow a
$$

$$
x+a\rightarrow -a
$$

### Linear Divisor

$$
ax+b=0
$$

so:

$$
\boxed{
x=-\frac ba
}
$$

### Factor Test

$$
\boxed{
P(a)=0
\Rightarrow
x-a\text{ is a factor}
}
$$

### `x-1`

$$
\boxed{
R=P(1)=\text{sum of coefficients}
}
$$

### `x+1`

$$
\boxed{
R=P(-1)=\text{alternating sum}
}
$$

### Golden Memory Trick

> **Set the divisor to zero, find the value of `x`, and substitute that value into the polynomial.**

### One-Line Recognition

> **Polynomial ÷ linear expression → set divisor = 0 → substitute into polynomial.**