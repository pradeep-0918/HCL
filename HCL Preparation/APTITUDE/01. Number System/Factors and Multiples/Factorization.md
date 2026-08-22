---
type: concept
subject: aptitude
topic: "Factorization"
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
  - factorization
  - prime-factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Factors and Multiples]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Number of Factors]]"
  - "[[Sum of Factors]]"
  - "[[Product of Factors]]"
  - "[[HCF]]"
  - "[[LCM]]"
  - "[[Prime and Composite Numbers]]"
---

# Factorization

## 1. Core Concept

> [!summary] Definition
> **Factorization** means expressing a number or algebraic expression as a product of smaller factors.

For aptitude, the most important type is **prime factorization**.

### Example

$$
60=2\times2\times3\times5
$$

Therefore:

$$
\boxed{60=2^2\times3\times5}
$$

This is the prime factorization of `60`.

---

# 2. What Is Prime Factorization?

Prime factorization means expressing a positive integer as a product of **prime numbers only**.

### Example

$$
84
$$

Divide by `2`:

$$
84=2\times42
$$

Again:

$$
42=2\times21
$$

Then:

$$
21=3\times7
$$

Therefore:

$$
\boxed{84=2^2\times3\times7}
$$

---

# 3. Fundamental Theorem of Arithmetic

> [!important] Core Property
> Every integer greater than `1` can be expressed as a product of prime numbers, and this representation is unique apart from the order of the primes.

For example:

$$
60=2^2\times3\times5
$$

You cannot obtain a different set of prime factors for `60`.

Therefore:

$$
\boxed{\text{Prime factorization is unique}}
$$

---

# 4. Basic Factorization Method

To factorize a number:

### Step 1

Start with the smallest prime:

$$
2
$$

### Step 2

Keep dividing while divisible.

### Step 3

Move to:

$$
3,5,7,11,\ldots
$$

### Step 4

Stop when the remaining number is prime.

---

# 5. Example — 120

Start:

$$
120\div2=60
$$

Again:

$$
60\div2=30
$$

Again:

$$
30\div2=15
$$

Now `15` is divisible by `3`:

$$
15\div3=5
$$

`5` is prime.

Therefore:

$$
\boxed{120=2^3\times3\times5}
$$

---

# 6. Example — 360

$$
360\div2=180
$$

$$
180\div2=90
$$

$$
90\div2=45
$$

$$
45\div3=15
$$

$$
15\div3=5
$$

Therefore:

$$
\boxed{360=2^3\times3^2\times5}
$$

---

# 7. Factor Tree Method

Another method is the **factor tree**.

For:

$$
60
$$

we can write:

$$
60=6\times10
$$

Then:

$$
6=2\times3
$$

and:

$$
10=2\times5
$$

Therefore:

$$
60=2\times3\times2\times5
$$

So:

$$
\boxed{60=2^2\times3\times5}
$$

> [!tip] Aptitude Tip
> You can use repeated division or a factor tree. Repeated division is usually faster in exams.

---

# 8. Prime Factorization and Number of Factors

Factorization is the foundation of the number-of-factors formula.

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
360=2^3\times3^2\times5
$$

Therefore:

$$
\tau(360)
=
(3+1)(2+1)(1+1)
$$

$$
=24
$$

---

# 9. Factorization and Sum of Factors

The same prime factorization gives:

$$
\boxed{
\sigma(N)
=
\prod
(1+p+p^2+\cdots+p^a)
}
$$

### Example

For:

$$
360=2^3\times3^2\times5
$$

we get:

$$
\sigma(360)
=
(1+2+4+8)
(1+3+9)
(1+5)
$$

$$
=15\times13\times6
$$

$$
\boxed{1170}
$$

---

# 10. Factorization and Product of Factors

After finding:

$$
\tau(N)
$$

the product of all positive factors is:

$$
\boxed{
N^{\tau(N)/2}
}
$$

### Example

For:

$$
360
$$

we found:

$$
\tau(360)=24
$$

Therefore:

$$
P(360)=360^{12}
$$

---

# 11. Factorization and HCF

For HCF, use the **common prime factors with the smallest powers**.

### Example

Find:

$$
\operatorname{HCF}(60,84)
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
2,3
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

# 12. Factorization and LCM

For LCM, use **all prime factors with the largest powers**.

Using:

$$
60=2^2\times3\times5
$$

and:

$$
84=2^2\times3\times7
$$

Take:

$$
2^2,\ 3,\ 5,\ 7
$$

Therefore:

$$
\operatorname{LCM}(60,84)
=
2^2\times3\times5\times7
$$

$$
\boxed{420}
$$

> [!important] Golden Difference
>
> **HCF → minimum powers**
>
> **LCM → maximum powers**

---

# 13. Prime Factorization of a Product

If:

$$
A=2^a3^b
$$

and:

