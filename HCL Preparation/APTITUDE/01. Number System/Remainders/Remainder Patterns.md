---
type: concept
subject: aptitude
topic: "Remainder Patterns"
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
  - remainder-patterns
  - modular-arithmetic
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Remainders]]"
  - "[[Basic Remainder]]"
  - "[[Remainder Theorem]]"
  - "[[Large Number Remainders]]"
  - "[[Cyclic Remainders]]"
---

# Remainder Patterns

## 1. Core Concept

> [!summary] Main Idea
> Remainder problems become easy when you recognize a repeating or algebraic pattern instead of calculating the complete number.

The most important idea is:

$$
\boxed{
\text{Simplify the expression modulo the divisor}
}
$$

Instead of calculating a huge expression directly, identify a useful pattern.

---

# 2. Pattern — Reduce Every Number

For modulus `m`:

$$
\boxed{
a\equiv a\bmod m
}
$$

Therefore:

$$
a\rightarrow r
$$

where:

$$
r=a\bmod m
$$

Then perform the calculation using `r`.

### Example

Find:

$$
1234\times5678\bmod9
$$

Since:

$$
1234\bmod9=1
$$

and:

$$
5678\bmod9=8
$$

then:

$$
1\times8=8
$$

Therefore:

$$
\boxed8
$$

---

# 3. Pattern — Sum of Remainders

For:

$$
a+b+c
$$

we can write:

$$
\boxed{
(a+b+c)\bmod m
=
[(a\bmod m)+(b\bmod m)+(c\bmod m)]\bmod m
}
$$

### Example

Find:

$$
123+456+789\bmod7
$$

Remainders:

$$
123\bmod7=4
$$

$$
456\bmod7=1
$$

$$
789\bmod7=5
$$

Therefore:

$$
4+1+5=10
$$

$$
10\bmod7=3
$$

Answer:

$$
\boxed3
$$

---

# 4. Pattern — Difference of Remainders

For:

$$
a-b
$$

use:

$$
\boxed{
(a-b)\bmod m
=
[(a\bmod m)-(b\bmod m)]\bmod m
}
$$

If the intermediate result is negative, add `m`.

### Example

Find:

$$
23-41\bmod7
$$

Remainders:

$$
23\bmod7=2
$$

$$
41\bmod7=6
$$

Therefore:

$$
2-6=-4
$$

Add `7`:

$$
-4+7=3
$$

Therefore:

$$
\boxed3
$$

---

# 5. Pattern — Product of Remainders

For:

$$
abc
$$

use:

$$
\boxed{
abc\bmod m
=
[(a\bmod m)(b\bmod m)(c\bmod m)]\bmod m
}
$$

### Example

Find:

$$
17\times24\times35\bmod5
$$

Remainders:

$$
17\rightarrow2
$$

$$
24\rightarrow4
$$

$$
35\rightarrow0
$$

Since one factor has remainder `0`:

$$
\boxed0
$$

---

# 6. Pattern — Zero Factor

If any factor is divisible by the divisor:

$$
a\equiv0\pmod m
$$

then:

$$
\boxed{
abc\equiv0\pmod m
}
$$

This is one of the fastest shortcuts.

### Example

Find:

$$
123\times456\times789\bmod3
$$

Since:

$$
123\bmod3=0
$$

the answer is immediately:

$$
\boxed0
$$

No further calculation is needed.

---

# 7. Pattern — Remainder `1`

If:

$$
a\equiv1\pmod m
$$

then:

$$
a^n\equiv1^n
$$

Therefore:

$$
\boxed{
a^n\equiv1\pmod m
}
$$

### Example

Find:

$$
31^{1000}\bmod10
$$

Since:

$$
31\bmod10=1
$$

therefore:

$$
\boxed1
$$

---

# 8. Pattern — Remainder `-1`

If:

$$
a\equiv-1\pmod m
$$

then:

$$
a^n\equiv(-1)^n\pmod m
$$

Therefore:

### Even power

$$
\boxed1
$$

### Odd power

$$
\boxed{m-1}
$$

### Example

Find:

$$
19^{2026}\bmod20
$$

