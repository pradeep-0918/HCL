---
type: concept
subject: aptitude
topic: "Factors"
parent: "01. Number System/Factors and Multiples"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - factors
  - factors-and-multiples
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Factors and Multiples]]"
  - "[[Multiples]]"
  - "[[Number of Factors]]"
  - "[[Sum of Factors]]"
  - "[[Product of Factors]]"
  - "[[Factorization]]"
  - "[[HCF]]"
  - "[[LCM]]"
---

# Factors

## 1. Core Concept

> [!summary] Definition
> A **factor** of a number is a positive integer that divides the number exactly, leaving remainder `0`.

If:

$$
a\times b=N
$$

then:

$$
\boxed{a\text{ and }b\text{ are factors of }N}
$$

Equivalently:

$$
\boxed{a\mid N}
$$

means:

> `a` is a factor of `N`.

---

# 2. Basic Examples

For:

$$
12
$$

we can write:

$$
1\times12
$$

$$
2\times6
$$

$$
3\times4
$$

Therefore the positive factors of `12` are:

$$
\boxed{1,2,3,4,6,12}
$$

---

# 3. Factor Pair

Two numbers whose product is the given number form a **factor pair**.

For `24`:

$$
1\times24
$$

$$
2\times12
$$

$$
3\times8
$$

$$
4\times6
$$

Therefore the factor pairs are:

$$
\boxed{(1,24),(2,12),(3,8),(4,6)}
$$

> [!important] Pattern
> Factors usually appear in **pairs**.

---

# 4. The Most Important Factor Property

For every positive integer:

$$
\boxed{1\text{ and }N\text{ are always factors of }N}
$$

Example:

For `50`:

$$
1\times50=50
$$

Therefore:

$$
\boxed{1\text{ and }50}
$$

are always factors.

---

# 5. Factor vs Multiple

This distinction is extremely important.

If:

$$
3\times4=12
$$

then:

- `3` is a **factor** of `12`.
- `4` is a **factor** of `12`.
- `12` is a **multiple** of `3`.
- `12` is a **multiple** of `4`.

Therefore:

$$
\boxed{\text{Factor}\times\text{Factor}=\text{Number}}
$$

and:

$$
\boxed{\text{Number}=\text{Multiple of its factors}}
$$

---

# 6. Factor Test

To check whether `a` is a factor of `N`:

$$
\boxed{N\bmod a=0}
$$

### Example

Is `7` a factor of `42`?

$$
42\bmod7=0
$$

Therefore:

$$
\boxed{7\text{ is a factor of }42}
$$

---

# 7. Non-Factor Example

Is `5` a factor of `18`?

$$
18\div5
$$

leaves remainder `3`.

Therefore:

$$
18\bmod5=3
$$

So:

$$
\boxed{5\text{ is not a factor of }18}
$$

---

# 8. Factor Pair Pattern

Suppose:

$$
a\times b=N
$$

Then if `a` is a factor, the corresponding pair is:

$$
\boxed{b=\frac Na}
$$

### Example

For:

$$
N=60
$$

If:

$$
a=5
$$

then:

$$
b=\frac{60}{5}=12
$$

So:

$$
\boxed{(5,12)}
$$

is a factor pair.

---

# 9. Efficient Way to Find Factors

To find all factors of `N`, you only need to test numbers up to:

$$
\boxed{\sqrt N}
$$

Why?

Because factors occur in pairs.

If:

$$
a\times b=N
$$

and:

$$
a<\sqrt N
$$

then:

$$
b>\sqrt N
$$

So after reaching:

$$
\sqrt N
$$

the remaining factors are already obtained as pairs.

---

# 10. Example — Find Factors of 36

We have:

$$
\sqrt{36}=6
$$

Check numbers from `1` to `6`.

### `1`

$$
36\div1=36
$$

Pair:

$$
(1,36)
$$

### `2`

$$
36\div2=18
$$

Pair:

$$
(2,18)
$$

### `3`

$$
36\div3=12
$$

Pair:

$$
(3,12)
$$

### `4`

$$
36\div4=9
$$

Pair:

$$
(4,9)
$$

### `5`

