---
type: concept
subject: aptitude
topic: "HCF"
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
  - gcd
  - factors
  - factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[HCF and LCM]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Factorization]]"
  - "[[LCM]]"
  - "[[HCF-LCM Relationship]]"
  - "[[Application Problems]]"
---

# HCF

## 1. Core Concept

> [!summary] Definition
> **HCF** stands for **Highest Common Factor**.
>
> It is the **greatest positive integer that divides two or more numbers exactly**.

HCF is also called:

- **GCD** — Greatest Common Divisor
- **GCF** — Greatest Common Factor

Therefore:

$$
\boxed{\text{HCF}=\text{GCD}=\text{GCF}}
$$

---

# 2. Basic Example

Find the HCF of:

$$
12,\ 18
$$

Factors of `12`:

$$
1,2,3,4,6,12
$$

Factors of `18`:

$$
1,2,3,6,9,18
$$

Common factors:

$$
1,2,3,6
$$

Highest:

$$
\boxed{6}
$$

Therefore:

$$
\boxed{\operatorname{HCF}(12,18)=6}
$$

---

# 3. What Does HCF Actually Mean?

If:

$$
H=\operatorname{HCF}(a,b)
$$

then:

$$
H\mid a
$$

and:

$$
H\mid b
$$

and there is no larger positive integer that divides both.

Therefore:

$$
\boxed{
H=\text{largest common divisor}
}
$$

---

# 4. HCF Using Prime Factorization

This is one of the most important methods.

Suppose:

$$
A=p_1^{a_1}p_2^{a_2}\cdots
$$

and:

$$
B=p_1^{b_1}p_2^{b_2}\cdots
$$

Then:

$$
\boxed{
\operatorname{HCF}(A,B)
=
\prod p_i^{\min(a_i,b_i)}
}
$$

> [!important] Golden Rule
>
> **HCF → Take the common prime factors with the smallest powers.**

---

# 5. Example — Prime Factorization

Find HCF of:

$$
60,\ 84
$$

Prime factorize:

$$
60=2^2\times3\times5
$$

$$
84=2^2\times3\times7
$$

Common primes:

$$
2,\ 3
$$

Take the smaller powers:

$$
2^2\times3
$$

Therefore:

$$
\boxed{\operatorname{HCF}(60,84)=12}
$$

---

# 6. Example — Different Powers

Find:

$$
\operatorname{HCF}(72,120)
$$

Prime factorization:

$$
72=2^3\times3^2
$$

$$
120=2^3\times3\times5
$$

Common primes:

$$
2,\ 3
$$

Minimum powers:

$$
2^3\times3
$$

Therefore:

$$
\boxed{24}
$$

---

# 7. Example — No Common Prime Factor

Find:

$$
\operatorname{HCF}(15,28)
$$

Prime factorization:

$$
15=3\times5
$$

$$
28=2^2\times7
$$

There are no common prime factors.

Therefore:

$$
\boxed{\operatorname{HCF}(15,28)=1}
$$

Such numbers are called **coprime**.

---

# 8. Coprime Numbers

Two positive integers are **coprime** if:

$$
\boxed{\operatorname{HCF}(a,b)=1}
$$

Examples:

$$
(8,15)
$$

because:

$$
\operatorname{HCF}(8,15)=1
$$

Also:

$$
(14,25)
$$

because:

$$
\operatorname{HCF}(14,25)=1
$$

> [!important] Important
> Coprime numbers **do not have to be prime**.
>
> Example:
>
> `8` and `15` are both composite, but they are coprime.

---

# 9. HCF by Listing Factors

This method is useful for small numbers.

Example:

$$
20,\ 30
$$

Factors of `20`:

$$
1,2,4,5,10,20
$$

Factors of `30`:

$$
1,2,3,5,6,10,15,30
$$

Common factors:

$$
1,2,5,10
$$

Therefore:

$$
\boxed{\operatorname{HCF}=10}
$$