Since:

$$
19\equiv-1\pmod{20}
$$

and `2026` is even:

$$
\boxed1
$$

---

# 9. Pattern — Powers

For:

$$
a^n\bmod m
$$

first reduce:

$$
a\bmod m
$$

Then calculate the power of the smaller number.

$$
\boxed{
a^n\bmod m
=
[(a\bmod m)^n]\bmod m
}
$$

### Example

Find:

$$
17^{20}\bmod6
$$

Since:

$$
17\bmod6=5
$$

we need:

$$
5^{20}\bmod6
$$

Since:

$$
5\equiv-1\pmod6
$$

and `20` is even:

$$
\boxed1
$$

---

# 10. Pattern — Difference From a Multiple

If:

$$
N=kd+r
$$

then:

$$
\boxed{
N\bmod d=r
}
$$

This is useful when the number is close to a convenient multiple.

### Example

Find:

$$
9998\bmod10
$$

Write:

$$
9998=10000-2
$$

Therefore:

$$
9998\equiv-2\pmod{10}
$$

Convert to standard remainder:

$$
-2+10=8
$$

Hence:

$$
\boxed8
$$

---

# 11. Pattern — Same Remainder

If:

$$
a\equiv b\pmod m
$$

then:

$$
\boxed{
m\mid(a-b)
}
$$

Therefore, numbers having the same remainder differ by a multiple of the divisor.

### Example

`47` and `82` both leave remainder `2` when divided by `5`.

Indeed:

$$
82-47=35
$$

and:

$$
5\mid35
$$

---

# 12. Pattern — HCF of Differences

If several numbers leave the same remainder when divided by `d`, then `d` divides all their pairwise differences.

Therefore the greatest possible divisor is:

$$
\boxed{
HCF(\text{differences})
}
$$

### Example

Find the greatest divisor that leaves the same remainder for:

$$
43,\ 67,\ 91
$$

Differences:

$$
67-43=24
$$

$$
91-67=24
$$

Therefore:

$$
HCF(24,24)=24
$$

Answer:

$$
\boxed{24}
$$

---

# 13. Pattern — Same Remainder + Smallest Number

If `N` leaves the same remainder `r` when divided by:

$$
a,b,c
$$

then:

$$
N-r
$$

is divisible by all three.

Therefore:

$$
\boxed{
N=LCM(a,b,c)+r
}
$$

### Example

Find the smallest number that leaves remainder `4` when divided by:

$$
5,\ 6,\ 8
$$

First:

$$
LCM(5,6,8)=120
$$

Therefore:

$$
N=120+4
$$

$$
\boxed{124}
$$

---

# 14. Pattern — Powers of 10

For:

$$
10^k
$$

only the last `k` digits matter.

$$
\boxed{
N\bmod10^k
=
\text{last }k\text{ digits}
}
$$

### Examples

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

# 15. Pattern — Modulo 3

For any number:

$$
N
$$

the remainder modulo `3` can be found using the digit sum.

$$
\boxed{
N\bmod3
=
(\text{digit sum})\bmod3
}
$$

### Example

Find:

$$
987654\bmod3
$$

Digit sum:

$$
9+8+7+6+5+4=39
$$

Then:

$$
39\bmod3=0
$$

Therefore:

$$
\boxed0
$$

---

# 16. Pattern — Modulo 9

Similarly:

$$
\boxed{
N\bmod9
=
(\text{digit sum})\bmod9
}
$$

### Example

Find:

$$
123456789\bmod9
$$

Digit sum:

$$
1+2+3+4+5+6+7+8+9=45
$$

Then:

$$
45\bmod9=0
$$

Therefore:

$$
\boxed0
$$

---

# 17. Pattern — Modulo 11

For modulo `11`, use the alternating sum of digits.

$$
\boxed{
N\bmod11
\text{ can be obtained from the alternating digit sum}
}
$$

### Example

Find:

$$
123456\bmod11
$$

Take:

$$
(6-5+4-3+2-1)
$$

$$
=3
$$

Therefore:

$$
\boxed3
$$

---

# 18. Pattern — Unit Digit

For:

$$
N\bmod10
$$

only the last digit matters.

Therefore:

$$
\boxed{
N\bmod10=\text{last digit}
}
$$

### Example

$$
9876543\bmod10
$$

Answer:

$$
\boxed3
$$

---

# 19. Pattern — Last Two Digits

For:

$$
N\bmod100
$$

only the final two digits matter.

### Example

$$
12345678\bmod100
$$

Therefore:

$$
\boxed78
$$

---

# 20. Pattern — Last Three Digits

For:

$$
N\bmod1000
$$

only the final three digits matter.

### Example

$$
12345678\bmod1000
$$

Therefore:

$$
\boxed678
$$

---

# 21. Pattern — Cyclic Powers

When:

$$
a^n\bmod m
$$

has a repeating sequence, find the cycle.

### Example

For powers of `2` modulo `10`:

$$
2,4,8,6,\boxed{2,4,8,6,\ldots}
$$

Cycle length:

$$
4
$$

Therefore:

$$
\boxed{
\text{Exponent position}=n\bmod4
}
$$

If the result is `0`, use position `4`.

---

# 22. Pattern — Unit-Digit Cycle Length

For unit digits:

| Base last digit | Cycle length |
|---:|---:|
| `0` | 1 |
| `1` | 1 |
| `2` | 4 |
| `3` | 4 |
| `4` | 2 |
| `5` | 1 |
| `6` | 1 |
| `7` | 4 |
| `8` | 4 |
| `9` | 2 |

> [!important] Shortcut
>
> For unit digits, cycle lengths are only:
>
> $$\boxed{1,\ 2,\ 4}
> $$

---

# 23. Pattern — Nested Powers

For:

$$
a^{b^c}\bmod m
$$

do not calculate:

$$
b^c
$$

completely.

Instead:

### Step 1

Find the cycle length of `a` modulo `m`.

### Step 2

Find:

$$
b^c\bmod(\text{cycle length})
$$

### Step 3

Use that as the position in the outer cycle.

---

# 24. Example — Nested Power

Find the unit digit of:

$$
2^{3^{100}}
$$

Cycle of `2`:

$$
2,4,8,6
$$

Cycle length:

$$
4
$$

Now find:

$$
3^{100}\bmod4
$$

Since:

$$
3^2\equiv1\pmod4
$$

and `100` is even:

$$
3^{100}\equiv1\pmod4
$$

Therefore use position `1` in:

$$
2,4,8,6
$$

Answer:

$$
\boxed2
$$

---

# 25. Pattern — Factorial Remainders

Factorials often become `0` modulo a number once they contain all required prime factors.

### Example

Find:

$$
10!\bmod10
$$

Since:

$$
10!
$$

contains a factor `10`:

$$
10\mid10!
$$

Therefore:

$$
\boxed{10!\bmod10=0}
$$

---

# 26. Factorial Zero Pattern

For:

$$
n!\bmod m
$$

look for whether `n!` contains enough factors to make it divisible by `m`.

### Example

Find:

$$
20!\bmod12
$$

Since:

$$
12=2^2\times3
$$

and `20!` contains more than enough factors of `2` and `3`:

$$
12\mid20!
$$

Therefore:

$$
\boxed0
$$

> [!tip] Pattern
> For factorial questions, **factorize the modulus** and check whether the factorial contains enough prime factors.

---

# 27. Pattern — Polynomial Modulo

If:

$$
P(x)
$$

is evaluated modulo `m`, first reduce `x`.

### Example

Find:

$$
x^2+3x+5
$$

modulo `7` when:

$$
x\equiv2\pmod7
$$

Substitute:

$$
2^2+3(2)+5
$$

$$
=4+6+5
$$

$$
=15
$$

Therefore:

$$
15\bmod7=1
$$

Answer:

$$
\boxed1
$$

---

# 28. Pattern — Polynomial Remainder

If a polynomial:

$$
P(x)
$$

is divided by:

$$
x-a
$$

then:

$$
\boxed{
R=P(a)
}
$$

This is the **Remainder Theorem**.

### Example

Find the remainder when:

$$
x^3+2x+5
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
8+4+5=17
$$

