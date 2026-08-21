---
type: concept
subject: aptitude
topic: "Prime and Composite Numbers"
parent: "01. Number System"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - prime-numbers
  - composite-numbers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Natural Numbers]]"
  - "[[Whole Numbers]]"
  - "[[Integers]]"
  - "[[Factors]]"
  - "[[Divisibility Rules]]"
  - "[[HCF]]"
  - "[[LCM]]"
---

# Prime and Composite Numbers

## 1. Overview

> [!summary] Core Idea
> A **prime number** is a natural number greater than `1` that has exactly **two positive factors**: `1` and itself.
>
> A **composite number** is a natural number greater than `1` that has **more than two positive factors**.

### Prime

$$
\boxed{\text{Exactly 2 factors}}
$$

### Composite

$$
\boxed{\text{More than 2 factors}}
$$

---

# 2. Prime Numbers

A prime number has exactly two positive factors:

1. `1`
2. The number itself

### Examples

$$
2,3,5,7,11,13,17,19,23,29,\ldots
$$

For example, the factors of `7` are:

$$
1,7
$$

Therefore:

$$
\boxed{7\text{ is prime}}
$$

---

# 3. Composite Numbers

A composite number has more than two positive factors.

Example:

$$
6
$$

Factors of `6`:

$$
1,2,3,6
$$

There are four factors.

Therefore:

$$
\boxed{6\text{ is composite}}
$$

Another example:

$$
12
$$

Factors:

$$
1,2,3,4,6,12
$$

Therefore:

$$
\boxed{12\text{ is composite}}
$$

---

# 4. The Special Cases

## Number `1`

`1` is **neither prime nor composite**.

Why?

The only positive factor of `1` is:

$$
1
$$

It has only **one factor**, not two.

Therefore:

$$
\boxed{1\text{ is neither prime nor composite}}
$$

> [!warning] Critical Trap
> Never classify `1` as a prime number.

---

## Number `2`

`2` has exactly two factors:

$$
1,2
$$

Therefore:

$$
\boxed{2\text{ is prime}}
$$

It is also the **only even prime number**.

> [!important] Must Remember
>
> $$\boxed{2=\text{Only even prime number}}
> $$

---

## Number `0`

`0` is neither prime nor composite.

Prime and composite classification normally applies to natural numbers greater than `1`.

Therefore:

$$
\boxed{0\text{ is neither prime nor composite}}
$$

---

# 5. Prime vs Composite

| Property | Prime | Composite |
|---|---|---|
| Number of positive factors | Exactly 2 | More than 2 |
| Minimum value | `2` | `4` |
| Example | `2, 3, 5, 7` | `4, 6, 8, 9` |
| Divisible by | `1` and itself | At least one additional number |

> [!tip] Fast Recognition
> For `n > 1`:
>
> **Exactly 2 factors → Prime**
>
> **More than 2 factors → Composite**

---

# 6. Factors of a Number

A factor is a number that divides another number exactly.

Example:

Factors of `12`:

$$
1,2,3,4,6,12
$$

Because:

$$
12\div1=12
$$

$$
12\div2=6
$$

$$
12\div3=4
$$

and so on.

Therefore:

$$
\boxed{\text{Factors divide a number exactly}}
$$

---

# 7. Prime Factor

A prime factor is a factor that is itself prime.

Example:

Factors of `12`:

$$
1,2,3,4,6,12
$$

Prime factors:

$$
\boxed{2,3}
$$

Therefore:

$$
12=2\times2\times3
$$

or:

$$
\boxed{12=2^2\times3}
$$

---

# 8. Prime Factorization

Prime factorization means expressing a number as a product of prime numbers.

### Example

Find the prime factorization of `60`.

Start dividing by the smallest prime:

$$
60=2\times30
$$

$$
=2\times2\times15
$$

$$
=2\times2\times3\times5
$$

Therefore:

$$
\boxed{60=2^2\times3\times5}
$$

> [!important] Pattern
> Every integer greater than `1` can be expressed as a product of prime numbers.