$$
B=2^c3^d
$$

then:

$$
AB=2^{a+c}3^{b+d}
$$

### Example

$$
12=2^2\times3
$$

$$
18=2\times3^2
$$

Therefore:

$$
12\times18
=
2^{2+1}\times3^{1+2}
$$

$$
=2^3\times3^3
$$

$$
\boxed{216}
$$

---

# 14. Prime Factorization of a Quotient

When division is possible:

$$
\frac{p^a}{p^b}=p^{a-b}
$$

### Example

$$
\frac{2^5\times3^4}{2^2\times3}
$$

Subtract exponents:

$$
2^{5-2}\times3^{4-1}
$$

$$
=2^3\times3^3
$$

$$
\boxed{216}
$$

> [!important] Pattern
> Multiplication → **add exponents**.
>
> Division → **subtract exponents**.

---

# 15. Factorization and Perfect Squares

A number is a perfect square if every prime exponent is even.

### Example

$$
144=2^4\times3^2
$$

Both exponents are even.

Therefore:

$$
\boxed{144\text{ is a perfect square}}
$$

---

# 16. Factorization and Perfect Cubes

A number is a perfect cube if every prime exponent is divisible by `3`.

### Example

$$
216=2^3\times3^3
$$

Therefore:

$$
\boxed{216\text{ is a perfect cube}}
$$

---

# 17. Perfect Square — Fast Test

Suppose:

$$
N=2^a3^b5^c
$$

Then `N` is a perfect square if:

$$
\boxed{a,b,c\text{ are all even}}
$$

### Example

$$
900=2^2\times3^2\times5^2
$$

All exponents are even.

Therefore:

$$
\boxed{900\text{ is a perfect square}}
$$

---

# 18. Perfect Cube — Fast Test

Suppose:

$$
N=2^a3^b5^c
$$

Then `N` is a perfect cube if:

$$
\boxed{a,b,c\text{ are all multiples of 3}}
$$

### Example

$$
1000=2^3\times5^3
$$

Therefore:

$$
\boxed{1000\text{ is a perfect cube}}
$$

---

# 19. Smallest Number to Multiply to Make a Square

This is a very common aptitude pattern.

Suppose:

$$
N=2^3\times3^2\times5
$$

To make `N` a perfect square, every exponent must become even.

Current exponents:

$$
3,\ 2,\ 1
$$

The odd exponents are:

$$
3,\ 1
$$

Multiply by:

$$
2\times5
$$

Therefore:

$$
\boxed{10}
$$

is the smallest number needed.

Check:

$$
N\times10
=
2^4\times3^2\times5^2
$$

All exponents are even.

---

# 20. Smallest Number to Divide to Make a Square

Suppose:

$$
N=2^5\times3^2\times5^3
$$

To obtain a perfect square by division, remove one `2` and one `5`:

$$
2^5\rightarrow2^4
$$

$$
5^3\rightarrow5^2
$$

Therefore divide by:

$$
\boxed{2\times5=10}
$$

Then:

$$
\frac N{10}
=
2^4\times3^2\times5^2
$$

which is a perfect square.

---

# 21. Smallest Number to Multiply to Make a Cube

For a perfect cube, every exponent must be a multiple of `3`.

Suppose:

$$
N=2^4\times3^2\times5
$$

We need:

### For `2⁴`

Next multiple of `3`:

$$
6
$$

Need:

$$
2^2
$$

### For `3²`

Need:

$$
3^1
$$

### For `5¹`

Need:

$$
5^2
$$

Therefore multiply by:

$$
2^2\times3\times5^2
$$

$$
=4\times3\times25
$$

$$
\boxed{300}
$$

---

# 22. Highest Power of a Prime Dividing N

This is another important factorization pattern.

Suppose:

$$
N=2^5\times3^2\times5
$$

The highest power of `2` dividing `N` is:

$$
\boxed{2^5}
$$

The highest power of `3` dividing `N` is:

$$
\boxed{3^2}
$$

The highest power of `5` dividing `N` is:

$$
\boxed{5}
$$

The exponent tells you the maximum power of that prime contained in `N`.

---

# 23. Number of Trailing Zeros

Trailing zeros come from factors of:

$$
10=2\times5
$$

Therefore the number of trailing zeros in a product depends on:

$$
\boxed{\min(v_2,v_5)}
$$

where:

- `v₂` = exponent of `2`
- `v₅` = exponent of `5`

### Example

$$
N=2^7\times5^3
$$

Number of trailing zeros:

$$
\min(7,3)
$$

$$
\boxed{3}
$$

---

# 24. Factorization of 100!

This is an advanced but important pattern.

To find the exponent of a prime `p` in:

$$
n!
$$

use:

$$
\boxed{
v_p(n!)
=
\left\lfloor\frac np\right\rfloor
+
\left\lfloor\frac n{p^2}\right\rfloor
+
\left\lfloor\frac n{p^3}\right\rfloor
+\cdots
}
$$

