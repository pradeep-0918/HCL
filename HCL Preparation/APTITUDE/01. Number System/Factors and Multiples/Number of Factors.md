---
type: concept
subject: aptitude
topic: "Number of Factors"
parent: "01. Number System/Factors and Multiples"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - factors
  - number-of-factors
  - factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Factors and Multiples]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Sum of Factors]]"
  - "[[Product of Factors]]"
  - "[[Factorization]]"
  - "[[Prime and Composite Numbers]]"
  - "[[HCF]]"
  - "[[LCM]]"
---

# Number of Factors

## 1. Core Concept

> [!summary] Definition
> The **number of factors** of a positive integer `N` means the number of positive integers that divide `N` exactly.

For example:

$$
12
$$

has factors:

$$
1,2,3,4,6,12
$$

Therefore:

$$
\boxed{12\text{ has }6\text{ positive factors}}
$$

We commonly represent the number of factors using:

$$
\boxed{\tau(N)}
$$

---

# 2. The Most Important Formula

Suppose the prime factorization of `N` is:

$$
N=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

Then:

$$
\boxed{
\tau(N)=(a_1+1)(a_2+1)\cdots(a_k+1)
}
$$

> [!important] Golden Formula
>
> **Add `1` to every prime exponent → multiply the results.**

This is one of the **highest-priority formulas in Number System aptitude**.

---

# 3. Why the Formula Works

Consider:

$$
N=2^3\times3^2
$$

A factor can contain:

$$
2^0,\ 2^1,\ 2^2,\ 2^3
$$

There are:

$$
4
$$

choices for the exponent of `2`.

For `3`, possible powers are:

$$
3^0,\ 3^1,\ 3^2
$$

There are:

$$
3
$$

choices.

Therefore:

$$
4\times3=12
$$

So:

$$
\boxed{\tau(72)=12}
$$

---

# 4. Basic Example

Find the number of factors of:

$$
36
$$

Prime factorization:

$$
36=2^2\times3^2
$$

Apply the formula:

$$
\tau(36)=(2+1)(2+1)
$$

$$
=3\times3
$$

$$
\boxed{9}
$$

The factors are:

$$
1,2,3,4,6,9,12,18,36
$$

Exactly `9`.

---

# 5. Example — Prime Number

Let:

$$
N=13
$$

Prime factorization:

$$
13=13^1
$$

Therefore:

$$
\tau(13)=1+1
$$

$$
\boxed{2}
$$

Every prime number has exactly:

$$
\boxed{2\text{ positive factors}}
$$

---

# 6. Example — Prime Power

Find the number of factors of:

$$
64
$$

Prime factorization:

$$
64=2^6
$$

Therefore:

$$
\tau(64)=6+1
$$

$$
\boxed{7}
$$

Factors:

$$
1,2,4,8,16,32,64
$$

---

# 7. Example — Multiple Prime Factors

Find the number of factors of:

$$
120
$$

Prime factorization:

$$
120=2^3\times3\times5
$$

Therefore:

$$
\tau(120)
=
(3+1)(1+1)(1+1)
$$

$$
=4\times2\times2
$$

$$
\boxed{16}
$$

---

# 8. Example — Large Number

Find the number of factors of:

$$
360
$$

Prime factorization:

$$
360=2^3\times3^2\times5
$$

Therefore:

$$
\tau(360)
=
(3+1)(2+1)(1+1)
$$

$$
=4\times3\times2
$$

$$
\boxed{24}
$$

---

# 9. The Step-by-Step Method

> [!tip] Exam Method

Whenever you see:

> **"Find the number of factors of N."**

Follow exactly these steps.

### Step 1

Prime factorize `N`.

### Step 2

Write every exponent.

### Step 3

Add `1` to each exponent.

### Step 4

Multiply.

### Example

$$
540
$$

Prime factorization:

$$
540=2^2\times3^3\times5
$$

Therefore:

$$
\tau(540)
=
(2+1)(3+1)(1+1)
$$

$$
=3\times4\times2
$$

$$
\boxed{24}
$$

---

# 10. Factor Count and Perfect Squares

This is extremely important.

> [!important] Perfect-Square Property
> A positive integer has an **odd number of positive factors if and only if it is a perfect square**.

### Example

$$
36=2^2\times3^2
$$

Both exponents are even.

Therefore:

$$
\tau(36)=3\times3=9
$$

`9` is odd.

Hence:

$$
\boxed{36\text{ is a perfect square}}
$$

---

# 11. Why Perfect Squares Have Odd Factors

Factors normally occur in pairs:

$$
a\times b=N
$$

For a non-square:

$$
a\ne b
$$

So every factor has a different partner.

For a perfect square:

$$
N=a^2
$$

the middle factor pairs with itself:

$$
a\times a=N
$$

Therefore one factor is unpaired.

Hence:

$$
\boxed{\text{Perfect square}\Rightarrow\text{odd number of factors}}
$$

---

# 12. Perfect Square Test Using Exponents

A number is a perfect square if **all prime exponents are even**.

### Example

$$
144=2^4\times3^2
$$

Exponents:

$$
4,\ 2
$$

Both are even.

Therefore:

$$
\boxed{144\text{ is a perfect square}}
$$

---

# 13. Perfect Cube Pattern

A number is a perfect cube if **all prime exponents are multiples of `3`**.

### Example

$$
216=2^3\times3^3
$$

Both exponents are multiples of `3`.

Therefore:

$$
\boxed{216\text{ is a perfect cube}}
$$

> [!important] Pattern
>
> Perfect square → exponents divisible by `2`.
>
> Perfect cube → exponents divisible by `3`.

---

# 14. Number With Exactly 2 Factors

If:

$$
\tau(N)=2
$$

then:

$$
\boxed{N\text{ is prime}}
$$

Because its only factors are:

$$
1,N
$$

---

# 15. Number With Exactly 3 Factors

If:

$$
\tau(N)=3
$$

then:

$$
N=p^2
$$

where `p` is prime.

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
\boxed{\tau(49)=3}
$$

---

# 16. Number With Exactly 4 Factors

If:

$$
\tau(N)=4
$$

then the possible structures are:

$$
\boxed{p^3}
$$

or:

$$
\boxed{pq}
$$

where `p` and `q` are distinct primes.

### Example 1

$$
8=2^3
$$

$$
\tau(8)=3+1=4
$$

### Example 2

$$
15=3\times5
$$

$$
\tau(15)=(1+1)(1+1)=4
$$

---

# 17. Number With Exactly 5 Factors

If:

$$
\tau(N)=5
$$

then:

$$
\boxed{N=p^4}
$$

where `p` is prime.

### Example

$$
16=2^4
$$

Therefore:

$$
\tau(16)=4+1
$$

$$
\boxed{5}
$$

---

# 18. Number With Exactly 6 Factors

Possible exponent structures:

$$
6=6
$$

or:

$$
6=3\times2
$$

Therefore:

$$
\boxed{N=p^5}
$$

or:

$$
\boxed{N=p^2q}
$$

where `p` and `q` are distinct primes.

### Examples

$$
32=2^5
$$

has:

$$
6
$$

factors.

And:

$$
12=2^2\times3
$$

has:

$$
(2+1)(1+1)=6
$$

factors.

---

# 19. Important Factor-Count Structure Table

> [!important] Memorize

| Number of factors | Possible structure |
|---:|---|
| `1` | `1` |
| `2` | `p` |
| `3` | `p²` |
| `4` | `p³`, `pq` |
| `5` | `p⁴` |
| `6` | `p⁵`, `p²q` |
| `7` | `p⁶` |
| `8` | `p⁷`, `p³q`, `pqr` |
| `9` | `p⁸`, `p²q²` |
| `10` | `p⁹`, `p⁴q` |

where `p`, `q`, `r` are distinct primes.

---

# 20. Number of Even Factors

This is a very important extension.

Suppose:

$$
N=2^a\times p_2^{b}\times p_3^{c}\cdots
$$

To count **even factors**, the exponent of `2` must be at least `1`.

For `2`, choices are:

$$
2^1,2^2,\ldots,2^a
$$

So there are:

$$
a
$$

choices.

Therefore:

$$
\boxed{
\text{Number of even factors}
=
a(b+1)(c+1)\cdots
}
$$

### Example

For:

$$
72=2^3\times3^2
$$

Total factors:

$$
(3+1)(2+1)=12
$$

Even factors:

$$
3\times3=9
$$

Therefore:

$$
\boxed{9\text{ even factors}}
$$

---

# 21. Number of Odd Factors

Odd factors cannot contain `2`.

Therefore, simply ignore the power of `2`.

If:

$$
N=2^a\times p^b\times q^c
$$

then:

$$
\boxed{
\text{Odd factors}=(b+1)(c+1)
}
$$

### Example

For:

$$
72=2^3\times3^2
$$

odd factors:

$$
2+1=3
$$

Therefore:

$$
\boxed{3\text{ odd factors}}
$$

They are:

$$
1,3,9
$$

---

# 22. Total = Odd + Even

Always:

$$
\boxed{
\text{Total factors}
=
\text{Odd factors}
+
\text{Even factors}
}
$$