Not a factor.

### `6`

$$
36\div6=6
$$

Pair:

$$
(6,6)
$$

Therefore:

$$
\boxed{1,2,3,4,6,9,12,18,36}
$$

---

# 11. Perfect Square Pattern

If `N` is a perfect square, one factor pair contains the same number twice.

Example:

$$
36=6\times6
$$

Therefore:

$$
\boxed{(6,6)}
$$

is a repeated factor pair.

This is why the number of factors of a perfect square is **odd**.

> [!important] Key Property
>
> If `N` is a perfect square:
>
> $$\boxed{\text{Number of factors is odd}}$$
>
> Otherwise:
>
> $$\boxed{\text{Number of factors is even}}
> $$

---

# 12. Number 1

The number `1` has exactly one positive factor:

$$
\boxed{1}
$$

Therefore:

$$
\boxed{\tau(1)=1}
$$

where `τ(N)` represents the number of positive factors of `N`.

---

# 13. Prime Number Pattern

A prime number has exactly two positive factors:

$$
\boxed{1\text{ and itself}}
$$

Examples:

$$
2,3,5,7,11,13,17,\ldots
$$

Therefore:

$$
\boxed{\text{Prime number}\Rightarrow2\text{ factors}}
$$

---

# 14. Composite Number Pattern

A composite number has more than two positive factors.

Example:

$$
12
$$

has:

$$
1,2,3,4,6,12
$$

Therefore:

$$
\boxed{12\text{ is composite}}
$$

---

# 15. Important Factor Properties

> [!important] Must Remember

For a positive integer `N`:

$$
\boxed{1\mid N}
$$

and:

$$
\boxed{N\mid N}
$$

Therefore:

$$
\boxed{1\text{ and }N\text{ are always factors of }N}
$$

---

# 16. Factor of a Factor

If:

$$
a\mid b
$$

and:

$$
b\mid N
$$

then:

$$
\boxed{a\mid N}
$$

### Example

`2` is a factor of `6`.

`6` is a factor of `30`.

Therefore:

$$
\boxed{2\text{ is a factor of }30}
$$

This is called the **transitive property of divisibility**.

---

# 17. Factors of a Product

If:

$$
a\mid b
$$

then:

$$
\boxed{a\mid bc}
$$

for any integer `c`.

### Example

Since:

$$
3\mid12
$$

then:

$$
3\mid60
$$

because:

$$
60=12\times5
$$

---

# 18. Factorization

Factorization means expressing a number as a product of smaller integers.

### Example

$$
60=2\times30
$$

Further:

$$
60=2\times2\times15
$$

Further:

$$
60=2\times2\times3\times5
$$

Therefore:

$$
\boxed{60=2^2\times3\times5}
$$

This is called **prime factorization**.

---

# 19. Prime Factorization — Why It Matters

Prime factorization is extremely important because it helps find:

- Number of factors
- Sum of factors
- HCF
- LCM
- Perfect-square conditions
- Perfect-cube conditions
- Divisibility
- Product of factors

> [!important] Aptitude Connection
> The upcoming topics:
>
> `Number of Factors`
>
> `Sum of Factors`
>
> `Product of Factors`
>
> all depend heavily on **prime factorization**.

---

# 20. Prime Factorization Example

Factorize:

$$
72
$$

Divide by `2`:

$$
72=2\times36
$$

Again:

$$
36=2\times18
$$

Again:

$$
18=2\times9
$$

And:

$$
9=3\times3
$$

Therefore:

$$
\boxed{72=2^3\times3^2}
$$

---

# 21. Factor Count Preview

If:

$$
N=p^a
$$

then the number of positive factors is:

$$
\boxed{a+1}
$$

### Example

$$
16=2^4
$$

Therefore:

$$
\text{Number of factors}=4+1
$$

$$
\boxed{5}
$$

The factors are:

$$
1,2,4,8,16
$$

---

# 22. General Factor Count Formula

If:

$$
N=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

then the number of positive factors is:

$$
\boxed{
\tau(N)=(a_1+1)(a_2+1)\cdots(a_k+1)
}
$$

### Example

For:

$$
72=2^3\times3^2
$$

number of factors:

$$
(3+1)(2+1)
$$

$$
=4\times3
$$

$$
\boxed{12}
$$

---

# 23. Why the Formula Works

For:

$$
N=2^3\times3^2
$$

a factor can contain:

$$
2^0,2^1,2^2,2^3
$$

There are:

$$
4
$$

choices for the exponent of `2`.

For `3`:

$$
3^0,3^1,3^2
$$

There are:

$$
3
$$

choices.

Therefore total combinations:

$$
4\times3=12
$$

Hence:

$$
\boxed{\tau(72)=12}
$$

---

# 24. Factor Pair Count

If `N` is **not** a perfect square:

$$
\boxed{
\text{Number of factor pairs}
=
\frac{\text{Number of factors}}{2}
}
$$

If `N` is a perfect square:

$$
\boxed{
\text{Number of factor pairs}
=
\frac{\text{Number of factors}+1}{2}
}
$$

### Example

For `36`:

Number of factors:

$$
9
$$

Therefore:

$$
\frac{9+1}{2}=5
$$

factor pairs:

$$
(1,36),(2,18),(3,12),(4,9),(6,6)
$$

---

# 25. Factor of Zero

Every non-zero integer divides `0` because:

$$
0=a\times0
$$

Therefore every non-zero integer is a divisor of `0`.

However, `0` is **not** a factor of a non-zero number because division by zero is undefined.

> [!warning] Important
> Avoid treating `0` as an ordinary factor in standard aptitude questions.

---

# 26. Negative Factors

In basic aptitude, we normally consider **positive factors**.

For example, positive factors of `12`:

$$
1,2,3,4,6,12
$$

Mathematically, negative factors also exist:

$$
-1,-2,-3,-4,-6,-12
$$

But unless the question explicitly asks for integers or negative factors, use:

$$
\boxed{\text{Positive factors}}
$$

---

# 27. Pattern — Is a Number Prime?

To determine whether `N` is prime, test divisibility by primes up to:

$$
\boxed{\sqrt N}
$$

### Example

Is `29` prime?

$$
\sqrt{29}\approx5.38
$$

Check primes:

$$
2,3,5
$$

`29` is not divisible by any of them.

Therefore:

$$
\boxed{29\text{ is prime}}
$$

> [!tip] Exam Pattern
> You do not need to test every number up to `N`.

---

# 28. Pattern — Number of Factors Is Odd

If a question says:

> "A number has an odd number of factors."

Immediately think:

$$
\boxed{\text{Perfect square}}
$$

### Example

Which number can have an odd number of factors?

$$
36
$$

because:

$$
36=6^2
$$

and its number of factors is:

$$
9
$$

which is odd.

---

# 29. Pattern — Exactly Two Factors

If a number has exactly two positive factors:

$$
\boxed{\text{It is prime}}
$$

Examples:

$$
2,3,5,7,11,13
$$

---

# 30. Pattern — Exactly Three Factors

A positive integer has exactly three positive factors **if and only if it is the square of a prime**.

### Example

$$
49=7^2
$$

Factors:

$$
1,7,49
$$

Therefore:

$$
\boxed{49\text{ has exactly 3 factors}}
$$

---

# 31. Pattern — Exactly Four Factors

If a number has exactly four positive factors, its prime-factorization form is either:

$$
\boxed{p^3}
$$

or:

$$
\boxed{pq}
$$

where `p` and `q` are distinct primes.

### Examples

$$
8=2^3
$$

Factors:

$$
1,2,4,8
$$

And:

$$
15=3\times5
$$

Factors:

$$
1,3,5,15
$$

Both have exactly `4` factors.

---

# 32. Important Pattern Table

> [!important] High-Yield

| Number of factors | Number structure |
|---:|---|
| `1` | `1` |
| `2` | Prime `p` |
| `3` | `p²` |
| `4` | `p³` or `pq` |
| `5` | `p⁴` |
| `6` | `p⁵` or `p²q` |
| `7` | `p⁶` |
| `8` | `p⁷`, `p³q`, or `pqr` |

where `p`, `q`, `r` are distinct primes.