until the power exceeds `n`.

### Example

Find the exponent of `5` in `100!`.

$$
\left\lfloor\frac{100}{5}\right\rfloor=20
$$

$$
\left\lfloor\frac{100}{25}\right\rfloor=4
$$

$$
\left\lfloor\frac{100}{125}\right\rfloor=0
$$

Therefore:

$$
20+4
$$

$$
\boxed{24}
$$

---

# 25. Trailing Zeros of 100!

Since factors of `2` occur much more frequently than factors of `5`, the number of trailing zeros is controlled by the number of `5`s.

For:

$$
100!
$$

we have:

$$
v_5(100!)=24
$$

Therefore:

$$
\boxed{100!\text{ has 24 trailing zeros}}
$$

---

# 26. Number of Factors of n!

To find the number of factors of a factorial:

### Step 1

Prime factorize `n!`.

### Step 2

Find each prime exponent using Legendre's formula.

### Step 3

Apply:

$$
\boxed{
\tau(n!)=\prod(v_p(n!)+1)
}
$$

This is an advanced aptitude pattern.

---

# 27. Greatest Power of a Number Dividing N

Suppose:

$$
N=2^7\times3^4\times5^2
$$

Find the greatest power of `6` dividing `N`.

Since:

$$
6=2\times3
$$

we need equal powers of `2` and `3`.

We have:

$$
v_2=7
$$

and:

$$
v_3=4
$$

Therefore the limiting exponent is:

$$
\min(7,4)=4
$$

Hence:

$$
\boxed{6^4}
$$

is the greatest power of `6` dividing `N`.

---

# 28. Greatest Power of 12 Dividing N

Suppose:

$$
N=2^8\times3^5\times5^2
$$

Since:

$$
12=2^2\times3
$$

For:

$$
12^k
$$

we need:

$$
2^{2k}\times3^k
$$

Therefore:

$$
2k\le8
$$

giving:

$$
k\le4
$$

and:

$$
k\le5
$$

from the power of `3`.

Therefore:

$$
\boxed{k=4}
$$

So the greatest power is:

$$
\boxed{12^4}
$$

---

# 29. HCF Through Prime Factorization

For:

$$
A=p_1^{a_1}p_2^{a_2}\cdots
$$

and:

$$
B=p_1^{b_1}p_2^{b_2}\cdots
$$

the HCF is:

$$
\boxed{
\operatorname{HCF}(A,B)
=
\prod p_i^{\min(a_i,b_i)}
}
$$

---

# 30. LCM Through Prime Factorization

The LCM is:

$$
\boxed{
\operatorname{LCM}(A,B)
=
\prod p_i^{\max(a_i,b_i)}
}
$$

> [!important] Golden Memory Trick
>
> **HCF → minimum exponent**
>
> **LCM → maximum exponent**

---

# 31. Example — HCF and LCM Together

Let:

$$
A=2^3\times3^2\times5
$$

and:

$$
B=2^2\times3\times5^2
$$

### HCF

Take minimum powers:

$$
2^2\times3\times5
$$

Therefore:

$$
\boxed{\operatorname{HCF}=60}
$$

### LCM

Take maximum powers:

$$
2^3\times3^2\times5^2
$$

Therefore:

$$
\boxed{\operatorname{LCM}=1800}
$$

---

# 32. Divisibility Using Prime Factorization

A number:

$$
A
$$

divides another number:

$$
B
$$

if every prime exponent in `A` is less than or equal to the corresponding exponent in `B`.

### Example

Does:

$$
12=2^2\times3
$$

divide:

$$
72=2^3\times3^2
$$

Compare exponents:

$$
2\le3
$$

and:

$$
1\le2
$$

Therefore:

$$
\boxed{12\mid72}
$$

---

# 33. When Does A Divide B?

If:

$$
A=p_1^{a_1}p_2^{a_2}\cdots
$$

and:

$$
B=p_1^{b_1}p_2^{b_2}\cdots
$$

then:

$$
\boxed{
A\mid B
\iff
a_i\le b_i
\text{ for every prime }p_i
}
$$

This is one of the most powerful uses of prime factorization.

---

# 34. Number of Divisors of a Factorial

For:

$$
n!
$$

prime factorize it using:

$$
v_p(n!)
=
\sum_{k\ge1}
\left\lfloor\frac n{p^k}\right\rfloor
$$

Then:

$$
\boxed{
\tau(n!)
=
\prod_p
\left(v_p(n!)+1\right)
}
$$

This pattern is more advanced and is usually used in higher-level aptitude problems.

---

# 35. Common Factorization Patterns

> [!important] Must Master

### Pattern 1 — Product

$$
p^a\times p^b=p^{a+b}
$$

### Pattern 2 — Division