> [!tip] Exam Tip
> For large numbers, **do not list factors**.
>
> Use prime factorization or Euclidean algorithm.

---

# 10. HCF by Euclidean Algorithm

This is one of the fastest methods for large numbers.

If:

$$
a>b
$$

divide:

$$
a=bq+r
$$

Then:

$$
\boxed{\operatorname{HCF}(a,b)=\operatorname{HCF}(b,r)}
$$

Continue until the remainder becomes `0`.

The last non-zero remainder is the HCF.

---

# 11. Example — Euclidean Algorithm

Find:

$$
\operatorname{HCF}(252,105)
$$

Divide:

$$
252=105\times2+42
$$

Therefore:

$$
\operatorname{HCF}(252,105)
=
\operatorname{HCF}(105,42)
$$

Next:

$$
105=42\times2+21
$$

Next:

$$
42=21\times2+0
$$

Therefore:

$$
\boxed{\operatorname{HCF}(252,105)=21}
$$

---

# 12. Euclidean Algorithm Pattern

> [!important] Memorize

If:

$$
a=bq+r
$$

then:

$$
\boxed{\gcd(a,b)=\gcd(b,r)}
$$

Repeat until:

$$
r=0
$$

Then:

$$
\boxed{\text{Last non-zero remainder}=\text{HCF}}
$$

---

# 13. Why Euclidean Algorithm Works

Suppose:

$$
a=bq+r
$$

Then:

$$
r=a-bq
$$

Any common divisor of `a` and `b` must also divide `r`.

Therefore the common divisors of:

$$
(a,b)
$$

and:

$$
(b,r)
$$

are the same.

Hence:

$$
\boxed{
\gcd(a,b)=\gcd(b,r)
}
$$

---

# 14. HCF of More Than Two Numbers

For three numbers:

$$
a,b,c
$$

calculate:

$$
\operatorname{HCF}(a,b,c)
=
\operatorname{HCF}(\operatorname{HCF}(a,b),c)
$$

### Example

Find:

$$
\operatorname{HCF}(24,36,60)
$$

First:

$$
\operatorname{HCF}(24,36)=12
$$

Then:

$$
\operatorname{HCF}(12,60)=12
$$

Therefore:

$$
\boxed{12}
$$

---

# 15. HCF of Fractions

For positive fractions:

$$
\frac{a}{b},\frac{c}{d}
$$

the HCF is:

$$
\boxed{
\frac{\operatorname{HCF}(a,c)}
{\operatorname{LCM}(b,d)}
}
$$

### Example

Find HCF of:

$$
\frac{6}{5},\frac{9}{10}
$$

Numerator HCF:

$$
\operatorname{HCF}(6,9)=3
$$

Denominator LCM:

$$
\operatorname{LCM}(5,10)=10
$$

Therefore:

$$
\boxed{\frac3{10}}
$$

---

# 16. LCM of Fractions — Connection

For positive fractions:

$$
\frac{a}{b},\frac{c}{d}
$$

the LCM is:

$$
\boxed{
\frac{\operatorname{LCM}(a,c)}
{\operatorname{HCF}(b,d)}
}
$$

Therefore remember:

> [!important] Fraction Rule
>
> **HCF of fractions → HCF numerators / LCM denominators**
>
> **LCM of fractions → LCM numerators / HCF denominators**

---

# 17. HCF of Decimals

For decimal numbers, first convert them into integers by multiplying by the appropriate power of `10`.

### Example

Find HCF of:

$$
1.2,\ 1.8
$$

Multiply both by `10`:

$$
12,\ 18
$$

Now:

$$
\operatorname{HCF}(12,18)=6
$$

Since we multiplied by `10`, divide the result by `10`:

$$
\boxed{0.6}
$$

> [!tip] Pattern
>
> **Remove decimals → Find HCF → Restore decimal scale.**

---

# 18. HCF and Divisibility

If:

$$
H=\operatorname{HCF}(a,b)
$$

then:

$$
\boxed{H\mid a}
$$

and:

$$
\boxed{H\mid b}
$$

Therefore both numbers are multiples of `H`.

We can write:

$$
a=Hx
$$

and:

$$
b=Hy
$$

where:

$$
\operatorname{HCF}(x,y)=1
$$

---

# 19. Dividing by the HCF

If:

$$
H=\operatorname{HCF}(a,b)
$$

then:

$$
\boxed{
\operatorname{HCF}\left(\frac aH,\frac bH\right)=1
}
$$

### Example

For:

$$
a=60,\quad b=84
$$

HCF:

$$
H=12
$$

Then:

$$
\frac{60}{12}=5
$$

and:

$$
\frac{84}{12}=7
$$

Since:

$$
\operatorname{HCF}(5,7)=1
$$

the reduced numbers are coprime.

---

# 20. HCF and LCM Relationship

For two positive integers:

$$
a,b
$$

the fundamental relationship is:

$$
\boxed{
\operatorname{HCF}(a,b)
\times
\operatorname{LCM}(a,b)
=
a\times b
}
$$

Therefore:

$$
\boxed{
\operatorname{LCM}(a,b)
=
\frac{a\times b}{\operatorname{HCF}(a,b)}
}
$$

And:

$$
\boxed{
\operatorname{HCF}(a,b)
=
\frac{a\times b}{\operatorname{LCM}(a,b)}
}
$$

---

# 21. Example — Find LCM Using HCF

Given:

$$
a=24,\quad b=36
$$

and:

$$
\operatorname{HCF}=12
$$

Then:

$$
\operatorname{LCM}
=
\frac{24\times36}{12}
$$

$$
=2\times36
$$

$$
\boxed{72}
$$

---

# 22. HCF of Consecutive Numbers

For any two consecutive positive integers:

$$
n,\ n+1
$$

their HCF is:

$$
\boxed{1}
$$

### Example

$$
\operatorname{HCF}(24,25)=1
$$

because no integer greater than `1` divides both.

---

# 23. HCF of Two Consecutive Even Numbers

Consider:

$$
2n,\ 2n+2
$$

Factor out `2`:

$$
2n,\ 2(n+1)
$$

Therefore:

$$
\operatorname{HCF}(2n,2n+2)
=
2\operatorname{HCF}(n,n+1)
$$

Since consecutive numbers are coprime:

$$
\boxed{\operatorname{HCF}(2n,2n+2)=2}
$$

### Example

$$
\operatorname{HCF}(18,20)=2
$$

---

# 24. HCF of Consecutive Multiples

For:

$$
ka,\ kb
$$

we have:

$$
\boxed{
\operatorname{HCF}(ka,kb)
=
k\operatorname{HCF}(a,b)
}
$$

### Example

Find:

$$
\operatorname{HCF}(24,36)
$$

Write:

$$
24=12\times2
$$

$$
36=12\times3
$$

Since:

$$
\operatorname{HCF}(2,3)=1
$$

the HCF is:

$$
\boxed{12}
$$

---

# 25. HCF of Multiples of the Same Number

If:

$$
a=mx
$$

and:

$$
b=my
$$

then:

$$
\boxed{
\operatorname{HCF}(a,b)
=
m\operatorname{HCF}(x,y)
}
$$

If `x` and `y` are coprime:

$$
\boxed{
\operatorname{HCF}(a,b)=m
}
$$

---

# 26. HCF Pattern — Difference

A very useful property is:

$$
\boxed{
\gcd(a,b)=\gcd(a,b-a)
}
$$

More generally:

$$
\boxed{
\gcd(a,b)=\gcd(a,b-ka)
}
$$

for any integer `k`.

This is the foundation of the Euclidean algorithm.

### Example

Find:

$$
\gcd(48,18)
$$

Subtract twice `18`:

$$
48-36=12
$$

Therefore:

$$
\gcd(48,18)=\gcd(18,12)
$$

Then:

$$
18-12=6
$$

Therefore:

$$
\boxed{\gcd(48,18)=6}
$$