For `72`:

$$
3+9=12
$$

which matches:

$$
\tau(72)=12
$$

---

# 23. Number of Factors Divisible by a Given Prime

Suppose:

$$
N=2^5\times3^2
$$

How many factors are divisible by `2`?

The exponent of `2` in the factor can be:

$$
1,2,3,4,5
$$

That gives:

$$
5
$$

choices.

For `3`:

$$
0,1,2
$$

gives:

$$
3
$$

choices.

Therefore:

$$
5\times3
$$

$$
\boxed{15}
$$

factors are divisible by `2`.

---

# 24. Number of Factors Divisible by a Given Number

Suppose:

$$
N=2^5\times3^3
$$

How many factors of `N` are divisible by:

$$
12=2^2\times3
$$

A factor must contain:

$$
2^2
$$

or higher.

Possible exponents of `2`:

$$
2,3,4,5
$$

Number of choices:

$$
4
$$

Possible exponents of `3`:

$$
1,2,3
$$

Number of choices:

$$
3
$$

Therefore:

$$
4\times3
$$

$$
\boxed{12}
$$

---

# 25. Number of Factors Divisible by 6

Suppose:

$$
N=2^a\times3^b\times\cdots
$$

A factor divisible by:

$$
6=2\times3
$$

must contain at least:

$$
2^1
$$

and:

$$
3^1
$$

Therefore the number of such factors is:

$$
\boxed{
a\times b\times
(\text{other exponent choices})
}
$$

### Example

For:

$$
72=2^3\times3^2
$$

factors divisible by `6`:

$$
3\times2=6
$$

Therefore:

$$
\boxed{6}
$$

---

# 26. Sum of Number of Factors — Important Connection

The number-of-factors formula is:

$$
\boxed{
\tau(N)=\prod(a_i+1)
}
$$

The **sum of factors** will use a different formula:

$$
\boxed{
\sigma(N)
=
\prod
\left(
1+p+p^2+\cdots+p^a
\right)
}
$$

This is the next topic after number of factors.

> [!note]
> Do not confuse:
>
> `τ(N)` → **number** of factors
>
> `σ(N)` → **sum** of factors

---

# 27. Factor Count of a Product

In general:

$$
\boxed{
\tau(ab)\ne\tau(a)\tau(b)
}
$$

unless `a` and `b` are coprime.

If:

$$
\gcd(a,b)=1
$$

then:

$$
\boxed{
\tau(ab)=\tau(a)\tau(b)
}
$$

### Example

Take:

$$
8=2^3
$$

and:

$$
9=3^2
$$

Since:

$$
\gcd(8,9)=1
$$

we have:

$$
\tau(72)=\tau(8)\tau(9)
$$

$$
=4\times3
$$

$$
\boxed{12}
$$

---

# 28. Important Property of Divisors

If `d` is a factor of `N`, then:

$$
\boxed{\frac Nd}
$$

is also a factor of `N`.

Therefore factors occur in pairs:

$$
\boxed{
d\longleftrightarrow\frac Nd
}
$$

This explains why non-square numbers have an even number of factors.

---

# 29. Example — Fast Factor Count

Find the number of factors of:

$$
840
$$

Prime factorization:

$$
840=2^3\times3\times5\times7
$$

Therefore:

$$
\tau(840)
=
(3+1)(1+1)(1+1)(1+1)
$$

$$
=4\times2\times2\times2
$$

$$
\boxed{32}
$$

> [!tip] Exam Trick
> Once prime factorization is known, **do not list the factors**.
>
> Immediately use:
>
> $$\boxed{\prod(a_i+1)}$$

---

# 30. Example — Very Large Number

Find the number of factors of:

$$
2^{10}\times3^5\times5^2
$$

No expansion is necessary.

Apply the formula:

$$
(10+1)(5+1)(2+1)
$$

$$
=11\times6\times3
$$

$$
\boxed{198}
$$

---

# 31. Minimum Number With a Given Number of Factors

This is a common higher-level aptitude pattern.

### Example

Find the smallest number having exactly `6` factors.

Possible structures:

$$
p^5
$$

or:

$$
p^2q
$$

For:

$$
p^5
$$

smallest:

$$
2^5=32
$$

For:

$$
p^2q
$$

choose the smallest distinct primes:

$$
2^2\times3=12
$$

Therefore:

$$
\boxed{12}
$$

has exactly `6` factors and is smaller than `32`.

---

# 32. Minimum Number With Exactly 12 Factors

Since:

$$
12=12
$$

or:

$$
12=6\times2
$$

or:

$$
12=4\times3
$$

or:

$$
12=3\times2\times2
$$

Possible structures include:

$$
p^{11}
$$

$$
p^5q
$$

$$
p^3q^2
$$

$$
p^2qr
$$

To minimize the number, assign larger exponents to smaller primes.

For:

$$
p^3q^2
$$

choose:

$$
2^3\times3^2
$$

$$
=8\times9
$$

$$
\boxed{72}
$$

For:

$$
p^2qr
$$

we get:

$$
2^2\times3\times5=60
$$

Therefore `60` is smaller.

So:

$$
\boxed{60}
$$

is the smallest positive integer having exactly `12` factors.

> [!important] Advanced Pattern
> When minimizing a number with a fixed number of factors:
>
> **Give larger exponents to smaller primes.**

---

# 33. Maximum Number of Factors Below N

This type of question requires comparing prime factorizations.

### Example

Compare:

$$
36=2^2\times3^2
$$

and:

$$
48=2^4\times3
$$

For `36`:

$$
\tau(36)=3\times3=9
$$

For `48`:

$$
\tau(48)=5\times2=10
$$

Therefore:

$$
\boxed{48\text{ has more factors}}
$$

---

# 34. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Counting factors by listing them when prime factorization is easier.
- ❌ Forgetting to add `1` to every exponent.
- ❌ Multiplying exponents directly.
- ❌ Confusing number of factors with sum of factors.
- ❌ Forgetting that `1` has exactly one positive factor.
- ❌ Assuming every number with an even number of factors is composite without context.
- ❌ Forgetting that perfect squares have odd factor counts.
- ❌ Counting the square-root factor twice.
- ❌ Forgetting that only positive factors are normally considered.
- ❌ Using `τ(ab)=τ(a)τ(b)` when `a` and `b` are not coprime.

---

# 35. Exam Strategy

> [!tip] Fast Decision Tree

### Asked: "Number of factors?"

Prime factorize:

$$
N=p_1^{a_1}p_2^{a_2}\cdots
$$

Then:

$$
\boxed{\tau(N)=\prod(a_i+1)}
$$

### Asked: "Odd number of factors?"

Think:

$$
\boxed{\text{Perfect square}}
$$

### Asked: "Exactly 2 factors?"

Think:

$$
\boxed{\text{Prime}}
$$

### Asked: "Exactly 3 factors?"

Think:

$$
\boxed{p^2}
$$

### Asked: "Even factors?"

Require exponent of `2`:

$$
\boxed{\ge1}
$$

### Asked: "Odd factors?"

Ignore the exponent of `2`.

### Asked: "Factors divisible by d?"

Write the prime factorization of `d` and determine the minimum exponent required in each factor.

---

# 36. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

This is one of the most important factor topics for aptitude.

### Master These First

1. Prime factorization
2. Number-of-factors formula
3. Perfect-square pattern
4. Prime-number pattern
5. Exact factor-count structures
6. Odd/even factors
7. Factors divisible by a number
8. Minimum number with N factors
9. Maximum factor-count comparisons
10. Connection with HCF and LCM

---

# 37. Practice Checklist

- [ ] Memorize `τ(N)` formula
- [ ] Practice prime factorization
- [ ] Find number of factors
- [ ] Practice perfect-square questions
- [ ] Practice prime-number questions
- [ ] Practice exactly N factors
- [ ] Practice odd/even factor questions
- [ ] Practice factors divisible by a given number
- [ ] Practice minimum-number questions
- [ ] Practice comparison questions
- [ ] Practice HCF/LCM connections
- [ ] Revise common traps

---

# 38. Related Topics

- [[Factors and Multiples]]
- [[Factors]]
- [[Multiples]]
- [[Sum of Factors]]
- [[Product of Factors]]
- [[Factorization]]
- [[HCF]]
- [[LCM]]
- [[Prime and Composite Numbers]]
- [[Divisibility Rules]]

---

# 39. Quick Revision

> [!summary] One-Minute Revision

### Main Formula

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

### Example

$$
72=2^3\times3^2
$$

Therefore:

$$
\tau(72)
=
(3+1)(2+1)
$$

$$
=12
$$

### Perfect Square

$$
\boxed{\text{Odd number of factors}}
$$

### Prime

$$
\boxed{\text{Exactly 2 factors}}
$$

### Exactly 3 Factors

$$
\boxed{p^2}
$$

### Exactly 4 Factors

$$
\boxed{p^3\text{ or }pq}
$$

### Odd Factors

Ignore the power of `2`.

### Even Factors

Exponent of `2` must be at least `1`.

### Golden Memory Trick

> **Prime factorize → Add 1 to every exponent → Multiply.**