This is called the **Fundamental Theorem of Arithmetic**.

---

# 9. Divisibility Test for Prime Numbers

To determine whether a number `n` is prime, you only need to test divisibility by prime numbers up to:

$$
\boxed{\sqrt n}
$$

### Example

Determine whether `29` is prime.

Calculate:

$$
\sqrt{29}\approx5.38
$$

Prime numbers up to `5.38`:

$$
2,3,5
$$

Check:

- `29` is not divisible by `2`
- `29` is not divisible by `3`
- `29` is not divisible by `5`

Therefore:

$$
\boxed{29\text{ is prime}}
$$

> [!tip] Important Shortcut
> **To check if `n` is prime, test only prime divisors ≤ `√n`.**

---

# 10. Why Only `√n`?

Suppose:

$$
n=a\times b
$$

If both `a` and `b` were greater than:

$$
\sqrt n
$$

then:

$$
a\times b>n
$$

which is impossible.

Therefore, if a number is composite, at least one of its factors must be:

$$
\boxed{\leq\sqrt n}
$$

This is why checking divisors only up to `√n` is sufficient.

---

# 11. Common Prime Numbers

> [!important] Must Know

The first few prime numbers are:

$$
\boxed{
2,3,5,7,11,13,17,19,23,29,
31,37,41,43,47
}
$$

Continue:

$$
53,59,61,67,71,73,79,83,89,97
$$

It is useful to memorize prime numbers at least up to `100`.

---

# 12. Important Pattern: Prime Numbers Greater Than 2

Every prime number greater than `2` is odd.

Why?

Every even number greater than `2` is divisible by `2`.

Therefore it has at least three factors:

$$
1,2,n
$$

So it cannot be prime.

Hence:

$$
\boxed{\text{Every prime number greater than 2 is odd}}
$$

> [!warning] Exception
> `2` is the only even prime number.

---

# 13. Important Pattern: Prime Numbers Ending in 5

The only prime number ending in `5` is:

$$
\boxed{5}
$$

Why?

Any larger number ending in `5` is divisible by `5`.

Examples:

$$
15,25,35,45,55,\ldots
$$

are composite.

Therefore:

$$
\boxed{\text{Prime } >5\text{ cannot end in }0\text{ or }5}
$$

---

# 14. Last-Digit Elimination

For a number greater than `5` to be prime, its last digit must be one of:

$$
\boxed{1,3,7,9}
$$

Why?

It cannot end in:

- `0` → divisible by `10`
- `2` → even
- `4` → even
- `5` → divisible by `5`
- `6` → even
- `8` → even

> [!tip] Fast Filter
> For a number greater than `5`:
>
> **Last digit must be `1, 3, 7, or 9` to even have a chance of being prime.**

> [!warning] Important
> Ending in `1, 3, 7, or 9` does **not guarantee** that a number is prime.

Example:

$$
21
$$

ends in `1`, but:

$$
21=3\times7
$$

so it is composite.

---

# 15. Number of Factors of a Prime

A prime number has exactly:

$$
\boxed{2}
$$

positive factors.

For prime `p`:

$$
\boxed{d(p)=2}
$$

where `d(n)` represents the number of positive factors.

---

# 16. Number of Factors Using Prime Factorization

Suppose:

$$
n=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

Then the number of positive factors is:

$$
\boxed{d(n)=(a_1+1)(a_2+1)\cdots(a_k+1)}
$$

### Example

Find the number of factors of:

$$
72
$$

Prime factorization:

$$
72=2^3\times3^2
$$

Therefore:

$$
d(72)=(3+1)(2+1)
$$

$$
=4\times3
$$

$$
\boxed{12}
$$

So `72` has `12` positive factors.

---

# 17. Perfect Square Factor Pattern

If:

$$
n=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

then `n` is a perfect square if and only if **all exponents are even**.

### Example

$$
144=2^4\times3^2
$$

All exponents are even.

Therefore:

$$
\boxed{144\text{ is a perfect square}}
$$