Therefore:

$$
\boxed{17}
$$

---

# 29. Pattern — Divisor `x+ a`

For:

$$
x+a
$$

use:

$$
x=-a
$$

Therefore:

$$
\boxed{
R=P(-a)
}
$$

### Example

For divisor:

$$
x+3
$$

use:

$$
x=-3
$$

---

# 30. Pattern — Divisibility From Remainder

If:

$$
N\bmod d=0
$$

then:

$$
\boxed{
d\mid N
}
$$

If:

$$
N\bmod d\ne0
$$

then:

$$
\boxed{
d\nmid N
}
$$

This connects remainder questions directly to divisibility.

---

# 31. Pattern — Product Divisibility

If:

$$
a\equiv0\pmod m
$$

then:

$$
ab\equiv0\pmod m
$$

for any integer `b`.

But be careful:

If neither factor is individually divisible by `m`, their product may still be divisible by `m`.

### Example

$$
2\times3=6
$$

Neither `2` nor `3` is divisible by `6`, but:

$$
6\bmod6=0
$$

So:

> [!warning] Important
> A zero remainder from one factor is a quick sufficient condition, not the only possible way for a product to be divisible.

---

# 32. Pattern — Common Factor of Modulus

Suppose:

$$
m=ab
$$

and an expression contains enough factors of `a` and `b`.

Then the expression may be divisible by `m`.

This is especially useful with:

- factorials
- products
- prime factorization
- powers

---

# 33. Pattern — Negative Representation

A large remainder can often be simplified by using a negative equivalent.

For modulus `m`:

$$
m-1\equiv-1\pmod m
$$

$$
m-2\equiv-2\pmod m
$$

Therefore:

$$
\boxed{
m-k\equiv-k\pmod m
}
$$

### Example

Modulo `11`:

$$
10\equiv-1
$$

Therefore:

$$
10^{2026}\equiv(-1)^{2026}
$$

$$
\boxed1
$$

---

# 34. Pattern — Complement to a Multiple

If:

$$
a=m-r
$$

then:

$$
a\equiv-r\pmod m
$$

This is useful when `a` is close to the modulus.

### Example

Find:

$$
98^{50}\bmod100
$$

Since:

$$
98\equiv-2\pmod{100}
$$

therefore:

$$
98^{50}\equiv(-2)^{50}
$$

So:

$$
\boxed{
98^{50}\bmod100
=
2^{50}\bmod100
}
$$

Now use the last two digits/cycle of powers of `2`.

---

# 35. Pattern — Common Modulus

If several terms use the same modulus, reduce all of them using that modulus.

Example:

$$
A\bmod7,\quad B\bmod7,\quad C\bmod7
$$

Do not repeatedly perform full divisions.

Instead:

$$
A\rightarrow a
$$

$$
B\rightarrow b
$$

$$
C\rightarrow c
$$

Then calculate using:

$$
a,b,c
$$

---

# 36. Pattern — Remainder of a Quotient

If:

$$
N=dq+r
$$

then:

$$
\boxed{
q=\frac{N-r}{d}
}
$$

This is useful when a problem gives:

- dividend
- divisor
- remainder

and asks for the quotient.

---

# 37. Pattern — Count Numbers With a Given Remainder

Numbers leaving remainder `r` when divided by `d` have the form:

$$
\boxed{
N=dk+r
}
$$

where `k` is a non-negative integer.

Therefore:

$$
r,\ d+r,\ 2d+r,\ 3d+r,\ldots
$$

all have remainder `r`.

---

# 38. Example — Counting

How many numbers from `1` to `100` leave remainder `3` when divided by `7`?

Numbers are:

$$
3,10,17,\ldots,94
$$

This is an arithmetic progression.

Solve:

$$
7k+3\le100
$$

$$
7k\le97
$$

$$
k\le13
$$

Since:

$$
k=0,1,\ldots,13
$$

there are:

$$
\boxed{14}
$$

numbers.

---

# 39. Pattern — Common Remainder Representation

If:

$$
a,b,c
$$

all leave remainder `r` modulo `d`, then:

$$
\boxed{
a=dx+r
}
$$

$$
\boxed{
b=dy+r
}
$$

$$
\boxed{
c=dz+r
}
$$

Subtracting any two removes the remainder.

Therefore:

$$
\boxed{
d\mid(a-b)
}
$$

This is the foundation of many hidden HCF questions.

---

# 40. Pattern — Modular Equality

If:

$$
a\equiv b\pmod m
$$

then you may replace `a` with `b` inside modular addition, subtraction, multiplication, and powers.

For example:

$$
a\equiv b\pmod m
$$

implies:

$$
\boxed{
a^n\equiv b^n\pmod m
}
$$

---

# 41. Pattern — Exponent Reduction

If a cycle exists with length `k`:

$$
\boxed{
a^{n+k}\equiv a^n\pmod m
}
$$

Therefore large exponents can be reduced modulo the cycle length.

This is the foundation of:

- cyclic remainders
- unit digits
- large power questions

---

# 42. Pattern — Multiple Moduli

Sometimes the same number is described using different remainders:

$$
N\bmod a=r_1
$$

and:

$$
N\bmod b=r_2
$$

These are simultaneous congruences.

Such questions may require:

- substitution
- pattern search
- LCM
- modular arithmetic
- Chinese Remainder Theorem in advanced cases

> [!warning] Scope
> Do not force the simple `LCM + remainder` formula when the remainders are different.

---

# 43. Pattern — Divisor Larger Than Number

If:

$$
N<d
$$

then:

$$
\boxed{
N\bmod d=N
}
$$

### Example

$$
7\bmod20=7
$$

---

# 44. Pattern — Divisor Equals Number

If:

$$
N=d
$$

then:

$$
\boxed{
N\bmod d=0
}
$$

---

# 45. Pattern — Remainder Is Already Known

If:

$$
a\bmod m=r
$$

then:

$$
(a+km)\bmod m=r
$$

for any integer `k`.

Therefore:

$$
\boxed{
\text{Adding a multiple of the divisor does not change the remainder}
}
$$

---

# 46. Pattern — Subtracting a Multiple

Similarly:

$$
(a-km)\bmod m=r
$$

Therefore:

$$
\boxed{
\text{Adding or subtracting multiples of the modulus preserves the remainder}
}
$$

---

# 47. Master Pattern Table

| Pattern | Shortcut |
|---|---|
| Sum | Reduce each term |
| Difference | Reduce each term |
| Product | Reduce each factor |
| Power | Reduce base |
| Huge power | Find cycle |
| Same remainder | HCF of differences |
| Same remainder + smallest number | LCM + remainder |
| Mod `10` | Last digit |
| Mod `100` | Last two digits |
| Mod `1000` | Last three digits |
| Mod `3` | Digit sum |
| Mod `9` | Digit sum |
| Mod `11` | Alternating digit sum |
| Polynomial ÷ `x-a` | Substitute `a` |
| Divisor `x+a` | Substitute `-a` |
| Factor check | Evaluate polynomial = `0` |
| Factorial | Check prime factors |
| Remainder `0` | Divisible |
| Remainder `1` | Powers remain `1` |
| Remainder `-1` | Even → `1`, odd → `m-1` |

---

# 48. Formula Sheet

> [!important] Must Remember

### Division Algorithm

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

### Addition

$$
\boxed{
(a+b)\bmod m
=
[(a\bmod m)+(b\bmod m)]\bmod m
}
$$

### Multiplication

$$
\boxed{
ab\bmod m
=
[(a\bmod m)(b\bmod m)]\bmod m
}
$$

### Power

$$
\boxed{
a^n\bmod m
=
[(a\bmod m)^n]\bmod m
}
$$

### Same Remainder

$$
\boxed{
a\equiv b\pmod m
\iff
m\mid(a-b)
}
$$

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

### Remainder Theorem

$$
\boxed{
P(x)\div(x-a)
\Rightarrow
R=P(a)
}
$$

---

# 49. Exam Decision Tree

> [!tip] Fast Recognition

### Is it a simple number?

Use:

$$
\boxed{\text{Direct division}}
$$

### Is it a large sum/product?