---

# 27. HCF and Linear Combination

If:

$$
d=\gcd(a,b)
$$

then `d` can be expressed as:

$$
\boxed{
d=ax+by
}
$$

for some integers `x` and `y`.

This is called **Bézout's identity**.

### Example

For:

$$
\gcd(12,18)=6
$$

we can write:

$$
6=18-12
$$

Therefore:

$$
\boxed{6=12(-1)+18(1)}
$$

---

# 28. HCF of Numbers in a Sequence

If all numbers in a sequence share a common factor, factor it out first.

### Example

Find the HCF of:

$$
18,\ 30,\ 42
$$

Each is divisible by `6`:

$$
18=6\times3
$$

$$
30=6\times5
$$

$$
42=6\times7
$$

Since:

$$
\operatorname{HCF}(3,5,7)=1
$$

we get:

$$
\boxed{6}
$$

---

# 29. HCF Application — Largest Size

A common aptitude question:

> A rectangular sheet of size `48 cm × 60 cm` must be cut into the largest possible equal squares. What is the side of each square?

The side must divide both dimensions.

Therefore:

$$
\boxed{\text{Side}=\operatorname{HCF}(48,60)}
$$

Prime factorization:

$$
48=2^4\times3
$$

$$
60=2^2\times3\times5
$$

HCF:

$$
2^2\times3
$$

$$
\boxed{12\text{ cm}}
$$

---

# 30. HCF Application — Maximum Equal Groups

Suppose:

- `48` students
- `60` students

must be divided into the **maximum number of equal groups**, with each group having the same composition.

The number of groups is:

$$
\boxed{\operatorname{HCF}(48,60)}
$$

Therefore:

$$
\boxed{12\text{ groups}}
$$

Each group contains:

$$
48/12=4
$$

from the first group and:

$$
60/12=5
$$

from the second group.

---

# 31. HCF Application — Greatest Measure

If a question asks:

> Find the greatest length that can exactly measure several lengths.

Immediately think:

$$
\boxed{\text{HCF}}
$$

### Example

Find the greatest length that can exactly measure:

$$
36,\ 48,\ 60\text{ cm}
$$

Calculate:

$$
\operatorname{HCF}(36,48,60)=12
$$

Therefore:

$$
\boxed{12\text{ cm}}
$$

---

# 32. HCF Application — Minimum Number Added/Subtracted

Some problems ask:

> Find the greatest number that divides several numbers leaving the same remainder.

Suppose the numbers are:

$$
a,b,c
$$

If they leave the same remainder when divided by `d`, then:

$$
d\mid(a-b)
$$

and:

$$
d\mid(b-c)
$$

Therefore:

$$
\boxed{
d=\operatorname{HCF}(a-b,b-c)
}
$$

This is a very important aptitude pattern.

---

# 33. Example — Same Remainder

Find the greatest number that divides:

$$
43,\ 67,\ 91
$$

leaving the same remainder.

Take differences:

$$
67-43=24
$$

$$
91-67=24
$$

Therefore:

$$
\operatorname{HCF}(24,24)=24
$$

Hence:

$$
\boxed{24}
$$

Check:

$$
43\div24
$$

remainder `19`.

$$
67\div24
$$

remainder `19`.

$$
91\div24
$$

remainder `19`.

Correct.

---

# 34. HCF Application — Same Remainder Formula

For numbers:

$$
a,b,c
$$

the greatest divisor leaving the **same remainder** is:

$$
\boxed{
\operatorname{HCF}(a-b,b-c,c-a)
}
$$

Usually two differences are sufficient.

---

# 35. HCF Application — Different Remainders

If a divisor leaves different remainders, subtract the appropriate remainders first.

### Example Pattern

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
a-b\equiv r_1-r_2\pmod d
$$

So:

$$
\boxed{
d\mid[(a-b)-(r_1-r_2)]
}
$$

This is an advanced remainder-HCF connection.

---

# 36. HCF of Fractions — Formula