### Example

$$
72=2^3\times3^2
$$

The exponent of `2` is odd.

Therefore:

$$
\boxed{72\text{ is not a perfect square}}
$$

---

# 18. Important Aptitude Patterns

## Pattern 1 — Prime or Composite?

### Question

Is `37` prime or composite?

Calculate:

$$
\sqrt{37}\approx6.08
$$

Test prime numbers up to `6.08`:

$$
2,3,5
$$

`37` is not divisible by any of them.

Therefore:

$$
\boxed{37\text{ is prime}}
$$

---

## Pattern 2 — Quickly Identify Composite

### Question

Is `91` prime?

Check divisibility by small primes.

$$
91=7\times13
$$

Therefore:

$$
\boxed{91\text{ is composite}}
$$

> [!tip] Pattern
> Finding **one factor other than `1` and itself** is enough to prove a number is composite.

---

## Pattern 3 — Prime Factorization

### Question

Find the prime factorization of `180`.

$$
180=18\times10
$$

$$
=(2\times3^2)(2\times5)
$$

Therefore:

$$
\boxed{180=2^2\times3^2\times5}
$$

---

## Pattern 4 — Number of Factors

### Question

Find the number of positive factors of `180`.

Prime factorization:

$$
180=2^2\times3^2\times5^1
$$

Therefore:

$$
d(180)=(2+1)(2+1)(1+1)
$$

$$
=3\times3\times2
$$

$$
\boxed{18}
$$

---

## Pattern 5 — Sum of Factors

If:

$$
n=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

then the sum of positive factors is:

$$
\boxed{
\sigma(n)=
\frac{p_1^{a_1+1}-1}{p_1-1}
\times
\frac{p_2^{a_2+1}-1}{p_2-1}
\times\cdots
}
$$

### Example

For:

$$
12=2^2\times3
$$

Sum of factors:

$$
\sigma(12)
=
(1+2+4)(1+3)
$$

$$
=7\times4
$$

$$
\boxed{28}
$$

Check:

$$
1+2+3+4+6+12=28
$$

---

# 19. Product of Factors

For a positive integer `n` having `d(n)` positive factors, the product of all its positive factors is:

$$
\boxed{n^{d(n)/2}}
$$

### Example

For:

$$
12
$$

Number of factors:

$$
d(12)=6
$$

Therefore:

$$
\text{Product}
=
12^{6/2}
$$

$$
=12^3
$$

$$
\boxed{1728}
$$

---

# 20. Factor Pair Pattern

Factors often occur in pairs.

For `36`:

$$
1\times36
$$

$$
2\times18
$$

$$
3\times12
$$

$$
4\times9
$$

$$
6\times6
$$

Therefore:

$$
\boxed{(1,36),(2,18),(3,12),(4,9),(6,6)}
$$

> [!important] Perfect Square Pattern
> A perfect square has one factor pair where both factors are equal.
>
> Example:
>
> $$6\times6=36$$

---

# 21. Prime Factorization and HCF

If:

$$
a=2^3\times3^2\times5
$$

and:

$$
b=2^2\times3^3\times7
$$

Then HCF uses the **minimum exponent** of common prime factors.

Common primes:

$$
2,3
$$

Therefore:

$$
\operatorname{HCF}(a,b)
=
2^2\times3^2
$$

$$
\boxed{\operatorname{HCF}(a,b)=36}
$$

> [!tip] Pattern
> **HCF → Minimum powers of common primes.**

---

# 22. Prime Factorization and LCM

For the same numbers:

$$
a=2^3\times3^2\times5
$$

$$
b=2^2\times3^3\times7
$$

LCM uses the **maximum exponent** of every prime appearing.

Therefore:

$$
\operatorname{LCM}(a,b)
=
2^3\times3^3\times5\times7
$$

> [!tip] Pattern
> **LCM → Maximum powers of all primes.**

---

# 23. Important Formula Sheet

> [!important] Must Remember