$$
\frac{p^a}{p^b}=p^{a-b}
$$

### Pattern 3 — Square

All exponents even.

### Pattern 4 — Cube

All exponents multiples of `3`.

### Pattern 5 — HCF

Minimum exponents.

### Pattern 6 — LCM

Maximum exponents.

### Pattern 7 — Divisibility

Every exponent in divisor ≤ corresponding exponent in dividend.

### Pattern 8 — Trailing Zeros

Count pairs of:

$$
2\times5
$$

### Pattern 9 — Number of Factors

Add `1` to exponents and multiply.

### Pattern 10 — Sum of Factors

Use geometric sums.

---

# 36. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Stopping factorization before reaching prime factors.
- ❌ Forgetting repeated prime powers.
- ❌ Using minimum exponents for LCM.
- ❌ Using maximum exponents for HCF.
- ❌ Checking only one prime when testing divisibility.
- ❌ Forgetting that perfect squares require all even exponents.
- ❌ Forgetting that perfect cubes require exponents divisible by `3`.
- ❌ Counting trailing zeros using only the number of `5`s without considering available `2`s.
- ❌ Expanding huge numbers unnecessarily.
- ❌ Confusing prime factorization with ordinary factorization.

---

# 37. Exam Strategy

> [!tip] Fast Decision Tree

### "Factorize N"

Use repeated division by:

$$
2,3,5,7,11,\ldots
$$

### "Number of factors"

Use:

$$
\boxed{\prod(a_i+1)}
$$

### "Sum of factors"

Use:

$$
\boxed{
\prod\frac{p_i^{a_i+1}-1}{p_i-1}
}
$$

### "Product of factors"

Use:

$$
\boxed{N^{\tau(N)/2}}
$$

### "HCF"

Use:

$$
\boxed{\min\text{ exponents}}
$$

### "LCM"

Use:

$$
\boxed{\max\text{ exponents}}
$$

### "Make it a square"

Make every exponent even.

### "Make it a cube"

Make every exponent a multiple of `3`.

### "Trailing zeros"

Count pairs of:

$$
2\text{ and }5
$$

---

# 38. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

Factorization is the **foundation** for the entire Factors and Multiples section.

### Master These First

1. Prime factorization
2. Factor trees
3. Exponent representation
4. Number of factors
5. Sum of factors
6. Product of factors
7. HCF using prime powers
8. LCM using prime powers
9. Perfect-square conditions
10. Perfect-cube conditions
11. Divisibility using exponents
12. Trailing-zero patterns

---

# 39. Practice Checklist

- [ ] Prime-factorize small numbers
- [ ] Prime-factorize large numbers
- [ ] Convert factorization into exponent form
- [ ] Find number of factors
- [ ] Find sum of factors
- [ ] Find product of factors
- [ ] Find HCF using prime powers
- [ ] Find LCM using prime powers
- [ ] Test divisibility using exponents
- [ ] Make numbers perfect squares
- [ ] Make numbers perfect cubes
- [ ] Find highest power of a prime
- [ ] Find highest power of a composite number
- [ ] Practice trailing-zero problems
- [ ] Revise all exponent patterns

---

# 40. Related Topics

- [[Factors and Multiples]]
- [[Factors]]
- [[Multiples]]
- [[Number of Factors]]
- [[Sum of Factors]]
- [[Product of Factors]]
- [[HCF]]
- [[LCM]]
- [[Prime and Composite Numbers]]
- [[Divisibility Rules]]
- [[Remainders]]

---

# 41. Quick Revision

> [!summary] One-Minute Revision

### Prime Factorization

$$
\boxed{
N=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
}
$$

### Number of Factors

$$
\boxed{
\tau(N)=\prod(a_i+1)
}
$$

### Sum of Factors

$$
\boxed{
\sigma(N)
=
\prod
\frac{p_i^{a_i+1}-1}{p_i-1}
}
$$

### Product of Factors

$$
\boxed{
P(N)=N^{\tau(N)/2}
}
$$

### HCF

$$
\boxed{\min\text{ exponents}}
$$

### LCM

$$
\boxed{\max\text{ exponents}}
$$

### Perfect Square

$$
\boxed{\text{All exponents even}}
$$

### Perfect Cube

$$
\boxed{\text{All exponents divisible by 3}}
$$

### Divisibility

$$
\boxed{
A\mid B
\iff
\text{every exponent of A}\le\text{corresponding exponent of B}
}
$$

### Trailing Zeros

$$
\boxed{
\min(v_2,v_5)
}
$$

### Golden Memory Trick

> **Prime factorization is the master key.**
>
> Once you have:
>
> $$N=p_1^{a_1}p_2^{a_2}\cdots$$
>
> you can solve **factor count, factor sum, factor product, HCF, LCM, divisibility, squares, cubes, and many remainder problems.**