For:

$$
\frac ab,\frac cd
$$

in lowest terms:

$$
\boxed{
\operatorname{HCF}
=
\frac{\operatorname{HCF}(a,c)}
{\operatorname{LCM}(b,d)}
}
$$

Remember:

$$
\boxed{
\text{HCF fraction}
=
\frac{\text{HCF numerators}}
{\text{LCM denominators}}
}
$$

---

# 37. HCF of Three Fractions

For:

$$
\frac{a}{p},
\frac{b}{q},
\frac{c}{r}
$$

the HCF is:

$$
\boxed{
\frac{
\operatorname{HCF}(a,b,c)
}{
\operatorname{LCM}(p,q,r)
}
}
$$

assuming the fractions are in their appropriate reduced form.

---

# 38. HCF and Coprime Reduction

Suppose:

$$
A=Hx
$$

and:

$$
B=Hy
$$

where:

$$
H=\operatorname{HCF}(A,B)
$$

Then:

$$
\boxed{\operatorname{HCF}(x,y)=1}
$$

This is useful for reducing ratios.

### Example

Ratio:

$$
84:126
$$

HCF:

$$
\operatorname{HCF}(84,126)=42
$$

Divide both by `42`:

$$
2:3
$$

Therefore the simplified ratio is:

$$
\boxed{2:3}
$$

---

# 39. HCF in Ratios

To simplify:

$$
a:b
$$

divide both terms by their HCF:

$$
\boxed{
\frac a{\operatorname{HCF}(a,b)}
:
\frac b{\operatorname{HCF}(a,b)}
}
$$

### Example

Simplify:

$$
120:180
$$

HCF:

$$
60
$$

Therefore:

$$
120:180
=
2:3
$$

---

# 40. Important Formula Sheet

> [!important] Must Remember

### Prime Factorization Method

$$
\boxed{
\operatorname{HCF}(A,B)
=
\prod p_i^{\min(a_i,b_i)}
}
$$

### Euclidean Algorithm

$$
\boxed{
\gcd(a,b)=\gcd(b,a\bmod b)
}
$$

### HCF-LCM Relationship

$$
\boxed{
\operatorname{HCF}(a,b)
\times
\operatorname{LCM}(a,b)
=
ab
}
$$

### LCM From HCF

$$
\boxed{
\operatorname{LCM}(a,b)
=
\frac{ab}{\operatorname{HCF}(a,b)}
}
$$

### HCF of Fractions

$$
\boxed{
\frac{\operatorname{HCF}(\text{numerators})}
{\operatorname{LCM}(\text{denominators})}
}
$$

### HCF of Multiples

$$
\boxed{
\operatorname{HCF}(ka,kb)
=
k\operatorname{HCF}(a,b)
}
$$

---

# 41. Important Patterns

> [!important] High-Yield Patterns

### Pattern 1 — Common Factor

If a number divides all given numbers:

$$
\boxed{\text{Think HCF}}
$$

### Pattern 2 — Largest Equal Size

$$
\boxed{\text{HCF}}
$$

### Pattern 3 — Greatest Measuring Length

$$
\boxed{\text{HCF}}
$$

### Pattern 4 — Maximum Equal Groups

$$
\boxed{\text{HCF}}
$$

### Pattern 5 — Same Remainder

Take differences:

$$
\boxed{\text{HCF of differences}}
$$

### Pattern 6 — Prime Factorization

$$
\boxed{\text{HCF → minimum powers}}
$$

### Pattern 7 — LCM Connection

$$
\boxed{
HCF\times LCM=Product
}
$$

### Pattern 8 — Consecutive Numbers

$$
\boxed{\operatorname{HCF}(n,n+1)=1}
$$

---

# 42. HCF vs LCM

> [!important] Never Confuse These

| Concept | HCF | LCM |
|---|---|---|
| Meaning | Highest Common Factor | Least Common Multiple |
| Think | Factors | Multiples |
| Prime powers | Minimum | Maximum |
| Application | Greatest equal size | Smallest common occurrence |
| Formula | Common minimum powers | All maximum powers |
| Relation | `HCF × LCM = Product` | `HCF × LCM = Product` |