| Concept | Formula / Rule |
|---|---|
| Prime number | Exactly 2 positive factors |
| Composite number | More than 2 positive factors |
| `1` | Neither prime nor composite |
| `2` | Only even prime |
| Prime test | Check prime divisors up to `√n` |
| Even prime | Only `2` |
| Prime `> 5` last digit | `1, 3, 7, 9` |
| Prime factorization | Product of prime powers |
| Number of factors | `(a₁+1)(a₂+1)...` |
| Sum of factors | Product of geometric-sum terms |
| Product of factors | `n^(d(n)/2)` |
| HCF using prime factors | Minimum common powers |
| LCM using prime factors | Maximum powers |

---

# 24. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Thinking `1` is prime.
- ❌ Thinking `2` is composite because it is even.
- ❌ Thinking every odd number is prime.
- ❌ Thinking a number ending in `1,3,7,9` is automatically prime.
- ❌ Testing every number up to `n` for primality.
- ❌ Forgetting to check divisors only up to `√n`.
- ❌ Confusing prime factors with all factors.
- ❌ Using maximum powers for HCF.
- ❌ Using minimum powers for LCM.
- ❌ Forgetting that perfect squares have an odd number of positive factors.

---

# 25. Exam Strategy

> [!tip] Fast Approach

When asked whether a number is prime:

1. If `n ≤ 1` → not prime.
2. If `n = 2` → prime.
3. If `n > 2` and even → composite.
4. Check divisibility by `3` and `5`.
5. Continue with prime divisors only.
6. Stop at:
   $$\sqrt n$$
7. If no divisor exists → prime.

### For Factor Questions

1. Prime-factorize the number.
2. Write the powers.
3. Apply:
   $$d(n)=(a_1+1)(a_2+1)\cdots$$
4. For HCF → minimum powers.
5. For LCM → maximum powers.

---

# 26. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Prime vs composite
2. Special cases `0`, `1`, and `2`
3. Prime-number recognition
4. Prime test using `√n`
5. Prime factorization
6. Number of factors
7. Factor pairs
8. HCF using prime factorization
9. LCM using prime factorization
10. Perfect-square factor patterns

---

# 27. Practice Checklist

- [ ] Memorize the definition of prime
- [ ] Memorize the definition of composite
- [ ] Remember `1` is neither
- [ ] Remember `2` is the only even prime
- [ ] Memorize primes up to `100`
- [ ] Practice the `√n` prime test
- [ ] Practice prime factorization
- [ ] Practice factor counting
- [ ] Practice factor-pair questions
- [ ] Practice HCF using prime factors
- [ ] Practice LCM using prime factors
- [ ] Practice perfect-square patterns
- [ ] Revise common traps

---

# 28. Related Topics

- [[01. Number System]]
- [[Natural Numbers]]
- [[Whole Numbers]]
- [[Integers]]
- [[Factors]]
- [[Multiples]]
- [[Divisibility Rules]]
- [[HCF]]
- [[LCM]]
- [[Perfect Squares]]
- [[Remainders]]

---

# 29. Quick Revision

> [!summary] One-Minute Revision

### Prime

$$
\boxed{\text{Exactly 2 positive factors}}
$$

### Composite

$$
\boxed{\text{More than 2 positive factors}}
$$

### Special Numbers

$$
\boxed{1=\text{Neither prime nor composite}}
$$

$$
\boxed{2=\text{Only even prime}}
$$

### Prime Test

$$
\boxed{\text{Check prime divisors }\leq\sqrt n}
$$

### Prime Factorization

$$
\boxed{n=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}}
$$

### Number of Factors

$$
\boxed{d(n)=(a_1+1)(a_2+1)\cdots(a_k+1)}
$$

### HCF

$$
\boxed{\text{Minimum common powers}}
$$

### LCM

$$
\boxed{\text{Maximum powers}}
$$

### Prime `> 5`

> Last digit must be `1`, `3`, `7`, or `9` to have a chance of being prime.

### Key Pattern

> **To prove a number is composite, finding just ONE divisor other than `1` and itself is enough.**