---

# 33. Factor and HCF Connection

The **HCF** of two numbers is the greatest number that is a factor of both.

### Example

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

Greatest:

$$
\boxed{6}
$$

Therefore:

$$
\boxed{\operatorname{HCF}(12,18)=6}
$$

---

# 34. Factor and LCM Connection

The **LCM** is the smallest positive number that is a multiple of both numbers.

For:

$$
4,\ 6
$$

multiples of `4`:

$$
4,8,12,16,\ldots
$$

multiples of `6`:

$$
6,12,18,\ldots
$$

First common multiple:

$$
\boxed{12}
$$

Therefore:

$$
\boxed{\operatorname{LCM}(4,6)=12}
$$

---

# 35. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Confusing factors with multiples.
- ❌ Forgetting `1` and the number itself.
- ❌ Testing every number up to `N` when `√N` is enough.
- ❌ Forgetting factor pairs.
- ❌ Counting a square-root factor twice.
- ❌ Treating `0` as a normal factor.
- ❌ Forgetting that prime numbers have exactly two positive factors.
- ❌ Using the factor-count formula without prime factorization.
- ❌ Forgetting that an odd number of factors means a perfect square.

---

# 36. Exam Strategy

> [!tip] Factor Problem Decision Tree

When you see a factor question:

### If asked:

**"Is `a` a factor of `N`?"**

Use:

$$
\boxed{N\bmod a=0}
$$

### If asked:

**"Find all factors."**

Use factor pairs and check up to:

$$
\boxed{\sqrt N}
$$

### If asked:

**"Find number of factors."**

Prime factorize:

$$
N=p_1^{a_1}p_2^{a_2}\cdots
$$

Then:

$$
\boxed{
\tau(N)=\prod(a_i+1)
}
$$

### If asked:

**"Odd number of factors?"**

Think:

$$
\boxed{\text{Perfect square}}
$$

### If asked:

**"Exactly two factors?"**

Think:

$$
\boxed{\text{Prime}}
$$

---

# 37. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

Factors are the foundation for:

- Number of factors
- Sum of factors
- Product of factors
- Factorization
- HCF
- LCM
- Perfect squares
- Perfect cubes
- Divisibility
- Remainders

### Master These First

1. Factor definition
2. Factor pairs
3. Prime factorization
4. Factor count
5. Perfect-square pattern
6. Prime/composite connection
7. HCF connection
8. LCM connection
9. Factorization patterns
10. Special factor-count structures

---

# 38. Practice Checklist

- [ ] Understand factor definition
- [ ] Find factors of small numbers
- [ ] Find factor pairs
- [ ] Practice checking factors
- [ ] Practice prime factorization
- [ ] Learn the factor-count formula
- [ ] Practice perfect-square questions
- [ ] Practice prime-number questions
- [ ] Practice HCF using factors
- [ ] Practice LCM using multiples
- [ ] Practice factor-count structure problems
- [ ] Revise common traps

---

# 39. Related Topics

- [[Factors and Multiples]]
- [[Multiples]]
- [[Number of Factors]]
- [[Sum of Factors]]
- [[Product of Factors]]
- [[Factorization]]
- [[HCF]]
- [[LCM]]
- [[Prime and Composite Numbers]]
- [[Divisibility Rules]]

---

# 40. Quick Revision

> [!summary] One-Minute Revision

### Definition

$$
\boxed{
a\text{ is a factor of }N
\iff
N\bmod a=0
}
$$

### Factor Pair

$$
\boxed{a\times b=N}
$$

### Always Factors

$$
\boxed{1\text{ and }N}
$$

### Check All Factors

Only test up to:

$$
\boxed{\sqrt N}
$$

### Number of Factors

If:

$$
N=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

then:

$$
\boxed{
\tau(N)=
(a_1+1)(a_2+1)\cdots(a_k+1)
}
$$

### Perfect Square

$$
\boxed{\text{Odd number of factors}}
$$

### Prime

$$
\boxed{\text{Exactly 2 positive factors}}
$$

### Key Pattern

> **Factors come in pairs. Find the pair up to `√N`, then you have all factors.**