### Memory Trick

> **HCF = Highest Common Factor → common factors → minimum powers**
>
> **LCM = Least Common Multiple → all factors → maximum powers**

---

# 43. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using maximum powers for HCF.
- ❌ Using minimum powers for LCM.
- ❌ Confusing HCF with the smallest common factor.
- ❌ Forgetting that `1` is always a common factor.
- ❌ Listing factors for very large numbers.
- ❌ Forgetting to reduce fractions before applying formulas.
- ❌ Assuming coprime numbers must both be prime.
- ❌ Using the HCF-LCM product formula for more than two numbers without care.
- ❌ Missing the "same remainder → HCF of differences" pattern.

---

# 44. Exam Strategy

> [!tip] Fast Decision Tree

### Question says:

**"Greatest number that divides..."**

Think:

$$
\boxed{\text{HCF}}
$$

### "Largest possible equal size"

Think:

$$
\boxed{\text{HCF}}
$$

### "Greatest length that exactly measures"

Think:

$$
\boxed{\text{HCF}}
$$

### "Maximum number of equal groups"

Think:

$$
\boxed{\text{HCF}}
$$

### "Same remainder"

Think:

$$
\boxed{\text{HCF of differences}}
$$

### "Prime factorization"

Take:

$$
\boxed{\text{minimum exponents}}
$$

### "Two numbers, HCF and LCM relationship"

Use:

$$
\boxed{
HCF\times LCM=a\times b
}
$$

---

# 45. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

HCF is one of the most frequently useful Number System concepts because it connects directly to:

- LCM
- Fractions
- Ratios
- Remainders
- Divisibility
- Factorization
- Application problems

### Master These First

1. HCF definition
2. Prime factorization method
3. Euclidean algorithm
4. HCF of multiple numbers
5. Coprime numbers
6. HCF-LCM relationship
7. HCF of fractions
8. Same-remainder problems
9. Greatest-measure problems
10. Maximum-group problems

---

# 46. Practice Checklist

- [ ] Find HCF by listing factors
- [ ] Find HCF by prime factorization
- [ ] Practice Euclidean algorithm
- [ ] Find HCF of 3 or more numbers
- [ ] Identify coprime numbers
- [ ] Practice HCF-LCM questions
- [ ] Find HCF of fractions
- [ ] Simplify ratios using HCF
- [ ] Solve greatest-measure problems
- [ ] Solve maximum-group problems
- [ ] Solve same-remainder problems
- [ ] Revise minimum-exponent rule

---

# 47. Related Topics

- [[HCF and LCM]]
- [[LCM]]
- [[Factors]]
- [[Multiples]]
- [[Factorization]]
- [[Number of Factors]]
- [[Sum of Factors]]
- [[Product of Factors]]
- [[Remainders]]
- [[Divisibility Rules]]
- [[Application Problems]]

---

# 48. Quick Revision

> [!summary] One-Minute Revision

### Definition

$$
\boxed{
HCF=\text{greatest common divisor}
}
$$

### Prime Factorization

$$
\boxed{
HCF=\text{common primes with minimum powers}
}
$$

### Euclidean Algorithm

$$
\boxed{
\gcd(a,b)=\gcd(b,a\bmod b)
}
$$

### HCF-LCM

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### Fractions

$$
\boxed{
HCF=
\frac{HCF(\text{numerators})}
{LCM(\text{denominators})}
}
$$

### Same Remainder

$$
\boxed{
HCF=\text{HCF of differences}
}
$$

### Consecutive Numbers

$$
\boxed{
HCF(n,n+1)=1
}
$$

### Golden Memory Trick

> **HCF → common factors → take the smallest prime powers.**

### One-Line Recognition

> **"Greatest", "largest equal", "maximum groups", or "greatest measure" → THINK HCF.**