Use:

$$
\boxed{\text{Reduce each term}}
$$

### Is it a huge power?

Use:

$$
\boxed{\text{Cyclicity}}
$$

### Is the divisor `10^k`?

Use:

$$
\boxed{\text{Last }k\text{ digits}}
$$

### Is the divisor `3` or `9`?

Use:

$$
\boxed{\text{Digit sum}}
$$

### Is the divisor `11`?

Use:

$$
\boxed{\text{Alternating digit sum}}
$$

### Same remainder for several numbers?

Use:

$$
\boxed{HCF\text{ of differences}}
$$

### Smallest number with same remainder?

Use:

$$
\boxed{LCM+r}
$$

### Polynomial divided by `x-a`?

Use:

$$
\boxed{P(a)}
$$

---

# 50. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Calculating huge numbers completely.
- ❌ Forgetting to reduce the final result.
- ❌ Using `LCM + r` for different remainders.
- ❌ Forgetting the `0 ≤ r < d` rule.
- ❌ Taking the first cycle element when exponent remainder is `0`.
- ❌ Confusing unit digit with general remainder.
- ❌ Using digit-sum rules for arbitrary divisors.
- ❌ Forgetting the sign change for `x+a`.
- ❌ Assuming a zero remainder from one factor is necessary for product divisibility.
- ❌ Applying `HCF × LCM = product` blindly to three numbers.

---

# 51. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

This topic is a **pattern-recognition chapter**. You should be able to identify the method within a few seconds.

### Master These First

1. Reduce before calculation
2. Sum/product remainder
3. `0`, `1`, `-1` patterns
4. Same remainder → HCF of differences
5. Same remainder → LCM + remainder
6. Cyclic powers
7. Unit-digit cycles
8. Digit-sum patterns
9. Last-digit patterns
10. Polynomial remainder
11. Factorial remainder
12. Negative-equivalent remainder

---

# 52. Practice Checklist

- [ ] Sum remainder
- [ ] Difference remainder
- [ ] Product remainder
- [ ] Power remainder
- [ ] Zero-remainder shortcut
- [ ] One-remainder shortcut
- [ ] Negative-one shortcut
- [ ] Same-remainder problems
- [ ] HCF of differences
- [ ] LCM + remainder
- [ ] Cyclic remainder
- [ ] Unit-digit cycle
- [ ] Digit-sum remainder
- [ ] Modulo `11`
- [ ] Last two/three digits
- [ ] Factorial remainder
- [ ] Polynomial remainder
- [ ] Nested powers

---

# 53. Related Topics

- [[Remainders]]
- [[Basic Remainder]]
- [[Remainder Theorem]]
- [[Large Number Remainders]]
- [[Cyclic Remainders]]
- [[Divisibility Rules]]
- [[Unit Digit]]
- [[Factors]]
- [[HCF]]
- [[LCM]]
- [[Factorization]]

---

# 54. Quick Revision

> [!summary] One-Minute Revision

### Golden Rule

$$
\boxed{
\text{Reduce first → calculate second}
}
$$

### Same Remainder

$$
\boxed{
a\equiv b\pmod m
\Rightarrow
m\mid(a-b)
}
$$

### Greatest Divisor

$$
\boxed{
HCF(\text{differences})
}
$$

### Smallest Number

$$
\boxed{
LCM+r
}
$$

### Huge Power

$$
\boxed{
\text{Find cycle → reduce exponent → select position}
}
$$

### Unit Digit

$$
\boxed{
\bmod10\rightarrow\text{last digit}
}
$$

### Last `k` Digits

$$
\boxed{
\bmod10^k\rightarrow\text{last }k\text{ digits}
}
$$

### Divisibility

$$
\boxed{
r=0\Rightarrow\text{divisible}
}
$$

### Polynomial

$$
\boxed{
P(x)\div(x-a)\Rightarrow P(a)
}
$$

### Golden Memory Trick

> **Every remainder problem asks: "What can I replace this huge expression with without changing its remainder?"**

### One-Line Recognition

> **Remainder question → identify the modulus → find the smallest useful pattern → reduce → calculate.**